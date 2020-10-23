---
description: Emular autenticadores e depurar webauthn no Microsoft Edge DevTools.
title: Emular autenticadores e depurar webauthn no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6727e9aeea1a51689a80570a2f1c9df880a8c9db
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133952"
---
# <span data-ttu-id="5f058-104">Emular autenticadores e depurar webauthn no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5f058-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="5f058-105">Em vez de fazer a depuração da autenticação da Web em seu site ou aplicativo com autenticadores físicos, use a ferramenta **Webauthn** no Microsoft Edge devtools para criar e interagir com os autenticadores virtuais baseados em software.</span><span class="sxs-lookup"><span data-stu-id="5f058-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <span data-ttu-id="5f058-106">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="5f058-106">Before you begin</span></span>  

<span data-ttu-id="5f058-107">Um ótimo lugar para começar a autenticação na Web é a [especificação da API de autenticação da Web][GithubW3cWebauthn].</span><span class="sxs-lookup"><span data-stu-id="5f058-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <span data-ttu-id="5f058-108">Configurar a ferramenta webauthn</span><span class="sxs-lookup"><span data-stu-id="5f058-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="5f058-109">Navegue até uma página da Web que usa webauthn, como o site de demonstração a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f058-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="5f058-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="5f058-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="5f058-111">Conecte-se ao website.</span><span class="sxs-lookup"><span data-stu-id="5f058-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="5f058-112">[Abra o devtools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="5f058-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="5f058-113">Para abrir a ferramenta **webauthn** , escolha o ícone **Personalizar e controlar devtools** \ ( `...` \) > **mais ferramentas**  >  **webauthn**.</span><span class="sxs-lookup"><span data-stu-id="5f058-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="5f058-115">Ferramenta **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="5f058-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5f058-116">Na ferramenta **Webauthn** , escolha a caixa de seleção ao lado de **habilitar ambiente do autenticador virtual**.</span><span class="sxs-lookup"><span data-stu-id="5f058-116">In the **WebAuthn** tool, choose the checkbox next to **Enable virtual authenticator environment**.</span></span>  
1.  <span data-ttu-id="5f058-117">Depois de habilitado, uma nova seção chamada **novo autenticador** será exibida.</span><span class="sxs-lookup"><span data-stu-id="5f058-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="5f058-119">Habilitar o ambiente do autenticador virtual</span><span class="sxs-lookup"><span data-stu-id="5f058-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="5f058-120">Na seção **novo autenticador** , configure as seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="5f058-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="5f058-121">Opção</span><span class="sxs-lookup"><span data-stu-id="5f058-121">Option</span></span> | <span data-ttu-id="5f058-122">Value</span><span class="sxs-lookup"><span data-stu-id="5f058-122">Value</span></span> | <span data-ttu-id="5f058-123">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5f058-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="5f058-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] ou [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="5f058-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="5f058-125">O protocolo que o autenticador virtual usa para codificar e decodificar</span><span class="sxs-lookup"><span data-stu-id="5f058-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="5f058-126">, `nfc` , `ble` , ou</span><span class="sxs-lookup"><span data-stu-id="5f058-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="5f058-127">O autenticador virtual simula o transporte selecionado para comunicação com clientes para obter uma asserção para uma credencial específica.</span><span class="sxs-lookup"><span data-stu-id="5f058-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="5f058-128">Para obter mais informações, navegue até [enumeração de transporte do autenticador][GithubW3cWebauthnEnumTransport]</span><span class="sxs-lookup"><span data-stu-id="5f058-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="5f058-129">Ative \ (ou desligado \) usando a caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="5f058-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="5f058-130">Ative se o seu aplicativo Web depende de chaves residentes \ (também conhecidas como credenciais detectável do lado do cliente \).</span><span class="sxs-lookup"><span data-stu-id="5f058-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="5f058-131">Para obter mais informações, navegue até [enumeração de requisitos da chave residente][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="5f058-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="5f058-132">Ative \ (ou desligado \) usando a caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="5f058-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="5f058-133">Ative se o seu aplicativo Web depende da autorização local usando as modalidades de gesto como toque e código PIN, entrada de senha ou reconhecimento biométrico.</span><span class="sxs-lookup"><span data-stu-id="5f058-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="5f058-134">Para obter mais informações, navegue até [verificação do usuário][GithubW3cWebauthnEnumUserverification]</span><span class="sxs-lookup"><span data-stu-id="5f058-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="5f058-135">Escolha o botão **Adicionar** .</span><span class="sxs-lookup"><span data-stu-id="5f058-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="5f058-136">Uma nova seção de seu autenticador recém-criado será exibida.</span><span class="sxs-lookup"><span data-stu-id="5f058-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="5f058-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="5f058-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="5f058-139">A seção do **autenticador** inclui uma tabela de **credenciais** .</span><span class="sxs-lookup"><span data-stu-id="5f058-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="5f058-140">A tabela estará vazia até que uma credencial seja registrada no autenticador.</span><span class="sxs-lookup"><span data-stu-id="5f058-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="5f058-142">Nenhuma credencial</span><span class="sxs-lookup"><span data-stu-id="5f058-142">No credentials</span></span>  
:::image-end:::  

## <span data-ttu-id="5f058-143">Registrar uma nova credencial</span><span class="sxs-lookup"><span data-stu-id="5f058-143">Register a new credential</span></span>  

<span data-ttu-id="5f058-144">Para registrar uma nova credencial, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f058-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="5f058-145">Para obter mais informações sobre o que a [API de autenticação da Web][GithubW3cWebauthn] está fazendo ao registrar uma nova credencial, navegue para [criar uma nova credencial][GithubW3cWebauthnSctnCreatecredential].</span><span class="sxs-lookup"><span data-stu-id="5f058-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="5f058-146">No site de demonstração, escolha **registrar nova credencial**.</span><span class="sxs-lookup"><span data-stu-id="5f058-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="5f058-147">Uma nova credencial agora é adicionada à tabela de **credenciais** na ferramenta webauthn.</span><span class="sxs-lookup"><span data-stu-id="5f058-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="5f058-149">Exibir credenciais</span><span class="sxs-lookup"><span data-stu-id="5f058-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="5f058-150">No site de demonstração, escolha o botão **autenticar** .</span><span class="sxs-lookup"><span data-stu-id="5f058-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="5f058-151">Verifique se a [contagem de sinal][GithubW3cWebauthnSctnSignCounter] da credencial na tabela de **credenciais** aumentou em 1, que marca uma operação [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5f058-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <span data-ttu-id="5f058-152">Exportar e remover credenciais</span><span class="sxs-lookup"><span data-stu-id="5f058-152">Export and remove credentials</span></span>  

<span data-ttu-id="5f058-153">Para exportar ou remover uma credencial, escolha o botão **Exportar** ou **remover** .</span><span class="sxs-lookup"><span data-stu-id="5f058-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="5f058-155">Exportar ou remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="5f058-155">Export or remove a credential</span></span>  
:::image-end:::  

## <span data-ttu-id="5f058-156">Renomear um autenticador</span><span class="sxs-lookup"><span data-stu-id="5f058-156">Rename an authenticator</span></span>  

<span data-ttu-id="5f058-157">Para renomear um autenticador, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f058-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="5f058-158">Ao lado do nome do autenticador, escolha o botão **Editar** .</span><span class="sxs-lookup"><span data-stu-id="5f058-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="5f058-159">Edite o nome e escolha **Enter** para salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="5f058-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="5f058-161">Renomear um autenticador</span><span class="sxs-lookup"><span data-stu-id="5f058-161">Rename an authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="5f058-162">Definir o autenticador ativo</span><span class="sxs-lookup"><span data-stu-id="5f058-162">Set the active authenticator</span></span>  

<span data-ttu-id="5f058-163">Um autenticador recém-criado é ativado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5f058-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="5f058-164">Para usar outro autenticador virtual, escolha o botão de opção **ativo** ao lado do autenticador.</span><span class="sxs-lookup"><span data-stu-id="5f058-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f058-165">O DevTools oferece suporte a apenas um autenticador virtual ativo em qualquer point-in-time.</span><span class="sxs-lookup"><span data-stu-id="5f058-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="5f058-166">Se você remover o autenticador ativo, outro autenticador não será ativado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5f058-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="5f058-168">Definir autenticador ativo</span><span class="sxs-lookup"><span data-stu-id="5f058-168">Set active authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="5f058-169">Remover um autenticador virtual</span><span class="sxs-lookup"><span data-stu-id="5f058-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="5f058-170">Para remover um autenticador virtual, ao lado do autenticador, escolha o botão **remover** .</span><span class="sxs-lookup"><span data-stu-id="5f058-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="5f058-172">Remover autenticador</span><span class="sxs-lookup"><span data-stu-id="5f058-172">Remove authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="5f058-173">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5f058-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Demonstração webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Protocolo de cliente para autenticador (CTAP) | Fido Alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Visão geral do 2º fator (U2F) universal | Fido Alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação na Web: uma API para acessar as credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "A operação authenticatorGetAssertion-autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Enumeração de transporte autenticador (Enumeração AuthenticatorTransport)-autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeração de requisito de chave residente (Enumeração ResidentKeyRequirement)-autenticação da Web: uma API para acessar o nível 2 das credenciais de chave pública | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Verificação do usuário – autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Criar um novo método Credential-PublicKeyCredential [[Create]] (Origin, Options, sameOriginWithAncestors)-autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Considerações do contador de assinatura-autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | GitHub"  

> [!NOTE]
> <span data-ttu-id="5f058-185">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="5f058-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5f058-186">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="5f058-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5f058-188">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5f058-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
