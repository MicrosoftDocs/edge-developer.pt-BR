---
description: Testando a acessibilidade usando a guia Acessibilidade.
title: Teste a acessibilidade usando a guia de Acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 839feed56fc82af2b4d96a081c476696166075b9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597240"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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
# <a name="test-accessibility-using-the-accessibility-tab"></a><span data-ttu-id="83046-104">Teste a acessibilidade usando a guia de Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="83046-104">Test accessibility using the Accessibility tab</span></span>

<span data-ttu-id="83046-105">A **guia Acessibilidade** é onde você visualiza a árvore de acessibilidade, os atributos do ARIA e as propriedades de acessibilidade calculadas dos nós DOM.</span><span class="sxs-lookup"><span data-stu-id="83046-105">The **Accessibility** tab is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="83046-106">Para abrir a **guia Acessibilidade:**</span><span class="sxs-lookup"><span data-stu-id="83046-106">To open the **Accessibility** tab:</span></span>

1.  <span data-ttu-id="83046-107">Selecione a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="83046-107">Select the **Elements** tool.</span></span>  
1.  <span data-ttu-id="83046-108">Na Árvore **DOM,** selecione o elemento que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="83046-108">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="83046-109">Selecione a **guia Acessibilidade.**  Talvez seja necessário selecionar primeiro o botão Mais **guias** \( o botão Mais guias \) à ![ direita da guia ](../media/more-tabs-icon.msft.png) **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="83046-109">Select the **Accessibility** tab.  You might need to first select the **More tabs** \(![the More tabs button](../media/more-tabs-icon.msft.png)\) button to the right of the **Styles** tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecione o elemento h1 da homepage DevTools na guia Acessibilidade" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="83046-111">`h1`Inspecione o elemento da homepage DevTools na guia **Acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="83046-111">Inspect the `h1` element of the DevTools homepage in the **Accessibility** tab</span></span>
:::image-end:::  


## <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="83046-112">Exibir a posição de um elemento na Árvore de Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="83046-112">View the position of an element in the Accessibility Tree</span></span>

<span data-ttu-id="83046-113">A [árvore de acessibilidade][MDNAccessibilityTree] é um subconjunto da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="83046-113">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="83046-114">A árvore de acessibilidade contém apenas elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página por meio de tecnologias assistivas, como leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="83046-114">The accessibility tree only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page through assistive technologies such as screen readers.</span></span>

<span data-ttu-id="83046-115">Inspecione a posição de um elemento na árvore de acessibilidade da **guia** Acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="83046-115">Inspect the position of an element in the accessibility tree from the **Accessibility** tab.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="A seção Árvore de Acessibilidade" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="83046-117">A **seção Árvore de** Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="83046-117">The **Accessibility Tree** section</span></span>  
:::image-end:::  


## <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="83046-118">Exibir os atributos ARIA de um elemento</span><span class="sxs-lookup"><span data-stu-id="83046-118">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="83046-119">Os atributos do ARIA garantem que tecnologias assistivas, como leitores de tela, tenham todas as informações necessárias para representar corretamente o conteúdo de uma página.</span><span class="sxs-lookup"><span data-stu-id="83046-119">ARIA attributes ensure that assistive technologies such as screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="83046-120">Exibir os atributos ARIA de um elemento na **guia Acessibilidade.**</span><span class="sxs-lookup"><span data-stu-id="83046-120">View the ARIA attributes of an element in the **Accessibility** tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="A seção Atributos do ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="83046-122">A **seção Atributos do ARIA**</span><span class="sxs-lookup"><span data-stu-id="83046-122">The **ARIA Attributes** section</span></span>  
:::image-end:::  


## <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="83046-123">Exibir as propriedades de acessibilidade calculadas de um elemento</span><span class="sxs-lookup"><span data-stu-id="83046-123">View the computed accessibility properties of an element</span></span>  


<span data-ttu-id="83046-124">Algumas propriedades de acessibilidade são calculadas dinamicamente pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="83046-124">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="83046-125">Essas propriedades são exibidas na seção **Propriedades Computadas** da guia **Acessibilidade.**</span><span class="sxs-lookup"><span data-stu-id="83046-125">These properties are displayed in the **Computed Properties** section of the **Accessibility** tab.</span></span>  

<span data-ttu-id="83046-126">Exibir as propriedades de acessibilidade calculadas de um elemento na guia **Acessibilidade.**</span><span class="sxs-lookup"><span data-stu-id="83046-126">View the computed accessibility properties of an element in the **Accessibility** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="83046-127">Para propriedades CSS calculadas, use a [guia Computed.][DevtoolsCssReferenceViewActuallyAppliedElements]</span><span class="sxs-lookup"><span data-stu-id="83046-127">For computed CSS properties, use the [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="A seção Propriedades Computadas da guia Acessibilidade" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="83046-129">A **seção Propriedades Computadas** da guia **Acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="83046-129">The **Computed Properties** section of the **Accessibility** tab</span></span>  
:::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="83046-130">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="83046-130">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="83046-131">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83046-131">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="83046-132">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="83046-132">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="83046-134">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83046-134">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Exibir apenas o CSS que é realmente aplicado a um elemento - Referência CSS | Microsoft Docs"  
[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árvore de acessibilidade (AOM) | MDN"  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
