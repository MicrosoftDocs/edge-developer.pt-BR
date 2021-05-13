---
description: Saiba como avaliar o desempenho do tempo de execução Microsoft Edge DevTools.
title: Começar a analisar o desempenho do Tempo de Execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f40f23c4ac9fcc0bb0186ddb96956f691890c0c0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564270"
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
# <a name="get-started-with-analyzing-runtime-performance"></a><span data-ttu-id="a62b8-104">Começar a analisar o desempenho do Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="a62b8-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="a62b8-105">Para saber como fazer suas páginas carregarem mais rapidamente, navegue até [Otimizar a Velocidade do Site.][DevtoolsSpeedGetStarted]</span><span class="sxs-lookup"><span data-stu-id="a62b8-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="a62b8-106">O desempenho do tempo de execução é o desempenho da sua página durante a execução, em vez de carregar.</span><span class="sxs-lookup"><span data-stu-id="a62b8-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="a62b8-107">O artigo do tutorial a seguir ensina como usar o painel Microsoft Edge Desempenho do DevTools para analisar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a62b8-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="a62b8-108">Em termos do modelo **RAIL,** as habilidades que você aprender neste tutorial são úteis para analisar as fases resposta, animação e ociosidade da sua página.</span><span class="sxs-lookup"><span data-stu-id="a62b8-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a><span data-ttu-id="a62b8-109">Introdução</span><span class="sxs-lookup"><span data-stu-id="a62b8-109">Get started</span></span>  

<span data-ttu-id="a62b8-110">No tutorial a seguir, você abre o DevTools em uma página ao vivo e usa o painel Desempenho para encontrar um a gargalo de desempenho na página. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a62b8-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="a62b8-111">Abra Microsoft Edge no **modo InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="a62b8-112">O Modo InPrivate garante que Microsoft Edge seja executado em um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="a62b8-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="a62b8-113">Por exemplo, se você tiver muitas extensões instaladas, as extensões poderão criar ruído em suas medidas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a62b8-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="a62b8-114">Carregue a página a seguir na janela InPrivate.</span><span class="sxs-lookup"><span data-stu-id="a62b8-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="a62b8-115">A página é a demonstração que você vai perfilar.</span><span class="sxs-lookup"><span data-stu-id="a62b8-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="a62b8-116">A página mostra um monte de pequenos ícones movendo para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="a62b8-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="a62b8-117">Selecione `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` ou \(macOS\) para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="a62b8-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="A demonstração à esquerda e o DevTools à direita" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="a62b8-119">A demonstração à esquerda e o DevTools à direita</span><span class="sxs-lookup"><span data-stu-id="a62b8-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="a62b8-120">Para o restante dos números, o DevTools é desfazido para uma janela [separada][DevtoolsCustomizePlacement] para se concentrar melhor no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a62b8-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <a name="simulate-a-mobile-cpu"></a><span data-ttu-id="a62b8-121">Simular uma CPU móvel</span><span class="sxs-lookup"><span data-stu-id="a62b8-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="a62b8-122">Os dispositivos móveis têm muito menos energia da CPU do que desktops e laptops.</span><span class="sxs-lookup"><span data-stu-id="a62b8-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="a62b8-123">Sempre que você perfilar uma página, use a Throttling da CPU para simular o desempenho da sua página em dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="a62b8-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="a62b8-124">No DevTools, escolha a **ferramenta Performance.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-124">In DevTools, choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="a62b8-125">Certifique-se de escolher a caixa de seleção ao lado **de Capturas de Tela**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-125">Ensure the you choose the checkbox next to **Screenshots**.</span></span>  
1.  <span data-ttu-id="a62b8-126">Escolha **Capturar Configurações** \( Capture Configurações ![ ](../media/capture-settings-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="a62b8-126">Choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\).</span></span>  <span data-ttu-id="a62b8-127">O DevTools revela configurações relacionadas à forma como captura métricas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a62b8-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="a62b8-128">Para **CPU,** escolha **4x de lentidão**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="a62b8-129">O DevTools acelera sua CPU para que ela seja 4 vezes mais lenta do que o normal.</span><span class="sxs-lookup"><span data-stu-id="a62b8-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Aceleração da CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="a62b8-131">Aceleração da CPU</span><span class="sxs-lookup"><span data-stu-id="a62b8-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="a62b8-132">Ao testar outras páginas; se você quiser garantir que cada página funcione bem em dispositivos móveis de baixo nível, de definir a velocidade da CPU como **6x de lentidão**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="a62b8-133">A demonstração não funciona bem com a lentidão de 6x, portanto, ela usa apenas 4x de lentidão para fins instrucionais.</span><span class="sxs-lookup"><span data-stu-id="a62b8-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <a name="set-up-the-demo"></a><span data-ttu-id="a62b8-134">Configurar a demonstração</span><span class="sxs-lookup"><span data-stu-id="a62b8-134">Set up the demo</span></span>  

<span data-ttu-id="a62b8-135">É difícil criar uma demonstração de desempenho de tempo de execução que funcione de forma consistente para todos os leitores do site.</span><span class="sxs-lookup"><span data-stu-id="a62b8-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="a62b8-136">A seção a seguir permite personalizar a demonstração para garantir que sua experiência seja relativamente consistente com as capturas de tela e as descrições, independentemente da configuração específica.</span><span class="sxs-lookup"><span data-stu-id="a62b8-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="a62b8-137">Escolha o **botão Adicionar 10** até que os ícones azuis se movam visivelmente mais lentos do que antes.</span><span class="sxs-lookup"><span data-stu-id="a62b8-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="a62b8-138">Em um computador high-end, você pode escolher isso cerca de 20 vezes.</span><span class="sxs-lookup"><span data-stu-id="a62b8-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="a62b8-139">Escolha **Otimizar**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-139">Choose **Optimize**.</span></span>  <span data-ttu-id="a62b8-140">Os ícones azuis devem ser mais rápidos e suaves.</span><span class="sxs-lookup"><span data-stu-id="a62b8-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a62b8-141">Para exibir melhor uma diferença entre as versões otimizadas e não otimizadas, escolha o botão **Subtrair 10** algumas vezes e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="a62b8-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="a62b8-142">Se você adicionar muitos ícones azuis, poderá aumentar a CPU e, em seguida, não observar uma grande diferença nos resultados das duas versões.</span><span class="sxs-lookup"><span data-stu-id="a62b8-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="a62b8-143">Escolha **Não Otimizar**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="a62b8-144">Os ícones azuis são mais lentos e com mais lentidão novamente.</span><span class="sxs-lookup"><span data-stu-id="a62b8-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <a name="record-runtime-performance"></a><span data-ttu-id="a62b8-145">Registrar o desempenho do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="a62b8-145">Record runtime performance</span></span>  

<span data-ttu-id="a62b8-146">Quando você correu a versão otimizada da página, os ícones azuis são mais rápidos.</span><span class="sxs-lookup"><span data-stu-id="a62b8-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="a62b8-147">Por que isso?</span><span class="sxs-lookup"><span data-stu-id="a62b8-147">Why is that?</span></span>  <span data-ttu-id="a62b8-148">Ambas as versões devem mover os ícones da mesma quantidade de espaço no mesmo período de tempo.</span><span class="sxs-lookup"><span data-stu-id="a62b8-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="a62b8-149">Leve uma gravação no painel Desempenho para saber como detectar o a gargalo de desempenho na versão não otimizada.</span><span class="sxs-lookup"><span data-stu-id="a62b8-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="a62b8-150">Em DevTools, escolha **Gravar** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="a62b8-150">In DevTools, choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  <span data-ttu-id="a62b8-151">O DevTools captura métricas de desempenho à medida que a página é executado.</span><span class="sxs-lookup"><span data-stu-id="a62b8-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Perfil da página" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="a62b8-153">Perfil da página</span><span class="sxs-lookup"><span data-stu-id="a62b8-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a62b8-154">Aguarde alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="a62b8-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="a62b8-155">Escolha **Parar**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-155">Choose **Stop**.</span></span>  <span data-ttu-id="a62b8-156">O DevTools interrompe a gravação, processa os dados e exibe os resultados no painel Desempenho.</span><span class="sxs-lookup"><span data-stu-id="a62b8-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Os resultados do perfil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="a62b8-158">Os resultados do perfil</span><span class="sxs-lookup"><span data-stu-id="a62b8-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="a62b8-159">Uau, isso é uma quantidade avassaladora de dados.</span><span class="sxs-lookup"><span data-stu-id="a62b8-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="a62b8-160">não se preocupe, em breve o processo faz mais sentido.</span><span class="sxs-lookup"><span data-stu-id="a62b8-160">do not worry, soon the process makes more sense.</span></span>  

## <a name="analyze-the-results"></a><span data-ttu-id="a62b8-161">Analisar os resultados</span><span class="sxs-lookup"><span data-stu-id="a62b8-161">Analyze the results</span></span>  

<span data-ttu-id="a62b8-162">Depois de registrar o desempenho da página, mede a qualidade do desempenho da página e encontre as causas.</span><span class="sxs-lookup"><span data-stu-id="a62b8-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <a name="analyze-frames-per-second"></a><span data-ttu-id="a62b8-163">Analisar quadros por segundo</span><span class="sxs-lookup"><span data-stu-id="a62b8-163">Analyze frames per second</span></span>  

<span data-ttu-id="a62b8-164">A métrica principal para medir o desempenho de qualquer animação são quadros por segundo \(FPS\).</span><span class="sxs-lookup"><span data-stu-id="a62b8-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="a62b8-165">Os usuários ficam felizes quando as animações são executados em 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="a62b8-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="a62b8-166">Revise o **gráfico FPS.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-166">Review the **FPS** chart.</span></span>  <span data-ttu-id="a62b8-167">Sempre que uma barra vermelha é exibida acima **do FPS**, isso significa que a taxa de quadros caiu tão baixo que provavelmente está prejudicando a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="a62b8-167">Whenever a red bar is displayed above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="a62b8-168">Em geral, quanto maior for a barra verde, maior será o FPS.</span><span class="sxs-lookup"><span data-stu-id="a62b8-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="O gráfico FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="a62b8-170">O **gráfico FPS**</span><span class="sxs-lookup"><span data-stu-id="a62b8-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a62b8-171">Abaixo do **gráfico FPS,** o **gráfico de CPU** é exibido.</span><span class="sxs-lookup"><span data-stu-id="a62b8-171">Below the **FPS** chart, the **CPU** chart is displayed.</span></span>  <span data-ttu-id="a62b8-172">As cores no **gráfico da CPU** correspondem às cores no painel **Resumo,** na parte inferior do painel Desempenho.</span><span class="sxs-lookup"><span data-stu-id="a62b8-172">The colors in the **CPU** chart correspond to the colors in the **Summary** panel, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="a62b8-173">O fato de que o **gráfico da CPU** está cheio de cores significa que a CPU foi maxed para fora durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="a62b8-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="a62b8-174">Sempre que a CPU tiver um tempo máximo máximo por longos períodos, é um indicador de que você deve encontrar maneiras de fazer menos trabalho.</span><span class="sxs-lookup"><span data-stu-id="a62b8-174">Whenever the CPU maxed out for long periods, it is an indicator that you should find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="O gráfico da CPU e o painel Resumo" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="a62b8-176">O **gráfico da CPU** e o painel **Resumo**</span><span class="sxs-lookup"><span data-stu-id="a62b8-176">The **CPU** chart and **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a62b8-177">Passe o mouse nos **gráficos FPS,** **CPU**ou **NET.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="a62b8-178">DevTools mostra uma captura de tela da página nesse ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="a62b8-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="a62b8-179">Mova o mouse para a esquerda e para a direita para repetir a gravação.</span><span class="sxs-lookup"><span data-stu-id="a62b8-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="a62b8-180">A ação é referenciada como limpeza e é útil para analisar manualmente a progressão das animações.</span><span class="sxs-lookup"><span data-stu-id="a62b8-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Exibir uma captura de tela da página em torno da marca de 2500ms da gravação" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="a62b8-182">Exibir uma captura de tela da página em torno da marca de 2500ms da gravação</span><span class="sxs-lookup"><span data-stu-id="a62b8-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a62b8-183">Na seção **Quadros,** passe o mouse em um dos quadrados verdes.</span><span class="sxs-lookup"><span data-stu-id="a62b8-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="a62b8-184">DevTools mostra o FPS para esse quadro específico.</span><span class="sxs-lookup"><span data-stu-id="a62b8-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="a62b8-185">Cada quadro provavelmente está bem abaixo do destino de 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="a62b8-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Passar o mouse em um quadro" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="a62b8-187">Passar o mouse em um quadro</span><span class="sxs-lookup"><span data-stu-id="a62b8-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="a62b8-188">Obviamente, a exibição indica que a página da Web não está com bom desempenho.</span><span class="sxs-lookup"><span data-stu-id="a62b8-188">Of course, the display indicates that the webpage is not performing well.</span></span>  <span data-ttu-id="a62b8-189">Mas, em cenários reais, pode não ser tão claro, portanto, ter todas as ferramentas para fazer medições é útil.</span><span class="sxs-lookup"><span data-stu-id="a62b8-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <a name="bonus-open-the-fps-meter"></a><span data-ttu-id="a62b8-190">Bônus: Abra o medidor FPS</span><span class="sxs-lookup"><span data-stu-id="a62b8-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="a62b8-191">Outra ferramenta útil é o medidor FPS, que fornece estimativas em tempo real para FPS à medida que a página é executado.</span><span class="sxs-lookup"><span data-stu-id="a62b8-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="a62b8-192">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="a62b8-193">Comece a digitar `Rendering` no Menu de Comando **e** escolha **Mostrar Renderização**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="a62b8-194">Na ferramenta **Renderização,** a turn on **FPS Meter**.</span><span class="sxs-lookup"><span data-stu-id="a62b8-194">In the **Rendering** tool, turn on **FPS Meter**.</span></span>  <span data-ttu-id="a62b8-195">Uma nova sobreposição aparece na parte superior direita do seu viewport.</span><span class="sxs-lookup"><span data-stu-id="a62b8-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="O medidor FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="a62b8-197">O **medidor FPS**</span><span class="sxs-lookup"><span data-stu-id="a62b8-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="a62b8-198">Desligue o **Medidor de FPS e** selecione para fechar a ferramenta `Escape` **Rendering.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-198">Turn off the **FPS Meter** and select `Escape` to close the **Rendering** tool.</span></span>  <span data-ttu-id="a62b8-199">Você não está usando **o Medidor FPS** neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="a62b8-199">You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <a name="find-the-bottleneck"></a><span data-ttu-id="a62b8-200">Encontre o a gargalo</span><span class="sxs-lookup"><span data-stu-id="a62b8-200">Find the bottleneck</span></span>  

<span data-ttu-id="a62b8-201">Depois de medir e verificar se a animação não está bem, a próxima etapa é responder à pergunta "por quê?".</span><span class="sxs-lookup"><span data-stu-id="a62b8-201">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="a62b8-202">Quando nenhum evento é escolhido, o painel **Resumo** mostra uma divisão de atividades.</span><span class="sxs-lookup"><span data-stu-id="a62b8-202">When no events are chosen, the **Summary** panel shows you a breakdown of activity.</span></span>  <span data-ttu-id="a62b8-203">A página passou a maior parte do tempo renderização.</span><span class="sxs-lookup"><span data-stu-id="a62b8-203">The page spent most of the time rendering.</span></span>  <span data-ttu-id="a62b8-204">Como o desempenho é a arte de fazer menos trabalho, seu objetivo é reduzir o tempo gasto fazendo trabalho de renderização.</span><span class="sxs-lookup"><span data-stu-id="a62b8-204">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="O painel Resumo" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="a62b8-206">O **painel Resumo**</span><span class="sxs-lookup"><span data-stu-id="a62b8-206">The **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a62b8-207">Expanda **a seção** Principal.</span><span class="sxs-lookup"><span data-stu-id="a62b8-207">Expand the **Main** section.</span></span>  <span data-ttu-id="a62b8-208">DevTools mostra um gráfico de chama de atividade no thread principal, com o tempo.</span><span class="sxs-lookup"><span data-stu-id="a62b8-208">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="a62b8-209">O eixo x representa a gravação, com o passar do tempo.</span><span class="sxs-lookup"><span data-stu-id="a62b8-209">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="a62b8-210">Cada barra representa um evento.</span><span class="sxs-lookup"><span data-stu-id="a62b8-210">Each bar represents an event.</span></span>  <span data-ttu-id="a62b8-211">Uma barra mais ampla significa que o evento demorou mais.</span><span class="sxs-lookup"><span data-stu-id="a62b8-211">A wider bar means that event took longer.</span></span>  <span data-ttu-id="a62b8-212">O eixo y representa a pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="a62b8-212">The y-axis represents the call stack.</span></span>  <span data-ttu-id="a62b8-213">Quando os eventos são empilhados uns sobre os outros, isso significa que os eventos superiores causaram os eventos inferiores.</span><span class="sxs-lookup"><span data-stu-id="a62b8-213">When events are stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="A seção Principal" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="a62b8-215">A **seção** Principal</span><span class="sxs-lookup"><span data-stu-id="a62b8-215">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a62b8-216">Há muitos dados na gravação.</span><span class="sxs-lookup"><span data-stu-id="a62b8-216">There is a lot of data in the recording.</span></span>  <span data-ttu-id="a62b8-217">Para ampliar em um único evento; escolha, segure e arraste o cursor sobre a Visão Geral **,** que é a seção que inclui os gráficos **FPS,** **CPU**e **NET.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-217">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="a62b8-218">A **seção Principal** e **o** painel Resumo exibem apenas informações para a parte escolhida da gravação.</span><span class="sxs-lookup"><span data-stu-id="a62b8-218">The **Main** section and **Summary** panel only display information for the chosen portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Ampliar em um evento" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="a62b8-220">Ampliar em um evento</span><span class="sxs-lookup"><span data-stu-id="a62b8-220">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="a62b8-221">Outra maneira de ampliar, focalizar a **seção Principal,** escolher o plano de fundo ou um evento e `W` selecionar , , ou `A` `S` `D` .</span><span class="sxs-lookup"><span data-stu-id="a62b8-221">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="a62b8-222">Concentre-se no triângulo vermelho no canto superior direito do **evento Animation Frame Fired.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-222">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="a62b8-223">Sempre que um triângulo vermelho é exibido, é um aviso de que pode haver um problema relacionado ao evento.</span><span class="sxs-lookup"><span data-stu-id="a62b8-223">Whenever a red triangle is displayed, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a62b8-224">O **evento Animation Frame Fired** ocorre sempre que um retorno de chamada [requestAnimationFrame()][MDNWebRequestAnimationFrame] é executado.</span><span class="sxs-lookup"><span data-stu-id="a62b8-224">The **Animation Frame Fired** event occurs whenever a [requestAnimationFrame() callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="a62b8-225">Escolha o **evento Animation Frame Fired.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-225">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="a62b8-226">O **painel** Resumo agora mostra informações sobre esse evento.</span><span class="sxs-lookup"><span data-stu-id="a62b8-226">The **Summary** panel now shows you information about that event.</span></span>  <span data-ttu-id="a62b8-227">Observe o link **Revelação.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-227">Note the **Reveal** link.</span></span>  <span data-ttu-id="a62b8-228">Depois de escolher, DevTools realça o evento que iniciou o **evento Animation Frame Fired.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-228">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="a62b8-229">Além disso, concentre-se **no linkapp.js:95.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-229">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="a62b8-230">Depois de escolher, a linha relevante no código-fonte será exibida.</span><span class="sxs-lookup"><span data-stu-id="a62b8-230">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Mais informações sobre o evento Animation Frame Fired" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="a62b8-232">Mais informações sobre o evento **Animation Frame Fired**</span><span class="sxs-lookup"><span data-stu-id="a62b8-232">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="a62b8-233">Depois de escolher um evento, use as teclas de seta para selecionar os eventos ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="a62b8-233">After choosing an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="a62b8-234">No evento **app.update,** há um monte de eventos roxos.</span><span class="sxs-lookup"><span data-stu-id="a62b8-234">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="a62b8-235">Se cada evento roxo era mais amplo, parece que cada um deles pode ter um triângulo vermelho nele.</span><span class="sxs-lookup"><span data-stu-id="a62b8-235">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="a62b8-236">Escolha um dos eventos **layout roxo.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-236">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="a62b8-237">O DevTools fornece mais informações sobre o evento no painel **Resumo.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-237">DevTools provides more information about the event in the **Summary** panel.</span></span>  <span data-ttu-id="a62b8-238">Na verdade, há um aviso sobre refluxos forçados \(outra palavra para layout\).</span><span class="sxs-lookup"><span data-stu-id="a62b8-238">Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="a62b8-239">No painel **Resumo,** escolha o link **app.js:71** em **Layout Forçado.**</span><span class="sxs-lookup"><span data-stu-id="a62b8-239">In the **Summary** panel, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="a62b8-240">DevTools leva você para a linha de código que força o layout.</span><span class="sxs-lookup"><span data-stu-id="a62b8-240">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="A linha de código que causou o layout forçado" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="a62b8-242">A linha de código que causou o layout forçado</span><span class="sxs-lookup"><span data-stu-id="a62b8-242">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="a62b8-243">O problema com o código é que, em cada quadro de animação, ele altera o estilo de cada ícone e consulta a posição de cada ícone na página.</span><span class="sxs-lookup"><span data-stu-id="a62b8-243">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="a62b8-244">Como os estilos foram alterados, o navegador não sabe se cada posição de ícone foi alterada, portanto, ele precisa reposicioná-lo para calcular a nova posição.</span><span class="sxs-lookup"><span data-stu-id="a62b8-244">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="a62b8-245">Isso foi muito para aprender.</span><span class="sxs-lookup"><span data-stu-id="a62b8-245">That was a lot to learn.</span></span>  <span data-ttu-id="a62b8-246">Agora você tem uma base sólida no fluxo de trabalho básico para analisar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a62b8-246">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="a62b8-247">Muito bom trabalho.</span><span class="sxs-lookup"><span data-stu-id="a62b8-247">Good job.</span></span>  

### <a name="bonus-analyze-the-optimized-version"></a><span data-ttu-id="a62b8-248">Bônus: Analisar a versão otimizada</span><span class="sxs-lookup"><span data-stu-id="a62b8-248">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="a62b8-249">Usando os fluxos de trabalho e as ferramentas que você acabou de aprender, escolha **Otimizar** na demonstração para ativar o código otimizado, fazer outra gravação de desempenho e analisar os resultados.</span><span class="sxs-lookup"><span data-stu-id="a62b8-249">Using the workflows and tools that you just learned, choose **Optimize** on the demo to turn on the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="a62b8-250">Da taxa de quadros aprimorada até a redução de eventos no gráfico de chama na seção **Principal,** a versão otimizada do aplicativo faz muito menos trabalho, resultando em melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="a62b8-250">From the improved framerate to the reduction in events in the flame chart in the **Main** section, the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="a62b8-251">Mesmo a versão otimizada não é ótima, pois manipula a `top` propriedade de cada ícone.</span><span class="sxs-lookup"><span data-stu-id="a62b8-251">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="a62b8-252">Uma abordagem melhor é manter as propriedades que afetam apenas a composição.</span><span class="sxs-lookup"><span data-stu-id="a62b8-252">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a><span data-ttu-id="a62b8-253">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a62b8-253">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

<span data-ttu-id="a62b8-254">Para ficar mais confortável com a **ferramenta Performance,** a prática torna perfeito.</span><span class="sxs-lookup"><span data-stu-id="a62b8-254">To get more comfortable with the **Performance** tool, practice makes perfect.</span></span>  <span data-ttu-id="a62b8-255">Tente perfilar suas páginas e analisar os resultados.</span><span class="sxs-lookup"><span data-stu-id="a62b8-255">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="a62b8-256">Se você tiver alguma dúvida sobre seus resultados, use o ícone Enviar **Comentários,** selecione `Alt` + `Shift` + `I` \(Windows, Linux\), selecione `Option` + `Shift` + `I` \(macOS\) ou tweet a equipe [DevTools][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="a62b8-256">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="a62b8-257">Inclua capturas de tela ou links para páginas reprodutíveis, se possível.</span><span class="sxs-lookup"><span data-stu-id="a62b8-257">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="O ícone **Feedback** no Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="a62b8-259">O **ícone Enviar Comentários** no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a62b8-259">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="a62b8-260">Por fim, há muitas maneiras de melhorar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a62b8-260">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="a62b8-261">Este artigo se concentrou em um a gargalo de animação específico para dar a você um tour focado pelo painel Desempenho, mas é apenas um dos muitos gargalos que você pode encontrar.</span><span class="sxs-lookup"><span data-stu-id="a62b8-261">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a62b8-262">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a62b8-262">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Alterar Microsoft Edge posicionamento do DevTools (Desfazer, Encaixar na Parte Inferior, Doca para a Esquerda)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Otimizar a velocidade do site com Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools - Postar um tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\(\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> <span data-ttu-id="a62b8-267">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a62b8-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a62b8-268">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="a62b8-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a62b8-270">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a62b8-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
