---
description: Use a ferramenta Problemas para identificar e corrigir problemas com a página da Web atual.
title: Encontrar e corrigir problemas usando a ferramenta Problemas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 86277c509aa4b67635661ba3a316fb5b1e3b9d14
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624679"
---
<!-- Copyright Sam Dutton

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-and-fix-problems-using-the-issues-tool"></a>Encontrar e corrigir problemas usando a ferramenta Problemas

No Microsoft Edge DevTools, a ferramenta **Issues** analisa automaticamente a página da Web atual, relata problemas agrupados por tipo e fornece documentação para ajudar a explicar e resolver os problemas.

A **ferramenta Issues** fornece comentários nas seguintes categorias:
*  Acessibilidade.
*  Compatibilidade entre navegadores.
*  Desempenho.
*  Aplicativos Web Progressivos.
*  Segurança.
*  Outro.

Os comentários na ferramenta **Issues** são fornecidos por várias fontes, incluindo a plataforma Chromium, o eixo Deque, os dados de compatibilidade do navegador MDN e o webhint.  Para obter informações sobre essas fontes de comentários que preenchem a **ferramenta Problemas,** navegue até:
*  [visão geral das ferramentas de eixo][DequeAxe]
*  [browser-compat-data repo][MDNCompat]
*  [Dica da web][webhintIo]


## <a name="open-the-issues-tool"></a>Abra a ferramenta Problemas

Execute as etapas a seguir para abrir a **ferramenta Problemas** usando uma página de demonstração.


1.  Navegue até uma página da Web que contém problemas para corrigir.  Por exemplo, abra a [página de demonstração de][A11ytestingPagewitherrors] teste de acessibilidade em uma nova guia ou janela.

1.  Abra DevTools.  Após alguns segundos, o contador **Problemas** \( Contador de problemas ![ \) é exibido, no canto superior direito do ](../media/issues-counter-icon.msft.png) DevTools.  O número de problemas no contador Problemas pode ser diferente.

1.  Selecione o contador **Problemas**.  A **ferramenta Issues** é aberta com problemas agrupados em categorias diferentes.

    :::image type="complex" source="../media/issues-tool-categories.msft.png" alt-text="Categorias de problemas na ferramenta Problemas na página de demonstração" lightbox="../media/issues-tool-categories.msft.png":::
       Categorias de problemas na ferramenta Problemas na página de demonstração
    :::image-end:::

### <a name="other-ways-to-open-the-issues-tool"></a>Outras maneiras de abrir a ferramenta Problemas

Há várias maneiras adicionais de abrir a **ferramenta Problemas:**
*  Selecione o **menu Mais Ferramentas** ( ) no painel principal ou na **+** **Gaveta**e selecione **Problemas**.
*  Selecione **Personalizar e controlar DevTools**Mais problemas  >  **de**  >  **ferramentas.**
*  Na árvore DOM na ferramenta **Elementos,** selecione e clique em um nome `Shift` de elemento sublinhado ondulado.  Ou abra o menu de contexto em um elemento sublinhado ondulado e selecione **Exibir problemas**.

### <a name="issues-are-automatically-ordered-by-severity"></a>Os problemas são ordenados automaticamente por gravidade

Em cada categoria de problemas, primeiro os erros são listados, depois avisos e dicas.

:::image type="complex" source="../media/issues-ordered-by-severity.msft.png" alt-text="A ferramenta Issues exibe problemas de desempenho classificação por gravidade" lightbox="../media/issues-ordered-by-severity.msft.png":::
   A **ferramenta Issues** exibe problemas de desempenho classificação por gravidade
:::image-end:::

### <a name="include-third-party-issues"></a>Incluir problemas de terceiros

Para incluir problemas causados por sites de terceiros, na parte superior da ferramenta **Problemas,** selecione a caixa de seleção Incluir **problemas** de terceiros.


## <a name="expand-entries-in-the-issues-tool"></a>Expandir entradas na ferramenta Problemas

A **ferramenta Issues** apresenta documentação adicional e correções recomendadas para aplicar a cada problema.  Para expandir um problema para obter essas informações adicionais, selecione um problema, da seguinte forma.

1.  Abra a [página de demonstração][A11ytestingPagewitherrors] em uma nova janela ou guia e abra DevTools.

1.  Abra a **ferramenta Problemas** selecionando o contador **Problemas** \( Contador de ![ problemas ](../media/issues-counter-icon.msft.png) \).

1.  Selecione um problema para expandir o problema.

    :::image type="complex" source="../media/issues-tool-initial-view-accessibility-page.msft.png" alt-text="A ferramenta Issues que exibe informações adicionais sobre como corrigir o problema" lightbox="../media/issues-tool-initial-view-accessibility-page.msft.png":::
       A **ferramenta Issues** que exibe informações adicionais sobre como corrigir o problema
    :::image-end:::

Cada problema exibido tem os seguintes componentes:
*   Uma título que descreve o problema.
*   Uma descrição que fornece mais contexto e soluções propostas.
*   Uma **seção RECURSOS AFETADOs** que se vincula a recursos no DevTools, como **a ferramenta Elementos,** **Fontes** **ou** Rede.
*   Links para documentação posterior.


## <a name="view-issues-in-context-of-an-associated-tool"></a>Exibir problemas no contexto de uma ferramenta associada

Um problema na ferramenta **Problemas** pode incluir um ou mais links que abrem ferramentas diferentes, como **a ferramenta Elementos,** **Fontes** **ou** Rede. Você pode abrir uma dessas ferramentas para executar etapas adicionais de solução de problemas. Para abrir uma ferramenta vinculada da **ferramenta Problemas,** execute as etapas a seguir.

1.  Conforme descrito na seção anterior, abra a página de demonstração e expanda um problema na **ferramenta Problemas.**

1.  Em **RECURSOS**  >  **AFETADOs Abra**em , selecione o nome da ferramenta.  O recurso afetado é exibido na ferramenta selecionada.

    :::image type="complex" source="../media/issues-tool-affected-resource-opens-elements-tool.msft.png" alt-text="Selecione uma ferramenta para abrir um recurso afetado de dentro da ferramenta Issues" lightbox="../media/issues-tool-affected-resource-opens-elements-tool.msft.png":::
       Selecione uma ferramenta para abrir um recurso afetado de dentro da ferramenta Issues
    :::image-end:::

    Um problema expandido pode ter um link **Rede** para exibir o recurso afetado na **ferramenta Rede.**

    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="A ferramenta Rede é aberta quando você seleciona um link de recurso rede" lightbox="../media/issues-tab-view-issue.msft.png":::
    A **ferramenta Rede** é aberta quando você seleciona um link de **recurso** rede
    :::image-end:::


## <a name="open-issues-from-the-dom-tree"></a>Abrir problemas da árvore DOM

Se um elemento tiver um problema associado, a árvore DOM na ferramenta **Elements** mostrará um sublinhado ondulado sob o nome do elemento.  Você pode abrir o menu de contexto (clique com o botão direito do mouse) no elemento e selecione **Exibir**problemas ou selecione e clique com o botão esquerdo no elemento com o `Shift` sublinhado ondulado.

Para exibir um problema para elementos com sublinhados ondulados na árvore DOM, execute as etapas a seguir.

1.  Abra uma página, como a página [de demonstração][A11ytestingPagewitherrors], em uma nova guia ou janela.

1.  Abra DevTools e selecione a **guia Elementos.**

1.  Na árvore DOM, expanda `<body>`  >  `<header>`  >  `<form>` .  Observe que o `<input>` elemento tem um sublinhado ondulado.

    :::image type="complex" source="../media/issues-wavy-underlines-dom-tree.msft.png" alt-text="Problemas sublinhados ondulados na árvore DOM na ferramenta Elements" lightbox="../media/issues-wavy-underlines-dom-tree.msft.png":::
       Problemas sublinhados ondulados na árvore **DOM** na **ferramenta Elements**
    :::image-end:::

1.  Passe o mouse sobre o `<input>` elemento.  Uma dica de ferramenta exibe informações sobre o problema.

1.  Abra o menu de contexto no elemento com o sublinhado ondulado e selecione **Exibir problemas**.  A **ferramenta Issues** abre e exibe o problema associado a esse elemento.

    :::image type="complex" source="../media/issues-opened-from-dom-tree-wavy-underline.msft.png" alt-text="Detalhes sobre problemas em um elemento sublinhado ondulado na árvore DOM" lightbox="../media/issues-opened-from-dom-tree-wavy-underline.msft.png":::
       Detalhes sobre problemas em um elemento sublinhado **ondulado** na árvore DOM
    :::image-end:::


## <a name="see-also"></a>Consulte também

* [Teste automaticamente uma página da Web em busca de problemas de acessibilidade](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

<!-- links -->
[DevtoolsOpenIndex]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"
<!-- external links -->
[A11ytestingPagewitherrors]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página de demonstração de teste de acessibilidade | Microsoft Docs"
[DequeAxe]: https://www.deque.com/axe "axe Tools Overview | Deque"
[MDNCompat]: https://github.com/mdn/browser-compat-data "Dados de Compatibilidade do Navegador MDN | GitHub"
[webhintIo]: https://webhint.io "webhint.io"

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/issues/index) e é de autoria de [Sam Dutton][SamDutton] \(Developer Advocate\).
[ ![ Licença do Creative Commons Este][CCby4Image]][CCA4IL] trabalho é licenciado sob uma Licença Internacional de [Atribuição do Creative Commons 4.0.][CCA4IL]

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton
