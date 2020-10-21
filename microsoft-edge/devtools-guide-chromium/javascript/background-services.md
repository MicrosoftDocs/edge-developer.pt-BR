---
description: Como depurar a busca em segundo plano, sincronização em segundo plano, notificações e mensagens Push com o Microsoft Edge DevTools.
title: Depurar serviços em segundo plano com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: fb5e408eb261ae3b2145780a1d7d5566c4501936
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124814"
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

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   O painel de **mensagens Push**  
:::image-end:::  

## Busca em segundo plano  

A **API de busca em segundo plano** permite que um **trabalhador de serviço** Baixe com confiança recursos grandes, como filmes ou podcasts, como um serviço em segundo plano.  Para registrar o evento de busca em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:  

<!--Todo: add background fetch api section when available -->  

1.  [Abra o devtools][OpenDevTools].  
1.  Abrir o painel do **aplicativo** .  
1.  Abrir o painel **busca em segundo plano** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       O painel **busca em segundo plano**  
    :::image-end:::  
    
1.  Escolha **registro** \ ( ![ registro ][ImageRecordIcon] \).  
   Depois de disparar uma atividade de busca em segundo plano, o DevTools registra os eventos na tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Um log de eventos no painel de **busca em segundo plano**  
    :::image-end:::  
    
1.  Clique em um evento para ver os detalhes no espaço abaixo da tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Exibir os detalhes de um evento no painel de **busca em segundo plano**  
    :::image-end:::  
    
## Sincronização em segundo plano  

A **API de sincronização em segundo plano** permite que um **trabalhador de serviço** offline envie dados para um servidor depois que ele restabeleceu uma conexão com a Internet confiável.  Para registrar eventos de sincronização em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:  

<!--Todo: add background sync api section when available -->  

1.  [Abra o devtools][OpenDevTools].  
1.  Abrir o painel do **aplicativo** .  
1.  Abrir o painel **sincronização em segundo plano** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       O painel **sincronização em segundo plano**  
    :::image-end:::  
    
1.  Escolha **registro** \ ( ![ registro ][ImageRecordIcon] \).  
   Depois de disparar uma atividade de sincronização em segundo plano, o DevTools registra os eventos na tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Um log de eventos no painel **sincronização em segundo plano**  
    :::image-end:::  
    
1.  Clique em um evento para ver os detalhes no espaço abaixo da tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Exibir os detalhes de um evento no painel **sincronização em segundo plano**  
    :::image-end:::  
    
## Notificações  

Depois que um **trabalhador do serviço** recebeu uma mensagem de [envio][MDNPush] de um servidor, o trabalhador do serviço usa a API de [notificações][MDNNotifications] para exibir os dados para um usuário.  Para registrar notificações por três dias, mesmo quando o DevTools não estiver aberto:  

1.  [Abra o devtools][OpenDevTools].  
1.  Abrir o painel do **aplicativo** .  
1.  Abrir o painel **notificações** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       O painel **notificações**  
    :::image-end:::  
    
1.  Escolha **registro** \ ( ![ registro ][ImageRecordIcon] \).  
   Depois de disparar algumas atividades de notificações, o DevTools registra os eventos na tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Um log de eventos no painel **notificações**  
    :::image-end:::  
    
1.  Clique em um evento para ver os detalhes no espaço abaixo da tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Exibir os detalhes de um evento no painel **notificações**  
    :::image-end:::  
    
## Enviar mensagens por push  

Para exibir uma notificação por push para um usuário, um **trabalhador de serviço** deve primeiro usar a API de [mensagem Push][MDNPush] para receber dados de um servidor.  Quando o trabalhador do serviço está pronto para exibir a notificação, ele usa a [API de notificações][MDNNotifications].  Para registrar mensagens por Push por 3 dias, mesmo quando o DevTools não está aberto:  

1.  [Abra o devtools][OpenDevTools].  
1.  Abrir o painel do **aplicativo** .  
1.  Abrir o painel de **mensagens Push** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Abrir o painel de **mensagens Push**  
    :::image-end:::  
    
1.  Escolha **registro** \ ( ![ registro ][ImageRecordIcon] \).  
    Depois de disparar uma atividade de mensagem por push, o DevTools registra os eventos na tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Um log de eventos no painel de **mensagens Push**  
    :::image-end:::  
    
1.  Clique em um evento para ver os detalhes no espaço abaixo da tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Exibir os detalhes de um evento no painel de **mensagens Push**  
    :::image-end:::  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Abrir as ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

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
