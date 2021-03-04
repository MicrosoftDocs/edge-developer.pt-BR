---
description: Microsoft Edge no Linux, webhints aperfeiçoadas na ferramenta Issues, novos recursos de depuração de trabalho do serviço e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f56586fa77e34da7884d9d7c565b8cbcc4106c4a
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387289"
---
# <a name="whats-new-in-devtools-microsoft-edge-88"></a><span data-ttu-id="a63c3-104">O que há de novo no DevTools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="a63c3-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="microsoft-edge-and-microsoft-edge-driver-now-available-on-linux"></a><span data-ttu-id="a63c3-105">O Microsoft Edge e o Microsoft Edge Driver agora estão disponíveis no Linux</span><span class="sxs-lookup"><span data-stu-id="a63c3-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="a63c3-106">O Microsoft Edge Dev agora é compatível com o Ubuntu, o Debian, o Fedora e as distribuições do openSUSE.</span><span class="sxs-lookup"><span data-stu-id="a63c3-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="a63c3-107">Baixe e instale o pacote `.deb`ou `.rpm` do Microsoft Edge Dev diretamente do site [Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] ou use as ferramentas de gerenciamento de pacote padrão de sua distribuição Linux.</span><span class="sxs-lookup"><span data-stu-id="a63c3-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="a63c3-108">Se você estiver usando um ambiente Linux em suas soluções de integração e entrega contínuas (CI/CD\), o Microsoft Edge Driver também está disponível no Linux.</span><span class="sxs-lookup"><span data-stu-id="a63c3-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="a63c3-109">Para começar a automatizar o Microsoft Edge Dev com o Microsoft Edge Driver, navegue até a [página de downloads do Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="a63c3-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="a63c3-110">Para obter ajuda com a automação do Microsoft Edge Dev junto com o Microsoft Edge Driver, navegue até [Usar WebDriver (Chromium) para automação de teste][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="a63c3-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools no Microsoft Edge no Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="a63c3-112">DevTools no Microsoft Edge no Linux</span><span class="sxs-lookup"><span data-stu-id="a63c3-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <a name="improved-webhint-and-platform-tips-in-the-issues-tool"></a><span data-ttu-id="a63c3-113">Dica da web e plataforma aprimoradas na ferramenta Issues</span><span class="sxs-lookup"><span data-stu-id="a63c3-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="a63c3-114">Uma ferramenta de código-fonte aberto, [webhint][WebhintMain], fornece comentários em tempo real para sites e páginas da Web locais.</span><span class="sxs-lookup"><span data-stu-id="a63c3-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="a63c3-115">A partir do [Microsoft Edge versão 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], reveja comentários de webhint na ferramenta [Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="a63c3-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="a63c3-116">Os problemas que aparecem na ferramenta **Issues** agora estão mais fáceis de serem analisados com a adição das categorias a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="a63c3-117">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="a63c3-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="a63c3-118">Compatibilidade</span><span class="sxs-lookup"><span data-stu-id="a63c3-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="a63c3-119">Desempenho</span><span class="sxs-lookup"><span data-stu-id="a63c3-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="a63c3-120">Armadilhas</span><span class="sxs-lookup"><span data-stu-id="a63c3-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="a63c3-121">PWA</span><span class="sxs-lookup"><span data-stu-id="a63c3-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="a63c3-122">Segurança</span><span class="sxs-lookup"><span data-stu-id="a63c3-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="a63c3-123">Agora você pode filtrar problemas de terceiros usando uma nova caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="a63c3-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="a63c3-124">A funcionalidade de filtro ajuda você a ocultar problemas relacionados ao código de bibliotecas de terceiros ou de outras fontes.</span><span class="sxs-lookup"><span data-stu-id="a63c3-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="a63c3-125">Para ajudá-lo a revisar os problemas revelados pela [webhint][WebhintMain], a ferramenta **Problemas** agora exibe as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="a63c3-126">Trechos de código aprimorados.</span><span class="sxs-lookup"><span data-stu-id="a63c3-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="a63c3-127">Links para outros painéis relevantes.</span><span class="sxs-lookup"><span data-stu-id="a63c3-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="a63c3-128">Links para a documentação para ajudá-lo a corrigir problemas no seu website.</span><span class="sxs-lookup"><span data-stu-id="a63c3-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Ferramenta Issues" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="a63c3-130">Ferramenta **Issues**</span><span class="sxs-lookup"><span data-stu-id="a63c3-130">**Issues** tool</span></span>  
:::image-end:::  

## <a name="composited-layers-are-now-in-3d-view"></a><span data-ttu-id="a63c3-131">Camadas Compostas agora estão no modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="a63c3-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="a63c3-132">Agora você pode visualizar o conteúdo das **Camadas** juntamente com os valores de índice z e o Modelo de Objeto do Documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="a63c3-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="a63c3-133">Esse recurso ajuda você a depurar sem alternar entre as ferramentas[exibição 3D][Devtools3dViewIndex] e **Camadas** com frequência.</span><span class="sxs-lookup"><span data-stu-id="a63c3-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="a63c3-134">Para uma experiência de depuração visual abrangente, o [Modo de exibição 3D e as camadas compostas agora são combinados][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="a63c3-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Painel de Camadas compostas" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="a63c3-136">Painel de **Camadas Compostas**</span><span class="sxs-lookup"><span data-stu-id="a63c3-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <a name="css-variable-definitions-in-styles-pane"></a><span data-ttu-id="a63c3-137">Definições de variáveis CSS no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="a63c3-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="a63c3-138">No painel **Estilos**, as [variáveis CSS][MdnUsingCssCustomProperties] agora se vinculam diretamente a cada definição.</span><span class="sxs-lookup"><span data-stu-id="a63c3-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="a63c3-139">Escolha a variável para exibir ou alterar facilmente a definição da variável CSS.</span><span class="sxs-lookup"><span data-stu-id="a63c3-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="a63c3-140">No exemplo, DevTools exibe os atributos CSS do elemento`body`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="a63c3-141">Para exibir a definição de variável para a `--theme-body-background` variável CSS, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="a63c3-142">No painel **Estilos**, escolha `var(--theme-body-background)`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="a63c3-143">O painel **estilos** agora exibe a definição da `--theme-body-background` variável CSS.</span><span class="sxs-lookup"><span data-stu-id="a63c3-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variável CSS vinculada ao estilo" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="a63c3-145">Variável CSS vinculada ao estilo</span><span class="sxs-lookup"><span data-stu-id="a63c3-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variável CSS vinculada ao destino do estilo" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="a63c3-147">Variável CSS vinculada ao destino do estilo</span><span class="sxs-lookup"><span data-stu-id="a63c3-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="service-worker-debugging-improvements"></a><span data-ttu-id="a63c3-148">Melhorias na depuração do trabalho do serviço</span><span class="sxs-lookup"><span data-stu-id="a63c3-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="a63c3-149">Os novos recursos a seguir nas ferramentas [Rede](#network-tool), [Aplicativo](#application-tool)e [Fontes](#sources-tool) ajudam você a criar seu [PWA][ProgressiveWebAppsChromiumIndex].</span><span class="sxs-lookup"><span data-stu-id="a63c3-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsChromiumIndex].</span></span>  <span data-ttu-id="a63c3-150">Use os recursos a seguir quando tiver dificuldades para depurar o Trabalho de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a63c3-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="a63c3-151">O roteamento de solicitação exibe os eventos `startup` e os eventos `fetch` com base nas solicitações de rede executadas por meio de Trabalho de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a63c3-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="a63c3-152">As linhas do tempo são acessadas a partir da ferramenta **Aplicativo** ou **Rede**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="a63c3-153">Os cronogramas ajudam quando você está tendo problemas com Trabalho de Serviço e deseja ver se algo está errado com o evento `startup` ou `fetch`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-153">The timelines help when you are having trouble with service workers and want to see if something is wrong with the `startup` or `fetch` event.</span></span>  

### <a name="application-tool"></a><span data-ttu-id="a63c3-154">Ferramenta Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a63c3-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="a63c3-155">Exibir todas as informações de roteamento de solicitação de trabalho do serviço com o novo link**Solicitações de rede**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="a63c3-156">Para exibir um contexto adicional durante a depuração do trabalho do serviço, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="a63c3-157">Navegue até **Aplicativo**  >  **Trabalho de Serviço**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="a63c3-158">Escolha **Solicitações de rede**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Abra a ferramenta de rede no painel de Trabalho de Serviço" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="a63c3-160">Abra a ferramenta **Rede** no painel **Trabalho de Serviço**</span><span class="sxs-lookup"><span data-stu-id="a63c3-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="a63c3-161">A ferramenta **Rede** é aberta na **gaveta** e exibe todas as solicitações de rede relacionadas ao Trabalho de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a63c3-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="a63c3-162">As solicitações de rede são filtradas usando `is:service-worker-intercepted`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Ferramenta Rede na gaveta" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="a63c3-164">Ferramenta **Rede** na **gaveta**</span><span class="sxs-lookup"><span data-stu-id="a63c3-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="a63c3-165">Para retornar à ferramenta **Rede** para o painel superior, feche a **Gaveta**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Feche a gaveta para retornar à ferramenta Rede" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="a63c3-167">Feche a **gaveta** para retornar à ferramenta **Rede**</span><span class="sxs-lookup"><span data-stu-id="a63c3-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <a name="network-tool"></a><span data-ttu-id="a63c3-168">Ferramenta Rede</span><span class="sxs-lookup"><span data-stu-id="a63c3-168">Network tool</span></span>  

<span data-ttu-id="a63c3-169">Depure solicitações de rede executadas por meio de trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="a63c3-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="a63c3-170">Você também pode abrir solicitações de rede na ferramenta **Aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="a63c3-171">Para cada solicitação, DevTools exibe as informações a seguir no painel [Tempo][DevtoolsNetworkReferenceViewTimingBreakdownRequest].</span><span class="sxs-lookup"><span data-stu-id="a63c3-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="a63c3-172">O início de uma solicitação e a duração da inicialização.</span><span class="sxs-lookup"><span data-stu-id="a63c3-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="a63c3-173">Alterações no registro de trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="a63c3-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="a63c3-174">O tempo de execução de um manipulador de eventos `fetch`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="a63c3-175">O tempo de execução de todos os eventos `fetch` para carregar um cliente.</span><span class="sxs-lookup"><span data-stu-id="a63c3-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Painel Tempo" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="a63c3-177">Painel **Tempo**</span><span class="sxs-lookup"><span data-stu-id="a63c3-177">**Timing** pane</span></span>  
:::image-end:::  

### <a name="sources-tool"></a><span data-ttu-id="a63c3-178">Ferramenta Fontes</span><span class="sxs-lookup"><span data-stu-id="a63c3-178">Sources tool</span></span>  

<span data-ttu-id="a63c3-179">Em versões anteriores do Microsoft Edge, o nível de profundidade na pilha de chamadas era limitado ao código JavaScript no seu trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="a63c3-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="a63c3-180">No Microsoft Edge 88, a pilha de chamadas agora exibe o iniciador de solicitações que são executadas por meio do seu trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="a63c3-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="a63c3-181">Para localizar o iniciador da solicitação, use a pilha de chamadas do seu código JavaScript no trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="a63c3-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="a63c3-182">A pilha de chamadas nas figuras a seguir começa com o código JavaScript em seu trabalho de serviço e exibe uma referência à solicitação de página da Web original como `(index):157`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="a63c3-183">Na segunda figura, a referência é escolhida e abre o iniciador que fez a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a63c3-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="a63c3-184">O iniciador na segunda figura é a página da Web.</span><span class="sxs-lookup"><span data-stu-id="a63c3-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="O arquivo service-worker.js e a pilha de chamadas que destacam o remetente da solicitação" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="a63c3-186">O arquivo `service-worker.js` e a pilha de chamadas que destacam o remetente da solicitação</span><span class="sxs-lookup"><span data-stu-id="a63c3-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="A página da Web (índice) é o iniciador da solicitação" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="a63c3-188">A página da Web `(index)` é o iniciador da solicitação</span><span class="sxs-lookup"><span data-stu-id="a63c3-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="copy-property-value-of-a-network-request"></a><span data-ttu-id="a63c3-189">Copiar o valor da propriedade de uma solicitação de rede</span><span class="sxs-lookup"><span data-stu-id="a63c3-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="a63c3-190">Na ferramenta **Rede**, copie o valor da propriedade de uma solicitação de rede usando a opção nova **Valor de cópia**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="a63c3-191">O valor da propriedade é copiado como um valor JSON decodificado.</span><span class="sxs-lookup"><span data-stu-id="a63c3-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="a63c3-192">Em versões anteriores do Microsoft Edge, você precisava copiar um valor usando uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="a63c3-193">Realce o texto inteiro e copie-o.</span><span class="sxs-lookup"><span data-stu-id="a63c3-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="a63c3-194">Armazene o valor como variável global, conforme aplicável, e copie-o do [Console][DevtoolsConsoleIndex]do Devtools.</span><span class="sxs-lookup"><span data-stu-id="a63c3-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="a63c3-195">Para copiar o valor da propriedade para a área de transferência, navegue até [Copiar resposta formatada JSON para a área de transferência][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="a63c3-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="a63c3-196">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1132084][CR1132084].</span><span class="sxs-lookup"><span data-stu-id="a63c3-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copiar valor da propriedade em DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="a63c3-198">Copiar valor da propriedade em DevTools</span><span class="sxs-lookup"><span data-stu-id="a63c3-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Colar valor da propriedade no Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="a63c3-200">Colar valor da propriedade no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a63c3-200">Paste property value in Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="customize-multi-press-keyboard-shortcuts"></a><span data-ttu-id="a63c3-201">Personalizar atalhos de teclado com várias prensas</span><span class="sxs-lookup"><span data-stu-id="a63c3-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="a63c3-202">[Desde a versão 87 do Microsoft Edge][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], você pode personalizar os atalhos de teclado para qualquer ação no DevTools.</span><span class="sxs-lookup"><span data-stu-id="a63c3-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="a63c3-203">No Microsoft Edge versão 88, agora você pode criar atalhos de teclado com várias prensas.</span><span class="sxs-lookup"><span data-stu-id="a63c3-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="a63c3-204">Para definir um atalho para uma ação no DevTools, navegue até [Configurações][DevtoolsCustomizeIndexSettings] > **Experimentos** e escolha a caixa de seleção ao lado de **Habilitar o editor de atalhos de teclado**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="a63c3-205">Para obter mais informações sobre como personalizar e editar atalhos, acesse o [recurso experimental do editor de atalhos de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="a63c3-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="a63c3-206">Por exemplo, o realce vermelho exibe um atalho de teclado personalizado com várias prensas para a ação **Iniciar gravação de eventos**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="a63c3-207">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o [Issue #174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="a63c3-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Atalhos de teclado de corda" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="a63c3-209">Atalhos de teclado com várias prensas</span><span class="sxs-lookup"><span data-stu-id="a63c3-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <a name="devtools-now-match-browser-language"></a><span data-ttu-id="a63c3-210">O DevTools agora corresponde ao idioma do navegador</span><span class="sxs-lookup"><span data-stu-id="a63c3-210">DevTools now match browser language</span></span>  

<span data-ttu-id="a63c3-211">No Microsoft Edge versão 87, se você ativou a configuração de **idioma do navegador correspondente** nas [configurações do DevTools][DevtoolsCustomizeIndexSettings], o DevTools não correspondia ao idioma do navegador.</span><span class="sxs-lookup"><span data-stu-id="a63c3-211">In Microsoft Edge version 87, if you turned on the **Match browser language** setting in [DevTools Settings][DevtoolsCustomizeIndexSettings], DevTools did not match the browser language.</span></span>  <span data-ttu-id="a63c3-212">No Microsoft Edge versão 88, o DevTools agora corresponde ao idioma do navegador se você ativar a configuração de **Idioma do navegador correspondente**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-212">In Microsoft Edge version 88, DevTools now matches the browser language if you turn on the **Match browser language** setting.</span></span>  <span data-ttu-id="a63c3-213">Para obter mais informações sobre a configuração **corresponder ao idioma do navegador** do DevTools, navegue até [Alterar as configurações de idioma do DevTools][DevtoolsCustomizeLocalization].</span><span class="sxs-lookup"><span data-stu-id="a63c3-213">For more information about the **Match browser language** DevTools Setting, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="Corresponder a configuração DevTools ao idioma do navegador em japonês" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   <span data-ttu-id="a63c3-215">Configuração **Corresponder ao idioma do navegador** em Japonês</span><span class="sxs-lookup"><span data-stu-id="a63c3-215">**Match browser language** DevTools setting in Japanese</span></span>  
:::image-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="a63c3-216">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="a63c3-216">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-css-angle-visualization-tools"></a><span data-ttu-id="a63c3-217">Novas ferramentas de visualização do ângulo CSS</span><span class="sxs-lookup"><span data-stu-id="a63c3-217">New CSS angle visualization tools</span></span>  

<span data-ttu-id="a63c3-218">O DevTools agora tem melhor suporte para depuração de ângulos CSS.</span><span class="sxs-lookup"><span data-stu-id="a63c3-218">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="a63c3-219">Quando um elemento HTML na sua página tem ângulo CSS aplicado a ele, um ícone de relógio é exibido ao lado do ângulo na ferramenta **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-219">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="a63c3-220">Para alternar a sobreposição do relógio, escolha o ícone do relógio.</span><span class="sxs-lookup"><span data-stu-id="a63c3-220">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="a63c3-221">Para alterar o ângulo, escolha qualquer lugar no relógio ou arraste a agulha.</span><span class="sxs-lookup"><span data-stu-id="a63c3-221">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="a63c3-222">Para alterar o valor do ângulo, você também pode usar atalhos de teclado e mouse.</span><span class="sxs-lookup"><span data-stu-id="a63c3-222">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="a63c3-223">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até Issues [1126178][CR1126178] e [1138633][CR1138633].</span><span class="sxs-lookup"><span data-stu-id="a63c3-223">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="a63c3-224">O ângulo CSS a seguir é usado para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="a63c3-224">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Ângulo de CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="a63c3-226">Ângulo de CSS</span><span class="sxs-lookup"><span data-stu-id="a63c3-226">CSS angle</span></span>  
:::image-end:::  

### <a name="simulate-storage-quota-size-in-the-storage-pane"></a><span data-ttu-id="a63c3-227">Simule o tamanho da cota de armazenamento no painel Armazenamento</span><span class="sxs-lookup"><span data-stu-id="a63c3-227">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="a63c3-228">Agora você pode substituir o tamanho da cota de armazenamento no painel **Armazenamento**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-228">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="a63c3-229">Esse recurso permite simular diferentes dispositivos e testar o comportamento de seu site ou aplicativo em cenários de baixa disponibilidade de disco.</span><span class="sxs-lookup"><span data-stu-id="a63c3-229">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="a63c3-230">Para simular a cota de armazenamento, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-230">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="a63c3-231">Navegue até o **Aplicativo**  >  **Armazenamento**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-231">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="a63c3-232">Ative a caixa de seleção **Simular cota de armazenamento personalizada**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-232">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="a63c3-233">Digite um número válido.</span><span class="sxs-lookup"><span data-stu-id="a63c3-233">Enter a valid number.</span></span>  
    
<span data-ttu-id="a63c3-234">Para obter mais informações sobre como emular dispositivos móveis e outros recursos no DevTools, navegue para [Emular dispositivos móveis no DevTools do Microsoft Edge][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="a63c3-234">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="a63c3-235">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até Issues [945786][CR945786] e [1146985][CR1146985].</span><span class="sxs-lookup"><span data-stu-id="a63c3-235">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simular o tamanho da cota de armazenamento" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="a63c3-237">Simular o tamanho da cota de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a63c3-237">Simulate storage quota size</span></span>  
:::image-end:::  

### <a name="report-cors-errors-in-the-network-tool"></a><span data-ttu-id="a63c3-238">Relatar erros CORS na ferramenta Rede</span><span class="sxs-lookup"><span data-stu-id="a63c3-238">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="a63c3-239">Experimente este recurso ao navegar até a [demonstração de erro CORS][GlitchCorsErrors].</span><span class="sxs-lookup"><span data-stu-id="a63c3-239">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="a63c3-240">Abra a ferramenta de **Rede**, atualize a página e observe a solicitação de rede CORS com falha.</span><span class="sxs-lookup"><span data-stu-id="a63c3-240">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="a63c3-241">A coluna status exibe o **erro CORS**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-241">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="a63c3-242">Quando você focaliza o erro, a dica de ferramenta agora exibe o código de erro.</span><span class="sxs-lookup"><span data-stu-id="a63c3-242">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="a63c3-243">No Microsoft Edge versão 87 e anterior, o DevTools só exibia o status genérico **(com falha)** para erros CORS.</span><span class="sxs-lookup"><span data-stu-id="a63c3-243">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="a63c3-244">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="a63c3-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Erros CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="a63c3-246">Erros CORS</span><span class="sxs-lookup"><span data-stu-id="a63c3-246">CORS errors</span></span>  
:::image-end:::  

### <a name="frame-details-view-updates"></a><span data-ttu-id="a63c3-247">Atualizações da exibição de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="a63c3-247">Frame details view updates</span></span>  

#### <a name="cross-origin-isolation-information-in-the-frame-details-view"></a><span data-ttu-id="a63c3-248">Informações de isolamento de origem cruzada na visualização de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="a63c3-248">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="a63c3-249">O status isolado de origem cruzada agora é exibido na seção **Isolamento e Segurança**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-249">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="a63c3-250">A nova seção **disponibilidade da API** exibe a disponibilidade de `SharedArrayBuffer`s\ (SAB\) e se os buffers podem ser compartilhados usando `postMessage()`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-250">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="a63c3-251">Um aviso de substituição será exibido se o SAB e `postMessage()` estiverem disponíveis no momento, mas o contexto não estiver isolado na origem.</span><span class="sxs-lookup"><span data-stu-id="a63c3-251">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="a63c3-252">Para obter mais informações sobre o isolamento entre origens e por que é necessário para recursos como `SharedArrayBuffers`, navegue até [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="a63c3-252">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="a63c3-253">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="a63c3-253">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informações entre origens" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="a63c3-255">Informações entre origens</span><span class="sxs-lookup"><span data-stu-id="a63c3-255">Cross-origin information</span></span>  
:::image-end:::  

#### <a name="new-web-workers-information-in-the-frame-details-view"></a><span data-ttu-id="a63c3-256">Novas informações de Trabalhos na Web na visualização de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="a63c3-256">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="a63c3-257">O DevTools agora organiza os Trabalhadores da Web no quadro pai relevante.</span><span class="sxs-lookup"><span data-stu-id="a63c3-257">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="a63c3-258">Por exemplo, se o `someName`quadro criar `worker.js`, `worker.js` aparecerá abaixo `someName` na lista **Quadros**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-258">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="a63c3-259">Para exibir os detalhes do trabalho da web, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-259">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="a63c3-260">Abra a ferramenta **Aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-260">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="a63c3-261">Expanda um quadro que contém trabalhos da web.</span><span class="sxs-lookup"><span data-stu-id="a63c3-261">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="a63c3-262">Expanda a árvore **Trabalhos**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-262">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="a63c3-263">Escolha um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a63c3-263">Choose a worker.</span></span>  
    
<span data-ttu-id="a63c3-264">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até Issues [1122507][CR1122507] e [1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="a63c3-264">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informações de trabalho da web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="a63c3-266">Informações de trabalho da web</span><span class="sxs-lookup"><span data-stu-id="a63c3-266">Web workers information</span></span>  
:::image-end:::  

#### <a name="display-opener-frame-details-for-opened-windows"></a><span data-ttu-id="a63c3-267">Exibir detalhes do quadro aberto para janelas abertas</span><span class="sxs-lookup"><span data-stu-id="a63c3-267">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="a63c3-268">O DevTools agora organiza [Janelas][MdnWindowConstructors] abertas sob o [quadro][MdnWindowFrames]pai relevante.</span><span class="sxs-lookup"><span data-stu-id="a63c3-268">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="a63c3-269">Por exemplo, se o `top`quadro abrir uma`Window` para `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, o botão `Window` aparecerá abaixo `top` na lista **Quadros**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-269">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="a63c3-270">Para revelar o quadro responsável pela abertura de outra janela na ferramenta **Elementos**, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-270">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="a63c3-271">Abra a árvore **Quadros**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-271">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="a63c3-272">Expanda **Janelas Abertas** e escolha `Window` para o quadro pai que você deseja saber.</span><span class="sxs-lookup"><span data-stu-id="a63c3-272">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="a63c3-273">Escolha o link do**Quadro Aberto**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-273">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="a63c3-274">Os detalhes são exibidos sobre qual quadro causou a abertura do outro `Window`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-274">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="a63c3-275">Para revelar o abridor na ferramenta **Elementos**, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-275">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="a63c3-276">Abra a árvore **Quadros**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-276">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="a63c3-277">Escolha uma janela aberta para abrir os detalhes `Window`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-277">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="a63c3-278">Escolha o link do**Quadro Aberto**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-278">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="a63c3-279">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1107766][CR1107766].</span><span class="sxs-lookup"><span data-stu-id="a63c3-279">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Detalhes do quadro aberto" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="a63c3-281">Detalhes do quadro aberto</span><span class="sxs-lookup"><span data-stu-id="a63c3-281">Opened frame details</span></span>  
:::image-end:::  

### <a name="copy-stacktrace-for-network-initiator"></a><span data-ttu-id="a63c3-282">Copiar StackTrace para o iniciador de rede</span><span class="sxs-lookup"><span data-stu-id="a63c3-282">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="a63c3-283">Para copiar o StackTrace para a área de transferência, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63c3-283">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="a63c3-284">Abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="a63c3-284">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="a63c3-285">Escolha **Copiar**  >  **Copiar StackTrace**.</span><span class="sxs-lookup"><span data-stu-id="a63c3-285">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="a63c3-286">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1139615][CR1139615].</span><span class="sxs-lookup"><span data-stu-id="a63c3-286">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copiar StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="a63c3-288">Copiar StackTrace</span><span class="sxs-lookup"><span data-stu-id="a63c3-288">Copy stacktrace</span></span>  
:::image-end:::  

### <a name="preview-wasm-variable-value-on-mouseover"></a><span data-ttu-id="a63c3-289">Visualize o valor da variável Wasm ao passar o mouse</span><span class="sxs-lookup"><span data-stu-id="a63c3-289">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="a63c3-290">Use esse recurso para analisar o valor de uma variável Webassembly \(Wasm\) quando o código for pausado.</span><span class="sxs-lookup"><span data-stu-id="a63c3-290">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="a63c3-291">Para exibir o valor atual de uma variável, passe o mouse sobre uma variável.</span><span class="sxs-lookup"><span data-stu-id="a63c3-291">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="a63c3-292">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até Issues [1058836][CR1058836] e [1071432][CR1071432].</span><span class="sxs-lookup"><span data-stu-id="a63c3-292">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Variável de visualização do Wasm ao passar o mouse" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="a63c3-294">Variável de visualização do Wasm ao passar o mouse</span><span class="sxs-lookup"><span data-stu-id="a63c3-294">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <a name="consistent-units-of-measurement-for-sizes-of-files-and-memory"></a><span data-ttu-id="a63c3-295">Unidades de medida consistentes para tamanhos de arquivos e memória</span><span class="sxs-lookup"><span data-stu-id="a63c3-295">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="a63c3-296">O DevTools agora usa consistentemente `kB` para exibir tamanhos de arquivos e memória.</span><span class="sxs-lookup"><span data-stu-id="a63c3-296">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="a63c3-297">Anteriormente, o DevTools mesclava `kB` e `KiB`.</span><span class="sxs-lookup"><span data-stu-id="a63c3-297">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="a63c3-298">ou quilobyte \(10^3 ou 1000 bytes\)</span><span class="sxs-lookup"><span data-stu-id="a63c3-298">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="a63c3-299">ou kibibyte \(2^10 ou 1024 bytes \)</span><span class="sxs-lookup"><span data-stu-id="a63c3-299">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="a63c3-300">Por exemplo, a ferramenta **Rede** anteriormente usada `kB` em rótulos, mas agora usada `KiB` em cálculos.</span><span class="sxs-lookup"><span data-stu-id="a63c3-300">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="a63c3-301">Seus comentários mostraram que essa inconsistência causou confusão.</span><span class="sxs-lookup"><span data-stu-id="a63c3-301">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="a63c3-302">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1035309][CR1035309].</span><span class="sxs-lookup"><span data-stu-id="a63c3-302">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="a63c3-303">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a63c3-303">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="a63c3-304">Se você estiver no Windows, Linux ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="a63c3-304">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="a63c3-305">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="a63c3-305">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="a63c3-306">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a63c3-306">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Modo de exibição 3D | Microsoft Docs"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Visão geral do console | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Alterar configurações de idioma do DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar o editor de atalhos de teclado -Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Ativar camadas compostas no modo de exibição 3D – recursos experimentais | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copiar resposta formatada JSON para a área de transferência - Referência de análise da rede | Microsoft Docs"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Exibir a divisão de tempo de uma solicitação - Referência de análise de rede | Microsoft Docs"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Use o WebDriver (Chromium) para automação de teste | Microsoft Docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows | Microsoft Docs"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Personalizar atalhos de teclado em configurações – Novidades do DevTools (Microsoft Edge 87) | Microsoft Docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "comentários de webhint no painel Issues-novidades do DevTools (Microsoft Edge 85) | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Baixar o WebDriver | Desenvolvedor da Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir a personalização de atalhos de teclado/associações de chave | Erros de Chromium"  
[CR945786]: https://crbug.com/945786 "Problema 945786: DevTools: permitir a substituição de navigator.storage.estimate() | Erros do Chromium"  
[CR1029427]: https://crbug.com/1029427 "Problema 1029427: Reduzir a sobrecarga de desempenho do despacho de mensagens de protocolo no front-end | Erros do Chromium"  
[CR1035309]: https://crbug.com/1035309 "Problema 1035309: DevTools deve usar consistentemente MB para significar megabyte, não mebibyte | Erros do Chromium"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: suporte para a depuração COOP/COEP no DevTools | Erros do Chromium"  
[CR1058836]: https://crbug.com/1058836 "Problema 1058836: problemas com o UX na depuração Wasm| Erros do Chromium"  
[CR1071432]: https://crbug.com/1071432 "Problema 1071432: ☂️ experiência do desenvolvedor básico do WASM | Erros do Chromium"  
[CR1107766]: https://crbug.com/1107766 "Problema 1107766: exibir informações sobre quadros gerados por 'window.open()' na árvore de quadros | Erros do Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: informações sobre o trabalho da superfície no modo de exibição árvore de quadros | Erros do Chromium"  
[CR1126178]: https://crbug.com/1126178 "Problema 1126178: ☂ DevTools: CSS <type> components Erros do Chromium"  
[CR1130556]: https://crbug.com/1130556 "Problema 1130556: DevTools: testar fallbacks de imagem (emulação) | Erros do Chromium"  
[CR1132084]: https://crbug.com/1132084 "Problema 1132084: não há uma maneira fácil de copiar a carga de solicitação JSON | Erros do Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: ferramenta Flexbox | Erros de Chromium"  
[CR1138633]: https://crbug.com/1138633 "Problema 1138633: DevTools: o componente CSS <angle> deve refletir a aparência de sua propriedade residente no fundo do relógio | Erros do Chromium"  
[CR1139615]: https://crbug.com/1139615 "Problema 1139615: o iniciador de rede deve oferecer a capacidade de copiar o rastreamento de pilha | Erros do Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: relatar a disponibilidade da API restringida na exibição de detalhes do quadro | Erros do Chromium"  
[CR1139945]: https://crbug.com/1139945 "Problema 1139945: ícones para propriedades CSS do flexbox no painel Estilos | Erros do Chromium"  
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: melhorar o relatório de erros CORS no DevTools | Erros do Chromium"  
[CR1144090]: https://crbug.com/1144090 "Problema 1144090: adicionar adornos de estilo flexível à árvore de elementos | Erros de Chromium"  
[CR1146985]: https://crbug.com/1146985 "Problema 1146985: o texto limpo ainda é visto na caixa de texto da seção 'Armazenamento' da janela 'Ferramentas de Desenvolvimento' | Erros do Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Erros CORS | Falha"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Compartilhamento de recurso entre origens (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propriedades personalizadas CSS (variáveis) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Construtores - Janela | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Acessibilidade | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilidade | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Desempenho | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Armadilhas | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Segurança | webhint"  

> [!NOTE]
> <span data-ttu-id="a63c3-359">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a63c3-359">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a63c3-360">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/11/devtools/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="a63c3-360">The original page is found [here](https://developers.google.com/web/updates/2020/11/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a63c3-362">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a63c3-362">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
