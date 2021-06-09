---
description: Verifique se há problemas de contraste com tema escuro e tema claro (para modo escuro e modo claro) usando o recurso de mídia \"Emular mídia CSS prefers-color-scheme\" na ferramenta Rendering.
title: Verifique se há problemas de contraste com o tema escuro e o tema claro
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 052c75b610ec872329f387e46819867f299a8ca9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597204"
---
# <a name="check-for-contrast-issues-with-dark-theme-and-light-theme"></a>Verifique se há problemas de contraste com o tema escuro e o tema claro

<!-- Rendering tool: Emulate CSS media feature prefers-color-scheme -->

Ao testar a acessibilidade de cores, pode haver diferentes temas de cores de exibição que você precisa testar para problemas de contraste.

A maioria dos sistemas operacionais vem com um modo escuro e um modo claro.  Sua página da Web pode reagir a essa configuração do sistema operacional usando uma consulta de mídia CSS.  Você pode testar esses temas e testar sua consulta de mídia CSS sem precisar alterar a configuração do sistema operacional usando as opções CSS na `prefers-color-scheme` ferramenta **Rendering.**

Como exemplo, a página de demonstração de teste de acessibilidade inclui um tema claro e um tema escuro.  A página de demonstração herda a configuração de tema escuro ou claro do sistema operacional.  Se usarmos o DevTools para simular o sistema operacional que está sendo definido como um esquema de luz e atualizar a página da Web de demonstração, a ferramenta **Issues** mostrará seis problemas de contraste de cor em vez de dois.  (Você pode ver números diferentes.)


Para emular a seleção de um usuário do tema de cor preferencial:

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Selecione **Esc** para abrir a Gaveta na parte inferior do DevTools.  Selecione o ícone na parte superior da Gaveta para ver a lista de ferramentas e selecione **+** **Renderização**.  A ferramenta Rendering é exibida.

1.  No recurso **de mídia CSS emular prefere a lista** suspenso esquema de cores, selecione **prefers-color-scheme: light**.      A página da Web é renderizada usando `light-theme.css` .


    :::image type="complex" source="../media/a11y-testing-simulating-light-mode.msft.png" alt-text="Usar a ferramenta Rendering para simular um modo de luz e disparar o outro tema do documento" lightbox="../media/a11y-testing-simulating-light-mode.msft.png":::
        Usar a ferramenta Rendering para simular um modo de luz e disparar o outro tema do documento
    :::image-end:::


1.  Selecione a **ferramenta Problemas** e expanda a **seção Acessibilidade.**  Dependendo de vários fatores, você pode receber `Insufficient color contrast` avisos. Observe nos **RECURSOS AFETADOs** que há 6 elementos com contraste de cor insuficiente.
    
    :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Novos problemas de contraste detectados devido à alteração para tema claro" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
        Novos problemas de contraste detectados devido à alteração para tema claro
    :::image-end:::
    
    Em nossa página de demonstração, a seção **Status** de doação da página é ilegível no modo claro e precisa ser mudada. 
    
    :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="A seção Status da Doação tem problemas de contraste no modo claro" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
        A **seção Status da Doação** tem problemas de contraste no modo claro
    :::image-end:::
    
1.  No DevTools, selecione a ferramenta **Elementos** e selecione **Ctrl+F** em Windows/Linux ou **Command+F** no macOS.  A **caixa** de texto Encontrar é exibida, para pesquisar na árvore DOM HTML.
 
1.  Insira `scheme` .  As seguintes consultas de mídia CSS são encontradas e os arquivos CSS correspondentes agora podem ser atualizados.

    ```html
    <link rel="stylesheet" href="css/light-theme.css" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)">
    <link rel="stylesheet" href="css/dark-theme.css" media="(prefers-color-scheme: dark)">
    ```


## <a name="see-also"></a>Consulte também

*  [Simulação de esquema de cores escuro ou claro][DevToolsColorSchemeSimulation]
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Simulação de esquema de cores escuro ou claro | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
