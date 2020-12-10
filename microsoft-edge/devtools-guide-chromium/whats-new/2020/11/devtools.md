---
description: Microsoft Edge no Linux, dicas da WebDicas aperfeiçoadas na ferramenta problemas, novos recursos de depuração de trabalho do serviço e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205240"
---
# <span data-ttu-id="87d0b-104">O que há de novo no DevTools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="87d0b-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="87d0b-105">O Microsoft Edge e o Microsoft Edge driver agora estão disponíveis no Linux</span><span class="sxs-lookup"><span data-stu-id="87d0b-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="87d0b-106">O Microsoft Edge dev agora é compatível com o Ubuntu, o Debian, o Fedora e as distribuições do openSUSE.</span><span class="sxs-lookup"><span data-stu-id="87d0b-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="87d0b-107">Baixe e instale o `.deb` pacote ou o encapsulamento do Microsoft Edge `.rpm` diretamente do [site do Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] ou use as ferramentas de gerenciamento de pacotes padrão da sua distribuição Linux.</span><span class="sxs-lookup"><span data-stu-id="87d0b-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="87d0b-108">Se você estiver usando um ambiente Linux em suas soluções de integração contínua e distribuição \ (CI/CD \), o driver do Microsoft Edge também estará disponível no Linux.</span><span class="sxs-lookup"><span data-stu-id="87d0b-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="87d0b-109">Para começar a automatizar o Microsoft Edge dev com o Microsoft Edge Driver, acesse a [página de downloads do driver Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="87d0b-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="87d0b-110">Para obter ajuda com a automação de desenvolvimento do Microsoft Edge juntamente com o Microsoft Edge Driver, navegue para [usar o WebDriver (Chromium) para automação de teste][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="87d0b-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools no Microsoft Edge no Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="87d0b-112">DevTools no Microsoft Edge no Linux</span><span class="sxs-lookup"><span data-stu-id="87d0b-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <span data-ttu-id="87d0b-113">Dicas da webdica e plataforma aprimoradas na ferramenta problemas</span><span class="sxs-lookup"><span data-stu-id="87d0b-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="87d0b-114">Uma ferramenta de código-fonte aberto, [webhint][WebhintMain], fornece comentários em tempo real para sites e páginas da Web locais.</span><span class="sxs-lookup"><span data-stu-id="87d0b-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="87d0b-115">Começando com o [Microsoft Edge versão 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], reveja comentários do webhint na ferramenta [problemas][DevtoolsIssuesIndex] .</span><span class="sxs-lookup"><span data-stu-id="87d0b-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="87d0b-116">Os problemas que aparecem na ferramenta **problemas** agora são mais fáceis de serem analisados com a adição das categorias a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="87d0b-117">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="87d0b-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="87d0b-118">Compatibilidade</span><span class="sxs-lookup"><span data-stu-id="87d0b-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="87d0b-119">Desempenho</span><span class="sxs-lookup"><span data-stu-id="87d0b-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="87d0b-120">Armadilhas</span><span class="sxs-lookup"><span data-stu-id="87d0b-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="87d0b-121">PWA</span><span class="sxs-lookup"><span data-stu-id="87d0b-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="87d0b-122">Segurança</span><span class="sxs-lookup"><span data-stu-id="87d0b-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="87d0b-123">Agora você pode filtrar problemas de terceiros usando uma nova caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="87d0b-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="87d0b-124">A funcionalidade de filtro ajuda você a ocultar problemas relacionados ao código de bibliotecas de terceiros ou de outras fontes.</span><span class="sxs-lookup"><span data-stu-id="87d0b-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="87d0b-125">Para ajudá-lo a revisar os problemas revelados pela [webhint][WebhintMain], a ferramenta **problemas** agora exibe as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="87d0b-126">Trechos de código aprimorados.</span><span class="sxs-lookup"><span data-stu-id="87d0b-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="87d0b-127">Links para outros painéis relevantes.</span><span class="sxs-lookup"><span data-stu-id="87d0b-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="87d0b-128">Links para a documentação para ajudá-lo a corrigir problemas no seu website.</span><span class="sxs-lookup"><span data-stu-id="87d0b-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Ferramenta de problemas" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="87d0b-130">Ferramenta de **problemas**</span><span class="sxs-lookup"><span data-stu-id="87d0b-130">**Issues** tool</span></span>  
:::image-end:::  

## <span data-ttu-id="87d0b-131">Camadas compostas agora estão no modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="87d0b-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="87d0b-132">Agora você pode visualizar o conteúdo das **camadas** juntamente com os valores de índice z e o modelo de objeto do documento \ (dom \).</span><span class="sxs-lookup"><span data-stu-id="87d0b-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="87d0b-133">Esse recurso ajuda você a depurar sem alternar entre as ferramentas de [exibição 3D][Devtools3dViewIndex] e **camadas** com frequência.</span><span class="sxs-lookup"><span data-stu-id="87d0b-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="87d0b-134">Para uma experiência de depuração Visual abrangente, o [modo de exibição 3D e as camadas compostas agora são combinados][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="87d0b-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Painel de camadas compostas" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="87d0b-136">Painel de **camadas compostas**</span><span class="sxs-lookup"><span data-stu-id="87d0b-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="87d0b-137">Definições de variáveis CSS no painel estilos</span><span class="sxs-lookup"><span data-stu-id="87d0b-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="87d0b-138">No painel **estilos** , as [variáveis CSS][MdnUsingCssCustomProperties] agora se vinculam diretamente a cada definição.</span><span class="sxs-lookup"><span data-stu-id="87d0b-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="87d0b-139">Escolha a variável para exibir ou alterar facilmente a definição da variável CSS.</span><span class="sxs-lookup"><span data-stu-id="87d0b-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="87d0b-140">No exemplo, DevTools exibe os atributos CSS do `body` elemento.</span><span class="sxs-lookup"><span data-stu-id="87d0b-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="87d0b-141">Para exibir a definição de variável para a `--theme-body-background` variável CSS, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="87d0b-142">No painel **estilos** , escolha `var(--theme-body-background)` .</span><span class="sxs-lookup"><span data-stu-id="87d0b-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="87d0b-143">O painel **estilos** agora exibe a definição da `--theme-body-background` variável CSS.</span><span class="sxs-lookup"><span data-stu-id="87d0b-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variável CSS vinculada ao estilo" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="87d0b-145">Variável CSS vinculada ao estilo</span><span class="sxs-lookup"><span data-stu-id="87d0b-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variável CSS vinculada ao destino do estilo" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="87d0b-147">Variável CSS vinculada ao destino do estilo</span><span class="sxs-lookup"><span data-stu-id="87d0b-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="87d0b-148">Melhorias na depuração do trabalho do serviço</span><span class="sxs-lookup"><span data-stu-id="87d0b-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="87d0b-149">Os novos recursos a seguir nas ferramentas de [rede](#network-tool), [aplicativo](#application-tool)e [fontes](#sources-tool) ajudam você a criar seu [PWA][ProgressiveWebAppsChromiumIndex].</span><span class="sxs-lookup"><span data-stu-id="87d0b-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsChromiumIndex].</span></span>  <span data-ttu-id="87d0b-150">Use os recursos a seguir quando tiver dificuldades para depurar o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="87d0b-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="87d0b-151">O roteamento de solicitação exibe os `startup` eventos e os `fetch` eventos com base nas solicitações de rede executadas por meio de trabalhadores do serviço.</span><span class="sxs-lookup"><span data-stu-id="87d0b-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="87d0b-152">As linhas do tempo são acessadas a partir da ferramenta **aplicativo** ou **rede** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="87d0b-153">Os cronogramas ajudam quando você está tendo problemas com trabalhadores de serviço e deseja ver se algo está errado com o `startup` evento ou `fetch` .</span><span class="sxs-lookup"><span data-stu-id="87d0b-153">The timelines help when you are having trouble with service workers and want to see if something is wrong with the `startup` or `fetch` event.</span></span>  

### <span data-ttu-id="87d0b-154">Ferramenta do aplicativo</span><span class="sxs-lookup"><span data-stu-id="87d0b-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="87d0b-155">Exibir todas as informações de roteamento de solicitação de trabalho do serviço com o novo link de **solicitações de rede** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="87d0b-156">Para exibir um contexto adicional durante a depuração do trabalho do serviço, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="87d0b-157">Navegue até \*\*\*\*  >  **trabalhadores do serviço**de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87d0b-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="87d0b-158">Escolha **solicitações de rede**.</span><span class="sxs-lookup"><span data-stu-id="87d0b-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Abrir a ferramenta de rede no painel de trabalhadores do serviço" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="87d0b-160">Abrir a ferramenta de **rede** no painel de **trabalhadores do serviço**</span><span class="sxs-lookup"><span data-stu-id="87d0b-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="87d0b-161">A ferramenta **rede** é aberta na **gaveta** e exibe todas as solicitações de rede relacionadas ao trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="87d0b-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="87d0b-162">As solicitações de rede são filtradas usando `is:service-worker-intercepted` .</span><span class="sxs-lookup"><span data-stu-id="87d0b-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Ferramenta de rede na gaveta" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="87d0b-164">Ferramenta de **rede** na **gaveta**</span><span class="sxs-lookup"><span data-stu-id="87d0b-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="87d0b-165">Para retornar a ferramenta de **rede** para o painel superior, feche a **gaveta**.</span><span class="sxs-lookup"><span data-stu-id="87d0b-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Fechar a ferramenta gaveta para retornar a rede" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="87d0b-167">Fechar a ferramenta **gaveta** para retornar a **rede**</span><span class="sxs-lookup"><span data-stu-id="87d0b-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="87d0b-168">Ferramenta de rede</span><span class="sxs-lookup"><span data-stu-id="87d0b-168">Network tool</span></span>  

<span data-ttu-id="87d0b-169">Depurar solicitações de rede executadas por meio de trabalhadores de serviço.</span><span class="sxs-lookup"><span data-stu-id="87d0b-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="87d0b-170">Você também pode abrir solicitações de rede na ferramenta do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="87d0b-171">Para cada solicitação, DevTools exibir as informações a seguir no painel [intervalo][DevtoolsNetworkReferenceViewTimingBreakdownRequest] .</span><span class="sxs-lookup"><span data-stu-id="87d0b-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="87d0b-172">O início de uma solicitação e duração da inicialização.</span><span class="sxs-lookup"><span data-stu-id="87d0b-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="87d0b-173">Alterações no registro de trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="87d0b-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="87d0b-174">O tempo de execução de um `fetch` manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="87d0b-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="87d0b-175">O tempo de execução de todos os `fetch` eventos para carregar um cliente.</span><span class="sxs-lookup"><span data-stu-id="87d0b-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Painel de intervalo" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="87d0b-177">Painel de **intervalo**</span><span class="sxs-lookup"><span data-stu-id="87d0b-177">**Timing** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="87d0b-178">Ferramenta fontes</span><span class="sxs-lookup"><span data-stu-id="87d0b-178">Sources tool</span></span>  

<span data-ttu-id="87d0b-179">Em versões anteriores do Microsoft Edge, o nível de profundidade na pilha de chamadas era limitado ao código JavaScript no seu trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="87d0b-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="87d0b-180">No Microsoft Edge 88, a pilha de chamadas agora exibe o iniciador de solicitações que são executadas por meio do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="87d0b-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="87d0b-181">Para localizar o iniciador da solicitação, use a pilha de chamadas do seu código JavaScript no trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="87d0b-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="87d0b-182">A pilha de chamadas nas figuras a seguir começa com o código JavaScript em seu trabalhador do serviço e exibe uma referência à solicitação de página da Web original como `(index):157` .</span><span class="sxs-lookup"><span data-stu-id="87d0b-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="87d0b-183">Na segunda figura, a referência é escolhida e o iniciador que fez a solicitação foi aberto.</span><span class="sxs-lookup"><span data-stu-id="87d0b-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="87d0b-184">O iniciador na segunda figura é a página da Web.</span><span class="sxs-lookup"><span data-stu-id="87d0b-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="O arquivo service-worker.js e a pilha de chamadas que destacam o remetente da solicitação" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="87d0b-186">O `service-worker.js` remetente da solicitação de realce de arquivo e chamada</span><span class="sxs-lookup"><span data-stu-id="87d0b-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="A página da Web (índice) é o iniciador da solicitação" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="87d0b-188">A `(index)` página da Web é o iniciador da solicitação</span><span class="sxs-lookup"><span data-stu-id="87d0b-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="87d0b-189">Copiar o valor da propriedade de uma solicitação de rede</span><span class="sxs-lookup"><span data-stu-id="87d0b-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="87d0b-190">Na ferramenta **rede** , copie o valor da propriedade de uma solicitação de rede usando a opção novo **valor de cópia** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="87d0b-191">O valor da propriedade é copiado como um valor JSON decodificado.</span><span class="sxs-lookup"><span data-stu-id="87d0b-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="87d0b-192">Em versões anteriores do Microsoft Edge, você precisava copiar um valor usando uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="87d0b-193">Realce o texto inteiro e copie-o.</span><span class="sxs-lookup"><span data-stu-id="87d0b-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="87d0b-194">Armazene o valor como variável global, conforme aplicável, e copie-o do [console][DevtoolsConsoleIndex]do devtools.</span><span class="sxs-lookup"><span data-stu-id="87d0b-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="87d0b-195">Para copiar o valor da propriedade para a área de transferência, navegue até [copiar resposta formatada JSON para a área de transferência][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="87d0b-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="87d0b-196">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1132084][CR1132084].</span><span class="sxs-lookup"><span data-stu-id="87d0b-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copiar valor da propriedade em DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="87d0b-198">Copiar valor da propriedade em DevTools</span><span class="sxs-lookup"><span data-stu-id="87d0b-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Colar valor da propriedade no código do Visual Studio" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="87d0b-200">Colar valor da propriedade no código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="87d0b-200">Paste property value in Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="87d0b-201">Personalizar atalhos de teclado com várias prensas</span><span class="sxs-lookup"><span data-stu-id="87d0b-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="87d0b-202">[Desde a versão 87 do Microsoft Edge][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], você pode personalizar os atalhos de teclado para qualquer ação no devtools.</span><span class="sxs-lookup"><span data-stu-id="87d0b-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="87d0b-203">No Microsoft Edge versão 88, agora você pode criar atalhos de teclado com várias prensas.</span><span class="sxs-lookup"><span data-stu-id="87d0b-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="87d0b-204">Para definir um atalho para uma ação no devtools, navegue até experiências de [configurações][DevtoolsCustomizeIndexSettings]  >  \*\*\*\* e escolha a caixa de seleção ao lado de **habilitar o editor de atalhos de teclado**.</span><span class="sxs-lookup"><span data-stu-id="87d0b-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="87d0b-205">Para obter mais informações sobre como personalizar e editar atalhos, acesse o [recurso experimental do editor de atalhos de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="87d0b-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="87d0b-206">Por exemplo, o realce vermelho exibe um atalho de teclado com várias prensas personalizado para a ação **Iniciar gravação de eventos** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="87d0b-207">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o [Issue #174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="87d0b-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Atalhos de teclado de corda" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="87d0b-209">Atalhos de teclado com várias prensas</span><span class="sxs-lookup"><span data-stu-id="87d0b-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <span data-ttu-id="87d0b-210">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="87d0b-210">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="87d0b-211">Novas ferramentas de visualização do ângulo CSS</span><span class="sxs-lookup"><span data-stu-id="87d0b-211">New CSS angle visualization tools</span></span>  

<span data-ttu-id="87d0b-212">O DevTools agora tem melhor suporte para depuração de ângulo CSS.</span><span class="sxs-lookup"><span data-stu-id="87d0b-212">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="87d0b-213">Quando um elemento HTML na sua página tem ângulo CSS aplicado a ele, um ícone de relógio é exibido ao lado do ângulo na ferramenta **estilos** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-213">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="87d0b-214">Para alternar a sobreposição do relógio, escolha o ícone do relógio.</span><span class="sxs-lookup"><span data-stu-id="87d0b-214">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="87d0b-215">Para alterar o ângulo, escolha qualquer lugar no relógio ou arraste a agulha.</span><span class="sxs-lookup"><span data-stu-id="87d0b-215">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="87d0b-216">Para alterar o valor do ângulo, você também pode usar atalhos de teclado e mouse.</span><span class="sxs-lookup"><span data-stu-id="87d0b-216">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="87d0b-217">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até problemas [1126178][CR1126178] e [1138633][CR1138633].</span><span class="sxs-lookup"><span data-stu-id="87d0b-217">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="87d0b-218">O ângulo CSS a seguir é usado para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="87d0b-218">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Ângulo de CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="87d0b-220">Ângulo de CSS</span><span class="sxs-lookup"><span data-stu-id="87d0b-220">CSS angle</span></span>  
:::image-end:::  

### <span data-ttu-id="87d0b-221">Simular o tamanho da cota de armazenamento no painel armazenamento</span><span class="sxs-lookup"><span data-stu-id="87d0b-221">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="87d0b-222">Agora você pode substituir o tamanho da cota de armazenamento no painel **armazenamento** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-222">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="87d0b-223">Esse recurso permite simular diferentes dispositivos e testar o comportamento de seu site ou aplicativo em cenários de baixa disponibilidade de disco.</span><span class="sxs-lookup"><span data-stu-id="87d0b-223">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="87d0b-224">Para simular a cota de armazenamento, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-224">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="87d0b-225">Navegue até \*\*\*\*  >  **armazenamento**do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87d0b-225">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="87d0b-226">Ative a caixa de seleção **simular cota de armazenamento personalizada** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-226">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="87d0b-227">Digite um número válido.</span><span class="sxs-lookup"><span data-stu-id="87d0b-227">Enter a valid number.</span></span>  
    
<span data-ttu-id="87d0b-228">Para obter mais informações sobre como emular dispositivos móveis e outros recursos no DevTools, navegue para [emular dispositivos móveis no Microsoft Edge devtools ][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="87d0b-228">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="87d0b-229">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até problemas [945786][CR945786] e [1146985][CR1146985].</span><span class="sxs-lookup"><span data-stu-id="87d0b-229">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simular o tamanho da cota de armazenamento" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="87d0b-231">Simular o tamanho da cota de armazenamento</span><span class="sxs-lookup"><span data-stu-id="87d0b-231">Simulate storage quota size</span></span>  
:::image-end:::  

### <span data-ttu-id="87d0b-232">Relatar erros CORS na ferramenta rede</span><span class="sxs-lookup"><span data-stu-id="87d0b-232">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="87d0b-233">Experimente este recurso ao navegar até a [demonstração de erro CORS][GlitchCorsErrors].</span><span class="sxs-lookup"><span data-stu-id="87d0b-233">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="87d0b-234">Abra a ferramenta de **rede** , atualize a página e observe a solicitação de rede CORS com falha.</span><span class="sxs-lookup"><span data-stu-id="87d0b-234">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="87d0b-235">A coluna status exibe o **erro CORS**.</span><span class="sxs-lookup"><span data-stu-id="87d0b-235">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="87d0b-236">Quando você focaliza o erro, a dica de ferramenta agora exibe o código de erro.</span><span class="sxs-lookup"><span data-stu-id="87d0b-236">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="87d0b-237">No Microsoft Edge versão 87 e anterior, DevTools só exibiu status genérico **(com falha)** para erros CORS.</span><span class="sxs-lookup"><span data-stu-id="87d0b-237">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="87d0b-238">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="87d0b-238">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Erros CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="87d0b-240">Erros CORS</span><span class="sxs-lookup"><span data-stu-id="87d0b-240">CORS errors</span></span>  
:::image-end:::  

### <span data-ttu-id="87d0b-241">Atualizações da exibição de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="87d0b-241">Frame details view updates</span></span>  

#### <span data-ttu-id="87d0b-242">Informações de isolamento entre origens na exibição de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="87d0b-242">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="87d0b-243">O status isolado de origem cruzada agora é exibido na seção **isolamento de segurança &** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-243">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="87d0b-244">A nova seção **disponibilidade da API** exibe a disponibilidade de `SharedArrayBuffer` s \ (sab \) e se os buffers podem ser compartilhados usando `postMessage()` .</span><span class="sxs-lookup"><span data-stu-id="87d0b-244">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="87d0b-245">Um aviso de substituição será exibido se o SAB e `postMessage()` estiver disponível no momento, mas o contexto não estiver isolado na origem.</span><span class="sxs-lookup"><span data-stu-id="87d0b-245">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="87d0b-246">Para obter mais informações sobre o isolamento entre origens e por que é necessário para recursos como `SharedArrayBuffers` , navegue até [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="87d0b-246">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="87d0b-247">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="87d0b-247">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informações entre origens" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="87d0b-249">Informações entre origens</span><span class="sxs-lookup"><span data-stu-id="87d0b-249">Cross-origin information</span></span>  
:::image-end:::  

#### <span data-ttu-id="87d0b-250">Novas informações de funcionários da Web na exibição detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="87d0b-250">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="87d0b-251">O DevTools agora organiza os funcionários da Web no quadro pai relevante.</span><span class="sxs-lookup"><span data-stu-id="87d0b-251">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="87d0b-252">Por exemplo, se o `someName` quadro criar `worker.js` , `worker.js` aparecerá abaixo `someName` na lista de **quadros** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-252">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="87d0b-253">Para exibir os detalhes do Web Worker, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-253">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="87d0b-254">Ferramenta abrir **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-254">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="87d0b-255">Expanda um quadro que contém funcionários da Web.</span><span class="sxs-lookup"><span data-stu-id="87d0b-255">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="87d0b-256">Expanda a árvore **funcionários** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-256">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="87d0b-257">Escolha um trabalhador.</span><span class="sxs-lookup"><span data-stu-id="87d0b-257">Choose a worker.</span></span>  
    
<span data-ttu-id="87d0b-258">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até problemas [1122507][CR1122507] e [1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="87d0b-258">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informações de funcionários da Web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="87d0b-260">Informações de funcionários da Web</span><span class="sxs-lookup"><span data-stu-id="87d0b-260">Web workers information</span></span>  
:::image-end:::  

#### <span data-ttu-id="87d0b-261">Exibir detalhes do quadro aberto para janelas abertas</span><span class="sxs-lookup"><span data-stu-id="87d0b-261">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="87d0b-262">O DevTools agora organiza [janelas][MdnWindowConstructors] abertas sob o [quadro][MdnWindowFrames]pai relevante.</span><span class="sxs-lookup"><span data-stu-id="87d0b-262">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="87d0b-263">Por exemplo, se o `top` quadro abrir uma `Window` a para `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , o botão `Window` aparecerá abaixo `top` na lista de **quadros** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-263">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="87d0b-264">Para revelar o quadro responsável pela abertura de outra janela na ferramenta **elementos** , conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-264">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="87d0b-265">Abra a árvore de **quadros** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-265">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="87d0b-266">Expanda **janelas abertas** e escolha o `Window` para o quadro pai que você deseja saber.</span><span class="sxs-lookup"><span data-stu-id="87d0b-266">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="87d0b-267">Escolha o link de **quadro aberto** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-267">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="87d0b-268">Os detalhes são exibidos sobre qual quadro causou a abertura de outro `Window` .</span><span class="sxs-lookup"><span data-stu-id="87d0b-268">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="87d0b-269">Para revelar o abredor na ferramenta **elementos** , conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-269">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="87d0b-270">Abra a árvore de **quadros** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-270">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="87d0b-271">Escolha uma janela aberta para abrir os `Window` detalhes.</span><span class="sxs-lookup"><span data-stu-id="87d0b-271">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="87d0b-272">Escolha o link de **quadro aberto** .</span><span class="sxs-lookup"><span data-stu-id="87d0b-272">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="87d0b-273">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1107766][CR1107766].</span><span class="sxs-lookup"><span data-stu-id="87d0b-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Detalhes do quadro aberto" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="87d0b-275">Detalhes do quadro aberto</span><span class="sxs-lookup"><span data-stu-id="87d0b-275">Opened frame details</span></span>  
:::image-end:::  

### <span data-ttu-id="87d0b-276">Copiar StackTrace para o iniciador de rede</span><span class="sxs-lookup"><span data-stu-id="87d0b-276">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="87d0b-277">Para copiar o StackTrace para a área de transferência, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="87d0b-277">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="87d0b-278">Abra o menu contextual \ (clique com o botão direito do mouse \).</span><span class="sxs-lookup"><span data-stu-id="87d0b-278">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="87d0b-279">Escolha **copiar**  >  **StackTrace de cópia**.</span><span class="sxs-lookup"><span data-stu-id="87d0b-279">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="87d0b-280">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1139615][CR1139615].</span><span class="sxs-lookup"><span data-stu-id="87d0b-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copiar StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="87d0b-282">Copiar StackTrace</span><span class="sxs-lookup"><span data-stu-id="87d0b-282">Copy stacktrace</span></span>  
:::image-end:::  

### <span data-ttu-id="87d0b-283">Visualizar o valor da variável WASM ao mouseover</span><span class="sxs-lookup"><span data-stu-id="87d0b-283">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="87d0b-284">Use esse recurso para analisar o valor de uma variável Webassembly \ (WASM \) quando o código for pausado.</span><span class="sxs-lookup"><span data-stu-id="87d0b-284">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="87d0b-285">Para exibir o valor atual de uma variável, passe o mouse sobre uma variável.</span><span class="sxs-lookup"><span data-stu-id="87d0b-285">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="87d0b-286">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até problemas [1058836][CR1058836] e [1071432][CR1071432].</span><span class="sxs-lookup"><span data-stu-id="87d0b-286">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Visualização de WASM variável ao mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="87d0b-288">Visualização de WASM variável ao mouseover</span><span class="sxs-lookup"><span data-stu-id="87d0b-288">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <span data-ttu-id="87d0b-289">Unidades de medida consistentes para tamanhos de arquivos e memória</span><span class="sxs-lookup"><span data-stu-id="87d0b-289">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="87d0b-290">O DevTools agora usa consistentemente `kB` para exibir tamanhos de arquivos e memória.</span><span class="sxs-lookup"><span data-stu-id="87d0b-290">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="87d0b-291">DevTools anteriormente `kB` em combinação e `KiB` .</span><span class="sxs-lookup"><span data-stu-id="87d0b-291">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="87d0b-292">ou quilobyte \ (10 ^ 3 ou 1000 bytes \)</span><span class="sxs-lookup"><span data-stu-id="87d0b-292">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="87d0b-293">ou Kibibyte \ (2 ^ 10 ou 1024 bytes \)</span><span class="sxs-lookup"><span data-stu-id="87d0b-293">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="87d0b-294">Por exemplo, a ferramenta de **rede** anteriormente usada `kB` em rótulos, mas usada `KiB` em cálculos.</span><span class="sxs-lookup"><span data-stu-id="87d0b-294">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="87d0b-295">Seus comentários mostraram que essa inconsistência causou confusão.</span><span class="sxs-lookup"><span data-stu-id="87d0b-295">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="87d0b-296">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1035309][CR1035309].</span><span class="sxs-lookup"><span data-stu-id="87d0b-296">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <span data-ttu-id="87d0b-297">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="87d0b-297">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="87d0b-298">Se estiver no Windows, Linux ou macOS, considere o uso do [Microsoft Edge Preview Channels] [MicrosoftEdgePreviewChannels] como navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="87d0b-298">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="87d0b-299">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="87d0b-299">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="87d0b-300">Como entrar em contato com o Microsoft Edge DevTools equipe</span><span class="sxs-lookup"><span data-stu-id="87d0b-300">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Modo de exibição 3D | Documentos da Microsoft"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Visão geral do console | Documentos da Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar o editor de atalhos de teclado-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Ativar camadas compostas no modo de exibição 3D – recursos experimentais | Documentos da Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge | Documentos da Microsoft"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copiar resposta formatada JSON para a área de transferência-referência de análise da rede | Documentos da Microsoft"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Exibir a divisão de tempo de uma solicitação-referência de análise de rede | Documentos da Microsoft"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Use o WebDriver (Chromium) para automação de teste | Documentos da Microsoft"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows | Documentos da Microsoft"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Personalizar atalhos de teclado em configurações – novidades do DevTools (Microsoft Edge 87) | Documentos da Microsoft"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "webhint feedback no painel problemas-novidades do DevTools (Microsoft Edge 85) | Documentos da Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Baixar o WebDriver | Desenvolvedor da Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Baixar canais do Microsoft Edge Insider"  

[VisualStudioCode]: https://code.visualstudio.com "Código do Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"  

[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir a personalização de atalhos de teclado/associações de chave | Erros de Chromium"  
[CR945786]: https://crbug.com/945786 "Problema 945786: DevTools: permitir a substituição de Navigator. Storage. Estimate () | Erros de Chromium"  
[CR1029427]: https://crbug.com/1029427 "Problema 1029427: Reduza a sobrecarga de desempenho do despacho de mensagens de protocolo no front-end | Erros de Chromium"  
[CR1035309]: https://crbug.com/1035309 "Problema 1035309: DevTools deve usar consistentemente MB para significar megabyte, não mebibyte | Erros de Chromium"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: suporte para a depuração COOP/COEP no DevTools | Erros de Chromium"  
[CR1058836]: https://crbug.com/1058836 "Problema 1058836: problemas com o UX ao WASM a depuração | Erros de Chromium"  
[CR1071432]: https://crbug.com/1071432 "Problema 1071432: ☂️ experiência do desenvolvedor básico do WASM | Erros de Chromium"  
[CR1107766]: https://crbug.com/1107766 "Problema 1107766: exibir informações sobre quadros gerados por ' Window. Open () ' na árvore de quadros | Erros de Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: informações sobre o trabalhador da superfície no modo de exibição árvore de quadros | Erros de Chromium"  
[CR1126178]: https://crbug.com/1126178 "Problema 1126178: ☂ DevTools: CSS <tipo> componentes Erros de Chromium"  
[CR1130556]: https://crbug.com/1130556 "Problema 1130556: DevTools: testar fallbacks de imagem (emulação) | Erros de Chromium"  
[CR1132084]: https://crbug.com/1132084 "Problema 1132084: não há uma maneira fácil de copiar a carga de solicitação JSON | Erros de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: ferramenta de flexbox | Erros de Chromium"  
[CR1138633]: https://crbug.com/1138633 "Problema 1138633: DevTools: o ângulo de <de CSS> componente deve refletir a aparência da propriedade contida na tela de fundo do relógio | Erros de Chromium"  
[CR1139615]: https://crbug.com/1139615 "Problema 1139615: o iniciador de rede deve oferecer a capacidade de copiar o rastreamento de pilha | Erros de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: relatar a disponibilidade da API restringida na exibição de detalhes do quadro | Erros de Chromium"  
[CR1139945]: https://crbug.com/1139945 "Problema 1139945: ícones para propriedades de CSS do flexbox no painel estilos | Erros de Chromium"  
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: melhorar o relatório de erros CORS no DevTools | Erros de Chromium"  
[CR1144090]: https://crbug.com/1144090 "Problema 1144090: Adicione estilos Flex decoradores à árvore de elementos | Erros de Chromium"  
[CR1146985]: https://crbug.com/1146985 "Problema 1146985: o texto limpo ainda está sendo visto na caixa de texto da seção "armazenamento" da janela "ferramentas de desenvolvimento" Erros de Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Erros CORS | Problema"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Compartilhamento de recursos entre origens (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propriedades personalizadas CSS (variáveis) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Construtores-janela | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window. frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Acessibilidade | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilidade | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Desempenho | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Armadilhas | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Segurança | webhint"  

> [!NOTE]
> <span data-ttu-id="87d0b-351">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="87d0b-351">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="87d0b-352">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/11/devtools/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="87d0b-352">The original page is found [here](https://developers.google.com/web/updates/2020/11/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="87d0b-354">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="87d0b-354">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
