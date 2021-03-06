---
description: Como depurar a Busca de Plano de Fundo, Sincronização em Segundo Plano, Notificações e Enviar Mensagens com o Microsoft Edge DevTools.
title: Depurar serviços em segundo plano com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: cf3459e7b5f80a695a855ffdd0c249c2bc223d31
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398634"
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

# <a name="debug-background-services-with-microsoft-edge-devtools"></a>Depurar serviços em segundo plano com o Microsoft Edge DevTools  

A seção **Serviços em** Segundo Plano do Microsoft Edge DevTools é uma coleção de ferramentas para as APIs JavaScript que permite que seu site envie e receba atualizações, mesmo quando um usuário não tem seu site aberto.  
Um serviço em segundo plano é funcionalmente semelhante a um [processo em segundo plano][WikiBackgroundProcess].  
O Microsoft Edge DevTools considera cada uma das SEGUINTES APIs como um serviço em segundo plano:  

*   [Busca de plano de fundo](#background-fetch)  
*   [Sincronização em Segundo Plano](#background-sync)  
*   [Notificações](#notifications)  
*   [Enviar mensagens](#push-messages)  
    
O Microsoft Edge DevTools pode registrar eventos de serviço em segundo plano por 3 dias, mesmo quando o DevTools não estiver aberto.  
O log de eventos do serviço em segundo plano pode ajudá-lo a garantir que os eventos estão sendo enviados e recebidos conforme o esperado.  Você também pode inspecionar os detalhes de cada evento.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="O painel Mensagens por Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   O **painel Mensagens por** Push  
:::image-end:::  

## <a name="background-fetch"></a>Busca de plano de fundo  

A **API de Busca de Plano** de Fundo permite que um funcionário do serviço baixe com confiança grandes recursos, como filmes ou podcasts, como um serviço em segundo plano. ****  Para registrar o evento Background Fetch por 3 dias, mesmo quando o DevTools não estiver aberto:  

<!--Todo: add background fetch api section when available -->  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra a **ferramenta Application.**  
1.  Abra o **painel Busca de** Plano de Fundo.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="O painel Busca de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       O **painel Busca de** Plano de Fundo  
    :::image-end:::  
    
1.  Escolha **Registro** \( ![ Record ][ImageRecordIcon] \).  
   Depois de disparar alguma atividade de Busca em Segundo Plano, o DevTools registra os eventos na tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Um log de eventos no painel Busca em Segundo Plano" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Um log de eventos no painel **Busca em** Segundo Plano  
    :::image-end:::  
    
1.  Escolha um evento para exibir seus detalhes no espaço abaixo da tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Exibir os detalhes de um evento no painel Busca de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Exibir os detalhes de um evento no painel **Busca de** Plano de Fundo  
    :::image-end:::  
    
## <a name="background-sync"></a>Sincronização em Segundo Plano  

A **API de Sincronização** de Plano de Fundo permite que um trabalhador de serviço **offline** envie dados para um servidor depois de estabelecer uma conexão de internet confiável.  Para registrar eventos de Sincronização de Plano de Fundo por 3 dias, mesmo quando o DevTools não estiver aberto:  

<!--Todo: add background sync api section when available -->  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra a **ferramenta Application.**  
1.  Abra o **painel Sincronização de** Plano de Fundo.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="O painel Sincronização de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       O **painel Sincronização de** Plano de Fundo  
    :::image-end:::  
    
1.  Escolha **Registro** \( ![ Record ][ImageRecordIcon] \).  
   Depois de disparar alguma atividade de Sincronização em Segundo Plano, o DevTools registra os eventos na tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Um log de eventos no painel Sincronização de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Um log de eventos no painel **Sincronização de** Plano de Fundo  
    :::image-end:::  
    
1.  Escolha um evento para exibir seus detalhes no espaço abaixo da tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Exibir os detalhes de um evento no painel Sincronização de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Exibir os detalhes de um evento no painel **Sincronização de** Plano de Fundo  
    :::image-end:::  
    
## <a name="notifications"></a>Notificações  

Depois que **um funcionário** de serviço recebe uma [Mensagem push][MDNPush] de um servidor, o trabalhador do serviço usa a [API][MDNNotifications] de Notificações para exibir os dados para um usuário.  Para registrar notificações por 3 dias, mesmo quando o DevTools não estiver aberto:  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra a **ferramenta Application.**  
1.  Abra o **painel Notificações.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="O painel Notificações" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       O **painel Notificações**  
    :::image-end:::  
    
1.  Escolha **Registro** \( ![ Record ][ImageRecordIcon] \).  
   Depois de disparar algumas atividades de Notificações, o DevTools registra os eventos na tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Um log de eventos no painel Notificações" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Um log de eventos no painel **Notificações**  
    :::image-end:::  
    
1.  Escolha um evento para exibir seus detalhes no espaço abaixo da tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Exibir os detalhes de um evento no painel Notificações" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Exibir os detalhes de um evento no painel **Notificações**  
    :::image-end:::  
    
## <a name="push-messages"></a>Enviar mensagens  

Para exibir uma notificação por push para um usuário, um funcionário do serviço **deve** primeiro usar a API de Mensagem de [Push][MDNPush] para receber dados de um servidor.  Quando o trabalhador do serviço está pronto para exibir a notificação, ele usa a [API de Notificações][MDNNotifications].  Para registrar mensagens push por 3 dias, mesmo quando o DevTools não estiver aberto:  

1.  [Abra DevTools][OpenDevTools].  
1.  Abra a **ferramenta Application.**  
1.  Abra o **painel Mensagens por** Push.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Abra o painel Mensagens por Push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Abra o **painel Mensagens por** Push  
    :::image-end:::  
    
1.  Escolha **Registro** \( ![ Record ][ImageRecordIcon] \).  
    Depois de disparar alguma atividade de Mensagem push, o DevTools registra os eventos na tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Um log de eventos no painel Mensagens por Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Um log de eventos no painel **Mensagens por** Push  
    :::image-end:::  
    
1.  Escolha um evento para exibir os detalhes no espaço abaixo da tabela.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Exibir os detalhes de um evento no painel Mensagens por Push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Exibir os detalhes de um evento no painel **Mensagens por** Push  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Abra as Ferramentas de Desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Api de notificações | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Push API | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Processo em segundo plano - Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
