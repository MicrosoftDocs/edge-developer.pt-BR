---
title: Acelerar o tempo de execução do JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 0e198be3e1cef53590a24bfaa2382746ced299ed
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611868"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# <span data-ttu-id="2afdc-103">Acelerar o tempo de execução do JavaScript</span><span class="sxs-lookup"><span data-stu-id="2afdc-103">Speed Up JavaScript Runtime</span></span>   




<span data-ttu-id="2afdc-104">Identifique funções caras usando o painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="2afdc-104">Identify expensive functions using the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="2afdc-105">Figura 1</span><span class="sxs-lookup"><span data-stu-id="2afdc-105">Figure 1</span></span>  
> <span data-ttu-id="2afdc-106">Perfis de amostragem</span><span class="sxs-lookup"><span data-stu-id="2afdc-106">Sampling Profiles</span></span>  
> ![Perfis de amostragem][ImageCpuProfile]  

### <span data-ttu-id="2afdc-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="2afdc-108">Summary</span></span>  

*   <span data-ttu-id="2afdc-109">Registre exatamente quais funções foram chamadas e quantas memórias cada requer com a amostragem de alocação no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="2afdc-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="2afdc-110">Visualize seus perfis como um gráfico de chama.</span><span class="sxs-lookup"><span data-stu-id="2afdc-110">Visualize your profiles as a flame chart.</span></span>  

## <span data-ttu-id="2afdc-111">Gravar um perfil de amostra</span><span class="sxs-lookup"><span data-stu-id="2afdc-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="2afdc-112">Se você observar o Jank em seu JavaScript, colete um perfil de amostragem.</span><span class="sxs-lookup"><span data-stu-id="2afdc-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="2afdc-113">Os perfis de amostragem mostram onde o tempo de execução é gasto em funções na sua página.</span><span class="sxs-lookup"><span data-stu-id="2afdc-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="2afdc-114">Vá para o painel **memória** do devtools.</span><span class="sxs-lookup"><span data-stu-id="2afdc-114">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="2afdc-115">Selecione o botão de opção de **amostragem de alocação** .</span><span class="sxs-lookup"><span data-stu-id="2afdc-115">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="2afdc-116">Selecione **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="2afdc-116">Select **Start**.</span></span>  
1.  <span data-ttu-id="2afdc-117">Dependendo do que você está tentando analisar, você pode recarregar a página, interagir com a página ou simplesmente deixar a página ser executada.</span><span class="sxs-lookup"><span data-stu-id="2afdc-117">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="2afdc-118">Selecione o botão **parar** quando terminar.</span><span class="sxs-lookup"><span data-stu-id="2afdc-118">Select the **Stop** button when you are finished.</span></span>  

> [!NOTE]
> <span data-ttu-id="2afdc-119">Você também pode usar a [API de utilitários de console][DevtoolsConsoleUtilities] para gravar e agrupar perfis a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="2afdc-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="2afdc-120">Ver Perfil de amostragem</span><span class="sxs-lookup"><span data-stu-id="2afdc-120">View Sampling Profile</span></span>  

<span data-ttu-id="2afdc-121">Quando terminar a gravação, o DevTools automaticamente preenche o painel **memória** em **perfis de amostragem** com os dados da sua gravação.</span><span class="sxs-lookup"><span data-stu-id="2afdc-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="2afdc-122">O modo de exibição padrão é **Heavy \ (baixo para cima \)**.</span><span class="sxs-lookup"><span data-stu-id="2afdc-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="2afdc-123">Este modo de exibição permite que você veja quais funções tiveram mais impacto no desempenho e examine os caminhos de chamadas para essas funções.</span><span class="sxs-lookup"><span data-stu-id="2afdc-123">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="2afdc-124">Alterar a ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="2afdc-124">Change sort order</span></span>   

<span data-ttu-id="2afdc-125">Para alterar a ordem de classificação, selecione o menu suspenso ao lado do ícone função selecionada foco **da função** ![ selecionada ][ImageFocusIcon] e escolha uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="2afdc-125">To change the sorting order, select the dropdown menu next to the **focus selected function** ![focus selected function][ImageFocusIcon] icon and then choose one of the following options.</span></span>

<span data-ttu-id="2afdc-126">**Gráfico**.</span><span class="sxs-lookup"><span data-stu-id="2afdc-126">**Chart**.</span></span>  <span data-ttu-id="2afdc-127">Exibe um gráfico cronológico da gravação.</span><span class="sxs-lookup"><span data-stu-id="2afdc-127">Displays a chronological chart of the recording.</span></span>  

> ##### <span data-ttu-id="2afdc-128">Figura 2</span><span class="sxs-lookup"><span data-stu-id="2afdc-128">Figure 2</span></span>  
> <span data-ttu-id="2afdc-129">Gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="2afdc-129">Flame chart</span></span>  
> ![Gráfico de chama][ImageFlameChart]  

<span data-ttu-id="2afdc-131">**Pesado \ (abaixo)**.</span><span class="sxs-lookup"><span data-stu-id="2afdc-131">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="2afdc-132">Lista as funções por meio do impacto no desempenho e permite que você examine os caminhos de chamadas para as funções.</span><span class="sxs-lookup"><span data-stu-id="2afdc-132">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="2afdc-133">Este é o modo de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="2afdc-133">This is the default view.</span></span>  

> ##### <span data-ttu-id="2afdc-134">Figura 3</span><span class="sxs-lookup"><span data-stu-id="2afdc-134">Figure 3</span></span>  
> <span data-ttu-id="2afdc-135">Gráfico pesado</span><span class="sxs-lookup"><span data-stu-id="2afdc-135">Heavy chart</span></span>  
> ![Gráfico pesado][ImageHeavyChart]  

<span data-ttu-id="2afdc-137">**Árvore \ (acima para baixo \)**.</span><span class="sxs-lookup"><span data-stu-id="2afdc-137">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="2afdc-138">Mostra uma imagem geral da estrutura de chamadas, começando na parte superior da pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2afdc-138">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

> ##### <span data-ttu-id="2afdc-139">Figura 4</span><span class="sxs-lookup"><span data-stu-id="2afdc-139">Figure 4</span></span>  
> <span data-ttu-id="2afdc-140">Gráfico de árvore</span><span class="sxs-lookup"><span data-stu-id="2afdc-140">Tree chart</span></span>  
> ![Gráfico de árvore][ImageTreeChart]  

### <span data-ttu-id="2afdc-142">Funções Exclude</span><span class="sxs-lookup"><span data-stu-id="2afdc-142">Exclude functions</span></span>   

<span data-ttu-id="2afdc-143">Para excluir uma função do seu perfil de amostragem, selecione-a para selecioná-la e, em seguida, **Selecione o ícone Excluir função** selecionada ![ excluir função selecionada ][ImageExcludeIcon] .</span><span class="sxs-lookup"><span data-stu-id="2afdc-143">To exclude a function from your Sampling Profile, select it to select it and then select the **exclude selected function** ![exclude selected function][ImageExcludeIcon] icon.</span></span>  <span data-ttu-id="2afdc-144">A função solicitante \ (pai \) da função excluída \ (filho \) é cobrada pela memória alocada atribuída à função excluída \ (filho \).</span><span class="sxs-lookup"><span data-stu-id="2afdc-144">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="2afdc-145">Selecione o ícone **restaurar todas** as funções ![ restaurar todas as funções ][ImageRestoreIcon] para restaurar novamente todas as funções excluídas na gravação.</span><span class="sxs-lookup"><span data-stu-id="2afdc-145">Select the **restore all functions** ![restore all functions][ImageRestoreIcon] icon to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="2afdc-146">Exibir Perfil de amostra como gráfico</span><span class="sxs-lookup"><span data-stu-id="2afdc-146">View Sampling Profile as Chart</span></span>   

<span data-ttu-id="2afdc-147">O modo de exibição de gráfico fornece uma representação visual do perfil de amostragem ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="2afdc-147">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="2afdc-148">Depois de [gravar um perfil de amostragem](#record-a-sampling-profile), exiba a gravação como um gráfico de chama, [alterando a ordem de classificação](#change-sort-order) para **gráfico**.</span><span class="sxs-lookup"><span data-stu-id="2afdc-148">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

> ##### <span data-ttu-id="2afdc-149">Figura 5</span><span class="sxs-lookup"><span data-stu-id="2afdc-149">Figure 5</span></span>  
> <span data-ttu-id="2afdc-150">Modo de exibição de gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="2afdc-150">Flame chart view</span></span>  
> ![Modo de exibição de gráfico de chama][ImageFlameChartView]  

<span data-ttu-id="2afdc-152">O gráfico de chama é dividido em duas partes.</span><span class="sxs-lookup"><span data-stu-id="2afdc-152">The flame chart is split into two parts.</span></span>  

| | <span data-ttu-id="2afdc-153">Parte</span><span class="sxs-lookup"><span data-stu-id="2afdc-153">Part</span></span> | <span data-ttu-id="2afdc-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="2afdc-154">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="2afdc-155">um</span><span class="sxs-lookup"><span data-stu-id="2afdc-155">1</span></span> | <span data-ttu-id="2afdc-156">Visão geral</span><span class="sxs-lookup"><span data-stu-id="2afdc-156">Overview</span></span> | <span data-ttu-id="2afdc-157">Uma exibição de olho de toda a gravação.</span><span class="sxs-lookup"><span data-stu-id="2afdc-157">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="2afdc-158">A altura das barras corresponde à profundidade da pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2afdc-158">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="2afdc-159">Portanto, quanto mais alta a barra, mais profunda a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2afdc-159">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="2afdc-160">2</span><span class="sxs-lookup"><span data-stu-id="2afdc-160">2</span></span> | <span data-ttu-id="2afdc-161">Pilha de chamadas</span><span class="sxs-lookup"><span data-stu-id="2afdc-161">Call Stacks</span></span> | <span data-ttu-id="2afdc-162">Esta é uma exibição detalhada das funções que foram chamadas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="2afdc-162">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="2afdc-163">O eixo horizontal é tempo e eixo vertical é a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2afdc-163">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="2afdc-164">As pilhas são organizadas de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="2afdc-164">The stacks are organized top-down.</span></span>  <span data-ttu-id="2afdc-165">Portanto, a função na parte superior acima dela e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2afdc-165">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="2afdc-166">As funções são coloridas aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="2afdc-166">Functions are colored randomly.</span></span>  <span data-ttu-id="2afdc-167">Não há nenhuma correlação entre as cores usadas nos outros painéis.</span><span class="sxs-lookup"><span data-stu-id="2afdc-167">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="2afdc-168">No entanto, as funções são sempre coloridas iguais em chamadas para que você possa ver padrões em cada tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2afdc-168">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

> ##### <span data-ttu-id="2afdc-169">Figura 6</span><span class="sxs-lookup"><span data-stu-id="2afdc-169">Figure 6</span></span>  
> <span data-ttu-id="2afdc-170">Gráfico de chama com anotações</span><span class="sxs-lookup"><span data-stu-id="2afdc-170">Annotated flame chart</span></span>  
> ![Gráfico de chama com anotações][ImageAnnotatedFlameChart]  

<span data-ttu-id="2afdc-172">Uma pilha de chamadas alta não é necessariamente importante, apenas significa que muitas funções foram chamadas.</span><span class="sxs-lookup"><span data-stu-id="2afdc-172">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="2afdc-173">Mas uma barra larga significa que uma função demorou muito tempo para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="2afdc-173">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="2afdc-174">Estes são candidatos para otimização.</span><span class="sxs-lookup"><span data-stu-id="2afdc-174">These are candidates for optimization.</span></span>  

### <span data-ttu-id="2afdc-175">Ampliar partes específicas da gravação</span><span class="sxs-lookup"><span data-stu-id="2afdc-175">Zoom in on specific parts of recording</span></span>   

<span data-ttu-id="2afdc-176">Selecione, segure e arraste o mouse para a esquerda e para a direita na visão geral para ampliar partes específicas da pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2afdc-176">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="2afdc-177">Depois de aplicar zoom, a pilha de chamadas exibirá automaticamente a parte da gravação selecionada.</span><span class="sxs-lookup"><span data-stu-id="2afdc-177">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

> ##### <span data-ttu-id="2afdc-178">Figura 7</span><span class="sxs-lookup"><span data-stu-id="2afdc-178">Figure 7</span></span>  
> <span data-ttu-id="2afdc-179">Gráfico ampliado</span><span class="sxs-lookup"><span data-stu-id="2afdc-179">Chart zoomed</span></span>  
> ![Gráfico ampliado][ImageFlameChartZoomed]  

### <span data-ttu-id="2afdc-181">Exibir detalhes da função</span><span class="sxs-lookup"><span data-stu-id="2afdc-181">View function details</span></span>   

<span data-ttu-id="2afdc-182">Selecione uma função para exibir a definição no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="2afdc-182">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="2afdc-183">Passe o mouse sobre uma função para exibir o nome e os dados de tempo.</span><span class="sxs-lookup"><span data-stu-id="2afdc-183">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="2afdc-184">As informações a seguir são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="2afdc-184">The following information is provided.</span></span>  

| <span data-ttu-id="2afdc-185">Minuciosa</span><span class="sxs-lookup"><span data-stu-id="2afdc-185">Detail</span></span> | <span data-ttu-id="2afdc-186">Descrição</span><span class="sxs-lookup"><span data-stu-id="2afdc-186">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="2afdc-187">Name</span><span class="sxs-lookup"><span data-stu-id="2afdc-187">Name</span></span>** | <span data-ttu-id="2afdc-188">O nome da função.</span><span class="sxs-lookup"><span data-stu-id="2afdc-188">The name of the function.</span></span>  |  
| **<span data-ttu-id="2afdc-189">Tamanho próprio</span><span class="sxs-lookup"><span data-stu-id="2afdc-189">Self size</span></span>** | <span data-ttu-id="2afdc-190">O tamanho da chamada atual da função, incluindo somente as instruções na função.</span><span class="sxs-lookup"><span data-stu-id="2afdc-190">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="2afdc-191">Tamanho total</span><span class="sxs-lookup"><span data-stu-id="2afdc-191">Total size</span></span>** | <span data-ttu-id="2afdc-192">O tamanho da invocação atual dessa função e de todas as funções chamadas.</span><span class="sxs-lookup"><span data-stu-id="2afdc-192">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="2afdc-193">URL</span><span class="sxs-lookup"><span data-stu-id="2afdc-193">URL</span></span>** | <span data-ttu-id="2afdc-194">O local da definição da função na forma de `base.js:261` onde `base.js` está o nome do arquivo em que a função está definida e `261` é o número da linha da definição.</span><span class="sxs-lookup"><span data-stu-id="2afdc-194">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

> ##### <span data-ttu-id="2afdc-195">Figura 8</span><span class="sxs-lookup"><span data-stu-id="2afdc-195">Figure 8</span></span>  
> <span data-ttu-id="2afdc-196">Exibir detalhes de funções no gráfico</span><span class="sxs-lookup"><span data-stu-id="2afdc-196">Viewing functions details in chart</span></span>  
> ![Exibir detalhes de funções no gráfico][ImageFunctionsDetails]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageExcludeIcon]: /microsoft-edge/devtools-guide-chromium/media/exclude-icon.msft.png  
[ImageFocusIcon]: /microsoft-edge/devtools-guide-chromium/media/images/focus-icon.msft.png  
[ImageRestoreIcon]: /microsoft-edge/devtools-guide-chromium/media/images/restore-icon.msft.png  

[ImageCpuProfile]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Figura 1: perfis de amostragem"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Figura 2: gráfico de chama"  
[ImageHeavyChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Figura 3: gráfico pesado"  
[ImageTreeChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png "Figura 4: gráfico de árvore"  
[ImageFlameChartView]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Figura 5: modo de exibição de gráfico da chama"  
[ImageAnnotatedFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png "Figura 6: gráfico de chama com anotações"  
[ImageFlameChartZoomed]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png "Figura 7: gráfico ampliado"  
[ImageFunctionsDetails]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png "Figura 8: Exibir detalhes de funções no gráfico"  

<!-- links -->  

[DevtoolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referência de API de utilitários de console"  
[DevtoolsConsoleUtilitiesProfile]: /microsoft-edge/devtools-guide-chromium/console/utilities#profile "Referência da API de utilitários do console-perfil"  
[DevtoolsConsoleUtilitiesProfileEnd]: /microsoft-edge/devtools-guide-chromium/console/utilities#profileend "profileEnd-referência de API de utilitários de console"  

> [!NOTE]
> <span data-ttu-id="2afdc-209">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="2afdc-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2afdc-210">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \) e [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="2afdc-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2afdc-212">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2afdc-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
