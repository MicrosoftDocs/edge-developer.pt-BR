---
description: Como depurar a busca em segundo plano, sincronização em segundo plano, notificações e mensagens Push com o Microsoft Edge DevTools.
title: Depurar serviços em segundo plano com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1724bd3a5e45734555650c3d46e377161a3a7c65
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992866"
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





# <span data-ttu-id="c4f3f-104">Depurar serviços em segundo plano com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c4f3f-104">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c4f3f-105">A seção **serviços em segundo plano** do Microsoft Edge devtools é uma coleção de ferramentas para APIs JavaScript que permite que seu site envie e Receba atualizações mesmo quando um usuário não tem seu site aberto.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="c4f3f-106">Um serviço em segundo plano é funcionalmente semelhante a um [processo em segundo plano] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="c4f3f-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="c4f3f-107">O Microsoft Edge DevTools considera que cada uma das seguintes APIs seja um serviço em segundo plano:</span><span class="sxs-lookup"><span data-stu-id="c4f3f-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="c4f3f-108">Busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c4f3f-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="c4f3f-109">Sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c4f3f-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="c4f3f-110">Notificações</span><span class="sxs-lookup"><span data-stu-id="c4f3f-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="c4f3f-111">Enviar mensagens por push</span><span class="sxs-lookup"><span data-stu-id="c4f3f-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="c4f3f-112">O Microsoft Edge DevTools pode registrar eventos de serviço em segundo plano por 3 dias, mesmo quando DevTools não está aberto.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-112">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="c4f3f-113">Isso pode ajudá-lo a garantir que os eventos sejam enviados e recebidos como esperado.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-113">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="c4f3f-114">Você também pode inspecionar os detalhes de cada evento.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Exibir os detalhes de um evento no painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="c4f3f-116">Exibir os detalhes de um evento no painel de **mensagens Push**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-116">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="c4f3f-117">Busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c4f3f-117">Background Fetch</span></span>   

<span data-ttu-id="c4f3f-118">A *API de busca em segundo plano*\* permite que um **trabalhador de serviço** Baixe recursos grandes, como filmes ou podcasts, como um serviço em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="c4f3f-119">Para registrar o evento de busca em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="c4f3f-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="c4f3f-120">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c4f3f-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c4f3f-121">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="c4f3f-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c4f3f-122">Abrir o painel **busca em segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="c4f3f-122">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="O painel busca em segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="c4f3f-124">O painel **busca em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-124">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c4f3f-125">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c4f3f-125">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c4f3f-126">Depois de disparar uma atividade de busca em segundo plano, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Um log de eventos no painel de busca em segundo plano" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="c4f3f-128">Um log de eventos no painel de **busca em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-128">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c4f3f-129">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-129">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Exibir os detalhes de um evento no painel de busca em segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="c4f3f-131">Exibir os detalhes de um evento no painel de **busca em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c4f3f-132">Sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c4f3f-132">Background Sync</span></span>   

<span data-ttu-id="c4f3f-133">A **API de sincronização em segundo plano** permite que um **trabalhador de serviço** offline envie dados para um servidor depois que ele restabeleceu uma conexão com a Internet confiável.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="c4f3f-134">Para registrar eventos de sincronização em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="c4f3f-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="c4f3f-135">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c4f3f-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c4f3f-136">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="c4f3f-136">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c4f3f-137">Abrir o painel **sincronização em segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="c4f3f-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="O painel sincronização em segundo plano" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="c4f3f-139">O painel **sincronização em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c4f3f-140">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c4f3f-140">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c4f3f-141">Depois de disparar uma atividade de sincronização em segundo plano, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Um log de eventos no painel sincronização em segundo plano" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="c4f3f-143">Um log de eventos no painel **sincronização em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c4f3f-144">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-144">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Exibir os detalhes de um evento no painel sincronização em segundo plano" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="c4f3f-146">Exibir os detalhes de um evento no painel **sincronização em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c4f3f-147">Notificações</span><span class="sxs-lookup"><span data-stu-id="c4f3f-147">Notifications</span></span> 

<span data-ttu-id="c4f3f-148">Depois que um **trabalhador do serviço** recebeu uma mensagem de [envio][MDNPush] de um servidor, o trabalhador do serviço usa a API de [notificações][MDNNotifications] para exibir os dados para um usuário.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="c4f3f-149">Para registrar notificações por três dias, mesmo quando o DevTools não estiver aberto:</span><span class="sxs-lookup"><span data-stu-id="c4f3f-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="c4f3f-150">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c4f3f-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c4f3f-151">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="c4f3f-151">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c4f3f-152">Abrir o painel **notificações** .</span><span class="sxs-lookup"><span data-stu-id="c4f3f-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="O painel notificações" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="c4f3f-154">O painel **notificações**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c4f3f-155">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c4f3f-155">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c4f3f-156">Depois de disparar algumas atividades de notificações, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Um log de eventos no painel notificações" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="c4f3f-158">Um log de eventos no painel **notificações**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c4f3f-159">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-159">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Exibir os detalhes de um evento no painel notificações" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="c4f3f-161">Exibir os detalhes de um evento no painel **notificações**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c4f3f-162">Enviar mensagens por push</span><span class="sxs-lookup"><span data-stu-id="c4f3f-162">Push Messages</span></span> 

<span data-ttu-id="c4f3f-163">Para exibir uma notificação por push para um usuário, um **trabalhador de serviço** deve primeiro usar a API de [mensagem Push][MDNPush] para receber dados de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="c4f3f-164">Quando o trabalhador do serviço está pronto para exibir a notificação, ele usa a [API de notificações][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="c4f3f-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="c4f3f-165">Para registrar mensagens por Push por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="c4f3f-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="c4f3f-166">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c4f3f-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c4f3f-167">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="c4f3f-167">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c4f3f-168">Abrir o painel de **mensagens Push** .</span><span class="sxs-lookup"><span data-stu-id="c4f3f-168">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="c4f3f-170">O painel de **mensagens Push**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-170">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c4f3f-171">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c4f3f-171">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="c4f3f-172">Depois de disparar uma atividade de mensagem por push, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Um log de eventos no painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="c4f3f-174">Um log de eventos no painel de **mensagens Push**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c4f3f-175">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-175">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Exibir os detalhes de um evento no painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="c4f3f-177">Exibir os detalhes de um evento no painel de **mensagens Push**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

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
> <span data-ttu-id="c4f3f-182">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="c4f3f-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c4f3f-183">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c4f3f-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c4f3f-185">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c4f3f-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
