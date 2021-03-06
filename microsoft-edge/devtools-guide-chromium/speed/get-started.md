---
description: Saiba como usar o Microsoft Edge DevTools para encontrar maneiras de fazer com que seus sites carreguem mais rápido.
title: Otimizar a velocidade do site com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7de97ab27528e89e2373e0a0d1002e8c86e37613
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398109"
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

# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a><span data-ttu-id="0c653-104">Otimizar a velocidade do site com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0c653-104">Optimize website speed with Microsoft Edge DevTools</span></span>  

## <a name="goal-of-tutorial"></a><span data-ttu-id="0c653-105">Objetivo do tutorial</span><span class="sxs-lookup"><span data-stu-id="0c653-105">Goal of tutorial</span></span>  

<span data-ttu-id="0c653-106">Este tutorial ensina como usar o Microsoft Edge DevTools para encontrar maneiras de fazer com que seus sites carreguem mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-106">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="0c653-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0c653-107">Prerequisites</span></span>  

*   <span data-ttu-id="0c653-108">Você deve ter uma experiência básica de desenvolvimento da Web, semelhante ao que é ensinada nesta classe [Introdução ao Desenvolvimento da Web.][CourseraIntroductionWebDevelopmentClass]</span><span class="sxs-lookup"><span data-stu-id="0c653-108">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="0c653-109">Você não precisa saber nada sobre o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="0c653-109">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="0c653-110">Você aprenderá sobre isso neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="0c653-110">You learn about it in this tutorial.</span></span>  

## <a name="introduction"></a><span data-ttu-id="0c653-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="0c653-111">Introduction</span></span>  

<span data-ttu-id="0c653-112">Este é Tony.</span><span class="sxs-lookup"><span data-stu-id="0c653-112">This is Tony.</span></span>  <span data-ttu-id="0c653-113">Tony é muito famoso na sociedade de gatos.</span><span class="sxs-lookup"><span data-stu-id="0c653-113">Tony is very famous in cat society.</span></span>  <span data-ttu-id="0c653-114">Ele criou um site para que seus fãs aprendam sobre suas comidas favoritas.</span><span class="sxs-lookup"><span data-stu-id="0c653-114">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="0c653-115">Seus fãs adoram o site, mas Tony continua ouvindo reclamações de que o site é carregado lentamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-115">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="0c653-116">Tony pediu para ajudá-lo a acelerar o site.</span><span class="sxs-lookup"><span data-stu-id="0c653-116">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony, o gato" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="0c653-118">Tony, o gato</span><span class="sxs-lookup"><span data-stu-id="0c653-118">Tony the cat</span></span>  
:::image-end:::  

## <a name="step-1-audit-the-site"></a><span data-ttu-id="0c653-119">Etapa 1: Auditar o site</span><span class="sxs-lookup"><span data-stu-id="0c653-119">Step 1: Audit the site</span></span>  

<span data-ttu-id="0c653-120">Sempre que você se definir para melhorar o desempenho de carga de um site, **sempre comece com uma auditoria**.</span><span class="sxs-lookup"><span data-stu-id="0c653-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="0c653-121">A auditoria tem duas funções importantes:</span><span class="sxs-lookup"><span data-stu-id="0c653-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="0c653-122">Ele cria uma **linha de base** para você medir as alterações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0c653-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="0c653-123">Ele fornece dicas **a actionable sobre** quais alterações têm mais impacto.</span><span class="sxs-lookup"><span data-stu-id="0c653-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <a name="set-up"></a><span data-ttu-id="0c653-124">Configurar</span><span class="sxs-lookup"><span data-stu-id="0c653-124">Set up</span></span>  

<span data-ttu-id="0c653-125">Primeiro, você deve configurar o site para que possa fazer alterações nele mais tarde.</span><span class="sxs-lookup"><span data-stu-id="0c653-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="0c653-126">[Abra o código-fonte do site](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="0c653-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="0c653-127">Essa guia é conhecida como a **guia editor**.</span><span class="sxs-lookup"><span data-stu-id="0c653-127">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="A guia editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="0c653-129">A **guia editor**</span><span class="sxs-lookup"><span data-stu-id="0c653-129">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-130">Escolha **tony**.</span><span class="sxs-lookup"><span data-stu-id="0c653-130">Choose **tony**.</span></span>  <span data-ttu-id="0c653-131">Um menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="0c653-131">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="O menu que aparece depois de escolher Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="0c653-133">O menu que aparece depois de escolher **Tony**</span><span class="sxs-lookup"><span data-stu-id="0c653-133">The menu that appears after choosing **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-134">Escolha **Projeto de Remix**.</span><span class="sxs-lookup"><span data-stu-id="0c653-134">Choose **Remix Project**.</span></span>  <span data-ttu-id="0c653-135">O nome do projeto muda de **tony** para algum nome gerado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-135">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="0c653-136">Agora você tem sua própria cópia editável do código.</span><span class="sxs-lookup"><span data-stu-id="0c653-136">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="0c653-137">Mais tarde, você pode fazer alterações nesse código.</span><span class="sxs-lookup"><span data-stu-id="0c653-137">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="0c653-138">Escolha **Mostrar** e escolher **Em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="0c653-138">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="0c653-139">A demonstração é aberta em uma nova guia.  Essa guia é chamada de guia **de demonstração**.  Pode levar algum tempo para o site ser carregado.</span><span class="sxs-lookup"><span data-stu-id="0c653-139">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="A guia demonstração" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="0c653-141">A guia demonstração</span><span class="sxs-lookup"><span data-stu-id="0c653-141">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-142">Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="0c653-142">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="0c653-143">O Microsoft Edge DevTools abre junto com a demonstração.</span><span class="sxs-lookup"><span data-stu-id="0c653-143">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools e a demonstração" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="0c653-145">DevTools e a demonstração</span><span class="sxs-lookup"><span data-stu-id="0c653-145">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0c653-146">Para o restante das capturas de tela neste tutorial, DevTools é mostrado em uma janela separada.</span><span class="sxs-lookup"><span data-stu-id="0c653-146">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="0c653-147">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) `Undock` \*\*\*\* para abrir o Menu de Comando, digitando e selecionando Desfazer em janela separada.</span><span class="sxs-lookup"><span data-stu-id="0c653-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools DevTools desfaçada" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="0c653-149">DevTools DevTools desfaçada</span><span class="sxs-lookup"><span data-stu-id="0c653-149">Undocked DevTools</span></span>  
:::image-end:::  

### <a name="establish-a-baseline"></a><span data-ttu-id="0c653-150">Estabelecer uma linha de base</span><span class="sxs-lookup"><span data-stu-id="0c653-150">Establish a baseline</span></span>  

<span data-ttu-id="0c653-151">A linha de base é um registro de como o site foi executado antes de você fazer quaisquer melhorias de desempenho.</span><span class="sxs-lookup"><span data-stu-id="0c653-151">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="0c653-152">Escolha a **ferramenta Auditorias.**</span><span class="sxs-lookup"><span data-stu-id="0c653-152">Choose the **Audits** tool.</span></span>  <span data-ttu-id="0c653-153">Ele pode estar oculto atrás do **botão Mais Painéis** \( ![ Mais ][ImageMorePanelsIcon] Painéis \).</span><span class="sxs-lookup"><span data-stu-id="0c653-153">It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="0c653-154">Há um Farol neste painel porque o projeto que alimenta o painel de Auditorias é chamado **de Farol**.</span><span class="sxs-lookup"><span data-stu-id="0c653-154">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="A ferramenta Auditorias" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="0c653-156">A **ferramenta Auditorias**</span><span class="sxs-lookup"><span data-stu-id="0c653-156">The **Audits** tool</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="0c653-157">Corresponder as configurações de auditoria às da figura anterior.</span><span class="sxs-lookup"><span data-stu-id="0c653-157">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="0c653-158">Aqui está uma explicação das diferentes opções:</span><span class="sxs-lookup"><span data-stu-id="0c653-158">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="0c653-159">**Dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="0c653-159">**Device**.</span></span>  <span data-ttu-id="0c653-160">Definir como **Móvel** altera a cadeia de caracteres do agente do usuário e simula um visualizador móvel.</span><span class="sxs-lookup"><span data-stu-id="0c653-160">Set to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="0c653-161">Definir como **Área de** Trabalho praticamente desliga as alterações **móveis.**</span><span class="sxs-lookup"><span data-stu-id="0c653-161">Set to **Desktop** pretty much just turns off the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="0c653-162">**Auditorias**.</span><span class="sxs-lookup"><span data-stu-id="0c653-162">**Audits**.</span></span>  <span data-ttu-id="0c653-163">Desativar uma categoria para impedir que o painel **de Auditorias** executa essas auditorias e exclui essas auditorias do seu relatório.</span><span class="sxs-lookup"><span data-stu-id="0c653-163">Turn off a category to prevent the **Audits** panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="0c653-164">Deixe as outras categorias ativas, se quiser exibir os tipos de recomendações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="0c653-164">Leave the other categories Turned on, if you want to display the types of recommendations that are provided.</span></span>  <span data-ttu-id="0c653-165">Desativar categorias para acelerar ligeiramente o processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0c653-165">Turn off categories to slightly speed up the auditing process.</span></span>  
    *   <span data-ttu-id="0c653-166">**Throttling**.</span><span class="sxs-lookup"><span data-stu-id="0c653-166">**Throttling**.</span></span>  <span data-ttu-id="0c653-167">Definido como **4G lento simulado,** a lentidão da CPU 4x simula as condições típicas de navegação em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="0c653-167">Set to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="0c653-168">Ele é chamado de "simulado" porque o painel De auditorias não realmente acelera durante o processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0c653-168">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="0c653-169">Em vez disso, ele apenas extrapola quanto tempo a página leva para carregar em condições móveis.</span><span class="sxs-lookup"><span data-stu-id="0c653-169">Instead, it just extrapolates how long the page takes to load under mobile conditions.</span></span>  <span data-ttu-id="0c653-170">A **configuração Aplicada...** por outro lado, realmente acelera sua CPU e rede, com a troca de um processo de auditoria mais longo.</span><span class="sxs-lookup"><span data-stu-id="0c653-170">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="0c653-171">**Limpar Armazenamento**.</span><span class="sxs-lookup"><span data-stu-id="0c653-171">**Clear Storage**.</span></span>  <span data-ttu-id="0c653-172">Ativar a caixa de seleção para limpar todo o armazenamento associado à página antes de cada auditoria.</span><span class="sxs-lookup"><span data-stu-id="0c653-172">Turn on the checkbox to clear all storage associated with the page before every audit.</span></span>  <span data-ttu-id="0c653-173">Deixe essa configuração em caso de você querer auditar como os visitantes pela primeira vez experimentam seu site.</span><span class="sxs-lookup"><span data-stu-id="0c653-173">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="0c653-174">Desativar essa configuração quando quiser a experiência de visita repetida.</span><span class="sxs-lookup"><span data-stu-id="0c653-174">Turn off this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="0c653-175">Escolha **Executar Auditorias**.</span><span class="sxs-lookup"><span data-stu-id="0c653-175">Choose **Run Audits**.</span></span>  <span data-ttu-id="0c653-176">Após 10 a 30 segundos, o painel **Auditorias** exibe um relatório do desempenho do site.</span><span class="sxs-lookup"><span data-stu-id="0c653-176">After 10 to 30 seconds, the **Audits** panel displays a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="O relatório do painel Auditorias do desempenho do site" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="0c653-178">O relatório do painel Auditorias do desempenho do site</span><span class="sxs-lookup"><span data-stu-id="0c653-178">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a><span data-ttu-id="0c653-179">Manipulando erros de relatório</span><span class="sxs-lookup"><span data-stu-id="0c653-179">Handling report errors</span></span>  

<span data-ttu-id="0c653-180">Se você receber um erro no relatório do painel Auditorias, tente executar a guia demonstração de uma janela **InPrivate** sem nenhuma outra guia aberta.</span><span class="sxs-lookup"><span data-stu-id="0c653-180">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="0c653-181">Isso garante que você está executando o Microsoft Edge de um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="0c653-181">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="0c653-182">Extensões do Microsoft Edge, em particular, frequentemente interferem no processo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0c653-182">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a><span data-ttu-id="0c653-183">Compreender seu relatório</span><span class="sxs-lookup"><span data-stu-id="0c653-183">Understand your report</span></span>  

<span data-ttu-id="0c653-184">O número na parte superior do relatório é a pontuação geral de desempenho do site.</span><span class="sxs-lookup"><span data-stu-id="0c653-184">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="0c653-185">Mais tarde, conforme você faz alterações no código, o número exibido deve aumentar.</span><span class="sxs-lookup"><span data-stu-id="0c653-185">Later, as you make changes to the code, the number displayed should rise.</span></span>  <span data-ttu-id="0c653-186">Uma pontuação mais alta significa melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="0c653-186">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="A pontuação geral do desempenho" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="0c653-188">A pontuação geral do desempenho</span><span class="sxs-lookup"><span data-stu-id="0c653-188">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-189">A **seção Metrics** fornece medidas quantitativos do desempenho do site.</span><span class="sxs-lookup"><span data-stu-id="0c653-189">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="0c653-190">Cada métrica fornece informações sobre um aspecto diferente do desempenho.</span><span class="sxs-lookup"><span data-stu-id="0c653-190">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="0c653-191">Por exemplo, First **Contentful Paint** informa quando o conteúdo é pintado pela primeira vez na tela, o que é um marco importante na percepção do usuário sobre a carga da página, enquanto Time **To Interactive** marca o ponto no qual a página aparece pronta o suficiente para lidar com interações do usuário.</span><span class="sxs-lookup"><span data-stu-id="0c653-191">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="A seção Métricas" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="0c653-193">A **seção Métricas**</span><span class="sxs-lookup"><span data-stu-id="0c653-193">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-194">Escolha o botão de alternância realçada na figura a seguir para exibir uma descrição para cada métrica e escolha **Saber mais** para ler a documentação sobre ela.</span><span class="sxs-lookup"><span data-stu-id="0c653-194">Choose the highlighted toggle button in the following figure to display a description for each metric, and choose **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Escolha o botão de alternância realçada para expandir os itens Metrics" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="0c653-196">Escolha o botão de alternância realçada para expandir os itens Metrics</span><span class="sxs-lookup"><span data-stu-id="0c653-196">Choose the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-197">Abaixo Métricas está uma coleção de capturas de tela que mostram como a página era carregada.</span><span class="sxs-lookup"><span data-stu-id="0c653-197">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Capturas de tela de como a página era durante o carregamento" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="0c653-199">Capturas de tela de como a página era durante o carregamento</span><span class="sxs-lookup"><span data-stu-id="0c653-199">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-200">A **seção Oportunidades** fornece dicas específicas sobre como melhorar o desempenho da carga desta página específica.</span><span class="sxs-lookup"><span data-stu-id="0c653-200">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="A seção Oportunidades" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="0c653-202">A **seção Oportunidades**</span><span class="sxs-lookup"><span data-stu-id="0c653-202">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-203">Escolha uma oportunidade para saber mais sobre isso.</span><span class="sxs-lookup"><span data-stu-id="0c653-203">Choose an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminar a oportunidade de recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="0c653-205">**Eliminar a oportunidade de recursos de bloqueio de** renderização</span><span class="sxs-lookup"><span data-stu-id="0c653-205">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-206">Escolha **Saiba mais para** exibir a documentação sobre por que uma oportunidade é importante e recomendações específicas sobre como corrigi-la.</span><span class="sxs-lookup"><span data-stu-id="0c653-206">Choose **Learn More** to display documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentação para a oportunidade de eliminar recursos de bloqueio de renderização" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="0c653-208">Documentação para a **oportunidade de eliminar recursos de bloqueio de renderização**</span><span class="sxs-lookup"><span data-stu-id="0c653-208">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-209">A **seção Diagnóstico** fornece mais informações sobre fatores que contribuem para o tempo de carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-209">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="A seção Diagnóstico" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="0c653-211">A **seção Diagnóstico**</span><span class="sxs-lookup"><span data-stu-id="0c653-211">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-212">A **seção Auditorias Passadas** mostra o que o site está fazendo corretamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-212">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="0c653-213">Escolha expandir a seção.</span><span class="sxs-lookup"><span data-stu-id="0c653-213">Choose to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="A seção Auditorias Aprovadas" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="0c653-215">A **seção Auditorias Aprovadas**</span><span class="sxs-lookup"><span data-stu-id="0c653-215">The **Passed Audits** section</span></span>  
:::image-end:::  

## <a name="step-2-experiment"></a><span data-ttu-id="0c653-216">Etapa 2: Experimento</span><span class="sxs-lookup"><span data-stu-id="0c653-216">Step 2: Experiment</span></span>  

<span data-ttu-id="0c653-217">A seção Oportunidades do relatório de auditoria fornece dicas sobre como melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-217">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="0c653-218">Nesta seção, você implementa as alterações recomendadas na base de código, auditando o site após cada alteração para medir como ele afeta a velocidade do site.</span><span class="sxs-lookup"><span data-stu-id="0c653-218">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <a name="enable-text-compression"></a><span data-ttu-id="0c653-219">Habilitar compactação de texto</span><span class="sxs-lookup"><span data-stu-id="0c653-219">Enable text compression</span></span>  

<span data-ttu-id="0c653-220">Seu relatório diz que evitar enormes cargas de rede é uma das principais oportunidades para melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-220">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="0c653-221">Habilenciar a compactação de texto é uma oportunidade para melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-221">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="0c653-222">A compactação de texto é quando você reduz ou compacta o tamanho de um arquivo de texto antes de enviá-lo pela rede.</span><span class="sxs-lookup"><span data-stu-id="0c653-222">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="0c653-223">Semelhante à forma como você pode arquivar um diretório antes de enviá-lo para reduzir o tamanho.</span><span class="sxs-lookup"><span data-stu-id="0c653-223">Similar to how you may archive a directory before sending it to reduce the size.</span></span>  

<span data-ttu-id="0c653-224">Antes de habilitar a compactação, aqui estão algumas maneiras de verificar manualmente se os recursos de texto são compactados.</span><span class="sxs-lookup"><span data-stu-id="0c653-224">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="0c653-225">Escolha a **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="0c653-225">Choose the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="O painel Rede" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="0c653-227">A **ferramenta Rede**</span><span class="sxs-lookup"><span data-stu-id="0c653-227">The **Network** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-228">Escolha o **ícone de configuração de** rede.</span><span class="sxs-lookup"><span data-stu-id="0c653-228">Choose the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="0c653-229">Escolha a **caixa de seleção Usar linhas de solicitação** grandes.</span><span class="sxs-lookup"><span data-stu-id="0c653-229">Choose the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="0c653-230">A altura das linhas na tabela de solicitações de rede aumenta.</span><span class="sxs-lookup"><span data-stu-id="0c653-230">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Linhas grandes na tabela de solicitações de rede" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="0c653-232">Linhas grandes na tabela de solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="0c653-232">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-233">Se a **coluna Tamanho** na tabela de solicitações de rede não for exibida, escolha o header de tabela > **Size**.</span><span class="sxs-lookup"><span data-stu-id="0c653-233">If the **Size** column in the table of network requests is not displayed, choose the table header > **Size**.</span></span>  

<span data-ttu-id="0c653-234">Cada **célula Size** mostra dois valores.</span><span class="sxs-lookup"><span data-stu-id="0c653-234">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="0c653-235">O valor superior é o tamanho do recurso baixado.</span><span class="sxs-lookup"><span data-stu-id="0c653-235">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="0c653-236">O valor inferior é o tamanho do recurso não compactado.</span><span class="sxs-lookup"><span data-stu-id="0c653-236">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="0c653-237">Se os dois valores são os mesmos, o recurso não está sendo compactado quando é enviado pela rede.</span><span class="sxs-lookup"><span data-stu-id="0c653-237">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="0c653-238">Por exemplo, na figura anterior, os valores superior e inferior `bundle.js` para são `1.2 MB` e `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="0c653-238">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="0c653-239">Verifique se há compactação inspecionando os cabeçalhos HTTP de um recurso:</span><span class="sxs-lookup"><span data-stu-id="0c653-239">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="0c653-240">Escolha `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="0c653-240">Choose `bundle.js`.</span></span>  
1.  <span data-ttu-id="0c653-241">Escolha o **painel Headers.**</span><span class="sxs-lookup"><span data-stu-id="0c653-241">Choose the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="O painel Headers" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="0c653-243">O **painel Headers**</span><span class="sxs-lookup"><span data-stu-id="0c653-243">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-244">**Pesquise** na seção Headers de Resposta para um `content-encoding` header.</span><span class="sxs-lookup"><span data-stu-id="0c653-244">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="0c653-245">Um `content-encoding` título não é exibido, o que significa que não foi `bundle.js` compactado.</span><span class="sxs-lookup"><span data-stu-id="0c653-245">A `content-encoding` heading is not displayed, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="0c653-246">Quando um recurso é compactado, esse header geralmente é definido como `gzip` `deflate` , ou `br` .</span><span class="sxs-lookup"><span data-stu-id="0c653-246">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="0c653-247">Para uma explicação dos valores, navegue até [Diretivas][MDNContentEncodingDirectives].</span><span class="sxs-lookup"><span data-stu-id="0c653-247">For an explanation of the values, navigate to [Directives][MDNContentEncodingDirectives].</span></span>  

<span data-ttu-id="0c653-248">Chega de explicações.</span><span class="sxs-lookup"><span data-stu-id="0c653-248">Enough with the explanations.</span></span>  <span data-ttu-id="0c653-249">Hora de fazer algumas alterações.</span><span class="sxs-lookup"><span data-stu-id="0c653-249">Time to make some changes.</span></span>  <span data-ttu-id="0c653-250">Habilita a compactação de texto adicionando algumas linhas de código:</span><span class="sxs-lookup"><span data-stu-id="0c653-250">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="0c653-251">Na guia editor, escolha **server.js**.</span><span class="sxs-lookup"><span data-stu-id="0c653-251">In the editor tab, choose **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Editar server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="0c653-253">Editar</span><span class="sxs-lookup"><span data-stu-id="0c653-253">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-254">Adicione o código a seguir \*\* aserver.js\*\*.</span><span class="sxs-lookup"><span data-stu-id="0c653-254">Add the following code to **server.js**.</span></span>  <span data-ttu-id="0c653-255">Certifique-se de colocar `app.use(compression())` antes `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="0c653-255">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="0c653-256">Normalmente, você precisa instalar o pacote por meio de algo como , mas `compression` isso já foi feito para `npm i -S compression` você.</span><span class="sxs-lookup"><span data-stu-id="0c653-256">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="0c653-257">Aguarde a falha para implantar a nova com build do site.</span><span class="sxs-lookup"><span data-stu-id="0c653-257">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="0c653-258">A animação sofisticada ao lado **de Ferramentas** significa que o site está sendo reconstruído e reimplantado.</span><span class="sxs-lookup"><span data-stu-id="0c653-258">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="0c653-259">A alteração estará pronta quando a animação ao lado de **Ferramentas** desaparecer.</span><span class="sxs-lookup"><span data-stu-id="0c653-259">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="0c653-260">Escolha **Mostrar** e escolha **Em uma nova janela** novamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-260">Choose **Show** and choose **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="0c653-261">Use os fluxos de trabalho que você aprendeu anteriormente para verificar manualmente se a compactação está funcionando:</span><span class="sxs-lookup"><span data-stu-id="0c653-261">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="0c653-262">Volte para a guia demonstração e atualize a página.</span><span class="sxs-lookup"><span data-stu-id="0c653-262">Go back to the demo tab and refresh the page.</span></span>  <span data-ttu-id="0c653-263">A **coluna Tamanho** agora deve mostrar 2 valores diferentes para recursos de texto como `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="0c653-263">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="0c653-264">Na figura após o seguinte, o valor superior de for é o tamanho do arquivo que foi enviado pela rede, e o valor inferior de é o tamanho do arquivo não `256 KB` `bundle.js` `1.2 MB` compactado.</span><span class="sxs-lookup"><span data-stu-id="0c653-264">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="A coluna Tamanho agora mostra 2 valores diferentes para recursos de texto" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="0c653-266">A **coluna Tamanho** agora mostra 2 valores diferentes para recursos de texto</span><span class="sxs-lookup"><span data-stu-id="0c653-266">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-267">A **seção Headers de** Resposta agora deve incluir um `bundle.js` `content-encoding: gzip` header.</span><span class="sxs-lookup"><span data-stu-id="0c653-267">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="A seção Headers de Resposta agora contém um header de codificação de conteúdo" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="0c653-269">A **seção Headers de** Resposta agora contém um header de codificação de conteúdo</span><span class="sxs-lookup"><span data-stu-id="0c653-269">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0c653-270">Audite a página novamente para medir que tipo de compactação de texto de impacto tem no desempenho da carga da página:</span><span class="sxs-lookup"><span data-stu-id="0c653-270">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="0c653-271">Escolha a **ferramenta Auditorias.**</span><span class="sxs-lookup"><span data-stu-id="0c653-271">Choose the **Audits** tool.</span></span>  
1.  <span data-ttu-id="0c653-272">Escolha **Executar uma auditoria** \( Executar uma auditoria ![ ][ImagePerformIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0c653-272">Choose **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="0c653-273">Deixe as configurações da mesma forma de antes.</span><span class="sxs-lookup"><span data-stu-id="0c653-273">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="0c653-274">Escolha **Executar auditoria**.</span><span class="sxs-lookup"><span data-stu-id="0c653-274">Choose **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Um relatório de Auditorias após habil passada a compactação de texto" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="0c653-276">Um relatório de Auditorias após habil passada a compactação de texto</span><span class="sxs-lookup"><span data-stu-id="0c653-276">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="0c653-277">Sua pontuação geral de desempenho deve ter aumentado, o que significa que o site está ficando mais rápido.</span><span class="sxs-lookup"><span data-stu-id="0c653-277">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <a name="text-compression-in-the-real-world"></a><span data-ttu-id="0c653-278">Compactação de texto no mundo real</span><span class="sxs-lookup"><span data-stu-id="0c653-278">Text compression in the real world</span></span>  

<span data-ttu-id="0c653-279">A maioria dos servidores realmente tem correções simples como esta para habilenciar a compactação!</span><span class="sxs-lookup"><span data-stu-id="0c653-279">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="0c653-280">Basta fazer uma pesquisa sobre como configurar qualquer servidor que você usa para compactar texto.</span><span class="sxs-lookup"><span data-stu-id="0c653-280">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <a name="resize-images"></a><span data-ttu-id="0c653-281">Resize imagens</span><span class="sxs-lookup"><span data-stu-id="0c653-281">Resize images</span></span>  

<span data-ttu-id="0c653-282">Seu relatório indica que evitar cargas de rede enormes é uma das principais oportunidades para melhorar o desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-282">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="0c653-283">Resizing images helps reduce the size of the network payload.</span><span class="sxs-lookup"><span data-stu-id="0c653-283">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="0c653-284">Se o usuário estiver exibindo suas imagens em uma tela de dispositivo móvel com 500 pixels de largura, não há realmente nenhum ponto em enviar uma imagem de 1500 pixels de largura.</span><span class="sxs-lookup"><span data-stu-id="0c653-284">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="0c653-285">O ideal é enviar uma imagem de 500 pixels no máximo.</span><span class="sxs-lookup"><span data-stu-id="0c653-285">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="0c653-286">No relatório, escolha **Evitar cargas de** rede enormes para exibir quais imagens devem ser resized.</span><span class="sxs-lookup"><span data-stu-id="0c653-286">In your report, choose **Avoid enormous network payloads** to display which images should be resized.</span></span>  <span data-ttu-id="0c653-287">Parece que 2 dos arquivos jpg têm mais de 2.000 KB, o que é maior do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="0c653-287">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="0c653-288">De volta à guia editor, abra `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="0c653-288">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="0c653-289">Substitua `const dir = 'big'` por `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="0c653-289">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="0c653-290">Esse diretório contém cópias das mesmas imagens que foram resized.</span><span class="sxs-lookup"><span data-stu-id="0c653-290">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="0c653-291">Audite a página novamente para exibir como a alteração afeta o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="0c653-291">Audit the page again to display how the change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Um relatório de auditorias após rea reizing imagens" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="0c653-293">Um relatório de auditorias após rea reizing imagens</span><span class="sxs-lookup"><span data-stu-id="0c653-293">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0c653-294">A alteração exibida tem apenas um pequeno efeito na pontuação geral do desempenho.</span><span class="sxs-lookup"><span data-stu-id="0c653-294">The change displays only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="0c653-295">No entanto, uma coisa que a pontuação não mostra claramente é quantos dados de rede você está salvando seus usuários.</span><span class="sxs-lookup"><span data-stu-id="0c653-295">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="0c653-296">O tamanho total das fotos antigas era de cerca de 5,3 megabytes, enquanto agora é de apenas cerca de 0,18 megabytes.</span><span class="sxs-lookup"><span data-stu-id="0c653-296">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <a name="resizing-images-in-the-real-world"></a><span data-ttu-id="0c653-297">Resizing images in the real world</span><span class="sxs-lookup"><span data-stu-id="0c653-297">Resizing images in the real world</span></span>  

<span data-ttu-id="0c653-298">Para um aplicativo pequeno, fazer um resize único como este pode ser bom o suficiente.</span><span class="sxs-lookup"><span data-stu-id="0c653-298">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="0c653-299">Mas para um aplicativo grande, isso obviamente não é escalonável.</span><span class="sxs-lookup"><span data-stu-id="0c653-299">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="0c653-300">Aqui estão algumas estratégias para gerenciar imagens em aplicativos grandes:</span><span class="sxs-lookup"><span data-stu-id="0c653-300">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="0c653-301">Resize imagens durante o processo de com build.</span><span class="sxs-lookup"><span data-stu-id="0c653-301">Resize images during your build process.</span></span>  
*   <span data-ttu-id="0c653-302">Crie vários tamanhos de cada imagem durante o processo de com build e use `srcset` em seu código.</span><span class="sxs-lookup"><span data-stu-id="0c653-302">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="0c653-303">Em tempo de execução, o navegador cuida de escolher qual tamanho é melhor para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c653-303">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="0c653-304">Use uma CDN de imagem que permite reorganizar dinamicamente uma imagem ao solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="0c653-304">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="0c653-305">No mínimo, otimize cada imagem.</span><span class="sxs-lookup"><span data-stu-id="0c653-305">At the very least, optimize each image.</span></span>  <span data-ttu-id="0c653-306">Isso pode criar grandes economias.</span><span class="sxs-lookup"><span data-stu-id="0c653-306">This may create huge savings.</span></span>  
  <span data-ttu-id="0c653-307">Otimização é quando você executar uma imagem por meio de um programa especial que reduz o tamanho do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="0c653-307">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="0c653-308">Para obter mais dicas, navegue até [Essential Image Optimization][EssentialImageOptimization].</span><span class="sxs-lookup"><span data-stu-id="0c653-308">For more tips, navigate to [Essential Image Optimization][EssentialImageOptimization].</span></span>  
    
### <a name="eliminate-render-blocking-resources"></a><span data-ttu-id="0c653-309">Eliminar recursos de bloqueio de renderização</span><span class="sxs-lookup"><span data-stu-id="0c653-309">Eliminate render-blocking resources</span></span>  

<span data-ttu-id="0c653-310">Seu relatório mais recente diz que a eliminação de recursos de bloqueio de renderização agora é a maior oportunidade.</span><span class="sxs-lookup"><span data-stu-id="0c653-310">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="0c653-311">Um recurso de bloqueio de renderização é um arquivo JavaScript ou CSS externo que o navegador deve baixar, analisar e executar antes de exibir a página.</span><span class="sxs-lookup"><span data-stu-id="0c653-311">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="0c653-312">O objetivo é executar apenas o CSS principal e o código JavaScript necessário para exibir a página corretamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-312">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="0c653-313">A primeira tarefa, então, é encontrar o código que você não precisa executar no carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-313">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="0c653-314">Escolha **Eliminar recursos de bloqueio de renderização** para exibir os recursos que estão bloqueando:</span><span class="sxs-lookup"><span data-stu-id="0c653-314">Choose **Eliminate render-blocking resources** to display the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="0c653-315">e `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="0c653-315">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Mais informações sobre a oportunidade De eliminar recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="0c653-317">Mais informações sobre a oportunidade **De eliminar recursos de bloqueio de renderização**</span><span class="sxs-lookup"><span data-stu-id="0c653-317">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-318">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) `Coverage` \*\*\*\* para abrir o Menu de Comando, começar a digitar e, em seguida, escolher Mostrar Cobertura .</span><span class="sxs-lookup"><span data-stu-id="0c653-318">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then choose **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Abra o Menu de Comando no painel Auditorias" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="0c653-320">Abra o Menu de Comando no **painel Auditorias**</span><span class="sxs-lookup"><span data-stu-id="0c653-320">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="A ferramenta Coverage" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="0c653-322">A **ferramenta Coverage**</span><span class="sxs-lookup"><span data-stu-id="0c653-322">The **Coverage** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-323">Escolha **Atualizar** \( ![ Atualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0c653-323">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="0c653-324">A **ferramenta Coverage** fornece uma visão geral de quanto do código em , e é executado enquanto a página é `bundle.js` `jquery.js` `lodash.js` carregada.</span><span class="sxs-lookup"><span data-stu-id="0c653-324">The **Coverage** tool provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="0c653-325">Na figura após o seguinte, cerca de 76% e 30% dos arquivos jQuery e Lodash não são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-325">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="O relatório de cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="0c653-327">O relatório de cobertura</span><span class="sxs-lookup"><span data-stu-id="0c653-327">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-328">Escolha a **linhajquery.js.**</span><span class="sxs-lookup"><span data-stu-id="0c653-328">Choose the **jquery.js** row.</span></span>  <span data-ttu-id="0c653-329">O DevTools abre o arquivo no painel Fontes.</span><span class="sxs-lookup"><span data-stu-id="0c653-329">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="0c653-330">Uma linha de código foi seguida se tiver uma barra azul ao lado dela.</span><span class="sxs-lookup"><span data-stu-id="0c653-330">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="0c653-331">Uma barra vermelha significa que não foi executado e, definitivamente, não é necessário no carregamento da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-331">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Exibindo o arquivo jQuery no painel Fontes" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="0c653-333">Exibindo o arquivo jQuery no painel **Fontes**</span><span class="sxs-lookup"><span data-stu-id="0c653-333">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-334">Role um pouco pelo código jQuery.</span><span class="sxs-lookup"><span data-stu-id="0c653-334">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="0c653-335">Algumas das linhas que são "executar" são, na verdade, apenas comentários.</span><span class="sxs-lookup"><span data-stu-id="0c653-335">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="0c653-336">Executar esse código por meio de um minifier que tira comentários é outra maneira de reduzir o tamanho desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="0c653-336">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="0c653-337">Em resumo, quando você está trabalhando com seu próprio código, a ferramenta **Coverage** ajuda você a analisar seu código, linha por linha e apenas enviar o código necessário para a carga da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-337">In short, when you are working with your own code, the **Coverage** tool helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="0c653-338">Os `jquery.js` arquivos e `lodash.js` são necessários para carregar a página?</span><span class="sxs-lookup"><span data-stu-id="0c653-338">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="0c653-339">A **ferramenta de bloqueio** solicitação exibe o que acontece quando os recursos não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0c653-339">The **Request blocking** tool displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="0c653-340">Escolha a **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="0c653-340">Choose the **Network** tool.</span></span>  
1.  <span data-ttu-id="0c653-341">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) para abrir o Menu de Comando novamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-341">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="0c653-342">Comece a digitar `blocking` e escolha Mostrar Bloqueio de **Solicitação.**</span><span class="sxs-lookup"><span data-stu-id="0c653-342">Start typing `blocking` and then choose **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="A ferramenta de bloqueio solicitação" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="0c653-344">A **ferramenta de bloqueio solicitação**</span><span class="sxs-lookup"><span data-stu-id="0c653-344">The **Request blocking** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-345">Escolha **Adicionar Padrão** \( Adicionar Padrão ![ ][ImageAddPatternIcon] \), digite e selecione `/libs/*` `Enter` confirmar.</span><span class="sxs-lookup"><span data-stu-id="0c653-345">Choose **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Adicionar um padrão para bloquear qualquer solicitação ao diretório libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="0c653-347">Adicionar um padrão para bloquear qualquer solicitação ao `libs` diretório</span><span class="sxs-lookup"><span data-stu-id="0c653-347">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-348">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="0c653-348">Refresh the page.</span></span>  <span data-ttu-id="0c653-349">As solicitações jQuery e Lodash são vermelhas, o que significa que as solicitações foram bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="0c653-349">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="0c653-350">A página ainda é carregada e interativa, portanto, parece que esses recursos não são necessários!</span><span class="sxs-lookup"><span data-stu-id="0c653-350">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="O painel Rede mostra que as solicitações foram bloqueadas" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="0c653-352">A **ferramenta Rede** mostra que as solicitações foram bloqueadas</span><span class="sxs-lookup"><span data-stu-id="0c653-352">The **Network** tool shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-353">Escolha **Remover todos os padrões** \( Remover todos os padrões ![ ][ImageRemoveIcon] \) para excluir o padrão de `/libs/*` bloqueio.</span><span class="sxs-lookup"><span data-stu-id="0c653-353">Choose **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="0c653-354">Em geral, a **ferramenta de** bloqueio solicitação é útil para simular como sua página se comporta quando um determinado recurso não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0c653-354">In general, the **Request blocking** tool is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="0c653-355">Agora, remova as referências a esses arquivos do código e audite a página novamente:</span><span class="sxs-lookup"><span data-stu-id="0c653-355">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="0c653-356">De volta à guia editor, abra `template.html` .</span><span class="sxs-lookup"><span data-stu-id="0c653-356">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="0c653-357">Exclua `<script src="/libs/lodash.js">` e `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="0c653-357">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="0c653-358">Aguarde até que o site seja rea build and re-deploy.</span><span class="sxs-lookup"><span data-stu-id="0c653-358">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="0c653-359">Audite a página novamente da **ferramenta Auditorias.**</span><span class="sxs-lookup"><span data-stu-id="0c653-359">Audit the page again from the **Audits** tool.</span></span>  <span data-ttu-id="0c653-360">Sua pontuação geral deve ter melhorado novamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-360">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Um relatório de auditorias após remover os recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="0c653-362">Um **relatório de auditorias** após remover os recursos de bloqueio de renderização</span><span class="sxs-lookup"><span data-stu-id="0c653-362">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a><span data-ttu-id="0c653-363">Otimizando o Caminho crítico de renderização no mundo real</span><span class="sxs-lookup"><span data-stu-id="0c653-363">Optimizing the Critical Rendering Path in the real-world</span></span>  

<span data-ttu-id="0c653-364">O **Caminho de Renderização Crítico** refere-se ao código que você precisa carregar uma página.</span><span class="sxs-lookup"><span data-stu-id="0c653-364">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="0c653-365">Em geral, acelere a carga da página enviando apenas código crítico durante a carga da página e carregando todo o resto.</span><span class="sxs-lookup"><span data-stu-id="0c653-365">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="0c653-366">É improvável que você consiga encontrar scripts que você possa remover de imediato, mas pode encontrar muitos scripts que você não precisa solicitar durante a carga da página e, em vez disso, pode ser solicitado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0c653-366">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--Navigate to [Using async or defer][async].  -->  
*   <span data-ttu-id="0c653-367">Se você estiver usando uma estrutura, verifique se ela tem um modo de produção.</span><span class="sxs-lookup"><span data-stu-id="0c653-367">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="0c653-368">Esse modo pode usar um recurso como [tremedeira][WebpackTreeShaking] de árvore para eliminar o código desnecessário que está bloqueando a renderização crítica.</span><span class="sxs-lookup"><span data-stu-id="0c653-368">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a><span data-ttu-id="0c653-369">Fazer menos trabalho de thread principal</span><span class="sxs-lookup"><span data-stu-id="0c653-369">Do less main thread work</span></span>  

<span data-ttu-id="0c653-370">Seu relatório mais recente mostra algumas pequenas economias potenciais na seção Oportunidades, mas se você olhar para baixo na seção Diagnósticos, parece que o maior a gargalo é a atividade de thread principal demais.</span><span class="sxs-lookup"><span data-stu-id="0c653-370">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="0c653-371">O thread principal é onde o navegador faz a maior parte do trabalho necessário para exibir uma página, como analisar e executar HTML, CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0c653-371">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="0c653-372">O objetivo é usar o painel Desempenho para analisar o trabalho que o thread principal está fazendo enquanto a página é carregada e encontrar maneiras de adiar ou remover o trabalho desnecessário.</span><span class="sxs-lookup"><span data-stu-id="0c653-372">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="0c653-373">Escolha a **ferramenta Desempenho.**</span><span class="sxs-lookup"><span data-stu-id="0c653-373">Choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="0c653-374">Escolha **Configurações de Captura** \( ![ Configurações de Captura ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0c653-374">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="0c653-375">Definir **Rede como** Slow **3G** e **CPU** como **6x de lentidão**.</span><span class="sxs-lookup"><span data-stu-id="0c653-375">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="0c653-376">Dispositivos móveis geralmente têm mais restrições de hardware do que laptops ou desktops, portanto, essas configurações permitem que você experimente a carga da página como se você estivesse usando um dispositivo menos poderoso.</span><span class="sxs-lookup"><span data-stu-id="0c653-376">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="0c653-377">Escolha **Atualizar** \( ![ Atualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0c653-377">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="0c653-378">O DevTools atualiza a página e produz uma visualização de todo o trabalho executado para carregar a página.</span><span class="sxs-lookup"><span data-stu-id="0c653-378">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="0c653-379">Essa visualização é chamada de **rastreamento**.</span><span class="sxs-lookup"><span data-stu-id="0c653-379">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="O rastreamento da ferramenta Performance da carga da página" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="0c653-381">O **rastreamento da** ferramenta Performance da carga da página</span><span class="sxs-lookup"><span data-stu-id="0c653-381">The **Performance** tool trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0c653-382">O rastreamento mostra a atividade cronologicamente, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="0c653-382">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="0c653-383">Os gráficos FPS, CPU e NET na parte superior dão uma visão geral dos quadros por segundo, atividade da CPU e atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="0c653-383">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="0c653-384">O bloco de amarelo realçado na figura após o próximo, a CPU estava completamente ocupada com a atividade de script.</span><span class="sxs-lookup"><span data-stu-id="0c653-384">The block of yellow highlighted in the figure after the next, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="0c653-385">Esta é uma dica de que você pode ser capaz de acelerar a carga da página fazendo menos trabalho javaScript.</span><span class="sxs-lookup"><span data-stu-id="0c653-385">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="A seção Visão geral do rastreamento" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="0c653-387">A seção Visão geral do rastreamento</span><span class="sxs-lookup"><span data-stu-id="0c653-387">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="0c653-388">Investigue o rastreamento para encontrar maneiras de fazer menos trabalho do JavaScript:</span><span class="sxs-lookup"><span data-stu-id="0c653-388">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="0c653-389">Escolha a **seção Timings** para expandi-la.</span><span class="sxs-lookup"><span data-stu-id="0c653-389">Choose the **Timings** section to expand it.</span></span>  <span data-ttu-id="0c653-390">Com base no fato de que pode haver várias medidas de [Timings][MDNUserTimingApi] do React, parece que o aplicativo de Tony está usando o modo de desenvolvimento do React.</span><span class="sxs-lookup"><span data-stu-id="0c653-390">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="0c653-391">Alternar para o modo de produção do React pode gerar algumas vitórias de desempenho fáceis.</span><span class="sxs-lookup"><span data-stu-id="0c653-391">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="A seção Timings" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="0c653-393">A **seção Timings**</span><span class="sxs-lookup"><span data-stu-id="0c653-393">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-394">Escolha **Timings** novamente para fechar essa seção.</span><span class="sxs-lookup"><span data-stu-id="0c653-394">Choose **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="0c653-395">Navegue pela **seção** Principal.</span><span class="sxs-lookup"><span data-stu-id="0c653-395">Browse the **Main** section.</span></span>  <span data-ttu-id="0c653-396">Esta seção mostra um log cronologicamente da atividade principal do thread, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="0c653-396">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="0c653-397">O eixo y (de cima para baixo) mostra por que os eventos ocorreram.</span><span class="sxs-lookup"><span data-stu-id="0c653-397">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="0c653-398">Por exemplo, na figueira após o seguinte, o evento fez com que a função seja executado, o que causou a sua executar, o que causou a sua realização `Evaluate Script` `(anonymous)` e assim por `(anonymous)` `__webpack__require__` diante.</span><span class="sxs-lookup"><span data-stu-id="0c653-398">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="A seção Principal" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="0c653-400">A **seção** Principal</span><span class="sxs-lookup"><span data-stu-id="0c653-400">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0c653-401">Role para baixo até a parte inferior da **seção** Principal.</span><span class="sxs-lookup"><span data-stu-id="0c653-401">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="0c653-402">Quando você usa uma estrutura, a maior parte da atividade superior é causada pela estrutura, que geralmente está fora de seu controle.</span><span class="sxs-lookup"><span data-stu-id="0c653-402">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="0c653-403">A atividade causada pelo aplicativo geralmente está na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="0c653-403">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="0c653-404">Neste aplicativo, parece que uma função chamada `App` está causando muitas solicitações a uma `mineBitcoin` função.</span><span class="sxs-lookup"><span data-stu-id="0c653-404">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="0c653-405">Parece que Tony pode estar usando os dispositivos de seus fãs para minerar a criptografia...</span><span class="sxs-lookup"><span data-stu-id="0c653-405">It sounds like Tony may be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Passe o mouse na atividade mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="0c653-407">Passe o mouse na `mineBitcoin` atividade</span><span class="sxs-lookup"><span data-stu-id="0c653-407">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="0c653-408">Embora as solicitações que sua estrutura faça geralmente estão fora de seu controle, às vezes, você pode estruturar seu aplicativo de uma maneira que faça com que a estrutura seja executado de forma ineficiente.</span><span class="sxs-lookup"><span data-stu-id="0c653-408">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="0c653-409">Reestruturar seu aplicativo para usar a estrutura com eficiência é uma maneira de fazer menos trabalho de thread principal.</span><span class="sxs-lookup"><span data-stu-id="0c653-409">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="0c653-410">No entanto, isso requer uma compreensão profunda de como sua estrutura funciona e que tipo de alterações você faz em seu próprio código para usar a estrutura com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="0c653-410">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="0c653-411">Expanda **a seção Bottom-Up.**</span><span class="sxs-lookup"><span data-stu-id="0c653-411">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="0c653-412">Essa guia divide quais atividades demorou mais tempo.</span><span class="sxs-lookup"><span data-stu-id="0c653-412">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="0c653-413">Se nada for exibido na seção Bottom-Up, escolha o rótulo para **a seção** Principal.</span><span class="sxs-lookup"><span data-stu-id="0c653-413">If nothing is displayed in the Bottom-Up section, choose the label for **Main** section.</span></span>  <span data-ttu-id="0c653-414">A **seção Bottom-Up** mostra apenas informações para qualquer atividade ou grupo de atividades que você selecionou no momento.</span><span class="sxs-lookup"><span data-stu-id="0c653-414">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="0c653-415">Por exemplo, se você escolher uma das atividades, a seção `mineBitcoin` **Bottom-Up** mostrará apenas informações para essa atividade.</span><span class="sxs-lookup"><span data-stu-id="0c653-415">For example, if you chose one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="A Bottom-Up guia" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="0c653-417">A **guia Bottom-Up**</span><span class="sxs-lookup"><span data-stu-id="0c653-417">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0c653-418">A **coluna Tempo Próprio** mostra quanto tempo foi gasto diretamente em cada atividade.</span><span class="sxs-lookup"><span data-stu-id="0c653-418">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="0c653-419">Por exemplo, na figura a seguir, cerca de 63% do tempo de thread principal foi gasto na `mineBitcoin` função.</span><span class="sxs-lookup"><span data-stu-id="0c653-419">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="0c653-420">Hora de revisar se o uso do modo de produção e a redução da atividade javaScript podem acelerar a carga da página.</span><span class="sxs-lookup"><span data-stu-id="0c653-420">Time to review whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="0c653-421">Comece com o modo de produção:</span><span class="sxs-lookup"><span data-stu-id="0c653-421">Start with production mode:</span></span>  

1.  <span data-ttu-id="0c653-422">Na guia editor, abra `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="0c653-422">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="0c653-423">Altere `"mode":"development"` para `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="0c653-423">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="0c653-424">Aguarde a implantação do novo build.</span><span class="sxs-lookup"><span data-stu-id="0c653-424">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="0c653-425">Audite a página novamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-425">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Um relatório de Auditorias após configurar o webpack para usar o modo de produção" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="0c653-427">Um relatório de Auditorias após configurar o webpack para usar o modo de produção</span><span class="sxs-lookup"><span data-stu-id="0c653-427">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0c653-428">Reduza a atividade do JavaScript removendo a solicitação para `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="0c653-428">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="0c653-429">Na guia editor, abra `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="0c653-429">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="0c653-430">Comente a solicitação `this.mineBitcoin(1500)` no `constructor` .</span><span class="sxs-lookup"><span data-stu-id="0c653-430">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="0c653-431">Aguarde a implantação do novo build.</span><span class="sxs-lookup"><span data-stu-id="0c653-431">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="0c653-432">Audite a página novamente.</span><span class="sxs-lookup"><span data-stu-id="0c653-432">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Um relatório de auditorias após remover o trabalho desnecessário do JavaScript" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="0c653-434">Um relatório de auditorias após remover o trabalho desnecessário do JavaScript</span><span class="sxs-lookup"><span data-stu-id="0c653-434">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0c653-435">Parece que a última alteração causou um grande salto no desempenho!</span><span class="sxs-lookup"><span data-stu-id="0c653-435">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="0c653-436">Esta seção forneceu uma breve introdução ao painel Desempenho.</span><span class="sxs-lookup"><span data-stu-id="0c653-436">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="0c653-437">Para saber mais sobre como analisar o desempenho da página, navegue até [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].</span><span class="sxs-lookup"><span data-stu-id="0c653-437">To learn more about how to analyze page performance, navigate to [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].</span></span>  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a><span data-ttu-id="0c653-438">Fazendo menos trabalho de thread principal no mundo real</span><span class="sxs-lookup"><span data-stu-id="0c653-438">Doing less main thread work in the real world</span></span>  

<span data-ttu-id="0c653-439">Em geral, a **ferramenta Performance** é a maneira mais comum de entender quais atividades o site faz à medida que carrega e encontrar maneiras de remover atividades desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="0c653-439">In general, the **Performance** tool is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="0c653-440">Se você preferir uma abordagem que se parece mais com , a API de Tempo do Usuário permite marcar arbitrariamente determinadas fases do ciclo de vida do aplicativo, a fim de rastrear quanto tempo cada uma dessas `console.log()` fases leva. [][MDNUserTimingApi]</span><span class="sxs-lookup"><span data-stu-id="0c653-440">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <a name="summary"></a><span data-ttu-id="0c653-441">Resumo</span><span class="sxs-lookup"><span data-stu-id="0c653-441">Summary</span></span>  

*   <span data-ttu-id="0c653-442">Sempre que você se definir para otimizar o desempenho de carga de um site, sempre comece com uma auditoria.</span><span class="sxs-lookup"><span data-stu-id="0c653-442">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="0c653-443">A auditoria estabelece uma linha de base e fornece dicas sobre como melhorar.</span><span class="sxs-lookup"><span data-stu-id="0c653-443">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="0c653-444">Faça uma alteração por vez e audite a página da Web após cada alteração para exibir como essa alteração isolada afeta o desempenho.</span><span class="sxs-lookup"><span data-stu-id="0c653-444">Make one change at a time, and audit the webpage after each change in order to display how that isolated change affects performance.</span></span>  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0c653-445">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0c653-445">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referência de análise de desempenho | Microsoft Docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introdução à classe desenvolvimento web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Otimização de Imagem Essencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Diretivas - Codificação de | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Api de tempo do usuário | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Árvore | webpack"  

> [!NOTE]
> <span data-ttu-id="0c653-452">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0c653-452">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0c653-453">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="0c653-453">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0c653-455">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0c653-455">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
