---
description: Uma referência sobre todas as maneiras de gravar e analisar o desempenho no Microsoft Edge DevTools.
title: Referência de Análise de Desempenho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d5b6be92c1419ba880a94c62c3f586a740816622
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230758"
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

# <span data-ttu-id="c685d-104">Referência de análise de desempenho</span><span class="sxs-lookup"><span data-stu-id="c685d-104">Performance analysis reference</span></span>  

<span data-ttu-id="c685d-105">Esta página é uma referência abrangente do Microsoft Edge DevTools recursos relacionados à análise de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c685d-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="c685d-106">Navegue até [introdução ao analisando o desempenho do tempo de execução][DevtoolsEvaluatePerformanceGettingStarted] em um tutorial orientado sobre como analisar o desempenho de uma página usando o [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="c685d-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="c685d-107">Desempenho do registro</span><span class="sxs-lookup"><span data-stu-id="c685d-107">Record performance</span></span>  

### <span data-ttu-id="c685d-108">Desempenho do registro em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="c685d-108">Record runtime performance</span></span>  

<span data-ttu-id="c685d-109">Grave o desempenho do tempo de execução quando quiser analisar o desempenho de uma página enquanto ela estiver em execução, em oposição a carregá-la.</span><span class="sxs-lookup"><span data-stu-id="c685d-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="c685d-110">Vá para a página que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="c685d-110">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="c685d-111">Escolha a guia **desempenho** no devtools.</span><span class="sxs-lookup"><span data-stu-id="c685d-111">Choose the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="c685d-112">Escolha **registro** \ ( ![ ícone de registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c685d-112">Choose **Record** \(![Record icon][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="c685d-114">Record</span><span class="sxs-lookup"><span data-stu-id="c685d-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="c685d-115">Interagir com a página.</span><span class="sxs-lookup"><span data-stu-id="c685d-115">Interact with the page.</span></span>  <span data-ttu-id="c685d-116">O DevTools registra todas as atividades de página que ocorrem como resultado de suas interações.</span><span class="sxs-lookup"><span data-stu-id="c685d-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="c685d-117">Escolha **gravar** novamente ou escolha **parar** para parar a gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="c685d-118">Desempenho da carga de registros</span><span class="sxs-lookup"><span data-stu-id="c685d-118">Record load performance</span></span>  

<span data-ttu-id="c685d-119">Grave o desempenho de carga quando quiser analisar o desempenho de uma página enquanto ela estiver sendo carregada, em vez de executá-la.</span><span class="sxs-lookup"><span data-stu-id="c685d-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="c685d-120">Vá para a página que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="c685d-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="c685d-121">Abra o painel **desempenho** do devtools.</span><span class="sxs-lookup"><span data-stu-id="c685d-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="c685d-122">Escolha **atualizar página** \ ( ![ atualizar página ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c685d-122">Choose **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="c685d-123">O DevTools registra métricas de desempenho enquanto a página é atualizada e, em seguida, interrompe automaticamente a gravação em alguns segundos após o término da carga.</span><span class="sxs-lookup"><span data-stu-id="c685d-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Atualizar página" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="c685d-125">Atualizar página</span><span class="sxs-lookup"><span data-stu-id="c685d-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="c685d-126">O DevTools amplia automaticamente a parte da gravação na qual a maioria da atividade ocorreu.</span><span class="sxs-lookup"><span data-stu-id="c685d-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Uma gravação de carregamento de página" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="c685d-128">Uma gravação de carregamento de página</span><span class="sxs-lookup"><span data-stu-id="c685d-128">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="c685d-129">Capturar capturas de tela durante a gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="c685d-130">Ative a caixa de seleção **capturas de tela** para capturar uma captura de tela de cada quadro durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-130">Turn on the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="A caixa de seleção capturas de tela" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="c685d-132">A caixa de seleção **capturas de tela**</span><span class="sxs-lookup"><span data-stu-id="c685d-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-133">Navegue para [exibir uma captura de tela](#view-a-screenshot) para aprender a interagir com capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="c685d-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="c685d-134">Forçar coleta de lixo durante a gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="c685d-135">Enquanto você estiver gravando uma página, escolha **coletar lixo** \ ( ![ coletar ícone ][ImageCollectGarbageIcon] de lixo \) para forçar a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="c685d-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Coletar lixo" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="c685d-137">Coletar lixo</span><span class="sxs-lookup"><span data-stu-id="c685d-137">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="c685d-138">Mostrar configurações de gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-138">Show recording settings</span></span>  

<span data-ttu-id="c685d-139">Escolha **configurações de captura** \ ( ![ configurações de captura ][ImageCaptureSettingsIcon] \) para expor mais configurações relacionadas à maneira como o devtools captura gravações de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c685d-139">Choose **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="A seção Configurações de captura" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="c685d-141">A seção **configurações de captura**</span><span class="sxs-lookup"><span data-stu-id="c685d-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="c685d-142">Desabilitar exemplos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="c685d-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="c685d-143">Por padrão, a seção **principal** de uma gravação exibe pilhas de chamadas detalhadas de funções JavaScript que foram chamadas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="c685d-144">Para desativar essas pilhas de chamadas:</span><span class="sxs-lookup"><span data-stu-id="c685d-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="c685d-145">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="c685d-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c685d-146">Navegue até [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c685d-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c685d-147">Ative a caixa de seleção **desativar exemplos de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="c685d-147">Turn on the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="c685d-148">Faça uma gravação da página.</span><span class="sxs-lookup"><span data-stu-id="c685d-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="c685d-149">Os 2 valores a seguir mostram a diferença entre desabilitar e habilitar exemplos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c685d-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="c685d-150">A seção **principal** da gravação é muito mais curta quando a amostragem está desativada, pois ela omite todas as pilhas de chamadas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c685d-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Um exemplo de uma gravação quando exemplos de JS está desabilitado" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="c685d-152">Um exemplo de uma gravação quando exemplos de JS está desabilitado</span><span class="sxs-lookup"><span data-stu-id="c685d-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Um exemplo de uma gravação quando os exemplos de JS está ativado" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="c685d-154">Um exemplo de uma gravação quando os exemplos de JS está ativado</span><span class="sxs-lookup"><span data-stu-id="c685d-154">An example of a recording when JS samples are turned on</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="c685d-155">Acelerar a rede durante a gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-155">Throttle the network while recording</span></span>  

<span data-ttu-id="c685d-156">Para acelerar a rede durante a gravação:</span><span class="sxs-lookup"><span data-stu-id="c685d-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="c685d-157">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="c685d-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c685d-158">Navegue até [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c685d-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c685d-159">Defina a **rede** para o nível de limitação desejado.</span><span class="sxs-lookup"><span data-stu-id="c685d-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="c685d-160">Acelerar a CPU durante a gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="c685d-161">Para reduzir a CPU durante a gravação:</span><span class="sxs-lookup"><span data-stu-id="c685d-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="c685d-162">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="c685d-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c685d-163">Navegue até [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c685d-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c685d-164">Defina a **CPU** para o nível de limitação desejado.</span><span class="sxs-lookup"><span data-stu-id="c685d-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="c685d-165">A limitação é relativa às funcionalidades do seu computador.</span><span class="sxs-lookup"><span data-stu-id="c685d-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="c685d-166">Por exemplo, a opção **2x de lentidão** faz com que a CPU opere 2 vezes mais lenta do que o normal.</span><span class="sxs-lookup"><span data-stu-id="c685d-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="c685d-167">O DevTools não simula realmente as CPUs de dispositivos móveis, porque a arquitetura de dispositivos móveis é muito diferente da dos desktops e laptops.</span><span class="sxs-lookup"><span data-stu-id="c685d-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="c685d-168">Ativar a instrumentação avançada de pintura</span><span class="sxs-lookup"><span data-stu-id="c685d-168">Turn on advanced paint instrumentation</span></span>  

<span data-ttu-id="c685d-169">Para ver a instrumentação de pintura detalhada:</span><span class="sxs-lookup"><span data-stu-id="c685d-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="c685d-170">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="c685d-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c685d-171">Navegue até [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c685d-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c685d-172">Marque a caixa de seleção **habilitar instrumentação avançada de pintura (lento)** .</span><span class="sxs-lookup"><span data-stu-id="c685d-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="c685d-173">Para saber como interagir com as informações de pintura, navegue para [Exibir camadas](#view-layers-information) e [Exibir o criador de perfil de tinta](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="c685d-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="c685d-174">Salvar uma gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-174">Save a recording</span></span>  

<span data-ttu-id="c685d-175">Para salvar uma gravação, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **salvar perfil**.</span><span class="sxs-lookup"><span data-stu-id="c685d-175">To save a recording, open the contextual menu \(right-click\), and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Salvar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="c685d-177">Salvar perfil</span><span class="sxs-lookup"><span data-stu-id="c685d-177">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="c685d-178">Carregar uma gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-178">Load a recording</span></span>  

<span data-ttu-id="c685d-179">Para carregar uma gravação, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **carregar perfil**.</span><span class="sxs-lookup"><span data-stu-id="c685d-179">To load a recording, open the contextual menu \(right-click\), and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Carregar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="c685d-181">Carregar perfil</span><span class="sxs-lookup"><span data-stu-id="c685d-181">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="c685d-182">Limpar a gravação anterior</span><span class="sxs-lookup"><span data-stu-id="c685d-182">Clear the previous recording</span></span>  

<span data-ttu-id="c685d-183">Depois de fazer uma gravação, pressione **limpar gravação** \ ( ![ limpar ícone ][ImageClearRecordingIcon] de gravação \) para limpar a gravação no painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="c685d-183">After making a recording, press **Clear recording** \(![Clear recording icon][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Limpar gravação" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="c685d-185">Limpar gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-185">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="c685d-186">Analisar uma gravação de desempenho</span><span class="sxs-lookup"><span data-stu-id="c685d-186">Analyze a performance recording</span></span>  

<span data-ttu-id="c685d-187">Depois de [registrar o desempenho do tempo de execução](#record-runtime-performance) ou o [desempenho da carga de registro](#record-load-performance), o painel **desempenho** fornece muitos dados para analisar o desempenho do que acabou de acontecer.</span><span class="sxs-lookup"><span data-stu-id="c685d-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="c685d-188">Selecionar uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-188">Select a portion of a recording</span></span>  

<span data-ttu-id="c685d-189">Arraste o mouse para a esquerda ou para a direita na **visão geral** para selecionar uma parte de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="c685d-190">A **visão geral** é a seção que contém os gráficos de **FPS**, **CPU**e **net** .</span><span class="sxs-lookup"><span data-stu-id="c685d-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Arraste o mouse pela visão geral para aplicar zoom" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="c685d-192">Arraste o mouse pela **visão geral** para aplicar zoom</span><span class="sxs-lookup"><span data-stu-id="c685d-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-193">Para selecionar uma parte usando o teclado:</span><span class="sxs-lookup"><span data-stu-id="c685d-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="c685d-194">Escolha o plano de fundo da seção **principal** ou de qualquer uma das seções ao lado dela, como **interações**, **rede**ou **GPU**.</span><span class="sxs-lookup"><span data-stu-id="c685d-194">Choose the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="c685d-195">Este fluxo de trabalho de teclado funciona apenas quando uma dessas seções está em foco.</span><span class="sxs-lookup"><span data-stu-id="c685d-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="c685d-196">Use as `W` teclas,, `A` `S` , `D` para ampliar, mover para a esquerda, reduzir e mover para a direita, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c685d-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="c685d-197">Para selecionar uma parte usando um trackpad, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="c685d-197">To select a portion using a trackpad, complete the following actions.</span></span>  

1.  <span data-ttu-id="c685d-198">Passe o mouse sobre a seção **visão geral** ou a seção **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="c685d-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="c685d-199">A seção **visão geral** é a área que contém os gráficos de **FPS**, **CPU**e **net** .</span><span class="sxs-lookup"><span data-stu-id="c685d-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="c685d-200">A seção **detalhes** é a área que contém a seção **principal** , a seção **interações** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c685d-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="c685d-201">Usando dois dedos, passe o dedo para baixo para reduzir, deslize o dedo para a esquerda para mover para a esquerda, passe o dedo para baixo para ampliar e passe o dedo para a direita para mover para a direita.</span><span class="sxs-lookup"><span data-stu-id="c685d-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="c685d-202">Para rolar um gráfico de chama longa na seção **principal** ou em qualquer um dos vizinhos, escolha e segure enquanto arrasta para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="c685d-202">To scroll a long flame chart in the **Main** section or any of the neighbors, choose and hold while dragging up and down.</span></span>  <span data-ttu-id="c685d-203">Arraste para a esquerda e para a direita para mover qual parte da gravação está selecionada.</span><span class="sxs-lookup"><span data-stu-id="c685d-203">Drag left and right to move what portion of the recording is chosen.</span></span>  

### <span data-ttu-id="c685d-204">Atividades de pesquisa</span><span class="sxs-lookup"><span data-stu-id="c685d-204">Search activities</span></span>  

<span data-ttu-id="c685d-205">Selecione `Control` + `F` \ (Windows, Linux \) ou `Command` + `F` \ (MacOS \) para abrir a caixa de pesquisa na parte inferior do painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="c685d-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="A caixa de pesquisa" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="c685d-207">A caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="c685d-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-208">Para navegar entre atividades que correspondam à sua consulta:</span><span class="sxs-lookup"><span data-stu-id="c685d-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="c685d-209">Use os botões **Previous** ( ![ Previous ][ImagePreviousIcon] ) e **Next** \ ( ![ próximo ][ImageNextIcon] \) anteriores.</span><span class="sxs-lookup"><span data-stu-id="c685d-209">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="c685d-210">Selecione `Shift` + `Enter` para selecionar o anterior ou `Enter` para selecionar o próximo.</span><span class="sxs-lookup"><span data-stu-id="c685d-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="c685d-211">Para modificar as configurações de consulta:</span><span class="sxs-lookup"><span data-stu-id="c685d-211">To modify query settings:</span></span>  

*   <span data-ttu-id="c685d-212">Pressione diferenciando **maiúsculas** de minúsculas \ (diferencia ![ maiúsculas de minúsculas ][ImageSearchCaseIcon] \) para fazer com que a consulta seja sensível</span><span class="sxs-lookup"><span data-stu-id="c685d-212">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="c685d-213">Pressione **Regex** \ ( ![ Regex ][ImageSearchRegexIcon] \) para usar uma expressão regular em sua consulta.</span><span class="sxs-lookup"><span data-stu-id="c685d-213">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="c685d-214">Para ocultar a caixa de pesquisa, clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="c685d-214">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="c685d-215">Exibir atividade de thread principal</span><span class="sxs-lookup"><span data-stu-id="c685d-215">View main thread activity</span></span>  

<span data-ttu-id="c685d-216">Use a seção **principal** para exibir atividades ocorridas no thread principal da página.</span><span class="sxs-lookup"><span data-stu-id="c685d-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="A seção principal" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="c685d-218">A seção **principal**</span><span class="sxs-lookup"><span data-stu-id="c685d-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-219">Escolha um evento para ver mais informações sobre ele na guia **Resumo** .  DevTools descreve o evento selecionado.</span><span class="sxs-lookup"><span data-stu-id="c685d-219">Choose an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Mais informações sobre a função anônimo na guia Resumo" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="c685d-221">Mais informações sobre a `anonymous` função na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="c685d-221">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-222">DevTools representa a atividade de thread principal com um gráfico de chama.</span><span class="sxs-lookup"><span data-stu-id="c685d-222">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="c685d-223">O eixo x representa a gravação ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="c685d-223">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="c685d-224">O eixo y representa a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="c685d-224">The y-axis represents the call stack.</span></span>  <span data-ttu-id="c685d-225">Os eventos na parte superior causam os eventos abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="c685d-225">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Um gráfico de chama" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="c685d-227">Um gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="c685d-227">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-228">Na figura anterior, um `click` evento causou uma `Function Call` entrada na `activitytabs.js` linha 53.</span><span class="sxs-lookup"><span data-stu-id="c685d-228">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="c685d-229">Abaixo `Function Call` , examine se uma função anônima foi executada.</span><span class="sxs-lookup"><span data-stu-id="c685d-229">Below `Function Call`, review that an anonymous function was run.</span></span>  <span data-ttu-id="c685d-230">A função anônima solicitada `a` , que solicitou `wait` , que solicitou `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="c685d-230">The anonymous function requested `a`, which requested `wait`, which requested `Minor GC`.</span></span>  

<span data-ttu-id="c685d-231">DevTools atribui as cores aleatórias de scripts.</span><span class="sxs-lookup"><span data-stu-id="c685d-231">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="c685d-232">Na figura anterior, as solicitações de função de um script são verde claro em cores.</span><span class="sxs-lookup"><span data-stu-id="c685d-232">In the previous figure, function requests from one script are colored light green.</span></span>  <span data-ttu-id="c685d-233">As solicitações de outro script são coloridas bege.</span><span class="sxs-lookup"><span data-stu-id="c685d-233">Requests from another script are colored beige.</span></span>  <span data-ttu-id="c685d-234">O amarelo mais escuro representa a atividade de script e o evento roxo representa a atividade de renderização.</span><span class="sxs-lookup"><span data-stu-id="c685d-234">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="c685d-235">Esses eventos amarelos e roxos mais escuros são consistentes em todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="c685d-235">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="c685d-236">Navegue até [desabilitar exemplos de JavaScript](#disable-javascript-samples) se quiser ocultar o gráfico de chama detalhado de solicitações JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c685d-236">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript requests.</span></span>  <span data-ttu-id="c685d-237">Quando os exemplos de JS são desativados, somente os eventos de alto nível, como `Event: click` e `Function Call` da figura anterior, são `str` exibidos.</span><span class="sxs-lookup"><span data-stu-id="c685d-237">When JS samples are disabled, only high-level events such as `Event: click` and `Function Call` from the previous figure `str` displayed.</span></span>  

### <span data-ttu-id="c685d-238">Exibir atividades em uma tabela</span><span class="sxs-lookup"><span data-stu-id="c685d-238">View activities in a table</span></span>  

<span data-ttu-id="c685d-239">Depois de gravar uma página, você não precisa confiar exclusivamente na seção **principal** para analisar atividades.</span><span class="sxs-lookup"><span data-stu-id="c685d-239">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="c685d-240">O DevTools também fornece três exibições em tabelas para analisar atividades.</span><span class="sxs-lookup"><span data-stu-id="c685d-240">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="c685d-241">Cada modo de exibição oferece uma perspectiva diferente nas atividades:</span><span class="sxs-lookup"><span data-stu-id="c685d-241">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="c685d-242">Quando quiser exibir as atividades raiz que causam mais trabalho, use [a guia árvore de chamadas](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="c685d-242">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="c685d-243">Quando você quiser exibir as atividades nas quais o tempo foi gasto diretamente, use [a guia Bottom-Up](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="c685d-243">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="c685d-244">Quando quiser exibir as atividades na ordem em que elas ocorreram durante a gravação, use [a guia log de eventos](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="c685d-244">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="c685d-245">Todas as próximas três seções fazem referência à mesma demonstração.</span><span class="sxs-lookup"><span data-stu-id="c685d-245">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="c685d-246">Execute a demonstração você mesmo na [demonstração das guias de atividades][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="c685d-246">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="c685d-247">Atividades raiz</span><span class="sxs-lookup"><span data-stu-id="c685d-247">Root activities</span></span>  

<span data-ttu-id="c685d-248">Aqui está uma explicação do conceito de **atividades raiz** que é mencionado na guia de **árvore de chamadas** , na guia **de baixo para cima** e nas seções do log de **eventos** .</span><span class="sxs-lookup"><span data-stu-id="c685d-248">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="c685d-249">As atividades raiz são aquelas que fazem com que o navegador execute algum trabalho.</span><span class="sxs-lookup"><span data-stu-id="c685d-249">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="c685d-250">Por exemplo, quando você escolhe uma página da Web, o navegador executa uma `Event` atividade como a atividade raiz.</span><span class="sxs-lookup"><span data-stu-id="c685d-250">For example, when you choose a webpage, the browser runs an `Event` activity as the root activity.</span></span>  <span data-ttu-id="c685d-251">Isso `Event` pode fazer com que um manipulador seja executado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c685d-251">That `Event` may cause a handler to run, and so on.</span></span>  

<span data-ttu-id="c685d-252">No gráfico chama da seção **principal** , as atividades raiz estão na parte superior do gráfico.</span><span class="sxs-lookup"><span data-stu-id="c685d-252">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="c685d-253">Nas guias **árvore de chamadas** e **log de eventos** , as atividades raiz são os itens de nível superior.</span><span class="sxs-lookup"><span data-stu-id="c685d-253">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="c685d-254">Navegue até [a guia árvore de chamadas](#the-call-tree-tab) para obter um exemplo de atividades raiz.</span><span class="sxs-lookup"><span data-stu-id="c685d-254">Navigate to [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="c685d-255">A guia árvore de chamadas</span><span class="sxs-lookup"><span data-stu-id="c685d-255">The Call Tree tab</span></span>  

<span data-ttu-id="c685d-256">Use a guia **árvore de chamadas** para ver quais [atividades raiz](#root-activities) causam mais trabalho.</span><span class="sxs-lookup"><span data-stu-id="c685d-256">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="c685d-257">A guia **árvore de chamadas** exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-257">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c685d-258">Navegue para [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="c685d-258">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="A guia árvore de chamadas" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="c685d-260">A guia **árvore de chamadas**</span><span class="sxs-lookup"><span data-stu-id="c685d-260">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-261">Na figura anterior, o nível superior de itens na coluna **atividade** , como `Evaluate Script` e `Parse HTML` são atividades raiz.</span><span class="sxs-lookup"><span data-stu-id="c685d-261">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="c685d-262">O aninhamento representa a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="c685d-262">The nesting represents the call stack.</span></span>  <span data-ttu-id="c685d-263">Por exemplo, na figura anterior, `Parse HTML` que causou `Evaluate Script` o resultado `Compile Script` e `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="c685d-263">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="c685d-264">A **auto-tempo** representa o tempo gasto diretamente nessa atividade.</span><span class="sxs-lookup"><span data-stu-id="c685d-264">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="c685d-265">**Tempo total** representa o tempo gasto nessa atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="c685d-265">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="c685d-266">Escolha **período automático**, **tempo total**ou **atividade** para classificar a tabela por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="c685d-266">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="c685d-267">Use a caixa de texto **Filtrar** para filtrar eventos por nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="c685d-267">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="c685d-268">Por padrão, o menu **agrupamento** é definido como **sem agrupamento**.</span><span class="sxs-lookup"><span data-stu-id="c685d-268">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="c685d-269">Use o menu **agrupamento** para classificar a tabela de atividades com base em vários critérios.</span><span class="sxs-lookup"><span data-stu-id="c685d-269">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="c685d-270">Escolha **Mostrar pilha mais pesada** \ ( ![ Mostrar pilha mais pesada ][ImageShowHeaviestStackIcon] \) para revelar outra tabela à direita da tabela **atividade** .</span><span class="sxs-lookup"><span data-stu-id="c685d-270">Choose **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="c685d-271">Escolha uma atividade para preencher a tabela de **pilha mais pesada** .</span><span class="sxs-lookup"><span data-stu-id="c685d-271">Choose an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="c685d-272">A tabela de **pilha mais pesada** exibe quais filhos da atividade selecionada levaram o tempo mais longo para ser executado.</span><span class="sxs-lookup"><span data-stu-id="c685d-272">The **Heaviest Stack** table displays which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="c685d-273">A guia Bottom-Up</span><span class="sxs-lookup"><span data-stu-id="c685d-273">The Bottom-Up tab</span></span>  

<span data-ttu-id="c685d-274">Use a guia de **cima para baixo** para ver quais atividades resumiram diretamente na maior parte do tempo em agregação.</span><span class="sxs-lookup"><span data-stu-id="c685d-274">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="c685d-275">A guia de **cima para baixo** exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-275">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c685d-276">Navegue para [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="c685d-276">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="A guia Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="c685d-278">A guia **seta para baixo**</span><span class="sxs-lookup"><span data-stu-id="c685d-278">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-279">Na seção **principal** da seção chama o gráfico da figura anterior, navegue até que quase todo o tempo gastou em execução `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="c685d-279">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="c685d-280">A atividade superior na guia **inferior** do número anterior é `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="c685d-280">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="c685d-281">Navegar até a guia **abaixo** , a próxima atividade mais cara é `Layout` .</span><span class="sxs-lookup"><span data-stu-id="c685d-281">Navigate to the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="c685d-282">A coluna **auto-time** representa o tempo agregado gasto diretamente nessa atividade em todas as ocorrências.</span><span class="sxs-lookup"><span data-stu-id="c685d-282">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="c685d-283">A coluna **tempo total** representa o tempo agregado gasto na atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="c685d-283">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="c685d-284">A guia log de eventos</span><span class="sxs-lookup"><span data-stu-id="c685d-284">The Event Log tab</span></span>  

<span data-ttu-id="c685d-285">Use a guia **log de eventos** para exibir atividades na ordem em que elas ocorreram durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-285">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="c685d-286">A guia **log de eventos** exibe apenas as atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-286">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c685d-287">Navegue para [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="c685d-287">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="A guia log de eventos" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="c685d-289">A guia **log de eventos**</span><span class="sxs-lookup"><span data-stu-id="c685d-289">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-290">A coluna **hora de início** representa o ponto em que a atividade começou, em relação ao início da gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-290">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="c685d-291">Por exemplo, a hora de início do `175.7 ms` item selecionado na figura anterior significa que a atividade começou 175,7 MS após o início da gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-291">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="c685d-292">A coluna **auto-time** representa o tempo gasto diretamente nessa atividade.</span><span class="sxs-lookup"><span data-stu-id="c685d-292">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="c685d-293">As colunas de **tempo total** representam o tempo gasto diretamente nessa atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="c685d-293">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="c685d-294">Escolha **hora de início**, **hora automática**ou **tempo total** para classificar a tabela por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="c685d-294">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="c685d-295">Use a caixa de texto **Filtrar** para filtrar atividades por nome.</span><span class="sxs-lookup"><span data-stu-id="c685d-295">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="c685d-296">Use o menu **duração** para filtrar todas as atividades que levaram menos de 1 MS ou 15 ms.</span><span class="sxs-lookup"><span data-stu-id="c685d-296">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="c685d-297">Por padrão, o menu **duração** é definido como **todos**, o que significa que todas as atividades são mostradas.</span><span class="sxs-lookup"><span data-stu-id="c685d-297">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="c685d-298">Desative as caixas de seleção **carregar**, **script**, **renderização**ou **pintura** para filtrar todas as atividades dessas categorias.</span><span class="sxs-lookup"><span data-stu-id="c685d-298">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="c685d-299">Exibir atividade GPU</span><span class="sxs-lookup"><span data-stu-id="c685d-299">View GPU activity</span></span>  

<span data-ttu-id="c685d-300">Exiba a atividade GPU na seção **GPU** .</span><span class="sxs-lookup"><span data-stu-id="c685d-300">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="A seção GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="c685d-302">A seção **GPU**</span><span class="sxs-lookup"><span data-stu-id="c685d-302">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="c685d-303">Exibir atividade rasterizada</span><span class="sxs-lookup"><span data-stu-id="c685d-303">View raster activity</span></span>  

<span data-ttu-id="c685d-304">Exiba atividades rasterizadas na seção de **rasterização** .</span><span class="sxs-lookup"><span data-stu-id="c685d-304">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="A seção de rasterização" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="c685d-306">A seção de **rasterização**</span><span class="sxs-lookup"><span data-stu-id="c685d-306">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="c685d-307">Exibir interações</span><span class="sxs-lookup"><span data-stu-id="c685d-307">View interactions</span></span>  

<span data-ttu-id="c685d-308">Use a seção **interações** para localizar e analisar interações do usuário ocorridas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-308">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="A seção interações" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="c685d-310">A seção **interações**</span><span class="sxs-lookup"><span data-stu-id="c685d-310">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-311">Uma linha vermelha na parte inferior de uma interação representa o tempo gasto aguardando o thread principal.</span><span class="sxs-lookup"><span data-stu-id="c685d-311">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="c685d-312">Escolha uma interação para exibir mais informações sobre ela na guia **Resumo** .</span><span class="sxs-lookup"><span data-stu-id="c685d-312">Choose an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="c685d-313">Analisar quadros por segundo (FPS)</span><span class="sxs-lookup"><span data-stu-id="c685d-313">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="c685d-314">O DevTools oferece várias maneiras de analisar os quadros por segundo:</span><span class="sxs-lookup"><span data-stu-id="c685d-314">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="c685d-315">Use [o gráfico de FPS](#the-fps-chart) para obter uma visão geral de FPS na duração da gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-315">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="c685d-316">Use [a seção quadros](#the-frames-section) para ver quanto tempo um determinado quadro levou.</span><span class="sxs-lookup"><span data-stu-id="c685d-316">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="c685d-317">Use o **medidor de FPS** para uma estimativa em tempo real de FPS à medida que a página é executada.</span><span class="sxs-lookup"><span data-stu-id="c685d-317">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="c685d-318">Navegue para [exibir os quadros por segundo em tempo real com o medidor de FPS](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="c685d-318">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="c685d-319">O gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="c685d-319">The FPS chart</span></span>  

<span data-ttu-id="c685d-320">O gráfico de **FPS** fornece uma visão geral da taxa de quadros na duração de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-320">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="c685d-321">Em geral, quanto maior a barra verde, melhor a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="c685d-321">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="c685d-322">Uma barra vermelha acima do gráfico de **FPS** é um aviso informando que a taxa de quadros ficou tão baixa que provavelmente danificaram a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="c685d-322">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="O gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="c685d-324">O gráfico de **FPS**</span><span class="sxs-lookup"><span data-stu-id="c685d-324">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="c685d-325">A seção quadros</span><span class="sxs-lookup"><span data-stu-id="c685d-325">The Frames section</span></span>  

<span data-ttu-id="c685d-326">A seção **frames** informa exatamente quanto tempo um determinado quadro levou.</span><span class="sxs-lookup"><span data-stu-id="c685d-326">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="c685d-327">Passe o mouse sobre um quadro para exibir uma dica de ferramenta com mais informações sobre ele.</span><span class="sxs-lookup"><span data-stu-id="c685d-327">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Passe o mouse sobre um quadro" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="c685d-329">Passe o mouse sobre um quadro</span><span class="sxs-lookup"><span data-stu-id="c685d-329">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-330">Escolha um quadro para ver mais informações sobre o quadro na guia **Resumo** .  DevTools descreve o quadro selecionado em azul.</span><span class="sxs-lookup"><span data-stu-id="c685d-330">Choose a frame to view more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Exibir um quadro na guia Resumo" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="c685d-332">Exibir um quadro na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="c685d-332">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="c685d-333">Exibir solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="c685d-333">View network requests</span></span>  

<span data-ttu-id="c685d-334">Expanda a seção **rede** para ver a cascata de solicitações de rede ocorridas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-334">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="A seção rede" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="c685d-336">A seção **rede**</span><span class="sxs-lookup"><span data-stu-id="c685d-336">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-337">As solicitações são codificadas por cor da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c685d-337">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="c685d-338">HTML: azul</span><span class="sxs-lookup"><span data-stu-id="c685d-338">HTML: Blue</span></span>  
*   <span data-ttu-id="c685d-339">CSS: roxo</span><span class="sxs-lookup"><span data-stu-id="c685d-339">CSS: Purple</span></span>  
*   <span data-ttu-id="c685d-340">JS: amarelo</span><span class="sxs-lookup"><span data-stu-id="c685d-340">JS: Yellow</span></span>  
*   <span data-ttu-id="c685d-341">Imagens: verde</span><span class="sxs-lookup"><span data-stu-id="c685d-341">Images: Green</span></span>  
    
<span data-ttu-id="c685d-342">Escolha uma solicitação para exibir mais informações sobre ela na guia **Resumo** .  Por exemplo, na figura anterior, a guia **Resumo** está exibindo mais informações sobre a solicitação azul selecionada na seção **rede** .</span><span class="sxs-lookup"><span data-stu-id="c685d-342">Choose a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="c685d-343">Um quadrado mais escuro-azul no canto superior esquerdo de uma solicitação significa que é uma solicitação de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="c685d-343">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="c685d-344">Um quadrado azul mais claro significa prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="c685d-344">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="c685d-345">Por exemplo, na figura anterior, a solicitação azul selecionada é de prioridade mais alta, e a verde abaixo é de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="c685d-345">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="c685d-346">Na 1ª das figuras a seguir, a solicitação de `www.bing.com` é representada por uma linha à esquerda, uma barra no meio de uma parte escura e uma parte clara e uma linha à direita.</span><span class="sxs-lookup"><span data-stu-id="c685d-346">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="c685d-347">No segundo dos seguintes valores mostram a representação correspondente da mesma solicitação na guia **intervalo** do painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="c685d-347">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="c685d-348">Veja como essas duas representações são mapeadas umas com as outras:</span><span class="sxs-lookup"><span data-stu-id="c685d-348">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="c685d-349">A linha à esquerda está tudo no `Connection Start` grupo de eventos, inclusive.</span><span class="sxs-lookup"><span data-stu-id="c685d-349">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="c685d-350">Em outras palavras, ele é tudo antes `Request Sent` , exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c685d-350">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="c685d-351">A parte leve da barra é `Request Sent` e `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="c685d-351">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="c685d-352">A parte escura da barra está `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="c685d-352">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="c685d-353">A linha certa é essencialmente tempo gasto aguardando o thread principal.</span><span class="sxs-lookup"><span data-stu-id="c685d-353">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="c685d-354">Isso não é representado na guia **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="c685d-354">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="A representação de barra de linhas da solicitação www.bing.com" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="c685d-356">A representação de barra de linhas da `www.bing.com` solicitação</span><span class="sxs-lookup"><span data-stu-id="c685d-356">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="A ferramenta rede" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="c685d-358">A ferramenta **rede**</span><span class="sxs-lookup"><span data-stu-id="c685d-358">The **Network** tool</span></span>  
<span data-ttu-id="c685d-359">::: fim da imagem:::</span><span class="sxs-lookup"><span data-stu-id="c685d-359">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="c685d-360">Exibir métricas de memória</span><span class="sxs-lookup"><span data-stu-id="c685d-360">View memory metrics</span></span>  

<span data-ttu-id="c685d-361">Ative a caixa de seleção **memória** para exibir as métricas de memória da última gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-361">Turn on the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="A caixa de seleção memória" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="c685d-363">A caixa de seleção **memória**</span><span class="sxs-lookup"><span data-stu-id="c685d-363">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-364">O DevTools exibe um novo gráfico de **memória** , acima da guia **Resumo** .  Há também um novo gráfico abaixo do gráfico de **rede** , chamado **heap**.</span><span class="sxs-lookup"><span data-stu-id="c685d-364">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="c685d-365">O gráfico de **heap** fornece as mesmas informações que a linha de **heap do js** no gráfico de **memória** .</span><span class="sxs-lookup"><span data-stu-id="c685d-365">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métricas de memória" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="c685d-367">Métricas de memória</span><span class="sxs-lookup"><span data-stu-id="c685d-367">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-368">As linhas coloridas do gráfico são mapeadas para as caixas de seleção coloridas acima do gráfico.</span><span class="sxs-lookup"><span data-stu-id="c685d-368">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="c685d-369">Desative uma caixa de seleção para ocultar essa categoria do gráfico.</span><span class="sxs-lookup"><span data-stu-id="c685d-369">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="c685d-370">O gráfico só exibe a região da gravação selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="c685d-370">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="c685d-371">Por exemplo, na figura anterior, o gráfico de **memória** só mostra o uso da memória em torno da 400 MS Mark para a 1750 MS Mark.</span><span class="sxs-lookup"><span data-stu-id="c685d-371">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="c685d-372">Exibir a duração de uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-372">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="c685d-373">Ao analisar uma seção como **Network** ou **Main**, às vezes você precisa de uma estimativa mais precisa de tempo que determinados eventos levaram.</span><span class="sxs-lookup"><span data-stu-id="c685d-373">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="c685d-374">Segure `Shift` , escolha e segure e arraste para a esquerda ou para a direita para selecionar uma parte da gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-374">Hold `Shift`, choose and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="c685d-375">Na parte inferior da seleção, o DevTools mostra o tempo que a parte levou.</span><span class="sxs-lookup"><span data-stu-id="c685d-375">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Exibir a duração de uma parte de uma gravação" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="c685d-377">Exibir a duração de uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="c685d-377">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="c685d-378">Exibir uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="c685d-378">View a screenshot</span></span>  

<span data-ttu-id="c685d-379">Navegue até [capturar capturas de tela enquanto estiver gravando](#capture-screenshots-while-recording) para aprender a ativar capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="c685d-379">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to turn on screenshots.</span></span>  

<span data-ttu-id="c685d-380">Passe o mouse sobre a **visão geral** para ver uma captura de tela de como a página procurou durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="c685d-380">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="c685d-381">A **visão geral** é a seção que contém os gráficos **CPU**, **FPS**e **net** .</span><span class="sxs-lookup"><span data-stu-id="c685d-381">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Exibir uma captura de tela" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="c685d-383">Exibir uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="c685d-383">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-384">Você também pode exibir capturas de tela escolhendo um quadro na seção **quadros** .</span><span class="sxs-lookup"><span data-stu-id="c685d-384">You may also view screenshots by choosing a frame in the **Frames** section.</span></span>  <span data-ttu-id="c685d-385">O DevTools exibe uma versão pequena da captura de tela na guia **Resumo** .</span><span class="sxs-lookup"><span data-stu-id="c685d-385">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Exibir uma captura de tela na guia Resumo" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="c685d-387">Exibir uma captura de tela na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="c685d-387">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-388">Escolha a miniatura na guia **Resumo** para ampliar a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="c685d-388">Choose the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Aplicar zoom em uma captura de tela da guia Resumo" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="c685d-390">Aplicar zoom em uma captura de tela da guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="c685d-390">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="c685d-391">Exibir informações de camadas</span><span class="sxs-lookup"><span data-stu-id="c685d-391">View layers information</span></span>  

<span data-ttu-id="c685d-392">Para exibir as informações de camadas avançadas sobre um quadro:</span><span class="sxs-lookup"><span data-stu-id="c685d-392">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="c685d-393">[Ative a instrumentação avançada de pintura](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="c685d-393">[Turn on advanced paint instrumentation](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="c685d-394">Selecione um quadro na seção **quadros** .</span><span class="sxs-lookup"><span data-stu-id="c685d-394">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="c685d-395">DevTools exibe informações sobre as camadas na guia novas **camadas** , ao lado da guia **log de eventos** .</span><span class="sxs-lookup"><span data-stu-id="c685d-395">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="O painel camadas" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="c685d-397">O painel **camadas**</span><span class="sxs-lookup"><span data-stu-id="c685d-397">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c685d-398">Passe o mouse sobre uma camada para realçá-la no diagrama.</span><span class="sxs-lookup"><span data-stu-id="c685d-398">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Realçar uma camada" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="c685d-400">Realçar uma camada</span><span class="sxs-lookup"><span data-stu-id="c685d-400">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="c685d-401">Para mover o diagrama:</span><span class="sxs-lookup"><span data-stu-id="c685d-401">To move the diagram:</span></span>  

*   <span data-ttu-id="c685d-402">Escolha **modo panorâmico** \ ( ![ modo panorâmico ][ImagePanModeIcon] \) para mover-se pelos eixos X e Y.</span><span class="sxs-lookup"><span data-stu-id="c685d-402">Choose **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="c685d-403">Escolha **modo de giro** \ ( ![ modo ][ImageRotateModeIcon] de rotação \) para girar ao longo do eixo Z.</span><span class="sxs-lookup"><span data-stu-id="c685d-403">Choose **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="c685d-404">Escolha **Redefinir transformação** \ ( ![ Redefinir transformação ][ImageResetTransformIcon] \) para redefinir o diagrama para a posição original.</span><span class="sxs-lookup"><span data-stu-id="c685d-404">Choose **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="c685d-405">Exibir o gerador de perfil do Paint</span><span class="sxs-lookup"><span data-stu-id="c685d-405">View paint profiler</span></span>  

<span data-ttu-id="c685d-406">Para exibir informações avançadas sobre um evento de pintura:</span><span class="sxs-lookup"><span data-stu-id="c685d-406">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="c685d-407">[Ativar](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="c685d-407">[Turn on](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="c685d-408">Selecione um evento de **pintura** na seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="c685d-408">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="A guia perfil do Paint" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="c685d-410">A guia **perfil do Paint**</span><span class="sxs-lookup"><span data-stu-id="c685d-410">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c685d-411">Analisar o desempenho de renderização com a guia renderização</span><span class="sxs-lookup"><span data-stu-id="c685d-411">Analyze rendering performance with the Rendering tab</span></span>  

<span data-ttu-id="c685d-412">Use os recursos da guia **renderização** para ajudar a visualizar o desempenho de renderização da página.</span><span class="sxs-lookup"><span data-stu-id="c685d-412">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="c685d-413">Para abrir a guia **renderização** :</span><span class="sxs-lookup"><span data-stu-id="c685d-413">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="c685d-414">[Abrir o menu de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="c685d-414">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="c685d-415">Comece a digitar `Rendering` e selecione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="c685d-415">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="c685d-416">DevTools exibe a guia **renderização** na parte inferior da janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="c685d-416">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="A guia renderização" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="c685d-418">A guia **renderização**</span><span class="sxs-lookup"><span data-stu-id="c685d-418">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="c685d-419">Exibir quadros por segundo em tempo real com o medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="c685d-419">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="c685d-420">O **medidor de FPS** é uma sobreposição que aparece no canto superior direito do seu visor.</span><span class="sxs-lookup"><span data-stu-id="c685d-420">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="c685d-421">Ele fornece uma estimativa em tempo real de FPS à medida que a página é executada.</span><span class="sxs-lookup"><span data-stu-id="c685d-421">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="c685d-422">Para abrir o **medidor de FPS**:</span><span class="sxs-lookup"><span data-stu-id="c685d-422">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="c685d-423">Abrir a guia **renderização** .  Na [analisa o desempenho da renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c685d-423">Open the **Rendering** tab.  Na [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c685d-424">Ative a caixa de seleção **medidor de FPS** .</span><span class="sxs-lookup"><span data-stu-id="c685d-424">Turn on the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="O medidor de FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="c685d-426">O **medidor de FPS**</span><span class="sxs-lookup"><span data-stu-id="c685d-426">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="c685d-427">Exibir eventos de pintura em tempo real com o Paint piscando</span><span class="sxs-lookup"><span data-stu-id="c685d-427">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="c685d-428">Use o Paint para obter uma exibição em tempo real de todos os eventos de pintura na página.</span><span class="sxs-lookup"><span data-stu-id="c685d-428">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="c685d-429">Sempre que uma parte da página é pintada novamente, o DevTools descreve essa seção em verde.</span><span class="sxs-lookup"><span data-stu-id="c685d-429">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="c685d-430">Para ativar a intermitência de tinta, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="c685d-430">To turn on Paint Flashing, complete the following actions.</span></span>  

1.  <span data-ttu-id="c685d-431">Abrir a guia **renderização** .  Navegue para [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c685d-431">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c685d-432">Ativar a caixa de seleção **pintura em intermitência** .</span><span class="sxs-lookup"><span data-stu-id="c685d-432">Turn on the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Pintura em intermitência" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="c685d-434">Pintura em intermitência</span><span class="sxs-lookup"><span data-stu-id="c685d-434">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="c685d-435">Exibir uma sobreposição de camadas com bordas de camada</span><span class="sxs-lookup"><span data-stu-id="c685d-435">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="c685d-436">Use **bordas de camada** para exibir uma sobreposição de bordas de camada e blocos na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="c685d-436">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="c685d-437">Para ativar as bordas da camada, conclua as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="c685d-437">To turn on Layer Borders, complete the following actions,</span></span>  

1.  <span data-ttu-id="c685d-438">Abrir a guia **renderização** .  Navegue para [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c685d-438">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c685d-439">Ative a caixa de seleção **bordas de camada** .</span><span class="sxs-lookup"><span data-stu-id="c685d-439">Turn on the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordas de camada" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="c685d-441">Bordas de camada</span><span class="sxs-lookup"><span data-stu-id="c685d-441">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="c685d-442">Navegue até os comentários em [debug_colors. CC][ChromiumDebugColors] para obter uma explicação das codificações de cores.</span><span class="sxs-lookup"><span data-stu-id="c685d-442">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="c685d-443">Encontrar problemas de desempenho de rolagem em tempo real</span><span class="sxs-lookup"><span data-stu-id="c685d-443">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="c685d-444">Use problemas de desempenho de rolagem para identificar elementos da página que têm ouvintes de eventos relacionados a rolagem que podem danificar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="c685d-444">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="c685d-445">DevTools descreve os elementos que podem ser problemáticos em azul-petróleo.</span><span class="sxs-lookup"><span data-stu-id="c685d-445">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="c685d-446">Para ver os problemas de desempenho de rolagem, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="c685d-446">To view scroll performance issues, complete the following actions.</span></span> 

1.  <span data-ttu-id="c685d-447">Abrir a guia **renderização** .  Navegue para [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c685d-447">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c685d-448">Ative a caixa de seleção de **problemas de desempenho de rolagem** .</span><span class="sxs-lookup"><span data-stu-id="c685d-448">Turn on the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Os problemas de desempenho de rolagem indicam que os objetos restritos de não-camada podem danificar o desempenho de rolagem" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="c685d-450">Os **problemas de desempenho de rolagem** indicam que os objetos restritos de não-camada podem danificar o desempenho de rolagem</span><span class="sxs-lookup"><span data-stu-id="c685d-450">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c685d-451">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c685d-451">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Abrir o menu de comandos-executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Comece a analisar o desempenho do tempo de execução | Documentos da Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demonstração de guias de atividades | problema"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. CC-pesquisa de código"  

> [!NOTE]
> <span data-ttu-id="c685d-457">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c685d-457">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c685d-458">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c685d-458">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c685d-460">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c685d-460">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
