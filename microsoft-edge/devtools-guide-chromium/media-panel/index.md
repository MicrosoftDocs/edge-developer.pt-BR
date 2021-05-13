---
description: Use a ferramenta Mídia para exibir informações e depurar os media players por guia do navegador.
title: Exibir e depurar informações de players de mídia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0d2a60c31d5239a4b47102ae96a713b8bfcf46f3
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564060"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="view-and-debug-media-players-information"></a>Exibir e depurar informações de players de mídia  

Use a **ferramenta Mídia** no Microsoft Edge DevTools para exibir informações e depurar os media players por guia do navegador.  

## <a name="open-the-media-tool"></a>Abra a ferramenta Mídia  

A **ferramenta Mídia** é o principal local no DevTools para inspecionar o media player de uma página da Web.

1.  [Abra DevTools][DevtoolsGuideChromiumOpen].  
1.  Para abrir o **painel Mídia,** escolha **Personalizar e controlar DevTools** `...`  >  **Mais ferramentas**  >  **Mídia**.  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Painel de mídia" lightbox="../media/media-panel-empty.msft.png":::
       **Painel de** mídia  
    :::image-end:::  
    
## <a name="view-media-players-information"></a>Exibir informações de media players  

1.  Navegue até uma página da Web com um media player, como a página da Web a seguir.  
    
    [Maximizando a produtividade com as Ferramentas de Desenvolvedor de Borda][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  No menu **Jogadores,** um media player é exibido.  
1.  Escolha o player.  O **painel Propriedades** exibe as propriedades do media player.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propriedades de mídia" lightbox="../media/media-panel-view.msft.png":::
       Propriedades de mídia  
    :::image-end:::  
    
1.  Para exibir todos os eventos do media player, escolha o **painel Eventos.**  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Eventos de mídia" lightbox="../media/media-panel-events.msft.png":::
       Eventos de mídia  
    :::image-end:::  
    
1.  Para exibir os logs de mensagens do media player, escolha o **painel Mensagens.**  Você pode filtrar as mensagens por nível de log ou cadeia de caracteres.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Mensagens de mídia" lightbox="../media/media-panel-messages.msft.png":::
       Mensagens de mídia  
    :::image-end:::  
    
1.  No painel **Linha do** Tempo, a reprodução de mídia e o status do buffer são exibidos ao vivo.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Linha do tempo da mídia" lightbox="../media/media-panel-timeline.msft.png":::
       Linha do tempo da mídia  
    :::image-end:::  
    
### <a name="remote-debugging"></a>Depuração remota  

Exibir as informações dos media players em um dispositivo Android do computador Windows ou macOS.  

1.  Para configurar a depuração remota, navegue até [Começar com dispositivos Android de depuração remota.][DevtoolsGuideChromiumRemoteDebuggingIndex]  
1.  Exibir as informações dos media players remotamente.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a>Ocultar e mostrar jogadores de mídia  

Às vezes, você pode executar mais de um media player em uma página da Web ou usar a mesma guia do navegador para navegar em diferentes páginas da Web, cada uma com media players.

Você pode optar por ocultar \(ou mostrar\) cada media player para uma experiência de depuração mais fácil.  

1.  Navegue até várias páginas da Web de vídeo diferentes usando a mesma guia do navegador.  
1.  Para ocultar media players, conclua uma das seguintes ações.  
    *   Para ocultar um media player, passe o mouse em um media player, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Ocultar player**.  
    *   Para ocultar todos os outros media players, passe o mouse em um media player, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Ocultar todos os outros**.  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ocultar media players" lightbox="../media/media-panel-hide-show.msft.png":::
       Ocultar media players  
    :::image-end:::  
    
## <a name="export-media-player-information"></a>Exportar informações do media player  

1.  Para baixar as informações do media player como um arquivo JSON, passe o mouse em um media player, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Salvar informações do player**.  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportar informações de mídia" lightbox="../media/media-panel-save.msft.png":::
       Exportar informações de mídia  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximizando a produtividade com as ferramentas de desenvolvedor de borda | Bing Vídeo"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

