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





# <span data-ttu-id="74ee2-103">Depurar serviços em segundo plano com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="74ee2-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="74ee2-104">A seção **serviços em segundo plano** do Microsoft Edge devtools é uma coleção de ferramentas para APIs JavaScript que permite que seu site envie e Receba atualizações mesmo quando um usuário não tem seu site aberto.</span><span class="sxs-lookup"><span data-stu-id="74ee2-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="74ee2-105">Um serviço em segundo plano é funcionalmente semelhante a um [processo em segundo plano] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="74ee2-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="74ee2-106">O Microsoft Edge DevTools considera que cada uma das seguintes APIs seja um serviço em segundo plano:</span><span class="sxs-lookup"><span data-stu-id="74ee2-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="74ee2-107">Busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="74ee2-108">Sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="74ee2-109">Notificações</span><span class="sxs-lookup"><span data-stu-id="74ee2-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="74ee2-110">Enviar mensagens por push</span><span class="sxs-lookup"><span data-stu-id="74ee2-110">Push Messages</span></span>](#push-messages)  

<span data-ttu-id="74ee2-111">O Microsoft Edge DevTools pode registrar eventos de serviço em segundo plano por 3 dias, mesmo quando DevTools não está aberto.</span><span class="sxs-lookup"><span data-stu-id="74ee2-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="74ee2-112">Isso pode ajudá-lo a garantir que os eventos sejam enviados e recebidos como esperado.</span><span class="sxs-lookup"><span data-stu-id="74ee2-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="74ee2-113">Você também pode inspecionar os detalhes de cada evento.</span><span class="sxs-lookup"><span data-stu-id="74ee2-113">You can also inspect the details of each event.</span></span>  

> ##### <span data-ttu-id="74ee2-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="74ee2-114">Figure 1</span></span>  
> <span data-ttu-id="74ee2-115">Exibir os detalhes de um evento no painel de mensagens push</span><span class="sxs-lookup"><span data-stu-id="74ee2-115">Viewing the details of an event in the Push Messaging pane</span></span>  
> ![Exibir os detalhes de um evento no painel de mensagens push][PushDetails]  

## <span data-ttu-id="74ee2-117">Busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-117">Background Fetch</span></span>   

<span data-ttu-id="74ee2-118">A *API de busca em segundo plano*\* permite que um **trabalhador de serviço** Baixe recursos grandes, como filmes ou podcasts, como um serviço em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="74ee2-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="74ee2-119">Para registrar o evento de busca em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="74ee2-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="74ee2-120">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="74ee2-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="74ee2-121">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="74ee2-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="74ee2-122">Abrir o painel **busca em segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="74ee2-122">Open the **Background Fetch** pane.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="74ee2-123">Figure 2</span></span>  
    > <span data-ttu-id="74ee2-124">O painel busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-124">The Background Fetch pane</span></span>  
    > ![O painel busca em segundo plano][FetchEmpty]  
    
1.  <span data-ttu-id="74ee2-126">Clique em **gravar** ![ registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="74ee2-126">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="74ee2-127">Depois de disparar uma atividade de busca em segundo plano, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="74ee2-127">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-128">Figura 3</span><span class="sxs-lookup"><span data-stu-id="74ee2-128">Figure 3</span></span>  
    > <span data-ttu-id="74ee2-129">Um log de eventos no painel de busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-129">A log of events in the Background Fetch pane</span></span>  
    > ![Um log de eventos no painel de busca em segundo plano][FetchLog]  
    
1.  <span data-ttu-id="74ee2-131">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="74ee2-131">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-132">Figura 4</span><span class="sxs-lookup"><span data-stu-id="74ee2-132">Figure 4</span></span>  
    > <span data-ttu-id="74ee2-133">Exibir os detalhes de um evento no painel de busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-133">Viewing the details of an event in the Background Fetch pane</span></span>  
    > ![Exibir os detalhes de um evento no painel de busca em segundo plano][FetchDetails]  

## <span data-ttu-id="74ee2-135">Sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-135">Background Sync</span></span>   

<span data-ttu-id="74ee2-136">A **API de sincronização em segundo plano** permite que um **trabalhador de serviço** offline envie dados para um servidor depois que ele restabeleceu uma conexão com a Internet confiável.</span><span class="sxs-lookup"><span data-stu-id="74ee2-136">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="74ee2-137">Para registrar eventos de sincronização em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="74ee2-137">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="74ee2-138">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="74ee2-138">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="74ee2-139">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="74ee2-139">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="74ee2-140">Abrir o painel **sincronização em segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="74ee2-140">Open the **Background Sync** pane.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-141">Figura 5</span><span class="sxs-lookup"><span data-stu-id="74ee2-141">Figure 5</span></span>  
    > <span data-ttu-id="74ee2-142">O painel sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-142">The Background Sync pane</span></span>  
    > ![O painel sincronização em segundo plano][SyncEmpty]  
    
1.  <span data-ttu-id="74ee2-144">Clique em **gravar** ![ registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="74ee2-144">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="74ee2-145">Depois de disparar uma atividade de sincronização em segundo plano, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="74ee2-145">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-146">Figura 6</span><span class="sxs-lookup"><span data-stu-id="74ee2-146">Figure 6</span></span>  
    > <span data-ttu-id="74ee2-147">Um log de eventos no painel sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-147">A log of events in the Background Sync pane</span></span>  
    > ![Um log de eventos no painel sincronização em segundo plano][SyncLog]  
    
1.  <span data-ttu-id="74ee2-149">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="74ee2-149">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-150">Figura 7</span><span class="sxs-lookup"><span data-stu-id="74ee2-150">Figure 7</span></span>  
    > <span data-ttu-id="74ee2-151">Exibir os detalhes de um evento no painel sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74ee2-151">Viewing the details of an event in the Background Sync pane</span></span>  
    > ![Exibir os detalhes de um evento no painel sincronização em segundo plano][SyncDetails]  
    
## <span data-ttu-id="74ee2-153">Notificações</span><span class="sxs-lookup"><span data-stu-id="74ee2-153">Notifications</span></span> 

<span data-ttu-id="74ee2-154">Depois que um **trabalhador do serviço** recebeu uma mensagem de [envio][MDNPush] de um servidor, o trabalhador do serviço usa a API de [notificações][MDNNotifications] para exibir os dados para um usuário.</span><span class="sxs-lookup"><span data-stu-id="74ee2-154">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="74ee2-155">Para registrar notificações por três dias, mesmo quando o DevTools não estiver aberto:</span><span class="sxs-lookup"><span data-stu-id="74ee2-155">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="74ee2-156">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="74ee2-156">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="74ee2-157">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="74ee2-157">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="74ee2-158">Abrir o painel **notificações** .</span><span class="sxs-lookup"><span data-stu-id="74ee2-158">Open the **Notifications** pane.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-159">Figura 8</span><span class="sxs-lookup"><span data-stu-id="74ee2-159">Figure 8</span></span>  
    > <span data-ttu-id="74ee2-160">O painel notificações</span><span class="sxs-lookup"><span data-stu-id="74ee2-160">The Notifications pane</span></span>  
    > ![O painel notificações][NotificationsEmpty]  
    
1.  <span data-ttu-id="74ee2-162">Clique em **gravar** ![ registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="74ee2-162">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="74ee2-163">Depois de disparar algumas atividades de notificações, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="74ee2-163">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-164">Figura 9</span><span class="sxs-lookup"><span data-stu-id="74ee2-164">Figure 9</span></span>  
    > <span data-ttu-id="74ee2-165">Um log de eventos no painel notificações</span><span class="sxs-lookup"><span data-stu-id="74ee2-165">A log of events in the Notifications pane</span></span>  
    > ![Um log de eventos no painel notificações][NotificationsLog]  
    
1.  <span data-ttu-id="74ee2-167">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="74ee2-167">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-168">Figura 10</span><span class="sxs-lookup"><span data-stu-id="74ee2-168">Figure 10</span></span>  
    > <span data-ttu-id="74ee2-169">Exibir os detalhes de um evento no painel notificações</span><span class="sxs-lookup"><span data-stu-id="74ee2-169">Viewing the details of an event in the Notifications pane</span></span>  
    > ![Exibir os detalhes de um evento no painel notificações][NotificationsDetails]  
    
## <span data-ttu-id="74ee2-171">Enviar mensagens por push</span><span class="sxs-lookup"><span data-stu-id="74ee2-171">Push Messages</span></span> 

<span data-ttu-id="74ee2-172">Para exibir uma notificação por push para um usuário, um **trabalhador de serviço** deve primeiro usar a API de [mensagem Push][MDNPush] para receber dados de um servidor.</span><span class="sxs-lookup"><span data-stu-id="74ee2-172">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="74ee2-173">Quando o trabalhador do serviço está pronto para exibir a notificação, ele usa a [API de notificações][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="74ee2-173">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="74ee2-174">Para registrar mensagens por Push por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="74ee2-174">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="74ee2-175">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="74ee2-175">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="74ee2-176">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="74ee2-176">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="74ee2-177">Abrir o painel de **mensagens Push** .</span><span class="sxs-lookup"><span data-stu-id="74ee2-177">Open the **Push Messaging** pane.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-178">Figura 11</span><span class="sxs-lookup"><span data-stu-id="74ee2-178">Figure 11</span></span>  
    > <span data-ttu-id="74ee2-179">O painel de mensagens push</span><span class="sxs-lookup"><span data-stu-id="74ee2-179">The Push Messaging pane</span></span>  
    > ![O painel de mensagens push][PushEmpty]  

1.  <span data-ttu-id="74ee2-181">Clique em **gravar** ![ registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="74ee2-181">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="74ee2-182">Depois de disparar uma atividade de mensagem por push, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="74ee2-182">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-183">Figura 12</span><span class="sxs-lookup"><span data-stu-id="74ee2-183">Figure 12</span></span>  
    > <span data-ttu-id="74ee2-184">Um log de eventos no painel de mensagens push</span><span class="sxs-lookup"><span data-stu-id="74ee2-184">A log of events in the Push Messaging pane</span></span>  
    > ![Um log de eventos no painel de mensagens push][PushLog]  

1.  <span data-ttu-id="74ee2-186">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="74ee2-186">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="74ee2-187">Figura 13</span><span class="sxs-lookup"><span data-stu-id="74ee2-187">Figure 13</span></span>  
    > <span data-ttu-id="74ee2-188">Exibir os detalhes de um evento no painel de mensagens push</span><span class="sxs-lookup"><span data-stu-id="74ee2-188">Viewing the details of an event in the Push Messaging pane</span></span>  
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
> <span data-ttu-id="74ee2-207">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="74ee2-207">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="74ee2-208">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="74ee2-208">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="74ee2-210">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="74ee2-210">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
