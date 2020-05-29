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
# <span data-ttu-id="b4f84-104">Autenticação da Web e Windows Hello</span><span class="sxs-lookup"><span data-stu-id="b4f84-104">Web authentication and Windows Hello</span></span>

<span data-ttu-id="b4f84-105">A API da autenticação da Web (anteriormente *FIDO 2,0* ) no Microsoft Edge permite que os aplicativos da Web usem a biometria do [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) para autenticação de usuário, para que você e seus usuários possam evitar todas as complicações e riscos de gerenciamento de senhas, incluindo adivinhação de senha, phishing e ataques de registro em log.</span><span class="sxs-lookup"><span data-stu-id="b4f84-105">The Web Authentication (formerly *FIDO 2.0* ) API in Microsoft Edge enables web applications to use [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometrics for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and keylogging attacks.</span></span> <span data-ttu-id="b4f84-106">A implementação atual do Microsoft Edge (*MS-* prefixado) se baseia em um rascunho anterior da especificação de autenticação da Web e provavelmente mudará no futuro.</span><span class="sxs-lookup"><span data-stu-id="b4f84-106">The current Microsoft Edge (*ms-* prefixed) implementation is based on an earlier draft of the Web Authentication specification and is likely to change in the future.</span></span> **<span data-ttu-id="b4f84-107">Este tópico mostrará como experimentar a autenticação do Windows Hello com o Microsoft Edge e, além disso, passará o seu código para a atualização do navegador para o futuro.</span><span class="sxs-lookup"><span data-stu-id="b4f84-107">This topic will show you how to try out Windows Hello authentication with Microsoft Edge while also future-proofing your code against browser updates.</span></span>**

<span data-ttu-id="b4f84-108">A API de autenticação da Web é um padrão emergente colocado pela [Fido Alliance](https://fidoalliance.org/) com o objetivo de fornecer uma maneira interoperável de fazer autenticação na Web usando o Windows Hello e outros dispositivos biométricos entre navegadores.</span><span class="sxs-lookup"><span data-stu-id="b4f84-108">The Web Authentication API is an emerging standard put forth by the [FIDO Alliance](https://fidoalliance.org/) with the aim of providing an interoperable way of doing web authentication using Windows Hello and other biometric devices across browsers.</span></span> <span data-ttu-id="b4f84-109">A especificação de autenticação da Web define dois cenários de autenticação: menos por senha e dois fatores.</span><span class="sxs-lookup"><span data-stu-id="b4f84-109">The Web Authentication specification defines two authentication scenarios: password-less and two factor.</span></span> <span data-ttu-id="b4f84-110">No caso sem senha, o usuário não precisa fazer logon na página da Web usando um nome de usuário ou senha – eles podem fazer logon unicamente usando o Windows Hello.</span><span class="sxs-lookup"><span data-stu-id="b4f84-110">In the password-less case, the user does not need to log into the web page using a user name or password – they can login solely using Windows Hello.</span></span> <span data-ttu-id="b4f84-111">No caso de dois fatores, o usuário faz logon normalmente usando um nome de usuário e uma senha, mas o Windows Hello é usado como um segundo fator para dar a autenticação geral mais forte.</span><span class="sxs-lookup"><span data-stu-id="b4f84-111">In the two factor case, the user logs in normally using a username and password, but Windows Hello is used as a second factor check to make the overall authentication stronger.</span></span>

<span data-ttu-id="b4f84-112">Usando a autenticação da Web combinada com o Windows Hello, o servidor envia um desafio de texto sem formatação para o navegador.</span><span class="sxs-lookup"><span data-stu-id="b4f84-112">Using Web Authentication combined with Windows Hello, the server sends down a plain text challenge to the browser.</span></span> <span data-ttu-id="b4f84-113">Depois que o Microsoft Edge for capaz de verificar o usuário por meio do Windows Hello, o sistema assinará o desafio com uma chave privada fornecida anteriormente para este usuário e enviar a assinatura de volta para o servidor.</span><span class="sxs-lookup"><span data-stu-id="b4f84-113">Once Microsoft Edge is able to verify the user through Windows Hello, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span> <span data-ttu-id="b4f84-114">Se o servidor puder validar a assinatura usando a chave pública que ele tem para o usuário e verificar se o desafio está correto, ele pode autenticar o usuário com segurança.</span><span class="sxs-lookup"><span data-stu-id="b4f84-114">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span> <span data-ttu-id="b4f84-115">Com a [criptografia assimétrica](https://en.wikipedia.org/wiki/Public-key_cryptography) , como isso, a chave pública não tem significado algum e a chave privada nunca é compartilhada.</span><span class="sxs-lookup"><span data-stu-id="b4f84-115">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span> <span data-ttu-id="b4f84-116">Além disso, a chave privada nunca pode ser movida de sistemas modernos com hardware compatível com TPM.</span><span class="sxs-lookup"><span data-stu-id="b4f84-116">Furthermore, the private key can never be moved from modern systems with TPM-enabled hardware.</span></span>

<span data-ttu-id="b4f84-117">Há duas etapas básicas para usar a API de autenticação da Web:</span><span class="sxs-lookup"><span data-stu-id="b4f84-117">There are two basic steps to using the Web Authentication API:</span></span>

**<span data-ttu-id="b4f84-118">1. Registre seu usuário com</span><span class="sxs-lookup"><span data-stu-id="b4f84-118">1. Register your user with</span></span> `makeCredential`**

**<span data-ttu-id="b4f84-119">2. autentique seu usuário com</span><span class="sxs-lookup"><span data-stu-id="b4f84-119">2. Authenticate your user with</span></span> `getAssertion`**

<span data-ttu-id="b4f84-120">O seguinte irá orientá-lo nesse fluxo usando o [metapreenchimento recomendado webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js).</span><span class="sxs-lookup"><span data-stu-id="b4f84-120">The following will walk you through this flow using the recommended [Webauthn.js polyfill](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js).</span></span> <span data-ttu-id="b4f84-121">O [código completo](https://github.com/adrianba/fido-snippets/) está disponível para este servidor e demonstração do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="b4f84-121">The [complete code](https://github.com/adrianba/fido-snippets/) is available for this server and client side demo.</span></span> <span data-ttu-id="b4f84-122">Versões do lado do servidor [C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [php](https://github.com/adrianba/fido-snippets/tree/master/php)e [node. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b4f84-122">[C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [PHP](https://github.com/adrianba/fido-snippets/tree/master/php), and [Node.JS](https://github.com/adrianba/fido-snippets/tree/master/nodejs) server side versions are available.</span></span>

## <span data-ttu-id="b4f84-123">Registrar o usuário</span><span class="sxs-lookup"><span data-stu-id="b4f84-123">Register your user</span></span>

<span data-ttu-id="b4f84-124">Atuando como um *provedor de identidade*, você precisará primeiro criar uma credencial de autenticação da Web para o usuário com o Window. webauthn. método **makeCredential** .</span><span class="sxs-lookup"><span data-stu-id="b4f84-124">Acting as an *identity provider*, you will first need to create a Web Authentication credential for your user with the window.webauthn.**makeCredential** method.</span></span> <span data-ttu-id="b4f84-125">Antes de registrar essa credencial para o usuário em seu servidor, você precisará confirmar a identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="b4f84-125">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span> <span data-ttu-id="b4f84-126">Isso pode ser feito enviando ao usuário uma confirmação de email ou solicitando que use o método de login tradicional.</span><span class="sxs-lookup"><span data-stu-id="b4f84-126">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>

<span data-ttu-id="b4f84-127">O método makeCredential tem os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b4f84-127">The makeCredential method takes the following parameters:</span></span>
 - **<span data-ttu-id="b4f84-128">informações da conta do usuário</span><span class="sxs-lookup"><span data-stu-id="b4f84-128">user account information</span></span>**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **<span data-ttu-id="b4f84-129">parâmetros de criptografia</span><span class="sxs-lookup"><span data-stu-id="b4f84-129">crypto parameters</span></span>**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

<span data-ttu-id="b4f84-130">A promessa resultante retorna um objeto que representa a credencial que você envia de volta ao servidor para validar futuras autenticações:</span><span class="sxs-lookup"><span data-stu-id="b4f84-130">The resulting promise returns an object representing the credential that you then send back to the server for validating future authentications:</span></span>

**<span data-ttu-id="b4f84-131">Cliente</span><span class="sxs-lookup"><span data-stu-id="b4f84-131">Client</span></span>**

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

<span data-ttu-id="b4f84-132">Quando você usa o método makeCredential, o Microsoft Edge primeiro pedirá que o Windows Hello use a identificação de face ou de impressão digital para verificar se o usuário é o mesmo que está conectado à conta do Windows.</span><span class="sxs-lookup"><span data-stu-id="b4f84-132">When you use the makeCredential method, Microsoft Edge will first ask Windows Hello to use face or fingerprint identification to verify that the user is the same user as the one logged into the Windows account.</span></span> <span data-ttu-id="b4f84-133">Depois que esta etapa for concluída, o Microsoft Passport irá gerar um par de chaves pública/privada e armazenar a chave privada no TPM (Trusted Platform Module), o hardware do processador de criptografia dedicado usado para armazenar credenciais.</span><span class="sxs-lookup"><span data-stu-id="b4f84-133">Once this step is completed, Microsoft Passport will generate a public/private key pair and store the private key in the Trusted Platform Module (TPM), the dedicated crypto processor hardware used to store credentials.</span></span> <span data-ttu-id="b4f84-134">Se o usuário não tiver um dispositivo habilitado para TPM, essas chaves serão armazenadas em software.</span><span class="sxs-lookup"><span data-stu-id="b4f84-134">If the user doesn’t have a TPM enabled device, these keys will be stored in software.</span></span> <span data-ttu-id="b4f84-135">Essas credenciais são criadas por origem, por conta do Windows, e não serão móveis porque estão vinculadas ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4f84-135">These credentials are created per origin, per Windows account, and will not be roamed because they are tied to the device.</span></span> <span data-ttu-id="b4f84-136">Isso significa que você precisará verificar se o usuário está registrado para usar o Windows Hello para cada dispositivo que ele usa.</span><span class="sxs-lookup"><span data-stu-id="b4f84-136">This means that you’ll need to make sure the user registers to use Windows Hello for every device they use.</span></span>

## <span data-ttu-id="b4f84-137">Autenticar seu usuário</span><span class="sxs-lookup"><span data-stu-id="b4f84-137">Authenticate your user</span></span>

<span data-ttu-id="b4f84-138">Após a criação da credencial no cliente, na próxima vez que o usuário tentar acessar o site, você poderá oferecer a assinatura usando o Windows Hello em vez de uma senha com uma chamada para Window. webauthn. **Getassertion**.</span><span class="sxs-lookup"><span data-stu-id="b4f84-138">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using Windows Hello instead of a password with a call to window.webauthn.**getAssertion**.</span></span>

<span data-ttu-id="b4f84-139">O método getassertion assume o *desafio* como o único parâmetro obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b4f84-139">The getAssertion method takes the *challenge* as its only required parameter.</span></span> <span data-ttu-id="b4f84-140">O desafio é a quantidade gerada aleatoriamente que o servidor enviará a um cliente para se conectar com a chave privada do usuário.</span><span class="sxs-lookup"><span data-stu-id="b4f84-140">The challenge is the randomly generated quantity that the server will send down to a client to sign with the user's private key.</span></span> <span data-ttu-id="b4f84-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b4f84-141">For example:</span></span>

**<span data-ttu-id="b4f84-142">Servidor</span><span class="sxs-lookup"><span data-stu-id="b4f84-142">Server</span></span>**

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

<span data-ttu-id="b4f84-143">Depois que a chamada getassertion for feita, o Microsoft Edge mostrará o prompt do Windows Hello, que verificará a identidade do usuário usando a biometria.</span><span class="sxs-lookup"><span data-stu-id="b4f84-143">Once the getAssertion call is made, Microsoft Edge will show the Windows Hello prompt, which will verify the identity of the user using biometrics.</span></span> <span data-ttu-id="b4f84-144">Depois que o usuário for verificado, o desafio será assinado dentro do TPM e a promessa retornará com um objeto de asserção que contenha a assinatura e outros metadados para você enviar ao servidor:</span><span class="sxs-lookup"><span data-stu-id="b4f84-144">After the user is verified, the challenge will be signed within the TPM and the promise will return with an assertion object that contains the signature and other metadata for you to send to the server:</span></span>

**<span data-ttu-id="b4f84-145">Cliente</span><span class="sxs-lookup"><span data-stu-id="b4f84-145">Client</span></span>**

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

<span data-ttu-id="b4f84-146">Depois de receber a asserção no servidor, será preciso validar a assinatura para autenticar o usuário.</span><span class="sxs-lookup"><span data-stu-id="b4f84-146">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span> <span data-ttu-id="b4f84-147">Por exemplo (no node. JS):</span><span class="sxs-lookup"><span data-stu-id="b4f84-147">For example (in Node.JS):</span></span>

**<span data-ttu-id="b4f84-148">Servidor</span><span class="sxs-lookup"><span data-stu-id="b4f84-148">Server</span></span>**

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

## <span data-ttu-id="b4f84-149">Diferenças entre o Microsoft Edge e a especificação</span><span class="sxs-lookup"><span data-stu-id="b4f84-149">Differences between Microsoft Edge and the spec</span></span>

> [!NOTE]
> <span data-ttu-id="b4f84-150">Ao experimentar a API de autenticação da Web com o Windows Hello no Microsoft Edge, recomendamos usar o metapreenchimento webauthn. js, conforme mostrado acima, para evitar ter que considerar as discrepâncias listadas aqui.</span><span class="sxs-lookup"><span data-stu-id="b4f84-150">When trying out the Web Authentication API with Windows Hello in Microsoft Edge, we recommend using the Webauthn.js polyfill as shown above to avoid having to account for the discrepancies listed here.</span></span> <span data-ttu-id="b4f84-151">Atualizaremos este semipreenchimento para cada versão publicada mais importante da especificação.</span><span class="sxs-lookup"><span data-stu-id="b4f84-151">We'll update this polyfill for every major published version of the specification.</span></span>


<span data-ttu-id="b4f84-152">A implementação atual do Microsoft Edge é baseada em um rascunho anterior da especificação de autenticação da Web e provavelmente mudará nas futuras versões e, conforme a especificação evoluir.</span><span class="sxs-lookup"><span data-stu-id="b4f84-152">The current Microsoft Edge implementation is based on an earlier draft of the Web Authentication specification and is likely to change in future builds and as the spec evolves.</span></span> <span data-ttu-id="b4f84-153">As diferenças atuais incluem:</span><span class="sxs-lookup"><span data-stu-id="b4f84-153">The current differences include:</span></span>

- <span data-ttu-id="b4f84-154">As APIs do Microsoft Edge são MS-prefixadas.</span><span class="sxs-lookup"><span data-stu-id="b4f84-154">Microsoft Edge APIs are MS- prefixed.</span></span>
- <span data-ttu-id="b4f84-155">O Microsoft Edge ainda não dá suporte a credenciais externas, como chaves USB ou dispositivos Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="b4f84-155">Microsoft Edge does not yet support external credentials like USB keys or Bluetooth devices.</span></span> <span data-ttu-id="b4f84-156">A API atual limita-se a credenciais inseridas armazenadas no TPM.</span><span class="sxs-lookup"><span data-stu-id="b4f84-156">The current API is limited to embedded credentials stored in the TPM.</span></span>
- <span data-ttu-id="b4f84-157">A conta de usuário do Windows atualmente conectada deve ser configurada para dar suporte a pelo menos um PIN, e preferencialmente diante ou biometria de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="b4f84-157">The currently logged in Windows user account must be configured to support at least a PIN, and preferably face or fingerprint biometrics.</span></span> <span data-ttu-id="b4f84-158">Isso é para garantir que o Windows possa autenticar o acesso ao TPM.</span><span class="sxs-lookup"><span data-stu-id="b4f84-158">This is to ensure that Windows can authenticate the access to the TPM.</span></span>
- <span data-ttu-id="b4f84-159">A implementação do Microsoft Edge ainda não dá suporte à experiência do seletor de conta.</span><span class="sxs-lookup"><span data-stu-id="b4f84-159">The Microsoft Edge implementation does not yet support the account picker experience.</span></span>
- <span data-ttu-id="b4f84-160">Um segundo parâmetro de *filtros* especificando a ID de credencial é atualmente necessário para chamadas para msCredentials. [Getassertion](https://msdn.microsoft.com/library/mt697640).</span><span class="sxs-lookup"><span data-stu-id="b4f84-160">A second *filters* parameter specifying the credential id is currently required for calls to msCredentials.[getAssertion](https://msdn.microsoft.com/library/mt697640).</span></span> <span data-ttu-id="b4f84-161">Assim, você precisará armazenar suas informações de identificação de credenciais no armazenamento local do cliente, no indexDB ou no localStorage, ao fazer uma credencial.</span><span class="sxs-lookup"><span data-stu-id="b4f84-161">As such, you’ll need to store your credential ID information in local storage on the client, either in indexDB or localStorage when making your credential.</span></span> <span data-ttu-id="b4f84-162">Se um usuário excluir seu histórico de navegação, incluindo armazenamento local, será necessário registrá-lo novamente para usar o Windows Hello da próxima vez que fizerem logon.</span><span class="sxs-lookup"><span data-stu-id="b4f84-162">If a user deletes their browsing history, including local storage, they will need to re-register to use Windows Hello the next time they log in.</span></span>
- <span data-ttu-id="b4f84-163">O Microsoft Edge não oferece suporte a todas as opções no rascunho de especificação de autenticação da Web atual, como extensões ou tempos limite.</span><span class="sxs-lookup"><span data-stu-id="b4f84-163">Microsoft Edge does not support all of the options in the current Web Authentication specification draft, such as extensions or timeouts.</span></span>

<span data-ttu-id="b4f84-164">Nesse último ponto, as diferenças específicas do Microsoft Edge são observadas nas seguintes definições de especificação de autenticação da Web:</span><span class="sxs-lookup"><span data-stu-id="b4f84-164">On that last point, the specific Microsoft Edge differences are noted in the following Web Authentication spec definitions:</span></span>

### <span data-ttu-id="b4f84-165">Especificação do W3C</span><span class="sxs-lookup"><span data-stu-id="b4f84-165">W3C spec</span></span>

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



## <span data-ttu-id="b4f84-166">Referência da API</span><span class="sxs-lookup"><span data-stu-id="b4f84-166">API Reference</span></span>

[<span data-ttu-id="b4f84-167">MSCredentials</span><span class="sxs-lookup"><span data-stu-id="b4f84-167">MSCredentials</span></span>](https://msdn.microsoft.com/library/mt697639)

[<span data-ttu-id="b4f84-168">makeCredential</span><span class="sxs-lookup"><span data-stu-id="b4f84-168">makeCredential</span></span>](https://msdn.microsoft.com/library/mt697641)

[<span data-ttu-id="b4f84-169">getassertion</span><span class="sxs-lookup"><span data-stu-id="b4f84-169">getAssertion</span></span>](https://msdn.microsoft.com/library/mt697640)

## <span data-ttu-id="b4f84-170">Demonstrações</span><span class="sxs-lookup"><span data-stu-id="b4f84-170">Demos</span></span>

[<span data-ttu-id="b4f84-171">Exemplos de código do cliente e do servidor</span><span class="sxs-lookup"><span data-stu-id="b4f84-171">Client and server code samples</span></span>](https://github.com/adrianba/fido-snippets/)

[<span data-ttu-id="b4f84-172">Metapreenchimento do webauthn. js</span><span class="sxs-lookup"><span data-stu-id="b4f84-172">Webauthn.js polyfill</span></span>](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[<span data-ttu-id="b4f84-173">Demonstração da unidade de teste do Windows Hello</span><span class="sxs-lookup"><span data-stu-id="b4f84-173">Windows Hello Test Drive demo</span></span>](https://testdrive-fido.azurewebsites.net/)

## <span data-ttu-id="b4f84-174">Especificada</span><span class="sxs-lookup"><span data-stu-id="b4f84-174">Specification</span></span>

[<span data-ttu-id="b4f84-175">Autenticação da Web: uma API da Web para acessar as credenciais de escopo 1</span><span class="sxs-lookup"><span data-stu-id="b4f84-175">Web Authentication: A Web API for accessing scoped credentials 1</span></span>](http://w3c.github.io/webauthn/)  
