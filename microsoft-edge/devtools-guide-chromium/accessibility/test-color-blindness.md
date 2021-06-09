---
description: Verifique se as páginas da Web podem ser usáveis por pessoas com deficiências de cor usando a lista lista suspenso Deficiências de Visão emular na ferramenta Renderização.
title: Verifique se a página pode ser usada por pessoas com daltonismo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 54cd7230f0402bfeb4b5ee28d2bcd0947794676f
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597205"
---
# <a name="verify-that-the-page-is-usable-by-people-with-color-blindness"></a>Verifique se a página pode ser usada por pessoas com daltonismo

<!-- Rendering tool: Emulate vision deficiencies: Protanopia -->

Para verificar se uma página da Web pode ser usada por pessoas com deficiências de cor, na ferramenta **Rendering,** use a lista suspenso Deficiências de visão **emular.**

Na página da web de demonstração de teste de acessibilidade, os diferentes estados de doação usam a cor como o único meio de diferenciação.
*  Verde significa que uma grande quantidade de doações foram recebidas.
*  Amarelo significa que uma quantidade média de doações foi recebida.
*  Vermelho significa que uma baixa quantidade de doações foi recebida.

Mas você não pode esperar que todos os seus usuários experimentem essas cores conforme o pretendido.  Usando o recurso **Emular** deficiências de visão da ferramenta **Rendering,** você pode descobrir que esse design não é bom o suficiente, simulando como as pessoas com uma visão diferente perceberiam seu design.


Para verificar se uma página da Web pode ser usável por pessoas com deficiência de cor:

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Selecione **Esc** para abrir a Gaveta na parte inferior do DevTools.  Selecione o ícone na parte superior da Gaveta para ver a lista de ferramentas e selecione **+** **Renderização**.  

1.  Na lista lista lista suspenso **Deficiências de visão** emular, selecione **Protanopia**.  _A protanopia_ reduz a sensibilidade à luz vermelha, tornando difícil diferenciar verde, vermelho e amarelo.

    :::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Mostrar o documento como alguém com protanopia o verá" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
        Mostrar o documento como alguém com protanopia o verá
    :::image-end:::
    
1.  Na ferramenta **Renderização,** abaixo **Emular**deficiências de visão, selecione **Nenhuma emulação** para remover a simulação.


## <a name="see-also"></a>Consulte também

*  [Emular][DevToolsVisionDeficiencies] deficiências de visão - Define **** os itens na lista de lista suspenso deficiências de visão emular, incluindo Protanopia, Deuteranopia, Tritanopia e Achromatopsia.
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emular deficiências de visão | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
