---
description: Uma referência abrangente dos recursos de acessibilidade no Microsoft Edge DevTools.
title: Referência de acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: de8f4bee6fef7725af9b97fb80ab45582dfa2286
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125311"
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

# <span data-ttu-id="3dd20-104">Referência de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="3dd20-104">Accessibility reference</span></span>  

<span data-ttu-id="3dd20-105">Esta página é uma referência abrangente dos recursos de acessibilidade no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3dd20-105">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="3dd20-106">Destina-se a desenvolvedores da Web que:</span><span class="sxs-lookup"><span data-stu-id="3dd20-106">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="3dd20-107">Tenha noções básicas sobre o DevTools, como abri-lo.</span><span class="sxs-lookup"><span data-stu-id="3dd20-107">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="3dd20-108">Estão familiarizados com [princípios de acessibilidade e práticas recomendadas][MDNAccessibility].</span><span class="sxs-lookup"><span data-stu-id="3dd20-108">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="3dd20-109">A finalidade dessa referência é ajudar você a descobrir todas as ferramentas disponíveis no DevTools que ajudam a examinar a acessibilidade de uma página.</span><span class="sxs-lookup"><span data-stu-id="3dd20-109">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="3dd20-110">Consulte [navegando no Microsoft Edge devtools com tecnologia assistencial][DevtoolsAccessibilityNavigation] se você estiver procurando ajuda sobre como navegar no devtools com uma tecnologia assistencial como um leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="3dd20-110">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="3dd20-111">Visão geral dos recursos de acessibilidade no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3dd20-111">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="3dd20-112">Esta seção explica como o DevTools se encaixa no seu kit de ferramentas de acessibilidade geral.</span><span class="sxs-lookup"><span data-stu-id="3dd20-112">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="3dd20-113">Ao determinar se uma página está acessível, você precisa ter duas perguntas gerais em mente:</span><span class="sxs-lookup"><span data-stu-id="3dd20-113">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="3dd20-114">Você consegue navegar na página com um [leitor de tela][MDNScreenReader]ou teclado?</span><span class="sxs-lookup"><span data-stu-id="3dd20-114">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="3dd20-115">Os elementos da página são marcados corretamente para os leitores de tela?</span><span class="sxs-lookup"><span data-stu-id="3dd20-115">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="3dd20-116">Em geral, o DevTools deve ajudá-lo a corrigir erros relacionados a perguntas #2, pois esses erros são fáceis de detectar de maneira automatizada.</span><span class="sxs-lookup"><span data-stu-id="3dd20-116">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="3dd20-117">Pergunta #1 é tão importante, mas infelizmente, infelizmente, o DevTools não o ajuda.</span><span class="sxs-lookup"><span data-stu-id="3dd20-117">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="3dd20-118">A única maneira de encontrar erros relacionados a perguntas #1 é tentar usar uma página com um leitor de tela ou teclado.</span><span class="sxs-lookup"><span data-stu-id="3dd20-118">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="3dd20-119">Fazer auditoria da acessibilidade de uma página</span><span class="sxs-lookup"><span data-stu-id="3dd20-119">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="3dd20-120">O painel **auditorias** fornece links para conteúdo hospedado em sites de terceiros.</span><span class="sxs-lookup"><span data-stu-id="3dd20-120">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="3dd20-121">A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e todos os dados que possam ser coletados.</span><span class="sxs-lookup"><span data-stu-id="3dd20-121">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="3dd20-122">Em geral, use o painel auditorias para determinar se:</span><span class="sxs-lookup"><span data-stu-id="3dd20-122">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="3dd20-123">Uma página está marcada corretamente para leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="3dd20-123">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="3dd20-124">Os elementos de texto em uma página têm taxas de contraste suficientes.</span><span class="sxs-lookup"><span data-stu-id="3dd20-124">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="3dd20-125">Consulte [exibir a taxa de contraste de um elemento de texto no seletor de cores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="3dd20-125">See [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="3dd20-126">Para fazer auditoria em uma página:</span><span class="sxs-lookup"><span data-stu-id="3dd20-126">To audit a page:</span></span>  

1.  <span data-ttu-id="3dd20-127">Vá para a URL que você deseja auditar.</span><span class="sxs-lookup"><span data-stu-id="3dd20-127">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="3dd20-128">No DevTools, clique na guia **auditorias** .  O DevTools mostra várias opções de configuração.</span><span class="sxs-lookup"><span data-stu-id="3dd20-128">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="3dd20-130">Configurar auditorias</span><span class="sxs-lookup"><span data-stu-id="3dd20-130">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="3dd20-131">As capturas de tela desta seção foram tiradas com a versão 79 do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3dd20-131">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="3dd20-132">Você pode verificar qual versão está executando em `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="3dd20-132">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="3dd20-133">A interface do usuário do painel **auditoria** tem uma aparência diferente nas versões anteriores do Microsoft Edge, mas o fluxo de trabalho geral é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="3dd20-133">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="3dd20-134">Em **dispositivo**, escolha **celular** se desejar simular um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="3dd20-134">For **Device**, choose **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="3dd20-135">Essa opção muda a cadeia de caracteres do seu agente de usuário e redimensiona o visor.</span><span class="sxs-lookup"><span data-stu-id="3dd20-135">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="3dd20-136">Se a versão móvel da página for exibida de forma diferente da versão para área de trabalho, essa opção poderá ter um efeito significativo nos resultados da sua auditoria.</span><span class="sxs-lookup"><span data-stu-id="3dd20-136">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="3dd20-137">Na seção **auditorias** , certifique-se de que **acessibilidade** está ativada.</span><span class="sxs-lookup"><span data-stu-id="3dd20-137">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="3dd20-138">Desabilite as outras categorias se desejar excluí-las do relatório.</span><span class="sxs-lookup"><span data-stu-id="3dd20-138">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="3dd20-139">Deixe-os habilitados se você quiser descobrir outras maneiras de melhorar a qualidade da página.</span><span class="sxs-lookup"><span data-stu-id="3dd20-139">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="3dd20-140">A seção **throttling** permite que você controle a rede e a CPU, o que é útil para analisar o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="3dd20-140">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="3dd20-141">Essa opção deve ser irrelevante para a pontuação de acessibilidade, portanto, você pode usar o que preferir.</span><span class="sxs-lookup"><span data-stu-id="3dd20-141">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="3dd20-142">A caixa de seleção **limpar armazenamento** permite limpar todo o armazenamento antes de carregar a página ou preservar o armazenamento entre as cargas da página.</span><span class="sxs-lookup"><span data-stu-id="3dd20-142">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="3dd20-143">Essa opção também é provavelmente irrelevante para a pontuação de acessibilidade, portanto, você pode usar o que preferir.</span><span class="sxs-lookup"><span data-stu-id="3dd20-143">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="3dd20-144">Escolha **executar auditorias**.</span><span class="sxs-lookup"><span data-stu-id="3dd20-144">Choose **Run Audits**.</span></span> <span data-ttu-id="3dd20-145">Após 10 a 30 segundos, o DevTools fornece um relatório.</span><span class="sxs-lookup"><span data-stu-id="3dd20-145">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="3dd20-146">Seu relatório oferece várias dicas sobre como melhorar a acessibilidade da página.</span><span class="sxs-lookup"><span data-stu-id="3dd20-146">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="3dd20-148">Um relatório</span><span class="sxs-lookup"><span data-stu-id="3dd20-148">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3dd20-149">Clique em uma auditoria para saber mais sobre isso.</span><span class="sxs-lookup"><span data-stu-id="3dd20-149">Click an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="3dd20-151">Mais informações sobre uma auditoria</span><span class="sxs-lookup"><span data-stu-id="3dd20-151">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3dd20-152">Escolha **saiba mais** para ver a documentação da auditoria.</span><span class="sxs-lookup"><span data-stu-id="3dd20-152">Choose **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="3dd20-154">Exibir a documentação de uma auditoria</span><span class="sxs-lookup"><span data-stu-id="3dd20-154">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3dd20-155">Consulte também: extensão aXe</span><span class="sxs-lookup"><span data-stu-id="3dd20-155">See also: aXe extension</span></span>  

<span data-ttu-id="3dd20-156">Você pode preferir usar a [extensão Axe][ChromeWebStoreAxe] em vez do painel **auditorias** .</span><span class="sxs-lookup"><span data-stu-id="3dd20-156">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="3dd20-157">A extensão aXe geralmente fornece as mesmas informações, já que é o mecanismo subjacente que alimenta o painel auditorias.</span><span class="sxs-lookup"><span data-stu-id="3dd20-157">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="3dd20-158">A extensão aXe tem uma interface do usuário diferente e descreve as auditorias de forma ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="3dd20-158">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="3dd20-159">Uma vantagem de que a extensão aXe tem sobre o painel **auditorias** é que ele permite que você inspecione e destaque os nós com falha.</span><span class="sxs-lookup"><span data-stu-id="3dd20-159">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="3dd20-161">A extensão aXe</span><span class="sxs-lookup"><span data-stu-id="3dd20-161">The aXe extension</span></span>  
:::image-end:::  

## <span data-ttu-id="3dd20-162">O painel Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="3dd20-162">The Accessibility pane</span></span>  

<span data-ttu-id="3dd20-163">O painel **acessibilidade** é onde você vê a árvore de acessibilidade, atributos do Aria e propriedades de acessibilidade calculadas dos nós dom.</span><span class="sxs-lookup"><span data-stu-id="3dd20-163">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="3dd20-164">Para abrir o painel de **acessibilidade** :</span><span class="sxs-lookup"><span data-stu-id="3dd20-164">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="3dd20-165">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="3dd20-165">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="3dd20-166">Na **árvore DOM**, selecione o elemento que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="3dd20-166">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="3dd20-167">Clique na guia **acessibilidade** .  Esta guia pode estar oculta atrás do botão **mais guias** \ ( ![ mais guias ][ImageMoreTabsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3dd20-167">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="3dd20-169">Inspecionar o `h1` elemento da home page do devtools no painel **acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="3dd20-169">Inspect the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="3dd20-170">Exibir a posição de um elemento na árvore de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="3dd20-170">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="3dd20-171">A [árvore de acessibilidade][MDNAccessibilityTree] é um subconjunto da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="3dd20-171">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="3dd20-172">Ele somente contém elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página em um leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="3dd20-172">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="3dd20-173">Inspecione a posição de um elemento na árvore de acessibilidade no [painel Acessibilidade](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="3dd20-173">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="3dd20-175">A seção de **árvore de acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="3dd20-175">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <span data-ttu-id="3dd20-176">Exibir os atributos do ARIA de um elemento</span><span class="sxs-lookup"><span data-stu-id="3dd20-176">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="3dd20-177">Os atributos do ARIA garantem que os leitores de tela tenham todas as informações necessárias para representar adequadamente o conteúdo de uma página.</span><span class="sxs-lookup"><span data-stu-id="3dd20-177">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="3dd20-178">Exiba os atributos do ARIA de um elemento no [painel Acessibilidade](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="3dd20-178">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="3dd20-180">A seção de **atributos do Aria**</span><span class="sxs-lookup"><span data-stu-id="3dd20-180">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <span data-ttu-id="3dd20-181">Exibir as propriedades de acessibilidade calculadas de um elemento</span><span class="sxs-lookup"><span data-stu-id="3dd20-181">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="3dd20-182">Se você estiver procurando propriedades CSS calculadas, navegue até a [guia calculada][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="3dd20-182">If you are looking for computed CSS properties, navigate to [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="3dd20-183">Algumas propriedades de acessibilidade são calculadas dinamicamente pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="3dd20-183">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="3dd20-184">Essas propriedades são exibidas na seção **Propriedades calculadas** do painel **acessibilidade** .</span><span class="sxs-lookup"><span data-stu-id="3dd20-184">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="3dd20-185">Exiba as propriedades de acessibilidade calculadas de um elemento no [painel Acessibilidade](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="3dd20-185">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="3dd20-187">A seção **Propriedades calculadas** do painel **acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="3dd20-187">The **Computed Properties** section of the **Accessibility** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="3dd20-188">Exibir a taxa de contraste de um elemento de texto no seletor de cores</span><span class="sxs-lookup"><span data-stu-id="3dd20-188">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="3dd20-189">Algumas pessoas com visão subnormal não veem áreas como muito brilhantes ou muito escuras.</span><span class="sxs-lookup"><span data-stu-id="3dd20-189">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="3dd20-190">Tudo tem a aparência da mesma forma de brilho, o que torna difícil distinguir estruturas de tópicos e bordas.</span><span class="sxs-lookup"><span data-stu-id="3dd20-190">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="3dd20-191">A taxa de contraste mede a diferença de brilho entre o primeiro e o plano de fundo do texto.</span><span class="sxs-lookup"><span data-stu-id="3dd20-191">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="3dd20-192">Se o texto tiver uma taxa de contraste baixa, esses usuários com deficiência visual poderão ter literalmente o seu site como uma tela em branco.</span><span class="sxs-lookup"><span data-stu-id="3dd20-192">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="3dd20-193">O seletor de cores ajuda a verificar se o texto atende aos níveis de taxa de contraste recomendados:</span><span class="sxs-lookup"><span data-stu-id="3dd20-193">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="3dd20-194">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="3dd20-194">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="3dd20-195">Na **árvore DOM**, selecione o elemento de texto que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="3dd20-195">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="3dd20-197">Inspecionar um parágrafo na **árvore DOM**</span><span class="sxs-lookup"><span data-stu-id="3dd20-197">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3dd20-198">No painel **estilos** , clique no quadrado colorido ao lado do `color` valor do elemento.</span><span class="sxs-lookup"><span data-stu-id="3dd20-198">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="3dd20-200">A `color` Propriedade do elemento</span><span class="sxs-lookup"><span data-stu-id="3dd20-200">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3dd20-201">Marque a seção **taxa de contraste** do seletor de cores.</span><span class="sxs-lookup"><span data-stu-id="3dd20-201">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="3dd20-202">Uma marca de opção significa que o elemento atende à [recomendação mínima][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="3dd20-202">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="3dd20-203">Duas marcas de opção significa que ela atende à [recomendação aprimorada][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="3dd20-203">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="3dd20-205">A seção **taxa de contraste** do seletor de cores mostra 2 marcas de seleção e um valor de</span><span class="sxs-lookup"><span data-stu-id="3dd20-205">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="3dd20-206">Clique na seção **taxa de contraste** para ver mais informações.</span><span class="sxs-lookup"><span data-stu-id="3dd20-206">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="3dd20-207">Uma linha aparece no seletor Visual na parte superior do seletor de cores.</span><span class="sxs-lookup"><span data-stu-id="3dd20-207">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="3dd20-208">Se a cor atual atender às recomendações, qualquer coisa no mesmo lado da linha também atenderá às recomendações.</span><span class="sxs-lookup"><span data-stu-id="3dd20-208">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="3dd20-209">Se a cor atual não atender às recomendações, qualquer coisa no mesmo lado também não atende às recomendações.</span><span class="sxs-lookup"><span data-stu-id="3dd20-209">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="3dd20-211">A linha de **taxa de contraste** no seletor Visual</span><span class="sxs-lookup"><span data-stu-id="3dd20-211">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3dd20-212">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3dd20-212">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegar no Microsoft Edge DevTools com tecnologia assistencial | Documentos da Microsoft"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Exiba somente a CSS que realmente é aplicada a um elemento-referência de elemento CSS | Documentos da Microsoft"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe-teste de acessibilidade na Web-Web Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árvore de acessibilidade (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Acessibilidade | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Leitor de tela | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (aprimorado) nível AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nível AA | W3C"  

> [!NOTE]
> <span data-ttu-id="3dd20-221">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="3dd20-221">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3dd20-222">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3dd20-222">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3dd20-224">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3dd20-224">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
