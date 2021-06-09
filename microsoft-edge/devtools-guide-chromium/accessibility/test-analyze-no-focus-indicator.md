---
description: Analisando a falta de indicação do foco do teclado em um menu de barra lateral, devido à falta de uma regra de pseudo-classe CSS para o estado de foco em um link, combinado com o link sem configuração de estrutura.
title: Analise a falta de indicação do foco do teclado em um menu de barra lateral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3626de9bdc2cce266efafe4b1b2e8fff501a74f7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597218"
---
# <a name="analyze-the-lack-of-indication-of-keyboard-focus-in-a-sidebar-menu"></a>Analise a falta de indicação do foco do teclado em um menu de barra lateral

<!-- Inspect tool, and CSS rules: pseudo-classes for states -->

Na página de demonstração de teste de acessibilidade, o menu de navegação da barra lateral com links azuis não indica visualmente qual link tem foco ao usar um teclado.  Para descobrir por que o menu de barra lateral é confuso para os usuários de teclado, procuraremos regras de pseudo-classe CSS para os estados e, juntamente com a propriedade CSS para estruturas de `hover` `focus` links.  

Esta análise descobre que a falta de indicação do foco do teclado nos links do menu de navegação da barra lateral é porque:
*  Os `a` links têm uma configuração de propriedade CSS de `outline: none` .
*  Os `a` links não têm uma regra de pseudo-classe CSS para o `:focus` estado.

Para navegar até o CSS, vamos usar a ferramenta **Inspecionar** para realçar um link azul no menu de navegação da barra lateral e, em seguida, exibir a árvore DOM e CSS para o elemento `a` que define esse link.

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Selecione o **botão Inspecionar** \( Inspecionar ícone \) no canto superior esquerdo do DevTools para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).

1.  Passe o mouse sobre o link **gatos** azuis no menu de navegação da barra lateral.  A sobreposição Inspecionar é exibida, mostrando que o elemento é focalizado `a` no teclado.  Mas a sobreposição não mostra que não há nenhuma indicação visual quando o link tem foco.

    Em seguida, inspecionaremos o estilo CSS deste link.
 
1.  Selecione o link **Gatos** no menu de navegação da barra lateral.  A **ferramenta Inspecionar** é desligada e a ferramenta **Elements** é aberta, realçando o nó na `a` árvore DOM.

1.  Selecione a **guia Estilos.**  A regra CSS `#sidebar nav li a` é exibida, juntamente com um link para um número de linha em `styles.css` .

    :::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspecionar o código-fonte e os estilos aplicados de um link no menu" lightbox="../media/a11y-testing-menu-link.msft.png":::
        Inspecionar o código-fonte e os estilos aplicados de um link no menu
    :::image-end:::
    
1.  Selecione o link para o arquivo CSS.  O arquivo CSS é aberto na **ferramenta Sources.**

    :::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Os estilos aplicados ao link na ferramenta Sources" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
        Os estilos aplicados ao link na ferramenta Sources
    :::image-end:::
    
Os estilos da página têm uma regra de pseudo-classe CSS para o estado que indica qual item de menu você está `hover` ao usar um mouse: `#sidebar nav li a:hover` .  No entanto, não há nenhuma regra de pseudo-classe CSS para o estado indicar visualmente qual item de menu você está usando ao usar `focus` um teclado, como `#sidebar nav li a:focus` .

Além disso, observe que os links têm uma configuração de propriedade CSS de `outline: none` .  Essa é uma prática comum, para remover o contorno que os navegadores adicionam automaticamente aos elementos quando você se concentra neles usando um teclado.  Não usar `focus` o estilo causa confusão para os usuários.


## <a name="see-also"></a>Consulte também 

*  [Acompanhar qual elemento tem o foco](focus.md)
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
