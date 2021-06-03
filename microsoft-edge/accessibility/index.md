---
description: Saiba como criar, projetar e testar sites acessíveis em Microsoft Edge.
title: Acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, borda, desenvolvimento da Web, ARIA, desenvolvedor, UIA, Automação da Interface do Usuário
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231398"
---
# Visão geral de acessibilidade  

> "\[T\]o impacto da deficiência é alterado radicalmente na Web porque a Web remove barreiras à comunicação e à interação que muitas pessoas enfrentam no mundo físico." [(Acessibilidade | W3C)][W3CAccessibility]  

A [Organização Mundial de][WHODisabilities] Saúde define a deficiência como "uma incompatibilidade na interação entre os recursos do corpo de uma pessoa e os recursos do ambiente em que ela mora".  As deficiências variam de deficiências de situação, como mobilidade limitada ao segurar um bebê ou luz do sol brilhante em um telefone, até outras deficiências físicas, auditivas, visuais ou relacionadas à idade.  

Projetar sites e outras tecnologias para inclusão cria uma experiência agradável para cada pessoa.  O design inclusivo e a acessibilidade da Web capacitam e ajudam a todos a usar a Web.  

Aqui estão algumas práticas recomendadas, exemplos de código e recursos adicionais para você saber mais sobre [Designing,][AccessibilityDesign] [Building][AccessibilityBuild]e [Testing][AccessibilityTest] accessible websites in Microsoft Edge.  

## Acessibilidade no Microsoft Edge  

Em Microsoft Edge, introduzimos a MODERNA API de Automação da [Interface do][WindowsWin32AutoEntryui] Usuário \(API UIA\).  A alteração para a UIA foi um grande investimento na acessibilidade do navegador e estabelece a base para uma experiência da Web mais inclusiva para usuários que dependem da tecnologia assistida no Windows 10.  Os usuários também se beneficiam da natureza cada vez maior do Chromium mecanismo.  

O sistema de acessibilidade no Microsoft Edge oferece suporte inerentemente a padrões web modernos, incluindo ARIA, HTML5 e CSS3.  O diagrama a seguir do pipeline de navegador simplificado segue o conteúdo da página da Web em uma camada de apresentação acessível.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="O conteúdo transformado no modelo de mecanismo é projetado em exibições visuais e de acessibilidade que são apresentadas como apresentação visual ou acessível":::
   O conteúdo transformado no modelo de mecanismo é projetado em exibições visuais e de acessibilidade que são apresentadas como apresentação visual ou acessível  
:::image-end:::  

A Microsoft Edge trabalha com o W3C e outros fornecedores de navegadores de forma contínua para garantir que os novos recursos da plataforma Web tenham acessibilidade interna suficiente.  

Para obter informações sobre quais novos recursos HTML5 têm suporte Microsoft Edge, navegue até [HTML5Accessibility][HTML5Accessibility].  

## Recursos  

#### Blog Windows automação da interface do usuário da Microsoft  

O [blog Windows automação da interface][ArchiveBlogsWinuiautomation] do usuário da Microsoft aborda tópicos relacionados à API Windows Automação.  

#### Iniciativa de Acessibilidade da Web (WAI)  

A [Iniciativa de Acessibilidade da Web (WAI)][W3CWaiHome] fornecida bt o W3C é um esforço para ajudar a melhorar a acessibilidade da Web.  O site fornece uma variedade de recursos para Introdução à Acessibilidade da [Web,][W3CWaiGettingstartedOverview] [Design para][W3CWaiFundamentals]Inclusão, tutoriais e [apresentações][W3CWaiTeachAdvocate]e muito mais.  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Criar sites acessíveis | Microsoft Doc"  
[AccessibilityDesign]: ./design.md "Criar sites acessíveis | Microsoft Doc"  
[AccessibilityTest]: ./test.md "Testes de acessibilidade | Microsoft Docs"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Interface do usuário | Microsoft Doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog Windows de Automação da Interface do Usuário da Microsoft | Microsoft Doc"  

[HTML5Accessibility]: https://html5accessibility.com "Acessibilidade HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Acessibilidade | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Introdução à | Iniciativa de Acessibilidade da Web (S) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Iniciando: tornando um site acessível | Iniciativa de Acessibilidade da Web (S) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Iniciativa de Acessibilidade da Web (S) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Visão geral do professor e do advogado | Iniciativa de Acessibilidade da Web (S) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Deficiências | OMS"  

