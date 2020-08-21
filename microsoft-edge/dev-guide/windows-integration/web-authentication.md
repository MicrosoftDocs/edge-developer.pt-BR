---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Saiba como a API de autenticação da Web pode permitir que os aplicativos da Web usem o Windows Hello e o FIDO2 para autenticação de usuário.
title: Autenticação da Web-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: b8ff3769434c17b5508978c64b5d9c14e7e3bdaa
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941816"
---
# <span data-ttu-id="49287-104">Autenticação da Web e Windows Hello</span><span class="sxs-lookup"><span data-stu-id="49287-104">Web Authentication and Windows Hello</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="49287-105">A [API de autenticação da Web](https://w3c.github.io/webauthn) no Microsoft Edge permite que os aplicativos da Web usem dispositivos [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) e [FIDO2 externos](https://fidoalliance.org/fido2) para autenticação de usuário, para que você e seus usuários possam evitar todas as complicações e riscos de gerenciamento de senhas, incluindo adivinhação de senha, phishing e ataques de registro de chave.</span><span class="sxs-lookup"><span data-stu-id="49287-105">The [Web Authentication API](https://w3c.github.io/webauthn) in Microsoft Edge enables web applications to use [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) and [external FIDO2 devices](https://fidoalliance.org/fido2) for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and key-logging attacks.</span></span>  <span data-ttu-id="49287-106">A implementação atual do Microsoft Edge é baseada na recomendação de candidatos da especificação de autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="49287-106">The current Microsoft Edge implementation is based on the Candidate Recommendation of the Web Authentication specification.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="49287-107">Este tópico mostra como experimentar a autenticação do Windows Hello e do FIDO2 com o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="49287-107">This topic will show you how to try out Windows Hello and FIDO2 authentication with Microsoft Edge.</span></span>  

<span data-ttu-id="49287-108">Usando a autenticação da Web, o servidor envia um desafio de texto sem formatação para o navegador.</span><span class="sxs-lookup"><span data-stu-id="49287-108">Using Web Authentication, the server sends down a plain text challenge to the browser.</span></span>  <span data-ttu-id="49287-109">Depois que o Microsoft Edge for capaz de verificar o usuário por meio do Windows Hello ou de um dispositivo de FIDO2 externo, o sistema assinará o desafio com uma chave privada fornecida anteriormente para esse usuário e enviar a assinatura de volta para o servidor.</span><span class="sxs-lookup"><span data-stu-id="49287-109">Once Microsoft Edge is able to verify the user through Windows Hello or an external FIDO2 device, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span>  <span data-ttu-id="49287-110">Se o servidor puder validar a assinatura usando a chave pública que ele tem para o usuário e verificar se o desafio está correto, ele pode autenticar o usuário com segurança.</span><span class="sxs-lookup"><span data-stu-id="49287-110">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span>  <span data-ttu-id="49287-111">Com a [criptografia assimétrica](https://en.wikipedia.org/wiki/Public-key_cryptography) , como isso, a chave pública não tem significado algum e a chave privada nunca é compartilhada.</span><span class="sxs-lookup"><span data-stu-id="49287-111">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span>  <span data-ttu-id="49287-112">Além disso, a chave privada nunca pode ser movida de elementos seguros ou sistemas modernos com hardware compatível com TPM.</span><span class="sxs-lookup"><span data-stu-id="49287-112">Furthermore, the private key can never be moved from secure elements or modern systems with TPM-enabled hardware.</span></span>  

<span data-ttu-id="49287-113">Há duas etapas básicas para usar a API de autenticação da Web:</span><span class="sxs-lookup"><span data-stu-id="49287-113">There are two basic steps to using the Web Authentication API:</span></span>  

1.  <span data-ttu-id="49287-114">Registre seu usuário com</span><span class="sxs-lookup"><span data-stu-id="49287-114">Register your user with</span></span> `create`  
1.  <span data-ttu-id="49287-115">Autentique seu usuário com</span><span class="sxs-lookup"><span data-stu-id="49287-115">Authenticate your user with</span></span> `get`  

<span data-ttu-id="49287-116">O seguinte guia de desenvolvimento orientará você nesse fluxo usando o [aplicativo de exemplo Webauthn](https://github.com/MicrosoftEdge/webauthnsample).</span><span class="sxs-lookup"><span data-stu-id="49287-116">The following dev guide will walk you through this flow using the [WebAuthn Sample App](https://github.com/MicrosoftEdge/webauthnsample).</span></span>  

## <span data-ttu-id="49287-117">Registrar o usuário</span><span class="sxs-lookup"><span data-stu-id="49287-117">Register your user</span></span>  

<span data-ttu-id="49287-118">Atuando como um provedor de identidade, você precisará primeiro criar uma credencial de autenticação da Web para o usuário com o `navigator.credentials.create` método.</span><span class="sxs-lookup"><span data-stu-id="49287-118">Acting as an identity provider, you will first need to create a Web Authentication credential for your user with the `navigator.credentials.create` method.</span></span>  <span data-ttu-id="49287-119">Antes de registrar essa credencial para o usuário em seu servidor, você precisará confirmar a identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="49287-119">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span>  <span data-ttu-id="49287-120">Isso pode ser feito enviando ao usuário uma confirmação de email ou solicitando que use o método de login tradicional.</span><span class="sxs-lookup"><span data-stu-id="49287-120">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>  

<span data-ttu-id="49287-121">O `create` método usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="49287-121">The `create` method takes the following parameters:</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="49287-122">informações da terceira parte confiável</span><span class="sxs-lookup"><span data-stu-id="49287-122">relying party information</span></span>**  
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
      **<span data-ttu-id="49287-123">informações da conta do usuário</span><span class="sxs-lookup"><span data-stu-id="49287-123">user account information</span></span>**  
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
      **<span data-ttu-id="49287-124">parâmetros de criptografia</span><span class="sxs-lookup"><span data-stu-id="49287-124">crypto parameters</span></span>**  
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
      **<span data-ttu-id="49287-125">parâmetros de seleção do autenticador</span><span class="sxs-lookup"><span data-stu-id="49287-125">authenticator selection parameters</span></span>**  
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
      **<span data-ttu-id="49287-126">outras opções</span><span class="sxs-lookup"><span data-stu-id="49287-126">other options</span></span>**  
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

<span data-ttu-id="49287-127">Você pode usar os [parâmetros de criação de credenciais](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) para configurar a credencial que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="49287-127">You can use [credential creation parameters](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) to configure the credential you want to create.</span></span>  <span data-ttu-id="49287-128">Em particular, você pode optar por criar uma credencial do Windows Hello Configurando `authenticatorAttachment` para `platform` ou uma credencial de roaming em um dispositivo de FIDO2 externo definindo `authenticatorAttachment` como `cross-platform` .</span><span class="sxs-lookup"><span data-stu-id="49287-128">In particular, you can choose to create a Windows Hello credential by setting `authenticatorAttachment` to `platform`, or a roaming credential on an external FIDO2 device by setting `authenticatorAttachment` to `cross-platform`.</span></span>  

<span data-ttu-id="49287-129">Quando você usa o `create` método, o Microsoft Edge pede primeiro que o usuário Verifique sua presença digitalizando a face ou a impressão digital, inserindo um PIN ou executando uma ação em um dispositivo FIDO2 externo.</span><span class="sxs-lookup"><span data-stu-id="49287-129">When you use the `create` method, Microsoft Edge will first ask the user to verify their presence by scanning their face or fingerprint, entering a PIN, or taking action on an external FIDO2 device.</span></span>  <span data-ttu-id="49287-130">Depois que esta etapa for concluída, o autenticador gerará um par de chaves PublicPrivate e armazenará a chave privada.</span><span class="sxs-lookup"><span data-stu-id="49287-130">Once this step is completed the authenticator will generate a publicprivate key pair and store the private key.</span></span>  <span data-ttu-id="49287-131">Essas credenciais são criadas por origem, por conta e não podem ser extraídas porque são armazenadas de forma segura para o dispositivo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="49287-131">These credentials are created per origin, per account, and cannot be extracted because they are stored securely to the authentication device.</span></span>  

<span data-ttu-id="49287-132">A promessa resultante retorna um [objeto atestador](https://w3c.github.io/webauthn#sctn-attestation) que representa a nova credencial.</span><span class="sxs-lookup"><span data-stu-id="49287-132">The resulting promise returns an [attestation object](https://w3c.github.io/webauthn#sctn-attestation) representing the new credential.</span></span>  <span data-ttu-id="49287-133">O objeto de atestado contém a chave pública da credencial.</span><span class="sxs-lookup"><span data-stu-id="49287-133">The attestation object contains the public key for the credential.</span></span>  <span data-ttu-id="49287-134">Você enviará esse objeto ao servidor para validar futuras autenticações.</span><span class="sxs-lookup"><span data-stu-id="49287-134">You'll send this object to the server for validating future authentications.</span></span>  <span data-ttu-id="49287-135">Antes de enviar de volta ao servidor, você precisará codificar os dados brutos em base64.</span><span class="sxs-lookup"><span data-stu-id="49287-135">Before sending back to the server, you'll need to base64-encode the raw data.</span></span>  

**<span data-ttu-id="49287-136">Cliente</span><span class="sxs-lookup"><span data-stu-id="49287-136">Client</span></span>**  

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

<span data-ttu-id="49287-137">Em seguida, o servidor deve decodificar o objeto de atestado, executar etapas de verificação, extrair a chave pública para esta credencial e armazená-la para autenticações futuras.</span><span class="sxs-lookup"><span data-stu-id="49287-137">The server should then decode the attestation object, perform verification steps, extract the public key for this credential, and store it for future authentications.</span></span>  <span data-ttu-id="49287-138">Uma lista detalhada de etapas pode ser encontrada no [algoritmo de registro de credenciais](https://w3c.github.io/webauthn#registering-a-new-credential) na especificação webauthn.</span><span class="sxs-lookup"><span data-stu-id="49287-138">A detailed list of steps can be found in the [credential registration algorithm](https://w3c.github.io/webauthn#registering-a-new-credential) in the WebAuthn specification.</span></span>  

**<span data-ttu-id="49287-139">Servidor</span><span class="sxs-lookup"><span data-stu-id="49287-139">Server</span></span>**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## <span data-ttu-id="49287-140">Autenticar seu usuário</span><span class="sxs-lookup"><span data-stu-id="49287-140">Authenticate your user</span></span>  

<span data-ttu-id="49287-141">Após a criação da credencial no cliente, na próxima vez que o usuário tentar se conectar ao site, você poderá oferecer a assinatura usando a credencial de autenticação da Web, em vez de uma senha com uma chamada para `navigator.credentials.get` .</span><span class="sxs-lookup"><span data-stu-id="49287-141">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using their Web Authentication credential instead of a password with a call to `navigator.credentials.get`.</span></span>  

<span data-ttu-id="49287-142">O `get` método assume o desafio como o único parâmetro obrigatório.</span><span class="sxs-lookup"><span data-stu-id="49287-142">The `get` method takes the challenge as its only required parameter.</span></span>  <span data-ttu-id="49287-143">O desafio é uma sequência opaca de bytes que o servidor enviará a um cliente para assinar com a chave privada do usuário.</span><span class="sxs-lookup"><span data-stu-id="49287-143">The challenge is an opaque sequence of bytes that the server will send down to a client to sign with the user's private key.</span></span>  <span data-ttu-id="49287-144">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="49287-144">For example:</span></span>  

**<span data-ttu-id="49287-145">Servidor</span><span class="sxs-lookup"><span data-stu-id="49287-145">Server</span></span>**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

<span data-ttu-id="49287-146">Depois de recuperar um desafio do servidor, você chamará a API Get juntamente com [as opções de solicitação de credenciais](https://w3c.github.io/webauthn#credentialrequestoptions-extension).</span><span class="sxs-lookup"><span data-stu-id="49287-146">After retrieving a challenge from the server, you'll call the get API along with [credential request options](https://w3c.github.io/webauthn#credentialrequestoptions-extension).</span></span>  <span data-ttu-id="49287-147">O Microsoft Edge mostrará um prompt, que verificará a identidade do usuário usando o Windows Hello ou um dispositivo de FIDO2 externo.</span><span class="sxs-lookup"><span data-stu-id="49287-147">Microsoft Edge will show a prompt, which will verify the identity of the user using Windows Hello or an external FIDO2 device.</span></span>  <span data-ttu-id="49287-148">Depois que o usuário for verificado, o desafio será assinado dentro do dispositivo TPM ou FIDO2 e a promessa retornará com um [objeto de asserção](https://w3c.github.io/webauthn#authenticatorassertionresponse) que contenha a assinatura e outros metadados para você enviar para o servidor.</span><span class="sxs-lookup"><span data-stu-id="49287-148">After the user is verified, the challenge will be signed within the TPM or FIDO2 device and the promise will return with an [assertion object](https://w3c.github.io/webauthn#authenticatorassertionresponse) that contains the signature and other metadata for you to send to the server.</span></span>  

**<span data-ttu-id="49287-149">Cliente</span><span class="sxs-lookup"><span data-stu-id="49287-149">Client</span></span>**  

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

<span data-ttu-id="49287-150">Depois de receber a asserção no servidor, será preciso validar a assinatura para autenticar o usuário.</span><span class="sxs-lookup"><span data-stu-id="49287-150">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span>  <span data-ttu-id="49287-151">Veja a seguir um exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="49287-151">The following is some sample code.</span></span>  <span data-ttu-id="49287-152">Uma lista detalhada de etapas pode ser encontrada no [algoritmo de verificação de asserção](https://w3c.github.io/webauthn#verifying-assertion) na especificação webauthn.</span><span class="sxs-lookup"><span data-stu-id="49287-152">A detailed list of steps can be found in the [assertion verification algorithm](https://w3c.github.io/webauthn#verifying-assertion) in the WebAuthn specification.</span></span>  

**<span data-ttu-id="49287-153">Servidor</span><span class="sxs-lookup"><span data-stu-id="49287-153">Server</span></span>**  

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

## <span data-ttu-id="49287-154">Notas de implementação</span><span class="sxs-lookup"><span data-stu-id="49287-154">Implementation notes</span></span>  

### <span data-ttu-id="49287-155">Plataformas compatíveis</span><span class="sxs-lookup"><span data-stu-id="49287-155">Supported platforms</span></span>  

*   <span data-ttu-id="49287-156">A versão de recomendação de candidatos da API de autenticação da Web pode ser usada do Microsoft Edge começando com o EdgeHTML 18 \ (Windows Insider Preview versão 17713 ou mais recente \).</span><span class="sxs-lookup"><span data-stu-id="49287-156">The Candidate Recommendation version of the Web Authentication API can be used from Microsoft Edge beginning with EdgeHTML 18 \(Windows Insider Preview version 17713 or newer\).</span></span>  
*   <span data-ttu-id="49287-157">A [versão de visualização prefixada](https://blogs.windows.com/msedgedev/2016/04/12) da API de autenticação da Web foi removida e não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="49287-157">The [prefixed, preview version](https://blogs.windows.com/msedgedev/2016/04/12) of the Web Authentication API has been removed and is no longer available.</span></span>  
*   <span data-ttu-id="49287-158">A API de autenticação da Web ainda não está disponível para aplicativos UWP e PWAs.</span><span class="sxs-lookup"><span data-stu-id="49287-158">The Web Authentication API is not yet available to UWP apps and PWAs.</span></span>  
*   <span data-ttu-id="49287-159">O Internet Explorer não é compatível com a API de autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="49287-159">Internet Explorer does not support the Web Authentication API.</span></span>  

### <span data-ttu-id="49287-160">Autenticadores com suporte</span><span class="sxs-lookup"><span data-stu-id="49287-160">Supported authenticators</span></span>  

<span data-ttu-id="49287-161">Com a API de autenticação da Web no Microsoft Edge, você pode autenticar usuários com as seguintes tecnologias:</span><span class="sxs-lookup"><span data-stu-id="49287-161">With the Web Authentication API in Microsoft Edge, you can authenticate users with the following technologies:</span></span>  

*   <span data-ttu-id="49287-162">**Windows Hello**  Habilita a autenticação no dispositivo sem senha com face, impressão digital ou PIN</span><span class="sxs-lookup"><span data-stu-id="49287-162">**Windows Hello**  Enables passwordless on-device authentication with  face, fingerprint, or PIN</span></span>  
*   <span data-ttu-id="49287-163">**FIDO2**  Habilita a autenticação de roaming sem senha com um dispositivo removível e uma impressão digital ou PIN</span><span class="sxs-lookup"><span data-stu-id="49287-163">**FIDO2**  Enables passwordless roaming authentication with a removable device and a fingerprint or PIN</span></span>  
*   <span data-ttu-id="49287-164">**U2F**  Habilita a autenticação de segundo fator forte para sites que não estão prontos para serem movidos para um modelo sem senha</span><span class="sxs-lookup"><span data-stu-id="49287-164">**U2F**  Enables strong second factor authentication for websites that are not ready to move to a passwordless model</span></span>  

### <span data-ttu-id="49287-165">Considerações especiais para o Windows Hello</span><span class="sxs-lookup"><span data-stu-id="49287-165">Special considerations for Windows Hello</span></span>  

<span data-ttu-id="49287-166">Algumas coisas a serem observadas ao usar o autenticador Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="49287-166">A few things to note when using the Windows Hello authenticator:</span></span>  

*   <span data-ttu-id="49287-167">Você pode detectar se o Windows Hello está disponível em um computador chamando a `isUserVerifyingPlatformAuthenticatorAvailable` API.</span><span class="sxs-lookup"><span data-stu-id="49287-167">You can detect if Windows Hello is available on a PC by calling the `isUserVerifyingPlatformAuthenticatorAvailable` API.</span></span>  <span data-ttu-id="49287-168">Saiba mais sobre esta API [aqui](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).</span><span class="sxs-lookup"><span data-stu-id="49287-168">Learn more about this API [here](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).</span></span>  
*   <span data-ttu-id="49287-169">Ao criar uma credencial para o Windows Hello, você deve definir `authenticatorAttachment` para `platform` a melhor experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="49287-169">When creating a credential for Windows Hello, you should set `authenticatorAttachment` to `platform` for the best user experience.</span></span>
*   <span data-ttu-id="49287-170">O Windows Hello só dá suporte a RS256 \ (alg-257 \) como algoritmo de chave pública.</span><span class="sxs-lookup"><span data-stu-id="49287-170">Windows Hello only supports RS256 \(alg -257\) as its public key algorithm.</span></span>  <span data-ttu-id="49287-171">Certifique-se de especificar esse algoritmo ao criar uma credencial.</span><span class="sxs-lookup"><span data-stu-id="49287-171">Be sure to specify this algorithm when creating a credential.</span></span>  
*   <span data-ttu-id="49287-172">Para receber uma [instrução de atestado de TPM](https://w3c.github.io/webauthn#tpm-attestation), defina atestador como "direto" ao chamar a `create` API.</span><span class="sxs-lookup"><span data-stu-id="49287-172">To receive a [TPM attestation statement](https://w3c.github.io/webauthn#tpm-attestation), set attestation to "direct" when calling the `create` API.</span></span>  <span data-ttu-id="49287-173">O atestado TPM é um melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="49287-173">TPM attestation is a best effort.</span></span>  <span data-ttu-id="49287-174">Somente os computadores com TPM 2,0 retornarão uma instrução de atestado TPM, e o processo de atestado poderá falhar por várias razões.</span><span class="sxs-lookup"><span data-stu-id="49287-174">Only PCs with TPM 2.0 will return a TPM attestation statement, and the attestation process could fail for a variety of reasons.</span></span>  
*   <span data-ttu-id="49287-175">O Windows Hello emprega diversas maneiras de proteger as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="49287-175">Windows Hello employs a variety of ways to protect user credentials.</span></span>  <span data-ttu-id="49287-176">Você pode verificar qual método foi usado para proteger uma credencial consumindo o campo [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) no objeto de atestado retornado na criação de credenciais.</span><span class="sxs-lookup"><span data-stu-id="49287-176">You can check which method has been used to protect a credential by consuming the [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) field in the attestation object returned at credential creation.</span></span>  <span data-ttu-id="49287-177">Veja a seguir a lista de AAGUIDs que o Windows Hello pode retornar:</span><span class="sxs-lookup"><span data-stu-id="49287-177">The following is the list of AAGUIDs that Windows Hello may return:</span></span>   
    *   <span data-ttu-id="49287-178">Autenticadores reproduzidos por software</span><span class="sxs-lookup"><span data-stu-id="49287-178">Software backed authenticators</span></span>  
        *   <span data-ttu-id="49287-179">Autenticador de software do Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="49287-179">Windows Hello software authenticator:</span></span>  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   <span data-ttu-id="49287-180">Autenticador de software VBS do Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="49287-180">Windows Hello VBS software authenticator:</span></span>  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   <span data-ttu-id="49287-181">Autenticadores com backup do Trusted Platform Module \ (TPM \)</span><span class="sxs-lookup"><span data-stu-id="49287-181">Trusted Platform Module \(TPM\) backed authenticators</span></span>  
        *   <span data-ttu-id="49287-182">Autenticador de hardware do Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="49287-182">Windows Hello hardware authenticator:</span></span>  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   <span data-ttu-id="49287-183">Autenticador de hardware do Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="49287-183">Windows Hello VBS hardware authenticator:</span></span>  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### <span data-ttu-id="49287-184">Superfície da API</span><span class="sxs-lookup"><span data-stu-id="49287-184">API surface</span></span>  

*   <span data-ttu-id="49287-185">O Microsoft Edge tem uma implementação completa da versão de recomendação de candidatos da especificação de autenticação da Web principal.</span><span class="sxs-lookup"><span data-stu-id="49287-185">Microsoft Edge has a complete implementation of the Candidate Recommendation version of the core Web Authentication specification.</span></span>  
*   <span data-ttu-id="49287-186">A [extensão AppID](https://w3c.github.io/webauthn#sctn-appid-extension) tem suporte.</span><span class="sxs-lookup"><span data-stu-id="49287-186">The [AppID extension](https://w3c.github.io/webauthn#sctn-appid-extension) is supported.</span></span>  
*   <span data-ttu-id="49287-187">Não há suporte para nenhuma outra extensão.</span><span class="sxs-lookup"><span data-stu-id="49287-187">No other extensions are supported.</span></span>  

## <span data-ttu-id="49287-188">Demonstrações</span><span class="sxs-lookup"><span data-stu-id="49287-188">Demos</span></span>  

[<span data-ttu-id="49287-189">Amostra de código do cliente e do servidor</span><span class="sxs-lookup"><span data-stu-id="49287-189">Client and server code sample</span></span>](https://github.com/MicrosoftEdge/webauthnsample)  

[<span data-ttu-id="49287-190">Demonstração da unidade de teste do Windows Hello</span><span class="sxs-lookup"><span data-stu-id="49287-190">Windows Hello Test Drive demo</span></span>](https://webauthnsample.azurewebsites.net)  

## <span data-ttu-id="49287-191">Especificada</span><span class="sxs-lookup"><span data-stu-id="49287-191">Specification</span></span>  

[<span data-ttu-id="49287-192">Autenticação na Web: uma API para acessar credenciais de chave pública</span><span class="sxs-lookup"><span data-stu-id="49287-192">Web Authentication: An API for accessing Public Key Credentials</span></span>](http://w3c.github.io/webauthn)  
