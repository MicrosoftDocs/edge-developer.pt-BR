---
description: Um tutorial sobre os recursos relacionados à rede mais populares no Microsoft Edge DevTools.
title: Inspecionar a atividade de rede no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 16b60716c91d2f4ce778f1fac37afc0e73e30ab6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398655"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.  
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a><span data-ttu-id="03973-104">Inspecionar a atividade de rede no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="03973-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="03973-105">Este é um tutorial prática de alguns dos recursos de DevTools mais usados relacionados à inspeção da atividade de rede para uma página.</span><span class="sxs-lookup"><span data-stu-id="03973-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="03973-106">Se você quiser navegar por recursos, navegue até [Referência de Rede][DevtoolsNetworkReference].</span><span class="sxs-lookup"><span data-stu-id="03973-106">If you want to browse features, navigate to [Network Reference][DevtoolsNetworkReference].</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a><span data-ttu-id="03973-107">Quando usar o painel Rede</span><span class="sxs-lookup"><span data-stu-id="03973-107">When to use the Network panel</span></span>  

<span data-ttu-id="03973-108">Em geral, use o painel Rede quando precisar se certificar de que os recursos estão sendo baixados ou carregados conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="03973-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="03973-109">Os casos de uso mais comuns para o painel Rede são:</span><span class="sxs-lookup"><span data-stu-id="03973-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="03973-110">Certifique-se de que os recursos realmente estão sendo carregados ou baixados.</span><span class="sxs-lookup"><span data-stu-id="03973-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="03973-111">Inspecionando as propriedades de um recurso individual, como os cabeçalhos HTTP, conteúdo, tamanho e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="03973-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="03973-112">Se você estiver procurando maneiras de melhorar o desempenho da carga da página, **não comece** com a **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="03973-112">If you are looking for ways to improve page load performance, **do not** start with the **Network** tool.</span></span>  <span data-ttu-id="03973-113">Há muitos tipos de problemas de desempenho de carga que não estão relacionados à atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="03973-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="03973-114">Comece com o painel Auditorias porque ele fornece sugestões direcionadas sobre como melhorar sua página.</span><span class="sxs-lookup"><span data-stu-id="03973-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="03973-115">Navegue até [Otimizar Velocidade do Site.][DevtoolsSpeedGetStarted]</span><span class="sxs-lookup"><span data-stu-id="03973-115">Navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <a name="open-the-network-panel"></a><span data-ttu-id="03973-116">Abrir o painel Rede</span><span class="sxs-lookup"><span data-stu-id="03973-116">Open the Network panel</span></span>  

<span data-ttu-id="03973-117">Para obter o máximo deste tutorial, abra a demonstração e experimente os recursos na página de demonstração.</span><span class="sxs-lookup"><span data-stu-id="03973-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="03973-118">Abra a [demonstração Get Started][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="03973-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="03973-120">A demonstração</span><span class="sxs-lookup"><span data-stu-id="03973-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="03973-121">Para [Abrir DevTools,][DevToolsOpen]selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="03973-121">To [Open DevTools][DevToolsOpen], select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="03973-122">A **ferramenta Console** é aberta.</span><span class="sxs-lookup"><span data-stu-id="03973-122">The **Console** tool opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="O Console" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="03973-124">O **Console**</span><span class="sxs-lookup"><span data-stu-id="03973-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="03973-125">Você pode preferir [acoplar o DevTools na parte inferior da janela.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="03973-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools encaixado na parte inferior da janela" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="03973-127">DevTools encaixado na parte inferior da janela</span><span class="sxs-lookup"><span data-stu-id="03973-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-128">Abra a **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="03973-128">Open the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Ferramenta de console no DevTools encaixado na parte inferior da janela" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="03973-130">**Ferramenta de** console no DevTools encaixado na parte inferior da janela</span><span class="sxs-lookup"><span data-stu-id="03973-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="03973-131">No momento, **a ferramenta Rede** está vazia.</span><span class="sxs-lookup"><span data-stu-id="03973-131">Right now the **Network** tool is empty.</span></span>  <span data-ttu-id="03973-132">O DevTools registra somente a atividade de rede depois de abri-la e nenhuma atividade de rede ocorreu desde que você abriu o DevTools.</span><span class="sxs-lookup"><span data-stu-id="03973-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <a name="log-network-activity"></a><span data-ttu-id="03973-133">Atividade de rede de log</span><span class="sxs-lookup"><span data-stu-id="03973-133">Log network activity</span></span>  

<span data-ttu-id="03973-134">Para exibir a atividade de rede que uma página causa:</span><span class="sxs-lookup"><span data-stu-id="03973-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="03973-135">Atualize a página da Web.</span><span class="sxs-lookup"><span data-stu-id="03973-135">Refresh the webpage.</span></span>  <span data-ttu-id="03973-136">O painel Rede registra todas as atividades de rede no **Log de Rede.**</span><span class="sxs-lookup"><span data-stu-id="03973-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="O Log de Rede" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="03973-138">O **Log de Rede**</span><span class="sxs-lookup"><span data-stu-id="03973-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="03973-139">Cada linha do **Log de Rede** representa um recurso.</span><span class="sxs-lookup"><span data-stu-id="03973-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="03973-140">Por padrão, os recursos são listados cronologicamente.</span><span class="sxs-lookup"><span data-stu-id="03973-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="03973-141">O recurso superior geralmente é o documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="03973-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="03973-142">O recurso inferior é o que foi solicitado por último.</span><span class="sxs-lookup"><span data-stu-id="03973-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="03973-143">Cada coluna representa informações sobre um recurso.</span><span class="sxs-lookup"><span data-stu-id="03973-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="03973-144">Na figura anterior, as colunas padrão são exibidas.</span><span class="sxs-lookup"><span data-stu-id="03973-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="03973-145">**Status**.</span><span class="sxs-lookup"><span data-stu-id="03973-145">**Status**.</span></span>  <span data-ttu-id="03973-146">O código de status HTTP para resposta.</span><span class="sxs-lookup"><span data-stu-id="03973-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="03973-147">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="03973-147">**Type**.</span></span>  <span data-ttu-id="03973-148">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="03973-148">The resource type.</span></span>  
    *   <span data-ttu-id="03973-149">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="03973-149">**Initiator**.</span></span>  <span data-ttu-id="03973-150">A causa da solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="03973-150">The cause of the resource request.</span></span>  <span data-ttu-id="03973-151">CHoosing a link in the Initiator column takes you to the source code that caused the request.</span><span class="sxs-lookup"><span data-stu-id="03973-151">CHoosing a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="03973-152">**Hora**.</span><span class="sxs-lookup"><span data-stu-id="03973-152">**Time**.</span></span>  <span data-ttu-id="03973-153">A duração da solicitação.</span><span class="sxs-lookup"><span data-stu-id="03973-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="03973-154">**Cascata**.</span><span class="sxs-lookup"><span data-stu-id="03973-154">**Waterfall**.</span></span>  <span data-ttu-id="03973-155">Uma representação gráfica dos diferentes estágios da solicitação.</span><span class="sxs-lookup"><span data-stu-id="03973-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="03973-156">Para exibir uma divisão, passe o mouse em uma Cascata.</span><span class="sxs-lookup"><span data-stu-id="03973-156">To display a breakdown, hover on a Waterfall.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="03973-157">O gráfico acima do Log de Rede é chamado de Visão Geral.</span><span class="sxs-lookup"><span data-stu-id="03973-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="03973-158">Você não usará o gráfico Visão geral neste tutorial, portanto, pode escondê-lo.</span><span class="sxs-lookup"><span data-stu-id="03973-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="03973-159">Navegue [até Ocultar o painel Visão Geral.][DevtoolsReferenceHideOverview]</span><span class="sxs-lookup"><span data-stu-id="03973-159">Navigate to [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="03973-160">Depois de abrir o DevTools, ele registra a atividade de rede no Log de Rede.</span><span class="sxs-lookup"><span data-stu-id="03973-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="03973-161">Para demonstrar isso, primeiro veja a parte inferior do Log de **Rede** e faça uma anotação mental da última atividade.</span><span class="sxs-lookup"><span data-stu-id="03973-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="03973-162">Agora, selecione o **botão Obter Dados** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="03973-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="03973-163">Veja a parte inferior do **Log de Rede novamente.**</span><span class="sxs-lookup"><span data-stu-id="03973-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="03973-164">Um novo recurso chamado `getstarted.json` é exibido.</span><span class="sxs-lookup"><span data-stu-id="03973-164">A new resource named `getstarted.json` is displayed.</span></span>  <span data-ttu-id="03973-165">Para fazer com que a página da Web solicite o arquivo, escolha o **botão Obter Dados.**</span><span class="sxs-lookup"><span data-stu-id="03973-165">To cause the webpage to request the file, choose the **Get Data** button.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Um novo recurso no Log de Rede" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="03973-167">Um novo recurso no Log **de Rede**</span><span class="sxs-lookup"><span data-stu-id="03973-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <a name="show-more-information"></a><span data-ttu-id="03973-168">Mostrar mais informações</span><span class="sxs-lookup"><span data-stu-id="03973-168">Show more information</span></span>  

<span data-ttu-id="03973-169">As colunas do Log de Rede são configuráveis.</span><span class="sxs-lookup"><span data-stu-id="03973-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="03973-170">Você pode ocultar colunas que não está usando.</span><span class="sxs-lookup"><span data-stu-id="03973-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="03973-171">Há também muitas colunas ocultas por padrão que você pode achar útil.</span><span class="sxs-lookup"><span data-stu-id="03973-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="03973-172">Passe o mouse no header da tabela Log de Rede, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Domínio**.</span><span class="sxs-lookup"><span data-stu-id="03973-172">Hover on the header of the Network Log table, open the contextual menu \(right-click\), and choose **Domain**.</span></span>  <span data-ttu-id="03973-173">O domínio de cada recurso agora é mostrado.</span><span class="sxs-lookup"><span data-stu-id="03973-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Habilitar a coluna Domínio" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="03973-175">Habilitar a coluna Domínio</span><span class="sxs-lookup"><span data-stu-id="03973-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="03973-176">Para revisar a URL completa de um recurso, passe o mouse na célula na **coluna** Nome.</span><span class="sxs-lookup"><span data-stu-id="03973-176">To review the full URL of a resource, hover on the cell in the **Name** column.</span></span>  
    
## <a name="simulate-a-slower-network-connection"></a><span data-ttu-id="03973-177">Simular uma conexão de rede mais lenta</span><span class="sxs-lookup"><span data-stu-id="03973-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="03973-178">A conexão de rede do computador que você usa para criar sites provavelmente é mais rápida do que as conexões de rede dos dispositivos móveis de seus usuários.</span><span class="sxs-lookup"><span data-stu-id="03973-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="03973-179">Ao throttling da página, você tem uma ideia melhor de quanto tempo uma página leva para carregar em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="03973-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="03973-180">Escolha o **menu suspenso Throttling,** que é definido como **Online** por padrão.</span><span class="sxs-lookup"><span data-stu-id="03973-180">Choose the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Habilitar a throttling" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="03973-182">Habilitar a throttling</span><span class="sxs-lookup"><span data-stu-id="03973-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-183">Escolha **Slow 3G**.</span><span class="sxs-lookup"><span data-stu-id="03973-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Escolha Slow 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="03973-185">Escolha Slow 3G</span><span class="sxs-lookup"><span data-stu-id="03973-185">Choose Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-186">Pressione Longa **carga** \( Recarregar \) e escolha ![ Cache Vazio e ][ImageRefreshIcon] **Recarregá-lo.**</span><span class="sxs-lookup"><span data-stu-id="03973-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Cache vazio e recarregá-la" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="03973-188">Cache vazio e recarregá-la</span><span class="sxs-lookup"><span data-stu-id="03973-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="03973-189">Em visitas repetidas, o navegador geralmente atende alguns arquivos do [cache][MDNHTTPCache], o que acelera o carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="03973-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="03973-190">**O Cache Vazio e a Recarga Dura** forçam o navegador a ir para a rede para todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="03973-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="03973-191">Use-o para exibir como um visitante de primeira vez experimenta uma carga de página.</span><span class="sxs-lookup"><span data-stu-id="03973-191">Use it to display how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="03973-192">O **fluxo de trabalho DevTools** e Cache Vazio e Carga Dura só estará disponível quando o DevTools estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="03973-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <a name="capture-screenshots"></a><span data-ttu-id="03973-193">Capturar capturas de tela</span><span class="sxs-lookup"><span data-stu-id="03973-193">Capture screenshots</span></span>  

<span data-ttu-id="03973-194">Capturas de tela exibem a aparência de uma página da Web ao longo do tempo enquanto ela é carregada.</span><span class="sxs-lookup"><span data-stu-id="03973-194">Screenshots display how a webpage looks over time while it loads.</span></span>  

1.  <span data-ttu-id="03973-195">Escolha \( Configurações de rede \) e a caixa de seleção ![ ][ImageSettingsIcon] Captura captura **capturas** de tela.</span><span class="sxs-lookup"><span data-stu-id="03973-195">Choose \(![Network settings][ImageSettingsIcon]\) and turn on the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="03973-196">Atualize a página novamente usando **o fluxo de trabalho de Cache Vazio e De Carregamento** Rígido.</span><span class="sxs-lookup"><span data-stu-id="03973-196">Refresh the page again using the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="03973-197">Navegue [até Simular uma conexão mais](#simulate-a-slower-network-connection) lenta se precisar de um lembrete sobre como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="03973-197">Navigate to [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="03973-198">O painel Capturas de Tela fornece miniaturas de como a página foi olhada em vários pontos durante o processo de carregamento.</span><span class="sxs-lookup"><span data-stu-id="03973-198">The Screenshots panel provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Capturas de tela da carga da página" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="03973-200">Capturas de tela da carga da página</span><span class="sxs-lookup"><span data-stu-id="03973-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-201">Escolha a primeira miniatura.</span><span class="sxs-lookup"><span data-stu-id="03973-201">Choose the first thumbnail.</span></span>  <span data-ttu-id="03973-202">O DevTools mostra qual atividade de rede estava ocorrendo nesse momento no tempo.</span><span class="sxs-lookup"><span data-stu-id="03973-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="A atividade de rede que estava acontecendo durante a primeira captura de tela" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="03973-204">A atividade de rede que estava acontecendo durante a primeira captura de tela</span><span class="sxs-lookup"><span data-stu-id="03973-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-205">Escolha \( Configurações de rede \) novamente e desativar a caixa de seleção Captura capturas de tela para fechar o ![ ][ImageSettingsIcon] painel Capturas de Tela. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03973-205">Choose \(![Network settings][ImageSettingsIcon]\) again and turn off the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="03973-206">Atualize a página novamente.</span><span class="sxs-lookup"><span data-stu-id="03973-206">Refresh the page again.</span></span>  
    
## <a name="inspect-the-details-of-the-resource"></a><span data-ttu-id="03973-207">Inspecionar os detalhes do recurso</span><span class="sxs-lookup"><span data-stu-id="03973-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="03973-208">Escolha um recurso para saber mais sobre ele.</span><span class="sxs-lookup"><span data-stu-id="03973-208">Choose a resource to learn more information about it.</span></span>  <span data-ttu-id="03973-209">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="03973-209">Try it now:</span></span>  

1.  <span data-ttu-id="03973-210">Escolha `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="03973-210">Choose `getstarted.html`.</span></span>  <span data-ttu-id="03973-211">O **painel Headers** é mostrado.</span><span class="sxs-lookup"><span data-stu-id="03973-211">The **Headers** panel is shown.</span></span>  <span data-ttu-id="03973-212">Use este painel para inspecionar cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="03973-212">Use this panel to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="O painel Headers" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="03973-214">O **painel Headers**</span><span class="sxs-lookup"><span data-stu-id="03973-214">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-215">Escolha o **painel Visualização.**</span><span class="sxs-lookup"><span data-stu-id="03973-215">Choose the **Preview** panel.</span></span>  <span data-ttu-id="03973-216">Uma renderização básica do HTML é mostrada.</span><span class="sxs-lookup"><span data-stu-id="03973-216">A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="O painel Visualização" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="03973-218">O **painel Visualização**</span><span class="sxs-lookup"><span data-stu-id="03973-218">The **Preview** panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="03973-219">O painel é útil quando uma API retorna um código de erro em HTML.</span><span class="sxs-lookup"><span data-stu-id="03973-219">The panel is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="03973-220">Você pode achar mais fácil ler o HTML renderizado do que o código-fonte HTML ou ao inspecionar imagens.</span><span class="sxs-lookup"><span data-stu-id="03973-220">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="03973-221">Escolha o **painel Resposta.**</span><span class="sxs-lookup"><span data-stu-id="03973-221">Choose the **Response** panel.</span></span>  <span data-ttu-id="03973-222">O código-fonte HTML é mostrado.</span><span class="sxs-lookup"><span data-stu-id="03973-222">The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="O painel Resposta" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="03973-224">O **painel Resposta**</span><span class="sxs-lookup"><span data-stu-id="03973-224">The **Response** panel</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="03973-225">Quando um arquivo for minificado, escolha o botão **Formatar** \( Formatar \) na parte inferior do painel resposta para formatar o conteúdo do arquivo para capacidade ![ ][ImageFormatIcon] de leitura. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03973-225">When a file is minified, choose the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** panel to re-format the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="03973-226">Escolha o **painel Timing.**</span><span class="sxs-lookup"><span data-stu-id="03973-226">Choose the **Timing** panel.</span></span>  <span data-ttu-id="03973-227">Uma divisão da atividade de rede do recurso é exibida.</span><span class="sxs-lookup"><span data-stu-id="03973-227">A breakdown of the network activity for the resource is displayed.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="O painel Timing" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="03973-229">O **painel Timing**</span><span class="sxs-lookup"><span data-stu-id="03973-229">The **Timing** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-230">Escolha **Fechar** \( ![ Fechar ][ImageCloseIcon] \) para exibir o Log de Rede novamente.</span><span class="sxs-lookup"><span data-stu-id="03973-230">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="O botão Fechar" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="03973-232">O **botão Fechar**</span><span class="sxs-lookup"><span data-stu-id="03973-232">The **Close** button</span></span>  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a><span data-ttu-id="03973-233">Respostas e headers de rede de pesquisa</span><span class="sxs-lookup"><span data-stu-id="03973-233">Search network headers and responses</span></span>  

<span data-ttu-id="03973-234">Use o **painel** Pesquisar quando precisar pesquisar os cabeçalhos HTTP e respostas de todos os recursos para uma determinada cadeia de caracteres ou expressão regular.</span><span class="sxs-lookup"><span data-stu-id="03973-234">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="03973-235">Por exemplo, suponha que você queira verificar se seus recursos estão usando políticas de **cache razoáveis.**</span><span class="sxs-lookup"><span data-stu-id="03973-235">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="03973-236">Escolha **Pesquisar** \( ![ Pesquisar ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="03973-236">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="03973-237">O painel Pesquisar é aberto à esquerda do log de rede.</span><span class="sxs-lookup"><span data-stu-id="03973-237">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="O painel Pesquisar" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="03973-239">O **painel** Pesquisar</span><span class="sxs-lookup"><span data-stu-id="03973-239">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-240">Digite `Cache-Control` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="03973-240">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="03973-241">O painel Pesquisar lista todas as instâncias que encontra `Cache-Control` em headers de recursos ou conteúdo.</span><span class="sxs-lookup"><span data-stu-id="03973-241">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Resultados da pesquisa para Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="03973-243">Resultados da pesquisa‎‏ para </span><span class="sxs-lookup"><span data-stu-id="03973-243">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-244">Escolha um resultado para exibir o recurso no qual o resultado foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="03973-244">Choose a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="03973-245">Se você estiver olhando para os detalhes do recurso, selecione um resultado para ir diretamente para ele.</span><span class="sxs-lookup"><span data-stu-id="03973-245">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="03973-246">Por exemplo, se a consulta foi encontrada em um header, o **painel Headers** será aberto.</span><span class="sxs-lookup"><span data-stu-id="03973-246">For example, if the query was found in a header, the **Headers** panel opens.</span></span>   <span data-ttu-id="03973-247">Se a consulta foi encontrada no conteúdo, o **painel Resposta** será aberto.</span><span class="sxs-lookup"><span data-stu-id="03973-247">If the query was found in content, the **Response** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Um resultado de pesquisa realçado no painel Headers" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="03973-249">Um resultado de pesquisa realçado no painel **Headers**</span><span class="sxs-lookup"><span data-stu-id="03973-249">A search result highlighted in the **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-250">Feche o painel Pesquisa e o **painel Headers.**</span><span class="sxs-lookup"><span data-stu-id="03973-250">Close the Search pane and the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Os botões Fechar" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="03973-252">Os **botões Fechar**</span><span class="sxs-lookup"><span data-stu-id="03973-252">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <a name="filter-resources"></a><span data-ttu-id="03973-253">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="03973-253">Filter resources</span></span>  

<span data-ttu-id="03973-254">O DevTools fornece vários fluxos de trabalho para filtrar recursos que não são relevantes para a tarefa em questão.</span><span class="sxs-lookup"><span data-stu-id="03973-254">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="A barra de ferramentas Filters" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="03973-256">A **barra de ferramentas Filters**</span><span class="sxs-lookup"><span data-stu-id="03973-256">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="03973-257">A **barra de** ferramentas Filters deve ser ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="03973-257">The **Filters** toolbar should be turned on by default.</span></span>  <span data-ttu-id="03973-258">Caso não seja:</span><span class="sxs-lookup"><span data-stu-id="03973-258">If not:</span></span>  

1.  <span data-ttu-id="03973-259">Escolha **Filtrar** \( ![ ][ImageFilterIcon] Filtrar \) para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="03973-259">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <a name="filter-by-string-regular-expression-or-property"></a><span data-ttu-id="03973-260">Filtrar por cadeia de caracteres, expressão regular ou propriedade</span><span class="sxs-lookup"><span data-stu-id="03973-260">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="03973-261">A **caixa de** texto Filtro oferece suporte a vários tipos diferentes de filtragem.</span><span class="sxs-lookup"><span data-stu-id="03973-261">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="03973-262">Digite `png` na caixa de **texto** Filtrar.</span><span class="sxs-lookup"><span data-stu-id="03973-262">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="03973-263">Somente os arquivos que contêm o texto `png` são mostrados.</span><span class="sxs-lookup"><span data-stu-id="03973-263">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="03973-264">Nesse caso, os únicos arquivos que corresponderem ao filtro são as imagens PNG.</span><span class="sxs-lookup"><span data-stu-id="03973-264">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Um filtro de cadeia de caracteres" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="03973-266">Um filtro de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="03973-266">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-267">Digite `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="03973-267">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="03973-268">O DevTools filtra qualquer recurso com um nome de arquivo que não termine com um ou um seguido `j` `c` de 1 ou mais `s` caracteres.</span><span class="sxs-lookup"><span data-stu-id="03973-268">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Um filtro de expressão regular" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="03973-270">Um filtro de expressão regular</span><span class="sxs-lookup"><span data-stu-id="03973-270">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-271">Digite `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="03973-271">Type `-main.css`.</span></span>  <span data-ttu-id="03973-272">O DevTools filtra `main.css` .</span><span class="sxs-lookup"><span data-stu-id="03973-272">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="03973-273">Se qualquer arquivo corresponde ao padrão, o tit também é filtrado.</span><span class="sxs-lookup"><span data-stu-id="03973-273">If any file matches the pattern, tit is also filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Um filtro negativo" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="03973-275">Um filtro negativo</span><span class="sxs-lookup"><span data-stu-id="03973-275">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-276">Digite `domain:cdn.glitch.com` na caixa de **texto** Filtrar.</span><span class="sxs-lookup"><span data-stu-id="03973-276">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="03973-277">O DevTools filtra qualquer recurso com uma URL que não corresponder a esse domínio.</span><span class="sxs-lookup"><span data-stu-id="03973-277">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Um filtro de propriedade" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="03973-279">Um filtro de propriedade</span><span class="sxs-lookup"><span data-stu-id="03973-279">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="03973-280">Para a lista completa de propriedades filtáveis, navegue até [Filter requests by properties][DevtoolsReferenceProperty].</span><span class="sxs-lookup"><span data-stu-id="03973-280">For the full list of filterable properties, navigate to [Filter requests by properties][DevtoolsReferenceProperty].</span></span>  
    
1.  <span data-ttu-id="03973-281">**Desempacar a** caixa de texto Filtrar de qualquer texto.</span><span class="sxs-lookup"><span data-stu-id="03973-281">Clear the **Filter** text box of any text.</span></span>  
    
### <a name="filter-by-resource-type"></a><span data-ttu-id="03973-282">Filtrar por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="03973-282">Filter by resource type</span></span>  

<span data-ttu-id="03973-283">Para se concentrar em um determinado tipo de arquivo, como folhas de estilo:</span><span class="sxs-lookup"><span data-stu-id="03973-283">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="03973-284">Escolha **CSS**.</span><span class="sxs-lookup"><span data-stu-id="03973-284">Choose **CSS**.</span></span>  <span data-ttu-id="03973-285">Todos os outros tipos de arquivo são filtrados.</span><span class="sxs-lookup"><span data-stu-id="03973-285">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Mostrar somente arquivos CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="03973-287">Mostrar somente arquivos CSS</span><span class="sxs-lookup"><span data-stu-id="03973-287">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-288">Para também exibir scripts, selecione e segure `Control` \(Windows, Linux\) `Command` ou \(macOS\) e escolha **JS**.</span><span class="sxs-lookup"><span data-stu-id="03973-288">To also display scripts, select and hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Mostrar somente arquivos CSS e JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="03973-290">Mostrar somente arquivos CSS e JS</span><span class="sxs-lookup"><span data-stu-id="03973-290">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-291">Para remover os filtros e exibir todos os recursos novamente, escolha **Todos**.</span><span class="sxs-lookup"><span data-stu-id="03973-291">To remove the filters and display all resources again, choose **All**.</span></span>  
    
<span data-ttu-id="03973-292">Para outros fluxos de trabalho de filtragem, navegue até [Solicitações de filtro][DevtoolsNetworkReferenceFilter].</span><span class="sxs-lookup"><span data-stu-id="03973-292">For other filtering workflows, navigate to [Filter requests][DevtoolsNetworkReferenceFilter].</span></span>  

## <a name="block-requests"></a><span data-ttu-id="03973-293">Bloquear solicitações</span><span class="sxs-lookup"><span data-stu-id="03973-293">Block requests</span></span>  

<span data-ttu-id="03973-294">Como uma página fica e se comporta quando alguns dos recursos da página não estão disponíveis?</span><span class="sxs-lookup"><span data-stu-id="03973-294">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="03973-295">Falha completamente ou ainda é um pouco funcional?</span><span class="sxs-lookup"><span data-stu-id="03973-295">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="03973-296">Bloquear solicitações para descobrir:</span><span class="sxs-lookup"><span data-stu-id="03973-296">Block requests to find out:</span></span>  

1.  <span data-ttu-id="03973-297">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="03973-297">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="O Menu De comando" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="03973-299">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="03973-299">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-300">Digite `block` , escolha Mostrar Bloqueio de **Solicitação**e `Enter` selecione .</span><span class="sxs-lookup"><span data-stu-id="03973-300">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Mostrar Bloqueio de Solicitação" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="03973-302">Mostrar Bloqueio de Solicitação</span><span class="sxs-lookup"><span data-stu-id="03973-302">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-303">Escolha **Adicionar Padrão** \( Adicionar Padrão ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="03973-303">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="03973-304">Digite `main.css`.</span><span class="sxs-lookup"><span data-stu-id="03973-304">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Bloqueando main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="03973-306">Bloqueio</span><span class="sxs-lookup"><span data-stu-id="03973-306">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-307">Escolha **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="03973-307">Choose **Add**.</span></span>  
1.  <span data-ttu-id="03973-308">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="03973-308">Refresh the page.</span></span>  <span data-ttu-id="03973-309">Como esperado, o estilo da página está um pouco confuso porque a folha de estilos principal foi bloqueada.</span><span class="sxs-lookup"><span data-stu-id="03973-309">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="03973-310">A `main.css` linha no Log de Rede.</span><span class="sxs-lookup"><span data-stu-id="03973-310">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="03973-311">O texto vermelho significa que o recurso foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="03973-311">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css foi bloqueado" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="03973-313">foi bloqueado</span><span class="sxs-lookup"><span data-stu-id="03973-313">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="03973-314">Desmarque a caixa de seleção **Habilitar bloqueio de** solicitação.</span><span class="sxs-lookup"><span data-stu-id="03973-314">Deselect the **Enable request blocking** checkbox.</span></span>  

## <a name="conclusion"></a><span data-ttu-id="03973-315">Conclusão</span><span class="sxs-lookup"><span data-stu-id="03973-315">Conclusion</span></span>  

<span data-ttu-id="03973-316">Parabéns, você concluiu o tutorial.</span><span class="sxs-lookup"><span data-stu-id="03973-316">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="03973-317">Agora você sabe como usar a **ferramenta Rede** no Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="03973-317">You now know how to use the **Network** tool in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="03973-318">Navegue até [a Referência de Rede][DevtoolsNetworkReference] para descobrir mais recursos do DevTools relacionados à inspeção da atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="03973-318">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="03973-319">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="03973-319">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReference]: ./reference.md "Referência de análise de rede | Microsoft Docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Solicitações de filtro - Referência de análise de rede | Microsoft Docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ocultar o painel Visão geral - Referência de análise de rede | Microsoft Docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrar solicitações por propriedades - Referência de análise de rede | Microsoft Docs"
[DevToolsOpen]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Otimizar a velocidade do site com o Microsoft Edge DevTools | Microsoft Docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspecionar a demonstração de atividade de rede | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Armazenamento em cache HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="03973-329">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="03973-329">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="03973-330">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/network/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="03973-330">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="03973-332">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="03973-332">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
