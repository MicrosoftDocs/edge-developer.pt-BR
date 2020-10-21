---
description: Identifique funções caras usando o painel de memória do Microsoft Edge DevTools.
title: Acelerar o Tempo de Execução do JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f3cf0440579865495f4afc8b1ae4e3940af7b04f
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125353"
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

# <span data-ttu-id="edbe0-104">Acelerar o tempo de execução do JavaScript</span><span class="sxs-lookup"><span data-stu-id="edbe0-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="edbe0-105">Identifique funções caras usando o painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="edbe0-105">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="edbe0-107">Perfis de exemplo</span><span class="sxs-lookup"><span data-stu-id="edbe0-107">Sample Profiles</span></span>  
:::image-end:::  

### <span data-ttu-id="edbe0-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="edbe0-108">Summary</span></span>  

*   <span data-ttu-id="edbe0-109">Registre exatamente quais funções foram chamadas e quantas memórias cada requer com a amostragem de alocação no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="edbe0-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="edbe0-110">Visualize seus perfis como um gráfico de chama.</span><span class="sxs-lookup"><span data-stu-id="edbe0-110">Visualize your profiles as a flame chart.</span></span>  
    
## <span data-ttu-id="edbe0-111">Gravar um perfil de amostra</span><span class="sxs-lookup"><span data-stu-id="edbe0-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="edbe0-112">Se você observar o Jank em seu JavaScript, colete um perfil de amostragem.</span><span class="sxs-lookup"><span data-stu-id="edbe0-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="edbe0-113">Os perfis de amostragem mostram onde o tempo de execução é gasto em funções na sua página.</span><span class="sxs-lookup"><span data-stu-id="edbe0-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="edbe0-114">Vá para o painel **memória** do devtools.</span><span class="sxs-lookup"><span data-stu-id="edbe0-114">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="edbe0-115">Selecione o botão de opção de **amostragem de alocação** .</span><span class="sxs-lookup"><span data-stu-id="edbe0-115">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="edbe0-116">Escolha **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="edbe0-116">Choose **Start**.</span></span>  
1.  <span data-ttu-id="edbe0-117">Dependendo do que você está tentando analisar, você pode recarregar a página, interagir com a página ou simplesmente deixar a página ser executada.</span><span class="sxs-lookup"><span data-stu-id="edbe0-117">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="edbe0-118">Selecione o botão **parar** quando terminar.</span><span class="sxs-lookup"><span data-stu-id="edbe0-118">Select the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="edbe0-119">Você também pode usar a [API de utilitários de console][DevtoolsConsoleUtilities] para gravar e agrupar perfis a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="edbe0-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="edbe0-120">Ver Perfil de amostragem</span><span class="sxs-lookup"><span data-stu-id="edbe0-120">View Sampling Profile</span></span>  

<span data-ttu-id="edbe0-121">Quando terminar a gravação, o DevTools automaticamente preenche o painel **memória** em **perfis de amostragem** com os dados da sua gravação.</span><span class="sxs-lookup"><span data-stu-id="edbe0-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="edbe0-122">O modo de exibição padrão é **Heavy \ (baixo para cima \)**.</span><span class="sxs-lookup"><span data-stu-id="edbe0-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="edbe0-123">Este modo de exibição permite que você veja quais funções tiveram mais impacto no desempenho e examine os caminhos de chamadas para essas funções.</span><span class="sxs-lookup"><span data-stu-id="edbe0-123">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="edbe0-124">Alterar a ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="edbe0-124">Change sort order</span></span>  

<span data-ttu-id="edbe0-125">Para alterar a ordem de classificação, selecione o menu suspenso ao lado do ícone **função de foco selecionado** \ ( ![ foco selecionado função ][ImageFocusIcon] \) e escolha uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="edbe0-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="edbe0-126">**Gráfico**.</span><span class="sxs-lookup"><span data-stu-id="edbe0-126">**Chart**.</span></span>  <span data-ttu-id="edbe0-127">Exibe um gráfico cronológico da gravação.</span><span class="sxs-lookup"><span data-stu-id="edbe0-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="edbe0-129">Gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="edbe0-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="edbe0-130">**Pesado \ (abaixo)**.</span><span class="sxs-lookup"><span data-stu-id="edbe0-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="edbe0-131">Lista as funções por meio do impacto no desempenho e permite que você examine os caminhos de chamadas para as funções.</span><span class="sxs-lookup"><span data-stu-id="edbe0-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="edbe0-132">Este é o modo de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="edbe0-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="edbe0-134">Gráfico pesado</span><span class="sxs-lookup"><span data-stu-id="edbe0-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="edbe0-135">**Árvore \ (acima para baixo \)**.</span><span class="sxs-lookup"><span data-stu-id="edbe0-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="edbe0-136">Mostra uma imagem geral da estrutura de chamadas, começando na parte superior da pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="edbe0-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="edbe0-138">Gráfico de árvore</span><span class="sxs-lookup"><span data-stu-id="edbe0-138">Tree chart</span></span>  
:::image-end:::  

### <span data-ttu-id="edbe0-139">Funções Exclude</span><span class="sxs-lookup"><span data-stu-id="edbe0-139">Exclude functions</span></span>  

<span data-ttu-id="edbe0-140">Para excluir uma função do seu perfil de amostragem, selecione-a e, em seguida, selecione o botão **excluir função selecionada** \ ( ![ excluir função selecionada ][ImageExcludeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="edbe0-140">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="edbe0-141">A função solicitante \ (pai \) da função excluída \ (filho \) é cobrada pela memória alocada atribuída à função excluída \ (filho \).</span><span class="sxs-lookup"><span data-stu-id="edbe0-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="edbe0-142">Selecione o botão **restaurar todas as funções** \ ( ![ restaurar todas as funções ][ImageRestoreIcon] \) para restaurar novamente todas as funções excluídas na gravação.</span><span class="sxs-lookup"><span data-stu-id="edbe0-142">Select the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="edbe0-143">Exibir Perfil de amostra como gráfico</span><span class="sxs-lookup"><span data-stu-id="edbe0-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="edbe0-144">O modo de exibição de gráfico fornece uma representação visual do perfil de amostragem ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="edbe0-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="edbe0-145">Depois de [gravar um perfil de amostragem](#record-a-sampling-profile), exiba a gravação como um gráfico de chama, [alterando a ordem de classificação](#change-sort-order) para **gráfico**.</span><span class="sxs-lookup"><span data-stu-id="edbe0-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="edbe0-147">Modo de exibição de gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="edbe0-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="edbe0-148">O gráfico de chama é dividido em duas partes.</span><span class="sxs-lookup"><span data-stu-id="edbe0-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="edbe0-149">dedo</span><span class="sxs-lookup"><span data-stu-id="edbe0-149">index</span></span> | <span data-ttu-id="edbe0-150">Parte</span><span class="sxs-lookup"><span data-stu-id="edbe0-150">Part</span></span> | <span data-ttu-id="edbe0-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="edbe0-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="edbe0-152">um</span><span class="sxs-lookup"><span data-stu-id="edbe0-152">1</span></span> | <span data-ttu-id="edbe0-153">Visão geral</span><span class="sxs-lookup"><span data-stu-id="edbe0-153">Overview</span></span> | <span data-ttu-id="edbe0-154">Uma exibição de olho de toda a gravação.</span><span class="sxs-lookup"><span data-stu-id="edbe0-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="edbe0-155">A altura das barras corresponde à profundidade da pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="edbe0-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="edbe0-156">Portanto, quanto mais alta a barra, mais profunda a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="edbe0-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="edbe0-157">2</span><span class="sxs-lookup"><span data-stu-id="edbe0-157">2</span></span> | <span data-ttu-id="edbe0-158">Pilha de chamadas</span><span class="sxs-lookup"><span data-stu-id="edbe0-158">Call Stacks</span></span> | <span data-ttu-id="edbe0-159">Esta é uma exibição detalhada das funções que foram chamadas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="edbe0-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="edbe0-160">O eixo horizontal é tempo e eixo vertical é a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="edbe0-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="edbe0-161">As pilhas são organizadas de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="edbe0-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="edbe0-162">Portanto, a função na parte superior acima dela e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="edbe0-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="edbe0-163">As funções são coloridas aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="edbe0-163">Functions are colored randomly.</span></span>  <span data-ttu-id="edbe0-164">Não há nenhuma correlação entre as cores usadas nos outros painéis.</span><span class="sxs-lookup"><span data-stu-id="edbe0-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="edbe0-165">No entanto, as funções são sempre coloridas iguais em chamadas para que você possa ver padrões em cada tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="edbe0-165">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="edbe0-167">Gráfico de chama com anotações</span><span class="sxs-lookup"><span data-stu-id="edbe0-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="edbe0-168">Uma pilha de chamadas alta não é necessariamente importante, apenas significa que muitas funções foram chamadas.</span><span class="sxs-lookup"><span data-stu-id="edbe0-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="edbe0-169">Mas uma barra larga significa que uma função demorou muito tempo para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="edbe0-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="edbe0-170">Estes são candidatos para otimização.</span><span class="sxs-lookup"><span data-stu-id="edbe0-170">These are candidates for optimization.</span></span>  

### <span data-ttu-id="edbe0-171">Ampliar partes específicas da gravação</span><span class="sxs-lookup"><span data-stu-id="edbe0-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="edbe0-172">Selecione, segure e arraste o mouse para a esquerda e para a direita na visão geral para ampliar partes específicas da pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="edbe0-172">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="edbe0-173">Depois de aplicar zoom, a pilha de chamadas exibirá automaticamente a parte da gravação selecionada.</span><span class="sxs-lookup"><span data-stu-id="edbe0-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="edbe0-175">Gráfico ampliado</span><span class="sxs-lookup"><span data-stu-id="edbe0-175">Chart zoomed</span></span>  
:::image-end:::  

### <span data-ttu-id="edbe0-176">Exibir detalhes da função</span><span class="sxs-lookup"><span data-stu-id="edbe0-176">View function details</span></span>  

<span data-ttu-id="edbe0-177">Selecione uma função para exibir a definição no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="edbe0-177">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="edbe0-178">Passe o mouse sobre uma função para exibir o nome e os dados de tempo.</span><span class="sxs-lookup"><span data-stu-id="edbe0-178">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="edbe0-179">As informações a seguir são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="edbe0-179">The following information is provided.</span></span>  

| <span data-ttu-id="edbe0-180">Minuciosa</span><span class="sxs-lookup"><span data-stu-id="edbe0-180">Detail</span></span> | <span data-ttu-id="edbe0-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="edbe0-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="edbe0-182">Name</span><span class="sxs-lookup"><span data-stu-id="edbe0-182">Name</span></span>** | <span data-ttu-id="edbe0-183">O nome da função.</span><span class="sxs-lookup"><span data-stu-id="edbe0-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="edbe0-184">Tamanho próprio</span><span class="sxs-lookup"><span data-stu-id="edbe0-184">Self size</span></span>** | <span data-ttu-id="edbe0-185">O tamanho da chamada atual da função, incluindo somente as instruções na função.</span><span class="sxs-lookup"><span data-stu-id="edbe0-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="edbe0-186">Tamanho total</span><span class="sxs-lookup"><span data-stu-id="edbe0-186">Total size</span></span>** | <span data-ttu-id="edbe0-187">O tamanho da invocação atual dessa função e de todas as funções chamadas.</span><span class="sxs-lookup"><span data-stu-id="edbe0-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="edbe0-188">URL</span><span class="sxs-lookup"><span data-stu-id="edbe0-188">URL</span></span>** | <span data-ttu-id="edbe0-189">O local da definição da função na forma de `base.js:261` onde `base.js` está o nome do arquivo em que a função está definida e `261` é o número da linha da definição.</span><span class="sxs-lookup"><span data-stu-id="edbe0-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="edbe0-191">Exibir detalhes de funções no gráfico</span><span class="sxs-lookup"><span data-stu-id="edbe0-191">View functions details in chart</span></span>  
:::image-end:::  

## <span data-ttu-id="edbe0-192">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="edbe0-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referência de API de utilitários de console | Documentos da Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Perfil-referência API de utilitários de console | Documentos da Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd-referência de API de utilitários de console | Documentos da Microsoft"  

> [!NOTE]
> <span data-ttu-id="edbe0-196">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="edbe0-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="edbe0-197">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \) e [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="edbe0-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="edbe0-199">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="edbe0-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
