---
title: Comece a analisar o desempenho do tempo de execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611738"
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







# <span data-ttu-id="7fc86-103">Comece a analisar o desempenho do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="7fc86-103">Get Started With Analyzing Runtime Performance</span></span>   



> [!NOTE]
> <span data-ttu-id="7fc86-104">Consulte [otimizar a velocidade do site][DevtoolsSpeedGetStarted] para aprender a fazer com que suas páginas sejam carregadas mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="7fc86-104">See [Optimize Website Speed][DevtoolsSpeedGetStarted] to learn how to make your pages load faster.</span></span>  

<span data-ttu-id="7fc86-105">O desempenho do tempo de execução é a forma como a sua página é executada, em oposição ao carregamento.</span><span class="sxs-lookup"><span data-stu-id="7fc86-105">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="7fc86-106">Este tutorial ensina a usar o painel de desempenho do Microsoft Edge DevTools para analisar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7fc86-106">This tutorial teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="7fc86-107">Em termos do modelo de **trilho** , as habilidades que você aprende neste tutorial são úteis para analisar a resposta, a animação e as fases ociosas da página.</span><span class="sxs-lookup"><span data-stu-id="7fc86-107">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="7fc86-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="7fc86-108">Get started</span></span>   

<span data-ttu-id="7fc86-109">Neste tutorial, você abre o DevTools em uma página dinâmica e usa o painel desempenho para localizar um afunilamento de desempenho na página.</span><span class="sxs-lookup"><span data-stu-id="7fc86-109">In this tutorial, you open DevTools on a live page and use the Performance panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="7fc86-110">Abrir o Microsoft Edge no **modo InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-110">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="7fc86-111">O modo InPrivate garante que o Microsoft Edge seja executado em um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="7fc86-111">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="7fc86-112">Por exemplo, se você tiver muitas extensões instaladas, essas extensões poderão criar ruído em medidas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="7fc86-112">For example, if you have a lot of extensions installed, those extensions might create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="7fc86-113">Carregue a página a seguir na sua janela InPrivate.</span><span class="sxs-lookup"><span data-stu-id="7fc86-113">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="7fc86-114">Esta é a demonstração na qual você pretende fazer o perfil.</span><span class="sxs-lookup"><span data-stu-id="7fc86-114">This is the demo that you're going to profile.</span></span>  <span data-ttu-id="7fc86-115">A página mostra um monte de ícones pequenos em movimento para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="7fc86-115">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  <span data-ttu-id="7fc86-116">Pressione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \) para abrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="7fc86-116">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-117">Figura 1</span><span class="sxs-lookup"><span data-stu-id="7fc86-117">Figure 1</span></span>  
    > <span data-ttu-id="7fc86-118">A demonstração à esquerda e DevTools à direita</span><span class="sxs-lookup"><span data-stu-id="7fc86-118">The demo on the left, and DevTools on the right</span></span>  
    > ![A demonstração à esquerda e DevTools à direita][ImageGetStarted]  
    
    > [!NOTE]
    > <span data-ttu-id="7fc86-120">Para o restante das capturas de tela, o DevTools é [desencaixado em uma janela separada][DevtoolsCustomizePlacement] para que você possa ver o conteúdo melhor.</span><span class="sxs-lookup"><span data-stu-id="7fc86-120">For the rest of the screenshots, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] so that you can see the contents better.</span></span>  
    
### <span data-ttu-id="7fc86-121">Simular uma CPU móvel</span><span class="sxs-lookup"><span data-stu-id="7fc86-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="7fc86-122">Dispositivos móveis têm muito menos energia de CPU do que desktops e notebooks.</span><span class="sxs-lookup"><span data-stu-id="7fc86-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="7fc86-123">Sempre que você criar o perfil de uma página, use a limitação de CPU para simular como a sua página é realizada em dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="7fc86-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="7fc86-124">No DevTools, clique na guia **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-124">In DevTools, click the **Performance** tab.</span></span>  
1.  <span data-ttu-id="7fc86-125">Verifique se a caixa de seleção **capturas de tela** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7fc86-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="7fc86-126">Clique em capturar configurações de captura de **configurações** ![ ][ImageCaptureSettingsIcon] .</span><span class="sxs-lookup"><span data-stu-id="7fc86-126">Click **Capture Settings** ![Capture Settings][ImageCaptureSettingsIcon].</span></span>  <span data-ttu-id="7fc86-127">DevTools revela configurações relacionadas à maneira como ele captura métricas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="7fc86-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="7fc86-128">Para **CPU**, selecione **4x lentidão**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-128">For **CPU**, select **4x slowdown**.</span></span>  <span data-ttu-id="7fc86-129">O DevTools acelera a CPU para que seja 4 vezes mais lento do que o normal.</span><span class="sxs-lookup"><span data-stu-id="7fc86-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-130">Figura 2</span><span class="sxs-lookup"><span data-stu-id="7fc86-130">Figure 2</span></span>  
    > <span data-ttu-id="7fc86-131">Aceleração da CPU</span><span class="sxs-lookup"><span data-stu-id="7fc86-131">CPU throttling</span></span>  
    > ![Aceleração da CPU][ImageCPUThrottling]  
    
    > [!NOTE]
    > <span data-ttu-id="7fc86-133">Ao testar outras páginas, se você quiser garantir que elas funcionem bem em dispositivos móveis low-end, defina a limitação de CPU para **6x a lentidão**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-133">When testing other pages, if you want to ensure that they work well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="7fc86-134">Esta demonstração não funciona bem com 6X de lentidão, portanto, ele simplesmente usa 4 vezes de lentidão para fins de instrução.</span><span class="sxs-lookup"><span data-stu-id="7fc86-134">This demo doesn't work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="7fc86-135">Configurar a demonstração</span><span class="sxs-lookup"><span data-stu-id="7fc86-135">Set up the demo</span></span>  

<span data-ttu-id="7fc86-136">É difícil criar uma demonstração de desempenho do tempo de execução que funcione consistentemente para todos os leitores deste site.</span><span class="sxs-lookup"><span data-stu-id="7fc86-136">It is hard to create a runtime performance demo that works consistently for all readers of this website.</span></span>  <span data-ttu-id="7fc86-137">Esta seção permite que você personalize a demonstração para garantir que sua experiência seja relativamente consistente com as capturas de tela e descrições que você vê neste tutorial, independentemente de sua configuração específica.</span><span class="sxs-lookup"><span data-stu-id="7fc86-137">This section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions you see in this tutorial, regardless of your particular setup.</span></span>

1.  <span data-ttu-id="7fc86-138">Continue clicando em **Adicionar 10** até que os ícones azuis se movimentem visivelmente mais devagar do que antes.</span><span class="sxs-lookup"><span data-stu-id="7fc86-138">Keep clicking **Add 10** until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="7fc86-139">Em um computador high-end, pode demorar cerca de 20 cliques.</span><span class="sxs-lookup"><span data-stu-id="7fc86-139">On a high-end machine, it may take about 20 clicks.</span></span>  
1.  <span data-ttu-id="7fc86-140">Clique em **otimizar**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-140">Click **Optimize**.</span></span>  <span data-ttu-id="7fc86-141">Os ícones azuis devem se mover de forma mais rápida e mais suave.</span><span class="sxs-lookup"><span data-stu-id="7fc86-141">The blue icons should move faster and more smoothly.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="7fc86-142">Se você não vir uma diferença perceptível entre as versões otimizadas e não otimizadas, tente clicar em **subtrair 10** algumas vezes e tentar novamente.</span><span class="sxs-lookup"><span data-stu-id="7fc86-142">If you don't see a noticeable difference between the optimized and un-optimized versions, try clicking **Subtract 10** a few times and trying again.</span></span>  
    > <span data-ttu-id="7fc86-143">Se você adicionar muitos ícones azuis, terá apenas a versão máxima da CPU e não verá uma diferença importante nos resultados das duas versões (em inglês).</span><span class="sxs-lookup"><span data-stu-id="7fc86-143">If you add too many blue icons, you're just going to max out the CPU and you're not going to see a major difference in the results for the two versions.</span></span>  

1.  <span data-ttu-id="7fc86-144">Clique em **desfazer**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-144">Click **Un-Optimize**.</span></span>  <span data-ttu-id="7fc86-145">Os ícones azuis se movem mais lentos e com mais Jank.</span><span class="sxs-lookup"><span data-stu-id="7fc86-145">The blue icons move slower and with more jank again.</span></span>  

### <span data-ttu-id="7fc86-146">Desempenho do registro em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="7fc86-146">Record runtime performance</span></span>   

<span data-ttu-id="7fc86-147">Quando você executou a versão otimizada da página, os ícones azuis são movidos mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="7fc86-147">When you ran the optimized version of the page, the blue icons move faster.</span></span>  
<span data-ttu-id="7fc86-148">Por quê?</span><span class="sxs-lookup"><span data-stu-id="7fc86-148">Why is that?</span></span>  <span data-ttu-id="7fc86-149">Ambas as versões devem mover os ícones da mesma quantidade de espaço na mesma quantidade de tempo.</span><span class="sxs-lookup"><span data-stu-id="7fc86-149">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="7fc86-150">Faça uma gravação no painel desempenho para aprender a detectar o afunilamento de desempenho na versão desotimizada.</span><span class="sxs-lookup"><span data-stu-id="7fc86-150">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="7fc86-151">No DevTools, clique em **gravar** ![ registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="7fc86-151">In DevTools, click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="7fc86-152">DevTools captura métricas de desempenho à medida que a página é executada.</span><span class="sxs-lookup"><span data-stu-id="7fc86-152">DevTools captures performance metrics as the page runs.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-153">Figura 3</span><span class="sxs-lookup"><span data-stu-id="7fc86-153">Figure 3</span></span> 
    > <span data-ttu-id="7fc86-154">Criando o perfil da página</span><span class="sxs-lookup"><span data-stu-id="7fc86-154">Profiling the page</span></span>  
    > ![Criando o perfil da página][ImagePageProfiling]  
    
1.  <span data-ttu-id="7fc86-156">Aguarde alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="7fc86-156">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="7fc86-157">Clique em **parar**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-157">Click **Stop**.</span></span>  <span data-ttu-id="7fc86-158">DevTools interrompe a gravação, processa os dados e, em seguida, exibe os resultados no painel desempenho.</span><span class="sxs-lookup"><span data-stu-id="7fc86-158">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-159">Figura 4</span><span class="sxs-lookup"><span data-stu-id="7fc86-159">Figure 4</span></span>  
    > <span data-ttu-id="7fc86-160">Os resultados do perfil</span><span class="sxs-lookup"><span data-stu-id="7fc86-160">The results of the profile</span></span>  
    > ![Os resultados do perfil][ImageProfileResults]  

<span data-ttu-id="7fc86-162">Wow, que é um volume impressionante de dados.</span><span class="sxs-lookup"><span data-stu-id="7fc86-162">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="7fc86-163">Não se preocupe, tudo fará mais sentido em breve.</span><span class="sxs-lookup"><span data-stu-id="7fc86-163">Don't worry, it'll all make more sense shortly.</span></span>  

## <span data-ttu-id="7fc86-164">Analisar os resultados</span><span class="sxs-lookup"><span data-stu-id="7fc86-164">Analyze the results</span></span>   

<span data-ttu-id="7fc86-165">Depois de registrar o desempenho da página, você pode medir o desempenho da página e encontrar as causas possíveis e encontrar as causas mais lentas.</span><span class="sxs-lookup"><span data-stu-id="7fc86-165">Once you've got a recording the performance of the page, you can measure how poor the performance of the page is, and find the any causes.</span></span>  

### <span data-ttu-id="7fc86-166">Analisar quadros por segundo</span><span class="sxs-lookup"><span data-stu-id="7fc86-166">Analyze frames per second</span></span>  

<span data-ttu-id="7fc86-167">A principal métrica para medir o desempenho de qualquer animação é a de quadros por segundo \ (FPS \).</span><span class="sxs-lookup"><span data-stu-id="7fc86-167">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="7fc86-168">Os usuários ficam satisfeitos quando animações são executadas em 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="7fc86-168">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="7fc86-169">Examine o gráfico de **FPS** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-169">Look at the **FPS** chart.</span></span>  <span data-ttu-id="7fc86-170">Sempre que você vir uma barra vermelha acima de **FPS**, significa que a taxa de quadros ficou tão baixa que provavelmente está prejudicando a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="7fc86-170">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="7fc86-171">Em geral, quanto maior a barra verde, mais alta a FPS.</span><span class="sxs-lookup"><span data-stu-id="7fc86-171">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-172">Figura 5</span><span class="sxs-lookup"><span data-stu-id="7fc86-172">Figure 5</span></span>  
    > <span data-ttu-id="7fc86-173">O gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="7fc86-173">The FPS chart</span></span>  
    > ![O gráfico de FPS][ImageFPSChart]  

1.  <span data-ttu-id="7fc86-175">Abaixo do gráfico de **FPS** , você vê o gráfico **da CPU** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-175">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="7fc86-176">As cores do gráfico de **CPU** correspondem às cores na guia **Resumo** , na parte inferior do painel desempenho.</span><span class="sxs-lookup"><span data-stu-id="7fc86-176">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="7fc86-177">O fato de que o gráfico de **CPU** está cheio de cores significa que a CPU foi maximizada durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="7fc86-177">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="7fc86-178">Sempre que você vê a CPU esgotada durante longos períodos, é uma indicação para encontrar formas de fazer menos trabalho.</span><span class="sxs-lookup"><span data-stu-id="7fc86-178">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-179">Figura 6</span><span class="sxs-lookup"><span data-stu-id="7fc86-179">Figure 6</span></span>  
    > <span data-ttu-id="7fc86-180">A guia Resumo e gráfico da CPU</span><span class="sxs-lookup"><span data-stu-id="7fc86-180">The CPU chart and Summary tab</span></span>  
    > ![A guia Resumo e gráfico da CPU][ImageCPUSummary]  

1.  <span data-ttu-id="7fc86-182">Passe o mouse sobre os gráficos de **FPS**, **CPU**ou **rede** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-182">Hover your mouse over the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="7fc86-183">DevTools mostra uma captura de tela da página nesse momento.</span><span class="sxs-lookup"><span data-stu-id="7fc86-183">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="7fc86-184">Mova o mouse para a esquerda e para a direita para reproduzir a gravação.</span><span class="sxs-lookup"><span data-stu-id="7fc86-184">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="7fc86-185">Isso é chamado de depuração, e é útil para analisar manualmente a progressão de animações.</span><span class="sxs-lookup"><span data-stu-id="7fc86-185">This is called scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-186">Figura 7</span><span class="sxs-lookup"><span data-stu-id="7fc86-186">Figure 7</span></span>  
    > <span data-ttu-id="7fc86-187">Exibir uma captura de tela da página ao lado da marca 2500ms da gravação</span><span class="sxs-lookup"><span data-stu-id="7fc86-187">Viewing a screenshot of the page around the 2500ms mark of the recording</span></span>  
    > ![Exibir uma captura de tela da página ao lado da marca 2500ms da gravação][ImageViewingScreenshot]  

1.  <span data-ttu-id="7fc86-189">Na seção **quadros** , passe o mouse sobre um dos quadrados verdes.</span><span class="sxs-lookup"><span data-stu-id="7fc86-189">In the **Frames** section, hover your mouse over one of the green squares.</span></span>  <span data-ttu-id="7fc86-190">DevTools mostra as FPS para esse quadro específico.</span><span class="sxs-lookup"><span data-stu-id="7fc86-190">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="7fc86-191">Cada quadro provavelmente está logo abaixo do destino de 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="7fc86-191">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-192">Figura 8</span><span class="sxs-lookup"><span data-stu-id="7fc86-192">Figure 8</span></span>  
    > <span data-ttu-id="7fc86-193">Passar o mouse sobre um quadro</span><span class="sxs-lookup"><span data-stu-id="7fc86-193">Hovering over a frame</span></span>  
    > ![Passar o mouse sobre um quadro][ImageFrameHover]  

<span data-ttu-id="7fc86-195">Claro que, com esta demonstração, é muito óbvio que a página não está funcionando bem.</span><span class="sxs-lookup"><span data-stu-id="7fc86-195">Of course, with this demo, it is pretty obvious that the page is not performing well.</span></span>  <span data-ttu-id="7fc86-196">Mas, em situações reais, talvez não seja tão claro que ter todas essas ferramentas para fazer com que as medições se tornem úteis.</span><span class="sxs-lookup"><span data-stu-id="7fc86-196">But in real scenarios, it may not be so clear, so having all of these tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="7fc86-197">Bônus: abrir o medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="7fc86-197">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="7fc86-198">Outra ferramenta prática é o medidor de FPS, que fornece estimativas em tempo real para FPS quando a página é executada.</span><span class="sxs-lookup"><span data-stu-id="7fc86-198">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="7fc86-199">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="7fc86-199">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="7fc86-200">Comece `Rendering` a digitar no menu de comando e selecione **Mostrar renderização**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-200">Start typing `Rendering` in the Command Menu and select **Show Rendering**.</span></span>  
1.  <span data-ttu-id="7fc86-201">Na guia **renderização** , ative o **medidor de FPS**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-201">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="7fc86-202">Uma nova sobreposição aparece no canto superior direito do seu visor.</span><span class="sxs-lookup"><span data-stu-id="7fc86-202">A new overlay appears in the top-right of your viewport.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-203">Figura 9</span><span class="sxs-lookup"><span data-stu-id="7fc86-203">Figure 9</span></span>  
    > <span data-ttu-id="7fc86-204">O medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="7fc86-204">The FPS meter</span></span>  
    > ![O medidor de FPS][ImageFPSMeter]  

1.  <span data-ttu-id="7fc86-206">Desative o **medidor de FPS** e pressione `Escape` para fechar a guia **renderização** .  Você não o usará neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="7fc86-206">Disable the **FPS Meter** and press `Escape` to close the **Rendering** tab.  You won't be using it in this tutorial.</span></span>  

### <span data-ttu-id="7fc86-207">Localizar o afunilamento</span><span class="sxs-lookup"><span data-stu-id="7fc86-207">Find the bottleneck</span></span>  

<span data-ttu-id="7fc86-208">Agora que você já mediu e verificou que a animação não está funcionando bem, a próxima pergunta a ser respondida é: por quê?</span><span class="sxs-lookup"><span data-stu-id="7fc86-208">Now that you've measured and verified that the animation is not performing well, the next question to answer is:  why?</span></span>  

1.  <span data-ttu-id="7fc86-209">Observe a guia Resumo.  Quando nenhum evento é selecionado, essa guia mostra uma análise da atividade.</span><span class="sxs-lookup"><span data-stu-id="7fc86-209">Note the summary tab.  When no events are selected, this tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="7fc86-210">A página gastou na maior parte da renderização de tempo.</span><span class="sxs-lookup"><span data-stu-id="7fc86-210">The page spent most of its time rendering.</span></span>  <span data-ttu-id="7fc86-211">Como o desempenho é a arte de fazer menos trabalho, seu objetivo é reduzir a quantidade de tempo gasto com o trabalho de renderização.</span><span class="sxs-lookup"><span data-stu-id="7fc86-211">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-212">Figura 10</span><span class="sxs-lookup"><span data-stu-id="7fc86-212">Figure 10</span></span>  
    > <span data-ttu-id="7fc86-213">A guia Resumo</span><span class="sxs-lookup"><span data-stu-id="7fc86-213">The Summary tab</span></span>  
    > ![A guia Resumo][ImageSummaryTab]  

1.  <span data-ttu-id="7fc86-215">Expanda a seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-215">Expand the **Main** section.</span></span>  <span data-ttu-id="7fc86-216">DevTools mostra um gráfico de chama de atividade no thread principal ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="7fc86-216">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="7fc86-217">O eixo x representa a gravação ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="7fc86-217">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="7fc86-218">Cada barra representa um evento.</span><span class="sxs-lookup"><span data-stu-id="7fc86-218">Each bar represents an event.</span></span>  <span data-ttu-id="7fc86-219">Uma barra mais ampla significa que o evento demorou mais.</span><span class="sxs-lookup"><span data-stu-id="7fc86-219">A wider bar means that event took longer.</span></span>  <span data-ttu-id="7fc86-220">O eixo y representa a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="7fc86-220">The y-axis represents the call stack.</span></span>  <span data-ttu-id="7fc86-221">Quando você vê eventos empilhados uns sobre os outros, isso significa que os eventos superiores causaram os eventos inferiores.</span><span class="sxs-lookup"><span data-stu-id="7fc86-221">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    > ##### <span data-ttu-id="7fc86-222">Figura 11</span><span class="sxs-lookup"><span data-stu-id="7fc86-222">Figure 11</span></span>  
    > <span data-ttu-id="7fc86-223">A seção principal</span><span class="sxs-lookup"><span data-stu-id="7fc86-223">The Main section</span></span>  
    > ![A seção principal][ImageMainSection]  

1.  <span data-ttu-id="7fc86-225">Há muitos dados na gravação.</span><span class="sxs-lookup"><span data-stu-id="7fc86-225">There is a lot of data in the recording.</span></span>  <span data-ttu-id="7fc86-226">Amplie um único evento clicando, mantendo e arrastando o mouse sobre a **visão geral**, que inclui a seção que inclui os gráficos de **FPS**, **CPU**e **net** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-226">Zoom in on a single event by clicking, holding, and dragging your mouse over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="7fc86-227">A seção **principal** e a guia **Resumo** exibem apenas informações para a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="7fc86-227">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    > ###### <span data-ttu-id="7fc86-228">Figura 12</span><span class="sxs-lookup"><span data-stu-id="7fc86-228">Figure 12</span></span>  
    > <span data-ttu-id="7fc86-229">Ampliado em um único evento</span><span class="sxs-lookup"><span data-stu-id="7fc86-229">Zoomed in on a single event</span></span>  
    > ![Ampliado em um evento][ImageZoomedAnimation]  
    
    > [!NOTE]
    > <span data-ttu-id="7fc86-231">Outra maneira de ampliar é focalizar a seção **principal** clicando em seu plano de fundo ou selecionando um evento e, em seguida, pressione as `W` teclas,, `A` `S` e `D` .</span><span class="sxs-lookup"><span data-stu-id="7fc86-231">Another way to zoom is to focus the **Main** section by clicking its background or selecting an event, and then press the `W`, `A`, `S`, and `D` keys.</span></span>  
    
    1.  <span data-ttu-id="7fc86-232">Observe o triângulo vermelho no canto superior direito do evento do **quadro de animação acionado** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-232">Note the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="7fc86-233">Sempre que você vir um triângulo vermelho, é um aviso de que pode haver um problema relacionado a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fc86-233">Whenever you see a red triangle, it is a warning that there may be an issue related to this event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7fc86-234">O **quadro de animação acionado** pelo evento ocorre sempre que um [ `requestAnimationFrame()` retorno de chamada][MDNWebRequestAnimationFrame] é executado.</span><span class="sxs-lookup"><span data-stu-id="7fc86-234">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="7fc86-235">Clique no evento **frame de animação acionado** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-235">Click the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="7fc86-236">A guia **Resumo** agora mostra informações sobre esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fc86-236">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="7fc86-237">Observe o link **revelar** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-237">Note the **Reveal** link.</span></span>  <span data-ttu-id="7fc86-238">Clicar em isso faz com que o DevTools realce o evento que iniciou o evento **Framed de animação** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-238">Clicking that causes DevTools to highlight the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="7fc86-239">Observe também o link **app. js: 95** .</span><span class="sxs-lookup"><span data-stu-id="7fc86-239">Also note the **app.js:95** link.</span></span>  <span data-ttu-id="7fc86-240">Clicar nelas vai para a linha relevante no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="7fc86-240">Clicking that jumps you to the relevant line in the source code.</span></span>
    
    > ##### <span data-ttu-id="7fc86-241">Figura 13</span><span class="sxs-lookup"><span data-stu-id="7fc86-241">Figure 13</span></span>  
    > <span data-ttu-id="7fc86-242">Mais informações sobre o evento Framed de animação acionado</span><span class="sxs-lookup"><span data-stu-id="7fc86-242">More information about the Animation Frame Fired event</span></span>  
    > ![Mais informações sobre o evento Framed de animação acionado][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > <span data-ttu-id="7fc86-244">Depois de selecionar um evento, use as teclas de direção para selecionar os eventos ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="7fc86-244">After selecting an event, use the arrow keys to select the events next to it.</span></span>  

1.  <span data-ttu-id="7fc86-245">No evento **app. Update** , há vários eventos roxos.</span><span class="sxs-lookup"><span data-stu-id="7fc86-245">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="7fc86-246">Se fosse mais largo, parece que cada um deles pode ter um triângulo vermelho.</span><span class="sxs-lookup"><span data-stu-id="7fc86-246">If they were wider, it looks as though each one might have a red triangle on it.</span></span>  <span data-ttu-id="7fc86-247">Clique em um dos eventos de **layout** roxo agora.</span><span class="sxs-lookup"><span data-stu-id="7fc86-247">Click one of the purple **Layout** events now.</span></span>  <span data-ttu-id="7fc86-248">O DevTools fornece mais informações sobre o evento na guia **Resumo** .  De fato, há um aviso sobre refluxos forçados \ (outra palavra para layout \).</span><span class="sxs-lookup"><span data-stu-id="7fc86-248">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  

1.  <span data-ttu-id="7fc86-249">Na guia **Resumo** , clique no **aplicativo App. js: 71** um link em **layout forçado**.</span><span class="sxs-lookup"><span data-stu-id="7fc86-249">In the **Summary** tab, click the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="7fc86-250">DevTools leva você até a linha de código que forçou o layout.</span><span class="sxs-lookup"><span data-stu-id="7fc86-250">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    > ##### <span data-ttu-id="7fc86-251">Figura 14</span><span class="sxs-lookup"><span data-stu-id="7fc86-251">Figure 14</span></span>  
    > <span data-ttu-id="7fc86-252">A linha de código que causou o layout forçado</span><span class="sxs-lookup"><span data-stu-id="7fc86-252">The line of code that caused the forced layout</span></span>  
    > ![A linha de código que causou o layout forçado][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > <span data-ttu-id="7fc86-254">O problema com esse código é que, em cada quadro de animação, ele altera o estilo de cada ícone e, em seguida, consulta a posição de cada ícone na página.</span><span class="sxs-lookup"><span data-stu-id="7fc86-254">The problem with this code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="7fc86-255">Como os estilos foram alterados, o navegador não sabe se cada posição de ícone foi alterada, portanto, é preciso refazer o layout do ícone para calcular sua posição.</span><span class="sxs-lookup"><span data-stu-id="7fc86-255">Because the styles changed, the browser doesn't know if each icon position changed, so it has to re-layout the icon in order to compute its position.</span></span>  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

<span data-ttu-id="7fc86-256">Phew!</span><span class="sxs-lookup"><span data-stu-id="7fc86-256">Phew!</span></span>  <span data-ttu-id="7fc86-257">Isso foi muito demorado, mas agora você tem uma base sólida no fluxo de trabalho básico para analisar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7fc86-257">That was a lot to take in, but you now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="7fc86-258">Muito bom trabalho.</span><span class="sxs-lookup"><span data-stu-id="7fc86-258">Good job.</span></span>  

### <span data-ttu-id="7fc86-259">Bônus: analisar a versão otimizada</span><span class="sxs-lookup"><span data-stu-id="7fc86-259">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="7fc86-260">Usando os fluxos de trabalho e as ferramentas que você acabou de aprender, clique em **otimizar** na demonstração para habilitar o código otimizado, faça outra gravação de desempenho e, em seguida, analise os resultados.</span><span class="sxs-lookup"><span data-stu-id="7fc86-260">Using the workflows and tools that you just learned, click **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="7fc86-261">Na taxa de quadros aprimorada para a redução de eventos no gráfico de chama na seção **principal** , você pode ver que a versão otimizada do aplicativo faz muito menos trabalho, resultando em melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="7fc86-261">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you can see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="7fc86-262">Mesmo essa versão "otimizada" não é tão ótima, porque ela ainda manipula a `top` propriedade de cada ícone.</span><span class="sxs-lookup"><span data-stu-id="7fc86-262">Even this "optimized" version isn't that great, because it still manipulates the `top` property of each icon.</span></span>  <span data-ttu-id="7fc86-263">Uma abordagem melhor é aderir às propriedades que afetam somente a composição.</span><span class="sxs-lookup"><span data-stu-id="7fc86-263">A better approach is to stick to properties that only affect compositing.</span></span>  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="7fc86-264">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="7fc86-264">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="7fc86-265">Para se familiarizar com o painel de desempenho, a prática torna-se perfeita.</span><span class="sxs-lookup"><span data-stu-id="7fc86-265">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="7fc86-266">Tente fazer a criação de perfil de suas próprias páginas e analisar os resultados.</span><span class="sxs-lookup"><span data-stu-id="7fc86-266">Try profiling your own pages and analyzing the results.</span></span>  <span data-ttu-id="7fc86-267">Se tiver alguma dúvida sobre seus resultados, use o ícone de **comentários** , pressione `Alt`  +  `Shift`  +  `I` no Windows ( `Option`  +  `Shift`  +  `I` no MacOS) ou [tweet em nós][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="7fc86-267">If you have any questions about your results, use the **Feedback** icon, press `Alt` + `Shift` + `I` on Windows (`Option` + `Shift` + `I` on macOS), or [tweet at us][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="7fc86-268">Inclua capturas de tela ou links para páginas reproduzíveis, se possível.</span><span class="sxs-lookup"><span data-stu-id="7fc86-268">Include screenshots or links to reproducible pages, if possible.</span></span>

> ##### <span data-ttu-id="7fc86-269">Figura 15</span><span class="sxs-lookup"><span data-stu-id="7fc86-269">Figure 15</span></span>
> <span data-ttu-id="7fc86-270">O ícone de **comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="7fc86-270">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![O ícone \* \* feedback \* \* na Microsoft Edge DevTools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="7fc86-272">Por último, há muitas maneiras de melhorar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7fc86-272">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="7fc86-273">Este tutorial se concentrou em um afunilamento de animação específico para dar a você um tour focalizado pelo painel desempenho, mas é apenas um dos muitos afunilamentos que você pode encontrar.</span><span class="sxs-lookup"><span data-stu-id="7fc86-273">This tutorial focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Figura 1: a demonstração à esquerda e DevTools à direita"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Figura 2: limitação da CPU"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Figura 3: criando o perfil da página"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Figura 4: resultados do perfil"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Figura 5: o gráfico de FPS"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Figura 6: a guia Resumo e gráfico da CPU, organizada em azul"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Figura 7: exibindo uma captura de tela da página ao lado da marca 2500ms da gravação"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Figura 8: passando o mouse sobre um quadro"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Figura 9: o medidor de FPS"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Figura 10: a guia Resumo"  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "Figura 11: seção principal"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Figura 12: ampliada em um único quadro de animação evento acionado"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Figura 13: mais informações sobre o evento Framed de animação acionado"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Figura 14: a linha de código que causou o layout forçado"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Figura 15: o ícone * * feedback * * na Microsoft Edge DevTools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Otimizar a velocidade do site com o Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-postar um tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

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
> <span data-ttu-id="7fc86-293">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="7fc86-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7fc86-294">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7fc86-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7fc86-296">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7fc86-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
