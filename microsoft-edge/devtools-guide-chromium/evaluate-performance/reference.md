---
title: Referência de Análise de Desempenho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 59e2f67d773102554b96749690fae51da09428a8
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983933"
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







# <span data-ttu-id="a75eb-103">Referência de análise de desempenho</span><span class="sxs-lookup"><span data-stu-id="a75eb-103">Performance analysis reference</span></span>   



<span data-ttu-id="a75eb-104">Esta página é uma referência abrangente do Microsoft Edge DevTools recursos relacionados à análise de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a75eb-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="a75eb-105">Consulte [introdução ao analisando o desempenho do tempo de execução][DevtoolsEvaluatePerformanceGettingStarted] para obter um tutorial guia sobre como analisar o desempenho de uma página usando [o Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="a75eb-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="a75eb-106">Desempenho do registro</span><span class="sxs-lookup"><span data-stu-id="a75eb-106">Record performance</span></span>   

### <span data-ttu-id="a75eb-107">Desempenho do registro em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="a75eb-107">Record runtime performance</span></span>   

<span data-ttu-id="a75eb-108">Grave o desempenho do tempo de execução quando quiser analisar o desempenho de uma página enquanto ela estiver em execução, em oposição a carregá-la.</span><span class="sxs-lookup"><span data-stu-id="a75eb-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="a75eb-109">Vá para a página que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="a75eb-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="a75eb-110">Clique na guia **desempenho** do devtools.</span><span class="sxs-lookup"><span data-stu-id="a75eb-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="a75eb-111">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a75eb-111">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="a75eb-113">Record</span><span class="sxs-lookup"><span data-stu-id="a75eb-113">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="a75eb-114">Interagir com a página.</span><span class="sxs-lookup"><span data-stu-id="a75eb-114">Interact with the page.</span></span>  <span data-ttu-id="a75eb-115">O DevTools registra todas as atividades de página que ocorrem como resultado de suas interações.</span><span class="sxs-lookup"><span data-stu-id="a75eb-115">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="a75eb-116">Clique em **gravar** novamente ou em **parar** para parar a gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-116">Click **Record** again or click **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="a75eb-117">Desempenho da carga de registros</span><span class="sxs-lookup"><span data-stu-id="a75eb-117">Record load performance</span></span>   

<span data-ttu-id="a75eb-118">Grave o desempenho de carga quando quiser analisar o desempenho de uma página enquanto ela estiver sendo carregada, em vez de executá-la.</span><span class="sxs-lookup"><span data-stu-id="a75eb-118">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="a75eb-119">Vá para a página que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="a75eb-119">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="a75eb-120">Abra o painel **desempenho** do devtools.</span><span class="sxs-lookup"><span data-stu-id="a75eb-120">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="a75eb-121">Clique em **atualizar página** \ ( ![ atualizar página ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a75eb-121">Click **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="a75eb-122">O DevTools registra métricas de desempenho enquanto a página é atualizada e, em seguida, interrompe automaticamente a gravação em alguns segundos após o término da carga.</span><span class="sxs-lookup"><span data-stu-id="a75eb-122">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Atualizar página" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="a75eb-124">Atualizar página</span><span class="sxs-lookup"><span data-stu-id="a75eb-124">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="a75eb-125">O DevTools amplia automaticamente a parte da gravação na qual a maioria da atividade ocorreu.</span><span class="sxs-lookup"><span data-stu-id="a75eb-125">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Uma gravação de carregamento de página" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="a75eb-127">Uma gravação de carregamento de página</span><span class="sxs-lookup"><span data-stu-id="a75eb-127">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="a75eb-128">Capturar capturas de tela durante a gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-128">Capture screenshots while recording</span></span>   

<span data-ttu-id="a75eb-129">Habilite a caixa de seleção **capturas** de tela para capturar uma captura de tela de cada quadro durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-129">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="A caixa de seleção capturas de tela" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="a75eb-131">A caixa de seleção **capturas de tela**</span><span class="sxs-lookup"><span data-stu-id="a75eb-131">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-132">Consulte [exibir uma captura de tela](#view-a-screenshot) para aprender a interagir com capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="a75eb-132">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="a75eb-133">Forçar coleta de lixo durante a gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-133">Force garbage collection while recording</span></span>   

<span data-ttu-id="a75eb-134">Enquanto você estiver gravando uma página, clique em **coletar lixo** \ ( ![ coletar lixo ][ImageCollectGarbageIcon] \) para forçar a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="a75eb-134">While you are recording a page, click **Collect garbage** \(![Collect garbage][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Coletar lixo" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="a75eb-136">Coletar lixo</span><span class="sxs-lookup"><span data-stu-id="a75eb-136">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="a75eb-137">Mostrar configurações de gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-137">Show recording settings</span></span>   

<span data-ttu-id="a75eb-138">Clique em **configurações de captura** \ ( ![ configurações ][ImageCaptureSettingsIcon] de captura \) para expor mais configurações relacionadas à maneira como o devtools captura gravações de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a75eb-138">Click **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="A seção Configurações de captura" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="a75eb-140">A seção **configurações de captura**</span><span class="sxs-lookup"><span data-stu-id="a75eb-140">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="a75eb-141">Desabilitar exemplos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="a75eb-141">Disable JavaScript samples</span></span>   

<span data-ttu-id="a75eb-142">Por padrão, a seção **principal** de uma gravação exibe pilhas de chamadas detalhadas de funções JavaScript que foram chamadas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-142">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="a75eb-143">Para desativar essas pilhas de chamadas:</span><span class="sxs-lookup"><span data-stu-id="a75eb-143">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="a75eb-144">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-144">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="a75eb-145">Consulte [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="a75eb-145">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="a75eb-146">Habilite a caixa de seleção **desativar exemplos de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-146">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="a75eb-147">Faça uma gravação da página.</span><span class="sxs-lookup"><span data-stu-id="a75eb-147">Take a recording of the page.</span></span>  
    
<span data-ttu-id="a75eb-148">Os 2 valores a seguir mostram a diferença entre desabilitar e habilitar exemplos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a75eb-148">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="a75eb-149">A seção **principal** da gravação é muito mais curta quando a amostragem está desativada, pois ela omite todas as pilhas de chamadas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a75eb-149">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Um exemplo de uma gravação quando exemplos de JS está desabilitado" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="a75eb-151">Um exemplo de uma gravação quando exemplos de JS está desabilitado</span><span class="sxs-lookup"><span data-stu-id="a75eb-151">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Um exemplo de uma gravação quando exemplos de JS está habilitado" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="a75eb-153">Um exemplo de uma gravação quando exemplos de JS está habilitado</span><span class="sxs-lookup"><span data-stu-id="a75eb-153">An example of a recording when JS samples are enabled</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="a75eb-154">Acelerar a rede durante a gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-154">Throttle the network while recording</span></span>   

<span data-ttu-id="a75eb-155">Para acelerar a rede durante a gravação:</span><span class="sxs-lookup"><span data-stu-id="a75eb-155">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="a75eb-156">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-156">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="a75eb-157">Consulte [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="a75eb-157">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="a75eb-158">Defina a **rede** para o nível de limitação desejado.</span><span class="sxs-lookup"><span data-stu-id="a75eb-158">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="a75eb-159">Acelerar a CPU durante a gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-159">Throttle the CPU while recording</span></span>   

<span data-ttu-id="a75eb-160">Para reduzir a CPU durante a gravação:</span><span class="sxs-lookup"><span data-stu-id="a75eb-160">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="a75eb-161">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-161">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="a75eb-162">Consulte [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="a75eb-162">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="a75eb-163">Defina a **CPU** para o nível de limitação desejado.</span><span class="sxs-lookup"><span data-stu-id="a75eb-163">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="a75eb-164">A limitação é relativa às funcionalidades do seu computador.</span><span class="sxs-lookup"><span data-stu-id="a75eb-164">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="a75eb-165">Por exemplo, a opção **2x de lentidão** faz com que a CPU opere 2 vezes mais lenta do que o normal.</span><span class="sxs-lookup"><span data-stu-id="a75eb-165">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="a75eb-166">O DevTools não simula realmente as CPUs de dispositivos móveis, porque a arquitetura de dispositivos móveis é muito diferente da dos desktops e laptops.</span><span class="sxs-lookup"><span data-stu-id="a75eb-166">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="a75eb-167">Habilitar a instrumentação avançada de pintura</span><span class="sxs-lookup"><span data-stu-id="a75eb-167">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="a75eb-168">Para ver a instrumentação de pintura detalhada:</span><span class="sxs-lookup"><span data-stu-id="a75eb-168">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="a75eb-169">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="a75eb-170">Consulte [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="a75eb-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="a75eb-171">Marque a caixa de seleção **habilitar instrumentação avançada de pintura (lento)** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-171">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="a75eb-172">Para saber como interagir com as informações de pintura, consulte [Exibir camadas](#view-layers-information) e [Exibir o criador de perfil de tinta](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="a75eb-172">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="a75eb-173">Salvar uma gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-173">Save a recording</span></span>   

<span data-ttu-id="a75eb-174">Para salvar uma gravação, clique com o botão direito do mouse e selecione **salvar perfil**.</span><span class="sxs-lookup"><span data-stu-id="a75eb-174">To save a recording, right-click and select **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Salvar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="a75eb-176">Salvar perfil</span><span class="sxs-lookup"><span data-stu-id="a75eb-176">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="a75eb-177">Carregar uma gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-177">Load a recording</span></span>   

<span data-ttu-id="a75eb-178">Para carregar uma gravação, clique com o botão direito do mouse e selecione **carregar perfil**.</span><span class="sxs-lookup"><span data-stu-id="a75eb-178">To load a recording, right-click and select **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Carregar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="a75eb-180">Carregar perfil</span><span class="sxs-lookup"><span data-stu-id="a75eb-180">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="a75eb-181">Limpar a gravação anterior</span><span class="sxs-lookup"><span data-stu-id="a75eb-181">Clear the previous recording</span></span>   

<span data-ttu-id="a75eb-182">Depois de fazer uma gravação, pressione **limpar gravação** \ ( ![ limpar gravação ][ImageClearRecordingIcon] \) para limpar a gravação no painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-182">After making a recording, press **Clear recording** \(![Clear recording][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Limpar gravação" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="a75eb-184">Limpar gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-184">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="a75eb-185">Analisar uma gravação de desempenho</span><span class="sxs-lookup"><span data-stu-id="a75eb-185">Analyze a performance recording</span></span>   

<span data-ttu-id="a75eb-186">Depois de [registrar o desempenho do tempo de execução](#record-runtime-performance) ou o [desempenho da carga de registro](#record-load-performance), o painel **desempenho** fornece muitos dados para analisar o desempenho do que acabou de acontecer.</span><span class="sxs-lookup"><span data-stu-id="a75eb-186">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="a75eb-187">Selecionar uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-187">Select a portion of a recording</span></span>   

<span data-ttu-id="a75eb-188">Arraste o mouse para a esquerda ou para a direita na **visão geral** para selecionar uma parte de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-188">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="a75eb-189">A **visão geral** é a seção que contém os gráficos de **FPS**, **CPU**e **net** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-189">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Arraste o mouse pela visão geral para aplicar zoom" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="a75eb-191">Arraste o mouse pela **visão geral** para aplicar zoom</span><span class="sxs-lookup"><span data-stu-id="a75eb-191">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-192">Para selecionar uma parte usando o teclado:</span><span class="sxs-lookup"><span data-stu-id="a75eb-192">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="a75eb-193">Clique no plano de fundo da seção **principal** ou de qualquer uma das seções ao lado dela, como **interações**, **rede**ou **GPU**.</span><span class="sxs-lookup"><span data-stu-id="a75eb-193">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="a75eb-194">Este fluxo de trabalho de teclado funciona apenas quando uma dessas seções está em foco.</span><span class="sxs-lookup"><span data-stu-id="a75eb-194">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="a75eb-195">Use as `W` teclas,, `A` `S` , `D` para ampliar, mover para a esquerda, reduzir e mover para a direita, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a75eb-195">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="a75eb-196">Para selecionar uma parte usando uma trackpad:</span><span class="sxs-lookup"><span data-stu-id="a75eb-196">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="a75eb-197">Passe o mouse sobre a seção **visão geral** ou a seção **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-197">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="a75eb-198">A seção **visão geral** é a área que contém os gráficos de **FPS**, **CPU**e **net** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-198">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="a75eb-199">A seção **detalhes** é a área que contém a seção **principal** , a seção **interações** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a75eb-199">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="a75eb-200">Usando dois dedos, passe o dedo para baixo para reduzir, deslize o dedo para a esquerda para mover para a esquerda, passe o dedo para baixo para ampliar e passe o dedo para a direita para mover para a direita.</span><span class="sxs-lookup"><span data-stu-id="a75eb-200">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="a75eb-201">Para rolar um gráfico de chama longa na seção **principal** ou em qualquer um dos vizinhos, clique e mantenha pressionado enquanto arrasta para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="a75eb-201">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="a75eb-202">Arraste para a esquerda e para a direita para mover qual parte da gravação está selecionada.</span><span class="sxs-lookup"><span data-stu-id="a75eb-202">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="a75eb-203">Atividades de pesquisa</span><span class="sxs-lookup"><span data-stu-id="a75eb-203">Search activities</span></span>   

<span data-ttu-id="a75eb-204">Pressione `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \) para abrir a caixa de pesquisa na parte inferior do painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-204">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="A caixa de pesquisa" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="a75eb-206">A caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="a75eb-206">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-207">Para navegar entre atividades que correspondam à sua consulta:</span><span class="sxs-lookup"><span data-stu-id="a75eb-207">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="a75eb-208">Use os botões **Previous** ( ![ Previous ][ImagePreviousIcon] ) e **Next** \ ( ![ próximo ][ImageNextIcon] \) anteriores.</span><span class="sxs-lookup"><span data-stu-id="a75eb-208">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="a75eb-209">Pressione `Shift` + `Enter` para selecionar o anterior ou `Enter` para selecionar o próximo.</span><span class="sxs-lookup"><span data-stu-id="a75eb-209">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="a75eb-210">Para modificar as configurações de consulta:</span><span class="sxs-lookup"><span data-stu-id="a75eb-210">To modify query settings:</span></span>  

*   <span data-ttu-id="a75eb-211">Pressione diferenciando **maiúsculas** de minúsculas \ (diferencia ![ maiúsculas de minúsculas ][ImageSearchCaseIcon] \) para fazer com que a consulta seja sensível</span><span class="sxs-lookup"><span data-stu-id="a75eb-211">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="a75eb-212">Pressione **Regex** \ ( ![ Regex ][ImageSearchRegexIcon] \) para usar uma expressão regular em sua consulta.</span><span class="sxs-lookup"><span data-stu-id="a75eb-212">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="a75eb-213">Para ocultar a caixa de pesquisa, clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="a75eb-213">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="a75eb-214">Exibir atividade de thread principal</span><span class="sxs-lookup"><span data-stu-id="a75eb-214">View main thread activity</span></span>   

<span data-ttu-id="a75eb-215">Use a seção **principal** para exibir atividades ocorridas no thread principal da página.</span><span class="sxs-lookup"><span data-stu-id="a75eb-215">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="A seção principal" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="a75eb-217">A seção **principal**</span><span class="sxs-lookup"><span data-stu-id="a75eb-217">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-218">Clique em um evento para ver mais informações sobre ele na guia **Resumo** .  DevTools descreve o evento selecionado.</span><span class="sxs-lookup"><span data-stu-id="a75eb-218">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Mais informações sobre a função anônimo na guia Resumo" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="a75eb-220">Mais informações sobre a `anonymous` função na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="a75eb-220">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-221">DevTools representa a atividade de thread principal com um gráfico de chama.</span><span class="sxs-lookup"><span data-stu-id="a75eb-221">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="a75eb-222">O eixo x representa a gravação ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="a75eb-222">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="a75eb-223">O eixo y representa a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="a75eb-223">The y-axis represents the call stack.</span></span>  <span data-ttu-id="a75eb-224">Os eventos na parte superior causam os eventos abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="a75eb-224">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Um gráfico de chama" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="a75eb-226">Um gráfico de chama</span><span class="sxs-lookup"><span data-stu-id="a75eb-226">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-227">Na figura anterior, um `click` evento causou uma `Function Call` entrada na `activitytabs.js` linha 53.</span><span class="sxs-lookup"><span data-stu-id="a75eb-227">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="a75eb-228">Abaixo `Function Call` , você verá que uma função anônima foi chamada.</span><span class="sxs-lookup"><span data-stu-id="a75eb-228">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="a75eb-229">A função anônima chamada `a` , que é chamada `wait` , que é chamada `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="a75eb-229">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="a75eb-230">DevTools atribui as cores aleatórias de scripts.</span><span class="sxs-lookup"><span data-stu-id="a75eb-230">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="a75eb-231">Na figura anterior, as chamadas de função de um script são verde claro em cores.</span><span class="sxs-lookup"><span data-stu-id="a75eb-231">In the previous figure, function calls from one script are colored light green.</span></span>  <span data-ttu-id="a75eb-232">As chamadas de outro script são coloridas bege.</span><span class="sxs-lookup"><span data-stu-id="a75eb-232">Calls from another script are colored beige.</span></span>  <span data-ttu-id="a75eb-233">O amarelo mais escuro representa a atividade de script e o evento roxo representa a atividade de renderização.</span><span class="sxs-lookup"><span data-stu-id="a75eb-233">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="a75eb-234">Esses eventos amarelos e roxos mais escuros são consistentes em todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="a75eb-234">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="a75eb-235">Confira [desabilitar exemplos de JavaScript](#disable-javascript-samples) se você quiser ocultar o gráfico de chama detalhado de chamadas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a75eb-235">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="a75eb-236">Quando os exemplos de JS estiverem desativados, você verá apenas eventos de alto nível, como `Event: click` e `Function Call` da figura anterior.</span><span class="sxs-lookup"><span data-stu-id="a75eb-236">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from the previous figure.</span></span>  

### <span data-ttu-id="a75eb-237">Exibir atividades em uma tabela</span><span class="sxs-lookup"><span data-stu-id="a75eb-237">View activities in a table</span></span>   

<span data-ttu-id="a75eb-238">Depois de gravar uma página, você não precisa confiar exclusivamente na seção **principal** para analisar atividades.</span><span class="sxs-lookup"><span data-stu-id="a75eb-238">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="a75eb-239">O DevTools também fornece três exibições em tabelas para analisar atividades.</span><span class="sxs-lookup"><span data-stu-id="a75eb-239">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="a75eb-240">Cada modo de exibição oferece uma perspectiva diferente nas atividades:</span><span class="sxs-lookup"><span data-stu-id="a75eb-240">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="a75eb-241">Quando quiser exibir as atividades raiz que causam mais trabalho, use [a guia árvore de chamadas](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="a75eb-241">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="a75eb-242">Quando você quiser exibir as atividades nas quais o tempo foi gasto diretamente, use [a guia de baixo para cima](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="a75eb-242">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="a75eb-243">Quando quiser exibir as atividades na ordem em que elas ocorreram durante a gravação, use [a guia log de eventos](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="a75eb-243">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="a75eb-244">Todas as próximas três seções fazem referência à mesma demonstração.</span><span class="sxs-lookup"><span data-stu-id="a75eb-244">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="a75eb-245">Execute a demonstração você mesmo na [demonstração das guias de atividades][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="a75eb-245">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="a75eb-246">Atividades raiz</span><span class="sxs-lookup"><span data-stu-id="a75eb-246">Root activities</span></span>   

<span data-ttu-id="a75eb-247">Aqui está uma explicação do conceito de **atividades raiz** que é mencionado na guia de **árvore de chamadas** , na guia **de baixo para cima** e nas seções do log de **eventos** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-247">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="a75eb-248">As atividades raiz são aquelas que fazem com que o navegador execute algum trabalho.</span><span class="sxs-lookup"><span data-stu-id="a75eb-248">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="a75eb-249">Por exemplo, quando você clica em uma página, o navegador dispara uma `Event` atividade como a atividade raiz.</span><span class="sxs-lookup"><span data-stu-id="a75eb-249">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="a75eb-250">Isso `Event` pode fazer com que um manipulador seja executado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a75eb-250">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="a75eb-251">No gráfico chama da seção **principal** , as atividades raiz estão na parte superior do gráfico.</span><span class="sxs-lookup"><span data-stu-id="a75eb-251">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="a75eb-252">Nas guias **árvore de chamadas** e **log de eventos** , as atividades raiz são os itens de nível superior.</span><span class="sxs-lookup"><span data-stu-id="a75eb-252">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="a75eb-253">Consulte [a guia árvore de chamadas](#the-call-tree-tab) para obter um exemplo de atividades de raiz.</span><span class="sxs-lookup"><span data-stu-id="a75eb-253">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="a75eb-254">A guia árvore de chamadas</span><span class="sxs-lookup"><span data-stu-id="a75eb-254">The Call Tree tab</span></span>   

<span data-ttu-id="a75eb-255">Use a guia **árvore de chamadas** para ver quais [atividades raiz](#root-activities) causam mais trabalho.</span><span class="sxs-lookup"><span data-stu-id="a75eb-255">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="a75eb-256">A guia **árvore de chamadas** exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-256">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="a75eb-257">Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="a75eb-257">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="A guia árvore de chamadas" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="a75eb-259">A guia **árvore de chamadas**</span><span class="sxs-lookup"><span data-stu-id="a75eb-259">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-260">Na figura anterior, o nível superior de itens na coluna **atividade** , como `Evaluate Script` e `Parse HTML` são atividades raiz.</span><span class="sxs-lookup"><span data-stu-id="a75eb-260">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="a75eb-261">O aninhamento representa a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="a75eb-261">The nesting represents the call stack.</span></span>  <span data-ttu-id="a75eb-262">Por exemplo, na figura anterior, `Parse HTML` que causou `Evaluate Script` o resultado `Compile Script` e `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="a75eb-262">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="a75eb-263">A **auto-tempo** representa o tempo gasto diretamente nessa atividade.</span><span class="sxs-lookup"><span data-stu-id="a75eb-263">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="a75eb-264">**Tempo total** representa o tempo gasto nessa atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="a75eb-264">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="a75eb-265">Clique em **período automático**, **tempo total**ou **atividade** para classificar a tabela por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="a75eb-265">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="a75eb-266">Use a caixa de texto **Filtrar** para filtrar eventos por nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="a75eb-266">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="a75eb-267">Por padrão, o menu **agrupamento** é definido como **sem agrupamento**.</span><span class="sxs-lookup"><span data-stu-id="a75eb-267">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="a75eb-268">Use o menu **agrupamento** para classificar a tabela de atividades com base em vários critérios.</span><span class="sxs-lookup"><span data-stu-id="a75eb-268">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="a75eb-269">Clique em **Mostrar pilha mais pesada** \ ( ![ Mostrar pilha mais pesada ][ImageShowHeaviestStackIcon] \) para revelar outra tabela à direita da tabela **atividade** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-269">Click **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="a75eb-270">Clique em uma atividade para preencher a tabela de **pilha mais pesada** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-270">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="a75eb-271">A tabela de **pilha mais pesada** mostra quais filhos da atividade selecionada levaram o tempo mais longo para ser executado.</span><span class="sxs-lookup"><span data-stu-id="a75eb-271">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="a75eb-272">A guia seta para baixo</span><span class="sxs-lookup"><span data-stu-id="a75eb-272">The Bottom-Up tab</span></span>   

<span data-ttu-id="a75eb-273">Use a guia de **cima para baixo** para ver quais atividades resumiram diretamente na maior parte do tempo em agregação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-273">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="a75eb-274">A guia de **cima para baixo** exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-274">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="a75eb-275">Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="a75eb-275">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="A guia seta para baixo" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="a75eb-277">A guia **seta para baixo**</span><span class="sxs-lookup"><span data-stu-id="a75eb-277">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-278">Na seção **principal** da seção chama o gráfico da figura anterior, veja que praticamente praticamente todo o tempo foi gasto em execução `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="a75eb-278">In the **Main** section flame chart of the previous figure, see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="a75eb-279">A atividade superior na guia **inferior** do número anterior é `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="a75eb-279">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="a75eb-280">Veja na guia **abaixo** , a próxima atividade mais cara é `Layout` .</span><span class="sxs-lookup"><span data-stu-id="a75eb-280">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="a75eb-281">A coluna **auto-time** representa o tempo agregado gasto diretamente nessa atividade em todas as ocorrências.</span><span class="sxs-lookup"><span data-stu-id="a75eb-281">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="a75eb-282">A coluna **tempo total** representa o tempo agregado gasto na atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="a75eb-282">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="a75eb-283">A guia log de eventos</span><span class="sxs-lookup"><span data-stu-id="a75eb-283">The Event Log tab</span></span>   

<span data-ttu-id="a75eb-284">Use a guia **log de eventos** para exibir atividades na ordem em que elas ocorreram durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-284">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="a75eb-285">A guia **log de eventos** exibe apenas as atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-285">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="a75eb-286">Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="a75eb-286">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="A guia log de eventos" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="a75eb-288">A guia **log de eventos**</span><span class="sxs-lookup"><span data-stu-id="a75eb-288">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-289">A coluna **hora de início** representa o ponto em que a atividade começou, em relação ao início da gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-289">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="a75eb-290">Por exemplo, a hora de início do `175.7 ms` item selecionado na figura anterior significa que a atividade começou 175,7 MS após o início da gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-290">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="a75eb-291">A coluna **auto-time** representa o tempo gasto diretamente nessa atividade.</span><span class="sxs-lookup"><span data-stu-id="a75eb-291">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="a75eb-292">As colunas de **tempo total** representam o tempo gasto diretamente nessa atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="a75eb-292">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="a75eb-293">Clique em **hora de início**, **hora automática**ou **tempo total** para classificar a tabela por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="a75eb-293">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="a75eb-294">Use a caixa de texto **Filtrar** para filtrar atividades por nome.</span><span class="sxs-lookup"><span data-stu-id="a75eb-294">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="a75eb-295">Use o menu **duração** para filtrar todas as atividades que levaram menos de 1 MS ou 15 ms.</span><span class="sxs-lookup"><span data-stu-id="a75eb-295">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="a75eb-296">Por padrão, o menu **duração** é definido como **todos**, o que significa que todas as atividades são mostradas.</span><span class="sxs-lookup"><span data-stu-id="a75eb-296">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="a75eb-297">Desative as caixas de seleção **carregar**, **script**, **renderização**ou **pintura** para filtrar todas as atividades dessas categorias.</span><span class="sxs-lookup"><span data-stu-id="a75eb-297">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="a75eb-298">Exibir atividade GPU</span><span class="sxs-lookup"><span data-stu-id="a75eb-298">View GPU activity</span></span>   

<span data-ttu-id="a75eb-299">Exiba a atividade GPU na seção **GPU** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-299">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="A seção GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="a75eb-301">A seção **GPU**</span><span class="sxs-lookup"><span data-stu-id="a75eb-301">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="a75eb-302">Exibir atividade rasterizada</span><span class="sxs-lookup"><span data-stu-id="a75eb-302">View raster activity</span></span>   

<span data-ttu-id="a75eb-303">Exiba atividades rasterizadas na seção de **rasterização** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-303">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="A seção de rasterização" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="a75eb-305">A seção de **rasterização**</span><span class="sxs-lookup"><span data-stu-id="a75eb-305">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="a75eb-306">Exibir interações</span><span class="sxs-lookup"><span data-stu-id="a75eb-306">View interactions</span></span>   

<span data-ttu-id="a75eb-307">Use a seção **interações** para localizar e analisar interações do usuário ocorridas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-307">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="A seção interações" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="a75eb-309">A seção **interações**</span><span class="sxs-lookup"><span data-stu-id="a75eb-309">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-310">Uma linha vermelha na parte inferior de uma interação representa o tempo gasto aguardando o thread principal.</span><span class="sxs-lookup"><span data-stu-id="a75eb-310">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="a75eb-311">Clique em uma interação para ver mais informações sobre ela na guia **Resumo** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-311">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="a75eb-312">Analisar quadros por segundo (FPS)</span><span class="sxs-lookup"><span data-stu-id="a75eb-312">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="a75eb-313">O DevTools oferece várias maneiras de analisar os quadros por segundo:</span><span class="sxs-lookup"><span data-stu-id="a75eb-313">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="a75eb-314">Use [o gráfico de FPS](#the-fps-chart) para obter uma visão geral de FPS na duração da gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-314">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="a75eb-315">Use [a seção quadros](#the-frames-section) para ver quanto tempo um determinado quadro levou.</span><span class="sxs-lookup"><span data-stu-id="a75eb-315">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="a75eb-316">Use o **medidor de FPS** para uma estimativa em tempo real de FPS à medida que a página é executada.</span><span class="sxs-lookup"><span data-stu-id="a75eb-316">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="a75eb-317">Consulte [exibir quadros por segundo em tempo real com o medidor de FPS](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="a75eb-317">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="a75eb-318">O gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="a75eb-318">The FPS chart</span></span>   

<span data-ttu-id="a75eb-319">O gráfico de **FPS** fornece uma visão geral da taxa de quadros na duração de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-319">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="a75eb-320">Em geral, quanto maior a barra verde, melhor a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="a75eb-320">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="a75eb-321">Uma barra vermelha acima do gráfico de **FPS** é um aviso informando que a taxa de quadros ficou tão baixa que provavelmente danificaram a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="a75eb-321">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="O gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="a75eb-323">O gráfico de **FPS**</span><span class="sxs-lookup"><span data-stu-id="a75eb-323">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="a75eb-324">A seção quadros</span><span class="sxs-lookup"><span data-stu-id="a75eb-324">The Frames section</span></span>   

<span data-ttu-id="a75eb-325">A seção **frames** informa exatamente quanto tempo um determinado quadro levou.</span><span class="sxs-lookup"><span data-stu-id="a75eb-325">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="a75eb-326">Passe o mouse sobre um quadro para exibir uma dica de ferramenta com mais informações sobre ele.</span><span class="sxs-lookup"><span data-stu-id="a75eb-326">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Passe o mouse sobre um quadro" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="a75eb-328">Passe o mouse sobre um quadro</span><span class="sxs-lookup"><span data-stu-id="a75eb-328">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-329">Clique em um quadro para ver ainda mais informações sobre o quadro na guia **Resumo** .  DevTools descreve o quadro selecionado em azul.</span><span class="sxs-lookup"><span data-stu-id="a75eb-329">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Exibir um quadro na guia Resumo" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="a75eb-331">Exibir um quadro na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="a75eb-331">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="a75eb-332">Exibir solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="a75eb-332">View network requests</span></span>   

<span data-ttu-id="a75eb-333">Expanda a seção **rede** para ver a cascata de solicitações de rede ocorridas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-333">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="A seção rede" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="a75eb-335">A seção **rede**</span><span class="sxs-lookup"><span data-stu-id="a75eb-335">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-336">As solicitações são codificadas por cor da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a75eb-336">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="a75eb-337">HTML: azul</span><span class="sxs-lookup"><span data-stu-id="a75eb-337">HTML: Blue</span></span>  
*   <span data-ttu-id="a75eb-338">CSS: roxo</span><span class="sxs-lookup"><span data-stu-id="a75eb-338">CSS: Purple</span></span>  
*   <span data-ttu-id="a75eb-339">JS: amarelo</span><span class="sxs-lookup"><span data-stu-id="a75eb-339">JS: Yellow</span></span>  
*   <span data-ttu-id="a75eb-340">Imagens: verde</span><span class="sxs-lookup"><span data-stu-id="a75eb-340">Images: Green</span></span>  
    
<span data-ttu-id="a75eb-341">Clique em uma solicitação para ver mais informações sobre ela na guia **Resumo** .  Por exemplo, na figura anterior, a guia **Resumo** está exibindo mais informações sobre a solicitação azul selecionada na seção **rede** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-341">Click on a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="a75eb-342">Um quadrado mais escuro-azul no canto superior esquerdo de uma solicitação significa que é uma solicitação de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="a75eb-342">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="a75eb-343">Um quadrado azul mais claro significa prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="a75eb-343">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="a75eb-344">Por exemplo, na figura anterior, a solicitação azul selecionada é de prioridade mais alta, e a verde abaixo é de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="a75eb-344">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="a75eb-345">Na 1ª das figuras a seguir, a solicitação de `www.bing.com` é representada por uma linha à esquerda, uma barra no meio de uma parte escura e uma parte clara e uma linha à direita.</span><span class="sxs-lookup"><span data-stu-id="a75eb-345">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="a75eb-346">No segundo dos seguintes valores mostram a representação correspondente da mesma solicitação na guia **intervalo** do painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-346">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="a75eb-347">Veja como essas duas representações são mapeadas umas com as outras:</span><span class="sxs-lookup"><span data-stu-id="a75eb-347">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="a75eb-348">A linha à esquerda está tudo no `Connection Start` grupo de eventos, inclusive.</span><span class="sxs-lookup"><span data-stu-id="a75eb-348">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="a75eb-349">Em outras palavras, ele é tudo antes `Request Sent` , exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a75eb-349">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="a75eb-350">A parte leve da barra é `Request Sent` e `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="a75eb-350">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="a75eb-351">A parte escura da barra está `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="a75eb-351">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="a75eb-352">A linha certa é essencialmente tempo gasto aguardando o thread principal.</span><span class="sxs-lookup"><span data-stu-id="a75eb-352">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="a75eb-353">Isso não é representado na guia **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-353">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="A representação de barra de linhas da solicitação www.bing.com" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="a75eb-355">A representação de barra de linhas da `www.bing.com` solicitação</span><span class="sxs-lookup"><span data-stu-id="a75eb-355">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="A seção rede" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="a75eb-357">A seção **rede**</span><span class="sxs-lookup"><span data-stu-id="a75eb-357">The **Network** section</span></span>  
<span data-ttu-id="a75eb-358">::: fim da imagem:::</span><span class="sxs-lookup"><span data-stu-id="a75eb-358">:      ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="a75eb-359">Exibir métricas de memória</span><span class="sxs-lookup"><span data-stu-id="a75eb-359">View memory metrics</span></span>   

<span data-ttu-id="a75eb-360">Habilite a caixa de seleção **memória** para exibir as métricas de memória da última gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-360">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="A caixa de seleção memória" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="a75eb-362">A caixa de seleção **memória**</span><span class="sxs-lookup"><span data-stu-id="a75eb-362">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-363">O DevTools exibe um novo gráfico de **memória** , acima da guia **Resumo** .  Há também um novo gráfico abaixo do gráfico de **rede** , chamado **heap**.</span><span class="sxs-lookup"><span data-stu-id="a75eb-363">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="a75eb-364">O gráfico de **heap** fornece as mesmas informações que a linha de **heap do js** no gráfico de **memória** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-364">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métricas de memória" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="a75eb-366">Métricas de memória</span><span class="sxs-lookup"><span data-stu-id="a75eb-366">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-367">As linhas coloridas do gráfico são mapeadas para as caixas de seleção coloridas acima do gráfico.</span><span class="sxs-lookup"><span data-stu-id="a75eb-367">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="a75eb-368">Desative uma caixa de seleção para ocultar essa categoria do gráfico.</span><span class="sxs-lookup"><span data-stu-id="a75eb-368">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="a75eb-369">O gráfico só exibe a região da gravação selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="a75eb-369">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="a75eb-370">Por exemplo, na figura anterior, o gráfico de **memória** só mostra o uso da memória em torno da 400 MS Mark para a 1750 MS Mark.</span><span class="sxs-lookup"><span data-stu-id="a75eb-370">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="a75eb-371">Exibir a duração de uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-371">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="a75eb-372">Ao analisar uma seção como **Network** ou **Main**, às vezes você precisa de uma estimativa mais precisa de tempo que determinados eventos levaram.</span><span class="sxs-lookup"><span data-stu-id="a75eb-372">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="a75eb-373">Segure `Shift` , clique e segure e arraste para a esquerda ou para a direita para selecionar uma parte da gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-373">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="a75eb-374">Na parte inferior da seleção, o DevTools mostra o tempo que a parte levou.</span><span class="sxs-lookup"><span data-stu-id="a75eb-374">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Exibir a duração de uma parte de uma gravação" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="a75eb-376">Exibir a duração de uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="a75eb-376">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="a75eb-377">Exibir uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="a75eb-377">View a screenshot</span></span>   

<span data-ttu-id="a75eb-378">Consulte [capturar capturas de tela durante a gravação](#capture-screenshots-while-recording) para saber como habilitar capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="a75eb-378">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="a75eb-379">Passe o mouse sobre a **visão geral** para ver uma captura de tela de como a página procurou durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="a75eb-379">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="a75eb-380">A **visão geral** é a seção que contém os gráficos **CPU**, **FPS**e **net** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-380">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Exibir uma captura de tela" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="a75eb-382">Exibir uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="a75eb-382">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-383">Você também pode exibir capturas de tela clicando em um quadro na seção **quadros** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-383">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="a75eb-384">O DevTools exibe uma versão pequena da captura de tela na guia **Resumo** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-384">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Exibir uma captura de tela na guia Resumo" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="a75eb-386">Exibir uma captura de tela na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="a75eb-386">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-387">Clique na miniatura na guia **Resumo** para ampliar a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="a75eb-387">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Aplicar zoom em uma captura de tela da guia Resumo" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="a75eb-389">Aplicar zoom em uma captura de tela da guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="a75eb-389">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="a75eb-390">Exibir informações de camadas</span><span class="sxs-lookup"><span data-stu-id="a75eb-390">View layers information</span></span>   

<span data-ttu-id="a75eb-391">Para exibir as informações de camadas avançadas sobre um quadro:</span><span class="sxs-lookup"><span data-stu-id="a75eb-391">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="a75eb-392">[Habilite a instrumentação avançada de pintura](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="a75eb-392">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="a75eb-393">Selecione um quadro na seção **quadros** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-393">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="a75eb-394">DevTools exibe informações sobre as camadas na guia novas **camadas** , ao lado da guia **log de eventos** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-394">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="O painel camadas" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="a75eb-396">O painel **camadas**</span><span class="sxs-lookup"><span data-stu-id="a75eb-396">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="a75eb-397">Passe o mouse sobre uma camada para realçá-la no diagrama.</span><span class="sxs-lookup"><span data-stu-id="a75eb-397">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Realçar uma camada" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="a75eb-399">Realçar uma camada</span><span class="sxs-lookup"><span data-stu-id="a75eb-399">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="a75eb-400">Para mover o diagrama:</span><span class="sxs-lookup"><span data-stu-id="a75eb-400">To move the diagram:</span></span>  

*   <span data-ttu-id="a75eb-401">Clique em **modo panorâmico** \ ( ![ modo panorâmico ][ImagePanModeIcon] \) para mover-se ao longo dos eixos X e Y.</span><span class="sxs-lookup"><span data-stu-id="a75eb-401">Click **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="a75eb-402">Clique em **modo de rotação** \ ( ![ modo ][ImageRotateModeIcon] de rotação \) para girar ao longo do eixo Z.</span><span class="sxs-lookup"><span data-stu-id="a75eb-402">Click **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="a75eb-403">Clique em **Redefinir transformação** \ ( ![ Redefinir transformação ][ImageResetTransformIcon] \) para redefinir o diagrama para a posição original.</span><span class="sxs-lookup"><span data-stu-id="a75eb-403">Click **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="a75eb-404">Exibir o gerador de perfil do Paint</span><span class="sxs-lookup"><span data-stu-id="a75eb-404">View paint profiler</span></span>   

<span data-ttu-id="a75eb-405">Para exibir informações avançadas sobre um evento de pintura:</span><span class="sxs-lookup"><span data-stu-id="a75eb-405">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="a75eb-406">[Habilite a instrumentação avançada de pintura](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="a75eb-406">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="a75eb-407">Selecione um evento de **pintura** na seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-407">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="A guia perfil do Paint" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="a75eb-409">A guia **perfil do Paint**</span><span class="sxs-lookup"><span data-stu-id="a75eb-409">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a75eb-410">Analisar o desempenho de renderização com a guia renderização</span><span class="sxs-lookup"><span data-stu-id="a75eb-410">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="a75eb-411">Use os recursos da guia **renderização** para ajudar a visualizar o desempenho de renderização da página.</span><span class="sxs-lookup"><span data-stu-id="a75eb-411">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="a75eb-412">Para abrir a guia **renderização** :</span><span class="sxs-lookup"><span data-stu-id="a75eb-412">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="a75eb-413">[Abrir o menu de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="a75eb-413">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="a75eb-414">Comece a digitar `Rendering` e selecione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="a75eb-414">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="a75eb-415">DevTools exibe a guia **renderização** na parte inferior da janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="a75eb-415">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="A guia renderização" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="a75eb-417">A guia **renderização**</span><span class="sxs-lookup"><span data-stu-id="a75eb-417">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="a75eb-418">Exibir quadros por segundo em tempo real com o medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="a75eb-418">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="a75eb-419">O **medidor de FPS** é uma sobreposição que aparece no canto superior direito do seu visor.</span><span class="sxs-lookup"><span data-stu-id="a75eb-419">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="a75eb-420">Ele fornece uma estimativa em tempo real de FPS à medida que a página é executada.</span><span class="sxs-lookup"><span data-stu-id="a75eb-420">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="a75eb-421">Para abrir o **medidor de FPS**:</span><span class="sxs-lookup"><span data-stu-id="a75eb-421">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="a75eb-422">Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="a75eb-422">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="a75eb-423">Habilitar a caixa de seleção **meter de FPS** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-423">Enable the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="O medidor de FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="a75eb-425">O **medidor de FPS**</span><span class="sxs-lookup"><span data-stu-id="a75eb-425">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="a75eb-426">Exibir eventos de pintura em tempo real com o Paint piscando</span><span class="sxs-lookup"><span data-stu-id="a75eb-426">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="a75eb-427">Use o Paint para obter uma exibição em tempo real de todos os eventos de pintura na página.</span><span class="sxs-lookup"><span data-stu-id="a75eb-427">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="a75eb-428">Sempre que uma parte da página é pintada novamente, o DevTools descreve essa seção em verde.</span><span class="sxs-lookup"><span data-stu-id="a75eb-428">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="a75eb-429">Para habilitar a intermitência de tinta:</span><span class="sxs-lookup"><span data-stu-id="a75eb-429">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="a75eb-430">Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="a75eb-430">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="a75eb-431">Habilitar a caixa de seleção **pintura em intermitência** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-431">Enable the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Pintura em intermitência" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="a75eb-433">Pintura em intermitência</span><span class="sxs-lookup"><span data-stu-id="a75eb-433">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="a75eb-434">Exibir uma sobreposição de camadas com bordas de camada</span><span class="sxs-lookup"><span data-stu-id="a75eb-434">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="a75eb-435">Use **bordas de camada** para exibir uma sobreposição de bordas de camada e blocos na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="a75eb-435">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="a75eb-436">Para habilitar bordas de camada:</span><span class="sxs-lookup"><span data-stu-id="a75eb-436">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="a75eb-437">Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="a75eb-437">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="a75eb-438">Habilitar a caixa de seleção **bordas de camada** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-438">Enable the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordas de camada" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="a75eb-440">Bordas de camada</span><span class="sxs-lookup"><span data-stu-id="a75eb-440">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="a75eb-441">Veja os comentários em [`debug_colors.cc`][ChromiumDebugColors] para obter uma explicação das codificações de cores.</span><span class="sxs-lookup"><span data-stu-id="a75eb-441">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="a75eb-442">Encontrar problemas de desempenho de rolagem em tempo real</span><span class="sxs-lookup"><span data-stu-id="a75eb-442">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="a75eb-443">Use problemas de desempenho de rolagem para identificar elementos da página que têm ouvintes de eventos relacionados a rolagem que podem danificar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="a75eb-443">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="a75eb-444">DevTools descreve os elementos que podem ser problemáticos em azul-petróleo.</span><span class="sxs-lookup"><span data-stu-id="a75eb-444">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="a75eb-445">Para ver os problemas de desempenho de rolagem:</span><span class="sxs-lookup"><span data-stu-id="a75eb-445">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="a75eb-446">Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="a75eb-446">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="a75eb-447">Habilitar a caixa de seleção de **problemas de desempenho de rolagem** .</span><span class="sxs-lookup"><span data-stu-id="a75eb-447">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Os problemas de desempenho de rolagem indicam que os objetos restritos de não-camada podem danificar o desempenho de rolagem" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="a75eb-449">Os **problemas de desempenho de rolagem** indicam que os objetos restritos de não-camada podem danificar o desempenho de rolagem</span><span class="sxs-lookup"><span data-stu-id="a75eb-449">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
<!--  
<!--    


-->  

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

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Abrir o menu de comandos-executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Comece a analisar o desempenho do tempo de execução | Documentos da Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demonstração de guias de atividades | problema"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. CC-pesquisa de código"  

> [!NOTE]
> <span data-ttu-id="a75eb-455">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="a75eb-455">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a75eb-456">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a75eb-456">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a75eb-458">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a75eb-458">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
