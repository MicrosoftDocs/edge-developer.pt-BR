---
description: Um tutorial sobre os recursos mais populares relacionados à rede no Microsoft Edge DevTools.
title: Inspecionar atividades de rede no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a55ff05e29817c483cbf13b8713ef37cf96424d5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125423"
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

# <span data-ttu-id="e6679-104">Inspecionar atividades de rede no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e6679-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="e6679-105">Este é um tutorial prático de alguns dos recursos DevTools mais usados relacionados à inspeção de atividades da rede para uma página.</span><span class="sxs-lookup"><span data-stu-id="e6679-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="e6679-106">Consulte [referência de rede][DevtoolsNetworkReference] , se você quiser procurar recursos.</span><span class="sxs-lookup"><span data-stu-id="e6679-106">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="e6679-107">Quando usar o painel de rede</span><span class="sxs-lookup"><span data-stu-id="e6679-107">When to use the Network panel</span></span>  

<span data-ttu-id="e6679-108">Em geral, use o painel de rede quando precisar ter certeza de que os recursos estão sendo baixados ou carregados como esperado.</span><span class="sxs-lookup"><span data-stu-id="e6679-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="e6679-109">Os casos de uso mais comuns do painel rede são:</span><span class="sxs-lookup"><span data-stu-id="e6679-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="e6679-110">Garantir que os recursos estejam realmente sendo carregados ou baixados.</span><span class="sxs-lookup"><span data-stu-id="e6679-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="e6679-111">Inspecionar as propriedades de um recurso individual, como cabeçalhos HTTP, conteúdo, tamanho e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e6679-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="e6679-112">Se você estiver procurando maneiras de melhorar o desempenho do carregamento de página, **não** comece com o painel de rede.</span><span class="sxs-lookup"><span data-stu-id="e6679-112">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="e6679-113">Há muitos tipos de problemas de desempenho de carga que não estão relacionados à atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="e6679-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="e6679-114">Comece com o painel auditorias porque ele fornece sugestões direcionadas sobre como melhorar sua página.</span><span class="sxs-lookup"><span data-stu-id="e6679-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="e6679-115">Consulte [otimizar a velocidade do site][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="e6679-115">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="e6679-116">Abrir o painel rede</span><span class="sxs-lookup"><span data-stu-id="e6679-116">Open the Network panel</span></span>  

<span data-ttu-id="e6679-117">Para aproveitar ao máximo este tutorial, abra a demonstração e experimente os recursos na página de demonstração.</span><span class="sxs-lookup"><span data-stu-id="e6679-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="e6679-118">Abra a [demonstração][GlitchNetworkGetStarted]de introdução.</span><span class="sxs-lookup"><span data-stu-id="e6679-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="e6679-120">A demonstração</span><span class="sxs-lookup"><span data-stu-id="e6679-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="A demonstração" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="e6679-121">Para [abrir o devtools][DevToolsOpen] , pressione `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e6679-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="e6679-122">O painel **console** será aberto.</span><span class="sxs-lookup"><span data-stu-id="e6679-122">The **Console** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="e6679-124">O **console**</span><span class="sxs-lookup"><span data-stu-id="e6679-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e6679-125">Você pode preferir [encaixar devtools na parte inferior da janela][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="e6679-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="e6679-127">DevTools encaixado na parte inferior da janela</span><span class="sxs-lookup"><span data-stu-id="e6679-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-128">Selecione a guia **rede** .  O painel **rede** é aberto.</span><span class="sxs-lookup"><span data-stu-id="e6679-128">Select the **Network** tab.  The **Network** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="e6679-130">Ferramenta de **console** no devtools encaixada na parte inferior da janela</span><span class="sxs-lookup"><span data-stu-id="e6679-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e6679-131">No momento, o painel de rede está vazio.</span><span class="sxs-lookup"><span data-stu-id="e6679-131">Right now the Network panel is empty.</span></span>  <span data-ttu-id="e6679-132">O DevTools somente registra a atividade de rede depois que você a abre e não ocorreu nenhuma atividade de rede desde que você tenha aberto o DevTools.</span><span class="sxs-lookup"><span data-stu-id="e6679-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="e6679-133">Registrar atividades de rede</span><span class="sxs-lookup"><span data-stu-id="e6679-133">Log network activity</span></span>  

<span data-ttu-id="e6679-134">Para exibir a atividade de rede que uma página causa:</span><span class="sxs-lookup"><span data-stu-id="e6679-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="e6679-135">Recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="e6679-135">Reload the page.</span></span>  <span data-ttu-id="e6679-136">O painel rede registra toda a atividade de rede no **log de rede**.</span><span class="sxs-lookup"><span data-stu-id="e6679-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="e6679-138">O **log de rede**</span><span class="sxs-lookup"><span data-stu-id="e6679-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e6679-139">Cada linha do **log de rede** representa um recurso.</span><span class="sxs-lookup"><span data-stu-id="e6679-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="e6679-140">Por padrão, os recursos são listados cronologicamente.</span><span class="sxs-lookup"><span data-stu-id="e6679-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="e6679-141">O recurso superior geralmente é o principal documento HTML.</span><span class="sxs-lookup"><span data-stu-id="e6679-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="e6679-142">O recurso de baixo é o que foi solicitado por último.</span><span class="sxs-lookup"><span data-stu-id="e6679-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="e6679-143">Cada coluna representa informações sobre um recurso.</span><span class="sxs-lookup"><span data-stu-id="e6679-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="e6679-144">Na figura anterior, as colunas padrão são exibidas.</span><span class="sxs-lookup"><span data-stu-id="e6679-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="e6679-145">**Status**.</span><span class="sxs-lookup"><span data-stu-id="e6679-145">**Status**.</span></span>  <span data-ttu-id="e6679-146">O código de status HTTP para resposta.</span><span class="sxs-lookup"><span data-stu-id="e6679-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="e6679-147">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="e6679-147">**Type**.</span></span>  <span data-ttu-id="e6679-148">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e6679-148">The resource type.</span></span>  
    *   <span data-ttu-id="e6679-149">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="e6679-149">**Initiator**.</span></span>  <span data-ttu-id="e6679-150">A causa da solicitação do recurso.</span><span class="sxs-lookup"><span data-stu-id="e6679-150">The cause of the resource request.</span></span>  <span data-ttu-id="e6679-151">Selecionar um link na coluna do iniciador leva você ao código-fonte que causou a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e6679-151">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="e6679-152">**Tempo**.</span><span class="sxs-lookup"><span data-stu-id="e6679-152">**Time**.</span></span>  <span data-ttu-id="e6679-153">A duração da solicitação.</span><span class="sxs-lookup"><span data-stu-id="e6679-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="e6679-154">**Cascata**.</span><span class="sxs-lookup"><span data-stu-id="e6679-154">**Waterfall**.</span></span>  <span data-ttu-id="e6679-155">Uma representação gráfica dos diferentes estágios da solicitação.</span><span class="sxs-lookup"><span data-stu-id="e6679-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="e6679-156">Passe o mouse sobre uma cascata para ver uma divisão.</span><span class="sxs-lookup"><span data-stu-id="e6679-156">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e6679-157">O gráfico acima do log de rede é chamado de visão geral.</span><span class="sxs-lookup"><span data-stu-id="e6679-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="e6679-158">Você não usará o gráfico de visão geral neste tutorial, portanto, poderá ocultá-lo.</span><span class="sxs-lookup"><span data-stu-id="e6679-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="e6679-159">Consulte [ocultar o painel Visão geral][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="e6679-159">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="e6679-160">Depois de abrir o DevTools, ele registra a atividade de rede no log de rede.</span><span class="sxs-lookup"><span data-stu-id="e6679-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="e6679-161">Para demonstrar isso, primeiro examine a parte inferior do **log de rede** e faça uma anotação mental da última atividade.</span><span class="sxs-lookup"><span data-stu-id="e6679-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="e6679-162">Agora, selecione o botão **obter dados** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="e6679-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="e6679-163">Examine a parte inferior do **log de rede** novamente.</span><span class="sxs-lookup"><span data-stu-id="e6679-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="e6679-164">Você deve ver um novo recurso chamado `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="e6679-164">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="e6679-165">Selecionar o botão **obter dados** fez com que a página solicitasse esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="e6679-165">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="e6679-167">Um novo recurso no **log de rede**</span><span class="sxs-lookup"><span data-stu-id="e6679-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e6679-168">Mostrar mais informações</span><span class="sxs-lookup"><span data-stu-id="e6679-168">Show more information</span></span>  

<span data-ttu-id="e6679-169">As colunas do log de rede são configuráveis.</span><span class="sxs-lookup"><span data-stu-id="e6679-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="e6679-170">Você pode ocultar colunas que não está usando.</span><span class="sxs-lookup"><span data-stu-id="e6679-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="e6679-171">Também há muitas colunas que estão ocultas por padrão que podem ser úteis.</span><span class="sxs-lookup"><span data-stu-id="e6679-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="e6679-172">Clique com o botão direito do mouse no cabeçalho da tabela de log de rede e escolha **domínio**.</span><span class="sxs-lookup"><span data-stu-id="e6679-172">Right-click the header of the Network Log table and choose **Domain**.</span></span>  <span data-ttu-id="e6679-173">O domínio de cada recurso agora é mostrado.</span><span class="sxs-lookup"><span data-stu-id="e6679-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="e6679-175">Habilitar a coluna domínio</span><span class="sxs-lookup"><span data-stu-id="e6679-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="e6679-176">Veja a URL completa de um recurso passando o mouse sobre a célula na coluna **nome** .</span><span class="sxs-lookup"><span data-stu-id="e6679-176">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  
    
## <span data-ttu-id="e6679-177">Simular uma conexão de rede mais lenta</span><span class="sxs-lookup"><span data-stu-id="e6679-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="e6679-178">A conexão de rede do computador que você usa para criar sites é provavelmente mais rápida do que as conexões de rede dos dispositivos móveis dos seus usuários.</span><span class="sxs-lookup"><span data-stu-id="e6679-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="e6679-179">Ao estreitar a página, você tem uma ideia melhor do tempo que uma página leva para ser carregada em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="e6679-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="e6679-180">Selecione o menu suspenso **regulagem** , que é definido como **online** por padrão.</span><span class="sxs-lookup"><span data-stu-id="e6679-180">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="e6679-182">Habilitar limitação</span><span class="sxs-lookup"><span data-stu-id="e6679-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-183">Escolha **3G lento**.</span><span class="sxs-lookup"><span data-stu-id="e6679-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="e6679-185">Selecionar 3G lento</span><span class="sxs-lookup"><span data-stu-id="e6679-185">Select Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-186">Use o **recarregamento** de longa duração \ ( ![ recarregar ][ImageRefreshIcon] \) e escolha **esvaziar o cache e o recarregamento físico**.</span><span class="sxs-lookup"><span data-stu-id="e6679-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="e6679-188">Esvaziar o cache e o recarregamento rígido</span><span class="sxs-lookup"><span data-stu-id="e6679-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="e6679-189">Em visitas de repetição, o navegador geralmente serve alguns arquivos do [cache][MDNHTTPCache], o que acelera a carga da página.</span><span class="sxs-lookup"><span data-stu-id="e6679-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="e6679-190">O **cache vazio e o recarregamento rígido** força o navegador a acessar a rede para todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="e6679-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="e6679-191">Isso é útil quando você deseja ver como um visitante do primeiro visitante experimenta um carregamento de página.</span><span class="sxs-lookup"><span data-stu-id="e6679-191">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e6679-192">O fluxo de trabalho do **cache e do recarregamento de disco vazio** só está disponível quando o devtools está aberto.</span><span class="sxs-lookup"><span data-stu-id="e6679-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <span data-ttu-id="e6679-193">Capturar capturas de tela</span><span class="sxs-lookup"><span data-stu-id="e6679-193">Capture screenshots</span></span>  

<span data-ttu-id="e6679-194">As capturas de tela permitem ver como uma página é exibida ao longo do tempo durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="e6679-194">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="e6679-195">Selecione \ ( ![ configurações de rede ][ImageSettingsIcon] \) e marque a caixa de seleção **captura de tela de captura** .</span><span class="sxs-lookup"><span data-stu-id="e6679-195">Select \(![Network settings][ImageSettingsIcon]\) and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="e6679-196">Recarregue a página novamente por meio do fluxo de trabalho do **cache vazio e do recarregamento de disco** .</span><span class="sxs-lookup"><span data-stu-id="e6679-196">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="e6679-197">Consulte [simular uma conexão mais lenta](#simulate-a-slower-network-connection) se você precisar de um lembrete sobre como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="e6679-197">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="e6679-198">O painel capturas de tela fornece miniaturas de como a página examinou em vários pontos durante o processo de carregamento.</span><span class="sxs-lookup"><span data-stu-id="e6679-198">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="e6679-200">Capturas de tela do carregamento de página</span><span class="sxs-lookup"><span data-stu-id="e6679-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-201">Selecione a primeira miniatura.</span><span class="sxs-lookup"><span data-stu-id="e6679-201">Select the first thumbnail.</span></span>  <span data-ttu-id="e6679-202">O DevTools mostra o que a atividade de rede estava ocorrendo nesse momento.</span><span class="sxs-lookup"><span data-stu-id="e6679-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="e6679-204">A atividade de rede que está acontecendo durante a primeira captura de tela</span><span class="sxs-lookup"><span data-stu-id="e6679-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-205">Selecione \ ( ![ configurações de rede ][ImageSettingsIcon] \) novamente e desmarque a caixa de seleção **capturar capturas de tela** para fechar o painel capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="e6679-205">Select \(![Network settings][ImageSettingsIcon]\) again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="e6679-206">Recarregue a página novamente.</span><span class="sxs-lookup"><span data-stu-id="e6679-206">Reload the page again.</span></span>  
    
## <span data-ttu-id="e6679-207">Inspecionar os detalhes do recurso</span><span class="sxs-lookup"><span data-stu-id="e6679-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="e6679-208">Selecione um recurso para saber mais sobre ele.</span><span class="sxs-lookup"><span data-stu-id="e6679-208">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="e6679-209">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="e6679-209">Try it now:</span></span>  

1.  <span data-ttu-id="e6679-210">Selecione `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="e6679-210">Select `getstarted.html`.</span></span>  <span data-ttu-id="e6679-211">A guia **cabeçalhos** é mostrada.</span><span class="sxs-lookup"><span data-stu-id="e6679-211">The **Headers** tab is shown.</span></span>  <span data-ttu-id="e6679-212">Use esta guia para inspecionar cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6679-212">Use this tab to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="e6679-214">A guia **cabeçalhos**</span><span class="sxs-lookup"><span data-stu-id="e6679-214">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-215">Selecione a guia **Visualizar** .  Uma renderização básica do HTML é mostrada.</span><span class="sxs-lookup"><span data-stu-id="e6679-215">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="e6679-217">A guia **Visualização**</span><span class="sxs-lookup"><span data-stu-id="e6679-217">The **Preview** tab</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e6679-218">Esta guia é útil quando uma API retorna um código de erro em HTML.</span><span class="sxs-lookup"><span data-stu-id="e6679-218">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="e6679-219">Pode ser mais fácil ler o HTML renderizado do que o código-fonte HTML ou ao inspecionar imagens.</span><span class="sxs-lookup"><span data-stu-id="e6679-219">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="e6679-220">Selecione a guia **resposta** .  O código-fonte HTML é mostrado.</span><span class="sxs-lookup"><span data-stu-id="e6679-220">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="e6679-222">A guia **resposta**</span><span class="sxs-lookup"><span data-stu-id="e6679-222">The **Response** tab</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="e6679-223">Quando um arquivo é minified, selecionar o **formato** \ ( ![ formato ][ImageFormatIcon] \) na parte inferior da guia **resposta** reformata novamente o conteúdo do arquivo para facilitar a leitura.</span><span class="sxs-lookup"><span data-stu-id="e6679-223">When a file is minified, selecting the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="e6679-224">Selecione a guia **intervalo** .  Uma divisão da atividade de rede desse recurso é mostrada.</span><span class="sxs-lookup"><span data-stu-id="e6679-224">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="e6679-226">A guia **intervalo**</span><span class="sxs-lookup"><span data-stu-id="e6679-226">The **Timing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-227">Escolha **fechar** \ ( ![ fechar ][ImageCloseIcon] \) para exibir o log de rede novamente.</span><span class="sxs-lookup"><span data-stu-id="e6679-227">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="e6679-229">O botão **fechar**</span><span class="sxs-lookup"><span data-stu-id="e6679-229">The **Close** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e6679-230">Pesquisar cabeçalhos e respostas de rede</span><span class="sxs-lookup"><span data-stu-id="e6679-230">Search network headers and responses</span></span>  

<span data-ttu-id="e6679-231">Use o painel **Pesquisar** quando você precisar pesquisar os cabeçalhos HTTP e as respostas de todos os recursos para uma determinada cadeia de caracteres ou expressão regular.</span><span class="sxs-lookup"><span data-stu-id="e6679-231">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="e6679-232">Por exemplo, suponha que você queira verificar se seus recursos estão usando **políticas de cache**razoáveis.</span><span class="sxs-lookup"><span data-stu-id="e6679-232">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="e6679-233">Escolha **Pesquisar** \ ( ![ localizar ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e6679-233">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="e6679-234">O painel Pesquisar é aberto à esquerda do log de rede.</span><span class="sxs-lookup"><span data-stu-id="e6679-234">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="e6679-236">Painel de **pesquisa**</span><span class="sxs-lookup"><span data-stu-id="e6679-236">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-237">Digite `Cache-Control` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e6679-237">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="e6679-238">O painel Pesquisar lista todas as ocorrências `Cache-Control` que ele encontra em cabeçalhos ou conteúdo do recurso.</span><span class="sxs-lookup"><span data-stu-id="e6679-238">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="e6679-240">Resultados da pesquisa‎‏ para </span><span class="sxs-lookup"><span data-stu-id="e6679-240">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-241">Selecione um resultado para exibir o recurso no qual o resultado foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="e6679-241">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="e6679-242">Se você estiver vendo os detalhes do recurso, selecione um resultado para ir diretamente para ele.</span><span class="sxs-lookup"><span data-stu-id="e6679-242">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="e6679-243">Por exemplo, se a consulta foi encontrada em um cabeçalho, a guia cabeçalhos será aberta.</span><span class="sxs-lookup"><span data-stu-id="e6679-243">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="e6679-244">Se a consulta foi encontrada em conteúdo, a guia **resposta** é aberta.</span><span class="sxs-lookup"><span data-stu-id="e6679-244">If the query was found in content, the **Response** tab opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="e6679-246">Um resultado da pesquisa realçado na guia **cabeçalhos**</span><span class="sxs-lookup"><span data-stu-id="e6679-246">A search result highlighted in the **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-247">Feche o painel Pesquisar e a guia cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="e6679-247">Close the Search pane and the Headers tab.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="e6679-249">Os botões **fechar**</span><span class="sxs-lookup"><span data-stu-id="e6679-249">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e6679-250">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="e6679-250">Filter resources</span></span>  

<span data-ttu-id="e6679-251">O DevTools oferece vários fluxos de trabalho para a filtragem de recursos que não são relevantes para a tarefa em questão.</span><span class="sxs-lookup"><span data-stu-id="e6679-251">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="e6679-253">A barra de ferramentas **filtros**</span><span class="sxs-lookup"><span data-stu-id="e6679-253">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="e6679-254">A barra de ferramentas **filtros** deve ser habilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e6679-254">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="e6679-255">Se não:</span><span class="sxs-lookup"><span data-stu-id="e6679-255">If not:</span></span>  

1.  <span data-ttu-id="e6679-256">Escolha **filtro** \ ( ![ filtro ][ImageFilterIcon] \) para mostrá-lo.</span><span class="sxs-lookup"><span data-stu-id="e6679-256">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <span data-ttu-id="e6679-257">Filtrar por cadeia de caracteres, expressão regular ou propriedade</span><span class="sxs-lookup"><span data-stu-id="e6679-257">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="e6679-258">A caixa de texto **Filtrar** oferece suporte a muitos tipos diferentes de filtragem.</span><span class="sxs-lookup"><span data-stu-id="e6679-258">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="e6679-259">Digite `png` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="e6679-259">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="e6679-260">Somente os arquivos que contêm o texto `png` são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e6679-260">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="e6679-261">Nesse caso, os únicos arquivos que correspondem ao filtro são as imagens PNG.</span><span class="sxs-lookup"><span data-stu-id="e6679-261">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="e6679-263">Um filtro de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="e6679-263">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-264">Digite `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="e6679-264">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="e6679-265">O DevTools filtra qualquer recurso com um nome de arquivo que não termina com um `j` ou um `c` seguido de 1 ou mais `s` caracteres.</span><span class="sxs-lookup"><span data-stu-id="e6679-265">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="e6679-267">Um filtro de expressão regular</span><span class="sxs-lookup"><span data-stu-id="e6679-267">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-268">Digite `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="e6679-268">Type `-main.css`.</span></span>  <span data-ttu-id="e6679-269">DevTools filtros desconectados `main.css` .</span><span class="sxs-lookup"><span data-stu-id="e6679-269">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="e6679-270">Se qualquer outro arquivo coincidir com o padrão, ele também será filtrado.</span><span class="sxs-lookup"><span data-stu-id="e6679-270">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="e6679-272">Um filtro negativo</span><span class="sxs-lookup"><span data-stu-id="e6679-272">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-273">Digite `domain:cdn.glitch.com` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="e6679-273">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="e6679-274">O DevTools filtra qualquer recurso com uma URL que não corresponde a este domínio.</span><span class="sxs-lookup"><span data-stu-id="e6679-274">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="e6679-276">Um filtro de propriedade</span><span class="sxs-lookup"><span data-stu-id="e6679-276">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e6679-277">Consulte [Filtrar solicitações por Propriedades][DevtoolsReferenceProperty] para obter a lista completa de propriedades filtráveis.</span><span class="sxs-lookup"><span data-stu-id="e6679-277">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
1.  <span data-ttu-id="e6679-278">Desmarque a caixa de texto **Filtrar** de qualquer texto.</span><span class="sxs-lookup"><span data-stu-id="e6679-278">Clear the **Filter** text box of any text.</span></span>  
    
### <span data-ttu-id="e6679-279">Filtrar por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="e6679-279">Filter by resource type</span></span>  

<span data-ttu-id="e6679-280">Para se concentrar em um determinado tipo de arquivo, como folhas de estilos:</span><span class="sxs-lookup"><span data-stu-id="e6679-280">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="e6679-281">Escolha **CSS**.</span><span class="sxs-lookup"><span data-stu-id="e6679-281">Choose **CSS**.</span></span>  <span data-ttu-id="e6679-282">Todos os outros tipos de arquivo são filtrados.</span><span class="sxs-lookup"><span data-stu-id="e6679-282">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="e6679-284">Mostrar somente arquivos CSS</span><span class="sxs-lookup"><span data-stu-id="e6679-284">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-285">Para ver também os scripts, segure `Control` \ (Windows, Linux \) ou `Command` \ (MacOS \) e escolha **js**.</span><span class="sxs-lookup"><span data-stu-id="e6679-285">To also see scripts, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="e6679-287">Mostrar somente arquivos CSS e JS</span><span class="sxs-lookup"><span data-stu-id="e6679-287">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-288">Escolha **tudo** para remover os filtros e ver todos os recursos novamente.</span><span class="sxs-lookup"><span data-stu-id="e6679-288">Choose **All** to remove the filters and see all resources again.</span></span>  
    
<span data-ttu-id="e6679-289">Consulte [Filtrar solicitações][DevtoolsNetworkReferenceFilter] para outros fluxos de trabalho de filtragem.</span><span class="sxs-lookup"><span data-stu-id="e6679-289">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="e6679-290">Bloquear solicitações</span><span class="sxs-lookup"><span data-stu-id="e6679-290">Block requests</span></span>  

<span data-ttu-id="e6679-291">Qual a aparência de uma página e comportamento quando alguns dos recursos da página não estão disponíveis?</span><span class="sxs-lookup"><span data-stu-id="e6679-291">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="e6679-292">Ele falha completamente, ou ainda é um pouco funcional?</span><span class="sxs-lookup"><span data-stu-id="e6679-292">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="e6679-293">Bloquear solicitações para descobrir:</span><span class="sxs-lookup"><span data-stu-id="e6679-293">Block requests to find out:</span></span>  

1.  <span data-ttu-id="e6679-294">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.</span><span class="sxs-lookup"><span data-stu-id="e6679-294">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="e6679-296">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="e6679-296">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-297">Tipo `block` , escolha **Mostrar bloqueio de solicitação**e selecionar `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e6679-297">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="e6679-299">Mostrar bloqueio de solicitações</span><span class="sxs-lookup"><span data-stu-id="e6679-299">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-300">Escolha **Adicionar padrão** \ ( ![ Adicionar padrão ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e6679-300">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="e6679-301">Digite `main.css`.</span><span class="sxs-lookup"><span data-stu-id="e6679-301">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="e6679-303">Pedi</span><span class="sxs-lookup"><span data-stu-id="e6679-303">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-304">Escolha **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="e6679-304">Choose **Add**.</span></span>  
1.  <span data-ttu-id="e6679-305">Recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="e6679-305">Reload the page.</span></span>  <span data-ttu-id="e6679-306">Como esperado, o estilo da página é levemente bagunçado porque a folha de estilos principal foi bloqueada.</span><span class="sxs-lookup"><span data-stu-id="e6679-306">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e6679-307">A `main.css` linha no log de rede.</span><span class="sxs-lookup"><span data-stu-id="e6679-307">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="e6679-308">O texto vermelho significa que o recurso foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e6679-308">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="e6679-310">foi bloqueado</span><span class="sxs-lookup"><span data-stu-id="e6679-310">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e6679-311">Desmarque a caixa de seleção **habilitar o bloqueio de solicitações** .</span><span class="sxs-lookup"><span data-stu-id="e6679-311">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="e6679-312">Conclusão</span><span class="sxs-lookup"><span data-stu-id="e6679-312">Conclusion</span></span>  

<span data-ttu-id="e6679-313">Parabéns, você concluiu o tutorial.</span><span class="sxs-lookup"><span data-stu-id="e6679-313">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="e6679-314">Agora você sabe como usar o painel **rede** no Microsoft Edge devtools!</span><span class="sxs-lookup"><span data-stu-id="e6679-314">You now know how to use the **Network** panel in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="e6679-315">Navegue até a [referência de rede][DevtoolsNetworkReference] para descobrir recursos mais devtools relacionados à atividade de inspeção de rede.</span><span class="sxs-lookup"><span data-stu-id="e6679-315">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <span data-ttu-id="e6679-316">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e6679-316">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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

[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Referência de análise de rede | Documentos da Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Filtrar solicitações-referência de análise de rede | Documentos da Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ocultar o painel Visão geral-referência de análise de rede | Documentos da Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrar solicitações por Propriedades-referência de análise de rede | Documentos da Microsoft"
[DevToolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Otimizar a velocidade do site com o Microsoft Edge DevTools | Documentos da Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspecionar a demonstração da atividade de rede | Problema"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Cache HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="e6679-326">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="e6679-326">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e6679-327">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e6679-327">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e6679-329">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e6679-329">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
