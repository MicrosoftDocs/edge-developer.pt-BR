---
title: Inspecionar atividades de rede no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611809"
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





# <span data-ttu-id="cbb88-103">Inspecionar atividades de rede no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cbb88-103">Inspect Network Activity In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="cbb88-104">Este é um tutorial prático de alguns dos recursos DevTools mais usados relacionados à inspeção de atividades da rede para uma página.</span><span class="sxs-lookup"><span data-stu-id="cbb88-104">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="cbb88-105">Consulte [referência de rede][DevtoolsNetworkReference] , se você quiser procurar recursos.</span><span class="sxs-lookup"><span data-stu-id="cbb88-105">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="cbb88-106">Quando usar o painel de rede</span><span class="sxs-lookup"><span data-stu-id="cbb88-106">When to use the Network panel</span></span>   

<span data-ttu-id="cbb88-107">Em geral, use o painel de rede quando precisar ter certeza de que os recursos estão sendo baixados ou carregados como esperado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-107">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="cbb88-108">Os casos de uso mais comuns do painel rede são:</span><span class="sxs-lookup"><span data-stu-id="cbb88-108">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="cbb88-109">Garantir que os recursos estejam realmente sendo carregados ou baixados.</span><span class="sxs-lookup"><span data-stu-id="cbb88-109">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="cbb88-110">Inspecionar as propriedades de um recurso individual, como cabeçalhos HTTP, conteúdo, tamanho e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cbb88-110">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  

<span data-ttu-id="cbb88-111">Se você estiver procurando maneiras de melhorar o desempenho do carregamento de página, **não** comece com o painel de rede.</span><span class="sxs-lookup"><span data-stu-id="cbb88-111">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="cbb88-112">Há muitos tipos de problemas de desempenho de carga que não estão relacionados à atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="cbb88-112">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="cbb88-113">Comece com o painel auditorias porque ele fornece sugestões direcionadas sobre como melhorar sua página.</span><span class="sxs-lookup"><span data-stu-id="cbb88-113">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="cbb88-114">Consulte [otimizar a velocidade do site][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="cbb88-114">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="cbb88-115">Abrir o painel rede</span><span class="sxs-lookup"><span data-stu-id="cbb88-115">Open the Network panel</span></span>   

<span data-ttu-id="cbb88-116">Para aproveitar ao máximo este tutorial, abra a demonstração e experimente os recursos na página de demonstração.</span><span class="sxs-lookup"><span data-stu-id="cbb88-116">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="cbb88-117">Abra a [demonstração][GlitchNetworkGetStarted] de introdução.</span><span class="sxs-lookup"><span data-stu-id="cbb88-117">Open the [Get Started Demo][GlitchNetworkGetStarted] .</span></span>  
    
    > ##### <span data-ttu-id="cbb88-118">Figura 1</span><span class="sxs-lookup"><span data-stu-id="cbb88-118">Figure 1</span></span>  
    > <span data-ttu-id="cbb88-119">A demonstração</span><span class="sxs-lookup"><span data-stu-id="cbb88-119">The demo</span></span>  
    > ![A demonstração][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  <span data-ttu-id="cbb88-121">Para [abrir o devtools][DevToolsOpen] , pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="cbb88-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="cbb88-122">O painel **console** será aberto.</span><span class="sxs-lookup"><span data-stu-id="cbb88-122">The **Console** panel opens.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="cbb88-123">Figure 2</span></span>  
    > <span data-ttu-id="cbb88-124">O console</span><span class="sxs-lookup"><span data-stu-id="cbb88-124">The Console</span></span>  
    > <span data-ttu-id="cbb88-125">! [O console] [ImagesTutorialConsole]</span><span class="sxs-lookup"><span data-stu-id="cbb88-125">![The Console][ImagesTutorialConsole]</span></span>  
    
    <span data-ttu-id="cbb88-126">Você pode preferir [encaixar devtools na parte inferior da janela][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="cbb88-126">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="cbb88-127">Figura 3</span><span class="sxs-lookup"><span data-stu-id="cbb88-127">Figure 3</span></span>  
    > <span data-ttu-id="cbb88-128">DevTools encaixado na parte inferior da janela</span><span class="sxs-lookup"><span data-stu-id="cbb88-128">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="cbb88-129">! [DevTools encaixado na parte inferior da janela] [ImagesTutorialDocked]</span><span class="sxs-lookup"><span data-stu-id="cbb88-129">![DevTools docked to the bottom of the window][ImagesTutorialDocked]</span></span>  

1.  <span data-ttu-id="cbb88-130">Selecione a guia **rede** .  O painel rede é aberto.</span><span class="sxs-lookup"><span data-stu-id="cbb88-130">Select the **Network** tab.  The Network panel opens.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-131">Figura 4</span><span class="sxs-lookup"><span data-stu-id="cbb88-131">Figure 4</span></span>  
    > <span data-ttu-id="cbb88-132">DevTools encaixado na parte inferior da janela</span><span class="sxs-lookup"><span data-stu-id="cbb88-132">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="cbb88-133">! [DevTools encaixado na parte inferior da janela] [ImagesTutorialNetwork]</span><span class="sxs-lookup"><span data-stu-id="cbb88-133">![DevTools docked to the bottom of the window][ImagesTutorialNetwork]</span></span>  

<span data-ttu-id="cbb88-134">No momento, o painel de rede está vazio.</span><span class="sxs-lookup"><span data-stu-id="cbb88-134">Right now the Network panel is empty.</span></span>  <span data-ttu-id="cbb88-135">O DevTools somente registra a atividade de rede depois que você a abre e não ocorreu nenhuma atividade de rede desde que você tenha aberto o DevTools.</span><span class="sxs-lookup"><span data-stu-id="cbb88-135">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="cbb88-136">Registrar atividades de rede</span><span class="sxs-lookup"><span data-stu-id="cbb88-136">Log network activity</span></span>   

<span data-ttu-id="cbb88-137">Para exibir a atividade de rede que uma página causa:</span><span class="sxs-lookup"><span data-stu-id="cbb88-137">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="cbb88-138">Recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="cbb88-138">Reload the page.</span></span>  <span data-ttu-id="cbb88-139">O painel rede registra toda a atividade de rede no **log de rede**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-139">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-140">Figura 5</span><span class="sxs-lookup"><span data-stu-id="cbb88-140">Figure 5</span></span>  
    > <span data-ttu-id="cbb88-141">O log de rede</span><span class="sxs-lookup"><span data-stu-id="cbb88-141">The Network Log</span></span>  
    > <span data-ttu-id="cbb88-142">! [O log de rede] [ImagesTutorialLog]</span><span class="sxs-lookup"><span data-stu-id="cbb88-142">![The Network Log][ImagesTutorialLog]</span></span>  
    
    <span data-ttu-id="cbb88-143">Cada linha do **log de rede** representa um recurso.</span><span class="sxs-lookup"><span data-stu-id="cbb88-143">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="cbb88-144">Por padrão, os recursos são listados cronologicamente.</span><span class="sxs-lookup"><span data-stu-id="cbb88-144">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="cbb88-145">O recurso superior geralmente é o principal documento HTML.</span><span class="sxs-lookup"><span data-stu-id="cbb88-145">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="cbb88-146">O recurso de baixo é o que foi solicitado por último.</span><span class="sxs-lookup"><span data-stu-id="cbb88-146">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="cbb88-147">Cada coluna representa informações sobre um recurso.</span><span class="sxs-lookup"><span data-stu-id="cbb88-147">Each column represents information about a resource.</span></span>  <span data-ttu-id="cbb88-148">A [**Figura 6**](#figure-6) mostra as colunas padrão:</span><span class="sxs-lookup"><span data-stu-id="cbb88-148">[**Figure 6**](#figure-6) shows the default columns:</span></span>  

    *   <span data-ttu-id="cbb88-149">**Status**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-149">**Status**.</span></span>  <span data-ttu-id="cbb88-150">O código de status HTTP para resposta.</span><span class="sxs-lookup"><span data-stu-id="cbb88-150">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="cbb88-151">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-151">**Type**.</span></span>  <span data-ttu-id="cbb88-152">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="cbb88-152">The resource type.</span></span>  
    *   <span data-ttu-id="cbb88-153">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-153">**Initiator**.</span></span>  <span data-ttu-id="cbb88-154">A causa da solicitação do recurso.</span><span class="sxs-lookup"><span data-stu-id="cbb88-154">The cause of the resource request.</span></span>  <span data-ttu-id="cbb88-155">Selecionar um link na coluna do iniciador leva você ao código-fonte que causou a solicitação.</span><span class="sxs-lookup"><span data-stu-id="cbb88-155">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="cbb88-156">**Tempo**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-156">**Time**.</span></span>  <span data-ttu-id="cbb88-157">A duração da solicitação.</span><span class="sxs-lookup"><span data-stu-id="cbb88-157">The duration of the request.</span></span>  
    *   <span data-ttu-id="cbb88-158">**Cascata**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-158">**Waterfall**.</span></span>  <span data-ttu-id="cbb88-159">Uma representação gráfica dos diferentes estágios da solicitação.</span><span class="sxs-lookup"><span data-stu-id="cbb88-159">A graphical representation of the different stages of the request.</span></span>  
        <span data-ttu-id="cbb88-160">Passe o mouse sobre uma cascata para ver uma divisão.</span><span class="sxs-lookup"><span data-stu-id="cbb88-160">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cbb88-161">O gráfico acima do log de rede é chamado de visão geral.</span><span class="sxs-lookup"><span data-stu-id="cbb88-161">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="cbb88-162">Você não usará o gráfico de visão geral neste tutorial, portanto, poderá ocultá-lo.</span><span class="sxs-lookup"><span data-stu-id="cbb88-162">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="cbb88-163">Consulte [ocultar o painel Visão geral][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="cbb88-163">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
        
1.  <span data-ttu-id="cbb88-164">Depois de abrir o DevTools, ele registra a atividade de rede no log de rede.</span><span class="sxs-lookup"><span data-stu-id="cbb88-164">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="cbb88-165">Para demonstrar isso, primeiro examine a parte inferior do **log de rede** e faça uma anotação mental da última atividade.</span><span class="sxs-lookup"><span data-stu-id="cbb88-165">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="cbb88-166">Agora, selecione o botão **obter dados** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="cbb88-166">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="cbb88-167">Examine a parte inferior do **log de rede** novamente.</span><span class="sxs-lookup"><span data-stu-id="cbb88-167">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="cbb88-168">Você deve ver um novo recurso chamado `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="cbb88-168">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="cbb88-169">Selecionar o botão **obter dados** fez com que a página solicitasse esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="cbb88-169">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-170">Figura 6</span><span class="sxs-lookup"><span data-stu-id="cbb88-170">Figure 6</span></span>  
    > <span data-ttu-id="cbb88-171">Um novo recurso no log de rede</span><span class="sxs-lookup"><span data-stu-id="cbb88-171">A new resource in the Network Log</span></span>  
    > <span data-ttu-id="cbb88-172">! [Um novo recurso no log de rede] [ImagesTutorialRuntime]</span><span class="sxs-lookup"><span data-stu-id="cbb88-172">![A new resource in the Network Log][ImagesTutorialRuntime]</span></span>  

## <span data-ttu-id="cbb88-173">Mostrar mais informações</span><span class="sxs-lookup"><span data-stu-id="cbb88-173">Show more information</span></span>   

<span data-ttu-id="cbb88-174">As colunas do log de rede são configuráveis.</span><span class="sxs-lookup"><span data-stu-id="cbb88-174">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="cbb88-175">Você pode ocultar colunas que não está usando.</span><span class="sxs-lookup"><span data-stu-id="cbb88-175">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="cbb88-176">Também há muitas colunas que estão ocultas por padrão que podem ser úteis.</span><span class="sxs-lookup"><span data-stu-id="cbb88-176">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="cbb88-177">Clique com o botão direito do mouse no cabeçalho da tabela de log de rede e selecione **domínio**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-177">Right-click the header of the Network Log table and select **Domain**.</span></span>  <span data-ttu-id="cbb88-178">O domínio de cada recurso agora é mostrado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-178">The domain of each resource is now shown.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-179">Figura 7</span><span class="sxs-lookup"><span data-stu-id="cbb88-179">Figure 7</span></span>  
    > <span data-ttu-id="cbb88-180">Habilitando a coluna domínio</span><span class="sxs-lookup"><span data-stu-id="cbb88-180">Enabling the Domain column</span></span>  
    > <span data-ttu-id="cbb88-181">! [Habilitando a coluna de domínio] [ImagesTutorialDomain]</span><span class="sxs-lookup"><span data-stu-id="cbb88-181">![Enabling the Domain column][ImagesTutorialDomain]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="cbb88-182">Veja a URL completa de um recurso passando o mouse sobre a célula na coluna **nome** .</span><span class="sxs-lookup"><span data-stu-id="cbb88-182">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  

## <span data-ttu-id="cbb88-183">Simular uma conexão de rede mais lenta</span><span class="sxs-lookup"><span data-stu-id="cbb88-183">Simulate a slower network connection</span></span>   

<span data-ttu-id="cbb88-184">A conexão de rede do computador que você usa para criar sites é provavelmente mais rápida do que as conexões de rede dos dispositivos móveis dos seus usuários.</span><span class="sxs-lookup"><span data-stu-id="cbb88-184">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="cbb88-185">Ao estreitar a página, você tem uma ideia melhor do tempo que uma página leva para ser carregada em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="cbb88-185">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="cbb88-186">Selecione o menu suspenso **regulagem** , que é definido como **online** por padrão.</span><span class="sxs-lookup"><span data-stu-id="cbb88-186">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-187">Figura 8</span><span class="sxs-lookup"><span data-stu-id="cbb88-187">Figure 8</span></span>  
    > <span data-ttu-id="cbb88-188">Habilitando a limitação</span><span class="sxs-lookup"><span data-stu-id="cbb88-188">Enabling throttling</span></span>  
    > <span data-ttu-id="cbb88-189">! [Habilitando limitação] [ImagesTutorialThrottling]</span><span class="sxs-lookup"><span data-stu-id="cbb88-189">![Enabling throttling][ImagesTutorialThrottling]</span></span>  
    
1.  <span data-ttu-id="cbb88-190">Selecione **3G lento**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-190">Select **Slow 3G**.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-191">Figura 9</span><span class="sxs-lookup"><span data-stu-id="cbb88-191">Figure 9</span></span>  
    > <span data-ttu-id="cbb88-192">Seleção de 3G lento</span><span class="sxs-lookup"><span data-stu-id="cbb88-192">Selecting Slow 3G</span></span>  
    > <span data-ttu-id="cbb88-193">! [Seleção de 3G lento] [ImagesTutorialSlow3G]</span><span class="sxs-lookup"><span data-stu-id="cbb88-193">![Selecting Slow 3G][ImagesTutorialSlow3G]</span></span>  
    
1.  <span data-ttu-id="cbb88-194">Longo **-pressione a recarga do** recarregamento ![ ][ImageRefreshIcon] e selecione **esvaziar cache e recarregamento físico**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-194">Long-press **Reload** ![Reload][ImageRefreshIcon] and then select **Empty Cache And Hard Reload**.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-195">Figura 10</span><span class="sxs-lookup"><span data-stu-id="cbb88-195">Figure 10</span></span>  
    > <span data-ttu-id="cbb88-196">Esvaziar o cache e o recarregamento rígido</span><span class="sxs-lookup"><span data-stu-id="cbb88-196">Empty Cache And Hard Reload</span></span>  
    > <span data-ttu-id="cbb88-197">! [Esvaziar o cache e o recarregamento de disco rígido] [ImagesTutorialHardReload]</span><span class="sxs-lookup"><span data-stu-id="cbb88-197">![Empty Cache And Hard Reload][ImagesTutorialHardReload]</span></span>  
    
    <span data-ttu-id="cbb88-198">Em visitas de repetição, o navegador geralmente serve alguns arquivos do [cache][MDNHTTPCache] , o que acelera a carga da página.</span><span class="sxs-lookup"><span data-stu-id="cbb88-198">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache] , which speeds up the page load.</span></span>  <span data-ttu-id="cbb88-199">O **cache vazio e o recarregamento rígido** força o navegador a acessar a rede para todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="cbb88-199">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="cbb88-200">Isso é útil quando você deseja ver como um visitante do primeiro visitante experimenta um carregamento de página.</span><span class="sxs-lookup"><span data-stu-id="cbb88-200">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cbb88-201">O fluxo de trabalho do **cache e do recarregamento de disco vazio** só está disponível quando o devtools está aberto.</span><span class="sxs-lookup"><span data-stu-id="cbb88-201">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  

## <span data-ttu-id="cbb88-202">Capturar capturas de tela</span><span class="sxs-lookup"><span data-stu-id="cbb88-202">Capture screenshots</span></span>   

<span data-ttu-id="cbb88-203">As capturas de tela permitem ver como uma página é exibida ao longo do tempo durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="cbb88-203">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="cbb88-204">Selecione ![ configurações ][ImageSettingsIcon] de rede e marque a caixa de seleção **captura de tela de captura** .</span><span class="sxs-lookup"><span data-stu-id="cbb88-204">Select ![Network settings][ImageSettingsIcon] and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="cbb88-205">Recarregue a página novamente por meio do fluxo de trabalho do **cache vazio e do recarregamento de disco** .</span><span class="sxs-lookup"><span data-stu-id="cbb88-205">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="cbb88-206">Consulte [simular uma conexão mais lenta](#simulate-a-slower-network-connection) se você precisar de um lembrete sobre como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="cbb88-206">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="cbb88-207">O painel capturas de tela fornece miniaturas de como a página examinou em vários pontos durante o processo de carregamento.</span><span class="sxs-lookup"><span data-stu-id="cbb88-207">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-208">Figura 11</span><span class="sxs-lookup"><span data-stu-id="cbb88-208">Figure 11</span></span>  
    > <span data-ttu-id="cbb88-209">Capturas de tela do carregamento de página</span><span class="sxs-lookup"><span data-stu-id="cbb88-209">Screenshots of the page load</span></span>  
    > <span data-ttu-id="cbb88-210">! [Capturas de tela do carregamento da página] [ImagesTutorialAllScreenshots]</span><span class="sxs-lookup"><span data-stu-id="cbb88-210">![Screenshots of the page load][ImagesTutorialAllScreenshots]</span></span>  

1.  <span data-ttu-id="cbb88-211">Selecione a primeira miniatura.</span><span class="sxs-lookup"><span data-stu-id="cbb88-211">Select the first thumbnail.</span></span>  <span data-ttu-id="cbb88-212">O DevTools mostra o que a atividade de rede estava ocorrendo nesse momento.</span><span class="sxs-lookup"><span data-stu-id="cbb88-212">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-213">Figura 12</span><span class="sxs-lookup"><span data-stu-id="cbb88-213">Figure 12</span></span>  
    > <span data-ttu-id="cbb88-214">A atividade de rede que está acontecendo durante a primeira captura de tela</span><span class="sxs-lookup"><span data-stu-id="cbb88-214">The network activity that was happening during the first screenshot</span></span>  
    > <span data-ttu-id="cbb88-215">! [A atividade de rede que estava acontecendo durante a primeira captura de tela] [ImagesTutorialFirstScreenshot]</span><span class="sxs-lookup"><span data-stu-id="cbb88-215">![The network activity that was happening during the first screenshot][ImagesTutorialFirstScreenshot]</span></span>  

1.  <span data-ttu-id="cbb88-216">Selecione ![ as configurações ][ImageSettingsIcon] de rede novamente e desmarque a caixa de seleção **capturar capturas de tela** para fechar o painel capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="cbb88-216">Select ![Network settings][ImageSettingsIcon] again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="cbb88-217">Recarregue a página novamente.</span><span class="sxs-lookup"><span data-stu-id="cbb88-217">Reload the page again.</span></span>  

## <span data-ttu-id="cbb88-218">Inspecionar os detalhes do recurso</span><span class="sxs-lookup"><span data-stu-id="cbb88-218">Inspect the details of the resource</span></span>   

<span data-ttu-id="cbb88-219">Selecione um recurso para saber mais sobre ele.</span><span class="sxs-lookup"><span data-stu-id="cbb88-219">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="cbb88-220">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="cbb88-220">Try it now:</span></span>  

1.  <span data-ttu-id="cbb88-221">Selecione `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="cbb88-221">Select `getstarted.html`.</span></span>  <span data-ttu-id="cbb88-222">A guia **cabeçalhos** é mostrada.</span><span class="sxs-lookup"><span data-stu-id="cbb88-222">The **Headers** tab is shown.</span></span>  <span data-ttu-id="cbb88-223">Use esta guia para inspecionar cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="cbb88-223">Use this tab to inspect HTTP headers.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-224">Figura 13</span><span class="sxs-lookup"><span data-stu-id="cbb88-224">Figure 13</span></span>  
    > <span data-ttu-id="cbb88-225">A guia cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="cbb88-225">The Headers tab</span></span>  
    > <span data-ttu-id="cbb88-226">! [A guia cabeçalhos] [ImagesTutorialHeaders]</span><span class="sxs-lookup"><span data-stu-id="cbb88-226">![The Headers tab][ImagesTutorialHeaders]</span></span>  
    
1.  <span data-ttu-id="cbb88-227">Selecione a guia **Visualizar** .  Uma renderização básica do HTML é mostrada.</span><span class="sxs-lookup"><span data-stu-id="cbb88-227">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-228">Figura 14</span><span class="sxs-lookup"><span data-stu-id="cbb88-228">Figure 14</span></span>  
    > <span data-ttu-id="cbb88-229">A guia Visualização</span><span class="sxs-lookup"><span data-stu-id="cbb88-229">The Preview tab</span></span>  
    > <span data-ttu-id="cbb88-230">! [A guia Visualização] [ImagesTutorialPreview]</span><span class="sxs-lookup"><span data-stu-id="cbb88-230">![The Preview tab][ImagesTutorialPreview]</span></span>  

     <span data-ttu-id="cbb88-231">Esta guia é útil quando uma API retorna um código de erro em HTML.</span><span class="sxs-lookup"><span data-stu-id="cbb88-231">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="cbb88-232">Pode ser mais fácil ler o HTML renderizado do que o código-fonte HTML ou ao inspecionar imagens.</span><span class="sxs-lookup"><span data-stu-id="cbb88-232">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="cbb88-233">Selecione a guia **resposta** .  O código-fonte HTML é mostrado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-233">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-234">Figura 15</span><span class="sxs-lookup"><span data-stu-id="cbb88-234">Figure 15</span></span>  
    > <span data-ttu-id="cbb88-235">A guia resposta</span><span class="sxs-lookup"><span data-stu-id="cbb88-235">The Response tab</span></span>  
    > <span data-ttu-id="cbb88-236">! [A guia resposta] [ImagesTutorialResponse]</span><span class="sxs-lookup"><span data-stu-id="cbb88-236">![The Response tab][ImagesTutorialResponse]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="cbb88-237">Quando um arquivo é minified, **selecionar o** ![ botão Formatar formato ][ImageFormatIcon] na parte inferior da guia **resposta** reformata o conteúdo do arquivo para facilitar a leitura.</span><span class="sxs-lookup"><span data-stu-id="cbb88-237">When a file is minified, selecting the **Format** ![Format][ImageFormatIcon] button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  

1.  <span data-ttu-id="cbb88-238">Selecione a guia **intervalo** .  Uma divisão da atividade de rede desse recurso é mostrada.</span><span class="sxs-lookup"><span data-stu-id="cbb88-238">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-239">Figura 16</span><span class="sxs-lookup"><span data-stu-id="cbb88-239">Figure 16</span></span>  
    > <span data-ttu-id="cbb88-240">A guia intervalo</span><span class="sxs-lookup"><span data-stu-id="cbb88-240">The Timing tab</span></span>  
    > <span data-ttu-id="cbb88-241">! [A guia intervalo] [ImagesTutorialTiming]</span><span class="sxs-lookup"><span data-stu-id="cbb88-241">![The Timing tab][ImagesTutorialTiming]</span></span>  

1.  <span data-ttu-id="cbb88-242">Selecione **fechar** ![ fechar ][ImageCloseIcon] para exibir o log de rede novamente.</span><span class="sxs-lookup"><span data-stu-id="cbb88-242">Select **Close** ![Close][ImageCloseIcon] to view the Network Log again.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-243">Figura 17</span><span class="sxs-lookup"><span data-stu-id="cbb88-243">Figure 17</span></span>  
    > <span data-ttu-id="cbb88-244">O botão fechar</span><span class="sxs-lookup"><span data-stu-id="cbb88-244">The Close button</span></span>  
    > <span data-ttu-id="cbb88-245">! [O botão fechar] [ImagesTutorialCloseTiming]</span><span class="sxs-lookup"><span data-stu-id="cbb88-245">![The Close button][ImagesTutorialCloseTiming]</span></span>  

## <span data-ttu-id="cbb88-246">Pesquisar cabeçalhos e respostas de rede</span><span class="sxs-lookup"><span data-stu-id="cbb88-246">Search network headers and responses</span></span>   

<span data-ttu-id="cbb88-247">Use o painel **Pesquisar** quando você precisar pesquisar os cabeçalhos HTTP e as respostas de todos os recursos para uma determinada cadeia de caracteres ou expressão regular.</span><span class="sxs-lookup"><span data-stu-id="cbb88-247">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="cbb88-248">Por exemplo, suponha que você queira verificar se seus recursos estão usando **políticas de cache**razoáveis.</span><span class="sxs-lookup"><span data-stu-id="cbb88-248">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="cbb88-249">Selecione **Pesquisar** ![ pesquisa ][ImageSearchIcon] .</span><span class="sxs-lookup"><span data-stu-id="cbb88-249">Select **Search** ![Search][ImageSearchIcon].</span></span>  <span data-ttu-id="cbb88-250">O painel Pesquisar é aberto à esquerda do log de rede.</span><span class="sxs-lookup"><span data-stu-id="cbb88-250">The Search pane opens to the left of the Network log.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-251">Figura 18</span><span class="sxs-lookup"><span data-stu-id="cbb88-251">Figure 18</span></span>  
    > <span data-ttu-id="cbb88-252">Painel de pesquisa</span><span class="sxs-lookup"><span data-stu-id="cbb88-252">The Search pane</span></span>  
    > <span data-ttu-id="cbb88-253">! [O painel Pesquisar] [ImagesTutorialSearch]</span><span class="sxs-lookup"><span data-stu-id="cbb88-253">![The Search pane][ImagesTutorialSearch]</span></span>  

1.  <span data-ttu-id="cbb88-254">Digite `Cache-Control` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cbb88-254">Type `Cache-Control` and press `Enter`.</span></span>  <span data-ttu-id="cbb88-255">O painel Pesquisar lista todas as ocorrências `Cache-Control` que ele encontra em cabeçalhos ou conteúdo do recurso.</span><span class="sxs-lookup"><span data-stu-id="cbb88-255">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-256">Figura 19</span><span class="sxs-lookup"><span data-stu-id="cbb88-256">Figure 19</span></span>  
    > <span data-ttu-id="cbb88-257">Resultados da pesquisa‎‏ para </span><span class="sxs-lookup"><span data-stu-id="cbb88-257">Search results for</span></span> `Cache-Control`  
    > <span data-ttu-id="cbb88-258">! [Resultados da pesquisa para Cache-Control] [ImagesTutorialResults]</span><span class="sxs-lookup"><span data-stu-id="cbb88-258">![Search results for Cache-Control][ImagesTutorialResults]</span></span>  

1.  <span data-ttu-id="cbb88-259">Selecione um resultado para exibir o recurso no qual o resultado foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-259">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="cbb88-260">Se você estiver vendo os detalhes do recurso, selecione um resultado para ir diretamente para ele.</span><span class="sxs-lookup"><span data-stu-id="cbb88-260">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="cbb88-261">Por exemplo, se a consulta foi encontrada em um cabeçalho, a guia cabeçalhos será aberta.</span><span class="sxs-lookup"><span data-stu-id="cbb88-261">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="cbb88-262">Se a consulta foi encontrada em conteúdo, a guia **resposta** é aberta.</span><span class="sxs-lookup"><span data-stu-id="cbb88-262">If the query was found in content, the **Response** tab opens.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-263">Figura 20</span><span class="sxs-lookup"><span data-stu-id="cbb88-263">Figure 20</span></span>  
    > <span data-ttu-id="cbb88-264">Um resultado da pesquisa realçado na guia cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="cbb88-264">A search result highlighted in the Headers tab</span></span>  
    > <span data-ttu-id="cbb88-265">! [Um resultado de pesquisa é realçado na guia cabeçalhos] [ImagesTutorialCache]</span><span class="sxs-lookup"><span data-stu-id="cbb88-265">![A search result highlighted in the Headers tab][ImagesTutorialCache]</span></span>  
    
1.  <span data-ttu-id="cbb88-266">Feche o painel Pesquisar e a guia cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="cbb88-266">Close the Search pane and the Headers tab.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-267">Figura 21</span><span class="sxs-lookup"><span data-stu-id="cbb88-267">Figure 21</span></span>  
    > <span data-ttu-id="cbb88-268">Os botões fechar</span><span class="sxs-lookup"><span data-stu-id="cbb88-268">The Close buttons</span></span>  
    > <span data-ttu-id="cbb88-269">! [Os botões fechar] [ImagesTutorialCloseButtons]</span><span class="sxs-lookup"><span data-stu-id="cbb88-269">![The Close buttons][ImagesTutorialCloseButtons]</span></span>  
    
## <span data-ttu-id="cbb88-270">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="cbb88-270">Filter resources</span></span>   

<span data-ttu-id="cbb88-271">O DevTools oferece vários fluxos de trabalho para a filtragem de recursos que não são relevantes para a tarefa em questão.</span><span class="sxs-lookup"><span data-stu-id="cbb88-271">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

> ##### <span data-ttu-id="cbb88-272">Figura 22</span><span class="sxs-lookup"><span data-stu-id="cbb88-272">Figure 22</span></span>  
> <span data-ttu-id="cbb88-273">A barra de ferramentas filtros</span><span class="sxs-lookup"><span data-stu-id="cbb88-273">The Filters toolbar</span></span>  
> <span data-ttu-id="cbb88-274">! [A barra de ferramentas filtros] [ImagesTutorialFilters]</span><span class="sxs-lookup"><span data-stu-id="cbb88-274">![The Filters toolbar][ImagesTutorialFilters]</span></span>  

<span data-ttu-id="cbb88-275">A barra de ferramentas **filtros** deve ser habilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="cbb88-275">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="cbb88-276">Se não:</span><span class="sxs-lookup"><span data-stu-id="cbb88-276">If not:</span></span>  

1.  <span data-ttu-id="cbb88-277">Selecione **Filter** ![ filtro ][ImageFilterIcon] de filtro para mostrá-lo.</span><span class="sxs-lookup"><span data-stu-id="cbb88-277">Select **Filter** ![Filter][ImageFilterIcon] to show it.</span></span>  

### <span data-ttu-id="cbb88-278">Filtrar por cadeia de caracteres, expressão regular ou propriedade</span><span class="sxs-lookup"><span data-stu-id="cbb88-278">Filter by string, regular expression, or property</span></span>   

<span data-ttu-id="cbb88-279">A caixa de texto **Filtrar** oferece suporte a muitos tipos diferentes de filtragem.</span><span class="sxs-lookup"><span data-stu-id="cbb88-279">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="cbb88-280">Digite `png` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="cbb88-280">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="cbb88-281">Somente os arquivos que contêm o texto `png` são exibidos.</span><span class="sxs-lookup"><span data-stu-id="cbb88-281">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="cbb88-282">Nesse caso, os únicos arquivos que correspondem ao filtro são as imagens PNG.</span><span class="sxs-lookup"><span data-stu-id="cbb88-282">In this case the only files that match the filter are the PNG images.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-283">Figura 23</span><span class="sxs-lookup"><span data-stu-id="cbb88-283">Figure 23</span></span>  
    > <span data-ttu-id="cbb88-284">Um filtro de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="cbb88-284">A string filter</span></span>  
    > <span data-ttu-id="cbb88-285">! [Um filtro de cadeia de caracteres] [ImagesTutorialPNG]</span><span class="sxs-lookup"><span data-stu-id="cbb88-285">![A string filter][ImagesTutorialPNG]</span></span>  

1.  <span data-ttu-id="cbb88-286">Digite `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="cbb88-286">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="cbb88-287">O DevTools filtra qualquer recurso com um nome de arquivo que não termina com um `j` ou um `c` seguido de 1 ou mais `s` caracteres.</span><span class="sxs-lookup"><span data-stu-id="cbb88-287">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-288">Figura 24</span><span class="sxs-lookup"><span data-stu-id="cbb88-288">Figure 24</span></span>  
    > <span data-ttu-id="cbb88-289">Um filtro de expressão regular</span><span class="sxs-lookup"><span data-stu-id="cbb88-289">A regular expression filter</span></span>  
    > <span data-ttu-id="cbb88-290">! [Um filtro de expressão regular] [ImagesTutorialRegEx]</span><span class="sxs-lookup"><span data-stu-id="cbb88-290">![A regular expression filter][ImagesTutorialRegEx]</span></span>  
    
1.  <span data-ttu-id="cbb88-291">Digite `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="cbb88-291">Type `-main.css`.</span></span>  <span data-ttu-id="cbb88-292">DevTools filtros desconectados `main.css` .</span><span class="sxs-lookup"><span data-stu-id="cbb88-292">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="cbb88-293">Se qualquer outro arquivo coincidir com o padrão, ele também será filtrado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-293">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-294">Figura 25</span><span class="sxs-lookup"><span data-stu-id="cbb88-294">Figure 25</span></span>  
    > <span data-ttu-id="cbb88-295">Um filtro negativo</span><span class="sxs-lookup"><span data-stu-id="cbb88-295">A negative filter</span></span>  
    > <span data-ttu-id="cbb88-296">! [Um filtro negativo] [ImagesTutorialNegative]</span><span class="sxs-lookup"><span data-stu-id="cbb88-296">![A negative filter][ImagesTutorialNegative]</span></span>  
    
1.  <span data-ttu-id="cbb88-297">Digite `domain:cdn.glitch.com` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="cbb88-297">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="cbb88-298">O DevTools filtra qualquer recurso com uma URL que não corresponde a este domínio.</span><span class="sxs-lookup"><span data-stu-id="cbb88-298">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-299">Figura 26</span><span class="sxs-lookup"><span data-stu-id="cbb88-299">Figure 26</span></span>  
    > <span data-ttu-id="cbb88-300">Um filtro de propriedade</span><span class="sxs-lookup"><span data-stu-id="cbb88-300">A property filter</span></span>  
    > <span data-ttu-id="cbb88-301">! [Um filtro de propriedade] [ImagesTutorialProperty]</span><span class="sxs-lookup"><span data-stu-id="cbb88-301">![A property filter][ImagesTutorialProperty]</span></span>  

    <span data-ttu-id="cbb88-302">Consulte [Filtrar solicitações por Propriedades][DevtoolsReferenceProperty] para obter a lista completa de propriedades filtráveis.</span><span class="sxs-lookup"><span data-stu-id="cbb88-302">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
    
1.  <span data-ttu-id="cbb88-303">Desmarque a caixa de texto **Filtrar** de qualquer texto.</span><span class="sxs-lookup"><span data-stu-id="cbb88-303">Clear the **Filter** text box of any text.</span></span>  

### <span data-ttu-id="cbb88-304">Filtrar por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="cbb88-304">Filter by resource type</span></span>   

<span data-ttu-id="cbb88-305">Para se concentrar em um determinado tipo de arquivo, como folhas de estilos:</span><span class="sxs-lookup"><span data-stu-id="cbb88-305">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="cbb88-306">Selecione **CSS**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-306">Select **CSS**.</span></span>  <span data-ttu-id="cbb88-307">Todos os outros tipos de arquivo são filtrados.</span><span class="sxs-lookup"><span data-stu-id="cbb88-307">All other file types are filtered out.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-308">Figura 27</span><span class="sxs-lookup"><span data-stu-id="cbb88-308">Figure 27</span></span>  
    > <span data-ttu-id="cbb88-309">Mostrando somente arquivos CSS</span><span class="sxs-lookup"><span data-stu-id="cbb88-309">Showing CSS files only</span></span>  
    > <span data-ttu-id="cbb88-310">! [Mostrando somente arquivos CSS] [ImagesTutorialCSS]</span><span class="sxs-lookup"><span data-stu-id="cbb88-310">![Showing CSS files only][ImagesTutorialCSS]</span></span>  
    
1.  <span data-ttu-id="cbb88-311">Para ver também os scripts, segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e selecione **js**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-311">To also see scripts, hold `Control` \(Windows\) or `Command` \(macOS\) and then select **JS**.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-312">Figura 28</span><span class="sxs-lookup"><span data-stu-id="cbb88-312">Figure 28</span></span>  
    > <span data-ttu-id="cbb88-313">Mostrando somente arquivos CSS e JS</span><span class="sxs-lookup"><span data-stu-id="cbb88-313">Showing CSS and JS files only</span></span>  
    > <span data-ttu-id="cbb88-314">! [Mostrar somente arquivos CSS e JS] [ImagesTutorialCSSJS]</span><span class="sxs-lookup"><span data-stu-id="cbb88-314">![Showing CSS and JS files only][ImagesTutorialCSSJS]</span></span>  
    
1.  <span data-ttu-id="cbb88-315">Selecione **tudo** para remover os filtros e ver todos os recursos novamente.</span><span class="sxs-lookup"><span data-stu-id="cbb88-315">Select **All** to remove the filters and see all resources again.</span></span>  

<span data-ttu-id="cbb88-316">Consulte [Filtrar solicitações][DevtoolsNetworkReferenceFilter] para outros fluxos de trabalho de filtragem.</span><span class="sxs-lookup"><span data-stu-id="cbb88-316">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="cbb88-317">Bloquear solicitações</span><span class="sxs-lookup"><span data-stu-id="cbb88-317">Block requests</span></span>   

<span data-ttu-id="cbb88-318">Qual a aparência de uma página e comportamento quando alguns dos recursos da página não estão disponíveis?</span><span class="sxs-lookup"><span data-stu-id="cbb88-318">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="cbb88-319">Ele falha completamente, ou ainda é um pouco funcional?</span><span class="sxs-lookup"><span data-stu-id="cbb88-319">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="cbb88-320">Bloquear solicitações para descobrir:</span><span class="sxs-lookup"><span data-stu-id="cbb88-320">Block requests to find out:</span></span>  

1.  <span data-ttu-id="cbb88-321">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-321">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-322">Figura 29</span><span class="sxs-lookup"><span data-stu-id="cbb88-322">Figure 29</span></span>  
    > <span data-ttu-id="cbb88-323">O menu de comando</span><span class="sxs-lookup"><span data-stu-id="cbb88-323">The Command Menu</span></span>  
    > <span data-ttu-id="cbb88-324">! [O menu de comando] [ImagesTutorialCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="cbb88-324">![The Command Menu][ImagesTutorialCommandMenu]</span></span>  
    
1.  <span data-ttu-id="cbb88-325">Tipo `block` , selecione **Mostrar bloqueio de solicitação**e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cbb88-325">Type `block`, select **Show Request Blocking**, and press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-326">Figura 30</span><span class="sxs-lookup"><span data-stu-id="cbb88-326">Figure 30</span></span>  
    > <span data-ttu-id="cbb88-327">Mostrar bloqueio de solicitações</span><span class="sxs-lookup"><span data-stu-id="cbb88-327">Show Request Blocking</span></span>  
    > <span data-ttu-id="cbb88-328">! [Mostrar bloqueio de solicitação] [ImagesTutorialBlock]</span><span class="sxs-lookup"><span data-stu-id="cbb88-328">![Show Request Blocking][ImagesTutorialBlock]</span></span>  

1.  <span data-ttu-id="cbb88-329">Selecione **Adicionar padrão** ![ Adicionar padrão ][ImageAddIcon] .</span><span class="sxs-lookup"><span data-stu-id="cbb88-329">Select **Add Pattern** ![Add Pattern][ImageAddIcon].</span></span>  
1.  <span data-ttu-id="cbb88-330">Digite `main.css`.</span><span class="sxs-lookup"><span data-stu-id="cbb88-330">Type `main.css`.</span></span>  
    
    > ##### <span data-ttu-id="cbb88-331">Figura 31</span><span class="sxs-lookup"><span data-stu-id="cbb88-331">Figure 31</span></span>  
    > <span data-ttu-id="cbb88-332">Pedi</span><span class="sxs-lookup"><span data-stu-id="cbb88-332">Blocking</span></span> `main.css`  
    > <span data-ttu-id="cbb88-333">! [Bloqueando Main. CSS] [ImagesTutorialAddBlock]</span><span class="sxs-lookup"><span data-stu-id="cbb88-333">![Blocking main.css][ImagesTutorialAddBlock]</span></span>  
    
1.  <span data-ttu-id="cbb88-334">Selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="cbb88-334">Select **Add**.</span></span>  
1.  <span data-ttu-id="cbb88-335">Recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="cbb88-335">Reload the page.</span></span>  <span data-ttu-id="cbb88-336">Como esperado, o estilo da página é levemente bagunçado porque a folha de estilos principal foi bloqueada.</span><span class="sxs-lookup"><span data-stu-id="cbb88-336">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cbb88-337">A `main.css` linha no log de rede.</span><span class="sxs-lookup"><span data-stu-id="cbb88-337">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="cbb88-338">O texto vermelho significa que o recurso foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="cbb88-338">The red text means that the resource was blocked.</span></span>
    
    > ##### <span data-ttu-id="cbb88-339">Figura 32</span><span class="sxs-lookup"><span data-stu-id="cbb88-339">Figure 32</span></span>  
    > `main.css` <span data-ttu-id="cbb88-340">foi bloqueado</span><span class="sxs-lookup"><span data-stu-id="cbb88-340">has been blocked</span></span>  
    > <span data-ttu-id="cbb88-341">! [Main. CSS foi bloqueado] [ImagesTutorialBlockedStyles]</span><span class="sxs-lookup"><span data-stu-id="cbb88-341">![main.css has been blocked][ImagesTutorialBlockedStyles]</span></span>  

1.  <span data-ttu-id="cbb88-342">Desmarque a caixa de seleção **habilitar o bloqueio de solicitações** .</span><span class="sxs-lookup"><span data-stu-id="cbb88-342">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="cbb88-343">Conclusão</span><span class="sxs-lookup"><span data-stu-id="cbb88-343">Conclusion</span></span>  

<span data-ttu-id="cbb88-344">Parabéns, você concluiu o tutorial.</span><span class="sxs-lookup"><span data-stu-id="cbb88-344">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="cbb88-345">Agora você sabe como usar o painel rede no Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="cbb88-345">You now know how to use the Network panel in the Microsoft Edge DevTools!</span></span>






<span data-ttu-id="cbb88-346">Confira a [referência de rede][DevtoolsNetworkReference] para descobrir mais recursos do devtools relacionados à atividade de inspeção da rede.</span><span class="sxs-lookup"><span data-stu-id="cbb88-346">Check out the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Figura 1: a demonstração"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-console.msft.png "Figura 2: o console"  
[ImagesTutorialDocked]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-console-Bottom.msft.png "Figura 3: DevTools encaixado na parte inferior da janela"  
[ImagesTutorialNetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Bottom.msft.png "Figura 4: DevTools encaixado na parte inferior da janela"  
[ImagesTutorialLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network.msft.png "Figura 5: o log de rede"  
[ImagesTutorialRuntime]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-New-Resource.msft.png "Figura 6: um novo recurso no log de rede"  
[ImagesTutorialDomain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Edit-Column.msft.png "Figura 7: Habilitando a coluna de domínio"  
[ImagesTutorialThrottling]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-throttling.msft.png "Figura 8: habilitação da limitação"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-throttling-Slow-3G.msft.png "Figura 9: seleção de 3G lento"  
[ImagesTutorialHardReload]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Empty-cache-and-Hard-Reset.msft.png "Figura 10: cache vazio e recarregamento de disco rígido"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-screenshots.msft.png "Figura 11: capturas de tela do carregamento da página"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-screenshots-First.msft.png "Figura 12: a atividade de rede que aconteceu durante a primeira captura de tela"  
[ImagesTutorialHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Headers.msft.png "Figura 13: a guia cabeçalhos"  
[ImagesTutorialPreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Preview.msft.png "Figura 14: a guia Visualizar"  
[ImagesTutorialResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Response.msft.png "Figura 15: a guia resposta"  
[ImagesTutorialTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-timing.msft.png "Figura 16: a guia intervalo"  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Close-Tabs.msft.png "figura 17: o botão fechar"  
[ImagesTutorialSearch]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Empty.msft.png "Figura 18: o painel Pesquisar"  
[ImagesTutorialResults]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Cache-Control.msft.png "Figura 19: resultados da pesquisa para Cache-Control"  
[ImagesTutorialCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Cache-Control-Headers-Response-Headers.msft.png "Figura 20: um resultado de pesquisa realçado na guia cabeçalhos"  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Close.msft.png "figura 21: os botões fechar"  
[ImagesTutorialFilters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Empty.msft.png "Figura 22: a barra de ferramentas filtros"  
[ImagesTutorialPNG]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-png.msft.png "Figura 23: um filtro de cadeia de caracteres"  
[ImagesTutorialRegEx]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Regex.msft.png "Figura 24: um filtro de expressão regular"  
[ImagesTutorialNegative]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Negative-Statement.msft.png "figura 25: um filtro negativo"  
[ImagesTutorialProperty]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Property-Value.msft.png "Figura 26: um filtro de propriedade"  
[ImagesTutorialCSS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-File-Type-CSS.msft.png "Figura 27: mostrando apenas arquivos CSS"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-File-Type-CSS-JS.msft.png "Figura 28: mostrando somente arquivos CSS e JS"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Empty.msft.png "figura 29: o menu de comando"  
[ImagesTutorialBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block.msft.png "figura 30: mostrar bloqueio de solicitações"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Add-Pattern.msft.png "figura 31: bloqueando Main. css"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Main-CSS.msft.png "Figura 32: Main. CSS foi bloqueado"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Referência de análise de rede"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Filtrar solicitações-referência de análise de rede"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Ocultar o painel Visão geral-referência de análise de rede"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrar solicitações por Propriedades-referência de análise de rede"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge DevTools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Otimizar a velocidade do site com o Microsoft Edge DevTools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Demonstração de atividade da rede de inspeção"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Cache HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="cbb88-388">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="cbb88-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cbb88-389">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="cbb88-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cbb88-391">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cbb88-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
