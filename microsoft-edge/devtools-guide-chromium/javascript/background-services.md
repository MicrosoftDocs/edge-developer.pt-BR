---
title: Depurar serviços em segundo plano com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1fecd6f9c1dceb39482bf8c4ade71918e32dec00
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983249"
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





# <span data-ttu-id="1cc73-103">Depurar serviços em segundo plano com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1cc73-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="1cc73-104">A seção **serviços em segundo plano** do Microsoft Edge devtools é uma coleção de ferramentas para APIs JavaScript que permite que seu site envie e Receba atualizações mesmo quando um usuário não tem seu site aberto.</span><span class="sxs-lookup"><span data-stu-id="1cc73-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="1cc73-105">Um serviço em segundo plano é funcionalmente semelhante a um [processo em segundo plano] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="1cc73-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="1cc73-106">O Microsoft Edge DevTools considera que cada uma das seguintes APIs seja um serviço em segundo plano:</span><span class="sxs-lookup"><span data-stu-id="1cc73-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="1cc73-107">Busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1cc73-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="1cc73-108">Sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1cc73-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="1cc73-109">Notificações</span><span class="sxs-lookup"><span data-stu-id="1cc73-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="1cc73-110">Enviar mensagens por push</span><span class="sxs-lookup"><span data-stu-id="1cc73-110">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="1cc73-111">O Microsoft Edge DevTools pode registrar eventos de serviço em segundo plano por 3 dias, mesmo quando DevTools não está aberto.</span><span class="sxs-lookup"><span data-stu-id="1cc73-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="1cc73-112">Isso pode ajudá-lo a garantir que os eventos sejam enviados e recebidos como esperado.</span><span class="sxs-lookup"><span data-stu-id="1cc73-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="1cc73-113">Você também pode inspecionar os detalhes de cada evento.</span><span class="sxs-lookup"><span data-stu-id="1cc73-113">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Exibir os detalhes de um evento no painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="1cc73-115">Exibir os detalhes de um evento no painel de **mensagens Push**</span><span class="sxs-lookup"><span data-stu-id="1cc73-115">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="1cc73-116">Busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1cc73-116">Background Fetch</span></span>   

<span data-ttu-id="1cc73-117">A *API de busca em segundo plano*\* permite que um **trabalhador de serviço** Baixe recursos grandes, como filmes ou podcasts, como um serviço em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1cc73-117">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="1cc73-118">Para registrar o evento de busca em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="1cc73-118">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="1cc73-119">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="1cc73-119">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="1cc73-120">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="1cc73-120">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="1cc73-121">Abrir o painel **busca em segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="1cc73-121">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="O painel busca em segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="1cc73-123">O painel **busca em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="1cc73-123">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cc73-124">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="1cc73-124">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="1cc73-125">Depois de disparar uma atividade de busca em segundo plano, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="1cc73-125">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Um log de eventos no painel de busca em segundo plano" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="1cc73-127">Um log de eventos no painel de **busca em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="1cc73-127">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cc73-128">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="1cc73-128">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Exibir os detalhes de um evento no painel de busca em segundo plano" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="1cc73-130">Exibir os detalhes de um evento no painel de **busca em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="1cc73-130">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1cc73-131">Sincronização em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1cc73-131">Background Sync</span></span>   

<span data-ttu-id="1cc73-132">A **API de sincronização em segundo plano** permite que um **trabalhador de serviço** offline envie dados para um servidor depois que ele restabeleceu uma conexão com a Internet confiável.</span><span class="sxs-lookup"><span data-stu-id="1cc73-132">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="1cc73-133">Para registrar eventos de sincronização em segundo plano por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="1cc73-133">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="1cc73-134">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="1cc73-134">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="1cc73-135">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="1cc73-135">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="1cc73-136">Abrir o painel **sincronização em segundo plano** .</span><span class="sxs-lookup"><span data-stu-id="1cc73-136">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="O painel sincronização em segundo plano" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="1cc73-138">O painel **sincronização em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="1cc73-138">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cc73-139">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="1cc73-139">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="1cc73-140">Depois de disparar uma atividade de sincronização em segundo plano, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="1cc73-140">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Um log de eventos no painel sincronização em segundo plano" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="1cc73-142">Um log de eventos no painel **sincronização em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="1cc73-142">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cc73-143">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="1cc73-143">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Exibir os detalhes de um evento no painel sincronização em segundo plano" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="1cc73-145">Exibir os detalhes de um evento no painel **sincronização em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="1cc73-145">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1cc73-146">Notificações</span><span class="sxs-lookup"><span data-stu-id="1cc73-146">Notifications</span></span> 

<span data-ttu-id="1cc73-147">Depois que um **trabalhador do serviço** recebeu uma mensagem de [envio][MDNPush] de um servidor, o trabalhador do serviço usa a API de [notificações][MDNNotifications] para exibir os dados para um usuário.</span><span class="sxs-lookup"><span data-stu-id="1cc73-147">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="1cc73-148">Para registrar notificações por três dias, mesmo quando o DevTools não estiver aberto:</span><span class="sxs-lookup"><span data-stu-id="1cc73-148">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="1cc73-149">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="1cc73-149">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="1cc73-150">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="1cc73-150">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="1cc73-151">Abrir o painel **notificações** .</span><span class="sxs-lookup"><span data-stu-id="1cc73-151">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="O painel notificações" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="1cc73-153">O painel **notificações**</span><span class="sxs-lookup"><span data-stu-id="1cc73-153">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cc73-154">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="1cc73-154">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="1cc73-155">Depois de disparar algumas atividades de notificações, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="1cc73-155">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Um log de eventos no painel notificações" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="1cc73-157">Um log de eventos no painel **notificações**</span><span class="sxs-lookup"><span data-stu-id="1cc73-157">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cc73-158">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="1cc73-158">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Exibir os detalhes de um evento no painel notificações" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="1cc73-160">Exibir os detalhes de um evento no painel **notificações**</span><span class="sxs-lookup"><span data-stu-id="1cc73-160">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1cc73-161">Enviar mensagens por push</span><span class="sxs-lookup"><span data-stu-id="1cc73-161">Push Messages</span></span> 

<span data-ttu-id="1cc73-162">Para exibir uma notificação por push para um usuário, um **trabalhador de serviço** deve primeiro usar a API de [mensagem Push][MDNPush] para receber dados de um servidor.</span><span class="sxs-lookup"><span data-stu-id="1cc73-162">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="1cc73-163">Quando o trabalhador do serviço está pronto para exibir a notificação, ele usa a [API de notificações][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="1cc73-163">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="1cc73-164">Para registrar mensagens por Push por 3 dias, mesmo quando o DevTools não está aberto:</span><span class="sxs-lookup"><span data-stu-id="1cc73-164">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="1cc73-165">[Abra o devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="1cc73-165">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="1cc73-166">Abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="1cc73-166">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="1cc73-167">Abrir o painel de **mensagens Push** .</span><span class="sxs-lookup"><span data-stu-id="1cc73-167">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="O painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="1cc73-169">O painel de **mensagens Push**</span><span class="sxs-lookup"><span data-stu-id="1cc73-169">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cc73-170">Clique em **gravar** \ ( ![ registro ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="1cc73-170">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="1cc73-171">Depois de disparar uma atividade de mensagem por push, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="1cc73-171">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Um log de eventos no painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="1cc73-173">Um log de eventos no painel de **mensagens Push**</span><span class="sxs-lookup"><span data-stu-id="1cc73-173">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cc73-174">Clique em um evento para ver os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="1cc73-174">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Exibir os detalhes de um evento no painel de mensagens push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="1cc73-176">Exibir os detalhes de um evento no painel de **mensagens Push**</span><span class="sxs-lookup"><span data-stu-id="1cc73-176">View the details of an event in the **Push Messaging** pane</span></span>  
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
> <span data-ttu-id="1cc73-181">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="1cc73-181">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1cc73-182">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1cc73-182">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1cc73-184">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1cc73-184">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
