---
ms.assetid: ffd1bc60-2ef1-4f11-8156-b63544cede77
description: Saiba como Microsoft Edge pode reconhecer as informações do ARIA e, em seguida, expô-la a tecnologias assistivas que podem, em seguida, usar APIs de Automação da Interface do Usuário da Microsoft.
title: Acessibilidade - Automação de interface do usuário e ARIA
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, borda, desenvolvimento da Web, ARIA, desenvolvedor, UIA, Automação da Interface do Usuário
ms.custom: seodec18
ms.openlocfilehash: 2fcc8160c830b5a62d8023a5cb7cc9df376c49ca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560541"
---
# Automação de interface do usuário e ARIA no Microsoft Edge

O W3C define a ARIA (Accessible Rich Internet Applications) como uma sintaxe para tornar o conteúdo da Web dinâmico e a interface do usuário personalizada acessível. Microsoft Edge reconhece as informações de função, estado e propriedade do ARIA e as expõe a tecnologias assistivas, que, por sua vez, podem usar as APIs de Automação da Interface do Usuário da [Microsoft](https://blogs.msdn.microsoft.com/winuiautomation/) para recuperar as informações.

Visite [HTML5Accessibility para](https://html5accessibility.com) obter informações sobre quais novos recursos HTML5 têm suporte Microsoft Edge.

O Microsoft Edge de renderização (EdgeHTML) cria uma projeção acessível de páginas da Web, de acordo com as seguintes especificações W3C:

1. A [especificação Mapeamentos de API](https://w3.org/TR/html-aam-1.0/) de Acessibilidade HTML define como elementos HTML e atributos são mapeados para objetos ARIA e automação da interface do usuário.
   * [Rascunho de trabalho](https://w3.org/TR/html-aam-1.0/) - versão estável da especificação
   * [Rascunho do editor](https://w3c.github.io/html-aam/) - trabalho em andamento. Observe que, embora essa especificação tenha as alterações mais recentes, as alterações podem não estar disponíveis no Microsoft Edge ainda.


2. A [especificação Core Accessibility API Mappings](https://w3.org/TR/core-aam-1.1/) define princípios gerais para a criação da árvore de acessibilidade e o mapeamento de elementos e atributos do ARIA para objetos de Automação da Interface do Usuário.
   * [Rascunho de trabalho](https://w3.org/TR/core-aam-1.1/) - versão estável da especificação
   * [Rascunho do editor](https://w3c.github.io/core-aam/) - trabalho em andamento. Observe que, embora essa especificação tenha as alterações mais recentes, as alterações podem não estar disponíveis no Microsoft Edge ainda.  

3. A especificação Nome Acessível e [Descrição: Mapeamentos](https://w3.org/TR/accname-aam-1.1/) de Computação e API define como calcular o nome e a descrição de objetos acessíveis, considerando os valores HTML e os elementos e atributos do ARIA disponíveis para os elementos acessíveis.
   * [Rascunho de trabalho](https://w3.org/TR/accname-aam-1.1/) - versão estável da especificação  
   * [Rascunho do editor](https://w3c.github.io/accname/) - trabalho em andamento. Observe que, embora essa especificação tenha as alterações mais recentes, as alterações podem não estar disponíveis no Microsoft Edge ainda.   

Para obter mais informações sobre a arquitetura de acessibilidade Microsoft Edge, confira a postagem do blog [Criando uma plataforma Web mais](https://blogs.windows.com/msedgedev/2016/04/20/building-a-more-accessible-web-platform/) acessível.  Por exemplos de como a nova arquitetura melhora a experiência do usuário final e, especificamente, como a marcação define a experiência de navegar com tecnologias auxiliares, como leitores de tela, visite Criando uma experiência de usuário mais acessível com HTML5 e [UIA](https://blogs.windows.com/msedgedev/2016/05/12/accessible-ux-with-html5-and-uia/).
