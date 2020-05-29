---
title: Referência de análise de desempenho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611745"
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







# <span data-ttu-id="da2bf-103">Referência de análise de desempenho</span><span class="sxs-lookup"><span data-stu-id="da2bf-103">Performance Analysis Reference</span></span>   



<span data-ttu-id="da2bf-104">Esta página é uma referência abrangente do Microsoft Edge DevTools recursos relacionados à análise de desempenho.</span><span class="sxs-lookup"><span data-stu-id="da2bf-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="da2bf-105">Consulte [introdução ao analisando o desempenho do tempo de execução][DevtoolsEvaluatePerformanceGettingStarted] para obter um tutorial guia sobre como analisar o desempenho de uma página usando [o Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="da2bf-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="da2bf-106">Desempenho do registro</span><span class="sxs-lookup"><span data-stu-id="da2bf-106">Record performance</span></span>   

### <span data-ttu-id="da2bf-107">Desempenho do registro em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="da2bf-107">Record runtime performance</span></span>   

<span data-ttu-id="da2bf-108">Grave o desempenho do tempo de execução quando quiser analisar o desempenho de uma página enquanto ela estiver em execução, em oposição a carregá-la.</span><span class="sxs-lookup"><span data-stu-id="da2bf-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="da2bf-109">Vá para a página que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="da2bf-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="da2bf-110">Clique na guia **desempenho** do devtools.</span><span class="sxs-lookup"><span data-stu-id="da2bf-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="da2bf-111">Clique em **gravar** ![ registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="da2bf-111">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    
    > ##### <span data-ttu-id="da2bf-112">Figura 1</span><span class="sxs-lookup"><span data-stu-id="da2bf-112">Figure 1</span></span>  
    > **<span data-ttu-id="da2bf-113">Record</span><span class="sxs-lookup"><span data-stu-id="da2bf-113">Record</span></span>**  
    > ![Record][ImageRecord]  

1.  <span data-ttu-id="da2bf-115">Interagir com a página.</span><span class="sxs-lookup"><span data-stu-id="da2bf-115">Interact with the page.</span></span>  <span data-ttu-id="da2bf-116">O DevTools registra todas as atividades de página que ocorrem como resultado de suas interações.</span><span class="sxs-lookup"><span data-stu-id="da2bf-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="da2bf-117">Clique em **gravar** novamente ou em **parar** para parar a gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-117">Click **Record** again or click **Stop** to stop recording.</span></span>  

### <span data-ttu-id="da2bf-118">Desempenho da carga de registros</span><span class="sxs-lookup"><span data-stu-id="da2bf-118">Record load performance</span></span>   

<span data-ttu-id="da2bf-119">Grave o desempenho de carga quando quiser analisar o desempenho de uma página enquanto ela estiver sendo carregada, em vez de executá-la.</span><span class="sxs-lookup"><span data-stu-id="da2bf-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="da2bf-120">Vá para a página que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="da2bf-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="da2bf-121">Abra o painel **desempenho** do devtools.</span><span class="sxs-lookup"><span data-stu-id="da2bf-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="da2bf-122">Clique em atualizar página de atualização de **página** ![ ][ImageRefreshPageIcon] .</span><span class="sxs-lookup"><span data-stu-id="da2bf-122">Click **Refresh page** ![Refresh Page][ImageRefreshPageIcon].</span></span>  <span data-ttu-id="da2bf-123">O DevTools registra métricas de desempenho enquanto a página é atualizada e, em seguida, interrompe automaticamente a gravação em alguns segundos após o término da carga.</span><span class="sxs-lookup"><span data-stu-id="da2bf-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    > ##### <span data-ttu-id="da2bf-124">Figura 2</span><span class="sxs-lookup"><span data-stu-id="da2bf-124">Figure 2</span></span>  
    > **<span data-ttu-id="da2bf-125">Atualizar página</span><span class="sxs-lookup"><span data-stu-id="da2bf-125">Refresh page</span></span>**  
    > ![Atualizar página][ImageRefreshPage]  

<span data-ttu-id="da2bf-127">O DevTools amplia automaticamente a parte da gravação na qual a maioria da atividade ocorreu.</span><span class="sxs-lookup"><span data-stu-id="da2bf-127">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

> ##### <span data-ttu-id="da2bf-128">Figura 3</span><span class="sxs-lookup"><span data-stu-id="da2bf-128">Figure 3</span></span>  
> <span data-ttu-id="da2bf-129">Uma gravação de carregamento de página</span><span class="sxs-lookup"><span data-stu-id="da2bf-129">A page-load recording</span></span>  
> ![Uma gravação de carregamento de página][ImageLoadRecording]  

### <span data-ttu-id="da2bf-131">Capturar capturas de tela durante a gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-131">Capture screenshots while recording</span></span>   

<span data-ttu-id="da2bf-132">Habilite a caixa de seleção **capturas** de tela para capturar uma captura de tela de cada quadro durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-132">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

> ##### <span data-ttu-id="da2bf-133">Figura 4</span><span class="sxs-lookup"><span data-stu-id="da2bf-133">Figure 4</span></span>  
> <span data-ttu-id="da2bf-134">A caixa de seleção **capturas de tela**</span><span class="sxs-lookup"><span data-stu-id="da2bf-134">The **Screenshots** checkbox</span></span>  
> ![A caixa de seleção capturas de tela][ImageScreenshots]  

<span data-ttu-id="da2bf-136">Consulte [exibir uma captura de tela](#view-a-screenshot) para aprender a interagir com capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="da2bf-136">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="da2bf-137">Forçar coleta de lixo durante a gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-137">Force garbage collection while recording</span></span>   

<span data-ttu-id="da2bf-138">Enquanto estiver gravando uma página, clique em **coletar** lixo ![ coletar lixo ][ImageCollectGarbageIcon] para forçar a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="da2bf-138">While you are recording a page, click **Collect garbage** ![Collect garbage][ImageCollectGarbageIcon] to force garbage collection.</span></span>  

> ##### <span data-ttu-id="da2bf-139">Figura 5</span><span class="sxs-lookup"><span data-stu-id="da2bf-139">Figure 5</span></span>  
> <span data-ttu-id="da2bf-140">Coletar lixo</span><span class="sxs-lookup"><span data-stu-id="da2bf-140">Collect garbage</span></span>  
> ![Coletar lixo][ImageCollectGarbage]  

### <span data-ttu-id="da2bf-142">Mostrar configurações de gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-142">Show recording settings</span></span>   

<span data-ttu-id="da2bf-143">Clique em **capturar** configurações ![ de captura de configurações ][ImageCaptureSettingsIcon] para expor mais configurações relacionadas à maneira como o devtools captura gravações de desempenho.</span><span class="sxs-lookup"><span data-stu-id="da2bf-143">Click **Capture settings** ![Capture settings][ImageCaptureSettingsIcon] to expose more settings related to how DevTools captures performance recordings.</span></span>  

> ##### <span data-ttu-id="da2bf-144">Figura 6</span><span class="sxs-lookup"><span data-stu-id="da2bf-144">Figure 6</span></span>  
> <span data-ttu-id="da2bf-145">A seção **configurações de captura**</span><span class="sxs-lookup"><span data-stu-id="da2bf-145">The **Capture settings** section</span></span>  
> ![A seção Configurações de captura][ImageCaptureSettings]  

### <span data-ttu-id="da2bf-147">Desabilitar exemplos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="da2bf-147">Disable JavaScript samples</span></span>   

<span data-ttu-id="da2bf-148">Por padrão, a seção **principal** de uma gravação exibe pilhas de chamadas detalhadas de funções JavaScript que foram chamadas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-148">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="da2bf-149">Para desativar essas pilhas de chamadas:</span><span class="sxs-lookup"><span data-stu-id="da2bf-149">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="da2bf-150">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-150">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="da2bf-151">Consulte [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="da2bf-151">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="da2bf-152">Habilite a caixa de seleção **desativar exemplos de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-152">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="da2bf-153">Faça uma gravação da página.</span><span class="sxs-lookup"><span data-stu-id="da2bf-153">Take a recording of the page.</span></span>  

<span data-ttu-id="da2bf-154">As [figuras 7](#figure-7) e [8](#figure-8) mostram a diferença entre desabilitar e habilitar exemplos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="da2bf-154">[Figure 7](#figure-7) and [Figure 8](#figure-8) show the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="da2bf-155">A seção **principal** da gravação é muito mais curta quando a amostragem está desativada, pois ela omite todas as pilhas de chamadas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="da2bf-155">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

> ##### <span data-ttu-id="da2bf-156">Figura 7</span><span class="sxs-lookup"><span data-stu-id="da2bf-156">Figure 7</span></span>  
> <span data-ttu-id="da2bf-157">Um exemplo de uma gravação quando exemplos de JS está desabilitado</span><span class="sxs-lookup"><span data-stu-id="da2bf-157">An example of a recording when JS samples are disabled</span></span>  
> ![Um exemplo de uma gravação quando exemplos de JS está desabilitado][ImageJSSamplesDisabled]  

> ##### <span data-ttu-id="da2bf-159">Figura 8</span><span class="sxs-lookup"><span data-stu-id="da2bf-159">Figure 8</span></span>  
> <span data-ttu-id="da2bf-160">Um exemplo de uma gravação quando exemplos de JS está habilitado</span><span class="sxs-lookup"><span data-stu-id="da2bf-160">An example of a recording when JS samples are enabled</span></span>  
> ![Um exemplo de uma gravação quando exemplos de JS está habilitado][ImageJSSamplesEnabled]  

### <span data-ttu-id="da2bf-162">Acelerar a rede durante a gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-162">Throttle the network while recording</span></span>   

<span data-ttu-id="da2bf-163">Para acelerar a rede durante a gravação:</span><span class="sxs-lookup"><span data-stu-id="da2bf-163">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="da2bf-164">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-164">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="da2bf-165">Consulte [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="da2bf-165">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="da2bf-166">Defina a **rede** para o nível de limitação desejado.</span><span class="sxs-lookup"><span data-stu-id="da2bf-166">Set **Network** to the desired level of throttling.</span></span>  

### <span data-ttu-id="da2bf-167">Acelerar a CPU durante a gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-167">Throttle the CPU while recording</span></span>   

<span data-ttu-id="da2bf-168">Para reduzir a CPU durante a gravação:</span><span class="sxs-lookup"><span data-stu-id="da2bf-168">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="da2bf-169">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="da2bf-170">Consulte [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="da2bf-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="da2bf-171">Defina a **CPU** para o nível de limitação desejado.</span><span class="sxs-lookup"><span data-stu-id="da2bf-171">Set **CPU** to the desired level of throttling.</span></span>  

<span data-ttu-id="da2bf-172">A limitação é relativa às funcionalidades do seu computador.</span><span class="sxs-lookup"><span data-stu-id="da2bf-172">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="da2bf-173">Por exemplo, a opção **2x de lentidão** faz com que a CPU opere 2 vezes mais lenta do que o normal.</span><span class="sxs-lookup"><span data-stu-id="da2bf-173">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="da2bf-174">O DevTools não simula realmente as CPUs de dispositivos móveis, porque a arquitetura de dispositivos móveis é muito diferente da dos desktops e laptops.</span><span class="sxs-lookup"><span data-stu-id="da2bf-174">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="da2bf-175">Habilitar a instrumentação avançada de pintura</span><span class="sxs-lookup"><span data-stu-id="da2bf-175">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="da2bf-176">Para ver a instrumentação de pintura detalhada:</span><span class="sxs-lookup"><span data-stu-id="da2bf-176">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="da2bf-177">Abrir o menu **configurações de captura** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-177">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="da2bf-178">Consulte [Mostrar configurações de gravação](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="da2bf-178">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="da2bf-179">Marque a caixa de seleção **habilitar instrumentação avançada de pintura (lento)** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-179">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="da2bf-180">Para saber como interagir com as informações de pintura, consulte [Exibir camadas](#view-layers-information) e [Exibir o criador de perfil de tinta](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="da2bf-180">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="da2bf-181">Salvar uma gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-181">Save a recording</span></span>   

<span data-ttu-id="da2bf-182">Para salvar uma gravação, clique com o botão direito do mouse e selecione **salvar perfil**.</span><span class="sxs-lookup"><span data-stu-id="da2bf-182">To save a recording, right-click and select **Save Profile**.</span></span>  

> ##### <span data-ttu-id="da2bf-183">Figura 9</span><span class="sxs-lookup"><span data-stu-id="da2bf-183">Figure 9</span></span>  
> **<span data-ttu-id="da2bf-184">Salvar perfil</span><span class="sxs-lookup"><span data-stu-id="da2bf-184">Save Profile</span></span>**  
> ![Salvar perfil][ImageSaveProfile]  

## <span data-ttu-id="da2bf-186">Carregar uma gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-186">Load a recording</span></span>   

<span data-ttu-id="da2bf-187">Para carregar uma gravação, clique com o botão direito do mouse e selecione **carregar perfil**.</span><span class="sxs-lookup"><span data-stu-id="da2bf-187">To load a recording, right-click and select **Load Profile**.</span></span>  

> ##### <span data-ttu-id="da2bf-188">Figura 10</span><span class="sxs-lookup"><span data-stu-id="da2bf-188">Figure 10</span></span>  
> **<span data-ttu-id="da2bf-189">Carregar perfil</span><span class="sxs-lookup"><span data-stu-id="da2bf-189">Load Profile</span></span>**  
> ![Carregar perfil][ImageLoadProfile]  

## <span data-ttu-id="da2bf-191">Limpar a gravação anterior</span><span class="sxs-lookup"><span data-stu-id="da2bf-191">Clear the previous recording</span></span>   

<span data-ttu-id="da2bf-192">Depois de fazer uma gravação, pressione **limpar** gravação ![ limpar gravação ][ImageClearRecordingIcon] para limpar a gravação do painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-192">After making a recording, press **Clear recording** ![Clear recording][ImageClearRecordingIcon] to clear that recording from the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="da2bf-193">Figura 11</span><span class="sxs-lookup"><span data-stu-id="da2bf-193">Figure 11</span></span>  
> <span data-ttu-id="da2bf-194">Limpar gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-194">Clear recording</span></span>  
> ![Limpar gravação][ImageClearRecording]  

## <span data-ttu-id="da2bf-196">Analisar uma gravação de desempenho</span><span class="sxs-lookup"><span data-stu-id="da2bf-196">Analyze a performance recording</span></span>   

<span data-ttu-id="da2bf-197">Depois de [registrar o desempenho do tempo de execução](#record-runtime-performance) ou o [desempenho da carga de registro](#record-load-performance), o painel **desempenho** fornece muitos dados para analisar o desempenho do que acabou de acontecer.</span><span class="sxs-lookup"><span data-stu-id="da2bf-197">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="da2bf-198">Selecionar uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-198">Select a portion of a recording</span></span>   

<span data-ttu-id="da2bf-199">Arraste o mouse para a esquerda ou para a direita na **visão geral** para selecionar uma parte de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-199">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="da2bf-200">A **visão geral** é a seção que contém os gráficos de **FPS**, **CPU**e **net** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-200">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="da2bf-201">Figura 12</span><span class="sxs-lookup"><span data-stu-id="da2bf-201">Figure 12</span></span>  
> <span data-ttu-id="da2bf-202">Arrastando o mouse pela visão geral para aplicar zoom</span><span class="sxs-lookup"><span data-stu-id="da2bf-202">Dragging the mouse across the Overview to zoom</span></span>  
> ![Arrastando o mouse pela visão geral para aplicar zoom][ImageZoom]  

<span data-ttu-id="da2bf-204">Para selecionar uma parte usando o teclado:</span><span class="sxs-lookup"><span data-stu-id="da2bf-204">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="da2bf-205">Clique no plano de fundo da seção **principal** ou de qualquer uma das seções ao lado dela, como **interações**, **rede**ou **GPU**.</span><span class="sxs-lookup"><span data-stu-id="da2bf-205">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="da2bf-206">Este fluxo de trabalho de teclado funciona apenas quando uma dessas seções está em foco.</span><span class="sxs-lookup"><span data-stu-id="da2bf-206">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="da2bf-207">Use as `W` teclas,, `A` `S` , `D` para ampliar, mover para a esquerda, reduzir e mover para a direita, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="da2bf-207">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="da2bf-208">Para selecionar uma parte usando uma trackpad:</span><span class="sxs-lookup"><span data-stu-id="da2bf-208">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="da2bf-209">Passe o mouse sobre a seção **visão geral** ou a seção **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-209">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="da2bf-210">A seção **visão geral** é a área que contém os gráficos de **FPS**, **CPU**e **net** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-210">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="da2bf-211">A seção **detalhes** é a área que contém a seção **principal** , a seção **interações** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="da2bf-211">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="da2bf-212">Usando dois dedos, passe o dedo para baixo para reduzir, deslize o dedo para a esquerda para mover para a esquerda, passe o dedo para baixo para ampliar e passe o dedo para a direita para mover para a direita.</span><span class="sxs-lookup"><span data-stu-id="da2bf-212">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="da2bf-213">Para rolar um gráfico de chama longa na seção **principal** ou em qualquer um dos vizinhos, clique e mantenha pressionado enquanto arrasta para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="da2bf-213">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="da2bf-214">Arraste para a esquerda e para a direita para mover qual parte da gravação está selecionada.</span><span class="sxs-lookup"><span data-stu-id="da2bf-214">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="da2bf-215">Atividades de pesquisa</span><span class="sxs-lookup"><span data-stu-id="da2bf-215">Search activities</span></span>   

<span data-ttu-id="da2bf-216">Pressione `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \) para abrir a caixa de pesquisa na parte inferior do painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-216">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="da2bf-217">Figura 13</span><span class="sxs-lookup"><span data-stu-id="da2bf-217">Figure 13</span></span>  
> <span data-ttu-id="da2bf-218">Usando Regex na caixa de pesquisa na parte inferior da janela para localizar qualquer atividade que comece com</span><span class="sxs-lookup"><span data-stu-id="da2bf-218">Using regex in the search box at the bottom of the window to find any activity that begins with</span></span> `E`  
> ![A caixa de pesquisa][ImageSearch]  

<span data-ttu-id="da2bf-220">Para navegar entre atividades que correspondam à sua consulta:</span><span class="sxs-lookup"><span data-stu-id="da2bf-220">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="da2bf-221">Usar os **Previous** ![ botões anterior ][ImagePreviousIcon] e **próximo** ![ próximo ][ImageNextIcon] .</span><span class="sxs-lookup"><span data-stu-id="da2bf-221">Use the **Previous** ![Previous][ImagePreviousIcon] and **Next** ![Next][ImageNextIcon] buttons.</span></span>  
*   <span data-ttu-id="da2bf-222">Pressione `Shift` + `Enter` para selecionar o anterior ou `Enter` para selecionar o próximo.</span><span class="sxs-lookup"><span data-stu-id="da2bf-222">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="da2bf-223">Para modificar as configurações de consulta:</span><span class="sxs-lookup"><span data-stu-id="da2bf-223">To modify query settings:</span></span>  

*   <span data-ttu-id="da2bf-224">Pressione maiúsculas e minúsculas **diferenciando** maiúsculas de minúsculas ![ ][ImageSearchCaseIcon] para fazer a consulta diferencia maiúsculas</span><span class="sxs-lookup"><span data-stu-id="da2bf-224">Press **Case sensitive** ![Case sensitive][ImageSearchCaseIcon] to make the query case sensitive.</span></span>  
*   <span data-ttu-id="da2bf-225">Pressione **Regex** ![ Regex Regex ][ImageSearchRegexIcon] para usar uma expressão regular em sua consulta.</span><span class="sxs-lookup"><span data-stu-id="da2bf-225">Press **Regex** ![Regex][ImageSearchRegexIcon] to use a regular expression in your query.</span></span>  

<span data-ttu-id="da2bf-226">Para ocultar a caixa de pesquisa, clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="da2bf-226">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="da2bf-227">Exibir atividade de thread principal</span><span class="sxs-lookup"><span data-stu-id="da2bf-227">View main thread activity</span></span>   

<span data-ttu-id="da2bf-228">Use a seção **principal** para exibir atividades ocorridas no thread principal da página.</span><span class="sxs-lookup"><span data-stu-id="da2bf-228">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

> ##### <span data-ttu-id="da2bf-229">Figura 14</span><span class="sxs-lookup"><span data-stu-id="da2bf-229">Figure 14</span></span>  
> <span data-ttu-id="da2bf-230">A seção **principal**</span><span class="sxs-lookup"><span data-stu-id="da2bf-230">The **Main** section</span></span>  
> ![A seção principal][ImageMain]  

<span data-ttu-id="da2bf-232">Clique em um evento para ver mais informações sobre ele na guia **Resumo** .  DevTools descreve o evento selecionado.</span><span class="sxs-lookup"><span data-stu-id="da2bf-232">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

> ##### <span data-ttu-id="da2bf-233">Figura 15</span><span class="sxs-lookup"><span data-stu-id="da2bf-233">Figure 15</span></span>  
> <span data-ttu-id="da2bf-234">Mais informações sobre a `anonymous` função na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="da2bf-234">More information about the `anonymous` function in the **Summary** tab</span></span>  
> ![Mais informações sobre a função anônimo na guia Resumo][ImageMainEventSummary]  

<span data-ttu-id="da2bf-236">DevTools representa a atividade de thread principal com um gráfico de chama.</span><span class="sxs-lookup"><span data-stu-id="da2bf-236">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="da2bf-237">O eixo x representa a gravação ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="da2bf-237">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="da2bf-238">O eixo y representa a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="da2bf-238">The y-axis represents the call stack.</span></span>  <span data-ttu-id="da2bf-239">Os eventos na parte superior causam os eventos abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="da2bf-239">The events on top cause the events below it.</span></span>  

> ##### <span data-ttu-id="da2bf-240">Figura 16</span><span class="sxs-lookup"><span data-stu-id="da2bf-240">Figure 16</span></span>  
> <span data-ttu-id="da2bf-241">Um gráfico de chama na seção **principal**</span><span class="sxs-lookup"><span data-stu-id="da2bf-241">A flame chart in the **Main** section</span></span>  
> ![Um gráfico de chama][ImageFlameChart]  

<span data-ttu-id="da2bf-243">Na [Figura 16](#figure-16), um `click` evento causou uma `Function Call` entrada na `activitytabs.js` linha 53.</span><span class="sxs-lookup"><span data-stu-id="da2bf-243">In [Figure 16](#figure-16), a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="da2bf-244">Abaixo `Function Call` , você verá que uma função anônima foi chamada.</span><span class="sxs-lookup"><span data-stu-id="da2bf-244">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="da2bf-245">A função anônima chamada `a` , que é chamada `wait` , que é chamada `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="da2bf-245">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="da2bf-246">DevTools atribui as cores aleatórias de scripts.</span><span class="sxs-lookup"><span data-stu-id="da2bf-246">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="da2bf-247">Na [Figura 16](#figure-16), as chamadas de função de um script são verde claro em cores.</span><span class="sxs-lookup"><span data-stu-id="da2bf-247">In [Figure 16](#figure-16), function calls from one script are colored light green.</span></span>  <span data-ttu-id="da2bf-248">As chamadas de outro script são coloridas bege.</span><span class="sxs-lookup"><span data-stu-id="da2bf-248">Calls from another script are colored beige.</span></span>  <span data-ttu-id="da2bf-249">O amarelo mais escuro representa a atividade de script e o evento roxo representa a atividade de renderização.</span><span class="sxs-lookup"><span data-stu-id="da2bf-249">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="da2bf-250">Esses eventos amarelos e roxos mais escuros são consistentes em todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="da2bf-250">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="da2bf-251">Confira [desabilitar exemplos de JavaScript](#disable-javascript-samples) se você quiser ocultar o gráfico de chama detalhado de chamadas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="da2bf-251">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="da2bf-252">Quando os exemplos de JS estiverem desativados, você verá eventos de alto nível, como `Event: click` e `Function Call` da [Figura 16](#figure-16).</span><span class="sxs-lookup"><span data-stu-id="da2bf-252">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from [Figure 16](#figure-16).</span></span>  

### <span data-ttu-id="da2bf-253">Exibir atividades em uma tabela</span><span class="sxs-lookup"><span data-stu-id="da2bf-253">View activities in a table</span></span>   

<span data-ttu-id="da2bf-254">Depois de gravar uma página, você não precisa confiar exclusivamente na seção **principal** para analisar atividades.</span><span class="sxs-lookup"><span data-stu-id="da2bf-254">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="da2bf-255">O DevTools também fornece três exibições em tabelas para analisar atividades.</span><span class="sxs-lookup"><span data-stu-id="da2bf-255">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="da2bf-256">Cada modo de exibição oferece uma perspectiva diferente nas atividades:</span><span class="sxs-lookup"><span data-stu-id="da2bf-256">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="da2bf-257">Quando quiser exibir as atividades raiz que causam mais trabalho, use [a guia árvore de **chamadas** ](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="da2bf-257">When you want to view the root activities that cause the most work, use [the **Call Tree** tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="da2bf-258">Quando você quiser exibir as atividades nas quais o tempo foi gasto diretamente, use [a guia de **baixo para cima** ](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="da2bf-258">When you want to view the activities where the most time was directly spent, use [the **Bottom-Up** tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="da2bf-259">Quando quiser exibir as atividades na ordem em que elas ocorreram durante a gravação, use [a guia **log de eventos** ](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="da2bf-259">When you want to view the activities in the order in which they occurred during the recording, use [the **Event Log** tab](#the-event-log-tab).</span></span>  

> [!NOTE]
> <span data-ttu-id="da2bf-260">Todas as próximas três seções fazem referência à mesma demonstração.</span><span class="sxs-lookup"><span data-stu-id="da2bf-260">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="da2bf-261">Execute a demonstração você mesmo na [demonstração das guias de atividades][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="da2bf-261">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="da2bf-262">Atividades raiz</span><span class="sxs-lookup"><span data-stu-id="da2bf-262">Root activities</span></span>   

<span data-ttu-id="da2bf-263">Aqui está uma explicação do conceito de **atividades raiz** que é mencionado na guia de **árvore de chamadas** , na guia **de baixo para cima** e nas seções do log de **eventos** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-263">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="da2bf-264">As atividades raiz são aquelas que fazem com que o navegador execute algum trabalho.</span><span class="sxs-lookup"><span data-stu-id="da2bf-264">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="da2bf-265">Por exemplo, quando você clica em uma página, o navegador dispara uma `Event` atividade como a atividade raiz.</span><span class="sxs-lookup"><span data-stu-id="da2bf-265">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="da2bf-266">Isso `Event` pode fazer com que um manipulador seja executado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="da2bf-266">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="da2bf-267">No gráfico chama da seção **principal** , as atividades raiz estão na parte superior do gráfico.</span><span class="sxs-lookup"><span data-stu-id="da2bf-267">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="da2bf-268">Nas guias **árvore de chamadas** e **log de eventos** , as atividades raiz são os itens de nível superior.</span><span class="sxs-lookup"><span data-stu-id="da2bf-268">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="da2bf-269">Consulte [a guia árvore de chamadas](#the-call-tree-tab) para obter um exemplo de atividades de raiz.</span><span class="sxs-lookup"><span data-stu-id="da2bf-269">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="da2bf-270">A guia árvore de chamadas</span><span class="sxs-lookup"><span data-stu-id="da2bf-270">The Call Tree tab</span></span>   

<span data-ttu-id="da2bf-271">Use a guia **árvore de chamadas** para ver quais [atividades raiz](#root-activities) causam mais trabalho.</span><span class="sxs-lookup"><span data-stu-id="da2bf-271">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="da2bf-272">A guia **árvore de chamadas** exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-272">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="da2bf-273">Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="da2bf-273">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="da2bf-274">Figura 17</span><span class="sxs-lookup"><span data-stu-id="da2bf-274">Figure 17</span></span>  
> <span data-ttu-id="da2bf-275">A guia **árvore de chamadas**</span><span class="sxs-lookup"><span data-stu-id="da2bf-275">The **Call Tree** tab</span></span>  
> ![A guia árvore de chamadas][ImageCallTree]  

<span data-ttu-id="da2bf-277">Na [Figura 17](#figure-17), o nível superior de itens na coluna **atividade** , como `Evaluate Script` e `Parse HTML` são atividades raiz.</span><span class="sxs-lookup"><span data-stu-id="da2bf-277">In [Figure 17](#figure-17), the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="da2bf-278">O aninhamento representa a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="da2bf-278">The nesting represents the call stack.</span></span>  <span data-ttu-id="da2bf-279">Por exemplo, na [Figura 17](#figure-17), `Parse HTML` que causou `Evaluate Script` o resultado `Compile Script` e `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="da2bf-279">For example, in [Figure 17](#figure-17), `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="da2bf-280">A **auto-tempo** representa o tempo gasto diretamente nessa atividade.</span><span class="sxs-lookup"><span data-stu-id="da2bf-280">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="da2bf-281">**Tempo total** representa o tempo gasto nessa atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="da2bf-281">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="da2bf-282">Clique em **período automático**, **tempo total**ou **atividade** para classificar a tabela por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="da2bf-282">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="da2bf-283">Use a caixa de texto **Filtrar** para filtrar eventos por nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="da2bf-283">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="da2bf-284">Por padrão, o menu **agrupamento** é definido como **sem agrupamento**.</span><span class="sxs-lookup"><span data-stu-id="da2bf-284">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="da2bf-285">Use o menu **agrupamento** para classificar a tabela de atividades com base em vários critérios.</span><span class="sxs-lookup"><span data-stu-id="da2bf-285">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="da2bf-286">Clique em **Mostrar pilha mais pesada** ![ Mostrar pilha mais pesada ][ImageShowHeaviestStackIcon] para revelar outra tabela à direita da tabela **atividade** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-286">Click **Show Heaviest Stack** ![Show Heaviest Stack][ImageShowHeaviestStackIcon] to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="da2bf-287">Clique em uma atividade para preencher a tabela de **pilha mais pesada** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-287">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="da2bf-288">A tabela de **pilha mais pesada** mostra quais filhos da atividade selecionada levaram o tempo mais longo para ser executado.</span><span class="sxs-lookup"><span data-stu-id="da2bf-288">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="da2bf-289">A guia seta para baixo</span><span class="sxs-lookup"><span data-stu-id="da2bf-289">The Bottom-Up tab</span></span>   

<span data-ttu-id="da2bf-290">Use a guia de **cima para baixo** para ver quais atividades resumiram diretamente na maior parte do tempo em agregação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-290">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="da2bf-291">A guia de **cima para baixo** exibe apenas atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-291">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="da2bf-292">Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="da2bf-292">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="da2bf-293">Figura 18</span><span class="sxs-lookup"><span data-stu-id="da2bf-293">Figure 18</span></span>  
> <span data-ttu-id="da2bf-294">A guia **seta para baixo**</span><span class="sxs-lookup"><span data-stu-id="da2bf-294">The **Bottom-Up** tab</span></span>  
> ![A guia seta para baixo][ImageBottomUp]  

<span data-ttu-id="da2bf-296">Na seção **principal** , gráfico da [Figura 18](#figure-18), veja que quase todo o tempo gastou em execução `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="da2bf-296">In the **Main** section flame chart of [Figure 18](#figure-18), see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="da2bf-297">A atividade superior na guia de **baixo para cima** da [Figura 18](#figure-18) é `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="da2bf-297">The top activity in the **Bottom-Up** tab of [Figure 18](#figure-18) is `Parse HTML`.</span></span>  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="da2bf-298">Veja na guia **abaixo** , a próxima atividade mais cara é `Layout` .</span><span class="sxs-lookup"><span data-stu-id="da2bf-298">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="da2bf-299">A coluna **auto-time** representa o tempo agregado gasto diretamente nessa atividade em todas as ocorrências.</span><span class="sxs-lookup"><span data-stu-id="da2bf-299">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="da2bf-300">A coluna **tempo total** representa o tempo agregado gasto na atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="da2bf-300">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="da2bf-301">A guia log de eventos</span><span class="sxs-lookup"><span data-stu-id="da2bf-301">The Event Log tab</span></span>   

<span data-ttu-id="da2bf-302">Use a guia **log de eventos** para exibir atividades na ordem em que elas ocorreram durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-302">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="da2bf-303">A guia **log de eventos** exibe apenas as atividades durante a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-303">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="da2bf-304">Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.</span><span class="sxs-lookup"><span data-stu-id="da2bf-304">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="da2bf-305">Figura 19</span><span class="sxs-lookup"><span data-stu-id="da2bf-305">Figure 19</span></span>  
> <span data-ttu-id="da2bf-306">A guia **log de eventos**</span><span class="sxs-lookup"><span data-stu-id="da2bf-306">The **Event Log** tab</span></span>  
> ![A guia log de eventos][ImageEventLog]  

<span data-ttu-id="da2bf-308">A coluna **hora de início** representa o ponto em que a atividade começou, em relação ao início da gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-308">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="da2bf-309">Por exemplo, a hora de início do `175.7 ms` item selecionado na [Figura 19](#figure-19) significa que a atividade começou 175,7 MS após o início da gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-309">For example, the start time of `175.7 ms` for the selected item in [Figure 19](#figure-19) means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="da2bf-310">A coluna **auto-time** representa o tempo gasto diretamente nessa atividade.</span><span class="sxs-lookup"><span data-stu-id="da2bf-310">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="da2bf-311">As colunas de **tempo total** representam o tempo gasto diretamente nessa atividade ou em qualquer um dos filhos.</span><span class="sxs-lookup"><span data-stu-id="da2bf-311">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="da2bf-312">Clique em **hora de início**, **hora automática**ou **tempo total** para classificar a tabela por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="da2bf-312">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="da2bf-313">Use a caixa de texto **Filtrar** para filtrar atividades por nome.</span><span class="sxs-lookup"><span data-stu-id="da2bf-313">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="da2bf-314">Use o menu **duração** para filtrar todas as atividades que levaram menos de 1 MS ou 15 ms.</span><span class="sxs-lookup"><span data-stu-id="da2bf-314">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="da2bf-315">Por padrão, o menu **duração** é definido como **todos**, o que significa que todas as atividades são mostradas.</span><span class="sxs-lookup"><span data-stu-id="da2bf-315">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="da2bf-316">Desative as caixas de seleção **carregar**, **script**, **renderização**ou **pintura** para filtrar todas as atividades dessas categorias.</span><span class="sxs-lookup"><span data-stu-id="da2bf-316">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="da2bf-317">Exibir atividade GPU</span><span class="sxs-lookup"><span data-stu-id="da2bf-317">View GPU activity</span></span>   

<span data-ttu-id="da2bf-318">Exiba a atividade GPU na seção **GPU** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-318">View GPU activity in the **GPU** section.</span></span>  

> ##### <span data-ttu-id="da2bf-319">Figura 20</span><span class="sxs-lookup"><span data-stu-id="da2bf-319">Figure 20</span></span>  
> <span data-ttu-id="da2bf-320">A seção **GPU**</span><span class="sxs-lookup"><span data-stu-id="da2bf-320">The **GPU** section</span></span>  
> ![A seção GPU][ImageGpu]  

### <span data-ttu-id="da2bf-322">Exibir atividade rasterizada</span><span class="sxs-lookup"><span data-stu-id="da2bf-322">View raster activity</span></span>   

<span data-ttu-id="da2bf-323">Exiba atividades rasterizadas na seção de **rasterização** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-323">View raster activity in the **Raster** section.</span></span>  

> ##### <span data-ttu-id="da2bf-324">Figura 21</span><span class="sxs-lookup"><span data-stu-id="da2bf-324">Figure 21</span></span>  
> <span data-ttu-id="da2bf-325">A seção de **rasterização**</span><span class="sxs-lookup"><span data-stu-id="da2bf-325">The **Raster** section</span></span>  
> ![A seção de rasterização][ImageRaster]  

### <span data-ttu-id="da2bf-327">Exibir interações</span><span class="sxs-lookup"><span data-stu-id="da2bf-327">View interactions</span></span>   

<span data-ttu-id="da2bf-328">Use a seção **interações** para localizar e analisar interações do usuário ocorridas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-328">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

> ##### <span data-ttu-id="da2bf-329">Figura 22</span><span class="sxs-lookup"><span data-stu-id="da2bf-329">Figure 22</span></span>  
> <span data-ttu-id="da2bf-330">A seção **interações**</span><span class="sxs-lookup"><span data-stu-id="da2bf-330">The **Interactions** section</span></span>  
> ![A seção interações][ImageInteractions]  

<span data-ttu-id="da2bf-332">Uma linha vermelha na parte inferior de uma interação representa o tempo gasto aguardando o thread principal.</span><span class="sxs-lookup"><span data-stu-id="da2bf-332">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="da2bf-333">Clique em uma interação para ver mais informações sobre ela na guia **Resumo** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-333">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="da2bf-334">Analisar quadros por segundo (FPS)</span><span class="sxs-lookup"><span data-stu-id="da2bf-334">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="da2bf-335">O DevTools oferece várias maneiras de analisar os quadros por segundo:</span><span class="sxs-lookup"><span data-stu-id="da2bf-335">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="da2bf-336">Use [o gráfico de **FPS** ](#the-fps-chart) para obter uma visão geral de FPS na duração da gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-336">Use [the **FPS** chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="da2bf-337">Use [a seção **quadros** ](#the-frames-section) para ver quanto tempo um determinado quadro levou.</span><span class="sxs-lookup"><span data-stu-id="da2bf-337">Use [the **Frames** section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="da2bf-338">Use o **medidor de FPS** para uma estimativa em tempo real de FPS à medida que a página é executada.</span><span class="sxs-lookup"><span data-stu-id="da2bf-338">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="da2bf-339">Consulte [exibir quadros por segundo em tempo real com o medidor de FPS](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="da2bf-339">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  

#### <span data-ttu-id="da2bf-340">O gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="da2bf-340">The FPS chart</span></span>   

<span data-ttu-id="da2bf-341">O gráfico de **FPS** fornece uma visão geral da taxa de quadros na duração de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-341">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="da2bf-342">Em geral, quanto maior a barra verde, melhor a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="da2bf-342">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="da2bf-343">Uma barra vermelha acima do gráfico de **FPS** é um aviso informando que a taxa de quadros ficou tão baixa que provavelmente danificaram a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="da2bf-343">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

> ##### <span data-ttu-id="da2bf-344">Figura 23</span><span class="sxs-lookup"><span data-stu-id="da2bf-344">Figure 23</span></span>  
> <span data-ttu-id="da2bf-345">O gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="da2bf-345">The FPS chart</span></span>  
> ![O gráfico de FPS][ImageFpsChart]  

#### <span data-ttu-id="da2bf-347">A seção quadros</span><span class="sxs-lookup"><span data-stu-id="da2bf-347">The Frames section</span></span>   

<span data-ttu-id="da2bf-348">A seção **frames** informa exatamente quanto tempo um determinado quadro levou.</span><span class="sxs-lookup"><span data-stu-id="da2bf-348">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="da2bf-349">Passe o mouse sobre um quadro para exibir uma dica de ferramenta com mais informações sobre ele.</span><span class="sxs-lookup"><span data-stu-id="da2bf-349">Hover over a frame to view a tooltip with more information about it.</span></span>  

> ##### <span data-ttu-id="da2bf-350">Figura 24</span><span class="sxs-lookup"><span data-stu-id="da2bf-350">Figure 24</span></span>  
> <span data-ttu-id="da2bf-351">Passar o mouse sobre um quadro</span><span class="sxs-lookup"><span data-stu-id="da2bf-351">Hovering over a frame</span></span>  
> ![Passar o mouse sobre um quadro][ImageFramesSection]  

<span data-ttu-id="da2bf-353">Clique em um quadro para ver ainda mais informações sobre o quadro na guia **Resumo** .  DevTools descreve o quadro selecionado em azul.</span><span class="sxs-lookup"><span data-stu-id="da2bf-353">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

> ##### <span data-ttu-id="da2bf-354">Figura 25</span><span class="sxs-lookup"><span data-stu-id="da2bf-354">Figure 25</span></span>  
> <span data-ttu-id="da2bf-355">Exibir um quadro na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="da2bf-355">Viewing a frame in the **Summary** tab</span></span>  
> ![Exibir um quadro na guia Resumo][ImageFrameSummary]  

### <span data-ttu-id="da2bf-357">Exibir solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="da2bf-357">View network requests</span></span>   

<span data-ttu-id="da2bf-358">Expanda a seção **rede** para ver a cascata de solicitações de rede ocorridas durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-358">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

> ##### <span data-ttu-id="da2bf-359">Figura 26</span><span class="sxs-lookup"><span data-stu-id="da2bf-359">Figure 26</span></span>  
> <span data-ttu-id="da2bf-360">A seção **rede**</span><span class="sxs-lookup"><span data-stu-id="da2bf-360">The **Network** section</span></span>  
> ![A seção rede][ImageNetworkRequest]  

<span data-ttu-id="da2bf-362">As solicitações são codificadas por cor da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="da2bf-362">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="da2bf-363">HTML: azul</span><span class="sxs-lookup"><span data-stu-id="da2bf-363">HTML: Blue</span></span>  
*   <span data-ttu-id="da2bf-364">CSS: roxo</span><span class="sxs-lookup"><span data-stu-id="da2bf-364">CSS: Purple</span></span>  
*   <span data-ttu-id="da2bf-365">JS: amarelo</span><span class="sxs-lookup"><span data-stu-id="da2bf-365">JS: Yellow</span></span>  
*   <span data-ttu-id="da2bf-366">Imagens: verde</span><span class="sxs-lookup"><span data-stu-id="da2bf-366">Images: Green</span></span>  

<span data-ttu-id="da2bf-367">Clique em uma solicitação para ver mais informações sobre ela na guia **Resumo** .  Por exemplo, na [Figura 26](#figure-26) , a guia **Resumo** está exibindo mais informações sobre a solicitação azul selecionada na seção **rede** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-367">Click on a request to view more information about it in the **Summary** tab.  For example, in [Figure 26](#figure-26) the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="da2bf-368">Um quadrado mais escuro-azul no canto superior esquerdo de uma solicitação significa que é uma solicitação de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="da2bf-368">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="da2bf-369">Um quadrado azul mais claro significa prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="da2bf-369">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="da2bf-370">Por exemplo, na [Figura 26](#figure-26) , a solicitação azul selecionada é de prioridade mais alta, e a verde abaixo é de prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="da2bf-370">For example, in [Figure 26](#figure-26) the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="da2bf-371">Na [Figura 27](#figure-27), a solicitação para `www.bing.com` é representada por uma linha à esquerda, uma barra no meio com uma parte escura e uma parte Light e uma linha à direita.</span><span class="sxs-lookup"><span data-stu-id="da2bf-371">In [Figure 27](#figure-27), the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="da2bf-372">A [Figura 28](#figure-28) mostra a representação correspondente da mesma solicitação na guia **intervalo** do painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-372">[Figure 28](#figure-28) shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="da2bf-373">Veja como essas duas representações são mapeadas umas com as outras:</span><span class="sxs-lookup"><span data-stu-id="da2bf-373">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="da2bf-374">A linha à esquerda está tudo no `Connection Start` grupo de eventos, inclusive.</span><span class="sxs-lookup"><span data-stu-id="da2bf-374">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="da2bf-375">Em outras palavras, ele é tudo antes `Request Sent` , exclusivo.</span><span class="sxs-lookup"><span data-stu-id="da2bf-375">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="da2bf-376">A parte leve da barra é `Request Sent` e `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="da2bf-376">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="da2bf-377">A parte escura da barra está `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="da2bf-377">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="da2bf-378">A linha certa é essencialmente tempo gasto aguardando o thread principal.</span><span class="sxs-lookup"><span data-stu-id="da2bf-378">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="da2bf-379">Isso não é representado na guia **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-379">This is not represented in the **Timing** tab.</span></span>  

> ##### <span data-ttu-id="da2bf-380">Figura 27</span><span class="sxs-lookup"><span data-stu-id="da2bf-380">Figure 27</span></span>  
> <span data-ttu-id="da2bf-381">A representação de barra de linhas da `www.bing.com` solicitação</span><span class="sxs-lookup"><span data-stu-id="da2bf-381">The line-bar representation of the `www.bing.com` request</span></span>  
> ![A representação de barra de linhas da solicitação www.bing.com][ImageLineBar]  

> ##### <span data-ttu-id="da2bf-383">Figura 28</span><span class="sxs-lookup"><span data-stu-id="da2bf-383">Figure 28</span></span>  
> <span data-ttu-id="da2bf-384">A representação da guia **intervalo** da `www.bing.com` solicitação</span><span class="sxs-lookup"><span data-stu-id="da2bf-384">The **Timing** tab representation of the `www.bing.com` request</span></span>  
> ![A seção rede][ImageTiming]  

### <span data-ttu-id="da2bf-386">Exibir métricas de memória</span><span class="sxs-lookup"><span data-stu-id="da2bf-386">View memory metrics</span></span>   

<span data-ttu-id="da2bf-387">Habilite a caixa de seleção **memória** para exibir as métricas de memória da última gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-387">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

> ##### <span data-ttu-id="da2bf-388">Figura 29</span><span class="sxs-lookup"><span data-stu-id="da2bf-388">Figure 29</span></span>  
> <span data-ttu-id="da2bf-389">A caixa de seleção **memória**</span><span class="sxs-lookup"><span data-stu-id="da2bf-389">The **Memory** checkbox</span></span>  
> ![A caixa de seleção memória][ImageMemory]  

<span data-ttu-id="da2bf-391">O DevTools exibe um novo gráfico de **memória** , acima da guia **Resumo** .  Há também um novo gráfico abaixo do gráfico de **rede** , chamado **heap**.</span><span class="sxs-lookup"><span data-stu-id="da2bf-391">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="da2bf-392">O gráfico de **heap** fornece as mesmas informações que a linha de **heap do js** no gráfico de **memória** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-392">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

> ##### <span data-ttu-id="da2bf-393">Figura 30</span><span class="sxs-lookup"><span data-stu-id="da2bf-393">Figure 30</span></span>  
> <span data-ttu-id="da2bf-394">Métricas de memória, acima da guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="da2bf-394">Memory metrics, above the **Summary** tab</span></span>  
> ![Métricas de memória][ImageMemoryMetrics]  

<span data-ttu-id="da2bf-396">As linhas coloridas do gráfico são mapeadas para as caixas de seleção coloridas acima do gráfico.</span><span class="sxs-lookup"><span data-stu-id="da2bf-396">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="da2bf-397">Desative uma caixa de seleção para ocultar essa categoria do gráfico.</span><span class="sxs-lookup"><span data-stu-id="da2bf-397">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="da2bf-398">O gráfico só exibe a região da gravação selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="da2bf-398">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="da2bf-399">Por exemplo, na [Figura 30](#figure-30), o gráfico de **memória** só mostra o uso da memória em torno da 400 ms Mark para a 1750 MS Mark.</span><span class="sxs-lookup"><span data-stu-id="da2bf-399">For example, in [Figure 30](#figure-30), the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="da2bf-400">Exibir a duração de uma parte de uma gravação</span><span class="sxs-lookup"><span data-stu-id="da2bf-400">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="da2bf-401">Ao analisar uma seção como **Network** ou **Main**, às vezes você precisa de uma estimativa mais precisa de tempo que determinados eventos levaram.</span><span class="sxs-lookup"><span data-stu-id="da2bf-401">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="da2bf-402">Segure `Shift` , clique e segure e arraste para a esquerda ou para a direita para selecionar uma parte da gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-402">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="da2bf-403">Na parte inferior da seleção, o DevTools mostra o tempo que a parte levou.</span><span class="sxs-lookup"><span data-stu-id="da2bf-403">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

> ##### <span data-ttu-id="da2bf-404">Figura 31</span><span class="sxs-lookup"><span data-stu-id="da2bf-404">Figure 31</span></span>  
> <span data-ttu-id="da2bf-405">O `9.47ms` carimbo de data/hora na parte inferior da parte selecionada indica o tempo que a parte levou</span><span class="sxs-lookup"><span data-stu-id="da2bf-405">The `9.47ms` timestamp at the bottom of the selected portion indicates how long that portion took</span></span>  
> ![Exibindo a duração de uma parte de uma gravação][ImageDuration]  

### <span data-ttu-id="da2bf-407">Exibir uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="da2bf-407">View a screenshot</span></span>   

<span data-ttu-id="da2bf-408">Consulte [capturar capturas de tela durante a gravação](#capture-screenshots-while-recording) para saber como habilitar capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="da2bf-408">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="da2bf-409">Passe o mouse sobre a **visão geral** para ver uma captura de tela de como a página procurou durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="da2bf-409">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="da2bf-410">A **visão geral** é a seção que contém os gráficos **CPU**, **FPS**e **net** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-410">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="da2bf-411">Figura 32</span><span class="sxs-lookup"><span data-stu-id="da2bf-411">Figure 32</span></span>  
> <span data-ttu-id="da2bf-412">Visualizando uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="da2bf-412">Viewing a screenshot</span></span>  
> ![Visualizando uma captura de tela][ImageViewScreenshot]  

<span data-ttu-id="da2bf-414">Você também pode exibir capturas de tela clicando em um quadro na seção **quadros** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-414">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="da2bf-415">O DevTools exibe uma versão pequena da captura de tela na guia **Resumo** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-415">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

> ##### <span data-ttu-id="da2bf-416">Figura 33</span><span class="sxs-lookup"><span data-stu-id="da2bf-416">Figure 33</span></span>  
> <span data-ttu-id="da2bf-417">Depois de clicar no `233.9ms` quadro na seção **quadros** , a captura de tela desse quadro é exibida na guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="da2bf-417">After clicking the `233.9ms` frame in the **Frames** section, the screenshot for that frame is displayed in the **Summary** tab</span></span>  
> ![Exibir uma captura de tela na guia Resumo][ImageFrameScreenshotSummary]  

<span data-ttu-id="da2bf-419">Clique na miniatura na guia **Resumo** para ampliar a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="da2bf-419">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

> ##### <span data-ttu-id="da2bf-420">Figura 34</span><span class="sxs-lookup"><span data-stu-id="da2bf-420">Figure 34</span></span>  
> <span data-ttu-id="da2bf-421">Depois de clicar na miniatura na guia **Resumo** , o devtools amplia a captura de tela</span><span class="sxs-lookup"><span data-stu-id="da2bf-421">After clicking the thumbnail in the **Summary** tab, DevTools zooms in on the screenshot</span></span>  
> ![Ampliando uma captura de tela na guia Resumo][ImageFrameScreenshotZoom]  

### <span data-ttu-id="da2bf-423">Exibir informações de camadas</span><span class="sxs-lookup"><span data-stu-id="da2bf-423">View layers information</span></span>   

<span data-ttu-id="da2bf-424">Para exibir as informações de camadas avançadas sobre um quadro:</span><span class="sxs-lookup"><span data-stu-id="da2bf-424">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="da2bf-425">[Habilite a instrumentação avançada de pintura](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="da2bf-425">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="da2bf-426">Selecione um quadro na seção **quadros** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-426">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="da2bf-427">DevTools exibe informações sobre as camadas na guia novas **camadas** , ao lado da guia **log de eventos** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-427">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    > ##### <span data-ttu-id="da2bf-428">Figura 35</span><span class="sxs-lookup"><span data-stu-id="da2bf-428">Figure 35</span></span>  
    > <span data-ttu-id="da2bf-429">O painel **camadas**</span><span class="sxs-lookup"><span data-stu-id="da2bf-429">The **Layers** pane</span></span>  
    > ![O painel camadas][ImageLayers]  
    
<span data-ttu-id="da2bf-431">Passe o mouse sobre uma camada para realçá-la no diagrama.</span><span class="sxs-lookup"><span data-stu-id="da2bf-431">Hover over a layer to highlight it in the diagram.</span></span>  

> ##### <span data-ttu-id="da2bf-432">Figura 36</span><span class="sxs-lookup"><span data-stu-id="da2bf-432">Figure 36</span></span>  
> <span data-ttu-id="da2bf-433">Realçando **#39** de camada</span><span class="sxs-lookup"><span data-stu-id="da2bf-433">Highlighting layer **#39**</span></span>  
> ![Realçando uma camada][ImageLayerHover]  

<span data-ttu-id="da2bf-435">Para mover o diagrama:</span><span class="sxs-lookup"><span data-stu-id="da2bf-435">To move the diagram:</span></span>  

*   <span data-ttu-id="da2bf-436">Clique **em modo panorâmico panorâmico** ![ ][ImagePanModeIcon] para mover-se pelos eixos X e Y.</span><span class="sxs-lookup"><span data-stu-id="da2bf-436">Click **Pan Mode** ![Pan Mode][ImagePanModeIcon] to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="da2bf-437">Clique **em modo de rotação** ![ do modo de rotação ][ImageRotateModeIcon] para girar ao longo do eixo Z.</span><span class="sxs-lookup"><span data-stu-id="da2bf-437">Click **Rotate Mode** ![Rotate Mode][ImageRotateModeIcon] to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="da2bf-438">Clique em **Redefinir transformação** ![ Redefinir transformação ][ImageResetTransformIcon] para redefinir o diagrama para a posição original.</span><span class="sxs-lookup"><span data-stu-id="da2bf-438">Click **Reset Transform** ![Reset Transform][ImageResetTransformIcon] to reset the diagram to the original position.</span></span>  

### <span data-ttu-id="da2bf-439">Exibir o gerador de perfil do Paint</span><span class="sxs-lookup"><span data-stu-id="da2bf-439">View paint profiler</span></span>   

<span data-ttu-id="da2bf-440">Para exibir informações avançadas sobre um evento de pintura:</span><span class="sxs-lookup"><span data-stu-id="da2bf-440">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="da2bf-441">[Habilite a instrumentação avançada de pintura](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="da2bf-441">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="da2bf-442">Selecione um evento de **pintura** na seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-442">Select a **Paint** event in the **Main** section.</span></span>  
    
    > ##### <span data-ttu-id="da2bf-443">Figura 37</span><span class="sxs-lookup"><span data-stu-id="da2bf-443">Figure 37</span></span>  
    > <span data-ttu-id="da2bf-444">A guia **perfil do Paint**</span><span class="sxs-lookup"><span data-stu-id="da2bf-444">The **Paint Profiler** tab</span></span>  
    > ![A guia perfil do Paint][ImagePaintProfiler]  
    
## <span data-ttu-id="da2bf-446">Analisar o desempenho de renderização com a guia renderização</span><span class="sxs-lookup"><span data-stu-id="da2bf-446">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="da2bf-447">Use os recursos da guia **renderização** para ajudar a visualizar o desempenho de renderização da página.</span><span class="sxs-lookup"><span data-stu-id="da2bf-447">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="da2bf-448">Para abrir a guia **renderização** :</span><span class="sxs-lookup"><span data-stu-id="da2bf-448">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="da2bf-449">[Abrir o menu de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="da2bf-449">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="da2bf-450">Comece a digitar `Rendering` e selecione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="da2bf-450">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="da2bf-451">DevTools exibe a guia **renderização** na parte inferior da janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="da2bf-451">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    > ##### <span data-ttu-id="da2bf-452">Figura 38</span><span class="sxs-lookup"><span data-stu-id="da2bf-452">Figure 38</span></span>  
    > <span data-ttu-id="da2bf-453">A guia **renderização**</span><span class="sxs-lookup"><span data-stu-id="da2bf-453">The **Rendering** tab</span></span>  
    > ![A guia renderização][ImageRenderingTab]  
    
### <span data-ttu-id="da2bf-455">Exibir quadros por segundo em tempo real com o medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="da2bf-455">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="da2bf-456">O **medidor de FPS** é uma sobreposição que aparece no canto superior direito do seu visor.</span><span class="sxs-lookup"><span data-stu-id="da2bf-456">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="da2bf-457">Ele fornece uma estimativa em tempo real de FPS à medida que a página é executada.</span><span class="sxs-lookup"><span data-stu-id="da2bf-457">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="da2bf-458">Para abrir o **medidor de FPS**:</span><span class="sxs-lookup"><span data-stu-id="da2bf-458">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="da2bf-459">Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="da2bf-459">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="da2bf-460">Habilitar a caixa de seleção **meter de FPS** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-460">Enable the **FPS Meter** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="da2bf-461">Figura 39</span><span class="sxs-lookup"><span data-stu-id="da2bf-461">Figure 39</span></span>  
    > <span data-ttu-id="da2bf-462">O medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="da2bf-462">The FPS meter</span></span>  
    > ![O medidor de FPS][ImageFpsMeter]  
    
### <span data-ttu-id="da2bf-464">Exibir eventos de pintura em tempo real com o Paint piscando</span><span class="sxs-lookup"><span data-stu-id="da2bf-464">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="da2bf-465">Use o Paint para obter uma exibição em tempo real de todos os eventos de pintura na página.</span><span class="sxs-lookup"><span data-stu-id="da2bf-465">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="da2bf-466">Sempre que uma parte da página é pintada novamente, o DevTools descreve essa seção em verde.</span><span class="sxs-lookup"><span data-stu-id="da2bf-466">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="da2bf-467">Para habilitar a intermitência de tinta:</span><span class="sxs-lookup"><span data-stu-id="da2bf-467">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="da2bf-468">Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="da2bf-468">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="da2bf-469">Habilitar a caixa de seleção **pintura em intermitência** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-469">Enable the **Paint Flashing** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="da2bf-470">Figura 40</span><span class="sxs-lookup"><span data-stu-id="da2bf-470">Figure 40</span></span>  
    > **<span data-ttu-id="da2bf-471">Pintura em intermitência</span><span class="sxs-lookup"><span data-stu-id="da2bf-471">Paint Flashing</span></span>**  
    > ![Pintura em intermitência][ImagePaintFlashing]  
    
### <span data-ttu-id="da2bf-473">Exibir uma sobreposição de camadas com bordas de camada</span><span class="sxs-lookup"><span data-stu-id="da2bf-473">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="da2bf-474">Use **bordas de camada** para exibir uma sobreposição de bordas de camada e blocos na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="da2bf-474">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="da2bf-475">Para habilitar bordas de camada:</span><span class="sxs-lookup"><span data-stu-id="da2bf-475">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="da2bf-476">Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="da2bf-476">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="da2bf-477">Habilitar a caixa de seleção **bordas de camada** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-477">Enable the **Layer Borders** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="da2bf-478">Figura 41</span><span class="sxs-lookup"><span data-stu-id="da2bf-478">Figure 41</span></span>  
    > **<span data-ttu-id="da2bf-479">Bordas de camada</span><span class="sxs-lookup"><span data-stu-id="da2bf-479">Layer Borders</span></span>**  
    > ![Bordas de camada][ImageLayerBorders]  
    
<span data-ttu-id="da2bf-481">Veja os comentários em [`debug_colors.cc`][ChromiumDebugColors] para obter uma explicação das codificações de cores.</span><span class="sxs-lookup"><span data-stu-id="da2bf-481">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="da2bf-482">Encontrar problemas de desempenho de rolagem em tempo real</span><span class="sxs-lookup"><span data-stu-id="da2bf-482">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="da2bf-483">Use problemas de desempenho de rolagem para identificar elementos da página que têm ouvintes de eventos relacionados a rolagem que podem danificar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="da2bf-483">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="da2bf-484">DevTools descreve os elementos que podem ser problemáticos em azul-petróleo.</span><span class="sxs-lookup"><span data-stu-id="da2bf-484">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="da2bf-485">Para ver os problemas de desempenho de rolagem:</span><span class="sxs-lookup"><span data-stu-id="da2bf-485">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="da2bf-486">Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="da2bf-486">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="da2bf-487">Habilitar a caixa de seleção de **problemas de desempenho de rolagem** .</span><span class="sxs-lookup"><span data-stu-id="da2bf-487">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
 
    > ##### <span data-ttu-id="da2bf-488">Figura 42</span><span class="sxs-lookup"><span data-stu-id="da2bf-488">Figure 42</span></span>  
    > <span data-ttu-id="da2bf-489">Os **problemas de desempenho de rolagem** indicam que os objetos restritos de não-camada podem danificar o desempenho de rolagem</span><span class="sxs-lookup"><span data-stu-id="da2bf-489">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    > ![Os problemas de desempenho de rolagem indicam que os objetos restritos de não-camada podem danificar o desempenho de rolagem][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Figura 1: gravar"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Figura 2: página de atualização"  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Figura 3: uma gravação de carregamento de página"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Figura 4: caixa de seleção capturas de tela"  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Figura 5: coletar lixo"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Figura 6: seção de configurações de captura"  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Figura 7: um exemplo de uma gravação quando exemplos de JS são desabilitados"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Figura 8: um exemplo de uma gravação quando os exemplos de JS estão habilitados"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Figura 9: salvar perfil"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Figura 10: carregar perfil"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Figura 11: limpar a gravação"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Figura 12: arrastando o mouse pela visão geral para aplicar zoom"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Figura 13: caixa de pesquisa"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Figura 14: seção principal"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Figura 15: mais informações sobre a função anônimo na guia Resumo"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Figura 16: um gráfico de chama"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Figura 17: guia da árvore de chamadas"  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Figura 18: a guia de baixo para cima"  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "Figura 19: a guia log de eventos"  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Figura 20: seção GPU"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Figura 21: a seção de rasterização"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Figura 22: seção interações"  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Figura 23: o gráfico de FPS"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Figura 24: passando o mouse sobre um quadro"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Figura 25: exibindo um quadro na guia Resumo"  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Figura 26: seção rede"  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Figura 27: representação de barra de linhas da solicitação www.bing.com"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Figura 28: seção Network"  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Figura 29: a caixa de seleção memória"  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Figura 30: métricas de memória"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Figura 31: exibindo a duração de uma parte de uma gravação"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Figura 32: exibindo uma captura de tela"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Figura 33: exibindo uma captura de tela na guia Resumo"  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Figura 34: ampliando uma captura de tela na guia Resumo"  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Figura 35: o painel camadas"  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Figura 36: realçando uma camada"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Figura 37: a guia do criador de perfil do Paint"  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Figura 38: a guia renderização"  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Figura 39: o medidor de FPS"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Figura 40: pintura em intermitência"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Figura 41: bordas da camada"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Figura 42: problemas de desempenho de rolagem indica que os objetos que não se enlimitadas de viewport-Layer podem danificar o desempenho de rolagem"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Abrir o menu de comandos-executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Comece a analisar o desempenho do tempo de execução"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demonstração de guias de atividades"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. CC-pesquisa de código"  

> [!NOTE]
> <span data-ttu-id="da2bf-538">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="da2bf-538">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="da2bf-539">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="da2bf-539">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="da2bf-541">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="da2bf-541">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
