---
description: Identifique funções caras usando o painel Memória do Microsoft Edge DevTools.
title: Acelerar o tempo de execução do JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 682001ae8d265b342e5d6e0725f9f8ac4e298cf8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397598"
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

# <a name="speed-up-javascript-runtime"></a><span data-ttu-id="0115f-104">Acelerar o tempo de execução do JavaScript</span><span class="sxs-lookup"><span data-stu-id="0115f-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="0115f-105">Identifique funções caras usando o **painel Memória.**</span><span class="sxs-lookup"><span data-stu-id="0115f-105">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfis de Exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="0115f-107">Perfis de Exemplo</span><span class="sxs-lookup"><span data-stu-id="0115f-107">Sample Profiles</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="0115f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="0115f-108">Summary</span></span>  

*   <span data-ttu-id="0115f-109">Grave exatamente quais funções foram chamadas e quanta memória cada uma requer com a Amostragem de Alocação no **painel Memória.**</span><span class="sxs-lookup"><span data-stu-id="0115f-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="0115f-110">Visualize seus perfis como um gráfico de chama.</span><span class="sxs-lookup"><span data-stu-id="0115f-110">Visualize your profiles as a flame chart.</span></span>  
    
## <a name="record-a-sampling-profile"></a><span data-ttu-id="0115f-111">Registrar um perfil de amostragem</span><span class="sxs-lookup"><span data-stu-id="0115f-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="0115f-112">Se você observar jank em seu JavaScript, colete um Perfil de Amostragem.</span><span class="sxs-lookup"><span data-stu-id="0115f-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="0115f-113">Os Perfis de Amostragem mostram onde o tempo de execução é gasto em funções em sua página.</span><span class="sxs-lookup"><span data-stu-id="0115f-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="0115f-114">Navegue até **o painel Memória** do DevTools.</span><span class="sxs-lookup"><span data-stu-id="0115f-114">Navigate to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="0115f-115">Escolha o **botão de rádio de amostragem** de alocação.</span><span class="sxs-lookup"><span data-stu-id="0115f-115">Choose the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="0115f-116">Escolha **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="0115f-116">Choose **Start**.</span></span>  
1.  <span data-ttu-id="0115f-117">Dependendo do que você está tentando analisar, você pode atualizar a página, interagir com a página ou apenas deixar a página ser executado.</span><span class="sxs-lookup"><span data-stu-id="0115f-117">Depending on what you are trying to analyze, you may either refresh the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="0115f-118">Escolha o **botão Parar** quando terminar.</span><span class="sxs-lookup"><span data-stu-id="0115f-118">Choose the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="0115f-119">Você também pode usar a [API Utilitários de Console][DevtoolsConsoleUtilities] para gravar e agrupar perfis da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="0115f-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <a name="view-sampling-profile"></a><span data-ttu-id="0115f-120">Exibir Perfil de Amostragem</span><span class="sxs-lookup"><span data-stu-id="0115f-120">View Sampling Profile</span></span>  

<span data-ttu-id="0115f-121">Quando você terminar de gravar, o DevTools preencherá automaticamente o painel **Memória** em **PERFIS DE AMOSTRAGEM** com os dados da gravação.</span><span class="sxs-lookup"><span data-stu-id="0115f-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="0115f-122">O modo de exibição padrão **é Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="0115f-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="0115f-123">Essa exibição permite que você revise quais funções tiveram mais impacto no desempenho e examine o caminho de solicitação para cada função.</span><span class="sxs-lookup"><span data-stu-id="0115f-123">This view allows you to review which functions had the most impact on performance and examine the requesting path for each function.</span></span>  

### <a name="change-sort-order"></a><span data-ttu-id="0115f-124">Alterar ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="0115f-124">Change sort order</span></span>  

<span data-ttu-id="0115f-125">Para alterar a ordem de classificação, selecione o menu suspenso ao lado da função selecionada **de** foco \( ícone de função selecionada por foco \) e escolha uma ![ das opções a ][ImageFocusIcon] seguir.</span><span class="sxs-lookup"><span data-stu-id="0115f-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="0115f-126">**Gráfico**.</span><span class="sxs-lookup"><span data-stu-id="0115f-126">**Chart**.</span></span>  <span data-ttu-id="0115f-127">Exibe um gráfico cronologicamente da gravação.</span><span class="sxs-lookup"><span data-stu-id="0115f-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Gráfico de chama" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="0115f-129">Gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="0115f-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="0115f-130">**Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="0115f-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="0115f-131">Lista funções por impacto no desempenho e permite examinar os caminhos de chamada para as funções.</span><span class="sxs-lookup"><span data-stu-id="0115f-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="0115f-132">Esse é o modo de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="0115f-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Gráfico pesado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="0115f-134">Gráfico pesado</span><span class="sxs-lookup"><span data-stu-id="0115f-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="0115f-135">**Árvore \(Top Down\)**.</span><span class="sxs-lookup"><span data-stu-id="0115f-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="0115f-136">Mostra uma imagem geral da estrutura de chamada, começando na parte superior da pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="0115f-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Gráfico de árvore" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="0115f-138">Gráfico de árvore</span><span class="sxs-lookup"><span data-stu-id="0115f-138">Tree chart</span></span>  
:::image-end:::  

### <a name="exclude-functions"></a><span data-ttu-id="0115f-139">Excluir funções</span><span class="sxs-lookup"><span data-stu-id="0115f-139">Exclude functions</span></span>  

<span data-ttu-id="0115f-140">Para excluir uma função do seu Perfil de Amostragem, selecione-a e selecione o botão **excluir** função selecionada \( excluir função ![ selecionada ][ImageExcludeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0115f-140">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="0115f-141">A função solicitante \(parent\) da função excluída \(child\) é carregada com a memória alocada atribuída à função excluída \(child\).</span><span class="sxs-lookup"><span data-stu-id="0115f-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="0115f-142">Escolha o **botão restaurar todas as** funções \( restaure todas as funções \) para restaurar todas as funções excluídas de volta à ![ ][ImageRestoreIcon] gravação.</span><span class="sxs-lookup"><span data-stu-id="0115f-142">Choose the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <a name="view-sampling-profile-as-chart"></a><span data-ttu-id="0115f-143">Exibir Perfil de Amostragem como Gráfico</span><span class="sxs-lookup"><span data-stu-id="0115f-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="0115f-144">A exibição Gráfico fornece uma representação visual do Perfil de Amostragem ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="0115f-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="0115f-145">Depois de [gravar um Perfil de Amostragem,](#record-a-sampling-profile)veja a gravação como um gráfico de chama alterando a ordem de [classificação](#change-sort-order) para **Chart**.</span><span class="sxs-lookup"><span data-stu-id="0115f-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Exibição do gráfico de chama" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="0115f-147">Exibição do gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="0115f-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="0115f-148">O gráfico de chama é dividido em duas partes.</span><span class="sxs-lookup"><span data-stu-id="0115f-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="0115f-149">index</span><span class="sxs-lookup"><span data-stu-id="0115f-149">index</span></span> | <span data-ttu-id="0115f-150">Parte</span><span class="sxs-lookup"><span data-stu-id="0115f-150">Part</span></span> | <span data-ttu-id="0115f-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="0115f-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="0115f-152">1</span><span class="sxs-lookup"><span data-stu-id="0115f-152">1</span></span> | <span data-ttu-id="0115f-153">Visão geral</span><span class="sxs-lookup"><span data-stu-id="0115f-153">Overview</span></span> | <span data-ttu-id="0115f-154">Um ponto de vista de visão de visão de toda a gravação.</span><span class="sxs-lookup"><span data-stu-id="0115f-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="0115f-155">A altura das barras corresponde à profundidade da pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="0115f-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="0115f-156">Assim, quanto maior for a barra, mais profunda será a pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="0115f-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="0115f-157">2</span><span class="sxs-lookup"><span data-stu-id="0115f-157">2</span></span> | <span data-ttu-id="0115f-158">Pilha de chamada</span><span class="sxs-lookup"><span data-stu-id="0115f-158">Call Stacks</span></span> | <span data-ttu-id="0115f-159">Esta é uma visão detalhada das funções que foram chamadas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="0115f-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="0115f-160">O eixo horizontal é o tempo e o eixo vertical é a pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="0115f-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="0115f-161">As pilhas são organizadas de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="0115f-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="0115f-162">Assim, a função na parte superior chamou a uma abaixo dela e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0115f-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="0115f-163">As funções são coloridas aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="0115f-163">Functions are colored randomly.</span></span>  <span data-ttu-id="0115f-164">Não há correlação com as cores usadas nos outros painéis.</span><span class="sxs-lookup"><span data-stu-id="0115f-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="0115f-165">No entanto, as funções são sempre coloridas da mesma forma em invocações para que você possa observar padrões em cada tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0115f-165">However, functions are always colored the same across invocations so that you may observe patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Gráfico de chama anotado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="0115f-167">Gráfico de chama anotado</span><span class="sxs-lookup"><span data-stu-id="0115f-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="0115f-168">Uma pilha de chamadas altas não é necessariamente significativa, apenas significa que muitas funções foram chamadas.</span><span class="sxs-lookup"><span data-stu-id="0115f-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="0115f-169">Mas uma barra larga significa que uma função levou muito tempo para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="0115f-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="0115f-170">São candidatos à otimização.</span><span class="sxs-lookup"><span data-stu-id="0115f-170">These are candidates for optimization.</span></span>  

### <a name="zoom-in-on-specific-parts-of-recording"></a><span data-ttu-id="0115f-171">Ampliar partes específicas da gravação</span><span class="sxs-lookup"><span data-stu-id="0115f-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="0115f-172">Escolha, segure e arraste o mouse para a esquerda e para a direita na visão geral para ampliar partes específicas da pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="0115f-172">Choose, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="0115f-173">Depois de ampliar, a pilha de chamada exibe automaticamente a parte da gravação selecionada.</span><span class="sxs-lookup"><span data-stu-id="0115f-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Gráfico ampliado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="0115f-175">Gráfico ampliado</span><span class="sxs-lookup"><span data-stu-id="0115f-175">Chart zoomed</span></span>  
:::image-end:::  

### <a name="view-function-details"></a><span data-ttu-id="0115f-176">Exibir detalhes da função</span><span class="sxs-lookup"><span data-stu-id="0115f-176">View function details</span></span>  

<span data-ttu-id="0115f-177">Escolha uma função para exibir a definição no painel **Fontes.**</span><span class="sxs-lookup"><span data-stu-id="0115f-177">Choose a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="0115f-178">Passe o mouse em uma função para exibir o nome e os dados de tempo.</span><span class="sxs-lookup"><span data-stu-id="0115f-178">Hover on a function to display the name and timing data.</span></span>  <span data-ttu-id="0115f-179">As informações a seguir são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="0115f-179">The following information is provided.</span></span>  

| <span data-ttu-id="0115f-180">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0115f-180">Detail</span></span> | <span data-ttu-id="0115f-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="0115f-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="0115f-182">Name</span><span class="sxs-lookup"><span data-stu-id="0115f-182">Name</span></span>** | <span data-ttu-id="0115f-183">O nome da função.</span><span class="sxs-lookup"><span data-stu-id="0115f-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="0115f-184">Tamanho próprio</span><span class="sxs-lookup"><span data-stu-id="0115f-184">Self size</span></span>** | <span data-ttu-id="0115f-185">O tamanho da invocação atual da função, incluindo apenas as instruções na função.</span><span class="sxs-lookup"><span data-stu-id="0115f-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="0115f-186">Tamanho total</span><span class="sxs-lookup"><span data-stu-id="0115f-186">Total size</span></span>** | <span data-ttu-id="0115f-187">O tamanho da invocação atual dessa função e todas as funções que ela chamou.</span><span class="sxs-lookup"><span data-stu-id="0115f-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="0115f-188">URL</span><span class="sxs-lookup"><span data-stu-id="0115f-188">URL</span></span>** | <span data-ttu-id="0115f-189">O local da definição da função na forma de onde é o nome do arquivo em que a função é definida e é o número `base.js:261` `base.js` de linha da `261` definição.</span><span class="sxs-lookup"><span data-stu-id="0115f-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Exibir detalhes das funções no gráfico" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="0115f-191">Exibir detalhes das funções no gráfico</span><span class="sxs-lookup"><span data-stu-id="0115f-191">View functions details in chart</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0115f-192">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0115f-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referência da API de utilitários de console | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "profile - Referência da API de utilitários de console | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd - Referência da API de utilitários de console | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="0115f-196">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0115f-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0115f-197">A página original [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) é encontrada aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) e [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="0115f-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0115f-199">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0115f-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
