---
title: Depurar serviços em segundo plano com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 0ac2a057307a939069cbb3b48ecd38c9de71e5db
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581828"
---
<!-- Copyright Kayce Basques 
   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0
       
   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# Depurar serviços em segundo plano com o Microsoft Edge DevTools   



A seção **serviços em segundo plano** do Microsoft Edge devtools é uma coleção de ferramentas para APIs JavaScript que permite que seu site envie e Receba atualizações mesmo quando um usuário não tem seu site aberto.  
Um serviço em segundo plano é funcionalmente semelhante a um [processo em segundo plano] [WikiBackgroundProcess].  
O Microsoft Edge DevTools considera que cada uma das seguintes APIs seja um serviço em segundo plano:  

*   [Busca em segundo plano](#background-fetch)  
*   [Sincronização em segundo plano](#background-sync)  
*   [Notificações](#notifications)  
*   [Enviar mensagens por push](#push-messages)  

O Microsoft Edge DevTools pode registrar eventos de serviço em segundo plano por 3 dias, mesmo quando DevTools não está aberto.  
Isso pode ajudá-lo a garantir que os eventos sejam enviados e recebidos como esperado.  Você também pode inspecionar os detalhes de cada evento.  

> ##### Figura 1  
> Exibir os detalhes de um evento no painel de mensagens push  
> ![Exibir os detalhes de um evento no painel de mensagens push][PushDetails]  

## Busca em segundo plano   

A *API de busca em segundo plano** permite que um **trabalhador de serviço** Baixe recursos grandes, como filmes ou podcasts, como um serviço em segundo plano.  Para registrar o evento de busca em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:  

<!--Todo: add background fetch api section when available -->  

1.  [Abra o devtools][OpenDevTools].  
1.  Abrir o painel do **aplicativo** .  
1.  Abrir o painel **busca em segundo plano** .  
    
    > ##### Figura 2  
    > O painel busca em segundo plano  
    > ![O painel busca em segundo plano][FetchEmpty]  
    
1.  Clique em **gravar** ![ registro ][ImageRecordIcon] .  
   Depois de disparar uma atividade de busca em segundo plano, o DevTools registra os eventos na tabela.  
    
    > ##### Figura 3  
    > Um log de eventos no painel de busca em segundo plano  
    > ![Um log de eventos no painel de busca em segundo plano][FetchLog]  
    
1.  Clique em um evento para ver os detalhes no espaço abaixo da tabela.  
    
    > ##### Figura 4  
    > Exibir os detalhes de um evento no painel de busca em segundo plano  
    > ![Exibir os detalhes de um evento no painel de busca em segundo plano][FetchDetails]  

## Sincronização em segundo plano   

A **API de sincronização em segundo plano** permite que um **trabalhador de serviço** offline envie dados para um servidor depois que ele restabeleceu uma conexão com a Internet confiável.  Para registrar eventos de sincronização em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:  

<!--Todo: add background sync api section when available -->  

1.  [Abra o devtools][OpenDevTools].  
1.  Abrir o painel do **aplicativo** .  
1.  Abrir o painel **sincronização em segundo plano** .  
    
    > ##### Figura 5  
    > O painel sincronização em segundo plano  
    > ![O painel sincronização em segundo plano][SyncEmpty]  
    
1.  Clique em **gravar** ![ registro ][ImageRecordIcon] .  
   Depois de disparar uma atividade de sincronização em segundo plano, o DevTools registra os eventos na tabela.  
    
    > ##### Figura 6  
    > Um log de eventos no painel sincronização em segundo plano  
    > ![Um log de eventos no painel sincronização em segundo plano][SyncLog]  
    
1.  Clique em um evento para ver os detalhes no espaço abaixo da tabela.  
    
    > ##### Figura 7  
    > Exibir os detalhes de um evento no painel sincronização em segundo plano  
    > ![Exibir os detalhes de um evento no painel sincronização em segundo plano][SyncDetails]  
    
## Notificações 

Depois que um **trabalhador do serviço** recebeu uma mensagem de [envio][MDNPush] de um servidor, o trabalhador do serviço usa a API de [notificações][MDNNotifications] para exibir os dados para um usuário.  Para registrar notificações por três dias, mesmo quando o DevTools não estiver aberto:  

1.  [Abra o devtools][OpenDevTools].  
1.  Abrir o painel do **aplicativo** .  
1.  Abrir o painel **notificações** .  
    
    > ##### Figura 8  
    > O painel notificações  
    > ![O painel notificações][NotificationsEmpty]  
    
1.  Clique em **gravar** ![ registro ][ImageRecordIcon] .  
   Depois de disparar algumas atividades de notificações, o DevTools registra os eventos na tabela.  
    
    > ##### Figura 9  
    > Um log de eventos no painel notificações  
    > ![Um log de eventos no painel notificações][NotificationsLog]  
    
1.  Clique em um evento para ver os detalhes no espaço abaixo da tabela.  
    
    > ##### Figura 10  
    > Exibir os detalhes de um evento no painel notificações  
    > ![Exibir os detalhes de um evento no painel notificações][NotificationsDetails]  
    
## Enviar mensagens por push 

Para exibir uma notificação por push para um usuário, um **trabalhador de serviço** deve primeiro usar a API de [mensagem Push][MDNPush] para receber dados de um servidor.  Quando o trabalhador do serviço está pronto para exibir a notificação, ele usa a [API de notificações][MDNNotifications].  Para registrar mensagens por Push por 3 dias, mesmo quando o DevTools não está aberto:  

1.  [Abra o devtools][OpenDevTools].  
1.  Abrir o painel do **aplicativo** .  
1.  Abrir o painel de **mensagens Push** .  
    
    > ##### Figura 11  
    > O painel de mensagens push  
    > ![O painel de mensagens push][PushEmpty]  

1.  Clique em **gravar** ![ registro ][ImageRecordIcon] .  
    Depois de disparar uma atividade de mensagem por push, o DevTools registra os eventos na tabela.  
    
    > ##### Figura 12  
    > Um log de eventos no painel de mensagens push  
    > ![Um log de eventos no painel de mensagens push][PushLog]  

1.  Clique em um evento para ver os detalhes no espaço abaixo da tabela.  
    
    > ##### Figura 13  
    > Exibir os detalhes de um evento no painel de mensagens push  
    > ![Exibir os detalhes de um evento no painel de mensagens push][PushDetails2]  
    
 



<!-- image links -->  

[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[PushDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Figura 1: exibindo os detalhes de um evento no painel de mensagens push"  
[FetchEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-empty.msft.png "Figura 2: painel de busca em segundo plano"  
[FetchLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch.msft.png "Figura 3: um log de eventos no painel de busca em segundo plano"  
[FetchDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-details.msft.png "Figura 4: exibindo os detalhes de um evento no painel de busca em segundo plano"  
[SyncEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-empty.msft.png "Figura 5: painel de sincronização em segundo plano"  
[SyncLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync.msft.png "Figura 6: um log de eventos no painel de sincronização em segundo plano"  
[SyncDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-details.msft.png "Figura 7: exibindo os detalhes de um evento no painel de sincronização em segundo plano"  
[NotificationsEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-empty.msft.png "Figura 8: painel notificações"  
[NotificationsLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications.msft.png "Figura 9: um log de eventos no painel notificações"  
[NotificationsDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-details.msft.png "Figura 10: exibindo os detalhes de um evento no painel notificações"  
[PushEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-empty.msft.png "Figura 11: o painel de mensagens push"  
[PushLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Figura 12: um log de eventos no painel de mensagens push"  
[PushDetails2]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-details.msft.png "Figura 13: exibir os detalhes de um evento no painel de mensagens push"  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Abrir ferramentas para desenvolvedores do Microsoft Edge (Chromium)"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificações | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API push | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "processo em segundo plano-Wikipédia"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
