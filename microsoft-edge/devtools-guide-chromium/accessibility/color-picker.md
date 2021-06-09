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
# <a name="test-text-color-contrast-using-the-color-picker"></a>Teste o contraste da cor do texto usando o Seletor de Cor

Pessoas com baixa visão podem não ver áreas muito claras ou muito escuras.  Tudo tende a aparecer no mesmo nível de brilho, o que dificulta a distinção de contornos e bordas.  

A taxa de contraste mede a diferença no brilho entre o primeiro plano e o plano de fundo do texto.  Se o texto tiver uma taxa de contraste baixa, as pessoas com baixa visão poderão experimentar seu site como uma tela em branco.  

No DevTools, uma maneira de exibir a taxa de contraste de um elemento de texto é usar o Selador de Cores, na guia **Estilos.**  O Selador de Cores ajuda você a verificar se seu texto atende aos níveis de taxa de contraste recomendados.

**Para verificar o contraste de cor de texto usando o Se picker de cores:**

1.  Em DevTools, selecione a **ferramenta Elements.**  
1.  Na Árvore **DOM,** selecione o elemento de texto que você deseja inspecionar.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecionar um parágrafo na árvore DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Inspecionar um parágrafo na árvore **DOM**  
    :::image-end:::  
    
1.  Na guia **Estilos,** localize a propriedade **color** aplicada ao elemento e selecione o quadrado de cores ao lado da **propriedade color.**
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="A propriedade color do elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       A `color` propriedade do elemento  
    :::image-end:::  
    
1.  Examine a **seção Taxa** de Contraste do Selador de Cores.  Uma marca de verificação significa que o elemento atende à [recomendação mínima][W3CContrastMinimum].  Duas marcas de verificação significam que ela atende [à recomendação aprimorada][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="A seção Taxa de Contraste do Selador de Cores mostra 2 marcas de verificação e um valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       A **seção Taxa de** Contraste do Selador de Cores mostra 2 marcas de verificação e um valor de `13.97`  
    :::image-end:::  
    
1.  Para obter mais informações, selecione a seção **Taxa de contraste** para expandi-la.  No se picker visual na parte superior do Selador de Cores, duas linhas aparecem, em execução no selador visual, juntamente com um círculo para a cor atual.  Se a cor atual atender às recomendações, qualquer coisa do mesmo lado da linha também atende às recomendações.  Se a cor atual não atender às recomendações, qualquer coisa do mesmo lado também não atenderá às recomendações.  

    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="A Linha de Taxa de Contraste no selador visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       A **Linha de Taxa** de Contraste no selador visual  
    :::image-end:::  

1. Para experimentar cores diferentes, selecione dentro do seletor visual ou selecione uma amostra de cores na parte inferior do Seletor de Cores.
    

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  


<!-- links -->  
[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Nível AAA de contraste (aprimorado) | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Nível AA de contraste (mínimo) | W3C"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
