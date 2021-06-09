---
description: Teste automaticamente uma página da Web para problemas de acessibilidade usando a seção Acessibilidade da ferramenta Problemas.
title: Teste automaticamente uma página da Web em busca de problemas de acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 986a021d2fd390cd45bd53dcfc37a83d58ed2338
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597172"
---
# <a name="automatically-test-a-webpage-for-accessibility-issues"></a>Teste automaticamente uma página da Web em busca de problemas de acessibilidade

A **ferramenta Issues** inclui uma seção **Acessibilidade** que relata automaticamente problemas como falta de texto alternativo em imagens, rótulos ausentes em campos de formulário e contraste insuficiente de cores de texto.  A **ferramenta Issues** está dentro da **Gaveta** na parte inferior do DevTools.  Este artigo usa a página da Web de demonstração de teste de acessibilidade para passar por meio do uso da seção **Acessibilidade** da **ferramenta Issues.**

Há várias maneiras de abrir a **ferramenta Problemas,** como:
*  Selecione o **contador Problemas** \( Contador de problemas ![ ](../media/issues-counter-icon.msft.png) \) no canto superior direito do DevTools.
*  Na ferramenta **Elementos,** na árvore DOM, **Shift+clique em** um sublinhado ondulado em um elemento.
*  No **Menu Comando ,** digite `issues` e selecione Mostrar **Problemas**.


## <a name="view-the-accessibility-section-of-the-issues-tool"></a>Exibir a seção Acessibilidade da ferramenta Problemas

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.  No canto superior direito, o contador **Problemas** \( Contador de problemas \) é exibido, como um ícone de bolha de fala juntamente com o número de problemas ![ ](../media/issues-counter-icon.msft.png) detectados automaticamente.  Um número diferente pode aparecer no navegador, e o número pode ser atualizado à medida que você usa o DevTools.

    :::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="O contador Problemas no DevTools, indicando quantos problemas há no documento atual" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
        O **contador Problemas** no DevTools, indicando quantos problemas há no documento atual
    :::image-end:::

1.  Selecione o contador **Problemas**.  A **ferramenta Issues** é aberta, na **Gaveta** na parte inferior do DevTools.

    :::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Avisos de acessibilidade exibidos na ferramenta Problemas" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
        Avisos de acessibilidade exibidos na ferramenta Problemas
    :::image-end:::

1.  Na guia **Problemas,** expanda **a seção Acessibilidade.**


## <a name="verify-that-input-fields-have-labels"></a>Verificar se os campos de entrada têm rótulos

Para verificar se os campos de entrada têm rótulos conectados a eles, use a ferramenta **Problemas,** que verifica automaticamente toda a página da Web e relata esse problema na **seção** Acessibilidade.

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  No canto superior direito, selecione o contador **Problemas** \( ![ Contador de problemas ](../media/issues-counter-icon.msft.png) \).  A **ferramenta Issues** é aberta, na **Gaveta** na parte inferior do DevTools.

1.  Na guia **Problemas,** expanda **a seção Acessibilidade.**

1.  Expanda **o Aviso** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute` .

1. Selecione o link **Abrir em Elementos.**

    :::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Ferramenta Elements mostrando o HTML problemático após selecionar o link na ferramenta Problemas" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
        Ferramenta Elements mostrando o HTML problemático após selecionar o link na ferramenta **Problemas** :::image-end:::

    A **ferramenta Elements** é aberta, com o elemento realçado na árvore DOM.  O **painel Estilos** exibe as regras CSS aplicadas para o elemento.  O código a seguir agora é exibido.

    ```html
    <label>Search</label>
    <input type="search">
    <input type="submit" value="go">
    ```

    No código acima, o elemento é usado incorretamente, porque não há nenhuma conexão entre `label` o elemento e um elemento `label` `input` específico.  Para conectar o `label` elemento a um elemento `input` específico, use qualquer uma das opções a seguir.
    *   Aninhar `input` o elemento dentro do `label` elemento.
    *   No `label` elemento, adicione um `for` atributo que corresponde a um atributo do `id` `input` elemento.

    Também há outra maneira de testar a falta de conexões entre os elementos. Na ferramenta **Elementos,** selecione `<label>Search</label>` o elemento na árvore DOM.  Na página da Web, observe que o foco só aparece no rótulo **de** Pesquisa e não na caixa de texto de entrada.  A implementação correta colocaria o foco na caixa de texto de `search` entrada e no rótulo **de** Pesquisa.

1.  Como exemplo de uma conexão correta, selecione **o rótulo Outro** no formulário de doação.  Uma caixa de indicador de foco aparece corretamente na caixa de texto de entrada ao lado do **outro** rótulo, porque há valores de correspondência e `for` `id` atributo.

1.  Na ferramenta **Problemas,** selecione **Mais leitura** para saber mais sobre o problema.  Para abrir o link em uma nova guia, **Ctrl**clique no link em Windows/Linux ou Comando clique no + **** link **** + **** no macOS.

    :::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Link na guia Problemas apontando para informações mais detalhadas sobre o problema" lightbox="../media/a11y-testing-more-information-links.msft.png":::
        Link na guia **Problemas** apontando para informações mais detalhadas sobre o problema
    :::image-end:::


## <a name="verify-that-images-have-alt-text"></a>Verificar se as imagens têm texto alt

Os testes básicos de acessibilidade exigem que o texto alternativo (também chamado _de texto alt)_ seja fornecido para imagens.

Para verificar automaticamente se o texto alt é fornecido para imagens, use a **ferramenta Issues,** que tem uma **seção Accessibility.**  A **ferramenta Issues** está localizada na **Gaveta** na parte inferior do DevTools.

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Para abrir a **ferramenta Problemas,** selecione o contador **Problemas** no canto superior direito do DevTools.

1.  Na guia **Problemas,** expanda o aviso `Images must have alternate text: Element has no title attribute` .  Há quatro instâncias de imagens que não têm texto alt.

    :::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="A ferramenta Issues relata imagens que estão faltando texto alternativo" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
        A ferramenta Issues relata imagens que estão faltando texto alternativo
    :::image-end:::

Para obter mais informações, navegue [até Imagens deve ter texto alternativo](https://dequeuniversity.com/rules/axe/4.1/image-alt).


## <a name="verify-that-text-colors-have-enough-contrast"></a>Verificar se as cores de texto têm contraste suficiente

Para verificar automaticamente se as cores de texto têm contraste suficiente, use a ferramenta **Issues,** que tem uma **seção Accessibility.**  A **ferramenta Issues** está localizada na **Gaveta** na parte inferior do DevTools.

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Para abrir a **ferramenta Problemas,** selecione o contador **Problemas** no canto superior direito do DevTools.  Você pode receber avisos de que dois elementos na página da Web de demonstração não têm contraste suficiente.

    :::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problemas de contraste relatados na ferramenta Problemas" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
        Problemas de contraste relatados na ferramenta Problemas
    :::image-end:::

1.  Dependendo das configurações, a guia **Problemas** pode ter um aviso, como Os usuários podem ter dificuldades para ler conteúdo de texto devido ao contraste de **cor insuficiente.**   Você pode expandir esse aviso e, em seguida, expandir **recursos afetados.**  Uma lista de elementos aparece com uma lista de elementos que não têm contraste suficiente.


1.  Selecione o `li.high` elemento.  Na página da Web renderizada, o link **Cachorros** na seção **Doar** é realçado, exibindo uma pequena sobreposição de informações.  Essa é a mesma sobreposição que aparece quando você passar o mouse sobre um elemento na árvore DOM na **ferramenta Elements.**

    :::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Elemento na página da Web realçada após selecionar um link na seção Recursos Afetados" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
        Elemento na página da Web realçada após selecionar um link na seção **Recursos Afetados**
    :::image-end:::


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a>Sublinhados ondulados na árvore DOM indicam problemas detectados automaticamente 

A árvore DOM na ferramenta **Elements** sinaliza problemas diretamente no HTML com sublinhados ondulados.  Esses problemas são relatados pela **ferramenta Issues.**  Quando você **clica em Shift+clique** em qualquer elemento com um sublinhado ondulado, a **ferramenta Issues** é exibida.

1.  Na ferramenta **Elementos,** na árvore DOM, **Shift+clique** no elemento `<input type="search">` , que tem uma linha ondulada em `input` .  A **ferramenta Issues** é exibida e mostra o problema desse elemento.

    :::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Um elemento que tem um sublinhado ondulado no exibição DOM tem um problema" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
        Um elemento que tem um sublinhado ondulado no exibição DOM tem um problema
    :::image-end:::


## <a name="see-also"></a>Consulte também

*  [Encontre e corrige problemas com a ferramenta Microsoft Edge Problemas do DevTools][DevToolsIssuesTool]
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsIssuesTool]: ../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
