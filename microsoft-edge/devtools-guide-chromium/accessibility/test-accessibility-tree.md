---
description: Verificando a Árvore de Acessibilidade para suporte a teclado e leitor de tela.
title: Verifique o suporte ao leitor de tela e ao teclado na Árvore de Acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0ab5e5609485505d1ad5fa6e2fffced9af25edcb
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597219"
---
# <a name="check-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a>Verifique o suporte ao leitor de tela e ao teclado na Árvore de Acessibilidade

<!-- Accessibility tab: Accessibility Tree -->

Vários recursos do DevTools verificam se há suporte para teclado e leitor de tela.  Usar a **ferramenta Inspecionar** para verificar a acessibilidade de cada elemento de página individualmente pode se tornar muito demorado.  Uma maneira alternativa de verificar uma página da Web é usar a **Árvore de Acessibilidade**.  A **Árvore de Acessibilidade** indica quais informações a página fornece para tecnologias assistivas, como leitores de tela.

A **Árvore de** Acessibilidade é um subconjunto da árvore DOM, que contém elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página em um leitor de tela.  A **Árvore de Acessibilidade** está na guia **Acessibilidade** da ferramenta **Elements** (perto da **guia Estilos).**


Para explorar usando a Árvore de Acessibilidade com a página de demonstração:

1.  Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia.  Em seguida, **selecione F12** para abrir o DevTools.

1.  Selecione o **botão Inspecionar** \( o botão Inspecionar ícone \) no canto superior esquerdo do DevTools para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).

1.  Na página da Web renderizada, na seção **Doação,** passe o mouse sobre o botão **100.**  A **sobreposição da** ferramenta Inspect é exibida.

1.  Na página da Web renderizada, selecione o botão **100.**  No DevTools, a **ferramenta Elements** é exibida.  A árvore DOM mostra `div` o elemento do botão **100.**  O **painel Estilos** mostra as configurações CSS do elemento.

1.  À direita da guia **Estilos,** selecione **a** guia Acessibilidade.  A **Árvore de** Acessibilidade do elemento é exibida e expandida.

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Botão Formulário de doação na ferramenta Árvore de Acessibilidade" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    Botão Formulário de doação na ferramenta Árvore de Acessibilidade
:::image-end:::

Qualquer elemento na árvore que não tenha um nome ou que tenha uma função (como o elemento) é um problema, porque esse elemento não estará disponível para usuários de teclado ou para usuários que estão usando a tecnologia `generic` `div` assistida.


## <a name="see-also"></a>Consulte também

*  [Exibir a posição de um elemento na Árvore de Acessibilidade][DevtoolsAccessibilityAccessibilityTabViewTree]
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityAccessibilityTabViewTree]: accessibility-tab.md#view-the-position-of-an-element-in-the-accessibility-tree "Exibir a posição de um elemento na Árvore de Acessibilidade - Testar acessibilidade usando a guia Acessibilidade | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
