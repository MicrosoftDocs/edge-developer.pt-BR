---
description: Verifique se há suporte para teclado usando as teclas Tab e Enter.
title: Verifique o suporte ao teclado usando as teclas Tab e Enter
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 48151e16a9059b5ebaadca36f29447d4ad3be8c7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597167"
---
# <a name="check-for-keyboard-support-by-using-the-tab-and-enter-keys"></a>Verifique o suporte ao teclado usando as teclas Tab e Enter


Nem todos os usuários têm um ponteiro ou dispositivo de toque, e nem todos os usuários podem ver os projetos da Web que criamos.  Por isso, é importante que a interface do usuário funcione pelo menos com um teclado.  Certifique-se de usar a chave para mover o foco para cada controle de formulário em uma página da Web e garantir que você possa usar a chave `Tab` `Enter` para enviar formulários.

Você pode testar a usabilidade de uma página da Web para usuários de teclado de várias maneiras:
*  Usando o teclado, especialmente `Tab` as `Shift` + `Tab` teclas , e `Enter` .  Esta abordagem é descrita neste artigo.
*  Verifique se há suporte para teclado para um elemento individual usando a **ferramenta Inspecionar.**  A sobreposição de informações da ferramenta Inspect inclui uma seção **Accessibility** que inclui uma linha focalizada **no** teclado.  
*  Verifique a **seção Acessibilidade** do relatório **problemas em** busca de problemas de suporte ao teclado.

Para verificar a página de demonstração de problemas de acessibilidade usando um teclado em vez de um mouse, execute as seguintes etapas:

1.  Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia do navegador.

1.  Use um teclado para navegar no documento de demonstração, usando as `Tab` teclas e `Shift` + `Tab` para saltar de elemento para elemento.  Na página da web de demonstração, a `Tab` chave primeiro move o foco para o formulário de pesquisa na `header` seção.

1.  Selecione `Tab` para colocar o foco em um botão e clique no botão `Enter` focado.  Por exemplo, na página de demonstração, selecione para colocar o foco no campo Pesquisa e `Tab` selecione enviar a **** `Enter` pesquisa.  Essa abordagem produz o mesmo resultado que selecionar o **botão ir.**  Selecionar `Enter` para enviar o formulário **de** Pesquisa funciona corretamente.

1.  Selecione `Tab` novamente.  O próximo elemento em que você coloca o foco é o primeiro link **Mais** na seção da página da Web, conforme `content` indicado por um contorno.
    
    :::image type="complex" source="../media/a11y-testing-keyboard-focus-on-element.msft.png" alt-text="Navegando o documento usando o teclado e a tecla Tab. O foco é mostrado em um link no documento." lightbox="../media/a11y-testing-keyboard-focus-on-element.msft.png":::
        Navegando o documento usando o teclado e a tecla de tabulação. O foco é mostrado em um link no documento.
    :::image-end:::
    
1.  Selecione `Tab` várias outras vezes até passar o último link **Mais.**  A página rola para cima e você parece estar em um elemento da página, mas não há como dizer qual elemento é.

1.  Observe a URL na parte inferior esquerda.  Se você olhar para a parte inferior esquerda da tela (ou se você usar um leitor de tela), perceberá que está no menu de navegação da barra lateral com links azuis, pois o navegador mostra a URL que o link **Gatos** aponta para ( `#cats` ).

    :::image type="complex" source="../media/a11y-testing-lack-of-focus-style.msft.png" alt-text="A falta de estilo de foco torna impossível saber onde você está no documento no momento. A única dica é a exibição do destino do link no canto inferior esquerdo da tela" lightbox="../media/a11y-testing-lack-of-focus-style.msft.png":::
        A falta de estilo de foco torna impossível saber onde você está no documento no momento. A única dica é a exibição do destino do link no canto inferior esquerdo da tela.
    :::image-end:::

1.  Selecione `Tab` novamente, para chegar ao campo de entrada no formulário de doação.  No entanto, você não pode alcançar os botões acima da caixa de texto selecionando `Tab` . Não é possível usar o teclado para colocar o foco nos **botões 50,** **100**ou **200** e, em seguida, selecione-os.  Além disso, `Enter` selecionar não envia o formulário de doação.

    :::image type="complex" source="../media/a11y-testing-form-field-with-outline.msft.png" alt-text="O único elemento acessível ao teclado no formulário de doação é o campo de entrada de texto" lightbox="../media/a11y-testing-form-field-with-outline.msft.png":::
        O único elemento acessível ao teclado no formulário de doação é o campo de entrada de texto
    :::image-end:::
    
1.  Selecionar novamente coloca o foco na barra de navegação superior da página, com botões de `Tab` menu para **Home,** **Adopt a Pet,** **Doar,** **Trabalhos**e **Sobre Nós**.  Selecione `Tab` ou coloque o foco em um botão de `Shift` + `Tab` menu, conforme indicado por um contorno de foco.  Em `Enter` seguida, selecione para acessar essa seção da página da Web.

    :::image type="complex" source="../media/a11y-testing-menu-with-outline.msft.png" alt-text="O menu principal tem um destaque e um contorno de foco e, portanto, é acessível ao teclado" lightbox="../media/a11y-testing-menu-with-outline.msft.png":::
        O menu principal tem um destaque e um contorno de foco e, portanto, é acessível ao teclado
    :::image-end:::
    
Com base no passo a passo acima, encontramos os seguintes problemas que precisam ser corrigidos.

*  Ao usar um teclado, os links azuis do menu de navegação da barra lateral não indicam visualmente qual link tem foco.  Para obter mais informações, navegue [até Analisar a falta de indicação](test-analyze-no-focus-indicator.md)do foco do teclado em um menu de barra lateral .

*  No formulário de doação, a quantidade de botões e **o** botão Doar não funcionam com um teclado.  Para obter mais informações, navegue [até Analisar a falta de suporte ao teclado em um formulário](test-analyze-no-keyboard-support.md).

*  A ordem do acesso ao teclado por meio de seções da página não está correta.  Navegue por todos os links **Mais** no documento antes de chegar ao menu de navegação da barra lateral.  Quando a chave coloca o foco no menu de navegação da barra lateral, você `Tab` já percorreu todo o conteúdo da página. O menu de navegação da barra lateral destina-se a fornecer acesso fácil ao conteúdo da página.  Para obter mais informações sobre como resolver esse problema, navegue até Testar o suporte ao [teclado usando o Visualizador de](test-tab-key-source-order-viewer.md)Ordem de Origem .


## <a name="see-also"></a>Consulte também

*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
