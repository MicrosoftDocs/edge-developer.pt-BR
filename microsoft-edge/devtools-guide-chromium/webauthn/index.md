---
description: Emular Autenticadores e Depurar WebAuthn no Microsoft Edge DevTools.
title: Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d5eeedfaa98e56bbba81634685a223844803a1ad
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564032"
---
# <a name="emulate-authenticators-and-debug-webauthn-in-microsoft-edge-devtools"></a><span data-ttu-id="7aa30-104">Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7aa30-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7aa30-105">Em vez de depurar a Autenticação Web em seu site ou aplicativo com autenticadores físicos, use a ferramenta **WebAuthn** no Microsoft Edge DevTools para criar e interagir com autenticadores virtuais baseados em software.</span><span class="sxs-lookup"><span data-stu-id="7aa30-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="7aa30-106">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="7aa30-106">Before you begin</span></span>  

<span data-ttu-id="7aa30-107">Um ótimo lugar para começar a autenticação da Web é a [especificação da API de Autenticação da Web.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="7aa30-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <a name="set-up-the-webauthn-tool"></a><span data-ttu-id="7aa30-108">Configurar a ferramenta WebAuthn</span><span class="sxs-lookup"><span data-stu-id="7aa30-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="7aa30-109">Navegue até uma página da Web que usa WebAuthn, como o seguinte site de demonstração.</span><span class="sxs-lookup"><span data-stu-id="7aa30-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="7aa30-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="7aa30-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="7aa30-111">Entre no site.</span><span class="sxs-lookup"><span data-stu-id="7aa30-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="7aa30-112">[Abra DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="7aa30-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="7aa30-113">Para abrir a **ferramenta WebAuthn,** escolha o ícone Personalizar e controlar **DevTools** \( \) > `...` Mais **ferramentas**  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="7aa30-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Ferramenta WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="7aa30-115">**Ferramenta WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="7aa30-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7aa30-116">Na ferramenta **WebAuthn,** ative a caixa de seleção Habilitar ambiente **de autenticador virtual.**</span><span class="sxs-lookup"><span data-stu-id="7aa30-116">In the **WebAuthn** tool, turn on **Enable virtual authenticator environment** checkbox.</span></span>  
1.  <span data-ttu-id="7aa30-117">Depois de habilitada, uma nova seção chamada **Novo autenticador** é exibida.</span><span class="sxs-lookup"><span data-stu-id="7aa30-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Habilitar ambiente de autenticador virtual" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="7aa30-119">Habilitar ambiente de autenticador virtual</span><span class="sxs-lookup"><span data-stu-id="7aa30-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="7aa30-120">Na seção **Novo autenticador,** configure as seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="7aa30-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="7aa30-121">Opção</span><span class="sxs-lookup"><span data-stu-id="7aa30-121">Option</span></span> | <span data-ttu-id="7aa30-122">Value</span><span class="sxs-lookup"><span data-stu-id="7aa30-122">Value</span></span> | <span data-ttu-id="7aa30-123">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7aa30-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="7aa30-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] ou [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="7aa30-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="7aa30-125">O protocolo que o autenticador virtual usa para codificação e decodificação</span><span class="sxs-lookup"><span data-stu-id="7aa30-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="7aa30-126">, `nfc` `ble` , ou</span><span class="sxs-lookup"><span data-stu-id="7aa30-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="7aa30-127">O autenticador virtual simula o transporte selecionado para se comunicar com clientes para obter uma declaração para uma credencial específica.</span><span class="sxs-lookup"><span data-stu-id="7aa30-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="7aa30-128">Para obter mais informações, navegue [até Authenticator Enumeração de Transporte][GithubW3cWebauthnEnumTransport]</span><span class="sxs-lookup"><span data-stu-id="7aa30-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="7aa30-129">Ativar \(ou desativar\) usando a caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="7aa30-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="7aa30-130">A ativar se o aplicativo Web depende de chaves de residente \(também conhecidas como credenciais de descoberta do lado do cliente\).</span><span class="sxs-lookup"><span data-stu-id="7aa30-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="7aa30-131">Para obter mais informações, navegue até [Enumeração de Requisitos de Chave de Residente][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="7aa30-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="7aa30-132">Ativar \(ou desativar\) usando a caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="7aa30-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="7aa30-133">A opção Ativar se seu aplicativo Web depende da autorização local usando modalidades de gesto, como código de toque e pino, entrada de senha ou reconhecimento biométrico.</span><span class="sxs-lookup"><span data-stu-id="7aa30-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="7aa30-134">Para obter mais informações, navegue até [Verificação do Usuário][GithubW3cWebauthnEnumUserverification]</span><span class="sxs-lookup"><span data-stu-id="7aa30-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="7aa30-135">Escolha o **botão Adicionar.**</span><span class="sxs-lookup"><span data-stu-id="7aa30-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="7aa30-136">Uma nova seção do autenticador recém-criado é exibida.</span><span class="sxs-lookup"><span data-stu-id="7aa30-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="7aa30-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="7aa30-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="7aa30-139">A **Authenticator** inclui uma tabela **Credentials.**</span><span class="sxs-lookup"><span data-stu-id="7aa30-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="7aa30-140">A tabela está vazia até que uma credencial seja registrada no autenticador.</span><span class="sxs-lookup"><span data-stu-id="7aa30-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Sem credenciais" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="7aa30-142">Sem credenciais</span><span class="sxs-lookup"><span data-stu-id="7aa30-142">No credentials</span></span>  
:::image-end:::  

## <a name="register-a-new-credential"></a><span data-ttu-id="7aa30-143">Registrar uma nova credencial</span><span class="sxs-lookup"><span data-stu-id="7aa30-143">Register a new credential</span></span>  

<span data-ttu-id="7aa30-144">Para registrar uma nova credencial, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="7aa30-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="7aa30-145">Para obter mais informações sobre o que a API de Autenticação [da Web][GithubW3cWebauthn] está fazendo ao registrar uma nova credencial, navegue até Criar uma [nova credencial.][GithubW3cWebauthnSctnCreatecredential]</span><span class="sxs-lookup"><span data-stu-id="7aa30-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="7aa30-146">No site de demonstração, escolha **Registrar nova credencial.**</span><span class="sxs-lookup"><span data-stu-id="7aa30-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="7aa30-147">Uma nova credencial agora é adicionada à tabela **Credenciais** na ferramenta WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="7aa30-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Exibir credenciais" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="7aa30-149">Exibir credenciais</span><span class="sxs-lookup"><span data-stu-id="7aa30-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="7aa30-150">No site de demonstração, escolha o **botão Autenticar.**</span><span class="sxs-lookup"><span data-stu-id="7aa30-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="7aa30-151">Verifique se a [Contagem de][GithubW3cWebauthnSctnSignCounter] Sinais da credencial na tabela **Credenciais** aumentou 1, o que marca uma operação bem-sucedida [do autenticadorGetAssertion.][GithubW3cWebauthnAuthenticatorgetassertion]</span><span class="sxs-lookup"><span data-stu-id="7aa30-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <a name="export-and-remove-credentials"></a><span data-ttu-id="7aa30-152">Exportar e remover credenciais</span><span class="sxs-lookup"><span data-stu-id="7aa30-152">Export and remove credentials</span></span>  

<span data-ttu-id="7aa30-153">Para exportar ou remover uma credencial, escolha o **botão Exportar** ou **Remover.**</span><span class="sxs-lookup"><span data-stu-id="7aa30-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exportar ou remover uma credencial" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="7aa30-155">Exportar ou remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="7aa30-155">Export or remove a credential</span></span>  
:::image-end:::  

## <a name="rename-an-authenticator"></a><span data-ttu-id="7aa30-156">Renomear um autenticador</span><span class="sxs-lookup"><span data-stu-id="7aa30-156">Rename an authenticator</span></span>  

<span data-ttu-id="7aa30-157">Para renomear um autenticador, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="7aa30-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="7aa30-158">Ao lado do nome do autenticador, escolha o **botão Editar.**</span><span class="sxs-lookup"><span data-stu-id="7aa30-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="7aa30-159">Edite o nome e escolha **Enter** para salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="7aa30-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Renomear um autenticador" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="7aa30-161">Renomear um autenticador</span><span class="sxs-lookup"><span data-stu-id="7aa30-161">Rename an authenticator</span></span>  
:::image-end:::  

## <a name="set-the-active-authenticator"></a><span data-ttu-id="7aa30-162">Definir o autenticador ativo</span><span class="sxs-lookup"><span data-stu-id="7aa30-162">Set the active authenticator</span></span>  

<span data-ttu-id="7aa30-163">Um autenticador recém-criado é ativado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7aa30-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="7aa30-164">Para usar outro autenticador virtual, escolha o botão de rádio **Ativo** ao lado do autenticador.</span><span class="sxs-lookup"><span data-stu-id="7aa30-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="7aa30-165">O DevTools oferece suporte a apenas um autenticador virtual ativo a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="7aa30-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="7aa30-166">Se você remover o autenticador ativo, outro autenticador não será ativado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7aa30-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Definir autenticador ativo" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="7aa30-168">Definir autenticador ativo</span><span class="sxs-lookup"><span data-stu-id="7aa30-168">Set active authenticator</span></span>  
:::image-end:::  

## <a name="remove-a-virtual-authenticator"></a><span data-ttu-id="7aa30-169">Remover um autenticador virtual</span><span class="sxs-lookup"><span data-stu-id="7aa30-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="7aa30-170">Para remover um autenticador virtual, ao lado do autenticador, escolha o **botão Remover.**</span><span class="sxs-lookup"><span data-stu-id="7aa30-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Remover autenticador" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="7aa30-172">Remover autenticador</span><span class="sxs-lookup"><span data-stu-id="7aa30-172">Remove authenticator</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7aa30-173">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7aa30-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Demonstração webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Cliente para Authenticator Protocolo (CTAP) | fido alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Visão geral do Fator 2nd Universal (U2F) | fido alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "A operação authenticatorGetAssertion - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authenticator Enumeração de Transporte (enumeração AuthenticatorTransport) - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeração de Requisitos de Chave de Residente (enumeração ResidentKeyRequirement) - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Verificação do usuário - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Criar uma nova credencial - Método [[Create]]](origin, options, sameOriginWithAncestors) - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Considerações sobre o contador de assinaturas - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | GitHub"  

> [!NOTE]
> <span data-ttu-id="7aa30-185">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7aa30-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7aa30-186">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="7aa30-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7aa30-188">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7aa30-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
