---
title: Referência de acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 7417388023612b6e1ca651deba28e099e3c8e3d8
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581570"
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





# <span data-ttu-id="e04f5-103">Referência de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="e04f5-103">Accessibility Reference</span></span>   



<span data-ttu-id="e04f5-104">Esta página é uma referência abrangente dos recursos de acessibilidade no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e04f5-104">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="e04f5-105">Destina-se a desenvolvedores da Web que:</span><span class="sxs-lookup"><span data-stu-id="e04f5-105">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="e04f5-106">Tenha noções básicas sobre o DevTools, como abri-lo.</span><span class="sxs-lookup"><span data-stu-id="e04f5-106">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="e04f5-107">Estão familiarizados com [princípios de acessibilidade e práticas recomendadas][MDNAccessibility].</span><span class="sxs-lookup"><span data-stu-id="e04f5-107">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  

<span data-ttu-id="e04f5-108">A finalidade dessa referência é ajudar você a descobrir todas as ferramentas disponíveis no DevTools que ajudam a examinar a acessibilidade de uma página.</span><span class="sxs-lookup"><span data-stu-id="e04f5-108">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="e04f5-109">Consulte [navegando no Microsoft Edge devtools com tecnologia assistencial][DevtoolsAccessibilityNavigation] se você estiver procurando ajuda sobre como navegar no devtools com uma tecnologia assistencial como um leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="e04f5-109">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="e04f5-110">Visão geral dos recursos de acessibilidade no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e04f5-110">Overview of accessibility features in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="e04f5-111">Esta seção explica como o DevTools se encaixa no seu kit de ferramentas de acessibilidade geral.</span><span class="sxs-lookup"><span data-stu-id="e04f5-111">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="e04f5-112">Ao determinar se uma página está acessível, você precisa ter duas perguntas gerais em mente:</span><span class="sxs-lookup"><span data-stu-id="e04f5-112">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="e04f5-113">Você consegue navegar na página com um [leitor de tela][MDNScreenReader]ou teclado?</span><span class="sxs-lookup"><span data-stu-id="e04f5-113">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="e04f5-114">Os elementos da página são marcados corretamente para os leitores de tela?</span><span class="sxs-lookup"><span data-stu-id="e04f5-114">Are the elements of the page properly marked up for screen readers?</span></span>  

<span data-ttu-id="e04f5-115">Em geral, o DevTools deve ajudá-lo a corrigir erros relacionados a perguntas #2, pois esses erros são fáceis de detectar de maneira automatizada.</span><span class="sxs-lookup"><span data-stu-id="e04f5-115">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="e04f5-116">Pergunta #1 é tão importante, mas infelizmente, infelizmente, o DevTools não o ajuda.</span><span class="sxs-lookup"><span data-stu-id="e04f5-116">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="e04f5-117">A única maneira de encontrar erros relacionados a perguntas #1 é tentar usar uma página com um leitor de tela ou teclado.</span><span class="sxs-lookup"><span data-stu-id="e04f5-117">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="e04f5-118">Fazer auditoria da acessibilidade de uma página</span><span class="sxs-lookup"><span data-stu-id="e04f5-118">Audit the accessibility of a page</span></span>   

> [!NOTE]
> <span data-ttu-id="e04f5-119">O painel **auditorias** fornece links para conteúdo hospedado em sites de terceiros.</span><span class="sxs-lookup"><span data-stu-id="e04f5-119">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="e04f5-120">A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e todos os dados que possam ser coletados.</span><span class="sxs-lookup"><span data-stu-id="e04f5-120">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="e04f5-121">Em geral, use o painel auditorias para determinar se:</span><span class="sxs-lookup"><span data-stu-id="e04f5-121">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="e04f5-122">Uma página está marcada corretamente para leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="e04f5-122">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="e04f5-123">Os elementos de texto em uma página têm taxas de contraste suficientes.</span><span class="sxs-lookup"><span data-stu-id="e04f5-123">The text elements on a page have sufficient contrast ratios.</span></span> <span data-ttu-id="e04f5-124">Consulte também [exibir a taxa de contraste de um elemento de texto no seletor de cores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="e04f5-124">See also [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="e04f5-125">Para fazer auditoria em uma página:</span><span class="sxs-lookup"><span data-stu-id="e04f5-125">To audit a page:</span></span>  

1.  <span data-ttu-id="e04f5-126">Vá para a URL que você deseja auditar.</span><span class="sxs-lookup"><span data-stu-id="e04f5-126">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="e04f5-127">No DevTools, clique na guia **auditorias** .  O DevTools mostra várias opções de configuração.</span><span class="sxs-lookup"><span data-stu-id="e04f5-127">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    > ##### <span data-ttu-id="e04f5-128">Figura 1</span><span class="sxs-lookup"><span data-stu-id="e04f5-128">Figure 1</span></span>  
    > <span data-ttu-id="e04f5-129">Configurando auditorias</span><span class="sxs-lookup"><span data-stu-id="e04f5-129">Configuring audits</span></span>  
    > ![Configurando auditorias][ImageConfiguringAudits]  
    
    > [!NOTE]
    > <span data-ttu-id="e04f5-131">As capturas de tela desta seção foram tiradas com a versão 79 do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e04f5-131">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="e04f5-132">Você pode verificar qual versão está executando em `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="e04f5-132">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="e04f5-133">A interface do usuário do painel **auditoria** tem uma aparência diferente nas versões anteriores do Microsoft Edge, mas o fluxo de trabalho geral é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="e04f5-133">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="e04f5-134">Para **dispositivo**, selecione **móvel** se desejar simular um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="e04f5-134">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="e04f5-135">Essa opção muda a cadeia de caracteres do seu agente de usuário e redimensiona o visor.</span><span class="sxs-lookup"><span data-stu-id="e04f5-135">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="e04f5-136">Se a versão móvel da página for exibida de forma diferente da versão para área de trabalho, essa opção poderá ter um efeito significativo nos resultados da sua auditoria.</span><span class="sxs-lookup"><span data-stu-id="e04f5-136">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="e04f5-137">Na seção **auditorias** , certifique-se de que **acessibilidade** está ativada.</span><span class="sxs-lookup"><span data-stu-id="e04f5-137">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="e04f5-138">Desabilite as outras categorias se desejar excluí-las do relatório.</span><span class="sxs-lookup"><span data-stu-id="e04f5-138">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="e04f5-139">Deixe-os habilitados se você quiser descobrir outras maneiras de melhorar a qualidade da página.</span><span class="sxs-lookup"><span data-stu-id="e04f5-139">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="e04f5-140">A seção **throttling** permite que você controle a rede e a CPU, o que é útil para analisar o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="e04f5-140">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="e04f5-141">Essa opção deve ser irrelevante para a pontuação de acessibilidade, portanto, você pode usar o que preferir.</span><span class="sxs-lookup"><span data-stu-id="e04f5-141">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="e04f5-142">A caixa de seleção **limpar armazenamento** permite limpar todo o armazenamento antes de carregar a página ou preservar o armazenamento entre as cargas da página.</span><span class="sxs-lookup"><span data-stu-id="e04f5-142">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="e04f5-143">Essa opção também é provavelmente irrelevante para a pontuação de acessibilidade, portanto, você pode usar o que preferir.</span><span class="sxs-lookup"><span data-stu-id="e04f5-143">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="e04f5-144">Clique em **executar auditorias**.</span><span class="sxs-lookup"><span data-stu-id="e04f5-144">Click **Run Audits**.</span></span> <span data-ttu-id="e04f5-145">Após 10 a 30 segundos, o DevTools fornece um relatório.</span><span class="sxs-lookup"><span data-stu-id="e04f5-145">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="e04f5-146">Seu relatório oferece várias dicas sobre como melhorar a acessibilidade da página.</span><span class="sxs-lookup"><span data-stu-id="e04f5-146">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    > ##### <span data-ttu-id="e04f5-147">Figura 2</span><span class="sxs-lookup"><span data-stu-id="e04f5-147">Figure 2</span></span>  
    > <span data-ttu-id="e04f5-148">Um relatório</span><span class="sxs-lookup"><span data-stu-id="e04f5-148">A report</span></span>  
    > ![Um relatório][ImageReport]  
    
1.  <span data-ttu-id="e04f5-150">Clique em uma auditoria para saber mais sobre isso.</span><span class="sxs-lookup"><span data-stu-id="e04f5-150">Click an audit to learn more about it.</span></span>  
    
    > ##### <span data-ttu-id="e04f5-151">Figura 3</span><span class="sxs-lookup"><span data-stu-id="e04f5-151">Figure 3</span></span>  
    > <span data-ttu-id="e04f5-152">Mais informações sobre uma auditoria</span><span class="sxs-lookup"><span data-stu-id="e04f5-152">More information about an audit</span></span>  
    > ![Mais informações sobre uma auditoria][ImageAttributes]  
    
1.  <span data-ttu-id="e04f5-154">Clique em **saiba mais** para ver a documentação dessa auditoria.</span><span class="sxs-lookup"><span data-stu-id="e04f5-154">Click **Learn More** to view the documentation of that audit.</span></span>
    
    > ##### <span data-ttu-id="e04f5-155">Figura 4</span><span class="sxs-lookup"><span data-stu-id="e04f5-155">Figure 4</span></span>  
    > <span data-ttu-id="e04f5-156">Exibir a documentação de uma auditoria</span><span class="sxs-lookup"><span data-stu-id="e04f5-156">Viewing the documentation of an audit</span></span>  
    > ![Exibir a documentação de uma auditoria][ImageAuditDocumentation]  
    
### <span data-ttu-id="e04f5-158">Consulte também: extensão aXe</span><span class="sxs-lookup"><span data-stu-id="e04f5-158">See also: aXe extension</span></span>   

<span data-ttu-id="e04f5-159">Você pode preferir usar a [extensão Axe][ChromeWebStoreAxe] em vez do painel **auditorias** .</span><span class="sxs-lookup"><span data-stu-id="e04f5-159">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="e04f5-160">A extensão aXe geralmente fornece as mesmas informações, já que é o mecanismo subjacente que alimenta o painel auditorias.</span><span class="sxs-lookup"><span data-stu-id="e04f5-160">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="e04f5-161">A extensão aXe tem uma interface do usuário diferente e descreve as auditorias de forma ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="e04f5-161">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="e04f5-162">Uma vantagem de que a extensão aXe tem sobre o painel **auditorias** é que ele permite que você inspecione e destaque os nós com falha.</span><span class="sxs-lookup"><span data-stu-id="e04f5-162">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

> ##### <span data-ttu-id="e04f5-163">Figura 5</span><span class="sxs-lookup"><span data-stu-id="e04f5-163">Figure 5</span></span>  
> <span data-ttu-id="e04f5-164">A extensão aXe</span><span class="sxs-lookup"><span data-stu-id="e04f5-164">The aXe extension</span></span>  
> ![A extensão aXe][ImageAxeExtension]  

## <span data-ttu-id="e04f5-166">O painel Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="e04f5-166">The Accessibility pane</span></span>   

<span data-ttu-id="e04f5-167">O painel **acessibilidade** é onde você vê a árvore de acessibilidade, atributos do Aria e propriedades de acessibilidade calculadas dos nós dom.</span><span class="sxs-lookup"><span data-stu-id="e04f5-167">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="e04f5-168">Para abrir o painel de **acessibilidade** :</span><span class="sxs-lookup"><span data-stu-id="e04f5-168">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="e04f5-169">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="e04f5-169">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="e04f5-170">Na **árvore DOM**, selecione o elemento que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="e04f5-170">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="e04f5-171">Clique na guia **acessibilidade** .  Esta guia pode estar oculta atrás do botão **mais** guias ![ mais guias ][ImageMoreTabsIcon] .</span><span class="sxs-lookup"><span data-stu-id="e04f5-171">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** ![More Tabs][ImageMoreTabsIcon] button.</span></span>  

> ##### <span data-ttu-id="e04f5-172">Figura 6</span><span class="sxs-lookup"><span data-stu-id="e04f5-172">Figure 6</span></span>  
> <span data-ttu-id="e04f5-173">Inspecionar o `h1` elemento da home page do devtools no painel **acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="e04f5-173">Inspecting the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
> ![Inspecionar o elemento H1 da home page do DevTools no painel Acessibilidade][ImageA11yPane]  

### <span data-ttu-id="e04f5-175">Exibir a posição de um elemento na árvore de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="e04f5-175">View the position of an element in the accessibility tree</span></span>   

<span data-ttu-id="e04f5-176">A [árvore de acessibilidade][MDNAccessibilityTree] é um subconjunto da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="e04f5-176">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="e04f5-177">Ele somente contém elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página em um leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="e04f5-177">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="e04f5-178">Inspecione a posição de um elemento na árvore de acessibilidade no [painel Acessibilidade](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="e04f5-178">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="e04f5-179">Figura 7</span><span class="sxs-lookup"><span data-stu-id="e04f5-179">Figure 7</span></span>  
> <span data-ttu-id="e04f5-180">A seção de árvore de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="e04f5-180">The Accessibility Tree section</span></span>  
> ![A seção de árvore de acessibilidade][ImageAllyTree]  

### <span data-ttu-id="e04f5-182">Exibir os atributos do ARIA de um elemento</span><span class="sxs-lookup"><span data-stu-id="e04f5-182">View the ARIA attributes of an element</span></span>   

<span data-ttu-id="e04f5-183">Os atributos do ARIA garantem que os leitores de tela tenham todas as informações necessárias para representar adequadamente o conteúdo de uma página.</span><span class="sxs-lookup"><span data-stu-id="e04f5-183">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="e04f5-184">Exiba os atributos do ARIA de um elemento no [painel Acessibilidade](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="e04f5-184">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="e04f5-185">Figura 8</span><span class="sxs-lookup"><span data-stu-id="e04f5-185">Figure 8</span></span>  
> <span data-ttu-id="e04f5-186">A seção de atributos do ARIA</span><span class="sxs-lookup"><span data-stu-id="e04f5-186">The ARIA Attributes section</span></span>  
> ![A seção de atributos do ARIA][ImageAriaAttributesSection]  

### <span data-ttu-id="e04f5-188">Exibir as propriedades de acessibilidade calculadas de um elemento</span><span class="sxs-lookup"><span data-stu-id="e04f5-188">View the computed accessibility properties of an element</span></span>   

> [!NOTE]
> <span data-ttu-id="e04f5-189">Se você estiver procurando propriedades CSS calculadas, consulte a [guia calculada][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="e04f5-189">If you are looking for computed CSS properties, see the [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="e04f5-190">Algumas propriedades de acessibilidade são calculadas dinamicamente pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="e04f5-190">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="e04f5-191">Essas propriedades são exibidas na seção **Propriedades calculadas** do painel **acessibilidade** .</span><span class="sxs-lookup"><span data-stu-id="e04f5-191">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="e04f5-192">Exiba as propriedades de acessibilidade calculadas de um elemento no [painel Acessibilidade](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="e04f5-192">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="e04f5-193">Figura 9</span><span class="sxs-lookup"><span data-stu-id="e04f5-193">Figure 9</span></span>  
> <span data-ttu-id="e04f5-194">A seção Propriedades calculadas (acessibilidade)</span><span class="sxs-lookup"><span data-stu-id="e04f5-194">The Computed (Accessibility) Properties section</span></span>  
> ![A seção Propriedades calculadas (acessibilidade)][ImageComputedA11yPropertiesSection]  

## <span data-ttu-id="e04f5-196">Exibir a taxa de contraste de um elemento de texto no seletor de cores</span><span class="sxs-lookup"><span data-stu-id="e04f5-196">View the contrast ratio of a text element in the Color Picker</span></span>   

<span data-ttu-id="e04f5-197">Algumas pessoas com visão subnormal não veem áreas como muito brilhantes ou muito escuras.</span><span class="sxs-lookup"><span data-stu-id="e04f5-197">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="e04f5-198">Tudo tem a aparência da mesma forma de brilho, o que torna difícil distinguir estruturas de tópicos e bordas.</span><span class="sxs-lookup"><span data-stu-id="e04f5-198">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  
<span data-ttu-id="e04f5-199">A taxa de contraste mede a diferença de brilho entre o primeiro e o plano de fundo do texto.</span><span class="sxs-lookup"><span data-stu-id="e04f5-199">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="e04f5-200">Se o texto tiver uma taxa de contraste baixa, esses usuários com deficiência visual poderão ter literalmente o seu site como uma tela em branco.</span><span class="sxs-lookup"><span data-stu-id="e04f5-200">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="e04f5-201">O seletor de cores ajuda a verificar se o texto atende aos níveis de taxa de contraste recomendados:</span><span class="sxs-lookup"><span data-stu-id="e04f5-201">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="e04f5-202">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="e04f5-202">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="e04f5-203">Na **árvore DOM**, selecione o elemento de texto que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="e04f5-203">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    > ##### <span data-ttu-id="e04f5-204">Figura 10</span><span class="sxs-lookup"><span data-stu-id="e04f5-204">Figure 10</span></span>  
    > <span data-ttu-id="e04f5-205">Inspecionar um parágrafo na árvore DOM</span><span class="sxs-lookup"><span data-stu-id="e04f5-205">Inspecting a paragraph in the DOM Tree</span></span>  
    > ![Inspecionar um parágrafo na árvore DOM][ImageInspectDomTree]  
    
1.  <span data-ttu-id="e04f5-207">No painel **estilos** , clique no quadrado colorido ao lado do `color` valor do elemento.</span><span class="sxs-lookup"><span data-stu-id="e04f5-207">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    > ##### <span data-ttu-id="e04f5-208">Figura 11</span><span class="sxs-lookup"><span data-stu-id="e04f5-208">Figure 11</span></span>  
    > <span data-ttu-id="e04f5-209">A `color` Propriedade do elemento</span><span class="sxs-lookup"><span data-stu-id="e04f5-209">The `color` property of the element</span></span>  
    > ![A Propriedade Color do elemento][ImageColorElement]  
    
1.  <span data-ttu-id="e04f5-211">Marque a seção **taxa de contraste** do seletor de cores.</span><span class="sxs-lookup"><span data-stu-id="e04f5-211">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="e04f5-212">Uma marca de opção significa que o elemento atende à [recomendação mínima][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="e04f5-212">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="e04f5-213">Duas marcas de opção significa que ela atende à [recomendação aprimorada][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="e04f5-213">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>
    
    > ##### <span data-ttu-id="e04f5-214">Figura 12</span><span class="sxs-lookup"><span data-stu-id="e04f5-214">Figure 12</span></span>  
    > <span data-ttu-id="e04f5-215">A seção taxa de contraste do seletor de cores mostra 2 marcas de seleção e um valor de</span><span class="sxs-lookup"><span data-stu-id="e04f5-215">The Contrast Ratio section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    > ![A seção taxa de contraste do seletor de cores mostra duas marcas de seleção e um valor de 13,97][ImageColorPickerContrastRatio]  
    
1.  <span data-ttu-id="e04f5-217">Clique na seção **taxa de contraste** para ver mais informações.</span><span class="sxs-lookup"><span data-stu-id="e04f5-217">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="e04f5-218">Uma linha aparece no seletor Visual na parte superior do seletor de cores.</span><span class="sxs-lookup"><span data-stu-id="e04f5-218">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="e04f5-219">Se a cor atual atender às recomendações, qualquer coisa no mesmo lado da linha também atenderá às recomendações.</span><span class="sxs-lookup"><span data-stu-id="e04f5-219">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="e04f5-220">Se a cor atual não atender às recomendações, qualquer coisa no mesmo lado também não atende às recomendações.</span><span class="sxs-lookup"><span data-stu-id="e04f5-220">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    > ##### <span data-ttu-id="e04f5-221">Figura 13</span><span class="sxs-lookup"><span data-stu-id="e04f5-221">Figure 13</span></span>  
    > <span data-ttu-id="e04f5-222">A linha de taxa de contraste no seletor Visual</span><span class="sxs-lookup"><span data-stu-id="e04f5-222">The Contrast Ratio Line in the visual picker</span></span>  
    > ![A linha de taxa de contraste no seletor Visual][ImageContrastRatioLine]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  

[ImageConfiguringAudits]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-pane.msft.png "Figura 1: Configurando auditorias"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result.msft.png "Figura 2: uma figura"  
[ImageAttributes]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result-issues-expanded.msft.png "Figura 3: mais informações sobre uma auditoria"  
[ImageAuditDocumentation]: /microsoft-edge/devtools-guide-chromium/media/accessibility-web-dev-accessibility-audits-learn-more.msft.png "Figura 4: exibindo a documentação de uma auditoria"  
[ImageAxeExtension]: /microsoft-edge/devtools-guide-chromium/media/accessibility-devtools-extension-axe-panel.msft.png "Figura 5: a extensão aXe"  
[ImageA11yPane]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility.msft.png "Figura 6: inspecionando o elemento H1 da página inicial do DevTools no painel de acessibilidade"  
[ImageAllyTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-tree.msft.png "Figura 7: seção de árvore de acessibilidade"  
[ImageAriaAttributesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-aria-attributes.msft.png "Figura 8: seção atributos do ARIA"  
[ImageComputedA11yPropertiesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-computed-properties.msft.png "Figura 9: seção de propriedades calculadas (acessibilidade)"  
[ImageInspectDomTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-paragraph-highlight.msft.png "Figura 10: inspecionar um parágrafo na árvore DOM"  
[ImageColorElement]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color.msft.png "Figura 11: a Propriedade Color do elemento"  
[ImageColorPickerContrastRatio]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png "Figura 12: a seção índice de contraste do seletor de cores mostra 2 marcas de seleção e um valor de 13,97"  
[ImageContrastRatioLine]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png "Figura 13: linha de proporção de contraste no seletor Visual"  
<!-- links -->  

[DevtoolsAccessibilityNavigation]: navigation.md "Navegar no Microsoft Edge DevTools com tecnologia assistencial"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Exibir somente a CSS que realmente é aplicada a um elemento-referência de elemento CSS"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe-teste de acessibilidade na Web-Web Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árvore de acessibilidade (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Acessibilidade | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Leitor de tela | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (aprimorado) nível AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nível AA | W3C"  

> [!NOTE]
> <span data-ttu-id="e04f5-245">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="e04f5-245">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e04f5-246">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e04f5-246">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e04f5-248">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e04f5-248">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
