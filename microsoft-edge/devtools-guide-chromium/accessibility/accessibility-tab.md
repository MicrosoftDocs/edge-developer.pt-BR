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
# <a name="test-accessibility-using-the-accessibility-tab"></a>Teste a acessibilidade usando a guia de Acessibilidade

A **guia Acessibilidade** é onde você visualiza a árvore de acessibilidade, os atributos do ARIA e as propriedades de acessibilidade calculadas dos nós DOM.  

Para abrir a **guia Acessibilidade:**

1.  Selecione a **ferramenta Elementos.**  
1.  Na Árvore **DOM,** selecione o elemento que você deseja inspecionar.  
1.  Selecione a **guia Acessibilidade.**  Talvez seja necessário selecionar primeiro o botão Mais **guias** \( o botão Mais guias \) à ![ direita da guia ](../media/more-tabs-icon.msft.png) **Estilos.**

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecione o elemento h1 da homepage DevTools na guia Acessibilidade" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   `h1`Inspecione o elemento da homepage DevTools na guia **Acessibilidade**
:::image-end:::  


## <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Exibir a posição de um elemento na Árvore de Acessibilidade

A [árvore de acessibilidade][MDNAccessibilityTree] é um subconjunto da árvore DOM.  A árvore de acessibilidade contém apenas elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página por meio de tecnologias assistivas, como leitores de tela.

Inspecione a posição de um elemento na árvore de acessibilidade da **guia** Acessibilidade.  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="A seção Árvore de Acessibilidade" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   A **seção Árvore de** Acessibilidade  
:::image-end:::  


## <a name="view-the-aria-attributes-of-an-element"></a>Exibir os atributos ARIA de um elemento  

Os atributos do ARIA garantem que tecnologias assistivas, como leitores de tela, tenham todas as informações necessárias para representar corretamente o conteúdo de uma página.  

Exibir os atributos ARIA de um elemento na **guia Acessibilidade.**

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="A seção Atributos do ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   A **seção Atributos do ARIA**  
:::image-end:::  


## <a name="view-the-computed-accessibility-properties-of-an-element"></a>Exibir as propriedades de acessibilidade calculadas de um elemento  


Algumas propriedades de acessibilidade são calculadas dinamicamente pelo navegador.  Essas propriedades são exibidas na seção **Propriedades Computadas** da guia **Acessibilidade.**  

Exibir as propriedades de acessibilidade calculadas de um elemento na guia **Acessibilidade.**

> [!NOTE]
> Para propriedades CSS calculadas, use a [guia Computed.][DevtoolsCssReferenceViewActuallyAppliedElements]

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="A seção Propriedades Computadas da guia Acessibilidade" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   A **seção Propriedades Computadas** da guia **Acessibilidade**  
:::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  


<!-- links -->
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Exibir apenas o CSS que é realmente aplicado a um elemento - Referência CSS | Microsoft Docs"  
[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árvore de acessibilidade (AOM) | MDN"  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
