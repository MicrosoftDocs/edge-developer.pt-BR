---
description: Testar contraste de cor de texto usando o Selador de Cores.
title: Teste o contraste da cor do texto usando o Seletor de Cor
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f4ba5f3706460c443ae06a393e5ef63e5d336229
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597236"
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
# <a name="test-text-color-contrast-using-the-color-picker"></a><span data-ttu-id="1a759-104">Teste o contraste da cor do texto usando o Seletor de Cor</span><span class="sxs-lookup"><span data-stu-id="1a759-104">Test text-color contrast using the Color Picker</span></span>

<span data-ttu-id="1a759-105">Pessoas com baixa visão podem não ver áreas muito claras ou muito escuras.</span><span class="sxs-lookup"><span data-stu-id="1a759-105">People with low vision may not see areas that are very bright or very dark.</span></span>  <span data-ttu-id="1a759-106">Tudo tende a aparecer no mesmo nível de brilho, o que dificulta a distinção de contornos e bordas.</span><span class="sxs-lookup"><span data-stu-id="1a759-106">Everything tends to appear at about the same level of brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="1a759-107">A taxa de contraste mede a diferença no brilho entre o primeiro plano e o plano de fundo do texto.</span><span class="sxs-lookup"><span data-stu-id="1a759-107">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="1a759-108">Se o texto tiver uma taxa de contraste baixa, as pessoas com baixa visão poderão experimentar seu site como uma tela em branco.</span><span class="sxs-lookup"><span data-stu-id="1a759-108">If your text has a low contrast ratio, then people with low vision may experience your site as a blank screen.</span></span>  

<span data-ttu-id="1a759-109">No DevTools, uma maneira de exibir a taxa de contraste de um elemento de texto é usar o Selador de Cores, na guia **Estilos.**  O Selador de Cores ajuda você a verificar se seu texto atende aos níveis de taxa de contraste recomendados.</span><span class="sxs-lookup"><span data-stu-id="1a759-109">In DevTools, one way to view the contrast ratio of a text element is to use the Color Picker, from the **Styles** tab.  The Color Picker helps you verify that your text meets recommended contrast ratio levels.</span></span>

**<span data-ttu-id="1a759-110">Para verificar o contraste de cor de texto usando o Se picker de cores:</span><span class="sxs-lookup"><span data-stu-id="1a759-110">To check the text-color contrast using the Color Picker:</span></span>**

1.  <span data-ttu-id="1a759-111">Em DevTools, selecione a **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="1a759-111">In DevTools, select the **Elements** tool.</span></span>  
1.  <span data-ttu-id="1a759-112">Na Árvore **DOM,** selecione o elemento de texto que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="1a759-112">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecionar um parágrafo na árvore DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="1a759-114">Inspecionar um parágrafo na árvore **DOM**</span><span class="sxs-lookup"><span data-stu-id="1a759-114">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1a759-115">Na guia **Estilos,** localize a propriedade **color** aplicada ao elemento e selecione o quadrado de cores ao lado da **propriedade color.**</span><span class="sxs-lookup"><span data-stu-id="1a759-115">On the **Styles** tab, locate the **color** property that's applied to the element, and then select the color square next to the **color** property.</span></span>
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="A propriedade color do elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="1a759-117">A `color` propriedade do elemento</span><span class="sxs-lookup"><span data-stu-id="1a759-117">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1a759-118">Examine a **seção Taxa** de Contraste do Selador de Cores.</span><span class="sxs-lookup"><span data-stu-id="1a759-118">Examine the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="1a759-119">Uma marca de verificação significa que o elemento atende à [recomendação mínima][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="1a759-119">One check mark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="1a759-120">Duas marcas de verificação significam que ela atende [à recomendação aprimorada][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="1a759-120">Two check marks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="A seção Taxa de Contraste do Selador de Cores mostra 2 marcas de verificação e um valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="1a759-122">A **seção Taxa de** Contraste do Selador de Cores mostra 2 marcas de verificação e um valor de</span><span class="sxs-lookup"><span data-stu-id="1a759-122">The **Contrast Ratio** section of the Color Picker shows 2 check marks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="1a759-123">Para obter mais informações, selecione a seção **Taxa de contraste** para expandi-la.</span><span class="sxs-lookup"><span data-stu-id="1a759-123">For more information, select the **Contrast ratio** section to expand it.</span></span>  <span data-ttu-id="1a759-124">No se picker visual na parte superior do Selador de Cores, duas linhas aparecem, em execução no selador visual, juntamente com um círculo para a cor atual.</span><span class="sxs-lookup"><span data-stu-id="1a759-124">In the visual picker at the top of the Color Picker, two lines appear, running across the visual picker, along with a circle for the current color.</span></span>  <span data-ttu-id="1a759-125">Se a cor atual atender às recomendações, qualquer coisa do mesmo lado da linha também atende às recomendações.</span><span class="sxs-lookup"><span data-stu-id="1a759-125">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="1a759-126">Se a cor atual não atender às recomendações, qualquer coisa do mesmo lado também não atenderá às recomendações.</span><span class="sxs-lookup"><span data-stu-id="1a759-126">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  

    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="A Linha de Taxa de Contraste no selador visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="1a759-128">A **Linha de Taxa** de Contraste no selador visual</span><span class="sxs-lookup"><span data-stu-id="1a759-128">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  

1. <span data-ttu-id="1a759-129">Para experimentar cores diferentes, selecione dentro do seletor visual ou selecione uma amostra de cores na parte inferior do Seletor de Cores.</span><span class="sxs-lookup"><span data-stu-id="1a759-129">To try different colors, select within the visual picker, or select a color swatch at the bottom of the Color Picker.</span></span>
    

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1a759-130">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1a759-130">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="1a759-131">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1a759-131">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1a759-132">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="1a759-132">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1a759-134">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1a759-134">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->  
[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Nível AAA de contraste (aprimorado) | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Nível AA de contraste (mínimo) | W3C"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
