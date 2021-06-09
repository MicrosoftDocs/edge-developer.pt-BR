---
description: Para verificar se uma página da Web pode ser usada com visão desfocado, na ferramenta Renderização, use a lista suspenso Deficiências de visão emular.
title: Verifique se a página pode ser usada com visão turva
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2fc1a1cf7746591573fce07946c7fb11abf42705
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597207"
---
# <a name="verify-that-the-page-is-usable-with-blurred-vision"></a>Verifique se a página pode ser usada com visão turva

<!-- Rendering tool: Emulate vision deficiencies: Blurred vision -->

Para simular a visão desfocado, na ferramenta **Rendering,** use o menu **Emular deficiências de** visão.  Quando você usa esse recurso com a página da Web de demonstração, você pode ver que a sombra de soltar no texto no menu superior dificulta a leitura dos itens do menu.

Para verificar se uma página da Web é usável com visão desfocado:

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Selecione **Esc** para abrir a Gaveta na parte inferior do DevTools.  Selecione o ícone na parte superior da Gaveta para exibir a lista de ferramentas e selecione **+** **Renderização**.  

1.  Na lista **lista suspenso Deficiências de visão** emular, selecione Visão **desfocado**.

    :::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simulando uma página desfocado" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
        Simulando uma página desfocado
    :::image-end:::

    Observe que a `text-shadow` propriedade CSS torna o texto dos itens de menu difíceis de ler no menu superior. Por exemplo, revise **Home**, **Adopt a Pet**e outros itens de menu.
    
1.  Na ferramenta **Rendering,** em **Emular**deficiências de visão, selecione **Nenhuma emulação** para remover a simulação de visão desfocado.


## <a name="see-also"></a>Consulte também

*  [Emular deficiências visuais](emulate-vision-deficiencies.md)
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
