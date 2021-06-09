---
description: Use a ferramenta Inspecionar para detectar problemas de acessibilidade pairando sobre a página da Web.
title: Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c95116d38e5b0bda88af43ef8bfde4204b8cb372
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597174"
---
# <a name="use-the-inspect-tool-to-detect-accessibility-issues-by-hovering-over-the-webpage"></a>Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web

A **ferramenta Inspecionar** exibe informações sobre elementos individuais à medida que você passar o mouse sobre a página da Web renderizada, incluindo informações de acessibilidade.
Por outro lado, **a ferramenta Issues** relata automaticamente problemas para toda a página da Web.

O **botão Inspecionar** ferramenta \( Inspect ![ ](../media/inspect-icon.msft.png) \) está no canto superior esquerdo do DevTools.  Quando você seleciona o **botão Inspecionar** ferramenta, o botão fica azul, indicando que a **ferramenta Inspecionar** está ativa.

Quando a **ferramenta Inspect** está ativa, passar o mouse sobre qualquer elemento na página da Web renderizada exibe a **sobreposição Inspecionar.** Essa sobreposição exibe informações gerais e informações de acessibilidade sobre esse elemento.  A **seção Acessibilidade** da sobreposição **Inspecionar** exibe informações sobre contraste de cor de texto, texto do leitor de tela e suporte ao teclado.

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="A ferramenta Inspecionar, mostrando a área do elemento como uma sobreposição multicolor, e mostrando os detalhes do elemento como uma grande sobreposição de informações" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    A **ferramenta Inspecionar,** mostrando a área do elemento como uma sobreposição multicolor, e mostrando os detalhes do elemento como uma grande sobreposição de informações
:::image-end:::


## <a name="check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a>Verifique elementos individuais para contraste de texto, texto do leitor de tela e suporte ao teclado

<!-- Inspect tool: Accessibility section of overlay -->

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Selecione o **botão Inspecionar** \( Inspecionar \) no canto superior esquerdo do DevTools para que o ícone seja ![ ](../media/inspect-icon.msft.png) realçado (azul).

    :::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Para ativar a ferramenta Inspecionar, selecione o botão Inspecionar" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
        Para ativar a ferramenta **Inspecionar,** selecione o **botão Inspecionar**
    :::image-end:::

1.  Passe o mouse sobre qualquer elemento na página da Web de demonstração renderizada.  A **ferramenta Inspecionar** mostra uma sobreposição de informações abaixo do elemento na página da Web renderizada.

    :::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="A ferramenta Inspecionar, mostrando o layout do elemento como uma sobreposição multicolor, e mostrando os detalhes do elemento como uma grande sobreposição de informações" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
        A **ferramenta Inspecionar,** mostrando o layout do elemento como uma sobreposição multicolor, e mostrando os detalhes do elemento como uma grande sobreposição de informações
    :::image-end:::

A parte inferior da sobreposição **Inspecionar** tem uma seção **Accessibility** que contém as seguintes informações:

*   **Contraste** define se um elemento pode ser compreendido por pessoas com baixa visão.  A [taxa de][W3CContrastRatio] contraste, conforme definido pelas Diretrizes do [WCAG,][WCAG] indica se há contraste suficiente (um ícone de marca de verificação verde) ou não suficiente (um ícone de ponto de exclamação laranja).

*   **Nome** e **função** são quais tecnologias assistivas, como leitores de tela, relatarão sobre o elemento.
    *   O **Nome** é o conteúdo de texto de um `a` elemento.  Para o elemento `<a href="/">About Us</a>` , **o nome** mostrado na ferramenta Inspecionar é "Sobre nós".
    *   A **função** do elemento.  Geralmente, esse é o nome do elemento, como `article` `img` , , ou `link` `heading` .  Os `div` elementos e são chamados de `span` `generic` .

*   **O foco no teclado** indica se os usuários podem alcançar o elemento independentemente do dispositivo de entrada.
    *   Um ícone de marca de verificação verde indica que o elemento é focalizado no teclado.
    *   Um círculo cinza com linha diagonal indica que o elemento não é focalizado no teclado.


## <a name="additional-information-in-the-inspect-overlay"></a>Informações adicionais na sobreposição Inspecionar

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

A parte superior da sobreposição **Inspecionar,** que está acima da seção **Acessibilidade,** lista os seguintes detalhes do elemento.

*   Tipo de layout. Se o elemento estiver posicionado usando uma caixa de flexão ou grade, um ícone \(![Ícone de layout de grade](../media/grid-icon.msft.png)\) é exibido.
*   Nome do elemento, como `h1` , `h2` ou `div` .
*   As dimensões do elemento em pixels.
*   A cor como uma amostra de cores (ou um quadrado pequeno e colorido) e como uma cadeia de caracteres (como `#336699` ).
*   Informações de fonte, como famílias de tamanho e fonte.
*   Margem e preenchimento em pixels.


## <a name="identify-nested-regions-using-color-highlighting"></a>Identificar regiões aninhadas usando realçamento de cores 

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

Além da sobreposição de informações, a ferramenta **Inspect** também fornece coloração de região semelhante ao passar o mouse na árvore DOM na ferramenta **Elements.**

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Selecione o **botão Inspecionar** \( Inspecionar ícone da ferramenta \) no canto superior esquerdo do DevTools, para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).

1.  Passe o mouse sobre diferentes partes da página da web de demonstração renderizada.  Cada elemento na página da Web agora é exibido com uma sobreposição multicolor. Essa sobreposição multicolor pode exibir regiões aninhadas dentro de um elemento. Por exemplo, passe o mouse sobre a margem esquerda de **Gatos**.  A **ferramenta Inspect** realça várias partes retangulares da seção **Gatos** com cores diferentes, mostrando o layout que resulta das definições de flexbox CSS em sua página da Web.

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Sobreposição de flexbox multicolor e sobreposição de informações ao usar a ferramenta Inspecionar" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    Sobreposição de flexbox multicolor e sobreposição de informações ao usar a **ferramenta Inspecionar**
:::image-end:::

Para configurar a sobreposição de grade ou sobreposição de área flexível, na **ferramenta Elementos,** selecione a **guia Layout.**  Para obter mais informações, navegue até [Inspecionar Grade CSS](..\css\grid.md).


## <a name="use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a>Use a ferramenta Inspecionar para passar o mouse sobre a página da Web para realçar o DOM e CSS

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Selecione o **botão Inspecionar** \( a ferramenta Inspecionar \) no canto superior esquerdo do DevTools, para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).

1.  Selecione a **ferramenta Elementos.**

1.  Com a **ferramenta Inspecionar** ativa, passe o mouse sobre diferentes partes da página da Web renderizada.  Na ferramenta **Elementos,** a árvore DOM HTML se expande automaticamente para mostrar informações sobre o elemento sobre o que você passar o mouse.  O foco não faz com que o painel **Estilos** seja atualizado.

1.  Agora selecione qualquer elemento na página da Web renderizada.  A **ferramenta Elements** abre e exibe automaticamente o HTML do elemento na árvore DOM. A ferramenta também exibe o CSS aplicado no elemento no painel **Estilos.**  Selecionar um elemento na página da Web renderizada desliga a **ferramenta Inspecionar.**

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Detalhes sobre o elemento selecionado são exibidos na ferramenta Elements" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    Detalhes sobre o elemento selecionado são exibidos na **ferramenta Elements**
:::image-end:::

Depois de selecionar um elemento na página **** renderizada, você pode usar a **** guia Acessibilidade (perto da guia **Estilos)** para exibir a Árvore de Acessibilidade e usar o Visualizador de Ordem de **Origem**.


## <a name="see-also"></a>Consulte também

*  [Inspecionar um nó](../dom/index.md#inspect-a-node)
*  [Verifique o contraste de cor de texto no estado padrão usando a ferramenta Inspecionar](test-inspect-text-contrast.md)
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "taxa de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Diretrizes de acessibilidade de conteúdo da Web | W3C"
