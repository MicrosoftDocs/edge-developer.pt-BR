---
description: Verifique o contraste de cor do texto no estado padrão usando a sobreposição de informações da ferramenta Inspecionar na página, que tem uma seção Acessibilidade que inclui informações de contraste.
title: Verifique o contraste de cor de texto no estado padrão usando a ferramenta Inspecionar
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ade9fd6d685f6f7cea6311b1645a527ece352a38
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597170"
---
# <a name="check-text-color-contrast-in-the-default-state-using-the-inspect-tool"></a>Verifique o contraste de cor de texto no estado padrão usando a ferramenta Inspecionar

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

Verifique o contraste de cor do texto no estado padrão usando a **ferramenta Inspecionar.**  A **sobreposição** de informações da ferramenta Inspect na página da Web tem uma seção **Accessibility** que inclui informações **de contraste.**

Para verificar o contraste de cor de texto no estado padrão usando a sobreposição de informações da ferramenta Inspect, execute as etapas a seguir.

<!-- Inspect tool -->
Para elementos com texto, a sobreposição de informações da ferramenta **Inspect** mostra o seguinte:
*  A taxa de contraste entre cores de texto e plano de fundo.
*  Um ícone de marca de verificação verde para elementos com contraste suficiente.
*  Um ícone de alerta amarelo para elementos que não têm contraste suficiente.

Em alguns casos, o contraste é afetado pela configuração do navegador como tema claro ou tema escuro.

Como exemplo, na página de demonstração, os links azuis do menu de navegação da barra lateral têm contraste suficiente, mas o link verde **Cachorros** na seção **Status** de Doação não tem contraste suficiente.  Examine esses elementos usando **a ferramenta Inspecionar,** da seguinte forma:

1.  Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia.  Em seguida, **selecione F12** para abrir o DevTools.

1.  Selecione o **botão Inspecionar** \( Inspecionar botão \) no canto superior esquerdo do DevTools para que o ícone seja ![ realçado ](../media/inspect-icon.msft.png) (azul).

1.  Na página da Web renderizada, passe o mouse sobre o link **azul Gatos** do menu de navegação da barra lateral.  A **sobreposição** de informações da ferramenta Inspect é exibida.  Na seção **Acessibilidade da** sobreposição de informações, uma marca de seleção verde é exibida na linha **Contraste,** indicando que esse elemento tem contraste suficiente da cor do texto em relação à cor do plano de fundo.

    :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Os itens de menu têm contraste suficiente, conforme mostrado na ferramenta Inspecionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
        Os itens de menu têm contraste suficiente, conforme mostrado na ferramenta Inspecionar
    :::image-end:::

1.  Na página da Web renderizada, na seção Status da **Doação,** passe o mouse sobre o link **Cachorros.**  A **sobreposição** de informações da ferramenta Inspect mostra um ponto de exclamação laranja na linha **Contraste,** indicando que esse elemento não tem contraste suficiente de texto versus cores de plano de fundo.

    :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Um elemento que não tem contraste suficiente, conforme mostrado pelo aviso na ferramenta Inspecionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
        Um elemento que não tem contraste suficiente, conforme mostrado pelo aviso na ferramenta Inspecionar
    :::image-end:::


## <a name="different-options-to-inspect-text-color-contrast-in-devtools"></a>Opções diferentes para inspecionar o contraste de cor de texto no DevTools

Use os seguintes recursos de DevTools para inspecionar o contraste de cor de texto.

*  Use a **ferramenta Inspecionar** (como uma sobreposição de informações na página da Web) para verificar se um elemento de página individual tem contraste de cor de texto suficiente.  A **sobreposição** de informações da ferramenta Inspect inclui uma seção **Accessibility** que tem uma linha **de informações Contraste.**  A **ferramenta Inspect** mostra apenas informações de contraste de texto para o estado atual.  Essa abordagem é descrita no artigo atual.

*  A **ferramenta Issues** relata automaticamente quaisquer problemas de contraste de cor para toda a página da Web, quando o texto e a cor do plano de fundo não são contrastados o suficiente.  Esta abordagem é descrita em [Verificar se as cores de texto têm contraste suficiente.](test-issues-tool.md#verify-that-text-colors-have-enough-contrast)

*  Emular um estado não padrão, como o estado, usando o Estado do Elemento Toggle no painel Estilos, descrito em Verificar acessibilidade de todos os `hover` estados de [elementos](test-inspect-states.md). **** ****


## <a name="see-also"></a>Consulte também

*  [Verifique a acessibilidade de todos os estados dos elementos][DevtoolsAccessibilityTestInspectStates]
*  [Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web](test-inspect-tool.md)
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityTestInspectStates]: test-inspect-states.md "Verifique a acessibilidade de todos os estados de elementos | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
