---
description: Use o painel mídia para ver informações e depurar a guia media players por navegador.
title: Exibir e depurar informações do media players
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: dfcf17861c0296e347007bc3a1a02a2b80661e6f
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11105168"
---
# Exibir e depurar informações do media players  

Use o painel **mídia** no Microsoft Edge devtools para exibir informações e depurar a guia media players por navegador.  

## Abrir o painel mídia  

O painel **mídia** é o local principal no devtools para inspecionar o Media Player de uma página da Web.

1.  [Abra o devtools][DevtoolsGuideChromiumOpen].  
1.  Para abrir o painel **mídia** , escolha **Personalizar e controle devtools** `...`  >  **mais ferramentas**de  >  **mídia**.  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-empty.msft.png":::
       Painel **mídia**  
    :::image-end:::  
    
## Ver as informações do media players  

1.  Navegue até uma página da Web com um Media Player, como a página da Web a seguir.  
    
    [Maximizar a produtividade com as ferramentas de desenvolvedor Edge][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  No menu **jogadores** , é exibido um player de mídia.  
1.  Selecione o jogador.  A guia **Propriedades** exibe as propriedades do Media Player.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-view.msft.png":::
       Propriedades da mídia  
    :::image-end:::  
    
1.  Para ver todos os eventos do Media Player, escolha a guia **Events (eventos** ).  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-events.msft.png":::
       Eventos de mídia  
    :::image-end:::  
    
1.  Para exibir os logs de mensagens do Media Player, escolha a guia **mensagens** .  Você pode filtrar as mensagens por nível de log ou cadeia de caracteres.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-messages.msft.png":::
       Mensagens de mídia  
    :::image-end:::  
    
1.  Na guia **linha do tempo** , a reprodução de mídia e o status do buffer são exibidos ao vivo.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-timeline.msft.png":::
       Linha do tempo de mídia  
    :::image-end:::  
    
### Depuração remota  

Exiba as informações do Media Player em um dispositivo Android a partir de seu computador com Windows ou macOS.  

1.  Para configurar a depuração remota, navegue até [introdução à depuração remota de dispositivos Android][DevtoolsGuideChromiumRemoteDebuggingIndex].  
1.  Exiba as informações do Media Player remotamente.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## Ocultar e mostrar media players  

Às vezes, você executa mais de um Media Player em uma página da Web ou usa a mesma guia do navegador para navegar por páginas da Web diferentes, cada uma com media players.

Você pode optar por ocultar \ (ou mostrar \) cada Player de mídia para ter uma experiência de depuração mais fácil.  

1.  Navegue até várias páginas da Web de vídeo diferentes usando a mesma guia do navegador.  
1.  Para ocultar players de mídia, execute uma das seguintes ações.  
    *   Para ocultar um Media Player, passe o mouse sobre um Media Player, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **ocultar Player**.  
    *   Para ocultar todos os outros media players, passe o mouse em um Media Player, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **ocultar todos os outros**.  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-hide-show.msft.png":::
       Ocultar players de mídia  
    :::image-end:::  
    
## Exportar informações do player de mídia  

1.  Para baixar as informações do Media Player como um arquivo JSON, passe o mouse em um player de mídia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **salvar informações do jogador**.  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-save.msft.png":::
       Exportar informações de mídia  
    :::image-end:::  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Abrir o Microsoft Edge DevTools"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Introdução à depuração remota de dispositivos Android | Documentos da Microsoft"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximizar a produtividade com as ferramentas de desenvolvedor Edge | Vídeo do Bing"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

