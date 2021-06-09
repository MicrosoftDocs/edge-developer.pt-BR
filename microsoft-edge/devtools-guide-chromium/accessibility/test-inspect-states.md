---
description: Inspecione a acessibilidade de todos os estados de elementos, como o contraste de texto durante o estado de foco, no painel Estilos usando o estado do elemento Toggle.
title: Verificar a acessibilidade de todos os estados de elementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 129a89f94925de24a4e649bd91f513de031d6b4a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597200"
---
# <a name="verify-accessibility-of-all-states-of-elements"></a>Verifique a acessibilidade de todos os estados dos elementos

<!-- 5. STYLES: TOGGLE STATE -->

Verifique a acessibilidade de todos os estados de elementos, como contraste de cor de texto durante o `hover` estado.  A **ferramenta Inspecionar** relata problemas de acessibilidade para um estado de cada vez.  Para verificar a acessibilidade dos vários estados de elementos, na guia **Estilos,** selecione **\:hov** ( Estado do Elemento**Toggle**), conforme descrito neste artigo. Primeiro mostramos por que a simulação de estado é necessária usando a ferramenta **Inspecionar** e, em seguida, mostramos como usar a simulação de estado.


## <a name="checking-text-color-contrast-in-the-default-state"></a>Verificando o contraste de cor do texto no estado padrão

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

Além dos testes automáticos de contraste de cor na ferramenta **Problemas,** você também pode usar a ferramenta **Inspecionar** para verificar se elementos de página individuais têm contraste suficiente.  Se as informações de contraste estão disponíveis, a sobreposição **Inspecionar** mostra a taxa de contraste e um item de caixa de seleção.  Um ícone de marca de verificação verde indica que há contraste suficiente e um ícone de alerta amarelo indica que não há contraste suficiente.

Por exemplo, os links no menu de navegação da barra lateral têm contraste suficiente.  Mas o item de lista **de** Cachorros verdes na seção **Status** da Doação não tem contraste suficiente e, portanto, é sinalizado por um aviso na sobreposição **Inspecionar.**

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Os links no menu de navegação da barra lateral têm contraste suficiente, conforme mostrado na sobreposição Inspecionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            Os links no menu de navegação da barra lateral têm contraste suficiente, conforme mostrado na sobreposição **Inspecionar** :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Um elemento que não tem contraste suficiente é sinalizado por um aviso na sobreposição Inspecionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            Um elemento que não tem contraste suficiente é sinalizado por um aviso na sobreposição **Inspecionar** :::image-end:::
    :::column-end:::
:::row-end:::
        

## <a name="hovering-when-the-inspect-tool-is-active-doesnt-show-the-text-color-contrast-for-the-hover-state"></a>O foco quando a ferramenta Inspect está ativa não mostra o contraste de cor de texto para o estado de foco

A **sobreposição** de informações da ferramenta Inspect representa apenas um único estado.  Os elementos na página podem ter estados diferentes, todos eles precisam ser testados.  Por exemplo, quando você passar o ponteiro do mouse sobre o menu da página de demonstração de teste de acessibilidade, você obterá uma animação que altera as cores. Execute as etapas a seguir.

1.  Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia.

1.  Passe o mouse sobre os itens de menu azul no menu de navegação da barra lateral.  Observe que cada item tem uma animação.

    :::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="O item de menu mostrando cores diferentes quando o ponteiro do mouse está sobre ele" lightbox="../media/a11y-testing-hover.msft.png":::
        O item de menu mostrando cores diferentes quando o ponteiro do mouse está sobre ele
    :::image-end:::
    
Agora, use a ferramenta Inspecionar. Quando a ferramenta Inspect é usada, as animações nos itens de menu não são executados quando você passar o mouse sobre eles.  Ao usar a ferramenta Inspecionar, você não pode alcançar o estado nos itens de menu para testar a taxa de contraste, pois o estado em seus estilos não `hover` `hover` é disparado.  
    
Para confirmar se suas animações não são executados, execute as etapas a seguir.
    
1.  Selecione o **botão Inspecionar** \( o botão Inspecionar \) no canto superior esquerdo do DevTools para que o ícone seja ![ realçado ](../media/inspect-icon.msft.png) (azul).

1.  Passe o mouse sobre os links azuis no menu de navegação da barra lateral.  As animações dos itens de menu não são executados. Em vez disso, os itens de menu são exibidos usando cores e realçadores para a sobreposição da caixa de flexão.

Verificar o contraste de texto suficiente dessa forma não é suficiente, pois os elementos na página podem ter estados diferentes.


## <a name="use-state-simulation-to-simulate-the-hover-state-of-an-animated-menu-item"></a>Usar a simulação de estado para simular o estado de foco de um item de menu animado 

<!-- Elements tool: Styles pane: Toggle Element State -->

Quando a **ferramenta Inspect** estiver ativa, em vez de passar o mouse sobre um elemento animado, você precisará simular o estado do item de menu.  Para simular o estado de um item de menu, use a simulação de estado no painel **Estilos.**  O **painel Estilos** tem um botão **\:hov** ( Estado do Elemento**Toggle**), que exibe um grupo de caixas de seleção rotuladas estado do elemento **Force**.

Para ativar o estado de foco ao usar a ferramenta Inspecionar:

1.  Se ainda não estiver aberto, abra a página da [Web][DevToolsA11yErrorsDemopage] de demonstração de teste de acessibilidade em uma nova guia.  Em seguida, **selecione F12** para abrir o DevTools.

1.  Selecione o **botão Inspecionar** \( Inspecionar botão da ferramenta \) no canto superior esquerdo do DevTools para que o ícone seja ![ realçado ](../media/inspect-icon.msft.png) (azul).

1.  Na página da Web renderizada, selecione o link **azul Gatos** no menu de navegação da barra lateral.  A **ferramenta Elements** é aberta, com o elemento `<a href="#cats">Cats</a>` selecionado.

    :::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspecionar o elemento que tem um estado de foco na ferramenta Elements" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
        Inspecionar o elemento que tem um estado de foco na ferramenta Elements
    :::image-end:::

1.  Selecione a **guia Estilos.**  O elemento selecionado tem um estado no CSS que é aplicado a ele, mas que não `a` está visível no painel `hover` **Estilos.** 

1.  No painel **Estilos,** à direita da regra de `#sidebar nav li a` estilo, selecione o `styles.css` link.  A **ferramenta Sources** é aberta.  Em seguida, encontre a regra de pseudo-classe CSS `#sidebar nav li a:hover` .  Essa regra não é executado quando a **ferramenta Inspect** está ativa.  Vamos simular a execução dessa regra de estado nas próximas etapas.

1.  Selecione a **ferramenta Elementos.**  Em seguida, no painel **Estilos,** selecione o **botão :hov** (**Estado do Elemento De alternância**).  O **grupo de estado do** elemento Force das caixas de seleção é exibido.

    :::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="A ferramenta de simulação de estado mostrando todas as opções" lightbox="../media/a11y-testing-state-simulation.msft.png":::
        A ferramenta de simulação de estado mostrando todas as opções
    :::image-end:::

1.  Selecione a **caixa de seleção :hover.**  No DOM, à esquerda do elemento , aparece um ponto amarelo, indicando que o `<a href="#cats">Cats</a>` elemento tem um estado simulado.  O **** item de menu Gatos agora aparece na página da Web como se o ponteiro estivesse pairando sobre ele.  A animação no item de menu pode ser executado.

    :::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulando um estado de foco" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
        DevTools simulando um estado de foco
    :::image-end:::

    Depois que o estado simulado for aplicado, você poderá usar a ferramenta **Inspecionar** novamente para verificar o contraste do elemento quando o usuário passar o mouse sobre ele, da seguinte forma.

1.  Selecione o **botão Inspecionar** \( Ícone do Inspetor \) no canto superior esquerdo do DevTools para que o ícone seja ![ realçado ](../media/inspect-icon.msft.png) (azul).

1.  Passe o mouse sobre o link **gatos** azuis no menu de navegação da barra lateral.  O link agora está azul claro, devido à animação de foco simulado.  A **sobreposição** de informações da ferramenta Inspect é exibida, mostrando um ponto de exclamação laranja na linha **Contraste,** indicando que o contraste não é alto o suficiente.

    :::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Testar o contraste de um elemento em um estado de foco simulado" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
        Testar o contraste de um elemento em um estado de foco simulado
    :::image-end:::

A simulação de estado também é uma boa maneira de verificar se você considera diferentes necessidades do usuário, como as necessidades dos usuários de teclado.  Usando as caixas de seleção estado do elemento **Force,** você pode simular o estado para descobrir que a interface do usuário permanece inalterada `:focus` quando ela tem foco. Essa falta de um indicador quando um elemento tem foco é um problema.


## <a name="see-also"></a>Consulte também

*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
