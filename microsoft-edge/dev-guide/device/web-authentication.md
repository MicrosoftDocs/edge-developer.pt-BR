---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Saiba como a API de autenticação da Web pode ser usada para permitir que os aplicativos da Web usem a biometria do Windows Hello para autenticação do usuário.
title: Guia de desenvolvimento-autenticação na Web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: c49d181633ae1b2b35aa0f88287841d28e806f44
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560563"
---
# Autenticação da Web e Windows Hello

A API da autenticação da Web (anteriormente *FIDO 2,0* ) no Microsoft Edge permite que os aplicativos da Web usem a biometria do [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) para autenticação de usuário, para que você e seus usuários possam evitar todas as complicações e riscos de gerenciamento de senhas, incluindo adivinhação de senha, phishing e ataques de registro em log. A implementação atual do Microsoft Edge (*MS-* prefixado) se baseia em um rascunho anterior da especificação de autenticação da Web e provavelmente mudará no futuro. **Este tópico mostrará como experimentar a autenticação do Windows Hello com o Microsoft Edge e, além disso, passará o seu código para a atualização do navegador para o futuro.**

A API de autenticação da Web é um padrão emergente colocado pela [Fido Alliance](https://fidoalliance.org/) com o objetivo de fornecer uma maneira interoperável de fazer autenticação na Web usando o Windows Hello e outros dispositivos biométricos entre navegadores. A especificação de autenticação da Web define dois cenários de autenticação: menos por senha e dois fatores. No caso sem senha, o usuário não precisa fazer logon na página da Web usando um nome de usuário ou senha – eles podem fazer logon unicamente usando o Windows Hello. No caso de dois fatores, o usuário faz logon normalmente usando um nome de usuário e uma senha, mas o Windows Hello é usado como um segundo fator para dar a autenticação geral mais forte.

Usando a autenticação da Web combinada com o Windows Hello, o servidor envia um desafio de texto sem formatação para o navegador. Depois que o Microsoft Edge for capaz de verificar o usuário por meio do Windows Hello, o sistema assinará o desafio com uma chave privada fornecida anteriormente para este usuário e enviar a assinatura de volta para o servidor. Se o servidor puder validar a assinatura usando a chave pública que ele tem para o usuário e verificar se o desafio está correto, ele pode autenticar o usuário com segurança. Com a [criptografia assimétrica](https://en.wikipedia.org/wiki/Public-key_cryptography) , como isso, a chave pública não tem significado algum e a chave privada nunca é compartilhada. Além disso, a chave privada nunca pode ser movida de sistemas modernos com hardware compatível com TPM.

Há duas etapas básicas para usar a API de autenticação da Web:

**1. Registre seu usuário com `makeCredential`**

**2. autentique seu usuário com `getAssertion`**

O seguinte irá orientá-lo nesse fluxo usando o [metapreenchimento recomendado webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js). O [código completo](https://github.com/adrianba/fido-snippets/) está disponível para este servidor e demonstração do lado do cliente. Versões do lado do servidor [C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [php](https://github.com/adrianba/fido-snippets/tree/master/php)e [node. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) estão disponíveis.

## Registrar o usuário

Atuando como um *provedor de identidade*, você precisará primeiro criar uma credencial de autenticação da Web para o usuário com o Window. webauthn. método **makeCredential** . Antes de registrar essa credencial para o usuário em seu servidor, você precisará confirmar a identidade do usuário. Isso pode ser feito enviando ao usuário uma confirmação de email ou solicitando que use o método de login tradicional.

O método makeCredential tem os seguintes parâmetros:
 - **informações da conta do usuário**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **parâmetros de criptografia**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

A promessa resultante retorna um objeto que representa a credencial que você envia de volta ao servidor para validar futuras autenticações:

**Cliente**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var email = '<%=user.email%>';
    var name = '<%=user.name%>';

    webauthn.makeCredential(userAccountInformation, cryptoParams)
        .then(function (creds) {
            document.getElementById('form-id').value = creds.credential.id;
            document.getElementById('form-pk').value = JSON.stringify(creds.publicKey);
            document.getElementById('form-email').value = email;
            document.getElementById('form-name').value = name;
            document.getElementById('theform').submit();
        }).catch(function (err) {
            // No acceptable authenticator or user refused consent. Handle appropriately.
            alert(err);
        });
</script>
```

Quando você usa o método makeCredential, o Microsoft Edge primeiro pedirá que o Windows Hello use a identificação de face ou de impressão digital para verificar se o usuário é o mesmo que está conectado à conta do Windows. Depois que esta etapa for concluída, o Microsoft Passport irá gerar um par de chaves pública/privada e armazenar a chave privada no TPM (Trusted Platform Module), o hardware do processador de criptografia dedicado usado para armazenar credenciais. Se o usuário não tiver um dispositivo habilitado para TPM, essas chaves serão armazenadas em software. Essas credenciais são criadas por origem, por conta do Windows, e não serão móveis porque estão vinculadas ao dispositivo. Isso significa que você precisará verificar se o usuário está registrado para usar o Windows Hello para cada dispositivo que ele usa.

## Autenticar seu usuário

Após a criação da credencial no cliente, na próxima vez que o usuário tentar acessar o site, você poderá oferecer a assinatura usando o Windows Hello em vez de uma senha com uma chamada para Window. webauthn. **Getassertion**.

O método getassertion assume o *desafio* como o único parâmetro obrigatório. O desafio é a quantidade gerada aleatoriamente que o servidor enviará a um cliente para se conectar com a chave privada do usuário. Por exemplo:

**Servidor**

```
var crypto = require('crypto');

Strategy.prototype.generateChallenge = function() {
    return this.generateVerifiableString(crypto.randomBytes(32));
};

Strategy.prototype.generateVerifiableString = function(data) {
    // Create cipher using secret
    var d = new Buffer(data);
    var c = crypto.createCipher('aes192',new Buffer(this._secret));

    // Encrypt data
    c.update(d);

    // Hash results of encrypting data
    var hash = crypto.createHash('sha256');
    hash.update(c.final());

    // Combine original data with hash
    return d.toString('hex') + string_separator + hash.digest('hex');
};
```

Depois que a chamada getassertion for feita, o Microsoft Edge mostrará o prompt do Windows Hello, que verificará a identidade do usuário usando a biometria. Depois que o usuário for verificado, o desafio será assinado dentro do TPM e a promessa retornará com um objeto de asserção que contenha a assinatura e outros metadados para você enviar ao servidor:

**Cliente**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var challenge = '<%=challenge%>';

    webauthn.getAssertion(challenge)
    .then(function(assertion) {
      document.getElementById("form-id").value = assertion.credential.id;
      document.getElementById("form-type").value = assertion.credential.type;
      document.getElementById("form-data").value = assertion.clientData;
      document.getElementById("form-sig").value = assertion.signature;
      document.getElementById("form-authnr").value = assertion.authenticatorData;
      document.getElementById("form-challenge").value = challenge;
      document.getElementById("theform").submit();
    })
    .catch(function(err) {
      if(err && err.name) {
        document.getElementById("form-err").value = err.name;
      } else {
        document.getElementById("form-err").value = "unknown";
      }
      document.getElementById("theform").submit();
    });

</script>
```

Depois de receber a asserção no servidor, será preciso validar a assinatura para autenticar o usuário. Por exemplo (no node. JS):

**Servidor**

```
var jwkToPem = require('jwk-to-pem')
var crypto = require('crypto');

var fidoAuthenticator = {
     validateSignature: function (publicKey, clientData, authnrData, signature, challenge) {
         // Make sure the challenge in the client data
         // matches the expected challenge
         var c = new Buffer(clientData, 'base64');
         var cc = JSON.parse(c.toString().replace(/\0/g,''));
         if(cc.challenge != challenge) return false;

         // Hash data with sha256
         const hash = crypto.createHash('sha256');
         hash.update(c);
         var h = hash.digest();

         // Verify signature is correct for authnrData + hash
         var verify = crypto.createVerify('RSA-SHA256');
         verify.update(new Buffer(authnrData,'base64'));
         verify.update(h);
         return verify.verify(jwkToPem(JSON.parse(publicKey)), signature, 'base64');
     }
};   
```

## Diferenças entre o Microsoft Edge e a especificação

> [!NOTE]
> Ao experimentar a API de autenticação da Web com o Windows Hello no Microsoft Edge, recomendamos usar o metapreenchimento webauthn. js, conforme mostrado acima, para evitar ter que considerar as discrepâncias listadas aqui. Atualizaremos este semipreenchimento para cada versão publicada mais importante da especificação.


A implementação atual do Microsoft Edge é baseada em um rascunho anterior da especificação de autenticação da Web e provavelmente mudará nas futuras versões e, conforme a especificação evoluir. As diferenças atuais incluem:

- As APIs do Microsoft Edge são MS-prefixadas.
- O Microsoft Edge ainda não dá suporte a credenciais externas, como chaves USB ou dispositivos Bluetooth. A API atual limita-se a credenciais inseridas armazenadas no TPM.
- A conta de usuário do Windows atualmente conectada deve ser configurada para dar suporte a pelo menos um PIN, e preferencialmente diante ou biometria de impressão digital. Isso é para garantir que o Windows possa autenticar o acesso ao TPM.
- A implementação do Microsoft Edge ainda não dá suporte à experiência do seletor de conta.
- Um segundo parâmetro de *filtros* especificando a ID de credencial é atualmente necessário para chamadas para msCredentials. [Getassertion](https://msdn.microsoft.com/library/mt697640). Assim, você precisará armazenar suas informações de identificação de credenciais no armazenamento local do cliente, no indexDB ou no localStorage, ao fazer uma credencial. Se um usuário excluir seu histórico de navegação, incluindo armazenamento local, será necessário registrá-lo novamente para usar o Windows Hello da próxima vez que fizerem logon.
- O Microsoft Edge não oferece suporte a todas as opções no rascunho de especificação de autenticação da Web atual, como extensões ou tempos limite.

Nesse último ponto, as diferenças específicas do Microsoft Edge são observadas nas seguintes definições de especificação de autenticação da Web:

### Especificação do W3C

```
partial interface Window {
    readonly attribute WebAuthentication webauthn; // msCredentials
};

interface WebAuthentication { // MSCredentials
    Promise <ScopedCredentialInfo> makeCredential (
        Account                                 accountInformation,
        sequence <ScopedCredentialParameters>   cryptoParameters,
        DOMString                               attestationChallenge, // Optional in Microsoft Edge
        optional unsigned long                  credentialTimeoutSeconds, // Not yet supported
        optional sequence <Credential>          blacklist, // Not yet supported
        optional WebAuthnExtensions             credentialExtensions // Not yet supported
    );

    Promise <WebAuthnAssertion> getAssertion (
        DOMString                        assertionChallenge,
        optional unsigned long           assertionTimeoutSeconds, // Not yet supported
        optional sequence <Credential>   whitelist, // Not yet supported
        optional WebAuthnExtensions      assertionExtensions // Not yet supported
    );
};

interface ScopedCredentialInfo { // MSAssertion
    readonly attribute Credential           credential;
    readonly attribute any                  publicKey;
    readonly attribute AttestationStatement attestation;
};

dictionary Account { // MSAccountInfo
    required DOMString rpDisplayName;
    required DOMString displayName;
    DOMString          name; // Not yet supported
    DOMString          id; // Not yet supported
    DOMString          imageUri; // Not yet supported
};

dictionary ScopedCredentialParameters { // MSCredentialParameters
    required CredentialType        type;
    required AlgorithmIdentifier   algorithm;
};

enum CredentialType { // MSCredentialType
    "ScopedCred" // Must be "FIDO_2_0" in Microsoft Edge
};

interface Credential { // MSCredentialSpec
    readonly attribute CredentialType type;
    readonly attribute DOMString      id;
};

dictionary WebAuthnExtensions { // Not supported
};
```



## Referência da API

[MSCredentials](https://msdn.microsoft.com/library/mt697639)

[makeCredential](https://msdn.microsoft.com/library/mt697641)

[getassertion](https://msdn.microsoft.com/library/mt697640)

## Demonstrações

[Exemplos de código do cliente e do servidor](https://github.com/adrianba/fido-snippets/)

[Metapreenchimento do webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[Demonstração da unidade de teste do Windows Hello](https://testdrive-fido.azurewebsites.net/)

## Especificada

[Autenticação da Web: uma API da Web para acessar as credenciais de escopo 1](http://w3c.github.io/webauthn/)  
