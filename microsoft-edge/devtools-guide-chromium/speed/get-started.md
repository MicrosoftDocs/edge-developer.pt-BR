---
title: Otimizar a velocidade do site com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 7efc76fbcb3d1ed6cbd0760f789c8c952030d70c
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611886"
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





# <span data-ttu-id="df223-103">Otimizar a velocidade do site com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="df223-103">Optimize Website Speed With Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="df223-104">Objetivo do tutorial</span><span class="sxs-lookup"><span data-stu-id="df223-104">Goal of tutorial</span></span>  

<span data-ttu-id="df223-105">Este tutorial ensina a usar o Microsoft Edge DevTools para encontrar formas de fazer com que seus sites sejam carregados mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="df223-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="df223-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="df223-106">Prerequisites</span></span>  

*   <span data-ttu-id="df223-107">Você deve ter experiência básica de desenvolvimento na Web, semelhante ao que é ensinado nesta [introdução à classe de desenvolvimento na Web][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="df223-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="df223-108">Você não precisa saber nada sobre o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="df223-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="df223-109">Saiba mais sobre isso neste tutorial!</span><span class="sxs-lookup"><span data-stu-id="df223-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="df223-110">Introdução</span><span class="sxs-lookup"><span data-stu-id="df223-110">Introduction</span></span>   

<span data-ttu-id="df223-111">Isso é Tony.</span><span class="sxs-lookup"><span data-stu-id="df223-111">This is Tony.</span></span>  <span data-ttu-id="df223-112">Tony é muito famoso na sociedade da gato.</span><span class="sxs-lookup"><span data-stu-id="df223-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="df223-113">Ele criou um site para que seus fãs possam aprender sobre seus alimentos favoritos.</span><span class="sxs-lookup"><span data-stu-id="df223-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="df223-114">Seus fãs adoram o site, mas o Tony mantém reclamações auditivas que o site carrega lentamente.</span><span class="sxs-lookup"><span data-stu-id="df223-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="df223-115">Tony solicitou que você o ajude a acelerar o site.</span><span class="sxs-lookup"><span data-stu-id="df223-115">Tony has asked you to help him speed the site up.</span></span>  

> ##### <span data-ttu-id="df223-116">Figura 1</span><span class="sxs-lookup"><span data-stu-id="df223-116">Figure 1</span></span>  
> <span data-ttu-id="df223-117">Tony o gato</span><span class="sxs-lookup"><span data-stu-id="df223-117">Tony the cat</span></span>  
> ![Tony o gato][ImageTony]  

## <span data-ttu-id="df223-119">Etapa 1: auditar o site</span><span class="sxs-lookup"><span data-stu-id="df223-119">Step 1: Audit the site</span></span>   

<span data-ttu-id="df223-120">Sempre que você se configurar para melhorar o desempenho de carga de um site, **sempre comece com uma auditoria**.</span><span class="sxs-lookup"><span data-stu-id="df223-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="df223-121">A auditoria tem duas funções importantes:</span><span class="sxs-lookup"><span data-stu-id="df223-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="df223-122">Ele cria uma **linha de base** para você medir alterações subsequentes em relação a.</span><span class="sxs-lookup"><span data-stu-id="df223-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="df223-123">Ele oferece **dicas acionáveis** sobre quais alterações têm o maior impacto possível.</span><span class="sxs-lookup"><span data-stu-id="df223-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  

### <span data-ttu-id="df223-124">Configurar</span><span class="sxs-lookup"><span data-stu-id="df223-124">Set up</span></span>   

<span data-ttu-id="df223-125">Primeiro, você deve configurar o site para que possa fazer alterações nele mais tarde.</span><span class="sxs-lookup"><span data-stu-id="df223-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="df223-126">[Abra o código-fonte do site](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="df223-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="df223-127">Esta guia é referida como a **guia Editor**.</span><span class="sxs-lookup"><span data-stu-id="df223-127">This tab is referred to as the **editor tab**.</span></span>  
    
    > ##### <span data-ttu-id="df223-128">Figura 2</span><span class="sxs-lookup"><span data-stu-id="df223-128">Figure 2</span></span>  
    > <span data-ttu-id="df223-129">A guia Editor</span><span class="sxs-lookup"><span data-stu-id="df223-129">The editor tab</span></span>  
    > ![A guia Editor][ImageEditor]  

1.  <span data-ttu-id="df223-131">Selecione **Tony**.</span><span class="sxs-lookup"><span data-stu-id="df223-131">Select **tony**.</span></span>  <span data-ttu-id="df223-132">Um menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="df223-132">A menu appears.</span></span>  
    
    > ##### <span data-ttu-id="df223-133">Figura 3</span><span class="sxs-lookup"><span data-stu-id="df223-133">Figure 3</span></span>  
    > <span data-ttu-id="df223-134">O menu que aparece depois de clicar em **Tony**</span><span class="sxs-lookup"><span data-stu-id="df223-134">The menu that appears after clicking **tony**</span></span>  
    > ![O menu que aparece depois de clicar em Tony][ImageMenu]  
    
1.  <span data-ttu-id="df223-136">Selecione **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="df223-136">Select **Remix Project**.</span></span>  <span data-ttu-id="df223-137">O nome do projeto muda de **Tony** para algum nome gerado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="df223-137">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="df223-138">Agora você tem sua própria cópia editável do código.</span><span class="sxs-lookup"><span data-stu-id="df223-138">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="df223-139">Posteriormente, você pode fazer alterações nesse código.</span><span class="sxs-lookup"><span data-stu-id="df223-139">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="df223-140">Selecione **Mostrar** e selecione **em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="df223-140">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="df223-141">A demonstração é aberta em uma nova guia.  Esta guia é referida como a **guia demonstração**.  Pode levar alguns instantes para que o site seja carregado.</span><span class="sxs-lookup"><span data-stu-id="df223-141">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    > ##### <span data-ttu-id="df223-142">Figura 4</span><span class="sxs-lookup"><span data-stu-id="df223-142">Figure 4</span></span>  
    > <span data-ttu-id="df223-143">A guia demonstração</span><span class="sxs-lookup"><span data-stu-id="df223-143">The demo tab</span></span>  
    > ![A guia demonstração][ImageDemo]  

1.  <span data-ttu-id="df223-145">Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="df223-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="df223-146">O Microsoft Edge DevTools abre juntamente com a demonstração.</span><span class="sxs-lookup"><span data-stu-id="df223-146">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    > ##### <span data-ttu-id="df223-147">Figura 5</span><span class="sxs-lookup"><span data-stu-id="df223-147">Figure 5</span></span>  
    > <span data-ttu-id="df223-148">DevTools e a demonstração</span><span class="sxs-lookup"><span data-stu-id="df223-148">DevTools and the demo</span></span>  
    > ![DevTools e a demonstração][ImageDevtools]  

<span data-ttu-id="df223-150">Para o restante das capturas de tela neste tutorial, DevTools é exibido em uma janela separada.</span><span class="sxs-lookup"><span data-stu-id="df223-150">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="df223-151">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digitando `Undock` e, em seguida, selecione **desencaixar em uma janela separada**.</span><span class="sxs-lookup"><span data-stu-id="df223-151">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

> ##### <span data-ttu-id="df223-152">Figura 6</span><span class="sxs-lookup"><span data-stu-id="df223-152">Figure 6</span></span>  
> <span data-ttu-id="df223-153">DevTools desencaixado</span><span class="sxs-lookup"><span data-stu-id="df223-153">Undocked DevTools</span></span>  
> ![DevTools desencaixado][ImageUndocked]  

### <span data-ttu-id="df223-155">Estabelecer uma linha de base</span><span class="sxs-lookup"><span data-stu-id="df223-155">Establish a baseline</span></span>   

<span data-ttu-id="df223-156">A linha de base é um registro de como o site foi executado antes de você fazer qualquer melhoria no desempenho.</span><span class="sxs-lookup"><span data-stu-id="df223-156">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="df223-157">Selecione a guia **auditorias** .  Ele pode estar oculto atrás do botão **mais** painéis ![ mais painéis ][ImageMorePanelsIcon] .</span><span class="sxs-lookup"><span data-stu-id="df223-157">Select the **Audits** tab.  It may be hidden behind the **More Panels** ![More Panels][ImageMorePanelsIcon] button.</span></span>  <span data-ttu-id="df223-158">Há um Lighthouse neste painel porque o projeto que energiza o painel auditorias é denominado **Lighthouse**.</span><span class="sxs-lookup"><span data-stu-id="df223-158">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    > ##### <span data-ttu-id="df223-159">Figura 7</span><span class="sxs-lookup"><span data-stu-id="df223-159">Figure 7</span></span>  
    > <span data-ttu-id="df223-160">O painel auditorias</span><span class="sxs-lookup"><span data-stu-id="df223-160">The Audits panel</span></span>  
    > ![O painel auditorias][ImageAudits]  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="df223-162">Correspondam às suas configurações de auditoria para as da [Figura 7](#figure-7).</span><span class="sxs-lookup"><span data-stu-id="df223-162">Match your audit configuration settings to those in [Figure 7](#figure-7).</span></span>  <span data-ttu-id="df223-163">Aqui está uma explicação das diferentes opções:</span><span class="sxs-lookup"><span data-stu-id="df223-163">Here is an explanation of the different options:</span></span>  

    *   <span data-ttu-id="df223-164">**Device**.</span><span class="sxs-lookup"><span data-stu-id="df223-164">**Device**.</span></span>  <span data-ttu-id="df223-165">A configuração para **celular** altera a cadeia de caracteres do agente do usuário e simula um visor móvel.</span><span class="sxs-lookup"><span data-stu-id="df223-165">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="df223-166">A configuração para **área de trabalho** simplesmente desabilita as alterações de **celular** .</span><span class="sxs-lookup"><span data-stu-id="df223-166">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="df223-167">**Auditorias**.</span><span class="sxs-lookup"><span data-stu-id="df223-167">**Audits**.</span></span>  <span data-ttu-id="df223-168">A desativação de uma categoria impede que o painel auditorias execute essas auditorias e exclui essas auditorias do relatório.</span><span class="sxs-lookup"><span data-stu-id="df223-168">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="df223-169">Deixe as outras categorias habilitadas, se você quiser ver os tipos de recomendações que são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="df223-169">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="df223-170">Desabilitar categorias ligeiramente acelera o processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="df223-170">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="df223-171">**Limitação**.</span><span class="sxs-lookup"><span data-stu-id="df223-171">**Throttling**.</span></span>  <span data-ttu-id="df223-172">Configuração para **Simulated 4G lenta, a lentidão de CPU de 4** simula as condições típicas de navegação em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="df223-172">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="df223-173">Ele é chamado de "simulado" porque o painel auditorias não é controlado na verdade durante o processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="df223-173">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="df223-174">Em vez disso, ele apenas extrapola o tempo que a página levaria para carregar em condições de celular.</span><span class="sxs-lookup"><span data-stu-id="df223-174">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="df223-175">A configuração **aplicada...** , por outro lado, efetivamente limita sua CPU e rede, com a compensação de um processo de auditoria mais longo.</span><span class="sxs-lookup"><span data-stu-id="df223-175">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="df223-176">**Limpar o armazenamento**.</span><span class="sxs-lookup"><span data-stu-id="df223-176">**Clear Storage**.</span></span>  <span data-ttu-id="df223-177">Habilitar essa caixa de seleção limpa todo o armazenamento associado à página antes de cada auditoria.</span><span class="sxs-lookup"><span data-stu-id="df223-177">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="df223-178">Deixe essa configuração em caso de você desejar auditar como os visitantes da primeira vez que o visitante terão.</span><span class="sxs-lookup"><span data-stu-id="df223-178">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="df223-179">Desative essa configuração quando quiser a experiência de visita de repetição.</span><span class="sxs-lookup"><span data-stu-id="df223-179">Disable this setting when you want the repeat-visit experience.</span></span>  

1.  <span data-ttu-id="df223-180">Selecione **executar auditorias**.</span><span class="sxs-lookup"><span data-stu-id="df223-180">Select **Run Audits**.</span></span>  <span data-ttu-id="df223-181">Após 10 a 30 segundos, o painel auditorias mostra um relatório do desempenho do site.</span><span class="sxs-lookup"><span data-stu-id="df223-181">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    > ##### <span data-ttu-id="df223-182">Figura 8</span><span class="sxs-lookup"><span data-stu-id="df223-182">Figure 8</span></span>  
    > <span data-ttu-id="df223-183">O relatório para o painel auditorias do desempenho do site</span><span class="sxs-lookup"><span data-stu-id="df223-183">The report for the Audits panel of the performance of the site</span></span>  
    > ![O relatório para o painel auditorias do desempenho do site][ImageReport]  

#### <span data-ttu-id="df223-185">Manipulando erros de relatório</span><span class="sxs-lookup"><span data-stu-id="df223-185">Handling report errors</span></span>   

<span data-ttu-id="df223-186">Se você receber um erro no relatório do painel auditorias, tente executar a guia demonstração em uma janela **InPrivate** sem nenhuma outra guia aberta.</span><span class="sxs-lookup"><span data-stu-id="df223-186">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="df223-187">Isso garante que você esteja executando o Microsoft Edge a partir de um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="df223-187">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="df223-188">As extensões do Microsoft Edge em particular geralmente interferem no processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="df223-188">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
> ##### old Figure 9  
> A report that errored  
> ![A report that errored][ImageError]  
-->  

### <span data-ttu-id="df223-189">Entender o relatório</span><span class="sxs-lookup"><span data-stu-id="df223-189">Understand your report</span></span>   

<span data-ttu-id="df223-190">O número na parte superior do seu relatório é a pontuação de desempenho geral do site.</span><span class="sxs-lookup"><span data-stu-id="df223-190">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="df223-191">Posteriormente, ao fazer alterações no código, você verá esse número aumentará.</span><span class="sxs-lookup"><span data-stu-id="df223-191">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="df223-192">Uma pontuação mais alta significa melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="df223-192">A higher score means better performance.</span></span>  

> ##### <span data-ttu-id="df223-193">Figura 9</span><span class="sxs-lookup"><span data-stu-id="df223-193">Figure 9</span></span>  
> <span data-ttu-id="df223-194">A pontuação geral de desempenho</span><span class="sxs-lookup"><span data-stu-id="df223-194">The overall performance score</span></span>  
> <span data-ttu-id="df223-195">! [A pontuação geral de desempenho] [ImageOverall]</span><span class="sxs-lookup"><span data-stu-id="df223-195">![The overall performance score][ImageOverall]</span></span>  

<span data-ttu-id="df223-196">A seção **métricas** fornece medidas quantitativas do desempenho do site.</span><span class="sxs-lookup"><span data-stu-id="df223-196">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="df223-197">Cada métrica fornece uma visão geral de um aspecto diferente do desempenho.</span><span class="sxs-lookup"><span data-stu-id="df223-197">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="df223-198">Por exemplo, a **primeira tinta de conteúdo** informa quando o conteúdo é pintado pela primeira vez na tela, que é uma etapa importante da percepção do usuário da carga da página, enquanto o **tempo para interativo** marca o ponto em que a página parece estar pronta o suficiente para lidar com interações do usuário.</span><span class="sxs-lookup"><span data-stu-id="df223-198">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

> ##### <span data-ttu-id="df223-199">Figura 10</span><span class="sxs-lookup"><span data-stu-id="df223-199">Figure 10</span></span>  
> <span data-ttu-id="df223-200">A seção métricas</span><span class="sxs-lookup"><span data-stu-id="df223-200">The Metrics section</span></span>  
> <span data-ttu-id="df223-201">! [A seção métricas] [ImageMetrics]</span><span class="sxs-lookup"><span data-stu-id="df223-201">![The Metrics section][ImageMetrics]</span></span>  

<span data-ttu-id="df223-202">Selecione o botão de alternância realçado na [Figura 11](#figure-11) para ver uma descrição para cada métrica e clique em **saiba mais** para ler a documentação sobre ela.</span><span class="sxs-lookup"><span data-stu-id="df223-202">Select the highlighted toggle button in [Figure 11](#figure-11) to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

> ##### <span data-ttu-id="df223-203">Figura 11</span><span class="sxs-lookup"><span data-stu-id="df223-203">Figure 11</span></span>  
> <span data-ttu-id="df223-204">Selecione o botão de alternância realçado para expandir os itens de **métricas**</span><span class="sxs-lookup"><span data-stu-id="df223-204">Select the highlighted toggle button to expand the **Metrics** items</span></span>  
> <span data-ttu-id="df223-205">! [Selecione o botão de alternância realçado para expandir os itens de métricas] [ImageFirstMeaningfulPaint]</span><span class="sxs-lookup"><span data-stu-id="df223-205">![Select the highlighted toggle button to expand the Metrics items][ImageFirstMeaningfulPaint]</span></span>  

<span data-ttu-id="df223-206">As métricas a seguir são uma coleção de capturas de tela que mostram como a página parece ser carregada.</span><span class="sxs-lookup"><span data-stu-id="df223-206">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

> ##### <span data-ttu-id="df223-207">Figura 12</span><span class="sxs-lookup"><span data-stu-id="df223-207">Figure 12</span></span>  
> <span data-ttu-id="df223-208">Capturas de tela de como a página ficou ao carregar</span><span class="sxs-lookup"><span data-stu-id="df223-208">Screenshots of how the page looked while loading</span></span>  
> <span data-ttu-id="df223-209">! [Capturas de tela de como a página procurou durante o carregamento] [ImageScreenshots]</span><span class="sxs-lookup"><span data-stu-id="df223-209">![Screenshots of how the page looked while loading][ImageScreenshots]</span></span>  

<span data-ttu-id="df223-210">A seção **oportunidades** fornece dicas específicas sobre como melhorar o desempenho de carga dessa página específica.</span><span class="sxs-lookup"><span data-stu-id="df223-210">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

> ##### <span data-ttu-id="df223-211">Figura 13</span><span class="sxs-lookup"><span data-stu-id="df223-211">Figure 13</span></span>  
> <span data-ttu-id="df223-212">A seção oportunidades</span><span class="sxs-lookup"><span data-stu-id="df223-212">The Opportunities section</span></span>  
> <span data-ttu-id="df223-213">! [A seção oportunidades] [ImageOpportunities]</span><span class="sxs-lookup"><span data-stu-id="df223-213">![The Opportunities section][ImageOpportunities]</span></span>  

<span data-ttu-id="df223-214">Selecione uma oportunidade para saber mais sobre isso.</span><span class="sxs-lookup"><span data-stu-id="df223-214">Select an opportunity to learn more about it.</span></span>  

> ##### <span data-ttu-id="df223-215">Figura 14</span><span class="sxs-lookup"><span data-stu-id="df223-215">Figure 14</span></span>  
> <span data-ttu-id="df223-216">**Eliminar oportunidade de recursos de bloqueio de renderização**</span><span class="sxs-lookup"><span data-stu-id="df223-216">**Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="df223-217">! [Eliminar oportunidade de recursos de bloqueio de renderização] [ImageCompression]</span><span class="sxs-lookup"><span data-stu-id="df223-217">![Eliminate render-blocking resources opportunity][ImageCompression]</span></span>  

<span data-ttu-id="df223-218">Selecione **saiba mais** para ver a documentação sobre por que uma oportunidade é importante e recomendações específicas sobre como corrigi-lo.</span><span class="sxs-lookup"><span data-stu-id="df223-218">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

> ##### <span data-ttu-id="df223-219">Figura 15</span><span class="sxs-lookup"><span data-stu-id="df223-219">Figure 15</span></span>  
> <span data-ttu-id="df223-220">Documentação para a oportunidade de **eliminar recursos de bloqueio de renderização**</span><span class="sxs-lookup"><span data-stu-id="df223-220">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="df223-221">! [Documentação da oportunidade para eliminar recursos de bloqueio de renderização] [ImageReference]</span><span class="sxs-lookup"><span data-stu-id="df223-221">![Documentation for the Eliminate render-blocking resources opportunity][ImageReference]</span></span>  

<span data-ttu-id="df223-222">A seção **diagnóstico** fornece mais informações sobre fatores que contribuem para o tempo de carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="df223-222">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

> ##### <span data-ttu-id="df223-223">Figura 16</span><span class="sxs-lookup"><span data-stu-id="df223-223">Figure 16</span></span>  
> <span data-ttu-id="df223-224">A seção diagnóstico</span><span class="sxs-lookup"><span data-stu-id="df223-224">The Diagnostics section</span></span>  
> <span data-ttu-id="df223-225">! [A seção diagnóstico] [ImageDiagnostics]</span><span class="sxs-lookup"><span data-stu-id="df223-225">![The Diagnostics section][ImageDiagnostics]</span></span>  

<span data-ttu-id="df223-226">A seção de **auditorias passadas** mostra o que o site está fazendo corretamente.</span><span class="sxs-lookup"><span data-stu-id="df223-226">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="df223-227">Selecione para expandir a seção.</span><span class="sxs-lookup"><span data-stu-id="df223-227">Select to expand the section.</span></span>  

> ##### <span data-ttu-id="df223-228">Figura 17</span><span class="sxs-lookup"><span data-stu-id="df223-228">Figure 17</span></span>  
> <span data-ttu-id="df223-229">A seção de auditorias passadas</span><span class="sxs-lookup"><span data-stu-id="df223-229">The Passed Audits section</span></span>  
> <span data-ttu-id="df223-230">! [A seção de auditorias passadas] [ImagePassed]</span><span class="sxs-lookup"><span data-stu-id="df223-230">![The Passed Audits section][ImagePassed]</span></span>  

## <span data-ttu-id="df223-231">Etapa 2: Experimente</span><span class="sxs-lookup"><span data-stu-id="df223-231">Step 2: Experiment</span></span>   

<span data-ttu-id="df223-232">A seção oportunidades do seu relatório de auditoria fornece dicas sobre como melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="df223-232">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="df223-233">Nesta seção, você implementa as alterações recomendadas na base de código, fazendo auditoria do site após cada alteração para medir como ele afeta a velocidade do site.</span><span class="sxs-lookup"><span data-stu-id="df223-233">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="df223-234">Habilitar a compactação de texto</span><span class="sxs-lookup"><span data-stu-id="df223-234">Enable text compression</span></span>   

<span data-ttu-id="df223-235">O relatório informa que evitar cargas de rede enormes é uma das principais oportunidades para melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="df223-235">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="df223-236">Habilitar a compactação de texto é uma oportunidade de melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="df223-236">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="df223-237">A compactação de texto é quando você reduz ou compacta o tamanho de um arquivo de texto antes de enviá-lo pela rede.</span><span class="sxs-lookup"><span data-stu-id="df223-237">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="df223-238">Tipo de como você pode compactar uma pasta antes de enviar um email para ela para reduzir o tamanho.</span><span class="sxs-lookup"><span data-stu-id="df223-238">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="df223-239">Antes de habilitar a compactação, aqui estão algumas maneiras de verificar manualmente se os recursos de texto estão compactados.</span><span class="sxs-lookup"><span data-stu-id="df223-239">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="df223-240">Selecione a guia **rede** .</span><span class="sxs-lookup"><span data-stu-id="df223-240">Select the **Network** tab.</span></span>  
    
    > ##### <span data-ttu-id="df223-241">Figura 18</span><span class="sxs-lookup"><span data-stu-id="df223-241">Figure 18</span></span>  
    > <span data-ttu-id="df223-242">Painel de rede</span><span class="sxs-lookup"><span data-stu-id="df223-242">The Network panel</span></span>  
    > <span data-ttu-id="df223-243">! [O painel rede] [ImageNetwork]</span><span class="sxs-lookup"><span data-stu-id="df223-243">![The Network panel][ImageNetwork]</span></span>  
    
1.  <span data-ttu-id="df223-244">Selecione o ícone de **configuração de rede** .</span><span class="sxs-lookup"><span data-stu-id="df223-244">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="df223-245">Marque a caixa de seleção **usar linhas de solicitação grandes** .</span><span class="sxs-lookup"><span data-stu-id="df223-245">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="df223-246">A altura das linhas na tabela de solicitações de rede aumenta.</span><span class="sxs-lookup"><span data-stu-id="df223-246">The height of the rows in the table of network requests increases.</span></span>  
    
    > ##### <span data-ttu-id="df223-247">Figura 19</span><span class="sxs-lookup"><span data-stu-id="df223-247">Figure 19</span></span>  
    > <span data-ttu-id="df223-248">Linhas grandes na tabela solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="df223-248">Large rows in the network requests table</span></span>  
    > <span data-ttu-id="df223-249">! [Linhas grandes na tabela solicitações de rede] [ImageLargeRows]</span><span class="sxs-lookup"><span data-stu-id="df223-249">![Large rows in the network requests table][ImageLargeRows]</span></span>  
    
1.  <span data-ttu-id="df223-250">Se você não vir a coluna **tamanho** na tabela de solicitações de rede, clique no cabeçalho da tabela e selecione **tamanho**.</span><span class="sxs-lookup"><span data-stu-id="df223-250">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="df223-251">Cada célula de **tamanho** mostra dois valores.</span><span class="sxs-lookup"><span data-stu-id="df223-251">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="df223-252">O valor principal é o tamanho do recurso baixado.</span><span class="sxs-lookup"><span data-stu-id="df223-252">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="df223-253">O valor secundário é o tamanho do recurso descompactado.</span><span class="sxs-lookup"><span data-stu-id="df223-253">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="df223-254">Se os dois valores forem iguais, o recurso não será compactado quando for enviado pela rede.</span><span class="sxs-lookup"><span data-stu-id="df223-254">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="df223-255">Por exemplo, na [Figura 19](#figure-19) os valores superiores e inferiores para `bundle.js` são `1.2 MB` e `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="df223-255">For example, in [Figure 19](#figure-19) the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="df223-256">Verifique a compactação inspecionando os cabeçalhos HTTP de um recurso:</span><span class="sxs-lookup"><span data-stu-id="df223-256">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="df223-257">Selecione **Bundle. js**.</span><span class="sxs-lookup"><span data-stu-id="df223-257">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="df223-258">Selecione a guia **cabeçalhos** .</span><span class="sxs-lookup"><span data-stu-id="df223-258">Select the **Headers** tab.</span></span>  
    
    > ##### <span data-ttu-id="df223-259">Figura 20</span><span class="sxs-lookup"><span data-stu-id="df223-259">Figure 20</span></span>  
    > <span data-ttu-id="df223-260">A guia cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="df223-260">The Headers tab</span></span>  
    > <span data-ttu-id="df223-261">! [A guia cabeçalhos] [ImageHeaders]</span><span class="sxs-lookup"><span data-stu-id="df223-261">![The Headers tab][ImageHeaders]</span></span>  
    
1.  <span data-ttu-id="df223-262">Pesquisar o cabeçalho na seção de **cabeçalhos de resposta** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="df223-262">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="df223-263">Você não deve ver um, o que significa que `bundle.js` não foi compactado.</span><span class="sxs-lookup"><span data-stu-id="df223-263">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="df223-264">Quando um recurso é compactado, esse cabeçalho geralmente é definido como `gzip` , `deflate` ou `br` .</span><span class="sxs-lookup"><span data-stu-id="df223-264">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="df223-265">Consulte [diretrizes][MDNContentEncodingDirectives] para obter uma explicação desses valores.</span><span class="sxs-lookup"><span data-stu-id="df223-265">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="df223-266">Suficiente com as explicações.</span><span class="sxs-lookup"><span data-stu-id="df223-266">Enough with the explanations.</span></span>  <span data-ttu-id="df223-267">É hora de fazer algumas mudanças!</span><span class="sxs-lookup"><span data-stu-id="df223-267">Time to make some changes!</span></span>  <span data-ttu-id="df223-268">Habilite a compactação de texto adicionando algumas linhas de código:</span><span class="sxs-lookup"><span data-stu-id="df223-268">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="df223-269">Na guia Editor, clique em **Server. js**.</span><span class="sxs-lookup"><span data-stu-id="df223-269">In the editor tab, click **server.js**.</span></span>  
    
    > ##### <span data-ttu-id="df223-270">Figura 21</span><span class="sxs-lookup"><span data-stu-id="df223-270">Figure 21</span></span>  
    > <span data-ttu-id="df223-271">Editando Server. js</span><span class="sxs-lookup"><span data-stu-id="df223-271">Editing server.js</span></span>  
    > <span data-ttu-id="df223-272">! [Editing Server. js] [ImageServer]</span><span class="sxs-lookup"><span data-stu-id="df223-272">![Editing server.js][ImageServer]</span></span>  
    
1.  <span data-ttu-id="df223-273">Adicione o código a seguir ao **Server. js**.</span><span class="sxs-lookup"><span data-stu-id="df223-273">Add the following code to **server.js**.</span></span>  <span data-ttu-id="df223-274">Certifique-se de colocar `app.use(compression())` antes `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="df223-274">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="df223-275">Geralmente, você precisa instalar o `compression` pacote por algo semelhante `npm i -S compression` , mas isso já foi feito para você.</span><span class="sxs-lookup"><span data-stu-id="df223-275">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="df223-276">Aguarde até que a falha implante a nova compilação do site.</span><span class="sxs-lookup"><span data-stu-id="df223-276">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="df223-277">A animação sofisticada ao lado de **ferramentas** significa que o site está sendo recriado e reimplantado.</span><span class="sxs-lookup"><span data-stu-id="df223-277">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="df223-278">A alteração estará pronta quando a animação ao lado de **ferramentas** ficar ausente.</span><span class="sxs-lookup"><span data-stu-id="df223-278">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="df223-279">Selecione **Mostrar** e selecione novamente **em uma nova janela** .</span><span class="sxs-lookup"><span data-stu-id="df223-279">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    > ##### Old Figure 22  
    > The animation that indicates that the site is getting built  
    > ![The animation that indicates that the site is getting built][ImageBuilding]  
    -->  
    
<span data-ttu-id="df223-280">Use os fluxos de trabalho que você aprendeu anteriormente para verificar manualmente se a compactação está funcionando:</span><span class="sxs-lookup"><span data-stu-id="df223-280">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="df223-281">Volte para a guia demonstração e recarregue a página.</span><span class="sxs-lookup"><span data-stu-id="df223-281">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="df223-282">A coluna **tamanho** agora deve mostrar 2 valores diferentes para recursos de texto, como `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="df223-282">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="df223-283">Na [Figura 23](#figure-23) , o valor principal de for `256 KB` `bundle.js` é o tamanho do arquivo que foi enviado pela rede e o valor inferior de `1.2 MB` é o tamanho do arquivo descompactado.</span><span class="sxs-lookup"><span data-stu-id="df223-283">In [Figure 23](#figure-23) the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    > ##### <span data-ttu-id="df223-284">Figura 22</span><span class="sxs-lookup"><span data-stu-id="df223-284">Figure 22</span></span>  
    > <span data-ttu-id="df223-285">A coluna tamanho agora mostra 2 valores diferentes para recursos de texto</span><span class="sxs-lookup"><span data-stu-id="df223-285">The Size column now shows 2 different values for text resources</span></span>  
    > <span data-ttu-id="df223-286">! [A coluna tamanho agora mostra 2 valores diferentes para recursos de texto] [ImageRequests]</span><span class="sxs-lookup"><span data-stu-id="df223-286">![The Size column now shows 2 different values for text resources][ImageRequests]</span></span>  
    
1.  <span data-ttu-id="df223-287">A seção de **cabeçalhos de resposta** para `bundle.js` agora deve incluir um `content-encoding: gzip` cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="df223-287">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    > ##### <span data-ttu-id="df223-288">Figura 23</span><span class="sxs-lookup"><span data-stu-id="df223-288">Figure 23</span></span>  
    > <span data-ttu-id="df223-289">A seção de cabeçalhos de resposta agora contém um cabeçalho de codificação de conteúdo</span><span class="sxs-lookup"><span data-stu-id="df223-289">The Response Headers section now contains a content-encoding header</span></span>  
    > <span data-ttu-id="df223-290">! [A seção de cabeçalhos de resposta agora contém um cabeçalho de codificação de conteúdo] [ImageGzip]</span><span class="sxs-lookup"><span data-stu-id="df223-290">![The Response Headers section now contains a content-encoding header][ImageGzip]</span></span>  
    
<span data-ttu-id="df223-291">Faça a auditoria da página novamente para medir o tipo de compactação de texto de impacto no desempenho de carga da página:</span><span class="sxs-lookup"><span data-stu-id="df223-291">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="df223-292">Selecione a guia **auditorias** .</span><span class="sxs-lookup"><span data-stu-id="df223-292">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="df223-293">Selecione **executar uma auditoria** ![ executar uma auditoria ][ImagePerformIcon] .</span><span class="sxs-lookup"><span data-stu-id="df223-293">Select **Perform an audit** ![Perform an audit][ImagePerformIcon].</span></span>  
1.  <span data-ttu-id="df223-294">Deixe as configurações iguais às anteriores.</span><span class="sxs-lookup"><span data-stu-id="df223-294">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="df223-295">Selecione **executar auditoria**.</span><span class="sxs-lookup"><span data-stu-id="df223-295">Select **Run audit**.</span></span>  
    
    > ##### <span data-ttu-id="df223-296">Figura 24</span><span class="sxs-lookup"><span data-stu-id="df223-296">Figure 24</span></span>  
    > <span data-ttu-id="df223-297">Um relatório de auditorias após a habilitação da compactação de texto</span><span class="sxs-lookup"><span data-stu-id="df223-297">An Audits report after enabling text compression</span></span>  
    > <span data-ttu-id="df223-298">! [Um relatório de auditorias após a habilitação da compactação de texto] [ImageReport2]</span><span class="sxs-lookup"><span data-stu-id="df223-298">![An Audits report after enabling text compression][ImageReport2]</span></span>  
    
<span data-ttu-id="df223-299">Woohoo!</span><span class="sxs-lookup"><span data-stu-id="df223-299">Woohoo!</span></span>  <span data-ttu-id="df223-300">Isso tem a aparência do progresso.</span><span class="sxs-lookup"><span data-stu-id="df223-300">That looks like progress.</span></span>  <span data-ttu-id="df223-301">A pontuação geral do desempenho deve ter aumentado, o que significa que o site está ficando mais rápido.</span><span class="sxs-lookup"><span data-stu-id="df223-301">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="df223-302">Compactação de texto no mundo real</span><span class="sxs-lookup"><span data-stu-id="df223-302">Text compression in the real world</span></span>   

<span data-ttu-id="df223-303">A maioria dos servidores tem correções simples como essa para habilitar a compactação!</span><span class="sxs-lookup"><span data-stu-id="df223-303">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="df223-304">Basta fazer uma busca em como configurar o servidor que você usa para compactar texto.</span><span class="sxs-lookup"><span data-stu-id="df223-304">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="df223-305">Redimensionar imagens</span><span class="sxs-lookup"><span data-stu-id="df223-305">Resize images</span></span>   

<span data-ttu-id="df223-306">O relatório indica que evitar cargas de rede enormes é uma das principais oportunidades para melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="df223-306">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="df223-307">O redimensionamento de imagens ajuda a reduzir o tamanho da carga de rede.</span><span class="sxs-lookup"><span data-stu-id="df223-307">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="df223-308">Se o usuário estiver exibindo as imagens em uma tela de dispositivo móvel com 500 pixels de largura, não há nenhum ponto em enviar uma imagem de 1500 pixels para todo o seu país.</span><span class="sxs-lookup"><span data-stu-id="df223-308">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="df223-309">O ideal é que você envie uma imagem de 500 pixels para todo o tempo.</span><span class="sxs-lookup"><span data-stu-id="df223-309">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="df223-310">Em seu relatório, clique em **evitar enormes cargas de rede** para ver quais imagens devem ser redimensionadas.</span><span class="sxs-lookup"><span data-stu-id="df223-310">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="df223-311">Ele se parece com 2 dos arquivos jpg há mais de 2000 KB, o que é maior do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="df223-311">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    > ##### Old Figure 27  
    > Details about the **Properly size images** opportunity  
    > ![Details about the properly size images opportunity][ImageResize]  
    -->

1.  <span data-ttu-id="df223-312">De volta na guia Editor, abra `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="df223-312">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="df223-313">Substituir `const dir = 'big'` por `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="df223-313">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="df223-314">Esse diretório contém cópias das mesmas imagens que foram redimensionadas.</span><span class="sxs-lookup"><span data-stu-id="df223-314">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="df223-315">Faça a auditoria da página novamente para ver como essa alteração afeta o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="df223-315">Audit the page again to see how this change affects load performance.</span></span>  
    
    > ##### <span data-ttu-id="df223-316">Figura 25</span><span class="sxs-lookup"><span data-stu-id="df223-316">Figure 25</span></span>  
    > <span data-ttu-id="df223-317">Um relatório de auditorias após o redimensionamento de imagens</span><span class="sxs-lookup"><span data-stu-id="df223-317">An Audits report after resizing images</span></span>  
    > <span data-ttu-id="df223-318">! [Um relatório de auditorias após o redimensionamento de imagens] [ImageReport3]</span><span class="sxs-lookup"><span data-stu-id="df223-318">![An Audits report after resizing images][ImageReport3]</span></span>  

<span data-ttu-id="df223-319">Parece que a alteração tem apenas um efeito secundário na pontuação de desempenho geral.</span><span class="sxs-lookup"><span data-stu-id="df223-319">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="df223-320">No entanto, uma coisa que a pontuação não mostra claramente é o número de dados de rede que você está salvando os usuários.</span><span class="sxs-lookup"><span data-stu-id="df223-320">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="df223-321">O tamanho total das fotos antigas era cerca de 5,3 megabytes, enquanto agora só há cerca de 0,18 megabytes.</span><span class="sxs-lookup"><span data-stu-id="df223-321">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="df223-322">Redimensionamento de imagens no mundo real</span><span class="sxs-lookup"><span data-stu-id="df223-322">Resizing images in the real world</span></span>   

<span data-ttu-id="df223-323">Para um aplicativo pequeno, fazer um redimensionamento único como este pode ser bom o suficiente.</span><span class="sxs-lookup"><span data-stu-id="df223-323">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="df223-324">Mas para um aplicativo grande, isso obviamente não é dimensionável.</span><span class="sxs-lookup"><span data-stu-id="df223-324">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="df223-325">Aqui estão algumas estratégias para o gerenciamento de imagens em aplicativos grandes:</span><span class="sxs-lookup"><span data-stu-id="df223-325">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="df223-326">Redimensione imagens durante o processo de compilação.</span><span class="sxs-lookup"><span data-stu-id="df223-326">Resize images during your build process.</span></span>  
*   <span data-ttu-id="df223-327">Crie vários tamanhos de cada imagem durante o processo de compilação e, em seguida, use `srcset` em seu código.</span><span class="sxs-lookup"><span data-stu-id="df223-327">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="df223-328">Em tempo de execução, o navegador cuida da escolha de qual tamanho é melhor para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df223-328">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->

<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="df223-329">Use um CDN de imagem que permita redimensionar dinamicamente uma imagem quando você solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="df223-329">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="df223-330">No mínimo, otimize cada imagem.</span><span class="sxs-lookup"><span data-stu-id="df223-330">At the very least, optimize each image.</span></span>  <span data-ttu-id="df223-331">Isso pode criar uma grande economia.</span><span class="sxs-lookup"><span data-stu-id="df223-331">This may create huge savings.</span></span>  
  <span data-ttu-id="df223-332">A otimização é quando você executa uma imagem por meio de um programa especial que reduz o tamanho do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="df223-332">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="df223-333">Consulte [otimizações de imagem essenciais][EssentialImageOptimization] para obter mais dicas.</span><span class="sxs-lookup"><span data-stu-id="df223-333">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  

### <span data-ttu-id="df223-334">Eliminar recursos de bloqueio de renderização</span><span class="sxs-lookup"><span data-stu-id="df223-334">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="df223-335">O relatório mais recente diz que eliminar recursos de bloqueio de renderização agora é a maior oportunidade.</span><span class="sxs-lookup"><span data-stu-id="df223-335">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="df223-336">Um recurso de bloqueio de renderização é um arquivo JavaScript ou CSS externo que o navegador deve baixar, analisar e executar antes de exibir a página.</span><span class="sxs-lookup"><span data-stu-id="df223-336">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="df223-337">O objetivo é executar somente o código CSS básico e JavaScript que é necessário para exibir a página corretamente.</span><span class="sxs-lookup"><span data-stu-id="df223-337">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="df223-338">A primeira tarefa, então, é encontrar o código que você não precisa executar no carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="df223-338">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="df223-339">Selecione **eliminar recursos de bloqueio de renderização** para ver os recursos que estão bloqueando:</span><span class="sxs-lookup"><span data-stu-id="df223-339">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="df223-340">e `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="df223-340">and `jquery.js`.</span></span>  
    
    > ##### <span data-ttu-id="df223-341">Figura 26</span><span class="sxs-lookup"><span data-stu-id="df223-341">Figure 26</span></span>  
    > <span data-ttu-id="df223-342">Mais informações sobre a oportunidade de **eliminar recursos de bloqueio de renderização**</span><span class="sxs-lookup"><span data-stu-id="df223-342">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    > <span data-ttu-id="df223-343">! [Mais informações sobre a oportunidade de eliminar recursos de bloqueio de renderização] [ImageRender]</span><span class="sxs-lookup"><span data-stu-id="df223-343">![More information about the Eliminate render-blocking resources opportunity][ImageRender]</span></span>  
    
1.  <span data-ttu-id="df223-344">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, comece a digitar `Coverage` e selecione **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="df223-344">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    > ##### <span data-ttu-id="df223-345">Figura 27</span><span class="sxs-lookup"><span data-stu-id="df223-345">Figure 27</span></span>  
    > <span data-ttu-id="df223-346">Abrindo o menu de comando do painel auditorias</span><span class="sxs-lookup"><span data-stu-id="df223-346">Opening the Command Menu from the Audits panel</span></span>  
    > <span data-ttu-id="df223-347">! [Abrindo o menu de comando do painel auditorias] [ImageCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="df223-347">![Opening the Command Menu from the Audits panel][ImageCommandMenu]</span></span>  
    
    > ##### <span data-ttu-id="df223-348">Figura 28</span><span class="sxs-lookup"><span data-stu-id="df223-348">Figure 28</span></span>  
    > <span data-ttu-id="df223-349">A guia cobertura</span><span class="sxs-lookup"><span data-stu-id="df223-349">The Coverage tab</span></span>  
    > <span data-ttu-id="df223-350">! [A guia cobertura] [ImageCoverage]</span><span class="sxs-lookup"><span data-stu-id="df223-350">![The Coverage tab][ImageCoverage]</span></span>  
    
1.  <span data-ttu-id="df223-351">Selecione **Atualizar** ![ atualização ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="df223-351">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="df223-352">A guia **cobertura** fornece uma visão geral da quantidade de código em `bundle.js` , `jquery.js` e `lodash.js` é executada enquanto a página é carregada.</span><span class="sxs-lookup"><span data-stu-id="df223-352">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="df223-353">A [Figura 30](#figure-30) diz que cerca de 76% e 30% dos arquivos jQuery e Lodash não são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="df223-353">[Figure 30](#figure-30) says that about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    > ##### <span data-ttu-id="df223-354">Figura 29</span><span class="sxs-lookup"><span data-stu-id="df223-354">Figure 29</span></span>  
    > <span data-ttu-id="df223-355">O relatório de cobertura</span><span class="sxs-lookup"><span data-stu-id="df223-355">The Coverage report</span></span>  
    > <span data-ttu-id="df223-356">! [O relatório de cobertura] [ImageCoverageReport]</span><span class="sxs-lookup"><span data-stu-id="df223-356">![The Coverage report][ImageCoverageReport]</span></span>  
    
1.  <span data-ttu-id="df223-357">Selecione a linha **jQuery. js** .</span><span class="sxs-lookup"><span data-stu-id="df223-357">Select the **jquery.js** row.</span></span>  <span data-ttu-id="df223-358">DevTools abre o arquivo no painel fontes.</span><span class="sxs-lookup"><span data-stu-id="df223-358">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="df223-359">Uma linha de código foi executada se tiver uma barra azul ao lado dela.</span><span class="sxs-lookup"><span data-stu-id="df223-359">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="df223-360">Uma barra vermelha significa que ela não foi executada e não é necessária na carga da página.</span><span class="sxs-lookup"><span data-stu-id="df223-360">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    > ##### <span data-ttu-id="df223-361">Figura 30</span><span class="sxs-lookup"><span data-stu-id="df223-361">Figure 30</span></span>  
    > <span data-ttu-id="df223-362">Visualizar o arquivo jQuery no painel fontes</span><span class="sxs-lookup"><span data-stu-id="df223-362">Viewing the jQuery file in the Sources panel</span></span>  
    > <span data-ttu-id="df223-363">! [Exibindo o arquivo jQuery no painel fontes] [ImageJQuery]</span><span class="sxs-lookup"><span data-stu-id="df223-363">![Viewing the jQuery file in the Sources panel][ImageJQuery]</span></span>  
    
1.  <span data-ttu-id="df223-364">Role pelo código jQuery um pouco.</span><span class="sxs-lookup"><span data-stu-id="df223-364">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="df223-365">Na verdade, algumas das linhas que recebem "executar" são apenas comentários.</span><span class="sxs-lookup"><span data-stu-id="df223-365">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="df223-366">Executar esse código por meio de um Minifier que retira comentários é outra maneira de reduzir o tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="df223-366">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="df223-367">Resumindo, quando você estiver trabalhando com seu próprio código, a guia cobertura o ajudará a analisar o código, linha por linha, e enviar somente o código necessário para a carga da página.</span><span class="sxs-lookup"><span data-stu-id="df223-367">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="df223-368">Os `jquery.js` arquivos e os `lodash.js` arquivos ainda são necessários para carregar a página?</span><span class="sxs-lookup"><span data-stu-id="df223-368">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="df223-369">A guia solicitar bloqueio exibe o que acontece quando os recursos não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="df223-369">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="df223-370">Selecione a guia **rede** .</span><span class="sxs-lookup"><span data-stu-id="df223-370">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="df223-371">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando novamente.</span><span class="sxs-lookup"><span data-stu-id="df223-371">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="df223-372">Comece a digitar `blocking` e selecione **Mostrar bloqueio de solicitações**.</span><span class="sxs-lookup"><span data-stu-id="df223-372">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    > ##### <span data-ttu-id="df223-373">Figura 31</span><span class="sxs-lookup"><span data-stu-id="df223-373">Figure 31</span></span>  
    > <span data-ttu-id="df223-374">A guia bloqueio de solicitação</span><span class="sxs-lookup"><span data-stu-id="df223-374">The Request Blocking tab</span></span>  
    > <span data-ttu-id="df223-375">! [A guia bloqueio de solicitação] [ImageBlocking]</span><span class="sxs-lookup"><span data-stu-id="df223-375">![The Request Blocking tab][ImageBlocking]</span></span>  
    
1.  <span data-ttu-id="df223-376">Selecione **Adicionar padrão** ![ Adicionar padrão ][ImageAddPatternIcon] , tipo `/libs/*` e, em seguida, pressione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="df223-376">Select **Add Pattern** ![Add Pattern][ImageAddPatternIcon], type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    > ##### <span data-ttu-id="df223-377">Figura 32</span><span class="sxs-lookup"><span data-stu-id="df223-377">Figure 32</span></span>  
    > <span data-ttu-id="df223-378">Adicionando um padrão para bloquear qualquer solicitação ao `libs` diretório</span><span class="sxs-lookup"><span data-stu-id="df223-378">Adding a pattern to block any request to the `libs` directory</span></span>  
    > <span data-ttu-id="df223-379">! [Adicionar um padrão para bloquear qualquer solicitação para o diretório libs] [ImageLibs]</span><span class="sxs-lookup"><span data-stu-id="df223-379">![Adding a pattern to block any request to the libs directory][ImageLibs]</span></span>  
    
1.  <span data-ttu-id="df223-380">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="df223-380">Refresh the page.</span></span>  <span data-ttu-id="df223-381">As solicitações jQuery e Lodash são vermelhas, o que significa que as solicitações foram bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="df223-381">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="df223-382">A página ainda é carregada e é interativa, portanto, parece que esses recursos não são necessários!</span><span class="sxs-lookup"><span data-stu-id="df223-382">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    > ##### <span data-ttu-id="df223-383">Figura 33</span><span class="sxs-lookup"><span data-stu-id="df223-383">Figure 33</span></span>  
    > <span data-ttu-id="df223-384">O painel Rede mostra que as solicitações foram bloqueadas</span><span class="sxs-lookup"><span data-stu-id="df223-384">The Network panel shows that the requests have been blocked</span></span>  
    > <span data-ttu-id="df223-385">! [O painel Rede mostra que as solicitações foram bloqueadas] [ImageBlockedLibs]</span><span class="sxs-lookup"><span data-stu-id="df223-385">![The Network panel shows that the requests have been blocked][ImageBlockedLibs]</span></span>  
    
1.  <span data-ttu-id="df223-386">Selecione **remover todos os padrões** ![ remover todos os padrões ][ImageRemoveIcon] para excluir o `/libs/*` padrão de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="df223-386">Select **Remove all patterns** ![Remove all patterns][ImageRemoveIcon] to delete the `/libs/*` blocking pattern.</span></span>  

<span data-ttu-id="df223-387">Em geral, a guia bloqueio de solicitação é útil para simular como a sua página se comporta quando um determinado recurso não está disponível.</span><span class="sxs-lookup"><span data-stu-id="df223-387">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="df223-388">Agora, remova as referências a esses arquivos do código e faça a auditoria da página novamente:</span><span class="sxs-lookup"><span data-stu-id="df223-388">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="df223-389">De volta na guia Editor, abra `template.html` .</span><span class="sxs-lookup"><span data-stu-id="df223-389">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="df223-390">Exclua `<script src="/libs/lodash.js">` e `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="df223-390">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="df223-391">Aguarde até que o site reconstrua e implante novamente.</span><span class="sxs-lookup"><span data-stu-id="df223-391">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="df223-392">Faça a auditoria da página novamente no painel **auditorias** .</span><span class="sxs-lookup"><span data-stu-id="df223-392">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="df223-393">Sua pontuação geral deve ter sido aprimorada novamente.</span><span class="sxs-lookup"><span data-stu-id="df223-393">Your overall score should have improved again.</span></span>  
    
    > ##### <span data-ttu-id="df223-394">Figura 34</span><span class="sxs-lookup"><span data-stu-id="df223-394">Figure 34</span></span>  
    > <span data-ttu-id="df223-395">Um relatório de auditorias após a remoção dos recursos de bloqueio de renderização</span><span class="sxs-lookup"><span data-stu-id="df223-395">An Audits report after removing the render-blocking resources</span></span>  
    > <span data-ttu-id="df223-396">! [Um relatório de auditorias após a remoção dos recursos de bloqueio de renderização] [ImageReport4]</span><span class="sxs-lookup"><span data-stu-id="df223-396">![An Audits report after removing the render-blocking resources][ImageReport4]</span></span>  

#### <span data-ttu-id="df223-397">Otimizando o caminho de renderização crítica no mundo real</span><span class="sxs-lookup"><span data-stu-id="df223-397">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="df223-398">O **caminho de renderização crítica** se refere ao código que você precisa para carregar uma página.</span><span class="sxs-lookup"><span data-stu-id="df223-398">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="df223-399">Em geral, acelere a carga da página, enviando apenas o código Critical durante o carregamento da página e, em seguida, carregando tudo o mais.</span><span class="sxs-lookup"><span data-stu-id="df223-399">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="df223-400">É improvável que você possa encontrar scripts que você pode remover, mas pode encontrar muitos scripts que você não precisa solicitar durante o carregamento da página e, em vez disso, pode ser solicitado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="df223-400">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="df223-401">Se você estiver usando uma estrutura, verifique se ela tem um modo de produção.</span><span class="sxs-lookup"><span data-stu-id="df223-401">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="df223-402">Esse modo pode usar um recurso como o de uma [árvore][WebpackTreeShaking] para eliminar o código desnecessário que está bloqueando o render crítico.</span><span class="sxs-lookup"><span data-stu-id="df223-402">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  

<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="df223-403">Executar menos trabalho do thread principal</span><span class="sxs-lookup"><span data-stu-id="df223-403">Do less main thread work</span></span>   

<span data-ttu-id="df223-404">O relatório mais recente mostra algumas economias em potencial mínimas na seção oportunidades, mas se você olhar para baixo na seção diagnósticos, parece que o maior afunilamento é muito grande na atividade thread principal.</span><span class="sxs-lookup"><span data-stu-id="df223-404">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="df223-405">O thread principal é onde o navegador faz a maior parte do trabalho necessário para exibir uma página, como análise e execução de HTML, CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="df223-405">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="df223-406">O objetivo é usar o painel desempenho para analisar qual trabalho o thread principal está fazendo enquanto a página é carregada e localizar maneiras de adiar ou remover o trabalho desnecessário.</span><span class="sxs-lookup"><span data-stu-id="df223-406">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="df223-407">Selecione a guia **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="df223-407">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="df223-408">Selecione **capturar** configurações de captura de configurações ![ ][ImageCaptureIcon] .</span><span class="sxs-lookup"><span data-stu-id="df223-408">Select **Capture Settings** ![Capture Settings][ImageCaptureIcon].</span></span>  
1.  <span data-ttu-id="df223-409">Defina a **rede** para 3G e **CPU** **lenta** para **6X de lentidão**.</span><span class="sxs-lookup"><span data-stu-id="df223-409">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="df223-410">Dispositivos móveis geralmente têm mais restrições de hardware do que laptops ou desktops, portanto, essas configurações permitem que você experimente a carga da página como se estivesse usando um dispositivo menos potente.</span><span class="sxs-lookup"><span data-stu-id="df223-410">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="df223-411">Selecione **Atualizar** ![ atualização ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="df223-411">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="df223-412">O DevTools atualiza a página e, em seguida, produz uma visualização de todo o trabalho realizado para carregar a página.</span><span class="sxs-lookup"><span data-stu-id="df223-412">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="df223-413">Essa visualização é chamada de **rastreamento**.</span><span class="sxs-lookup"><span data-stu-id="df223-413">This visualization is referred to as the **trace**.</span></span>  
    
    > ##### <span data-ttu-id="df223-414">Figura 35</span><span class="sxs-lookup"><span data-stu-id="df223-414">Figure 35</span></span>  
    > <span data-ttu-id="df223-415">O rastreamento do painel desempenho do carregamento da página</span><span class="sxs-lookup"><span data-stu-id="df223-415">The Performance panel trace of the page load</span></span>  
    > <span data-ttu-id="df223-416">! [O rastreamento do painel desempenho do carregamento da página] [ImagePerformance]</span><span class="sxs-lookup"><span data-stu-id="df223-416">![The Performance panel trace of the page load][ImagePerformance]</span></span>  

<span data-ttu-id="df223-417">O rastreamento mostra a atividade cronologicamente, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="df223-417">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="df223-418">Os gráficos de FPS, CPU e NET na parte superior fornecem uma visão geral de quadros por segundo, atividade de CPU e atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="df223-418">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="df223-419">O bloco de amarelo selecionado que você vê na [figura 37](#figure-37) significa que a CPU estava completamente ocupada com a atividade de script.</span><span class="sxs-lookup"><span data-stu-id="df223-419">The block of yellow selected that you see in [Figure 37](#figure-37) means that the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="df223-420">Trata-se de uma pista de que você pode acelerar o carregamento da página fazendo menos trabalho em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="df223-420">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

> ##### <span data-ttu-id="df223-421">Figura 36</span><span class="sxs-lookup"><span data-stu-id="df223-421">Figure 36</span></span>  
> <span data-ttu-id="df223-422">A seção visão geral do rastreamento</span><span class="sxs-lookup"><span data-stu-id="df223-422">The Overview section of the trace</span></span>  
> <span data-ttu-id="df223-423">! [A seção visão geral do rastreamento] [ImageOverview]</span><span class="sxs-lookup"><span data-stu-id="df223-423">![The Overview section of the trace][ImageOverview]</span></span>  

<span data-ttu-id="df223-424">Investigue o rastreamento para encontrar formas de fazer menos trabalho em JavaScript:</span><span class="sxs-lookup"><span data-stu-id="df223-424">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="df223-425">Selecione a seção **intervalos** para expandi-la.</span><span class="sxs-lookup"><span data-stu-id="df223-425">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="df223-426">De acordo com o fato de que pode haver uma série de medidas de [tempo][MDNUserTimingApi] de reagir, parece que o aplicativo de Tony está usando o modo de desenvolvimento de reagir.</span><span class="sxs-lookup"><span data-stu-id="df223-426">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="df223-427">Alternar para o modo de produção de reagir pode produzir um pouco de desempenho simples.</span><span class="sxs-lookup"><span data-stu-id="df223-427">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    > ##### <span data-ttu-id="df223-428">Figura 37</span><span class="sxs-lookup"><span data-stu-id="df223-428">Figure 37</span></span>  
    > <span data-ttu-id="df223-429">A seção intervalos</span><span class="sxs-lookup"><span data-stu-id="df223-429">The Timings section</span></span>  
    > <span data-ttu-id="df223-430">! [A seção intervalos] [ImageUserTiming]</span><span class="sxs-lookup"><span data-stu-id="df223-430">![The Timings section][ImageUserTiming]</span></span>  

1.  <span data-ttu-id="df223-431">Selecione **intervalos** novamente para recolher essa seção.</span><span class="sxs-lookup"><span data-stu-id="df223-431">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="df223-432">Procure a seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="df223-432">Browse the **Main** section.</span></span>  <span data-ttu-id="df223-433">Esta seção mostra um log cronológico da atividade de thread principal, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="df223-433">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="df223-434">O eixo y (de cima para baixo) mostra o motivo pelo qual os eventos ocorreram.</span><span class="sxs-lookup"><span data-stu-id="df223-434">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="df223-435">Por exemplo, na [figura 39](#figure-39), o `Evaluate Script` evento causou a `(anonymous)` execução da função, que causou a execução, `(anonymous)` que causou `__webpack__require__` a execução e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="df223-435">For example, in [Figure 39](#figure-39), the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    > ##### <span data-ttu-id="df223-436">Figura 38</span><span class="sxs-lookup"><span data-stu-id="df223-436">Figure 38</span></span>  
    > <span data-ttu-id="df223-437">A seção principal</span><span class="sxs-lookup"><span data-stu-id="df223-437">The Main section</span></span>  
    > <span data-ttu-id="df223-438">! [A seção principal] [ImageMain]</span><span class="sxs-lookup"><span data-stu-id="df223-438">![The Main section][ImageMain]</span></span>  

1.  <span data-ttu-id="df223-439">Role a tela para baixo até a parte inferior da seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="df223-439">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="df223-440">Quando você usa uma estrutura, a maior parte da atividade superior é causada pela estrutura, que normalmente está fora do seu controle.</span><span class="sxs-lookup"><span data-stu-id="df223-440">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="df223-441">A atividade causada pelo aplicativo geralmente está na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="df223-441">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="df223-442">Nesse aplicativo, parece que uma função nomeada `App` está causando muitas solicitações para uma `mineBitcoin` função.</span><span class="sxs-lookup"><span data-stu-id="df223-442">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="df223-443">Parece que Tony pode estar usando os dispositivos de seus fãs para o meu cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="df223-443">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    > ##### <span data-ttu-id="df223-444">Figura 39</span><span class="sxs-lookup"><span data-stu-id="df223-444">Figure 39</span></span>  
    > <span data-ttu-id="df223-445">Passando o mouse sobre a `mineBitcoin` atividade</span><span class="sxs-lookup"><span data-stu-id="df223-445">Hovering over the `mineBitcoin` activity</span></span>  
    > <span data-ttu-id="df223-446">! [Passando o mouse sobre a atividade mineBitcoin] [ImageMine]</span><span class="sxs-lookup"><span data-stu-id="df223-446">![Hovering over the mineBitcoin activity][ImageMine]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="df223-447">Embora as solicitações que a sua estrutura fazer normalmente sejam de seu controle, às vezes você pode estruturar seu aplicativo de uma maneira que faz com que a estrutura seja executada ineficientemente.</span><span class="sxs-lookup"><span data-stu-id="df223-447">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="df223-448">Reestruturar seu aplicativo para usar a estrutura com eficiência é uma maneira de fazer menos trabalho do thread principal.</span><span class="sxs-lookup"><span data-stu-id="df223-448">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="df223-449">No entanto, isso exige uma compreensão profunda de como a estrutura funciona e o tipo de alterações feitas em seu próprio código para usar a estrutura com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="df223-449">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  

1.  <span data-ttu-id="df223-450">Expanda a seção de **baixo para cima** .</span><span class="sxs-lookup"><span data-stu-id="df223-450">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="df223-451">Esta guia quebra quais atividades levaram mais tempo.</span><span class="sxs-lookup"><span data-stu-id="df223-451">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="df223-452">Se você não vir nada na seção de baixo para cima, clique no rótulo da seção **principal** .</span><span class="sxs-lookup"><span data-stu-id="df223-452">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="df223-453">A seção de **baixo para cima** mostra apenas as informações sobre qualquer atividade ou grupo de atividades selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="df223-453">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="df223-454">Por exemplo, se você clicou em uma das `mineBitcoin` atividades, a seção de **baixo para cima** só irá mostrar as informações de uma atividade.</span><span class="sxs-lookup"><span data-stu-id="df223-454">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    > ##### <span data-ttu-id="df223-455">Figura 40</span><span class="sxs-lookup"><span data-stu-id="df223-455">Figure 40</span></span>  
    > <span data-ttu-id="df223-456">A guia seta para baixo</span><span class="sxs-lookup"><span data-stu-id="df223-456">The Bottom-Up tab</span></span>  
    > <span data-ttu-id="df223-457">! [A guia superior] [ImageBottomUp]</span><span class="sxs-lookup"><span data-stu-id="df223-457">![The Bottom-Up tab][ImageBottomUp]</span></span>  

<span data-ttu-id="df223-458">A coluna **autotempo** mostra quanto tempo foi gasto diretamente em cada atividade.</span><span class="sxs-lookup"><span data-stu-id="df223-458">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="df223-459">Por exemplo, a [figura 41](#figure-41) mostra que cerca de 63% do tempo do thread principal foi gasto na `mineBitcoin` função.</span><span class="sxs-lookup"><span data-stu-id="df223-459">For example, [Figure 41](#figure-41) shows that about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="df223-460">Tempo para ver se o uso do modo de produção e da redução da atividade JavaScript pode acelerar o carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="df223-460">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="df223-461">Comece com o modo de produção:</span><span class="sxs-lookup"><span data-stu-id="df223-461">Start with production mode:</span></span>  

1.  <span data-ttu-id="df223-462">Na guia Editor, abra `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="df223-462">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="df223-463">Alterar `"mode":"development"` para `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="df223-463">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="df223-464">Aguarde até que a nova compilação seja implementada.</span><span class="sxs-lookup"><span data-stu-id="df223-464">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="df223-465">Faça a auditoria da página novamente.</span><span class="sxs-lookup"><span data-stu-id="df223-465">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="df223-466">Figura 41</span><span class="sxs-lookup"><span data-stu-id="df223-466">Figure 41</span></span>  
    > <span data-ttu-id="df223-467">Um relatório de auditorias após a configuração do webpack para usar o modo de produção</span><span class="sxs-lookup"><span data-stu-id="df223-467">An Audits report after configuring webpack to use production mode</span></span>  
    > <span data-ttu-id="df223-468">! [Um relatório de auditorias após a configuração do webpack para usar o modo de produção] [ImageReport5]</span><span class="sxs-lookup"><span data-stu-id="df223-468">![An Audits report after configuring webpack to use production mode][ImageReport5]</span></span>  

<span data-ttu-id="df223-469">Para reduzir a atividade do JavaScript, remova a solicitação para `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="df223-469">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="df223-470">Na guia Editor, abra `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="df223-470">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="df223-471">Comente a solicitação para `this.mineBitcoin(1500)` no (a) `constructor` .</span><span class="sxs-lookup"><span data-stu-id="df223-471">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="df223-472">Aguarde até que a nova compilação seja implementada.</span><span class="sxs-lookup"><span data-stu-id="df223-472">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="df223-473">Faça a auditoria da página novamente.</span><span class="sxs-lookup"><span data-stu-id="df223-473">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="df223-474">Figura 42</span><span class="sxs-lookup"><span data-stu-id="df223-474">Figure 42</span></span>  
    > <span data-ttu-id="df223-475">Um relatório de auditorias após remover o trabalho em JavaScript desnecessário</span><span class="sxs-lookup"><span data-stu-id="df223-475">An Audits report after removing unnecessary JavaScript work</span></span>  
    > <span data-ttu-id="df223-476">! [Um relatório de auditorias após remover o trabalho JavaScript desnecessário] [ImageReport6]</span><span class="sxs-lookup"><span data-stu-id="df223-476">![An Audits report after removing unnecessary JavaScript work][ImageReport6]</span></span>  

<span data-ttu-id="df223-477">Parece que essa última alteração causou um salto maciço no desempenho!</span><span class="sxs-lookup"><span data-stu-id="df223-477">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="df223-478">Esta seção forneceu uma introdução breve ao painel desempenho.</span><span class="sxs-lookup"><span data-stu-id="df223-478">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="df223-479">Consulte [referência de análise de desempenho][DevtoolsEvaluatePerformanceReference] para saber mais sobre como analisar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="df223-479">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="df223-480">Como fazer o trabalho de threads principais no mundo real</span><span class="sxs-lookup"><span data-stu-id="df223-480">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="df223-481">Em geral, o painel **desempenho** é a maneira mais comum de entender quais atividades o seu site faz ao carregar e encontrar maneiras de remover atividades desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="df223-481">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="df223-482">Se você preferir uma abordagem que se pareça mais `console.log()` , a [API de tempo do usuário][MDNUserTimingApi] permite marcar arbitrariamente determinadas fases do ciclo de vida do aplicativo, para controlar quanto tempo leva cada uma dessas fases.</span><span class="sxs-lookup"><span data-stu-id="df223-482">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="df223-483">Resumo</span><span class="sxs-lookup"><span data-stu-id="df223-483">Summary</span></span>   

*   <span data-ttu-id="df223-484">Sempre que você tiver sido configurado para otimizar o desempenho de carga de um site, sempre comece com uma auditoria.</span><span class="sxs-lookup"><span data-stu-id="df223-484">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="df223-485">A auditoria estabelece uma linha de base e fornece dicas sobre como melhorar.</span><span class="sxs-lookup"><span data-stu-id="df223-485">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="df223-486">Faça uma alteração de cada vez e faça a auditoria da página após cada alteração para ver como essa alteração afeta o desempenho.</span><span class="sxs-lookup"><span data-stu-id="df223-486">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--    -->  



<!-- image links -->  

[ImageAddPatternIcon]: /microsoft-edge/devtools-guide-chromium/media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-panels-icon.msft.png  
[ImagePerformIcon]: /microsoft-edge/devtools-guide-chromium/media/perform-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRemoveIcon]: /microsoft-edge/devtools-guide-chromium/media/remove-icon.msft.png  

[ImageTony]: /microsoft-edge/devtools-guide-chromium/media/speed-tony.msft.png "Figura 1: Tony o gato"  
[ImageEditor]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js.msft.png "Figura 2: a guia Editor"  
[ImageMenu]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js-remix-project.msft.png "Figura 3: o menu que aparece depois de clicar em Tony"  
[ImageDemo]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live.msft.png "Figura 4: a guia demonstração"  
[ImageDevtools]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live-console.msft.png "Figura 5: DevTools e a demonstração"  
[ImageUndocked]: /microsoft-edge/devtools-guide-chromium/media/speed-console.msft.png "Figura 6: DevTools desencaixada"  
[ImageAudits]: /microsoft-edge/devtools-guide-chromium/media/speed-audits-performance.msft.png "Figura 7: painel auditorias"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png "Figura 8: o relatório para o painel auditorias do desempenho do site"  
<!--[ImageError]: /microsoft-edge/devtools-guide-chromium/media/speed-.msft.png "Old Figure 9: A report that errored"  -->  
[ImageOverall]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Audits-performance-Metrics-Collapsed-Metrics-highlighted.msft.png "Figura 9: a pontuação geral de desempenho"  
[ImageMetrics]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Audits-performance-Metrics-Collapsed-highlighted.msft.png "Figura 10: seção métricas"  
[ImageFirstMeaningfulPaint]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Audits-performance-Metrics-Expanded.msft.png "Figura 11: selecione o botão de alternância realçado para expandir os itens de métricas"  
[ImageScreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Audits-Performance-View-Trace.msft.png "Figura 12: capturas de tela de como a página procurou ao carregar"  
[ImageOpportunities]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Audits-performance-Opportunities.msft.png "Figura 13: a seção oportunidades"  
[ImageCompression]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Audits-performance-Opportunities-Expanded.msft.png "Figura 14: eliminar oportunidade de recursos de bloqueio de renderização"  
[ImageReference]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-web-dev-performance-Audits.msft.png "Figura 15: documentação para a oportunidade de eliminar recursos de bloqueio de renderização"  
[ImageDiagnostics]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Audits-performance-Diagnostics.msft.png "Figura 16: a seção diagnóstico"  
[ImagePassed]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Audits-performance-Passed-Audits.msft.png "figura 17: a seção de auditorias passadas"  
[ImageNetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Network.msft.png "Figura 18: painel de rede"  
[ImageLargeRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Network-use-Large-Request-Rows.msft.png "Figura 19: linhas grandes na tabela de solicitações de rede"  
[ImageHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Network-use-Large-Request-Rows-Bundle-js.msft.png "Figura 20: a guia cabeçalhos"  
[ImageServer]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Server-js.msft.png "figura 21: editando Server. js"  
<!--[ImageBuilding]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-server-js-edited.msft.png "Old Figure 22: The animation that indicates that the site is getting built"  -->  
[ImageRequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Network-Main.msft.png "Figura 22: a coluna tamanho agora mostra 2 valores diferentes para recursos de texto"  
[ImageGzip]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-Network-Bundle-js-Headers-Response.msft.png "Figura 23: a seção de cabeçalhos de resposta agora contém um `content-encoding` cabeçalho"  
[ImageReport2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-Audits-performance.msft.png "Figura 24: um relatório de auditoria após habilitar a compactação de texto"  
<!--[ImageResize]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png "Old Figure 27: Details about the properly size images opportunity"  -->
[ImageReport3]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Compression-Small-images-Audits-performance.msft.png "figura 25: um relatório de auditorias após o redimensionamento de imagens"  
[ImageRender]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-Audits-performance-oppportunities-Expanded.msft.png "Figura 26: mais informações sobre a oportunidade de eliminar recursos de bloqueio de renderização"  
[ImageCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-Audits-performance-oppportunities-Expanded-Command-Coverage.msft.png "Figura 27: abrindo o menu de comando do painel auditorias"  
[ImageCoverage]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-Audits-performance-oppportunities-Expanded-Drawer-Coverage.msft.png "Figura 28: a guia cobertura"  
[ImageCoverageReport]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-Audits-performance-oppportunities-Expanded-Drawer-Coverage-RELOADED.msft.png "figura 29: o relatório de cobertura"  
[ImageJQuery]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-sources-Drawer-Coverage-Reloaded-jQuery-js.msft.png "figura 30: Visualizar o arquivo jQuery no painel fontes"  
[ImageBlocking]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-Network-Drawer-Request-blocking-Empty.msft.png "figura 31: a guia de bloqueio de solicitação"  
[ImageLibs]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-Network-Drawer-Request-blocking-added.msft.png "Figura 32: adicionando um padrão para bloquear qualquer solicitação para o diretório libs"  
[ImageBlockedLibs]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-Network-Reloaded-Drawer-Request-blocking-added.msft.png "figura 33: o painel de rede mostra que as solicitações foram bloqueadas"  
[ImageReport4]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-2-Audits-performance.msft.png "Figura 34: um relatório de auditorias após remover os recursos de bloqueio de renderização"  
[ImagePerformance]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-performance-Slow-Network-Slow-CPU.msft.png "Figura 35: o rastreamento do painel desempenho do carregamento da página"  
[ImageOverview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-performance-Slow-Network-Slow-CPU-Main-Highlight.msft.png "Figura 36: a seção visão geral do rastreamento"  
[ImageUserTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-performance-Slow-Network-Slow-CPU-timings.msft.png "figura 37: a seção intervalos"  
[ImageMain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-performance-Slow-Network-Slow-CPU-Main.msft.png "figura 38: a seção principal"  
[ImageMine]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-performance-Slow-Network-Slow-CPU-timings-minebitcoin.msft.png "figura 39: passando o mouse sobre a atividade mineBitcoin"  
[ImageBottomUp]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-performance-Slow-Network-Slow-CPU-timings-Summary-minebitcoin.msft.png "figura 40: a guia de baixo para cima"  
[ImageReport5]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-3-Audits-performance.msft.png "Figura 41: um relatório de auditoria após a configuração do webpack para usar o modo de produção"  
[ImageReport6]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Glitch-Tony-remix-updated-4-Audits-performance.msft.png "Figura 42: um relatório de auditorias após remover trabalho de JavaScript desnecessário"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referência de análise de desempenho"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introdução à classe de desenvolvimento da Web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Otimização de imagem essencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Diretivas-codificação de conteúdo | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de tempo do usuário | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Aperto de árvore | webpack"  

> [!NOTE]
> <span data-ttu-id="df223-535">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="df223-535">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="df223-536">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="df223-536">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="df223-538">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="df223-538">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
