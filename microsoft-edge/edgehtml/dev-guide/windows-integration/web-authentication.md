---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Saiba como a API de autenticação da Web pode permitir que os aplicativos da Web usem o Windows Hello e o FIDO2 para autenticação de usuário.
title: Autenticação da Web-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 07f1de47156f43ff4726e8907a123c2cb1afc337
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231512"
---
# Autenticação da Web e Windows Hello  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

A [API de autenticação da Web](https://w3c.github.io/webauthn) no Microsoft Edge permite que os aplicativos da Web usem dispositivos [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) e [FIDO2 externos](https://fidoalliance.org/fido2) para autenticação de usuário, para que você e seus usuários possam evitar todas as complicações e riscos de gerenciamento de senhas, incluindo adivinhação de senha, phishing e ataques de registro de chave.  A implementação atual do Microsoft Edge é baseada na recomendação de candidatos da especificação de autenticação da Web.  

> [!IMPORTANT]
> Este tópico mostra como experimentar a autenticação do Windows Hello e do FIDO2 com o Microsoft Edge.  

Usando a autenticação da Web, o servidor envia um desafio de texto sem formatação para o navegador.  Depois que o Microsoft Edge for capaz de verificar o usuário por meio do Windows Hello ou de um dispositivo de FIDO2 externo, o sistema assinará o desafio com uma chave privada fornecida anteriormente para esse usuário e enviar a assinatura de volta para o servidor.  Se o servidor puder validar a assinatura usando a chave pública que ele tem para o usuário e verificar se o desafio está correto, ele pode autenticar o usuário com segurança.  Com a [criptografia assimétrica](https://en.wikipedia.org/wiki/Public-key_cryptography) , como isso, a chave pública não tem significado algum e a chave privada nunca é compartilhada.  Além disso, a chave privada nunca pode ser movida de elementos seguros ou sistemas modernos com hardware compatível com TPM.  

Há duas etapas básicas para usar a API de autenticação da Web:  

1.  Registre seu usuário com `create`  
1.  Autentique seu usuário com `get`  

O seguinte guia de desenvolvimento orientará você nesse fluxo usando o [aplicativo de exemplo Webauthn](https://github.com/MicrosoftEdge/webauthnsample).  

## Registrar o usuário  

Atuando como um provedor de identidade, você precisará primeiro criar uma credencial de autenticação da Web para o usuário com o `navigator.credentials.create` método.  Antes de registrar essa credencial para o usuário em seu servidor, você precisará confirmar a identidade do usuário.  Isso pode ser feito enviando ao usuário uma confirmação de email ou solicitando que use o método de login tradicional.  

O `create` método usa os seguintes parâmetros:  

:::row:::
   :::column span="1":::
      **informações da terceira parte confiável**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      rp: {
          name: "WebAuthn Sample App",
          icon: "https://example.com/rpIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **informações da conta do usuário**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      user: {
          id: stringToArrayBuffer("some.user.id"),
          name: "bob.smith@contoso.com",
          displayName: "Bob Smith",
          icon: "https://example.com/userIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **parâmetros de criptografia**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      pubKeyCredParams: [
          {
              //External authenticators support the ES256 algorithm
              type: "public-key",
              alg: -7                 
          }, 
          {
              //Windows Hello supports the RS256 algorithm
              type: "public-key",
              alg: -257
          }
      ],
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **parâmetros de seleção do autenticador**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      authenticatorSelection: {
          //Select authenticators that support username-less flows
          requireResidentKey: true,
          //Select authenticators that have a second factor (such as PIN, Bio)
          userVerification: "required",
          //Selects between bound or detachable authenticators
          authenticatorAttachment: "platform"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **outras opções**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      //Select larger timeout values, as Microsoft Edge shows UI
      timeout: 50000,
      //an opaque challenge that the authenticator signs over
      challenge: challenge,
      //prevent re-registration by specifying existing credentials here
      excludeCredentials: [],
      //specifies whether you need an attestation statement
      attestation: "none" 
      ```  
   :::column-end:::
:::row-end:::  

Você pode usar os [parâmetros de criação de credenciais](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) para configurar a credencial que você deseja criar.  Em particular, você pode optar por criar uma credencial do Windows Hello Configurando `authenticatorAttachment` para `platform` ou uma credencial de roaming em um dispositivo de FIDO2 externo definindo `authenticatorAttachment` como `cross-platform` .  

Quando você usa o `create` método, o Microsoft Edge pede primeiro que o usuário Verifique sua presença digitalizando a face ou a impressão digital, inserindo um PIN ou executando uma ação em um dispositivo FIDO2 externo.  Depois que esta etapa for concluída, o autenticador gerará um par de chaves PublicPrivate e armazenará a chave privada.  Essas credenciais são criadas por origem, por conta e não podem ser extraídas porque são armazenadas de forma segura para o dispositivo de autenticação.  

A promessa resultante retorna um [objeto atestador](https://w3c.github.io/webauthn#sctn-attestation) que representa a nova credencial.  O objeto de atestado contém a chave pública da credencial.  Você enviará esse objeto ao servidor para validar futuras autenticações.  Antes de enviar de volta ao servidor, você precisará codificar os dados brutos em base64.  

**Cliente**  

```javascript
<script>
    navigator.credentials.create({
        publicKey: createCredentialOptions
    }).then(rawAttestation => {
        var attestation = {
            id: base64encode(rawAttestation.rawId),
            clientDataJSON: arrayBufferToString(rawAttestation.response.clientDataJSON),
            attestationObject: base64encode(rawAttestation.response.attestationObject)
        };
        return rest_put("/credentials", attestation);
    })
</script>
```  

Em seguida, o servidor deve decodificar o objeto de atestado, executar etapas de verificação, extrair a chave pública para esta credencial e armazená-la para autenticações futuras.  Uma lista detalhada de etapas pode ser encontrada no [algoritmo de registro de credenciais](https://w3c.github.io/webauthn#registering-a-new-credential) na especificação webauthn.  

**Servidor**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## Autenticar seu usuário  

Após a criação da credencial no cliente, na próxima vez que o usuário tentar se conectar ao site, você poderá oferecer a assinatura usando a credencial de autenticação da Web, em vez de uma senha com uma chamada para `navigator.credentials.get` .  

O `get` método assume o desafio como o único parâmetro obrigatório.  O desafio é uma sequência opaca de bytes que o servidor enviará a um cliente para assinar com a chave privada do usuário.  Por exemplo:  

**Servidor**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

Depois de recuperar um desafio do servidor, você chamará a API Get juntamente com [as opções de solicitação de credenciais](https://w3c.github.io/webauthn#credentialrequestoptions-extension).  O Microsoft Edge mostrará um prompt, que verificará a identidade do usuário usando o Windows Hello ou um dispositivo de FIDO2 externo.  Depois que o usuário for verificado, o desafio será assinado dentro do dispositivo TPM ou FIDO2 e a promessa retornará com um [objeto de asserção](https://w3c.github.io/webauthn#authenticatorassertionresponse) que contenha a assinatura e outros metadados para você enviar para o servidor.  

**Cliente**  

```javascript
    var credentialRequestOptions = {
        //specifies which credential IDs are allowed to authenticate the user
        //if empty, any credential can authenticate the users
        allowCredentials: allowCredentials,
        //an opaque challenge that the authenticator signs over
        challenge: challenge,
        //Select larger timeout values, as Microsoft Edge shows UI
        timeout: 50000
    };

    navigator.credentials.get({
        publicKey: credentialRequestOptions
    }).then(rawAssertion => {
        var assertion = {
            id: base64encode(rawAssertion.rawId),
            clientDataJSON: arrayBufferToString(rawAssertion.response.clientDataJSON),
            userHandle: base64encode(rawAssertion.response.userHandle),
            signature: base64encode(rawAssertion.response.signature),
            authenticatorData: base64encode(rawAssertion.response.authenticatorData)
        };
        return rest_put("/assertion", assertion);
    })
```  

Depois de receber a asserção no servidor, será preciso validar a assinatura para autenticar o usuário.  Veja a seguir um exemplo de código.  Uma lista detalhada de etapas pode ser encontrada no [algoritmo de verificação de asserção](https://w3c.github.io/webauthn#verifying-assertion) na especificação webauthn.  

**Servidor**  

```javascript
    var jwkToPem = require('jwk-to-pem')
    var crypto = require('crypto');

    ...

    // Using credential’s id attribute, look up the corresponding 
    // credential public key.
    var credential = await storage.Credentials.findOne({
        id: assertion.id
    });

    //Refer to sample to see how to verify client data and authenticator data

    ...

    //Using the credential public key from lookup, verify that sig is a valid
    //signature over the binary concatenation of authData and hash.
    var publicKey = credential.publicKeyJwk;
    var verify = (publicKey.kty === "RSA") ? crypto.createVerify('RSA-SHA256') : crypto.createVerify('sha256');
    verify.update(authData);
    verify.update(hash);
    if (!verify.verify(jwkToPem(publicKey), sig))
        throw new Error("Could not verify signature");

    //Verify signCount has increased or is zero 
    if (authenticatorData.signCount != 0 &&
        authenticatorData.signCount < credential.signCount) {
        throw new Error("Received signCount of " + authenticatorData.signCount +
            " expected signCount > " + credential.signCount);
    }
```  

## Notas de implementação  

### Plataformas compatíveis  

*   A versão de recomendação de candidatos da API de autenticação da Web pode ser usada do Microsoft Edge começando com o EdgeHTML 18 \ (Windows Insider Preview versão 17713 ou mais recente \).  
*   A [versão de visualização prefixada](https://blogs.windows.com/msedgedev/2016/04/12) da API de autenticação da Web foi removida e não está mais disponível.  
*   A API de autenticação da Web ainda não está disponível para aplicativos UWP e PWAs.  
*   O Internet Explorer não é compatível com a API de autenticação da Web.  

### Autenticadores com suporte  

Com a API de autenticação da Web no Microsoft Edge, você pode autenticar usuários com as seguintes tecnologias:  

*   **Windows Hello**  Habilita a autenticação no dispositivo sem senha com face, impressão digital ou PIN  
*   **FIDO2**  Habilita a autenticação de roaming sem senha com um dispositivo removível e uma impressão digital ou PIN  
*   **U2F**  Habilita a autenticação de segundo fator forte para sites que não estão prontos para serem movidos para um modelo sem senha  

### Considerações especiais para o Windows Hello  

Algumas coisas a serem observadas ao usar o autenticador Windows Hello:  

*   Você pode detectar se o Windows Hello está disponível em um computador chamando a `isUserVerifyingPlatformAuthenticatorAvailable` API.  Saiba mais sobre esta API [aqui](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).  
*   Ao criar uma credencial para o Windows Hello, você deve definir `authenticatorAttachment` para `platform` a melhor experiência do usuário.
*   O Windows Hello só dá suporte a RS256 \ (alg-257 \) como algoritmo de chave pública.  Certifique-se de especificar esse algoritmo ao criar uma credencial.  
*   Para receber uma [instrução de atestado de TPM](https://w3c.github.io/webauthn#tpm-attestation), defina atestador como "direto" ao chamar a `create` API.  O atestado TPM é um melhor esforço.  Somente os computadores com TPM 2,0 retornarão uma instrução de atestado TPM, e o processo de atestado poderá falhar por várias razões.  
*   O Windows Hello emprega diversas maneiras de proteger as credenciais do usuário.  Você pode verificar qual método foi usado para proteger uma credencial consumindo o campo [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) no objeto de atestado retornado na criação de credenciais.  Veja a seguir a lista de AAGUIDs que o Windows Hello pode retornar:   
    *   Autenticadores reproduzidos por software  
        *   Autenticador de software do Windows Hello:  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   Autenticador de software VBS do Windows Hello:  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   Autenticadores com backup do Trusted Platform Module \ (TPM \)  
        *   Autenticador de hardware do Windows Hello:  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   Autenticador de hardware do Windows Hello VBS:  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### Superfície da API  

*   O Microsoft Edge tem uma implementação completa da versão de recomendação de candidatos da especificação de autenticação da Web principal.  
*   A [extensão AppID](https://w3c.github.io/webauthn#sctn-appid-extension) tem suporte.  
*   Não há suporte para nenhuma outra extensão.  

## Demonstrações  

[Amostra de código do cliente e do servidor](https://github.com/MicrosoftEdge/webauthnsample)  

[Demonstração da unidade de teste do Windows Hello](https://webauthnsample.azurewebsites.net)  

## Especificada  

[Autenticação na Web: uma API para acessar credenciais de chave pública](http://w3c.github.io/webauthn)  
