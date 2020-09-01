---
title: Otimizar a velocidade do site com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 42b742316ccaa64aa35fc1d21c5277e448b2d5b7
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984529"
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





# <span data-ttu-id="2f740-103">Otimizar a velocidade do site com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2f740-103">Optimize website speed with Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="2f740-104">Objetivo do tutorial</span><span class="sxs-lookup"><span data-stu-id="2f740-104">Goal of tutorial</span></span>  

<span data-ttu-id="2f740-105">Este tutorial ensina a usar o Microsoft Edge DevTools para encontrar formas de fazer com que seus sites sejam carregados mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="2f740-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2f740-106">Prerequisites</span></span>  

*   <span data-ttu-id="2f740-107">Você deve ter experiência básica de desenvolvimento na Web, semelhante ao que é ensinado nesta [introdução à classe de desenvolvimento na Web][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="2f740-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="2f740-108">Você não precisa saber nada sobre o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="2f740-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="2f740-109">Saiba mais sobre isso neste tutorial!</span><span class="sxs-lookup"><span data-stu-id="2f740-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="2f740-110">Introdução</span><span class="sxs-lookup"><span data-stu-id="2f740-110">Introduction</span></span>   

<span data-ttu-id="2f740-111">Isso é Tony.</span><span class="sxs-lookup"><span data-stu-id="2f740-111">This is Tony.</span></span>  <span data-ttu-id="2f740-112">Tony é muito famoso na sociedade da gato.</span><span class="sxs-lookup"><span data-stu-id="2f740-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="2f740-113">Ele criou um site para que seus fãs possam aprender sobre seus alimentos favoritos.</span><span class="sxs-lookup"><span data-stu-id="2f740-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="2f740-114">Seus fãs adoram o site, mas o Tony mantém reclamações auditivas que o site carrega lentamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="2f740-115">Tony solicitou que você o ajude a acelerar o site.</span><span class="sxs-lookup"><span data-stu-id="2f740-115">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony o gato" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="2f740-117">Tony o gato</span><span class="sxs-lookup"><span data-stu-id="2f740-117">Tony the cat</span></span>  
:::image-end:::  

## <span data-ttu-id="2f740-118">Etapa 1: auditar o site</span><span class="sxs-lookup"><span data-stu-id="2f740-118">Step 1: Audit the site</span></span>   

<span data-ttu-id="2f740-119">Sempre que você se configurar para melhorar o desempenho de carga de um site, **sempre comece com uma auditoria**.</span><span class="sxs-lookup"><span data-stu-id="2f740-119">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="2f740-120">A auditoria tem duas funções importantes:</span><span class="sxs-lookup"><span data-stu-id="2f740-120">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="2f740-121">Ele cria uma **linha de base** para você medir alterações subsequentes em relação a.</span><span class="sxs-lookup"><span data-stu-id="2f740-121">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="2f740-122">Ele oferece **dicas acionáveis** sobre quais alterações têm o maior impacto possível.</span><span class="sxs-lookup"><span data-stu-id="2f740-122">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <span data-ttu-id="2f740-123">Configurar</span><span class="sxs-lookup"><span data-stu-id="2f740-123">Set up</span></span>   

<span data-ttu-id="2f740-124">Primeiro, você deve configurar o site para que possa fazer alterações nele mais tarde.</span><span class="sxs-lookup"><span data-stu-id="2f740-124">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="2f740-125">[Abra o código-fonte do site](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="2f740-125">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="2f740-126">Esta guia é referida como a **guia Editor**.</span><span class="sxs-lookup"><span data-stu-id="2f740-126">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="A guia Editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="2f740-128">A **guia Editor**</span><span class="sxs-lookup"><span data-stu-id="2f740-128">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-129">Selecione **Tony**.</span><span class="sxs-lookup"><span data-stu-id="2f740-129">Select **tony**.</span></span>  <span data-ttu-id="2f740-130">Um menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="2f740-130">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="O menu que aparece depois de clicar em Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="2f740-132">O menu que aparece depois de clicar em **Tony**</span><span class="sxs-lookup"><span data-stu-id="2f740-132">The menu that appears after clicking **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-133">Selecione **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="2f740-133">Select **Remix Project**.</span></span>  <span data-ttu-id="2f740-134">O nome do projeto muda de **Tony** para algum nome gerado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-134">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="2f740-135">Agora você tem sua própria cópia editável do código.</span><span class="sxs-lookup"><span data-stu-id="2f740-135">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="2f740-136">Posteriormente, você pode fazer alterações nesse código.</span><span class="sxs-lookup"><span data-stu-id="2f740-136">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="2f740-137">Selecione **Mostrar** e selecione **em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="2f740-137">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="2f740-138">A demonstração é aberta em uma nova guia.  Esta guia é referida como a **guia demonstração**.  Pode levar alguns instantes para que o site seja carregado.</span><span class="sxs-lookup"><span data-stu-id="2f740-138">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="A guia demonstração" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="2f740-140">A guia demonstração</span><span class="sxs-lookup"><span data-stu-id="2f740-140">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-141">Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="2f740-141">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="2f740-142">O Microsoft Edge DevTools abre juntamente com a demonstração.</span><span class="sxs-lookup"><span data-stu-id="2f740-142">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools e a demonstração" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="2f740-144">DevTools e a demonstração</span><span class="sxs-lookup"><span data-stu-id="2f740-144">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2f740-145">Para o restante das capturas de tela neste tutorial, DevTools é exibido em uma janela separada.</span><span class="sxs-lookup"><span data-stu-id="2f740-145">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="2f740-146">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digitando `Undock` e, em seguida, selecione **desencaixar em uma janela separada**.</span><span class="sxs-lookup"><span data-stu-id="2f740-146">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools desencaixado" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="2f740-148">DevTools desencaixado</span><span class="sxs-lookup"><span data-stu-id="2f740-148">Undocked DevTools</span></span>  
:::image-end:::  

### <span data-ttu-id="2f740-149">Estabelecer uma linha de base</span><span class="sxs-lookup"><span data-stu-id="2f740-149">Establish a baseline</span></span>   

<span data-ttu-id="2f740-150">A linha de base é um registro de como o site foi executado antes de você fazer qualquer melhoria no desempenho.</span><span class="sxs-lookup"><span data-stu-id="2f740-150">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="2f740-151">Selecione a guia **auditorias** .  Ele pode estar oculto atrás do botão **mais painéis** \ ( ![ mais painéis ][ImageMorePanelsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="2f740-151">Select the **Audits** tab.  It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="2f740-152">Há um Lighthouse neste painel porque o projeto que energiza o painel auditorias é denominado **Lighthouse**.</span><span class="sxs-lookup"><span data-stu-id="2f740-152">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="O painel auditorias" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="2f740-154">O painel **auditorias**</span><span class="sxs-lookup"><span data-stu-id="2f740-154">The **Audits** panel</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="2f740-155">Correspondam às suas configurações de auditoria para as da figura anterior.</span><span class="sxs-lookup"><span data-stu-id="2f740-155">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="2f740-156">Aqui está uma explicação das diferentes opções:</span><span class="sxs-lookup"><span data-stu-id="2f740-156">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="2f740-157">**Device**.</span><span class="sxs-lookup"><span data-stu-id="2f740-157">**Device**.</span></span>  <span data-ttu-id="2f740-158">A configuração para **celular** altera a cadeia de caracteres do agente do usuário e simula um visor móvel.</span><span class="sxs-lookup"><span data-stu-id="2f740-158">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="2f740-159">A configuração para **área de trabalho** simplesmente desabilita as alterações de **celular** .</span><span class="sxs-lookup"><span data-stu-id="2f740-159">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="2f740-160">**Auditorias**.</span><span class="sxs-lookup"><span data-stu-id="2f740-160">**Audits**.</span></span>  <span data-ttu-id="2f740-161">A desativação de uma categoria impede que o painel auditorias execute essas auditorias e exclui essas auditorias do relatório.</span><span class="sxs-lookup"><span data-stu-id="2f740-161">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="2f740-162">Deixe as outras categorias habilitadas, se você quiser ver os tipos de recomendações que são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="2f740-162">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="2f740-163">Desabilitar categorias ligeiramente acelera o processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="2f740-163">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="2f740-164">**Limitação**.</span><span class="sxs-lookup"><span data-stu-id="2f740-164">**Throttling**.</span></span>  <span data-ttu-id="2f740-165">Configuração para **Simulated 4G lenta, a lentidão de CPU de 4** simula as condições típicas de navegação em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="2f740-165">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="2f740-166">Ele é chamado de "simulado" porque o painel auditorias não é controlado na verdade durante o processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="2f740-166">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="2f740-167">Em vez disso, ele apenas extrapola o tempo que a página levaria para carregar em condições de celular.</span><span class="sxs-lookup"><span data-stu-id="2f740-167">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="2f740-168">A configuração **aplicada...** , por outro lado, efetivamente limita sua CPU e rede, com a compensação de um processo de auditoria mais longo.</span><span class="sxs-lookup"><span data-stu-id="2f740-168">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="2f740-169">**Limpar o armazenamento**.</span><span class="sxs-lookup"><span data-stu-id="2f740-169">**Clear Storage**.</span></span>  <span data-ttu-id="2f740-170">Habilitar essa caixa de seleção limpa todo o armazenamento associado à página antes de cada auditoria.</span><span class="sxs-lookup"><span data-stu-id="2f740-170">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="2f740-171">Deixe essa configuração em caso de você desejar auditar como os visitantes da primeira vez que o visitante terão.</span><span class="sxs-lookup"><span data-stu-id="2f740-171">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="2f740-172">Desative essa configuração quando quiser a experiência de visita de repetição.</span><span class="sxs-lookup"><span data-stu-id="2f740-172">Disable this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="2f740-173">Selecione **executar auditorias**.</span><span class="sxs-lookup"><span data-stu-id="2f740-173">Select **Run Audits**.</span></span>  <span data-ttu-id="2f740-174">Após 10 a 30 segundos, o painel auditorias mostra um relatório do desempenho do site.</span><span class="sxs-lookup"><span data-stu-id="2f740-174">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="O relatório para o painel auditorias do desempenho do site" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="2f740-176">O relatório para o painel auditorias do desempenho do site</span><span class="sxs-lookup"><span data-stu-id="2f740-176">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="2f740-177">Manipulando erros de relatório</span><span class="sxs-lookup"><span data-stu-id="2f740-177">Handling report errors</span></span>   

<span data-ttu-id="2f740-178">Se você receber um erro no relatório do painel auditorias, tente executar a guia demonstração em uma janela **InPrivate** sem nenhuma outra guia aberta.</span><span class="sxs-lookup"><span data-stu-id="2f740-178">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="2f740-179">Isso garante que você esteja executando o Microsoft Edge a partir de um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="2f740-179">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="2f740-180">As extensões do Microsoft Edge em particular geralmente interferem no processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="2f740-180">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <span data-ttu-id="2f740-181">Entender o relatório</span><span class="sxs-lookup"><span data-stu-id="2f740-181">Understand your report</span></span>   

<span data-ttu-id="2f740-182">O número na parte superior do seu relatório é a pontuação de desempenho geral do site.</span><span class="sxs-lookup"><span data-stu-id="2f740-182">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="2f740-183">Posteriormente, ao fazer alterações no código, você verá esse número aumentará.</span><span class="sxs-lookup"><span data-stu-id="2f740-183">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="2f740-184">Uma pontuação mais alta significa melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="2f740-184">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="A pontuação geral de desempenho" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="2f740-186">A pontuação geral de desempenho</span><span class="sxs-lookup"><span data-stu-id="2f740-186">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-187">A seção **métricas** fornece medidas quantitativas do desempenho do site.</span><span class="sxs-lookup"><span data-stu-id="2f740-187">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="2f740-188">Cada métrica fornece uma visão geral de um aspecto diferente do desempenho.</span><span class="sxs-lookup"><span data-stu-id="2f740-188">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="2f740-189">Por exemplo, a **primeira tinta de conteúdo** informa quando o conteúdo é pintado pela primeira vez na tela, que é uma etapa importante da percepção do usuário da carga da página, enquanto o **tempo para interativo** marca o ponto em que a página parece estar pronta o suficiente para lidar com interações do usuário.</span><span class="sxs-lookup"><span data-stu-id="2f740-189">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="A seção métricas" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="2f740-191">A seção **métricas**</span><span class="sxs-lookup"><span data-stu-id="2f740-191">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-192">Selecione o botão de alternância realçado na figura a seguir para ver uma descrição para cada métrica e clique em **saiba mais** para ler a documentação sobre ela.</span><span class="sxs-lookup"><span data-stu-id="2f740-192">Select the highlighted toggle button in the following figure to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Selecione o botão de alternância realçado para expandir os itens de métricas" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="2f740-194">Selecione o botão de alternância realçado para expandir os itens de métricas</span><span class="sxs-lookup"><span data-stu-id="2f740-194">Select the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-195">As métricas a seguir são uma coleção de capturas de tela que mostram como a página parece ser carregada.</span><span class="sxs-lookup"><span data-stu-id="2f740-195">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Capturas de tela de como a página ficou ao carregar" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="2f740-197">Capturas de tela de como a página ficou ao carregar</span><span class="sxs-lookup"><span data-stu-id="2f740-197">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-198">A seção **oportunidades** fornece dicas específicas sobre como melhorar o desempenho de carga dessa página específica.</span><span class="sxs-lookup"><span data-stu-id="2f740-198">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="A seção oportunidades" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="2f740-200">A seção **oportunidades**</span><span class="sxs-lookup"><span data-stu-id="2f740-200">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-201">Selecione uma oportunidade para saber mais sobre isso.</span><span class="sxs-lookup"><span data-stu-id="2f740-201">Select an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminar oportunidade de recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="2f740-203">**Eliminar oportunidade de recursos de bloqueio de renderização**</span><span class="sxs-lookup"><span data-stu-id="2f740-203">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-204">Selecione **saiba mais** para ver a documentação sobre por que uma oportunidade é importante e recomendações específicas sobre como corrigi-lo.</span><span class="sxs-lookup"><span data-stu-id="2f740-204">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentação para a oportunidade de eliminar recursos de bloqueio de renderização" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="2f740-206">Documentação para a oportunidade de **eliminar recursos de bloqueio de renderização**</span><span class="sxs-lookup"><span data-stu-id="2f740-206">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-207">A seção **diagnóstico** fornece mais informações sobre fatores que contribuem para o tempo de carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-207">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="A seção diagnóstico" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="2f740-209">A seção **diagnóstico**</span><span class="sxs-lookup"><span data-stu-id="2f740-209">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-210">A seção de **auditorias passadas** mostra o que o site está fazendo corretamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-210">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="2f740-211">Selecione para expandir a seção.</span><span class="sxs-lookup"><span data-stu-id="2f740-211">Select to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="A seção de auditorias passadas" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="2f740-213">A seção de **auditorias passadas**</span><span class="sxs-lookup"><span data-stu-id="2f740-213">The **Passed Audits** section</span></span>  
:::image-end:::  

## <span data-ttu-id="2f740-214">Etapa 2: Experimente</span><span class="sxs-lookup"><span data-stu-id="2f740-214">Step 2: Experiment</span></span>   

<span data-ttu-id="2f740-215">A seção oportunidades do seu relatório de auditoria fornece dicas sobre como melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-215">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="2f740-216">Nesta seção, você implementa as alterações recomendadas na base de código, fazendo auditoria do site após cada alteração para medir como ele afeta a velocidade do site.</span><span class="sxs-lookup"><span data-stu-id="2f740-216">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="2f740-217">Habilitar a compactação de texto</span><span class="sxs-lookup"><span data-stu-id="2f740-217">Enable text compression</span></span>   

<span data-ttu-id="2f740-218">O relatório informa que evitar cargas de rede enormes é uma das principais oportunidades para melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-218">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="2f740-219">Habilitar a compactação de texto é uma oportunidade de melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-219">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="2f740-220">A compactação de texto é quando você reduz ou compacta o tamanho de um arquivo de texto antes de enviá-lo pela rede.</span><span class="sxs-lookup"><span data-stu-id="2f740-220">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="2f740-221">Tipo de como você pode compactar uma pasta antes de enviar um email para ela para reduzir o tamanho.</span><span class="sxs-lookup"><span data-stu-id="2f740-221">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="2f740-222">Antes de habilitar a compactação, aqui estão algumas maneiras de verificar manualmente se os recursos de texto estão compactados.</span><span class="sxs-lookup"><span data-stu-id="2f740-222">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="2f740-223">Selecione a guia **rede** .</span><span class="sxs-lookup"><span data-stu-id="2f740-223">Select the **Network** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Painel de rede" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="2f740-225">Painel de **rede**</span><span class="sxs-lookup"><span data-stu-id="2f740-225">The **Network** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-226">Selecione o ícone de **configuração de rede** .</span><span class="sxs-lookup"><span data-stu-id="2f740-226">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="2f740-227">Marque a caixa de seleção **usar linhas de solicitação grandes** .</span><span class="sxs-lookup"><span data-stu-id="2f740-227">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="2f740-228">A altura das linhas na tabela de solicitações de rede aumenta.</span><span class="sxs-lookup"><span data-stu-id="2f740-228">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Linhas grandes na tabela solicitações de rede" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="2f740-230">Linhas grandes na tabela solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="2f740-230">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-231">Se você não vir a coluna **tamanho** na tabela de solicitações de rede, clique no cabeçalho da tabela e selecione **tamanho**.</span><span class="sxs-lookup"><span data-stu-id="2f740-231">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="2f740-232">Cada célula de **tamanho** mostra dois valores.</span><span class="sxs-lookup"><span data-stu-id="2f740-232">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="2f740-233">O valor principal é o tamanho do recurso baixado.</span><span class="sxs-lookup"><span data-stu-id="2f740-233">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="2f740-234">O valor secundário é o tamanho do recurso descompactado.</span><span class="sxs-lookup"><span data-stu-id="2f740-234">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="2f740-235">Se os dois valores forem iguais, o recurso não será compactado quando for enviado pela rede.</span><span class="sxs-lookup"><span data-stu-id="2f740-235">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="2f740-236">Por exemplo, na figura anterior, os valores superiores e inferiores para `bundle.js` são `1.2 MB` e `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="2f740-236">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="2f740-237">Verifique a compactação inspecionando os cabeçalhos HTTP de um recurso:</span><span class="sxs-lookup"><span data-stu-id="2f740-237">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="2f740-238">Selecione **bundle.js**.</span><span class="sxs-lookup"><span data-stu-id="2f740-238">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="2f740-239">Selecione a guia **cabeçalhos** .</span><span class="sxs-lookup"><span data-stu-id="2f740-239">Select the **Headers** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="A guia cabeçalhos" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="2f740-241">A guia **cabeçalhos**</span><span class="sxs-lookup"><span data-stu-id="2f740-241">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-242">Pesquisar o cabeçalho na seção de **cabeçalhos de resposta** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="2f740-242">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="2f740-243">Você não deve ver um, o que significa que `bundle.js` não foi compactado.</span><span class="sxs-lookup"><span data-stu-id="2f740-243">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="2f740-244">Quando um recurso é compactado, esse cabeçalho geralmente é definido como `gzip` , `deflate` ou `br` .</span><span class="sxs-lookup"><span data-stu-id="2f740-244">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="2f740-245">Consulte [diretrizes][MDNContentEncodingDirectives] para obter uma explicação desses valores.</span><span class="sxs-lookup"><span data-stu-id="2f740-245">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="2f740-246">Suficiente com as explicações.</span><span class="sxs-lookup"><span data-stu-id="2f740-246">Enough with the explanations.</span></span>  <span data-ttu-id="2f740-247">É hora de fazer algumas mudanças!</span><span class="sxs-lookup"><span data-stu-id="2f740-247">Time to make some changes!</span></span>  <span data-ttu-id="2f740-248">Habilite a compactação de texto adicionando algumas linhas de código:</span><span class="sxs-lookup"><span data-stu-id="2f740-248">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="2f740-249">Na guia Editor, clique em **server.js**.</span><span class="sxs-lookup"><span data-stu-id="2f740-249">In the editor tab, click **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Editar server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="2f740-251">Editar</span><span class="sxs-lookup"><span data-stu-id="2f740-251">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-252">Adicione o código a seguir ao **server.js**.</span><span class="sxs-lookup"><span data-stu-id="2f740-252">Add the following code to **server.js**.</span></span>  <span data-ttu-id="2f740-253">Certifique-se de colocar `app.use(compression())` antes `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="2f740-253">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="2f740-254">Geralmente, você precisa instalar o `compression` pacote por algo semelhante `npm i -S compression` , mas isso já foi feito para você.</span><span class="sxs-lookup"><span data-stu-id="2f740-254">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="2f740-255">Aguarde até que a falha implante a nova compilação do site.</span><span class="sxs-lookup"><span data-stu-id="2f740-255">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="2f740-256">A animação sofisticada ao lado de **ferramentas** significa que o site está sendo recriado e reimplantado.</span><span class="sxs-lookup"><span data-stu-id="2f740-256">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="2f740-257">A alteração estará pronta quando a animação ao lado de **ferramentas** ficar ausente.</span><span class="sxs-lookup"><span data-stu-id="2f740-257">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="2f740-258">Selecione **Mostrar** e selecione novamente **em uma nova janela** .</span><span class="sxs-lookup"><span data-stu-id="2f740-258">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="2f740-259">Use os fluxos de trabalho que você aprendeu anteriormente para verificar manualmente se a compactação está funcionando:</span><span class="sxs-lookup"><span data-stu-id="2f740-259">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="2f740-260">Volte para a guia demonstração e recarregue a página.</span><span class="sxs-lookup"><span data-stu-id="2f740-260">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="2f740-261">A coluna **tamanho** agora deve mostrar 2 valores diferentes para recursos de texto, como `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="2f740-261">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="2f740-262">Na figura após o seguinte, o valor principal de `256 KB` para `bundle.js` é o tamanho do arquivo que foi enviado pela rede e o valor inferior de `1.2 MB` é o tamanho de arquivo descompactado.</span><span class="sxs-lookup"><span data-stu-id="2f740-262">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="A coluna tamanho agora mostra 2 valores diferentes para recursos de texto" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="2f740-264">A coluna **tamanho** agora mostra 2 valores diferentes para recursos de texto</span><span class="sxs-lookup"><span data-stu-id="2f740-264">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-265">A seção de **cabeçalhos de resposta** para `bundle.js` agora deve incluir um `content-encoding: gzip` cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="2f740-265">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="A seção de cabeçalhos de resposta agora contém um cabeçalho de codificação de conteúdo" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="2f740-267">A seção de **cabeçalhos de resposta** agora contém um cabeçalho de codificação de conteúdo</span><span class="sxs-lookup"><span data-stu-id="2f740-267">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2f740-268">Faça a auditoria da página novamente para medir o tipo de compactação de texto de impacto no desempenho de carga da página:</span><span class="sxs-lookup"><span data-stu-id="2f740-268">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="2f740-269">Selecione a guia **auditorias** .</span><span class="sxs-lookup"><span data-stu-id="2f740-269">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="2f740-270">Selecione **executar uma auditoria** \ ( ![ realizar uma auditoria ][ImagePerformIcon] \).</span><span class="sxs-lookup"><span data-stu-id="2f740-270">Select **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="2f740-271">Deixe as configurações iguais às anteriores.</span><span class="sxs-lookup"><span data-stu-id="2f740-271">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="2f740-272">Selecione **executar auditoria**.</span><span class="sxs-lookup"><span data-stu-id="2f740-272">Select **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Um relatório de auditorias após a habilitação da compactação de texto" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="2f740-274">Um relatório de auditorias após a habilitação da compactação de texto</span><span class="sxs-lookup"><span data-stu-id="2f740-274">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="2f740-275">A pontuação geral do desempenho deve ter aumentado, o que significa que o site está ficando mais rápido.</span><span class="sxs-lookup"><span data-stu-id="2f740-275">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="2f740-276">Compactação de texto no mundo real</span><span class="sxs-lookup"><span data-stu-id="2f740-276">Text compression in the real world</span></span>   

<span data-ttu-id="2f740-277">A maioria dos servidores tem correções simples como essa para habilitar a compactação!</span><span class="sxs-lookup"><span data-stu-id="2f740-277">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="2f740-278">Basta fazer uma busca em como configurar o servidor que você usa para compactar texto.</span><span class="sxs-lookup"><span data-stu-id="2f740-278">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="2f740-279">Redimensionar imagens</span><span class="sxs-lookup"><span data-stu-id="2f740-279">Resize images</span></span>   

<span data-ttu-id="2f740-280">O relatório indica que evitar cargas de rede enormes é uma das principais oportunidades para melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-280">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="2f740-281">O redimensionamento de imagens ajuda a reduzir o tamanho da carga de rede.</span><span class="sxs-lookup"><span data-stu-id="2f740-281">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="2f740-282">Se o usuário estiver exibindo as imagens em uma tela de dispositivo móvel com 500 pixels de largura, não há nenhum ponto em enviar uma imagem de 1500 pixels para todo o seu país.</span><span class="sxs-lookup"><span data-stu-id="2f740-282">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="2f740-283">O ideal é que você envie uma imagem de 500 pixels para todo o tempo.</span><span class="sxs-lookup"><span data-stu-id="2f740-283">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="2f740-284">Em seu relatório, clique em **evitar enormes cargas de rede** para ver quais imagens devem ser redimensionadas.</span><span class="sxs-lookup"><span data-stu-id="2f740-284">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="2f740-285">Ele se parece com 2 dos arquivos jpg há mais de 2000 KB, o que é maior do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="2f740-285">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="2f740-286">De volta na guia Editor, abra `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="2f740-286">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="2f740-287">Substituir `const dir = 'big'` por `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="2f740-287">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="2f740-288">Esse diretório contém cópias das mesmas imagens que foram redimensionadas.</span><span class="sxs-lookup"><span data-stu-id="2f740-288">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="2f740-289">Faça a auditoria da página novamente para ver como essa alteração afeta o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="2f740-289">Audit the page again to see how this change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Um relatório de auditorias após o redimensionamento de imagens" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="2f740-291">Um relatório de auditorias após o redimensionamento de imagens</span><span class="sxs-lookup"><span data-stu-id="2f740-291">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2f740-292">Parece que a alteração tem apenas um efeito secundário na pontuação de desempenho geral.</span><span class="sxs-lookup"><span data-stu-id="2f740-292">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="2f740-293">No entanto, uma coisa que a pontuação não mostra claramente é o número de dados de rede que você está salvando os usuários.</span><span class="sxs-lookup"><span data-stu-id="2f740-293">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="2f740-294">O tamanho total das fotos antigas era cerca de 5,3 megabytes, enquanto agora só há cerca de 0,18 megabytes.</span><span class="sxs-lookup"><span data-stu-id="2f740-294">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="2f740-295">Redimensionamento de imagens no mundo real</span><span class="sxs-lookup"><span data-stu-id="2f740-295">Resizing images in the real world</span></span>   

<span data-ttu-id="2f740-296">Para um aplicativo pequeno, fazer um redimensionamento único como este pode ser bom o suficiente.</span><span class="sxs-lookup"><span data-stu-id="2f740-296">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="2f740-297">Mas para um aplicativo grande, isso obviamente não é dimensionável.</span><span class="sxs-lookup"><span data-stu-id="2f740-297">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="2f740-298">Aqui estão algumas estratégias para o gerenciamento de imagens em aplicativos grandes:</span><span class="sxs-lookup"><span data-stu-id="2f740-298">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="2f740-299">Redimensione imagens durante o processo de compilação.</span><span class="sxs-lookup"><span data-stu-id="2f740-299">Resize images during your build process.</span></span>  
*   <span data-ttu-id="2f740-300">Crie vários tamanhos de cada imagem durante o processo de compilação e, em seguida, use `srcset` em seu código.</span><span class="sxs-lookup"><span data-stu-id="2f740-300">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="2f740-301">Em tempo de execução, o navegador cuida da escolha de qual tamanho é melhor para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f740-301">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="2f740-302">Use um CDN de imagem que permita redimensionar dinamicamente uma imagem quando você solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="2f740-302">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="2f740-303">No mínimo, otimize cada imagem.</span><span class="sxs-lookup"><span data-stu-id="2f740-303">At the very least, optimize each image.</span></span>  <span data-ttu-id="2f740-304">Isso pode criar uma grande economia.</span><span class="sxs-lookup"><span data-stu-id="2f740-304">This may create huge savings.</span></span>  
  <span data-ttu-id="2f740-305">A otimização é quando você executa uma imagem por meio de um programa especial que reduz o tamanho do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="2f740-305">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="2f740-306">Consulte [otimizações de imagem essenciais][EssentialImageOptimization] para obter mais dicas.</span><span class="sxs-lookup"><span data-stu-id="2f740-306">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  
    
### <span data-ttu-id="2f740-307">Eliminar recursos de bloqueio de renderização</span><span class="sxs-lookup"><span data-stu-id="2f740-307">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="2f740-308">O relatório mais recente diz que eliminar recursos de bloqueio de renderização agora é a maior oportunidade.</span><span class="sxs-lookup"><span data-stu-id="2f740-308">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="2f740-309">Um recurso de bloqueio de renderização é um arquivo JavaScript ou CSS externo que o navegador deve baixar, analisar e executar antes de exibir a página.</span><span class="sxs-lookup"><span data-stu-id="2f740-309">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="2f740-310">O objetivo é executar somente o código CSS básico e JavaScript que é necessário para exibir a página corretamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-310">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="2f740-311">A primeira tarefa, então, é encontrar o código que você não precisa executar no carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-311">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="2f740-312">Selecione **eliminar recursos de bloqueio de renderização** para ver os recursos que estão bloqueando:</span><span class="sxs-lookup"><span data-stu-id="2f740-312">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="2f740-313">e `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="2f740-313">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Mais informações sobre a oportunidade de eliminar recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="2f740-315">Mais informações sobre a oportunidade de **eliminar recursos de bloqueio de renderização**</span><span class="sxs-lookup"><span data-stu-id="2f740-315">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-316">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, comece a digitar `Coverage` e selecione **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="2f740-316">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Abrir o menu de comandos do painel auditorias" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="2f740-318">Abrir o menu de comandos do painel **auditorias**</span><span class="sxs-lookup"><span data-stu-id="2f740-318">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="A guia cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="2f740-320">A guia **cobertura**</span><span class="sxs-lookup"><span data-stu-id="2f740-320">The **Coverage** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-321">Selecione **Atualizar** \ ( ![ Atualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="2f740-321">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="2f740-322">A guia **cobertura** fornece uma visão geral da quantidade de código em `bundle.js` , `jquery.js` e `lodash.js` é executada enquanto a página é carregada.</span><span class="sxs-lookup"><span data-stu-id="2f740-322">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="2f740-323">Na figura após o seguinte, cerca de 76% e 30% dos arquivos jQuery e Lodash não são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-323">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="O relatório de cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="2f740-325">O relatório de cobertura</span><span class="sxs-lookup"><span data-stu-id="2f740-325">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-326">Selecione a linha **jquery.js** .</span><span class="sxs-lookup"><span data-stu-id="2f740-326">Select the **jquery.js** row.</span></span>  <span data-ttu-id="2f740-327">DevTools abre o arquivo no painel fontes.</span><span class="sxs-lookup"><span data-stu-id="2f740-327">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="2f740-328">Uma linha de código foi executada se tiver uma barra azul ao lado dela.</span><span class="sxs-lookup"><span data-stu-id="2f740-328">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="2f740-329">Uma barra vermelha significa que ela não foi executada e não é necessária na carga da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-329">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Visualizar o arquivo jQuery no painel fontes" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="2f740-331">Visualizar o arquivo jQuery no painel **fontes**</span><span class="sxs-lookup"><span data-stu-id="2f740-331">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-332">Role pelo código jQuery um pouco.</span><span class="sxs-lookup"><span data-stu-id="2f740-332">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="2f740-333">Na verdade, algumas das linhas que recebem "executar" são apenas comentários.</span><span class="sxs-lookup"><span data-stu-id="2f740-333">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="2f740-334">Executar esse código por meio de um Minifier que retira comentários é outra maneira de reduzir o tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2f740-334">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="2f740-335">Resumindo, quando você estiver trabalhando com seu próprio código, a guia cobertura o ajudará a analisar o código, linha por linha, e enviar somente o código necessário para a carga da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-335">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="2f740-336">Os `jquery.js` arquivos e os `lodash.js` arquivos ainda são necessários para carregar a página?</span><span class="sxs-lookup"><span data-stu-id="2f740-336">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="2f740-337">A guia solicitar bloqueio exibe o que acontece quando os recursos não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2f740-337">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="2f740-338">Selecione a guia **rede** .</span><span class="sxs-lookup"><span data-stu-id="2f740-338">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="2f740-339">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando novamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-339">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="2f740-340">Comece a digitar `blocking` e selecione **Mostrar bloqueio de solicitações**.</span><span class="sxs-lookup"><span data-stu-id="2f740-340">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="A guia bloqueio de solicitação" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="2f740-342">A guia **bloqueio de solicitação**</span><span class="sxs-lookup"><span data-stu-id="2f740-342">The **Request Blocking** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-343">Selecione **Adicionar padrão** \ ( ![ Adicionar padrão ][ImageAddPatternIcon] \), tipo `/libs/*` e, em seguida, pressione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="2f740-343">Select **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Adicionar um padrão para bloquear qualquer solicitação para o diretório libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="2f740-345">Adicionar um padrão para bloquear qualquer solicitação ao `libs` diretório</span><span class="sxs-lookup"><span data-stu-id="2f740-345">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-346">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="2f740-346">Refresh the page.</span></span>  <span data-ttu-id="2f740-347">As solicitações jQuery e Lodash são vermelhas, o que significa que as solicitações foram bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="2f740-347">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="2f740-348">A página ainda é carregada e é interativa, portanto, parece que esses recursos não são necessários!</span><span class="sxs-lookup"><span data-stu-id="2f740-348">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="O painel Rede mostra que as solicitações foram bloqueadas" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="2f740-350">O painel **rede** mostra que as solicitações foram bloqueadas</span><span class="sxs-lookup"><span data-stu-id="2f740-350">The **Network** panel shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-351">Selecione **remover todos os padrões** \ ( ![ remover todos os padrões ][ImageRemoveIcon] \) para excluir o `/libs/*` padrão de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="2f740-351">Select **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="2f740-352">Em geral, a guia bloqueio de solicitação é útil para simular como a sua página se comporta quando um determinado recurso não está disponível.</span><span class="sxs-lookup"><span data-stu-id="2f740-352">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="2f740-353">Agora, remova as referências a esses arquivos do código e faça a auditoria da página novamente:</span><span class="sxs-lookup"><span data-stu-id="2f740-353">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="2f740-354">De volta na guia Editor, abra `template.html` .</span><span class="sxs-lookup"><span data-stu-id="2f740-354">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="2f740-355">Exclua `<script src="/libs/lodash.js">` e `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="2f740-355">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="2f740-356">Aguarde até que o site reconstrua e implante novamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-356">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="2f740-357">Faça a auditoria da página novamente no painel **auditorias** .</span><span class="sxs-lookup"><span data-stu-id="2f740-357">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="2f740-358">Sua pontuação geral deve ter sido aprimorada novamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-358">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Um relatório de auditorias após a remoção dos recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="2f740-360">Um relatório de **auditorias** após a remoção dos recursos de bloqueio de renderização</span><span class="sxs-lookup"><span data-stu-id="2f740-360">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="2f740-361">Otimizando o caminho de renderização crítica no mundo real</span><span class="sxs-lookup"><span data-stu-id="2f740-361">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="2f740-362">O **caminho de renderização crítica** se refere ao código que você precisa para carregar uma página.</span><span class="sxs-lookup"><span data-stu-id="2f740-362">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="2f740-363">Em geral, acelere a carga da página, enviando apenas o código Critical durante o carregamento da página e, em seguida, carregando tudo o mais.</span><span class="sxs-lookup"><span data-stu-id="2f740-363">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="2f740-364">É improvável que você possa encontrar scripts que você pode remover, mas pode encontrar muitos scripts que você não precisa solicitar durante o carregamento da página e, em vez disso, pode ser solicitado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2f740-364">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="2f740-365">Se você estiver usando uma estrutura, verifique se ela tem um modo de produção.</span><span class="sxs-lookup"><span data-stu-id="2f740-365">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="2f740-366">Esse modo pode usar um recurso como o de uma [árvore][WebpackTreeShaking] para eliminar o código desnecessário que está bloqueando o render crítico.</span><span class="sxs-lookup"><span data-stu-id="2f740-366">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="2f740-367">Executar menos trabalho do thread principal</span><span class="sxs-lookup"><span data-stu-id="2f740-367">Do less main thread work</span></span>   

<span data-ttu-id="2f740-368">O relatório mais recente mostra algumas economias em potencial mínimas na seção oportunidades, mas se você olhar para baixo na seção diagnósticos, parece que o maior afunilamento é muito grande na atividade thread principal.</span><span class="sxs-lookup"><span data-stu-id="2f740-368">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="2f740-369">O thread principal é onde o navegador faz a maior parte do trabalho necessário para exibir uma página, como análise e execução de HTML, CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2f740-369">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="2f740-370">O objetivo é usar o painel desempenho para analisar qual trabalho o thread principal está fazendo enquanto a página é carregada e localizar maneiras de adiar ou remover o trabalho desnecessário.</span><span class="sxs-lookup"><span data-stu-id="2f740-370">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="2f740-371">Selecione a guia **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="2f740-371">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="2f740-372">Selecione **configurações de captura** \ ( ![ configurações de captura ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="2f740-372">Select **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="2f740-373">Defina a **rede** para 3G e **CPU** **lenta** para **6X de lentidão**.</span><span class="sxs-lookup"><span data-stu-id="2f740-373">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="2f740-374">Dispositivos móveis geralmente têm mais restrições de hardware do que laptops ou desktops, portanto, essas configurações permitem que você experimente a carga da página como se estivesse usando um dispositivo menos potente.</span><span class="sxs-lookup"><span data-stu-id="2f740-374">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="2f740-375">Selecione **Atualizar** \ ( ![ Atualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="2f740-375">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="2f740-376">O DevTools atualiza a página e, em seguida, produz uma visualização de todo o trabalho realizado para carregar a página.</span><span class="sxs-lookup"><span data-stu-id="2f740-376">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="2f740-377">Essa visualização é chamada de **rastreamento**.</span><span class="sxs-lookup"><span data-stu-id="2f740-377">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="O rastreamento do painel desempenho do carregamento da página" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="2f740-379">O rastreamento do painel **desempenho** do carregamento da página</span><span class="sxs-lookup"><span data-stu-id="2f740-379">The **Performance** panel trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2f740-380">O rastreamento mostra a atividade cronologicamente, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="2f740-380">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="2f740-381">Os gráficos de FPS, CPU e NET na parte superior fornecem uma visão geral de quadros por segundo, atividade de CPU e atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="2f740-381">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="2f740-382">O bloco de amarelo selecionado que você vê na figura após o seguinte, a CPU estava completamente ocupada com a atividade de script.</span><span class="sxs-lookup"><span data-stu-id="2f740-382">The block of yellow selected that you see in the figure after the following, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="2f740-383">Trata-se de uma pista de que você pode acelerar o carregamento da página fazendo menos trabalho em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2f740-383">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="A seção visão geral do rastreamento" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="2f740-385">A seção visão geral do rastreamento</span><span class="sxs-lookup"><span data-stu-id="2f740-385">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="2f740-386">Investigue o rastreamento para encontrar formas de fazer menos trabalho em JavaScript:</span><span class="sxs-lookup"><span data-stu-id="2f740-386">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="2f740-387">Selecione a seção **intervalos** para expandi-la.</span><span class="sxs-lookup"><span data-stu-id="2f740-387">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="2f740-388">De acordo com o fato de que pode haver uma série de medidas de [tempo][MDNUserTimingApi] de reagir, parece que o aplicativo de Tony está usando o modo de desenvolvimento de reagir.</span><span class="sxs-lookup"><span data-stu-id="2f740-388">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="2f740-389">Alternar para o modo de produção de reagir pode produzir um pouco de desempenho simples.</span><span class="sxs-lookup"><span data-stu-id="2f740-389">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="A seção intervalos" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="2f740-391">A seção **intervalos**</span><span class="sxs-lookup"><span data-stu-id="2f740-391">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-392">Selecione **intervalos** novamente para recolher essa seção.</span><span class="sxs-lookup"><span data-stu-id="2f740-392">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="2f740-393">Procure a seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="2f740-393">Browse the **Main** section.</span></span>  <span data-ttu-id="2f740-394">Esta seção mostra um log cronológico da atividade de thread principal, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="2f740-394">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="2f740-395">O eixo y (de cima para baixo) mostra o motivo pelo qual os eventos ocorreram.</span><span class="sxs-lookup"><span data-stu-id="2f740-395">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="2f740-396">Por exemplo, no figyre após o seguinte, o `Evaluate Script` evento causou a `(anonymous)` execução da função, que causou a execução `(anonymous)` , que causou `__webpack__require__` a execução e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2f740-396">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="A seção principal" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="2f740-398">A seção **principal**</span><span class="sxs-lookup"><span data-stu-id="2f740-398">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f740-399">Role a tela para baixo até a parte inferior da seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="2f740-399">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="2f740-400">Quando você usa uma estrutura, a maior parte da atividade superior é causada pela estrutura, que normalmente está fora do seu controle.</span><span class="sxs-lookup"><span data-stu-id="2f740-400">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="2f740-401">A atividade causada pelo aplicativo geralmente está na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="2f740-401">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="2f740-402">Nesse aplicativo, parece que uma função nomeada `App` está causando muitas solicitações para uma `mineBitcoin` função.</span><span class="sxs-lookup"><span data-stu-id="2f740-402">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="2f740-403">Parece que Tony pode estar usando os dispositivos de seus fãs para o meu cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="2f740-403">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Passe o mouse sobre a atividade mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="2f740-405">Passe o mouse sobre a `mineBitcoin` atividade</span><span class="sxs-lookup"><span data-stu-id="2f740-405">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="2f740-406">Embora as solicitações que a sua estrutura fazer normalmente sejam de seu controle, às vezes você pode estruturar seu aplicativo de uma maneira que faz com que a estrutura seja executada ineficientemente.</span><span class="sxs-lookup"><span data-stu-id="2f740-406">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="2f740-407">Reestruturar seu aplicativo para usar a estrutura com eficiência é uma maneira de fazer menos trabalho do thread principal.</span><span class="sxs-lookup"><span data-stu-id="2f740-407">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="2f740-408">No entanto, isso exige uma compreensão profunda de como a estrutura funciona e o tipo de alterações feitas em seu próprio código para usar a estrutura com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="2f740-408">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="2f740-409">Expanda a seção de **baixo para cima** .</span><span class="sxs-lookup"><span data-stu-id="2f740-409">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="2f740-410">Esta guia quebra quais atividades levaram mais tempo.</span><span class="sxs-lookup"><span data-stu-id="2f740-410">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="2f740-411">Se você não vir nada na seção de baixo para cima, clique no rótulo da seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="2f740-411">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="2f740-412">A seção de **baixo para cima** mostra apenas as informações sobre qualquer atividade ou grupo de atividades selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="2f740-412">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="2f740-413">Por exemplo, se você clicou em uma das `mineBitcoin` atividades, a seção de **baixo para cima** só irá mostrar as informações de uma atividade.</span><span class="sxs-lookup"><span data-stu-id="2f740-413">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="A guia seta para baixo" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="2f740-415">A guia **seta para baixo**</span><span class="sxs-lookup"><span data-stu-id="2f740-415">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2f740-416">A coluna **autotempo** mostra quanto tempo foi gasto diretamente em cada atividade.</span><span class="sxs-lookup"><span data-stu-id="2f740-416">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="2f740-417">Por exemplo, na figura a seguir, cerca de 63% do tempo do thread principal foi gasto na `mineBitcoin` função.</span><span class="sxs-lookup"><span data-stu-id="2f740-417">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="2f740-418">Tempo para ver se o uso do modo de produção e da redução da atividade JavaScript pode acelerar o carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-418">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="2f740-419">Comece com o modo de produção:</span><span class="sxs-lookup"><span data-stu-id="2f740-419">Start with production mode:</span></span>  

1.  <span data-ttu-id="2f740-420">Na guia Editor, abra `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="2f740-420">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="2f740-421">Alterar `"mode":"development"` para `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="2f740-421">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="2f740-422">Aguarde até que a nova compilação seja implementada.</span><span class="sxs-lookup"><span data-stu-id="2f740-422">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="2f740-423">Faça a auditoria da página novamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-423">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Um relatório de auditorias após a configuração do webpack para usar o modo de produção" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="2f740-425">Um relatório de auditorias após a configuração do webpack para usar o modo de produção</span><span class="sxs-lookup"><span data-stu-id="2f740-425">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2f740-426">Para reduzir a atividade do JavaScript, remova a solicitação para `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="2f740-426">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="2f740-427">Na guia Editor, abra `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="2f740-427">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="2f740-428">Comente a solicitação para `this.mineBitcoin(1500)` no (a) `constructor` .</span><span class="sxs-lookup"><span data-stu-id="2f740-428">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="2f740-429">Aguarde até que a nova compilação seja implementada.</span><span class="sxs-lookup"><span data-stu-id="2f740-429">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="2f740-430">Faça a auditoria da página novamente.</span><span class="sxs-lookup"><span data-stu-id="2f740-430">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Um relatório de auditorias após remover o trabalho em JavaScript desnecessário" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="2f740-432">Um relatório de auditorias após remover o trabalho em JavaScript desnecessário</span><span class="sxs-lookup"><span data-stu-id="2f740-432">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2f740-433">Parece que essa última alteração causou um salto maciço no desempenho!</span><span class="sxs-lookup"><span data-stu-id="2f740-433">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="2f740-434">Esta seção forneceu uma introdução breve ao painel desempenho.</span><span class="sxs-lookup"><span data-stu-id="2f740-434">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="2f740-435">Consulte [referência de análise de desempenho][DevtoolsEvaluatePerformanceReference] para saber mais sobre como analisar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="2f740-435">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="2f740-436">Como fazer o trabalho de threads principais no mundo real</span><span class="sxs-lookup"><span data-stu-id="2f740-436">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="2f740-437">Em geral, o painel **desempenho** é a maneira mais comum de entender quais atividades o seu site faz ao carregar e encontrar maneiras de remover atividades desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="2f740-437">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="2f740-438">Se você preferir uma abordagem que se pareça mais `console.log()` , a [API de tempo do usuário][MDNUserTimingApi] permite marcar arbitrariamente determinadas fases do ciclo de vida do aplicativo, para controlar quanto tempo leva cada uma dessas fases.</span><span class="sxs-lookup"><span data-stu-id="2f740-438">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="2f740-439">Resumo</span><span class="sxs-lookup"><span data-stu-id="2f740-439">Summary</span></span>   

*   <span data-ttu-id="2f740-440">Sempre que você tiver sido configurado para otimizar o desempenho de carga de um site, sempre comece com uma auditoria.</span><span class="sxs-lookup"><span data-stu-id="2f740-440">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="2f740-441">A auditoria estabelece uma linha de base e fornece dicas sobre como melhorar.</span><span class="sxs-lookup"><span data-stu-id="2f740-441">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="2f740-442">Faça uma alteração de cada vez e faça a auditoria da página após cada alteração para ver como essa alteração afeta o desempenho.</span><span class="sxs-lookup"><span data-stu-id="2f740-442">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--  
  


-->  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referência de análise de desempenho | Documentos da Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introdução à classe de desenvolvimento da Web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Otimização de imagem essencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Diretivas-codificação de conteúdo | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de tempo do usuário | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Aperto de árvore | webpack"  

> [!NOTE]
> <span data-ttu-id="2f740-449">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="2f740-449">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2f740-450">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="2f740-450">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2f740-452">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f740-452">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
