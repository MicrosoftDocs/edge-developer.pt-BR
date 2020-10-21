---
description: Saiba como avaliar o desempenho do tempo de execução no Microsoft Edge DevTools.
title: Comece a analisar o desempenho do tempo de execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7cb1d8f073cdb8a43093514dd7dea86d72102011
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124982"
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

# <span data-ttu-id="d7e26-104">Comece a analisar o desempenho do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="d7e26-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="d7e26-105">Para saber como fazer com que as páginas sejam carregadas mais rapidamente, navegue até [otimizar a velocidade do site][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="d7e26-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="d7e26-106">O desempenho do tempo de execução é a forma como a sua página é executada, em oposição ao carregamento.</span><span class="sxs-lookup"><span data-stu-id="d7e26-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="d7e26-107">O artigo do tutorial a seguir ensina a usar o painel de desempenho do Microsoft Edge DevTools para analisar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d7e26-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="d7e26-108">Em termos do modelo de **trilho** , as habilidades que você aprende neste tutorial são úteis para analisar a resposta, a animação e as fases ociosas da página.</span><span class="sxs-lookup"><span data-stu-id="d7e26-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="d7e26-109">Introdução</span><span class="sxs-lookup"><span data-stu-id="d7e26-109">Get started</span></span>  

<span data-ttu-id="d7e26-110">No tutorial a seguir, abra o DevTools em uma página dinâmica e use o painel **desempenho** para localizar um afunilamento de desempenho na página.</span><span class="sxs-lookup"><span data-stu-id="d7e26-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="d7e26-111">Abrir o Microsoft Edge no **modo InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="d7e26-112">O modo InPrivate garante que o Microsoft Edge seja executado em um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="d7e26-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="d7e26-113">Por exemplo, se você tiver muitas extensões instaladas, as extensões poderão criar ruído em medidas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="d7e26-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="d7e26-114">Carregue a página a seguir na sua janela InPrivate.</span><span class="sxs-lookup"><span data-stu-id="d7e26-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="d7e26-115">A página é a demonstração na qual você vai criar o perfil.</span><span class="sxs-lookup"><span data-stu-id="d7e26-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="d7e26-116">A página mostra um monte de ícones pequenos em movimento para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="d7e26-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="d7e26-117">Selecione `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \) para abrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="d7e26-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="d7e26-119">A demonstração à esquerda e DevTools à direita</span><span class="sxs-lookup"><span data-stu-id="d7e26-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d7e26-120">Para o restante dos números, o DevTools está [desencaixado em uma janela separada][DevtoolsCustomizePlacement] para se concentrar melhor no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d7e26-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <span data-ttu-id="d7e26-121">Simular uma CPU móvel</span><span class="sxs-lookup"><span data-stu-id="d7e26-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="d7e26-122">Dispositivos móveis têm muito menos energia de CPU do que desktops e notebooks.</span><span class="sxs-lookup"><span data-stu-id="d7e26-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="d7e26-123">Sempre que você criar o perfil de uma página, use a limitação de CPU para simular como a sua página é realizada em dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="d7e26-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="d7e26-124">No DevTools, escolha a guia **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-124">In DevTools, choose the **Performance** tab.</span></span>  
1.  <span data-ttu-id="d7e26-125">Verifique se a caixa de seleção **capturas de tela** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d7e26-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="d7e26-126">Escolha **configurações de captura** \ (! [ Configurações de captura] [ImageCaptureSettingsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d7e26-126">Choose **Capture Settings** \(![Capture Settings][ImageCaptureSettingsIcon]\).</span></span>  <span data-ttu-id="d7e26-127">DevTools revela configurações relacionadas à maneira como ele captura métricas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="d7e26-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="d7e26-128">Para **CPU**, escolha **4x lentidão**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="d7e26-129">O DevTools acelera a CPU para que seja 4 vezes mais lento do que o normal.</span><span class="sxs-lookup"><span data-stu-id="d7e26-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="d7e26-131">Acelerador de CPU</span><span class="sxs-lookup"><span data-stu-id="d7e26-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d7e26-132">Ao testar outras páginas; Se você quiser garantir que cada página funcione bem em dispositivos móveis low-end, defina a limitação de CPU para **6x a lentidão**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="d7e26-133">A demonstração não funciona bem com o 6X de lentidão, portanto, ele simplesmente usa 4 vezes a lentidão para fins de instrução.</span><span class="sxs-lookup"><span data-stu-id="d7e26-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="d7e26-134">Configurar a demonstração</span><span class="sxs-lookup"><span data-stu-id="d7e26-134">Set up the demo</span></span>  

<span data-ttu-id="d7e26-135">É difícil criar uma demonstração de desempenho do tempo de execução que funcione consistentemente para todos os leitores do site.</span><span class="sxs-lookup"><span data-stu-id="d7e26-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="d7e26-136">A seção a seguir permite que você personalize a demonstração para garantir que sua experiência seja relativamente consistente com as capturas de tela e as descrições, independentemente de sua configuração específica.</span><span class="sxs-lookup"><span data-stu-id="d7e26-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="d7e26-137">Escolha o botão **Adicionar 10** até que os ícones azuis sejam movidos visivelmente mais devagar do que antes.</span><span class="sxs-lookup"><span data-stu-id="d7e26-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="d7e26-138">Em um computador high-end, você pode escolher cerca de 20 vezes.</span><span class="sxs-lookup"><span data-stu-id="d7e26-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="d7e26-139">Escolha **otimizar**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-139">Choose **Optimize**.</span></span>  <span data-ttu-id="d7e26-140">Os ícones azuis devem se mover de forma mais rápida e mais suave.</span><span class="sxs-lookup"><span data-stu-id="d7e26-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d7e26-141">Para exibir melhor uma diferença entre as versões otimizadas e não otimizadas, escolha algumas vezes o botão **subtrair 10** e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="d7e26-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="d7e26-142">Se você adicionar muitos ícones azuis, poderá terminar a CPU e, em seguida, poderá não observar uma diferença importante nos resultados das duas versões.</span><span class="sxs-lookup"><span data-stu-id="d7e26-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="d7e26-143">Escolha não **otimizar**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="d7e26-144">Os ícones azuis se movem mais lentos e com mais lentidão.</span><span class="sxs-lookup"><span data-stu-id="d7e26-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <span data-ttu-id="d7e26-145">Desempenho do registro em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="d7e26-145">Record runtime performance</span></span>  

<span data-ttu-id="d7e26-146">Quando você executou a versão otimizada da página, os ícones azuis são movidos mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d7e26-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="d7e26-147">Por quê?</span><span class="sxs-lookup"><span data-stu-id="d7e26-147">Why is that?</span></span>  <span data-ttu-id="d7e26-148">Ambas as versões devem mover os ícones da mesma quantidade de espaço na mesma quantidade de tempo.</span><span class="sxs-lookup"><span data-stu-id="d7e26-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="d7e26-149">Faça uma gravação no painel desempenho para aprender a detectar o afunilamento de desempenho na versão desotimizada.</span><span class="sxs-lookup"><span data-stu-id="d7e26-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="d7e26-150">No DevTools, escolha **gravar** \ (! [ Record] [ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d7e26-150">In DevTools, choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  <span data-ttu-id="d7e26-151">DevTools captura métricas de desempenho à medida que a página é executada.</span><span class="sxs-lookup"><span data-stu-id="d7e26-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="d7e26-153">Criar perfil da página</span><span class="sxs-lookup"><span data-stu-id="d7e26-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7e26-154">Aguarde alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="d7e26-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="d7e26-155">Escolha **parar**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-155">Choose **Stop**.</span></span>  <span data-ttu-id="d7e26-156">DevTools interrompe a gravação, processa os dados e, em seguida, exibe os resultados no painel desempenho.</span><span class="sxs-lookup"><span data-stu-id="d7e26-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="d7e26-158">Os resultados do perfil</span><span class="sxs-lookup"><span data-stu-id="d7e26-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d7e26-159">Wow, que é um volume impressionante de dados.</span><span class="sxs-lookup"><span data-stu-id="d7e26-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="d7e26-160">Não se preocupe, logo, o processo faz mais sentido.</span><span class="sxs-lookup"><span data-stu-id="d7e26-160">do not worry, soon the process makes more sense.</span></span>  

## <span data-ttu-id="d7e26-161">Analisar os resultados</span><span class="sxs-lookup"><span data-stu-id="d7e26-161">Analyze the results</span></span>  

<span data-ttu-id="d7e26-162">Depois de registrar o desempenho da página, avalie a qualidade do desempenho da página e encontre as causas.</span><span class="sxs-lookup"><span data-stu-id="d7e26-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <span data-ttu-id="d7e26-163">Analisar quadros por segundo</span><span class="sxs-lookup"><span data-stu-id="d7e26-163">Analyze frames per second</span></span>  

<span data-ttu-id="d7e26-164">A principal métrica para medir o desempenho de qualquer animação é a de quadros por segundo \ (FPS \).</span><span class="sxs-lookup"><span data-stu-id="d7e26-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="d7e26-165">Os usuários ficam satisfeitos quando animações são executadas em 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="d7e26-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="d7e26-166">Examine o gráfico de **FPS** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-166">Look at the **FPS** chart.</span></span>  <span data-ttu-id="d7e26-167">Sempre que você vir uma barra vermelha acima de **FPS**, significa que a taxa de quadros ficou tão baixa que provavelmente está prejudicando a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="d7e26-167">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="d7e26-168">Em geral, quanto maior a barra verde, mais alta a FPS.</span><span class="sxs-lookup"><span data-stu-id="d7e26-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="d7e26-170">O gráfico de **FPS**</span><span class="sxs-lookup"><span data-stu-id="d7e26-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7e26-171">Abaixo do gráfico de **FPS** , você vê o gráfico **da CPU** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-171">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="d7e26-172">As cores do gráfico de **CPU** correspondem às cores na guia **Resumo** , na parte inferior do painel desempenho.</span><span class="sxs-lookup"><span data-stu-id="d7e26-172">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="d7e26-173">O fato de que o gráfico de **CPU** está cheio de cores significa que a CPU foi maximizada durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="d7e26-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="d7e26-174">Sempre que você vê a CPU esgotada durante longos períodos, é uma indicação para encontrar formas de fazer menos trabalho.</span><span class="sxs-lookup"><span data-stu-id="d7e26-174">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="d7e26-176">A guia **Resumo** e gráfico **da CPU**</span><span class="sxs-lookup"><span data-stu-id="d7e26-176">The **CPU** chart and **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7e26-177">Passe o mouse sobre os gráficos de **FPS**, **CPU**ou **rede** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="d7e26-178">DevTools mostra uma captura de tela da página nesse momento.</span><span class="sxs-lookup"><span data-stu-id="d7e26-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="d7e26-179">Mova o mouse para a esquerda e para a direita para reproduzir a gravação.</span><span class="sxs-lookup"><span data-stu-id="d7e26-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="d7e26-180">A ação é referenciada como scrubbing, e é útil para analisar manualmente a progressão de animações.</span><span class="sxs-lookup"><span data-stu-id="d7e26-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="d7e26-182">Exibir uma captura de tela da página ao lado da marca 2500ms da gravação</span><span class="sxs-lookup"><span data-stu-id="d7e26-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7e26-183">Na seção **quadros** , passe o mouse sobre um dos quadrados verdes.</span><span class="sxs-lookup"><span data-stu-id="d7e26-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="d7e26-184">DevTools mostra as FPS para esse quadro específico.</span><span class="sxs-lookup"><span data-stu-id="d7e26-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="d7e26-185">Cada quadro provavelmente está logo abaixo do destino de 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="d7e26-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="d7e26-187">Passe o mouse sobre um quadro</span><span class="sxs-lookup"><span data-stu-id="d7e26-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d7e26-188">É claro que você verá que a página não está funcionando bem.</span><span class="sxs-lookup"><span data-stu-id="d7e26-188">Of course, you should see that the page is not performing well.</span></span>  <span data-ttu-id="d7e26-189">Mas, em situações reais, talvez não seja tão claro que ter todas as ferramentas para fazer as medições se torne útil.</span><span class="sxs-lookup"><span data-stu-id="d7e26-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="d7e26-190">Bônus: abrir o medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="d7e26-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="d7e26-191">Outra ferramenta prática é o medidor de FPS, que fornece estimativas em tempo real para FPS quando a página é executada.</span><span class="sxs-lookup"><span data-stu-id="d7e26-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="d7e26-192">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="d7e26-193">Comece `Rendering` a digitar no **menu de comando** e escolha **Mostrar renderização**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="d7e26-194">Na guia **renderização** , ative o **medidor de FPS**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-194">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="d7e26-195">Uma nova sobreposição aparece no canto superior direito do seu visor.</span><span class="sxs-lookup"><span data-stu-id="d7e26-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="d7e26-197">O **medidor de FPS**</span><span class="sxs-lookup"><span data-stu-id="d7e26-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="d7e26-198">Desabilite o **medidor de FPS** e selecione `Escape` para fechar a guia **renderização** .  Você não está usando o **metro de FPS** neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="d7e26-198">Disable the **FPS Meter** and select `Escape` to close the **Rendering** tab.  You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <span data-ttu-id="d7e26-199">Localizar o afunilamento</span><span class="sxs-lookup"><span data-stu-id="d7e26-199">Find the bottleneck</span></span>  

<span data-ttu-id="d7e26-200">Depois de medir e verificar se a animação não está funcionando bem, a próxima etapa é responder a pergunta "por quê?".</span><span class="sxs-lookup"><span data-stu-id="d7e26-200">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="d7e26-201">Quando nenhum evento é selecionado, a guia **Resumo** mostra uma análise da atividade.</span><span class="sxs-lookup"><span data-stu-id="d7e26-201">When no events are selected, the **Summary** tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="d7e26-202">A página gastou na maioria do processamento de tempo.</span><span class="sxs-lookup"><span data-stu-id="d7e26-202">The page spent most of the time rendering.</span></span>  <span data-ttu-id="d7e26-203">Como o desempenho é a arte de fazer menos trabalho, seu objetivo é reduzir a quantidade de tempo gasto com o trabalho de renderização.</span><span class="sxs-lookup"><span data-stu-id="d7e26-203">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="d7e26-205">A guia **Resumo**</span><span class="sxs-lookup"><span data-stu-id="d7e26-205">The **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7e26-206">Expanda a seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-206">Expand the **Main** section.</span></span>  <span data-ttu-id="d7e26-207">DevTools mostra um gráfico de chama de atividade no thread principal ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="d7e26-207">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="d7e26-208">O eixo x representa a gravação ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="d7e26-208">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="d7e26-209">Cada barra representa um evento.</span><span class="sxs-lookup"><span data-stu-id="d7e26-209">Each bar represents an event.</span></span>  <span data-ttu-id="d7e26-210">Uma barra mais ampla significa que o evento demorou mais.</span><span class="sxs-lookup"><span data-stu-id="d7e26-210">A wider bar means that event took longer.</span></span>  <span data-ttu-id="d7e26-211">O eixo y representa a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="d7e26-211">The y-axis represents the call stack.</span></span>  <span data-ttu-id="d7e26-212">Quando você vê eventos empilhados uns sobre os outros, isso significa que os eventos superiores causaram os eventos inferiores.</span><span class="sxs-lookup"><span data-stu-id="d7e26-212">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="d7e26-214">A seção **principal**</span><span class="sxs-lookup"><span data-stu-id="d7e26-214">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7e26-215">Há muitos dados na gravação.</span><span class="sxs-lookup"><span data-stu-id="d7e26-215">There is a lot of data in the recording.</span></span>  <span data-ttu-id="d7e26-216">Para ampliar um único evento; escolha, segure e arrastou o cursor sobre a **visão geral**, que é a seção que inclui os gráficos de **FPS**, **CPU**e **net** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-216">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="d7e26-217">A seção **principal** e a guia **Resumo** exibem apenas informações para a parte selecionada da gravação.</span><span class="sxs-lookup"><span data-stu-id="d7e26-217">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="d7e26-219">Ampliar um evento</span><span class="sxs-lookup"><span data-stu-id="d7e26-219">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d7e26-220">Outra maneira de aplicar zoom, focalizar a seção **principal** , escolher o plano de fundo ou um evento e selecionar `W` , `A` , `S` ou `D` .</span><span class="sxs-lookup"><span data-stu-id="d7e26-220">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="d7e26-221">Foco no triângulo vermelho no canto superior direito do evento de **quadro de animação acionado** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-221">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="d7e26-222">Sempre que você vir um triângulo vermelho, é um aviso de que pode haver um problema relacionado ao evento.</span><span class="sxs-lookup"><span data-stu-id="d7e26-222">Whenever you see a red triangle, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d7e26-223">O **quadro de animação acionado** pelo evento ocorre sempre que um [ `requestAnimationFrame()` retorno de chamada][MDNWebRequestAnimationFrame] é executado.</span><span class="sxs-lookup"><span data-stu-id="d7e26-223">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="d7e26-224">Escolha o evento **Framed de animação acionado** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-224">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="d7e26-225">A guia **Resumo** agora mostra informações sobre esse evento.</span><span class="sxs-lookup"><span data-stu-id="d7e26-225">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="d7e26-226">Observe o link **revelar** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-226">Note the **Reveal** link.</span></span>  <span data-ttu-id="d7e26-227">Depois de escolher, DevTools para destacar o evento que iniciou o evento **Framed de animação** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-227">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="d7e26-228">Além disso, concentre-se no link **app.js:95** .</span><span class="sxs-lookup"><span data-stu-id="d7e26-228">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="d7e26-229">Depois de escolher, a linha relevante no código-fonte será exibida.</span><span class="sxs-lookup"><span data-stu-id="d7e26-229">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="d7e26-231">Mais informações sobre o evento **Framed de animação acionado**</span><span class="sxs-lookup"><span data-stu-id="d7e26-231">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d7e26-232">Depois de selecionar um evento, use as teclas de direção para selecionar os eventos ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="d7e26-232">After selecting an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="d7e26-233">No evento **app. Update** , há vários eventos roxos.</span><span class="sxs-lookup"><span data-stu-id="d7e26-233">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="d7e26-234">Se cada evento roxo foi mais largo, parece que cada um deles pode ter um triângulo vermelho sobre ele.</span><span class="sxs-lookup"><span data-stu-id="d7e26-234">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="d7e26-235">Escolha um dos eventos de **layout** roxo.</span><span class="sxs-lookup"><span data-stu-id="d7e26-235">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="d7e26-236">O DevTools fornece mais informações sobre o evento na guia **Resumo** .  De fato, há um aviso sobre refluxos forçados \ (outra palavra para layout \).</span><span class="sxs-lookup"><span data-stu-id="d7e26-236">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="d7e26-237">Na guia **Resumo** , escolha o link **app.js:71** em **layout forçado**.</span><span class="sxs-lookup"><span data-stu-id="d7e26-237">In the **Summary** tab, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="d7e26-238">DevTools leva você até a linha de código que forçou o layout.</span><span class="sxs-lookup"><span data-stu-id="d7e26-238">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="d7e26-240">A linha de código que causou o layout forçado</span><span class="sxs-lookup"><span data-stu-id="d7e26-240">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d7e26-241">O problema com o código é que, em cada quadro de animação, ele altera o estilo de cada ícone e, em seguida, consulta a posição de cada ícone na página.</span><span class="sxs-lookup"><span data-stu-id="d7e26-241">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="d7e26-242">Como os estilos foram alterados, o navegador não sabe se cada posição de ícone foi alterada, portanto, é preciso refazer o layout do ícone para calcular a nova posição.</span><span class="sxs-lookup"><span data-stu-id="d7e26-242">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="d7e26-243">Foi muito útil aprender.</span><span class="sxs-lookup"><span data-stu-id="d7e26-243">That was a lot to learn.</span></span>  <span data-ttu-id="d7e26-244">Agora você tem uma base sólida no fluxo de trabalho básico para analisar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d7e26-244">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="d7e26-245">Muito bom trabalho.</span><span class="sxs-lookup"><span data-stu-id="d7e26-245">Good job.</span></span>  

### <span data-ttu-id="d7e26-246">Bônus: analisar a versão otimizada</span><span class="sxs-lookup"><span data-stu-id="d7e26-246">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="d7e26-247">Usando os fluxos de trabalho e as ferramentas que você acabou de aprender, escolha **otimizar** na demonstração para habilitar o código otimizado, faça outra gravação de desempenho e, em seguida, analise os resultados.</span><span class="sxs-lookup"><span data-stu-id="d7e26-247">Using the workflows and tools that you just learned, choose **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="d7e26-248">Na taxa de quadros aprimorada para a redução de eventos no gráfico de chama na seção **principal** , você pode ver que a versão otimizada do aplicativo faz muito menos trabalho, resultando em melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="d7e26-248">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you are able to see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="d7e26-249">Até mesmo a versão otimizada não é ótima, porque ela manipula a `top` propriedade de cada ícone.</span><span class="sxs-lookup"><span data-stu-id="d7e26-249">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="d7e26-250">Uma abordagem melhor é aderir às propriedades que afetam somente a composição.</span><span class="sxs-lookup"><span data-stu-id="d7e26-250">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="d7e26-251">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d7e26-251">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="d7e26-252">Para se familiarizar com o painel de desempenho, a prática torna-se perfeita.</span><span class="sxs-lookup"><span data-stu-id="d7e26-252">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="d7e26-253">Tente fazer a criação de perfil de suas páginas e analisar os resultados.</span><span class="sxs-lookup"><span data-stu-id="d7e26-253">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="d7e26-254">Se tiver alguma dúvida sobre seus resultados, use o ícone **enviar comentários** , selecione `Alt` + `Shift` + `I` \ (Windows, Linux \), selecione `Option` + `Shift` + `I` \ (MacOS \) ou [tweet The devtools Team][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="d7e26-254">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="d7e26-255">Inclua capturas de tela ou links para páginas reproduzíveis, se possível.</span><span class="sxs-lookup"><span data-stu-id="d7e26-255">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="d7e26-257">O ícone **enviar comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="d7e26-257">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="d7e26-258">Por último, há muitas maneiras de melhorar o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d7e26-258">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="d7e26-259">Este artigo se concentrou em um afunilamento de animação específico para dar a você um tour focalizado pelo painel desempenho, mas é apenas um dos muitos afunilamentos que você pode encontrar.</span><span class="sxs-lookup"><span data-stu-id="d7e26-259">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <span data-ttu-id="d7e26-260">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d7e26-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Otimizar a velocidade do site com o Microsoft Edge DevTools"  

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
> <span data-ttu-id="d7e26-265">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="d7e26-265">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d7e26-266">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d7e26-266">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d7e26-268">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d7e26-268">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
