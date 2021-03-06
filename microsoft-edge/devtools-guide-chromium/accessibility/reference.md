---
description: Uma referência abrangente dos recursos de acessibilidade no Microsoft Edge DevTools.
title: Referência de acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e3fed1c4e53c69b7a6837f71c270c0bf2f65b7e2
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398333"
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

# <a name="accessibility-reference"></a><span data-ttu-id="f20be-104">Referência de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="f20be-104">Accessibility reference</span></span>  

<span data-ttu-id="f20be-105">Esta página é uma referência abrangente dos recursos de acessibilidade no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="f20be-105">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="f20be-106">Destina-se a desenvolvedores web que:</span><span class="sxs-lookup"><span data-stu-id="f20be-106">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="f20be-107">Tenha uma compreensão básica do DevTools, como como abri-lo.</span><span class="sxs-lookup"><span data-stu-id="f20be-107">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="f20be-108">Estão familiarizados com [princípios de acessibilidade e práticas recomendadas.][MDNAccessibility]</span><span class="sxs-lookup"><span data-stu-id="f20be-108">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="f20be-109">O objetivo dessa referência é ajudá-lo a descobrir todas as ferramentas disponíveis no DevTools que o ajudam a examinar a acessibilidade de uma página.</span><span class="sxs-lookup"><span data-stu-id="f20be-109">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="f20be-110">Se você estiver procurando ajuda para navegar no DevTools com uma tecnologia auxiliar, como um leitor de tela, navegue até Navegar pelo [Microsoft Edge DevTools][DevtoolsAccessibilityNavigation]com tecnologia assistida.</span><span class="sxs-lookup"><span data-stu-id="f20be-110">If you are looking for help on navigating DevTools with an assistive technology like a screen reader, navigate to [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation].</span></span>  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a><span data-ttu-id="f20be-111">Visão geral dos recursos de acessibilidade no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f20be-111">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f20be-112">Esta seção explica como o DevTools se encaixa no kit de ferramentas de acessibilidade geral.</span><span class="sxs-lookup"><span data-stu-id="f20be-112">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="f20be-113">Ao determinar se uma página está acessível, você precisa ter duas perguntas gerais em mente:</span><span class="sxs-lookup"><span data-stu-id="f20be-113">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="f20be-114">Você é capaz de navegar na página com um teclado ou [um leitor de tela?][MDNScreenReader]</span><span class="sxs-lookup"><span data-stu-id="f20be-114">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="f20be-115">Os elementos da página estão marcados corretamente para leitores de tela?</span><span class="sxs-lookup"><span data-stu-id="f20be-115">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="f20be-116">Em geral, o DevTools deve ajudá-lo a corrigir erros relacionados a perguntas #2, pois esses erros são fáceis de detectar de forma automatizada.</span><span class="sxs-lookup"><span data-stu-id="f20be-116">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="f20be-117">A #1 de perguntas é tão importante quanto, mas infelizmente o DevTools não o ajuda lá.</span><span class="sxs-lookup"><span data-stu-id="f20be-117">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="f20be-118">A única maneira de encontrar erros relacionados à #1 é tentar usar uma página com um teclado ou leitor de tela por conta própria.</span><span class="sxs-lookup"><span data-stu-id="f20be-118">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a><span data-ttu-id="f20be-119">Auditar a acessibilidade de uma página</span><span class="sxs-lookup"><span data-stu-id="f20be-119">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="f20be-120">A **ferramenta Auditorias** fornece links para conteúdo hospedado em sites de terceiros.</span><span class="sxs-lookup"><span data-stu-id="f20be-120">The **Audits** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="f20be-121">A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e quaisquer dados que possam ser coletados.</span><span class="sxs-lookup"><span data-stu-id="f20be-121">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="f20be-122">Em geral, use o painel Auditorias para determinar se:</span><span class="sxs-lookup"><span data-stu-id="f20be-122">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="f20be-123">Uma página é marcada corretamente para leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="f20be-123">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="f20be-124">Os elementos de texto em uma página têm taxas de contraste suficientes.</span><span class="sxs-lookup"><span data-stu-id="f20be-124">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="f20be-125">Navegue [até Exibir a taxa de contraste de um elemento de texto no Selador de Cores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="f20be-125">Navigate to [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="f20be-126">Para auditar uma página:</span><span class="sxs-lookup"><span data-stu-id="f20be-126">To audit a page:</span></span>  

1.  <span data-ttu-id="f20be-127">Navegue até a URL que você deseja auditar.</span><span class="sxs-lookup"><span data-stu-id="f20be-127">Navigate to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="f20be-128">No DevTools, escolha a **ferramenta Auditorias.**</span><span class="sxs-lookup"><span data-stu-id="f20be-128">In DevTools, choose the **Audits** tool.</span></span>  <span data-ttu-id="f20be-129">O DevTools mostra várias opções de configuração.</span><span class="sxs-lookup"><span data-stu-id="f20be-129">DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="f20be-131">Configurar auditorias</span><span class="sxs-lookup"><span data-stu-id="f20be-131">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="f20be-132">As capturas de tela nesta seção foram feitas com a versão 79 do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f20be-132">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="f20be-133">Você pode verificar qual versão está executando em `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="f20be-133">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="f20be-134">A **interface do usuário da** ferramenta Auditorias parece diferente em versões anteriores do Microsoft Edge, mas o fluxo de trabalho geral é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="f20be-134">The **Audits** tool UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="f20be-135">Para **Dispositivo**, escolha **Móvel** se quiser simular um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="f20be-135">For **Device**, choose **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="f20be-136">Essa opção altera a cadeia de caracteres do agente do usuário e resize o viewport.</span><span class="sxs-lookup"><span data-stu-id="f20be-136">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="f20be-137">Se a versão móvel da página for exibida de forma diferente da versão da área de trabalho, essa opção poderá ter um efeito significativo nos resultados da auditoria.</span><span class="sxs-lookup"><span data-stu-id="f20be-137">If the mobile version of the page displays differently than the desktop version, this option may have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="f20be-138">Na seção **Auditorias,** certifique-se de **que a Acessibilidade** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f20be-138">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="f20be-139">Desabilite as outras categorias se quiser exclui-las do relatório.</span><span class="sxs-lookup"><span data-stu-id="f20be-139">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="f20be-140">Deixe-os habilitados se você quiser descobrir outras maneiras de melhorar a qualidade da sua página.</span><span class="sxs-lookup"><span data-stu-id="f20be-140">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="f20be-141">A **seção Throttling** permite que você reduza a rede e a CPU, o que é útil ao analisar o desempenho da carga.</span><span class="sxs-lookup"><span data-stu-id="f20be-141">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="f20be-142">Essa opção deve ser irrelevante para sua pontuação de acessibilidade, portanto, você pode usar o que preferir.</span><span class="sxs-lookup"><span data-stu-id="f20be-142">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="f20be-143">A **caixa de seleção** Limpar Armazenamento permite limpar todo o armazenamento antes de carregar a página ou preservar o armazenamento entre cargas de página.</span><span class="sxs-lookup"><span data-stu-id="f20be-143">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="f20be-144">Essa opção também provavelmente é irrelevante para sua pontuação de acessibilidade, portanto, você pode usar o que preferir.</span><span class="sxs-lookup"><span data-stu-id="f20be-144">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="f20be-145">Escolha **Executar Auditorias**.</span><span class="sxs-lookup"><span data-stu-id="f20be-145">Choose **Run Audits**.</span></span> <span data-ttu-id="f20be-146">Após 10 a 30 segundos, o DevTools fornece um relatório.</span><span class="sxs-lookup"><span data-stu-id="f20be-146">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="f20be-147">Seu relatório fornece várias dicas sobre como melhorar a acessibilidade da página.</span><span class="sxs-lookup"><span data-stu-id="f20be-147">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Um relatório" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="f20be-149">Um relatório</span><span class="sxs-lookup"><span data-stu-id="f20be-149">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f20be-150">Escolha uma auditoria para saber mais sobre ela.</span><span class="sxs-lookup"><span data-stu-id="f20be-150">Choose an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Mais informações sobre uma auditoria" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="f20be-152">Mais informações sobre uma auditoria</span><span class="sxs-lookup"><span data-stu-id="f20be-152">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f20be-153">Escolha **Saber mais** para exibir a documentação dessa auditoria.</span><span class="sxs-lookup"><span data-stu-id="f20be-153">Choose **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Exibir a documentação de uma auditoria" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="f20be-155">Exibir a documentação de uma auditoria</span><span class="sxs-lookup"><span data-stu-id="f20be-155">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a><span data-ttu-id="f20be-156">Consulte também: extensão aXe</span><span class="sxs-lookup"><span data-stu-id="f20be-156">See also: aXe extension</span></span>  

<span data-ttu-id="f20be-157">Você pode preferir usar a extensão [aXe em][ChromeWebStoreAxe] vez da **ferramenta Auditorias.**</span><span class="sxs-lookup"><span data-stu-id="f20be-157">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** tool.</span></span>  
<span data-ttu-id="f20be-158">A extensão aXe geralmente fornece as mesmas informações, já que é o mecanismo subjacente que alimenta o painel auditorias.</span><span class="sxs-lookup"><span data-stu-id="f20be-158">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="f20be-159">A extensão aXe tem uma interface do usuário diferente e descreve as auditorias um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="f20be-159">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="f20be-160">Uma vantagem que a extensão aXe tem sobre a ferramenta **Auditorias** é que ela permite inspecionar e realçar nós com falha.</span><span class="sxs-lookup"><span data-stu-id="f20be-160">One advantage that the aXe extension has over the **Audits** tool is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="A extensão aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="f20be-162">A extensão aXe</span><span class="sxs-lookup"><span data-stu-id="f20be-162">The aXe extension</span></span>  
:::image-end:::  

## <a name="the-accessibility-panel"></a><span data-ttu-id="f20be-163">O painel Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="f20be-163">The Accessibility panel</span></span>  

<span data-ttu-id="f20be-164">O **painel Acessibilidade** é onde você visualiza a árvore de acessibilidade, os atributos do ARIA e as propriedades de acessibilidade calculadas dos nós DOM.</span><span class="sxs-lookup"><span data-stu-id="f20be-164">The **Accessibility** panel is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="f20be-165">Para abrir o **painel Acessibilidade:**</span><span class="sxs-lookup"><span data-stu-id="f20be-165">To open the **Accessibility** panel:</span></span>  

1.  <span data-ttu-id="f20be-166">Escolha a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="f20be-166">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="f20be-167">Na Árvore **DOM,** selecione o elemento que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="f20be-167">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="f20be-168">Escolha o **painel Acessibilidade.**</span><span class="sxs-lookup"><span data-stu-id="f20be-168">Choose the **Accessibility** panel.</span></span>  <span data-ttu-id="f20be-169">Esse painel pode estar oculto atrás do **botão Mais Guias** \( Mais Guias ![ ][ImageMoreTabsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f20be-169">This panel may be hidden behind the **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecione o elemento h1 da homepage DevTools no painel Acessibilidade" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="f20be-171">Inspecionar o `h1` elemento da homepage DevTools no painel **Acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="f20be-171">Inspect the `h1` element of the DevTools homepage in the **Accessibility** panel</span></span>  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="f20be-172">Exibir a posição de um elemento na árvore de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="f20be-172">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="f20be-173">A [árvore de acessibilidade][MDNAccessibilityTree] é um subconjunto da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="f20be-173">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="f20be-174">Ele contém apenas elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página em um leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="f20be-174">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="f20be-175">Inspecione a posição de um elemento na árvore de acessibilidade do painel [Acessibilidade.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="f20be-175">Inspect the position of an element in the accessibility tree from the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="A seção Árvore de Acessibilidade" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="f20be-177">A **seção Árvore de** Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="f20be-177">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="f20be-178">Exibir os atributos ARIA de um elemento</span><span class="sxs-lookup"><span data-stu-id="f20be-178">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="f20be-179">Os atributos do ARIA garantem que os leitores de tela tenham todas as informações necessárias para representar corretamente o conteúdo de uma página.</span><span class="sxs-lookup"><span data-stu-id="f20be-179">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="f20be-180">Exibir os atributos ARIA de um elemento no [painel Acessibilidade.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="f20be-180">View the ARIA attributes of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="A seção Atributos do ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="f20be-182">A **seção Atributos do ARIA**</span><span class="sxs-lookup"><span data-stu-id="f20be-182">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="f20be-183">Exibir as propriedades de acessibilidade calculadas de um elemento</span><span class="sxs-lookup"><span data-stu-id="f20be-183">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="f20be-184">Se você estiver procurando propriedades CSS calculadas, navegue até [Painel Computado.][DevtoolsCssReferenceViewActuallyAppliedElements]</span><span class="sxs-lookup"><span data-stu-id="f20be-184">If you are looking for computed CSS properties, navigate to [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] panel.</span></span>  

<span data-ttu-id="f20be-185">Algumas propriedades de acessibilidade são calculadas dinamicamente pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="f20be-185">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="f20be-186">Essas propriedades são exibidas na seção **Propriedades Computadas** do painel **Acessibilidade.**</span><span class="sxs-lookup"><span data-stu-id="f20be-186">These properties are displayed in the **Computed Properties** section of the **Accessibility** panel.</span></span>  

<span data-ttu-id="f20be-187">Exibir as propriedades de acessibilidade calculadas de um elemento no painel [Acessibilidade.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="f20be-187">View the computed accessibility properties of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="A seção Propriedades Computadas do painel Acessibilidade" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="f20be-189">A **seção Propriedades Computadas** do painel **Acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="f20be-189">The **Computed Properties** section of the **Accessibility** panel</span></span>  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a><span data-ttu-id="f20be-190">Exibir a taxa de contraste de um elemento de texto no Selador de Cores</span><span class="sxs-lookup"><span data-stu-id="f20be-190">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="f20be-191">Algumas pessoas com baixa visão não veem áreas muito claras ou muito escuras.</span><span class="sxs-lookup"><span data-stu-id="f20be-191">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="f20be-192">Tudo tende a aparecer com o mesmo brilho, o que dificulta a distinção de contornos e bordas.</span><span class="sxs-lookup"><span data-stu-id="f20be-192">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="f20be-193">A taxa de contraste mede a diferença no brilho entre o primeiro plano e o plano de fundo do texto.</span><span class="sxs-lookup"><span data-stu-id="f20be-193">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="f20be-194">Se o texto tiver uma taxa de contraste baixa, esses usuários de baixa visão poderão literalmente experimentar seu site como uma tela em branco.</span><span class="sxs-lookup"><span data-stu-id="f20be-194">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="f20be-195">O Selador de Cores ajuda você a verificar se seu texto atende aos níveis de taxa de contraste recomendados:</span><span class="sxs-lookup"><span data-stu-id="f20be-195">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="f20be-196">Escolha a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="f20be-196">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="f20be-197">Na Árvore **DOM,** selecione o elemento de texto que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="f20be-197">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecionar um parágrafo na árvore DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="f20be-199">Inspecionar um parágrafo na árvore **DOM**</span><span class="sxs-lookup"><span data-stu-id="f20be-199">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f20be-200">No painel **Estilos,** escolha o quadrado de cores ao lado `color` do valor do elemento.</span><span class="sxs-lookup"><span data-stu-id="f20be-200">In the **Styles** panel, choose the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="A propriedade color do elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="f20be-202">A `color` propriedade do elemento</span><span class="sxs-lookup"><span data-stu-id="f20be-202">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f20be-203">Verifique a **seção Taxa de** Contraste do Selador de Cores.</span><span class="sxs-lookup"><span data-stu-id="f20be-203">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="f20be-204">Uma marca de seleção significa que o elemento atende à [recomendação mínima][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="f20be-204">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="f20be-205">Dois indicadores de verificação significam que ele atende [à recomendação aprimorada][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="f20be-205">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="A seção Taxa de Contraste do Se picker de cores mostra 2 marcas de seleção e um valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="f20be-207">A **seção Taxa** de Contraste do Selador de Cores mostra 2 marcas de seleção e um valor de</span><span class="sxs-lookup"><span data-stu-id="f20be-207">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="f20be-208">Para obter mais informações, escolha a seção **Taxa de Contraste.**</span><span class="sxs-lookup"><span data-stu-id="f20be-208">For more information, choose the **Contrast Ratio** section.</span></span>  <span data-ttu-id="f20be-209">Uma linha aparece no se picker visual na parte superior do Selador de Cores.</span><span class="sxs-lookup"><span data-stu-id="f20be-209">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="f20be-210">Se a cor atual atender às recomendações, qualquer coisa do mesmo lado da linha também atende às recomendações.</span><span class="sxs-lookup"><span data-stu-id="f20be-210">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="f20be-211">Se a cor atual não atender às recomendações, qualquer coisa do mesmo lado também não atenderá às recomendações.</span><span class="sxs-lookup"><span data-stu-id="f20be-211">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="A Linha de Taxa de Contraste no selador visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="f20be-213">A **Linha de Taxa** de Contraste no selador visual</span><span class="sxs-lookup"><span data-stu-id="f20be-213">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f20be-214">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f20be-214">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegue pelo Microsoft Edge DevTools com tecnologia | Microsoft Docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Exibir apenas o CSS que é realmente aplicado a um elemento - Referência CSS | Microsoft Docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Teste de Acessibilidade da Web - Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árvore de acessibilidade (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Acessibilidade | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Leitor de tela | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Nível AAA de contraste (aprimorado) | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Nível AA de contraste (mínimo) | W3C"  

> [!NOTE]
> <span data-ttu-id="f20be-223">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f20be-223">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f20be-224">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="f20be-224">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f20be-226">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f20be-226">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
