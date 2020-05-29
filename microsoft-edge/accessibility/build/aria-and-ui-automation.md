---
ms.assetid: ffd1bc60-2ef1-4f11-8156-b63544cede77
description: Saiba como o Microsoft Edge pode reconhecer informações do ARIA e, em seguida, expô-lo a tecnologias adaptativas que podem usar APIs de automação da interface do usuário da Microsoft.
title: Acessibilidade-automação do ARIA e da interface do usuário
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, Edge, desenvolvimento da Web, ARIA, desenvolvedor, UIA, automação da interface do usuário
ms.custom: seodec18
ms.openlocfilehash: 2fcc8160c830b5a62d8023a5cb7cc9df376c49ca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560541"
---
# Automação do ARIA e da interface do usuário no Microsoft Edge

O W3C define o aplicativo Internet (ARIA) acessível como uma sintaxe para tornar o conteúdo dinâmico da Web e a interface do usuário personalizada acessíveis. O Microsoft Edge reconhece as informações de função, estado e Propriedade do ARIA e a expõe a tecnologias adaptativas, que, por sua vez, podem usar as APIs de [automação da interface do usuário da Microsoft](https://blogs.msdn.microsoft.com/winuiautomation/) para recuperar as informações.

Acesse [HTML5Accessibility](https://html5accessibility.com) para obter informações sobre quais novos recursos do HTML5 são accessibly suportados pelo Microsoft Edge.

O mecanismo de renderização do Microsoft Edge (EdgeHTML) cria uma projeção acessível de páginas da Web, de acordo com as seguintes especificações do W3C:

1. A especificação de [mapeamentos de API de acessibilidade HTML](https://w3.org/TR/html-aam-1.0/) define como elementos HTML e atributos mapeiam para objetos de automação do Aria e da interface do usuário.
   * [Rascunho funcional](https://w3.org/TR/html-aam-1.0/) – versão estável da especificação
   * [Rascunho do editor](https://w3c.github.io/html-aam/) -trabalho em andamento. Observe que, enquanto essa especificação tem as alterações mais recentes, as alterações podem não estar disponíveis no Microsoft Edge ainda.


2. A especificação de [mapeamentos de API de acessibilidade principais](https://w3.org/TR/core-aam-1.1/) define princípios gerais para construir a árvore de acessibilidade e o mapeamento de elementos e atributos do Aria para objetos de automação da interface do usuário.
   * [Rascunho funcional](https://w3.org/TR/core-aam-1.1/) – versão estável da especificação
   * [Rascunho do editor](https://w3c.github.io/core-aam/) -trabalho em andamento. Observe que, enquanto essa especificação tem as alterações mais recentes, as alterações podem não estar disponíveis no Microsoft Edge ainda.  

3. O [nome acessível e a descrição:](https://w3.org/TR/accname-aam-1.1/) a especificação de mapeamentos de API define como calcular o nome e a descrição dos objetos acessíveis, dados de elementos HTML e do Aria e os valores de atributos disponíveis para os elementos acessíveis.
   * [Rascunho funcional](https://w3.org/TR/accname-aam-1.1/) – versão estável da especificação  
   * [Rascunho do editor](https://w3c.github.io/accname/) -trabalho em andamento. Observe que, enquanto essa especificação tem as alterações mais recentes, as alterações podem não estar disponíveis no Microsoft Edge ainda.   

Para obter mais informações sobre a arquitetura de acessibilidade no Microsoft Edge, confira a postagem do blog [criando uma plataforma Web mais acessível](https://blogs.windows.com/msedgedev/2016/04/20/building-a-more-accessible-web-platform/) .  Para obter exemplos de como a nova arquitetura melhora a experiência do usuário final e como a marcação define a experiência de navegação com tecnologias assistenciais, como leitores de tela, acesse [criando uma experiência do usuário mais acessível com HTML5 e UIA](https://blogs.windows.com/msedgedev/2016/05/12/accessible-ux-with-html5-and-uia/).
