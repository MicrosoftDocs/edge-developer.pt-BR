---
description: Uma referência sobre todas as maneiras de registrar e analisar o desempenho no Microsoft Edge DevTools.
title: Referência de análise de desempenho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e7774dc0aab647b8cf2bf47699368fafe6c21d70
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439686"
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

# <a name="performance-analysis-reference"></a><span data-ttu-id="5d01b-104">Referência de análise de desempenho</span><span class="sxs-lookup"><span data-stu-id="5d01b-104">Performance analysis reference</span></span>  

<span data-ttu-id="5d01b-105">Esta página é uma referência abrangente dos recursos do Microsoft Edge DevTools relacionados à análise do desempenho.</span><span class="sxs-lookup"><span data-stu-id="5d01b-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="5d01b-106">Navegue [até Introdução à][DevtoolsEvaluatePerformanceGettingStarted] Análise do Desempenho do Tempo de Execução para obter um tutorial guiado sobre como analisar o desempenho de uma página usando o Microsoft Edge [DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="5d01b-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="record-performance"></a><span data-ttu-id="5d01b-107">Desempenho do registro</span><span class="sxs-lookup"><span data-stu-id="5d01b-107">Record performance</span></span>  

### <a name="record-runtime-performance"></a><span data-ttu-id="5d01b-108">Registrar o desempenho do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="5d01b-108">Record runtime performance</span></span>  

<span data-ttu-id="5d01b-109">Grave o desempenho do tempo de execução quando quiser analisar o desempenho de uma página enquanto ela está sendo executado, em vez de carregar.</span><span class="sxs-lookup"><span data-stu-id="5d01b-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="5d01b-110">Navegue até a página que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="5d01b-110">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="5d01b-111">Abra a **ferramenta Performance** no DevTools.</span><span class="sxs-lookup"><span data-stu-id="5d01b-111">Open the **Performance** tool in DevTools.</span></span>  
1.  <span data-ttu-id="5d01b-112">Escolha **Gravar** \( ![ Ícone de registro ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5d01b-112">Choose **Record** \(![Record icon](../media/record-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="5d01b-114">Record</span><span class="sxs-lookup"><span data-stu-id="5d01b-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="5d01b-115">Interaja com a página.</span><span class="sxs-lookup"><span data-stu-id="5d01b-115">Interact with the page.</span></span>  <span data-ttu-id="5d01b-116">O DevTools registra todas as atividades de página que ocorrem como resultado de suas interações.</span><span class="sxs-lookup"><span data-stu-id="5d01b-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="5d01b-117">Escolha **Gravar** novamente ou escolha **Parar** para interromper a gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <a name="record-load-performance"></a><span data-ttu-id="5d01b-118">Registrar o desempenho da carga</span><span class="sxs-lookup"><span data-stu-id="5d01b-118">Record load performance</span></span>  

<span data-ttu-id="5d01b-119">Registrar o desempenho da carga quando você quiser analisar o desempenho de uma página à medida que ela está sendo carregada, em vez de executar.</span><span class="sxs-lookup"><span data-stu-id="5d01b-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="5d01b-120">Navegue até a página que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="5d01b-120">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="5d01b-121">Abra o **painel Desempenho** do DevTools.</span><span class="sxs-lookup"><span data-stu-id="5d01b-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="5d01b-122">Escolha **Atualizar página** \( Atualizar Página ![ ](../media/refresh-page-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5d01b-122">Choose **Refresh page** \(![Refresh Page](../media/refresh-page-icon.msft.png)\).</span></span>  <span data-ttu-id="5d01b-123">O DevTools registra métricas de desempenho enquanto a página é atualizada e interrompe automaticamente a gravação alguns segundos depois que a carga é final.</span><span class="sxs-lookup"><span data-stu-id="5d01b-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Página Atualizar" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="5d01b-125">Página Atualizar</span><span class="sxs-lookup"><span data-stu-id="5d01b-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="5d01b-126">O DevTools amplia automaticamente a parte da gravação onde a maior parte da atividade ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5d01b-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Uma gravação de carga de página" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="5d01b-128">Uma gravação de carga de página</span><span class="sxs-lookup"><span data-stu-id="5d01b-128">A page-load recording</span></span>  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a><span data-ttu-id="5d01b-129">Capturar capturas de tela durante a gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="5d01b-130">Ativar a caixa **de seleção Capturas de** Tela para capturar uma captura de tela de cada quadro durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-130">Turn on the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="A caixa de seleção Capturas de Tela" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="5d01b-132">A **caixa de seleção Capturas de** Tela</span><span class="sxs-lookup"><span data-stu-id="5d01b-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-133">Navegue [até Exibir uma captura de](#view-a-screenshot) tela para saber como interagir com capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="5d01b-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <a name="force-garbage-collection-while-recording"></a><span data-ttu-id="5d01b-134">Forçar a coleta de lixo durante a gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="5d01b-135">Enquanto estiver gravando uma página, escolha **Coletar lixo** \( Coletar ícone de ![ lixo ](../media/collect-garbage-icon.msft.png) \) para forçar a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="5d01b-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon](../media/collect-garbage-icon.msft.png)\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Coletar lixo" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="5d01b-137">Coletar lixo</span><span class="sxs-lookup"><span data-stu-id="5d01b-137">Collect garbage</span></span>  
:::image-end:::  

### <a name="show-recording-settings"></a><span data-ttu-id="5d01b-138">Mostrar configurações de gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-138">Show recording settings</span></span>  

<span data-ttu-id="5d01b-139">Escolha **Configurações de captura** \( Configurações de captura \) para expor mais configurações relacionadas à forma como o ![ ](../media/capture-settings-icon.msft.png) DevTools captura gravações de desempenho.</span><span class="sxs-lookup"><span data-stu-id="5d01b-139">Choose **Capture settings** \(![Capture settings](../media/capture-settings-icon.msft.png)\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="A seção Configurações de Captura" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="5d01b-141">A **seção Configurações de** Captura</span><span class="sxs-lookup"><span data-stu-id="5d01b-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <a name="disable-javascript-samples"></a><span data-ttu-id="5d01b-142">Desabilitar amostras do JavaScript</span><span class="sxs-lookup"><span data-stu-id="5d01b-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="5d01b-143">Por padrão, a **seção Principal** de uma gravação exibe pilhas de chamadas detalhadas de funções JavaScript que foram chamadas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="5d01b-144">Para desabilitar essas pilhas de chamada:</span><span class="sxs-lookup"><span data-stu-id="5d01b-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="5d01b-145">Abra o menu **Configurações de** Captura.</span><span class="sxs-lookup"><span data-stu-id="5d01b-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="5d01b-146">Navegue [até Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="5d01b-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="5d01b-147">Ative a caixa de seleção **Desabilitar Exemplos de JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-147">Turn on the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="5d01b-148">Pegue uma gravação da página.</span><span class="sxs-lookup"><span data-stu-id="5d01b-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="5d01b-149">As 2 figuras a seguir exibem a diferença entre desabilitar e habilenciar amostras javaScript.</span><span class="sxs-lookup"><span data-stu-id="5d01b-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="5d01b-150">A **seção Principal** da gravação é muito mais curta quando a amostragem é desabilitada, pois omite todas as pilhas de chamada JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d01b-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Um exemplo de gravação quando amostras JS são desabilitadas" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="5d01b-152">Um exemplo de gravação quando amostras JS são desabilitadas</span><span class="sxs-lookup"><span data-stu-id="5d01b-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Um exemplo de uma gravação quando exemplos JS são ativas" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="5d01b-154">Um exemplo de uma gravação quando exemplos JS são ativas</span><span class="sxs-lookup"><span data-stu-id="5d01b-154">An example of a recording when JS samples are turned on</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a><span data-ttu-id="5d01b-155">Acelerar a rede durante a gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-155">Throttle the network while recording</span></span>  

<span data-ttu-id="5d01b-156">Para acelerar a rede durante a gravação:</span><span class="sxs-lookup"><span data-stu-id="5d01b-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="5d01b-157">Abra o menu **Configurações de** Captura.</span><span class="sxs-lookup"><span data-stu-id="5d01b-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="5d01b-158">Navegue [até Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="5d01b-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="5d01b-159">Definir **Rede** como o nível desejado de throttling.</span><span class="sxs-lookup"><span data-stu-id="5d01b-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <a name="throttle-the-cpu-while-recording"></a><span data-ttu-id="5d01b-160">Acelerar a CPU durante a gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="5d01b-161">Para acelerar a CPU durante a gravação:</span><span class="sxs-lookup"><span data-stu-id="5d01b-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="5d01b-162">Abra o menu **Configurações de** Captura.</span><span class="sxs-lookup"><span data-stu-id="5d01b-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="5d01b-163">Navegue [até Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="5d01b-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="5d01b-164">Desempate a **CPU** para o nível desejado de throttling.</span><span class="sxs-lookup"><span data-stu-id="5d01b-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="5d01b-165">A throttling é relativa aos recursos do computador.</span><span class="sxs-lookup"><span data-stu-id="5d01b-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="5d01b-166">Por exemplo, a opção **de lentidão 2x** faz sua CPU operar 2 vezes mais lenta do que o normal.</span><span class="sxs-lookup"><span data-stu-id="5d01b-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="5d01b-167">DevTools realmente não simulam as CPUs de dispositivos móveis, pois a arquitetura de dispositivos móveis é muito diferente da de desktops e laptops.</span><span class="sxs-lookup"><span data-stu-id="5d01b-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <a name="turn-on-advanced-paint-instrumentation"></a><span data-ttu-id="5d01b-168">Ativar instrumentação de tinta avançada</span><span class="sxs-lookup"><span data-stu-id="5d01b-168">Turn on advanced paint instrumentation</span></span>  

<span data-ttu-id="5d01b-169">Para exibir instrumentação de tinta detalhada:</span><span class="sxs-lookup"><span data-stu-id="5d01b-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="5d01b-170">Abra o menu **Configurações de** Captura.</span><span class="sxs-lookup"><span data-stu-id="5d01b-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="5d01b-171">Navegue [até Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="5d01b-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="5d01b-172">Marque a **caixa de seleção Habilitar instrumentação de tinta avançada (lenta).**</span><span class="sxs-lookup"><span data-stu-id="5d01b-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="5d01b-173">Para saber como interagir com as informações de tinta, navegue até [Exibir camadas](#view-layers-information) e [Exibir profiler de tinta.](#view-paint-profiler)</span><span class="sxs-lookup"><span data-stu-id="5d01b-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <a name="save-a-recording"></a><span data-ttu-id="5d01b-174">Salvar uma gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-174">Save a recording</span></span>  

<span data-ttu-id="5d01b-175">Para salvar uma gravação, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Salvar Perfil**.</span><span class="sxs-lookup"><span data-stu-id="5d01b-175">To save a recording, open the contextual menu \(right-click\), and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Salvar Perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="5d01b-177">Salvar Perfil</span><span class="sxs-lookup"><span data-stu-id="5d01b-177">Save Profile</span></span>**  
:::image-end:::  

## <a name="load-a-recording"></a><span data-ttu-id="5d01b-178">Carregar uma gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-178">Load a recording</span></span>  

<span data-ttu-id="5d01b-179">Para carregar uma gravação, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Load Profile**.</span><span class="sxs-lookup"><span data-stu-id="5d01b-179">To load a recording, open the contextual menu \(right-click\), and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Perfil de Carga" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="5d01b-181">Perfil de Carga</span><span class="sxs-lookup"><span data-stu-id="5d01b-181">Load Profile</span></span>**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a><span data-ttu-id="5d01b-182">Limpar a gravação anterior</span><span class="sxs-lookup"><span data-stu-id="5d01b-182">Clear the previous recording</span></span>  

<span data-ttu-id="5d01b-183">Depois de fazer uma gravação, escolha **Limpar gravação** \( Limpar o ícone de gravação \) para limpar essa gravação do ![ painel ](../media/clear-recording-icon.msft.png) **Desempenho.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-183">After making a recording, choose **Clear recording** \(![Clear recording icon](../media/clear-recording-icon.msft.png)\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Limpar gravação" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="5d01b-185">Limpar gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-185">Clear recording</span></span>**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a><span data-ttu-id="5d01b-186">Analisar uma gravação de desempenho</span><span class="sxs-lookup"><span data-stu-id="5d01b-186">Analyze a performance recording</span></span>  

<span data-ttu-id="5d01b-187">Depois de [gravar o desempenho do](#record-runtime-performance) \*\*\*\* tempo de execução ou o desempenho da carga do [registro,](#record-load-performance)o painel Desempenho fornece muitos dados para analisar o desempenho do que acabou de acontecer.</span><span class="sxs-lookup"><span data-stu-id="5d01b-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <a name="select-a-portion-of-a-recording"></a><span data-ttu-id="5d01b-188">Selecione uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-188">Select a portion of a recording</span></span>  

<span data-ttu-id="5d01b-189">Arraste o mouse para a esquerda ou para a direita na **Visão Geral** para selecionar uma parte de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="5d01b-190">A **Visão** Geral é a seção que contém os **gráficos FPS,** **CPU**e **NET.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Arraste o mouse pela Visão Geral para ampliar" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="5d01b-192">Arraste o mouse pela Visão **Geral para** ampliar</span><span class="sxs-lookup"><span data-stu-id="5d01b-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-193">Para selecionar uma parte usando o teclado:</span><span class="sxs-lookup"><span data-stu-id="5d01b-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="5d01b-194">Escolha o plano de fundo da seção **Principal** ou qualquer uma das seções ao lado dela, como **Interações,** **Rede**ou **GPU**.</span><span class="sxs-lookup"><span data-stu-id="5d01b-194">Choose the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="5d01b-195">Esse fluxo de trabalho de teclado só funciona quando uma dessas seções está em foco.</span><span class="sxs-lookup"><span data-stu-id="5d01b-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="5d01b-196">Use as teclas , , para ampliar, mover para a esquerda, diminuir o zoom e `W` mover para a `A` `S` `D` direita, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5d01b-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="5d01b-197">Para selecionar uma parte usando um trackpad, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="5d01b-197">To select a portion using a trackpad, complete the following actions.</span></span>  

1.  <span data-ttu-id="5d01b-198">Passe o mouse sobre a seção **Visão** Geral ou **a seção Detalhes.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="5d01b-199">A **seção Visão** geral é a área que contém os gráficos **FPS,** **CPU**e **NET.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="5d01b-200">A **seção Detalhes** é a área que contém a seção **Principal,** a **seção Interações** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5d01b-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="5d01b-201">Usando dois dedos, passe o dedo para cima para diminuir o zoom, passe o dedo para a esquerda para mover para a esquerda, deslize para baixo para ampliar e passe o dedo para a direita para mover para a direita.</span><span class="sxs-lookup"><span data-stu-id="5d01b-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="5d01b-202">Para rolar um gráfico de chama longo na **seção Principal** ou qualquer um dos vizinhos, escolha e segure enquanto arrasta para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="5d01b-202">To scroll a long flame chart in the **Main** section or any of the neighbors, choose and hold while dragging up and down.</span></span>  <span data-ttu-id="5d01b-203">Arraste para a esquerda e para a direita para mover qual parte da gravação foi escolhida.</span><span class="sxs-lookup"><span data-stu-id="5d01b-203">Drag left and right to move what portion of the recording is chosen.</span></span>  

### <a name="search-activities"></a><span data-ttu-id="5d01b-204">Atividades de pesquisa</span><span class="sxs-lookup"><span data-stu-id="5d01b-204">Search activities</span></span>  

<span data-ttu-id="5d01b-205">Selecione `Control` + `F` \(Windows, Linux\) ou `Command` + `F` \(macOS\) \*\*\*\* para abrir a caixa de pesquisa na parte inferior do painel Desempenho.</span><span class="sxs-lookup"><span data-stu-id="5d01b-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="A caixa de pesquisa" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="5d01b-207">A caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="5d01b-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-208">Para navegar em atividades que corresponderem à sua consulta:</span><span class="sxs-lookup"><span data-stu-id="5d01b-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="5d01b-209">Use os **botões Anterior** \( ![ Previous ](../media/previous-icon.msft.png) \) e **Next** \( ![ Next ](../media/next-icon.msft.png) \) .</span><span class="sxs-lookup"><span data-stu-id="5d01b-209">Use the **Previous** \(![Previous](../media/previous-icon.msft.png)\) and **Next** \(![Next](../media/next-icon.msft.png)\) buttons.</span></span>  
*   <span data-ttu-id="5d01b-210">Selecione `Shift` + `Enter` para selecionar o anterior ou `Enter` para selecionar o próximo.</span><span class="sxs-lookup"><span data-stu-id="5d01b-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="5d01b-211">Para modificar as configurações de consulta:</span><span class="sxs-lookup"><span data-stu-id="5d01b-211">To modify query settings:</span></span>  

*   <span data-ttu-id="5d01b-212">Escolha **Case sensitive** \( Case sensitive ![ ](../media/search-case-icon.msft.png) \) to make the query case sensitive.</span><span class="sxs-lookup"><span data-stu-id="5d01b-212">Choose **Case sensitive** \(![Case sensitive](../media/search-case-icon.msft.png)\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="5d01b-213">Escolha **Regex** \( ![ Regex ](../media/search-regex-icon.msft.png) \) para usar uma expressão regular em sua consulta.</span><span class="sxs-lookup"><span data-stu-id="5d01b-213">Choose **Regex** \(![Regex](../media/search-regex-icon.msft.png)\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="5d01b-214">Para ocultar a caixa de pesquisa, escolha **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="5d01b-214">To hide the search box, choose **Cancel**.</span></span>  

### <a name="view-main-thread-activity"></a><span data-ttu-id="5d01b-215">Exibir atividade de thread principal</span><span class="sxs-lookup"><span data-stu-id="5d01b-215">View main thread activity</span></span>  

<span data-ttu-id="5d01b-216">Use a **seção Principal** para exibir a atividade que ocorreu no thread principal da página.</span><span class="sxs-lookup"><span data-stu-id="5d01b-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="A seção Principal" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="5d01b-218">A **seção** Principal</span><span class="sxs-lookup"><span data-stu-id="5d01b-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-219">Escolha um evento para exibir mais informações sobre ele no painel **Resumo.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-219">Choose an event to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="5d01b-220">DevTools descreve o evento selecionado.</span><span class="sxs-lookup"><span data-stu-id="5d01b-220">DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Mais informações sobre a função anônima no painel Resumo" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="5d01b-222">Mais informações sobre a `anonymous` função no painel **Resumo**</span><span class="sxs-lookup"><span data-stu-id="5d01b-222">More information about the `anonymous` function in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-223">DevTools representa a atividade de thread principal com um gráfico de chama.</span><span class="sxs-lookup"><span data-stu-id="5d01b-223">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="5d01b-224">O eixo x representa a gravação ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="5d01b-224">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="5d01b-225">O eixo y representa a pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="5d01b-225">The y-axis represents the call stack.</span></span>  <span data-ttu-id="5d01b-226">Os eventos na parte superior causam os eventos abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="5d01b-226">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Um gráfico de chama" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="5d01b-228">Um gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="5d01b-228">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-229">Na figura anterior, um `click` evento causou um in na linha `Function Call` `activitytabs.js` 53.</span><span class="sxs-lookup"><span data-stu-id="5d01b-229">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="5d01b-230">Abaixo `Function Call` , revise se uma função anônima foi executado.</span><span class="sxs-lookup"><span data-stu-id="5d01b-230">Below `Function Call`, review that an anonymous function was run.</span></span>  <span data-ttu-id="5d01b-231">A função anônima solicitada `a` , que solicitou , que solicitou `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="5d01b-231">The anonymous function requested `a`, which requested `wait`, which requested `Minor GC`.</span></span>  

<span data-ttu-id="5d01b-232">O DevTools atribui cores aleatórias a scripts.</span><span class="sxs-lookup"><span data-stu-id="5d01b-232">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="5d01b-233">Na figura anterior, as solicitações de função de um script são coloridas em verde claro.</span><span class="sxs-lookup"><span data-stu-id="5d01b-233">In the previous figure, function requests from one script are colored light green.</span></span>  <span data-ttu-id="5d01b-234">As solicitações de outro script são bege coloridas.</span><span class="sxs-lookup"><span data-stu-id="5d01b-234">Requests from another script are colored beige.</span></span>  <span data-ttu-id="5d01b-235">O amarelo mais escuro representa a atividade de script e o evento roxo representa a atividade de renderização.</span><span class="sxs-lookup"><span data-stu-id="5d01b-235">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="5d01b-236">Esses eventos amarelos e roxos mais escuros são consistentes em todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="5d01b-236">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="5d01b-237">Navegue [até Desabilitar amostras do JavaScript](#disable-javascript-samples) se quiser ocultar o gráfico de chama detalhado das solicitações JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d01b-237">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript requests.</span></span>  <span data-ttu-id="5d01b-238">Quando exemplos JS são desabilitados, somente eventos de alto nível, como `Event: choose` e da figura anterior `Function Call` `str` exibida.</span><span class="sxs-lookup"><span data-stu-id="5d01b-238">When JS samples are disabled, only high-level events such as `Event: choose` and `Function Call` from the previous figure `str` displayed.</span></span>  

### <a name="view-activities-in-a-table"></a><span data-ttu-id="5d01b-239">Exibir atividades em uma tabela</span><span class="sxs-lookup"><span data-stu-id="5d01b-239">View activities in a table</span></span>  

<span data-ttu-id="5d01b-240">Depois de gravar uma página, você não precisa depender apenas da **seção Principal** para analisar atividades.</span><span class="sxs-lookup"><span data-stu-id="5d01b-240">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="5d01b-241">O DevTools também fornece três exibições tabular para analisar atividades.</span><span class="sxs-lookup"><span data-stu-id="5d01b-241">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="5d01b-242">Cada modo de exibição oferece uma perspectiva diferente sobre as atividades:</span><span class="sxs-lookup"><span data-stu-id="5d01b-242">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="5d01b-243">Quando quiser exibir as atividades raiz que causam mais trabalho, use o painel [Árvore de](#the-call-tree-panel) Chamada.</span><span class="sxs-lookup"><span data-stu-id="5d01b-243">When you want to view the root activities that cause the most work, use the [Call Tree](#the-call-tree-panel) panel.</span></span>  
*   <span data-ttu-id="5d01b-244">Quando você quiser exibir as atividades em que a maior parte do tempo foi gasto diretamente, use o [painel Bottom-Up.](#the-bottom-up-panel)</span><span class="sxs-lookup"><span data-stu-id="5d01b-244">When you want to view the activities where the most time was directly spent, use the [Bottom-Up](#the-bottom-up-panel) panel.</span></span>  
*   <span data-ttu-id="5d01b-245">Quando quiser exibir as atividades na ordem em que ocorreram durante a gravação, use o painel [Log de](#the-event-log-panel) Eventos.</span><span class="sxs-lookup"><span data-stu-id="5d01b-245">When you want to view the activities in the order in which they occurred during the recording, use the [Event Log](#the-event-log-panel) panel.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="5d01b-246">As próximas três seções referem-se à mesma demonstração.</span><span class="sxs-lookup"><span data-stu-id="5d01b-246">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="5d01b-247">Execute a demonstração por conta própria [na Demonstração de Guias de Atividade][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="5d01b-247">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <a name="root-activities"></a><span data-ttu-id="5d01b-248">Atividades raiz</span><span class="sxs-lookup"><span data-stu-id="5d01b-248">Root activities</span></span>  

<span data-ttu-id="5d01b-249">Aqui está uma explicação do **conceito** de \*\*\*\* atividades raiz mencionado no painel Árvore de Chamada, painel **Bottom-Up** e Painel **de Log de** Eventos.</span><span class="sxs-lookup"><span data-stu-id="5d01b-249">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** panel, **Bottom-Up** panel, and **Event Log** panel.</span></span>  

<span data-ttu-id="5d01b-250">As atividades raiz são aquelas que fazem com que o navegador faça algum trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d01b-250">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="5d01b-251">Por exemplo, quando você escolhe uma página da Web, o navegador executa uma `Event` atividade como a atividade raiz.</span><span class="sxs-lookup"><span data-stu-id="5d01b-251">For example, when you choose a webpage, the browser runs an `Event` activity as the root activity.</span></span>  <span data-ttu-id="5d01b-252">Isso `Event` pode fazer com que um manipulador seja executado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5d01b-252">That `Event` may cause a handler to run, and so on.</span></span>  

<span data-ttu-id="5d01b-253">No gráfico de chama da **seção Principal,** as atividades raiz estão na parte superior do gráfico.</span><span class="sxs-lookup"><span data-stu-id="5d01b-253">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="5d01b-254">Nos **painéis Árvore de Chamada** e **Log** de Eventos, as atividades raiz são os itens de nível superior.</span><span class="sxs-lookup"><span data-stu-id="5d01b-254">In the **Call Tree** and **Event Log** panels, root activities are the top-level items.</span></span>  

<span data-ttu-id="5d01b-255">Navegue até o [painel Árvore de](#the-call-tree-panel) Chamada para um exemplo de atividades raiz.</span><span class="sxs-lookup"><span data-stu-id="5d01b-255">Navigate to the [Call Tree](#the-call-tree-panel) panel for an example of root activities.</span></span>  

#### <a name="the-call-tree-panel"></a><span data-ttu-id="5d01b-256">O painel Árvore de Chamada</span><span class="sxs-lookup"><span data-stu-id="5d01b-256">The Call Tree panel</span></span>  

<span data-ttu-id="5d01b-257">Use o **painel Árvore de** Chamada para exibir quais atividades [raiz](#root-activities) causam mais trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d01b-257">Use the **Call Tree** panel to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="5d01b-258">O **painel Árvore de** Chamada exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-258">The **Call Tree** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="5d01b-259">Navegue [até Selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para saber como selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="5d01b-259">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="O painel Árvore de Chamada" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="5d01b-261">O **painel Árvore de** Chamada</span><span class="sxs-lookup"><span data-stu-id="5d01b-261">The **Call Tree** panel</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-262">Na figura anterior, o nível superior de itens na coluna **Atividade,** como `Evaluate Script` e são atividades `Parse HTML` raiz.</span><span class="sxs-lookup"><span data-stu-id="5d01b-262">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="5d01b-263">O aninhamento representa a pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="5d01b-263">The nesting represents the call stack.</span></span>  <span data-ttu-id="5d01b-264">Por exemplo, na figura anterior, `Parse HTML` que causou a causa e `Evaluate Script` `Compile Script` `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="5d01b-264">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="5d01b-265">**Self Time** representa o tempo gasto diretamente nessa atividade.</span><span class="sxs-lookup"><span data-stu-id="5d01b-265">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="5d01b-266">**Tempo Total** representa o tempo gasto nessa atividade ou qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="5d01b-266">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="5d01b-267">Escolha **Tempo Próprio**, Tempo **Total**ou **Atividade** para classificar a tabela por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="5d01b-267">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="5d01b-268">Use a **caixa de texto** Filtrar para filtrar eventos pelo nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="5d01b-268">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="5d01b-269">Por padrão, o menu **Agrupar** é definido como **Sem Agrupar**.</span><span class="sxs-lookup"><span data-stu-id="5d01b-269">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="5d01b-270">Use o menu **Agrupar** para classificar a tabela de atividades com base em vários critérios.</span><span class="sxs-lookup"><span data-stu-id="5d01b-270">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="5d01b-271">Escolha **Mostrar Pilha Mais Pesada** \( Mostrar Pilha Mais Pesada \) para revelar outra tabela à direita da tabela ![ ](../media/show-heaviest-stack-icon.msft.png) **Atividade.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-271">Choose **Show Heaviest Stack** \(![Show Heaviest Stack](../media/show-heaviest-stack-icon.msft.png)\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="5d01b-272">Escolha uma atividade para preencher a tabela **Pilha Mais** Pesada.</span><span class="sxs-lookup"><span data-stu-id="5d01b-272">Choose an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="5d01b-273">A **tabela Pilha mais pesada** exibe quais filhos da atividade selecionada levaram mais tempo para ser executado.</span><span class="sxs-lookup"><span data-stu-id="5d01b-273">The **Heaviest Stack** table displays which children of the selected activity took the longest time to run.</span></span>  

#### <a name="the-bottom-up-panel"></a><span data-ttu-id="5d01b-274">O Bottom-Up painel</span><span class="sxs-lookup"><span data-stu-id="5d01b-274">The Bottom-Up panel</span></span>  

<span data-ttu-id="5d01b-275">Use o **painel Bottom-Up** para exibir quais atividades assumiram a maior parte do tempo agregado.</span><span class="sxs-lookup"><span data-stu-id="5d01b-275">Use the **Bottom-Up** panel to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="5d01b-276">O **painel Bottom-Up** exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-276">The **Bottom-Up** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="5d01b-277">Navegue [até Selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para saber como selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="5d01b-277">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="O Bottom-Up painel" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="5d01b-279">O **painel Bottom-Up**</span><span class="sxs-lookup"><span data-stu-id="5d01b-279">The **Bottom-Up** panel</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-280">No gráfico **de** chama da seção Principal da figura anterior, navegue até que praticamente todo o tempo foi gasto em `Parse HTML` execução.</span><span class="sxs-lookup"><span data-stu-id="5d01b-280">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="5d01b-281">A atividade superior no **painel Bottom-Up** da figura anterior é `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="5d01b-281">The top activity in the **Bottom-Up** panel of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="5d01b-282">Navegue até **o painel Bottom-Up,** a próxima atividade mais cara é `Layout` .</span><span class="sxs-lookup"><span data-stu-id="5d01b-282">Navigate to the **Bottom-Up** panel, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="5d01b-283">A **coluna Tempo Próprio** representa o tempo agregado gasto diretamente nessa atividade, em todas as ocorrências.</span><span class="sxs-lookup"><span data-stu-id="5d01b-283">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="5d01b-284">A **coluna Tempo Total** representa o tempo agregado gasto nessa atividade ou qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="5d01b-284">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <a name="the-event-log-panel"></a><span data-ttu-id="5d01b-285">O painel Log de Eventos</span><span class="sxs-lookup"><span data-stu-id="5d01b-285">The Event Log panel</span></span>  

<span data-ttu-id="5d01b-286">Use o **painel Log** de Eventos para exibir atividades na ordem em que ocorreram durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-286">Use the **Event Log** panel to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="5d01b-287">O **painel Log** de Eventos exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-287">The **Event Log** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="5d01b-288">Navegue [até Selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para saber como selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="5d01b-288">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="O painel Log de Eventos" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="5d01b-290">O **painel Log de** Eventos</span><span class="sxs-lookup"><span data-stu-id="5d01b-290">The **Event Log** panel</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-291">A **coluna Hora de** Início representa o ponto no qual essa atividade foi iniciada, em relação ao início da gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-291">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="5d01b-292">Por exemplo, a hora de início do item selecionado na figura anterior significa que a atividade começou `175.7 ms` 175,7 ms depois que a gravação começou.</span><span class="sxs-lookup"><span data-stu-id="5d01b-292">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="5d01b-293">A **coluna Tempo Próprio** representa o tempo gasto diretamente nessa atividade.</span><span class="sxs-lookup"><span data-stu-id="5d01b-293">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="5d01b-294">As **colunas Tempo** Total representam o tempo gasto diretamente nessa atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="5d01b-294">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="5d01b-295">Escolha **Hora de Início,** **Hora De Auto**ou Tempo **Total** para classificar a tabela por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="5d01b-295">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="5d01b-296">Use a **caixa de texto** Filtrar para filtrar atividades pelo nome.</span><span class="sxs-lookup"><span data-stu-id="5d01b-296">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="5d01b-297">Use o menu **Duração** para filtrar todas as atividades que levaram menos de 1 ms ou 15 ms.</span><span class="sxs-lookup"><span data-stu-id="5d01b-297">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="5d01b-298">Por padrão, o menu **Duração** é definido como **Todos**, o que significa que todas as atividades são mostradas.</span><span class="sxs-lookup"><span data-stu-id="5d01b-298">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="5d01b-299">Desabilite **as caixas de**seleção \*\*\*\* Carregando, **Script,** **Renderização**ou Pintura para filtrar todas as atividades dessas categorias.</span><span class="sxs-lookup"><span data-stu-id="5d01b-299">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <a name="view-gpu-activity"></a><span data-ttu-id="5d01b-300">Exibir atividade de GPU</span><span class="sxs-lookup"><span data-stu-id="5d01b-300">View GPU activity</span></span>  

<span data-ttu-id="5d01b-301">Exibir atividade de GPU na **seção GPU.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-301">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="A seção GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="5d01b-303">A **seção GPU**</span><span class="sxs-lookup"><span data-stu-id="5d01b-303">The **GPU** section</span></span>  
:::image-end:::  

### <a name="view-raster-activity"></a><span data-ttu-id="5d01b-304">Exibir atividade de rasteridade</span><span class="sxs-lookup"><span data-stu-id="5d01b-304">View raster activity</span></span>  

<span data-ttu-id="5d01b-305">Exibir atividade de rasteridade na **seção Raster.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-305">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="A seção Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="5d01b-307">A **seção Raster**</span><span class="sxs-lookup"><span data-stu-id="5d01b-307">The **Raster** section</span></span>  
:::image-end:::  

### <a name="view-interactions"></a><span data-ttu-id="5d01b-308">Exibir interações</span><span class="sxs-lookup"><span data-stu-id="5d01b-308">View interactions</span></span>  

<span data-ttu-id="5d01b-309">Use a **seção Interações** para encontrar e analisar interações do usuário que aconteceram durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-309">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="A seção Interações" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="5d01b-311">A **seção Interações**</span><span class="sxs-lookup"><span data-stu-id="5d01b-311">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-312">Uma linha vermelha na parte inferior de uma interação representa o tempo gasto à espera do thread principal.</span><span class="sxs-lookup"><span data-stu-id="5d01b-312">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="5d01b-313">Escolha uma interação para exibir mais informações sobre ele no painel **Resumo.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-313">Choose an interaction to view more information about it in the **Summary** panel.</span></span>  

### <a name="analyze-frames-per-second-fps"></a><span data-ttu-id="5d01b-314">Analisar quadros por segundo (FPS)</span><span class="sxs-lookup"><span data-stu-id="5d01b-314">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="5d01b-315">O DevTools fornece várias maneiras de analisar quadros por segundo:</span><span class="sxs-lookup"><span data-stu-id="5d01b-315">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="5d01b-316">Use [o gráfico FPS para](#the-fps-chart) obter uma visão geral do FPS durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-316">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="5d01b-317">Use [a seção Quadros](#the-frames-section) para exibir quanto tempo um quadro específico levou.</span><span class="sxs-lookup"><span data-stu-id="5d01b-317">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="5d01b-318">Use o **medidor FPS** para uma estimativa em tempo real do FPS à medida que a página é executado.</span><span class="sxs-lookup"><span data-stu-id="5d01b-318">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="5d01b-319">Navegue [até Exibir quadros por segundo em tempo real com o medidor FPS](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="5d01b-319">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <a name="the-fps-chart"></a><span data-ttu-id="5d01b-320">O gráfico FPS</span><span class="sxs-lookup"><span data-stu-id="5d01b-320">The FPS chart</span></span>  

<span data-ttu-id="5d01b-321">O **gráfico FPS** fornece uma visão geral da taxa de quadros durante a duração de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-321">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="5d01b-322">Em geral, quanto maior for a barra verde, melhor será a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="5d01b-322">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="5d01b-323">Uma barra vermelha acima do gráfico **FPS** é um aviso de que a taxa de quadros caiu tão baixo que provavelmente prejudicava a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="5d01b-323">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="O gráfico FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="5d01b-325">O **gráfico FPS**</span><span class="sxs-lookup"><span data-stu-id="5d01b-325">The **FPS** chart</span></span>  
:::image-end:::  

#### <a name="the-frames-section"></a><span data-ttu-id="5d01b-326">A seção Quadros</span><span class="sxs-lookup"><span data-stu-id="5d01b-326">The Frames section</span></span>  

<span data-ttu-id="5d01b-327">A **seção Quadros** informa exatamente quanto tempo um quadro específico levou.</span><span class="sxs-lookup"><span data-stu-id="5d01b-327">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="5d01b-328">Passe o mouse em um quadro para exibir uma dica de ferramenta com mais informações sobre ele.</span><span class="sxs-lookup"><span data-stu-id="5d01b-328">Hover on a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Passar o mouse em um quadro" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="5d01b-330">Passar o mouse em um quadro</span><span class="sxs-lookup"><span data-stu-id="5d01b-330">Hover on a frame</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-331">Escolha um quadro para exibir mais informações sobre o quadro no painel **Resumo.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-331">Choose a frame to view more information about the frame in the **Summary** panel.</span></span>  <span data-ttu-id="5d01b-332">DevTools descreve o quadro selecionado em azul.</span><span class="sxs-lookup"><span data-stu-id="5d01b-332">DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Exibir um quadro no painel Resumo" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="5d01b-334">Exibir um quadro no painel **Resumo**</span><span class="sxs-lookup"><span data-stu-id="5d01b-334">View a frame in the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-network-requests"></a><span data-ttu-id="5d01b-335">Exibir solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="5d01b-335">View network requests</span></span>  

<span data-ttu-id="5d01b-336">Expanda **a seção Rede** para exibir uma cascata de solicitações de rede que ocorreram durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-336">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="A seção Rede" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="5d01b-338">A **seção Rede**</span><span class="sxs-lookup"><span data-stu-id="5d01b-338">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-339">As solicitações são codificadas por cores da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="5d01b-339">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="5d01b-340">HTML: Azul</span><span class="sxs-lookup"><span data-stu-id="5d01b-340">HTML: Blue</span></span>  
*   <span data-ttu-id="5d01b-341">CSS: Roxo</span><span class="sxs-lookup"><span data-stu-id="5d01b-341">CSS: Purple</span></span>  
*   <span data-ttu-id="5d01b-342">JS: Amarelo</span><span class="sxs-lookup"><span data-stu-id="5d01b-342">JS: Yellow</span></span>  
*   <span data-ttu-id="5d01b-343">Imagens: verde</span><span class="sxs-lookup"><span data-stu-id="5d01b-343">Images: Green</span></span>  
    
<span data-ttu-id="5d01b-344">Escolha uma solicitação para exibir mais informações sobre ela no painel **Resumo.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-344">Choose a request to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="5d01b-345">Por exemplo, na figura \*\*\*\* anterior, o painel Resumo está exibindo mais informações sobre a solicitação azul selecionada na **seção** Rede.</span><span class="sxs-lookup"><span data-stu-id="5d01b-345">For example, in the previous figure, the **Summary** panel is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="5d01b-346">Um quadrado azul mais escuro na parte superior esquerda de uma solicitação significa que é uma solicitação de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="5d01b-346">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="5d01b-347">Um quadrado azul claro significa prioridade inferior.</span><span class="sxs-lookup"><span data-stu-id="5d01b-347">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="5d01b-348">Por exemplo, na figura anterior, a solicitação azul selecionada é de prioridade mais alta e a verde abaixo dela é de prioridade inferior.</span><span class="sxs-lookup"><span data-stu-id="5d01b-348">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="5d01b-349">Na 1ª das figuras a seguir, a solicitação é representada por uma linha à esquerda, uma barra no meio com uma parte escura e uma parte clara e uma linha à `www.bing.com` direita.</span><span class="sxs-lookup"><span data-stu-id="5d01b-349">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="5d01b-350">No 2nd das figuras a seguir, mostra a representação correspondente da mesma solicitação no painel **Timing** da **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-350">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** panel of the **Network** tool.</span></span>  <span data-ttu-id="5d01b-351">Veja como essas duas representações são mapeados umas para as outras:</span><span class="sxs-lookup"><span data-stu-id="5d01b-351">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="5d01b-352">A linha esquerda é tudo até o `Connection Start` grupo de eventos, inclusive.</span><span class="sxs-lookup"><span data-stu-id="5d01b-352">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="5d01b-353">Em outras palavras, é tudo antes `Request Sent` , exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5d01b-353">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="5d01b-354">A parte light da barra é `Request Sent` e `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="5d01b-354">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="5d01b-355">A parte escura da barra é `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="5d01b-355">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="5d01b-356">A linha direita é essencialmente o tempo gasto aguardando o thread principal.</span><span class="sxs-lookup"><span data-stu-id="5d01b-356">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="5d01b-357">Isso não é representado no painel **Timing.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-357">This is not represented in the **Timing** panel.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="A representação de barra de linhas da solicitação www.bing.com de linha" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="5d01b-359">A representação de barra de linhas da `www.bing.com` solicitação</span><span class="sxs-lookup"><span data-stu-id="5d01b-359">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="A ferramenta Rede" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="5d01b-361">A **ferramenta Rede**</span><span class="sxs-lookup"><span data-stu-id="5d01b-361">The **Network** tool</span></span>  
<span data-ttu-id="5d01b-362">: ::image-end:::</span><span class="sxs-lookup"><span data-stu-id="5d01b-362">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a><span data-ttu-id="5d01b-363">Exibir métricas de memória</span><span class="sxs-lookup"><span data-stu-id="5d01b-363">View memory metrics</span></span>  

<span data-ttu-id="5d01b-364">Ativar a caixa **de seleção** Memória para exibir métricas de memória da última gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-364">Turn on the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="A caixa de seleção Memória" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="5d01b-366">A **caixa de seleção** Memória</span><span class="sxs-lookup"><span data-stu-id="5d01b-366">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-367">DevTools exibe um novo gráfico **de** memória, acima do **painel Resumo.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-367">DevTools displays a new **Memory** chart, above the **Summary** panel.</span></span>  <span data-ttu-id="5d01b-368">Também há um novo gráfico abaixo do gráfico **NET,** chamado **HEAP**.</span><span class="sxs-lookup"><span data-stu-id="5d01b-368">There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="5d01b-369">O **gráfico HEAP** fornece as mesmas informações que a linha heap **JS** no **gráfico memória.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-369">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métricas de memória" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="5d01b-371">Métricas de memória</span><span class="sxs-lookup"><span data-stu-id="5d01b-371">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-372">As linhas coloridas no mapa do gráfico para as caixas de seleção coloridas acima do gráfico.</span><span class="sxs-lookup"><span data-stu-id="5d01b-372">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="5d01b-373">Desabilite uma caixa de seleção para ocultar essa categoria do gráfico.</span><span class="sxs-lookup"><span data-stu-id="5d01b-373">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="5d01b-374">O gráfico exibe apenas a região da gravação que está selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="5d01b-374">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="5d01b-375">Por exemplo, na figura \*\*\*\* anterior, o gráfico Memória mostra apenas o uso da memória de cerca de 400 ms até a marca de 1750 ms.</span><span class="sxs-lookup"><span data-stu-id="5d01b-375">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a><span data-ttu-id="5d01b-376">Exibir a duração de uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-376">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="5d01b-377">Ao analisar uma seção como **Network** ou **Main**, às vezes você precisa de uma estimativa mais precisa de quanto tempo determinados eventos demoraram.</span><span class="sxs-lookup"><span data-stu-id="5d01b-377">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="5d01b-378">Segure , escolha e segure e arraste para a esquerda ou para a direita `Shift` para selecionar uma parte da gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-378">Hold `Shift`, choose and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="5d01b-379">Na parte inferior da sua seleção, o DevTools mostra quanto tempo essa parte demorou.</span><span class="sxs-lookup"><span data-stu-id="5d01b-379">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Exibir a duração de uma parte de uma gravação" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="5d01b-381">Exibir a duração de uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="5d01b-381">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <a name="view-a-screenshot"></a><span data-ttu-id="5d01b-382">Exibir uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="5d01b-382">View a screenshot</span></span>  

<span data-ttu-id="5d01b-383">Navegue [até Capturar capturas de tela durante a](#capture-screenshots-while-recording) gravação para saber como ativar capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="5d01b-383">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to turn on screenshots.</span></span>  

<span data-ttu-id="5d01b-384">Passe o mouse na **Visão** Geral para exibir uma captura de tela de como a página era durante o momento da gravação.</span><span class="sxs-lookup"><span data-stu-id="5d01b-384">Hover on the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="5d01b-385">A **Visão** Geral é a seção que contém os **gráficos CPU,** **FPS**e **NET.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-385">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Exibir uma captura de tela" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="5d01b-387">Exibir uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="5d01b-387">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-388">Você também pode exibir capturas de tela escolhendo um quadro na **seção Quadros.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-388">You may also view screenshots by choosing a frame in the **Frames** section.</span></span>  <span data-ttu-id="5d01b-389">DevTools exibe uma pequena versão da captura de tela no painel **Resumo.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-389">DevTools displays a small version of the screenshot in the **Summary** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Exibir uma captura de tela no painel Resumo" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="5d01b-391">Exibir uma captura de tela no painel **Resumo**</span><span class="sxs-lookup"><span data-stu-id="5d01b-391">View a screenshot in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-392">Escolha a miniatura no painel **Resumo** para ampliar a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="5d01b-392">Choose the thumbnail in the **Summary** panel to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Zoom em uma captura de tela do painel Resumo" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="5d01b-394">Zoom em uma captura de tela do painel **Resumo**</span><span class="sxs-lookup"><span data-stu-id="5d01b-394">Zoom into a screenshot from the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-layers-information"></a><span data-ttu-id="5d01b-395">Exibir informações sobre camadas</span><span class="sxs-lookup"><span data-stu-id="5d01b-395">View layers information</span></span>  

<span data-ttu-id="5d01b-396">Para exibir informações de camadas avançadas sobre um quadro:</span><span class="sxs-lookup"><span data-stu-id="5d01b-396">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="5d01b-397">[Ativar instrumentação de tinta avançada](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="5d01b-397">[Turn on advanced paint instrumentation](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="5d01b-398">Escolha um quadro na **seção Quadros.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-398">Choose a frame in the **Frames** section.</span></span>  <span data-ttu-id="5d01b-399">O DevTools exibe informações sobre as camadas no novo painel **Layers,** ao lado do painel **Log de** Eventos.</span><span class="sxs-lookup"><span data-stu-id="5d01b-399">DevTools displays information about the layers in the new **Layers** panel, next to the **Event Log** panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="O painel Layers" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="5d01b-401">O **painel Layers**</span><span class="sxs-lookup"><span data-stu-id="5d01b-401">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="5d01b-402">Passe o mouse em uma camada para realça-la no diagrama.</span><span class="sxs-lookup"><span data-stu-id="5d01b-402">Hover on a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Realça uma camada" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="5d01b-404">Realça uma camada</span><span class="sxs-lookup"><span data-stu-id="5d01b-404">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="5d01b-405">Para mover o diagrama:</span><span class="sxs-lookup"><span data-stu-id="5d01b-405">To move the diagram:</span></span>  

*   <span data-ttu-id="5d01b-406">Escolha **Modo Pan** \( Modo Pan ![ ](../media/pan-mode-icon.msft.png) \) para mover ao longo dos eixos X e Y.</span><span class="sxs-lookup"><span data-stu-id="5d01b-406">Choose **Pan Mode** \(![Pan Mode](../media/pan-mode-icon.msft.png)\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="5d01b-407">Escolha **Girar Modo** \( Modo de ![ Rotação ](../media/rotate-mode-icon.msft.png) \) para girar ao longo do eixo Z.</span><span class="sxs-lookup"><span data-stu-id="5d01b-407">Choose **Rotate Mode** \(![Rotate Mode](../media/rotate-mode-icon.msft.png)\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="5d01b-408">Escolha **Redefinir Transformar** \( ![ Redefinir Transformar ](../media/reset-transform-icon.msft.png) \) para redefinir o diagrama para a posição original.</span><span class="sxs-lookup"><span data-stu-id="5d01b-408">Choose **Reset Transform** \(![Reset Transform](../media/reset-transform-icon.msft.png)\) to reset the diagram to the original position.</span></span>  
    
### <a name="view-paint-profiler"></a><span data-ttu-id="5d01b-409">Exibir profiler de tinta</span><span class="sxs-lookup"><span data-stu-id="5d01b-409">View paint profiler</span></span>  

<span data-ttu-id="5d01b-410">Para exibir informações avançadas sobre um evento de tinta:</span><span class="sxs-lookup"><span data-stu-id="5d01b-410">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="5d01b-411">[Ativar](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="5d01b-411">[Turn on](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="5d01b-412">Escolha um **evento Paint** na **seção** Principal.</span><span class="sxs-lookup"><span data-stu-id="5d01b-412">Choose a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="O painel De perfil de tinta" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="5d01b-414">O **painel De perfil de tinta**</span><span class="sxs-lookup"><span data-stu-id="5d01b-414">The **Paint Profiler** panel</span></span>  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a><span data-ttu-id="5d01b-415">Analisar o desempenho da renderização com a ferramenta Rendering</span><span class="sxs-lookup"><span data-stu-id="5d01b-415">Analyze rendering performance with the Rendering tool</span></span>  

<span data-ttu-id="5d01b-416">Use os recursos do painel **Renderização** para ajudar a visualizar o desempenho de renderização da sua página.</span><span class="sxs-lookup"><span data-stu-id="5d01b-416">Use the features of the **Rendering** panel to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="5d01b-417">Para abrir a **ferramenta Rendering:**</span><span class="sxs-lookup"><span data-stu-id="5d01b-417">To open the **Rendering** tool:</span></span>  

1.  <span data-ttu-id="5d01b-418">[Abra o Menu de Comando][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="5d01b-418">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="5d01b-419">Comece a digitar `Rendering` e selecione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="5d01b-419">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="5d01b-420">O DevTools exibe a **ferramenta Rendering** na parte inferior da janela DevTools.</span><span class="sxs-lookup"><span data-stu-id="5d01b-420">DevTools displays the **Rendering** tool at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="A ferramenta Rendering" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="5d01b-422">A **ferramenta Rendering**</span><span class="sxs-lookup"><span data-stu-id="5d01b-422">The **Rendering** tool</span></span>  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a><span data-ttu-id="5d01b-423">Exibir quadros por segundo em tempo real com o medidor FPS</span><span class="sxs-lookup"><span data-stu-id="5d01b-423">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="5d01b-424">O **medidor FPS** é uma sobreposição que aparece no canto superior direito do seu viewport.</span><span class="sxs-lookup"><span data-stu-id="5d01b-424">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="5d01b-425">Ele fornece uma estimativa em tempo real do FPS à medida que a página é executado.</span><span class="sxs-lookup"><span data-stu-id="5d01b-425">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="5d01b-426">Para abrir o **medidor FPS**:</span><span class="sxs-lookup"><span data-stu-id="5d01b-426">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="5d01b-427">Abra a **ferramenta Rendering.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-427">Open the **Rendering** tool.</span></span>  <span data-ttu-id="5d01b-428">[Analisar o desempenho da renderização com a ferramenta Rendering.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="5d01b-428">[Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="5d01b-429">Ativar a caixa de **seleção Medidor FPS.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-429">Turn on the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="O medidor FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="5d01b-431">O **medidor FPS**</span><span class="sxs-lookup"><span data-stu-id="5d01b-431">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a><span data-ttu-id="5d01b-432">Exibir eventos de pintura em tempo real com Paint Flashing</span><span class="sxs-lookup"><span data-stu-id="5d01b-432">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="5d01b-433">Use Paint Flashing para obter uma exibição em tempo real de todos os eventos de tinta na página.</span><span class="sxs-lookup"><span data-stu-id="5d01b-433">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="5d01b-434">Sempre que uma parte da página é re-pintada, o DevTools descreve essa seção em verde.</span><span class="sxs-lookup"><span data-stu-id="5d01b-434">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="5d01b-435">Para ativar o Paint Flashing, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="5d01b-435">To turn on Paint Flashing, complete the following actions.</span></span>  

1.  <span data-ttu-id="5d01b-436">Abra a **ferramenta Rendering.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-436">Open the **Rendering** tool.</span></span>  <span data-ttu-id="5d01b-437">Navegue [até Analisar o desempenho da renderização com a ferramenta Rendering.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="5d01b-437">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="5d01b-438">A caixa de seleção **Pintar Piscando.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-438">Turn on the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint Flashing" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="5d01b-440">Paint Flashing</span><span class="sxs-lookup"><span data-stu-id="5d01b-440">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a><span data-ttu-id="5d01b-441">Exibir uma sobreposição de camadas com bordas de camada</span><span class="sxs-lookup"><span data-stu-id="5d01b-441">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="5d01b-442">Use **Bordas de Camada** para exibir uma sobreposição de bordas de camada e blocos na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="5d01b-442">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="5d01b-443">Para ativar Bordas de Camada, conclua as seguintes ações,</span><span class="sxs-lookup"><span data-stu-id="5d01b-443">To turn on Layer Borders, complete the following actions,</span></span>  

1.  <span data-ttu-id="5d01b-444">Abra a **ferramenta Rendering.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-444">Open the **Rendering** tool.</span></span>  <span data-ttu-id="5d01b-445">Navegue [até Analisar o desempenho da renderização com a ferramenta Rendering.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="5d01b-445">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="5d01b-446">Ativar a caixa **de seleção Bordas da** Camada.</span><span class="sxs-lookup"><span data-stu-id="5d01b-446">Turn on the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordas de camada" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="5d01b-448">Bordas de camada</span><span class="sxs-lookup"><span data-stu-id="5d01b-448">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="5d01b-449">Navegue até os comentários [em debug_colors.cc][ChromiumDebugColors] para saber mais sobre as codificações de cores.</span><span class="sxs-lookup"><span data-stu-id="5d01b-449">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <a name="find-scroll-performance-issues-in-realtime"></a><span data-ttu-id="5d01b-450">Encontrar problemas de desempenho de rolagem em tempo real</span><span class="sxs-lookup"><span data-stu-id="5d01b-450">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="5d01b-451">Use Scrolling Performance Issues para identificar elementos da página que têm ouvintes de eventos relacionados à rolagem que podem prejudicar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="5d01b-451">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="5d01b-452">DevTools descreve os elementos potencialmente problemáticos no teal.</span><span class="sxs-lookup"><span data-stu-id="5d01b-452">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="5d01b-453">Para exibir problemas de desempenho de rolagem, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="5d01b-453">To view scroll performance issues, complete the following actions.</span></span> 

1.  <span data-ttu-id="5d01b-454">Abra a **ferramenta Rendering.**</span><span class="sxs-lookup"><span data-stu-id="5d01b-454">Open the **Rendering** tool.</span></span>  <span data-ttu-id="5d01b-455">Navegue [até Analisar o desempenho da renderização com a ferramenta Rendering.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="5d01b-455">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="5d01b-456">A caixa de seleção **Problemas de Desempenho** de Rolagem.</span><span class="sxs-lookup"><span data-stu-id="5d01b-456">Turn on the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Scrolling Performance Issues indica que objetos não restritos a exibição de camada podem prejudicar o desempenho da rolagem" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="5d01b-458">**Scrolling Performance Issues** indica que objetos não restritos a exibição de camada podem prejudicar o desempenho da rolagem</span><span class="sxs-lookup"><span data-stu-id="5d01b-458">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5d01b-459">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5d01b-459">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Abrir o Menu de Comando - Executar comandos com o Menu de Comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Começar a analisar o desempenho do tempo de execução | Microsoft Docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demonstração de guias de atividade | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc - Pesquisa de código"  

> [!NOTE]
> <span data-ttu-id="5d01b-465">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d01b-465">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5d01b-466">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="5d01b-466">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5d01b-468">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d01b-468">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
