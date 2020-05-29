---
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
description: Saiba como criar, projetar e testar sites acessíveis dentro do Microsoft Edge.
title: Acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, Edge, desenvolvimento da Web, ARIA, desenvolvedor, UIA, automação da interface do usuário
ms.openlocfilehash: 6ad95e9c250aa6a4a61ca09470cea86efd715427
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583102"
---
# Acessibilidade  

> "\ [T \], o impacto da deficiência é alterado radicalmente na Web porque a Web remove barreiras à comunicação e à interação que muitas pessoas enfrentam no mundo físico." [(Acessibilidade | W3C][W3CAccessibility]  

A [organização de saúde do mundo][WHODisabilities] define a deficiência como "uma incompatibilidade entre os recursos do corpo de uma pessoa e os recursos do ambiente em que elas residem".  As desabilidades vão desde as desabilidades de situação, como mobilidade limitada enquanto mantém um bebê ou um sol brilhante em um telefone, a outros problemas físicos, auditivos, visuais ou relacionados à idade.  

A criação de sites e outras tecnologias para inclusão cria uma experiência agradável para cada pessoa.  O design inclusivo e a acessibilidade na Web capacitam e auxiliam todos a usar a Web.  

Veja a seguir algumas práticas recomendadas, exemplos de código e outros recursos para obter mais informações sobre como [projetar][AccessibilityDesign], [criar][AccessibilityBuild]e [testar][AccessibilityTest] sites acessíveis no Microsoft Edge.  

## Acessibilidade no Microsoft Edge  

No Microsoft Edge, introduzimos a [API de automação da interface do usuário][WindowsWin32AutoEntryui] moderna \ (UIA API \).  A mudança para UIA foi um grande investimento em acessibilidade do navegador, e ele prepara a base para uma experiência da Web mais inclusiva para os usuários que dependem da tecnologia assistencial no Windows 10.  Os usuários também se beneficiam da natureza verde do mecanismo Chromium.  

O sistema de acessibilidade no Microsoft Edge oferece suporte inerentemente a padrões da Web modernos, incluindo ARIA, HTML5 e CSS3.  O diagrama a seguir do pipeline simplificado de navegador segue o conteúdo da página da Web em uma camada de apresentação acessível.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="O conteúdo transformado para o modelo de mecanismo é projetado em modos de exibição visuais e de acessibilidade apresentados como uma apresentação visual ou acessível":::
   Figura 1.  O conteúdo transformado para o modelo de mecanismo é projetado em modos de exibição visuais e de acessibilidade apresentados como uma apresentação visual ou acessível
:::image-end:::

<!--![Figure 1.  Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation][ImageAccessibilityArchitecture]  -->  

A equipe do Microsoft Edge trabalha com o W3C e outros fornecedores de navegador continuamente para garantir que os novos recursos da plataforma da Web tenham acessibilidade interna suficiente.  

Para obter informações sobre quais novos recursos do HTML5 são accessibly suportados pelo Microsoft Edge, acesse [HTML5Accessibility][HTML5Accessibility].  

## Recursos  

#### Blog de automação da interface do usuário do Microsoft Windows  

O [blog de automação da interface do usuário do Microsoft Windows][ArchiveBlogsWinuiautomation] aborda tópicos relacionados à API de automação do Windows.  

#### Iniciativa de acessibilidade da Web (WAI)  

A [iniciativa de acessibilidade da Web (WAI)][W3CWaiHome] oferecida BT o W3C é um esforço para ajudar a melhorar a acessibilidade da Web.  O site fornece uma variedade de recursos para [introdução à acessibilidade da Web][W3CWaiGettingstartedOverview], [design para inclusão][W3CWaiFundamentals], [tutoriais e apresentações][W3CWaiTeachAdvocate]e muito mais.  


<!-- image links -->  

<!--[ImageAccessibilityArchitecture]: ./media/accessibilityarchitecture.png "Figure 1: Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation"  -->  

<!-- links -->  

[AccessibilityBuild]: ./accessibility/build.md "Criando sites acessíveis"  
[AccessibilityDesign]: ./accessibility/design.md "Criando sites acessíveis"  
[AccessibilityTest]: ./accessibility/test.md "Testes de acessibilidade"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Automação da interface do usuário"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog de automação da interface do usuário do Microsoft Windows"  

[HTML5Accessibility]: https://html5accessibility.com "Acessibilidade do HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Acessibilidade | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Introdução à acessibilidade na Web | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Introdução: tornar um site acessível | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Visão geral de ensinar e defensor | Web Accessibility Initiative (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Recursos | QUE"  

