---
description: Como depurar a Busca em Segundo Plano, Sincronização de Plano de Fundo, Notificações e Enviar Mensagens com Microsoft Edge DevTools.
title: Depurar serviços em segundo plano com Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4f5f52bcde976cea8432e3160a792438e5603e21
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564193"
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
# <a name="debug-background-services-with-microsoft-edge-devtools"></a><span data-ttu-id="92cb8-104">Depurar serviços em segundo plano com Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92cb8-104">Debug Background Services with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="92cb8-105">A seção **Serviços em** Segundo Plano do Microsoft Edge DevTools é uma coleção de ferramentas para as APIs JavaScript que permite que seu site envie e receba atualizações, mesmo quando um usuário não tem seu site aberto.</span><span class="sxs-lookup"><span data-stu-id="92cb8-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="92cb8-106">Um serviço em segundo plano é funcionalmente semelhante a um [processo em segundo plano][WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="92cb8-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="92cb8-107">Microsoft Edge O DevTools considera cada uma das SEGUINTES APIs como um serviço em segundo plano:</span><span class="sxs-lookup"><span data-stu-id="92cb8-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="92cb8-108">Busca de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="92cb8-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="92cb8-109">Sincronização em Segundo Plano</span><span class="sxs-lookup"><span data-stu-id="92cb8-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="92cb8-110">Notificações</span><span class="sxs-lookup"><span data-stu-id="92cb8-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="92cb8-111">Enviar mensagens</span><span class="sxs-lookup"><span data-stu-id="92cb8-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="92cb8-112">Microsoft Edge O DevTools pode registrar eventos de serviço em segundo plano por três dias, mesmo quando o DevTools não estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="92cb8-112">Microsoft Edge DevTools may log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="92cb8-113">O log de eventos do serviço em segundo plano pode ajudá-lo a garantir que os eventos estão sendo enviados e recebidos conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="92cb8-113">The background service events log may help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="92cb8-114">Você também pode inspecionar os detalhes de cada evento.</span><span class="sxs-lookup"><span data-stu-id="92cb8-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="O painel Mensagens por Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="92cb8-116">O **painel Mensagens por** Push</span><span class="sxs-lookup"><span data-stu-id="92cb8-116">The **Push Messaging** pane</span></span>  
:::image-end:::  

## <a name="background-fetch"></a><span data-ttu-id="92cb8-117">Busca de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="92cb8-117">Background Fetch</span></span>  

<span data-ttu-id="92cb8-118">A **API de Busca de Plano** de Fundo permite que um funcionário do serviço baixe com confiança grandes recursos, como filmes ou podcasts, como um serviço em segundo plano. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="92cb8-118">The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="92cb8-119">Para registrar o evento Background Fetch por 3 dias, mesmo quando o DevTools não estiver aberto:</span><span class="sxs-lookup"><span data-stu-id="92cb8-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="92cb8-120">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="92cb8-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="92cb8-121">Abra a **ferramenta Application.**</span><span class="sxs-lookup"><span data-stu-id="92cb8-121">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="92cb8-122">Abra o **painel Busca de** Plano de Fundo.</span><span class="sxs-lookup"><span data-stu-id="92cb8-122">Open the **Background Fetch** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="O painel Busca de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="92cb8-124">O **painel Busca de** Plano de Fundo</span><span class="sxs-lookup"><span data-stu-id="92cb8-124">The **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92cb8-125">Escolha **Registro** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="92cb8-125">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="92cb8-126">Depois de disparar alguma atividade de Busca em Segundo Plano, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="92cb8-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Um log de eventos no painel Busca em Segundo Plano" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="92cb8-128">Um log de eventos no painel **Busca em** Segundo Plano</span><span class="sxs-lookup"><span data-stu-id="92cb8-128">A log of events in the **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92cb8-129">Escolha um evento para exibir seus detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="92cb8-129">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Exibir os detalhes de um evento no painel Busca de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="92cb8-131">Exibir os detalhes de um evento no painel **Busca de** Plano de Fundo</span><span class="sxs-lookup"><span data-stu-id="92cb8-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <a name="background-sync"></a><span data-ttu-id="92cb8-132">Sincronização em Segundo Plano</span><span class="sxs-lookup"><span data-stu-id="92cb8-132">Background Sync</span></span>  

<span data-ttu-id="92cb8-133">A **API de Sincronização** de Plano de Fundo permite que um trabalhador de serviço **offline** envie dados para um servidor depois de estabelecer uma conexão de internet confiável.</span><span class="sxs-lookup"><span data-stu-id="92cb8-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="92cb8-134">Para registrar eventos de Sincronização de Plano de Fundo por 3 dias, mesmo quando o DevTools não estiver aberto:</span><span class="sxs-lookup"><span data-stu-id="92cb8-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="92cb8-135">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="92cb8-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="92cb8-136">Abra a **ferramenta Application.**</span><span class="sxs-lookup"><span data-stu-id="92cb8-136">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="92cb8-137">Abra o **painel Sincronização de** Plano de Fundo.</span><span class="sxs-lookup"><span data-stu-id="92cb8-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="O painel Sincronização de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="92cb8-139">O **painel Sincronização de** Plano de Fundo</span><span class="sxs-lookup"><span data-stu-id="92cb8-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92cb8-140">Escolha **Registro** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="92cb8-140">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="92cb8-141">Depois de disparar alguma atividade de Sincronização em Segundo Plano, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="92cb8-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Um log de eventos no painel Sincronização de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="92cb8-143">Um log de eventos no painel **Sincronização de** Plano de Fundo</span><span class="sxs-lookup"><span data-stu-id="92cb8-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92cb8-144">Escolha um evento para exibir seus detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="92cb8-144">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Exibir os detalhes de um evento no painel Sincronização de Plano de Fundo" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="92cb8-146">Exibir os detalhes de um evento no painel **Sincronização de** Plano de Fundo</span><span class="sxs-lookup"><span data-stu-id="92cb8-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <a name="notifications"></a><span data-ttu-id="92cb8-147">Notificações</span><span class="sxs-lookup"><span data-stu-id="92cb8-147">Notifications</span></span>  

<span data-ttu-id="92cb8-148">Depois que **um funcionário** de serviço recebe uma [Mensagem push][MDNPush] de um servidor, o trabalhador do serviço usa a [API][MDNNotifications] de Notificações para exibir os dados para um usuário.</span><span class="sxs-lookup"><span data-stu-id="92cb8-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="92cb8-149">Para registrar notificações por 3 dias, mesmo quando o DevTools não estiver aberto:</span><span class="sxs-lookup"><span data-stu-id="92cb8-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="92cb8-150">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="92cb8-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="92cb8-151">Abra a **ferramenta Application.**</span><span class="sxs-lookup"><span data-stu-id="92cb8-151">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="92cb8-152">Abra o **painel Notificações.**</span><span class="sxs-lookup"><span data-stu-id="92cb8-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="O painel Notificações" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="92cb8-154">O **painel Notificações**</span><span class="sxs-lookup"><span data-stu-id="92cb8-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92cb8-155">Escolha **Registro** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="92cb8-155">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="92cb8-156">Depois de disparar algumas atividades de Notificações, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="92cb8-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Um log de eventos no painel Notificações" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="92cb8-158">Um log de eventos no painel **Notificações**</span><span class="sxs-lookup"><span data-stu-id="92cb8-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92cb8-159">Escolha um evento para exibir seus detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="92cb8-159">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Exibir os detalhes de um evento no painel Notificações" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="92cb8-161">Exibir os detalhes de um evento no painel **Notificações**</span><span class="sxs-lookup"><span data-stu-id="92cb8-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <a name="push-messages"></a><span data-ttu-id="92cb8-162">Enviar mensagens</span><span class="sxs-lookup"><span data-stu-id="92cb8-162">Push Messages</span></span>  

<span data-ttu-id="92cb8-163">Para exibir uma notificação por push para um usuário, um funcionário do serviço **deve** primeiro usar a API de Mensagem de [Push][MDNPush] para receber dados de um servidor.</span><span class="sxs-lookup"><span data-stu-id="92cb8-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="92cb8-164">Quando o trabalhador do serviço está pronto para exibir a notificação, ele usa a [API de Notificações][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="92cb8-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="92cb8-165">Para registrar mensagens push por 3 dias, mesmo quando o DevTools não estiver aberto:</span><span class="sxs-lookup"><span data-stu-id="92cb8-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="92cb8-166">[Abra DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="92cb8-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="92cb8-167">Abra a **ferramenta Application.**</span><span class="sxs-lookup"><span data-stu-id="92cb8-167">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="92cb8-168">Abra o **painel Mensagens por** Push.</span><span class="sxs-lookup"><span data-stu-id="92cb8-168">Open the **Push Messaging** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Abra o painel Mensagens por Push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="92cb8-170">Abra o **painel Mensagens por** Push</span><span class="sxs-lookup"><span data-stu-id="92cb8-170">Open the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92cb8-171">Escolha **Registro** \( ![ Record ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="92cb8-171">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
    <span data-ttu-id="92cb8-172">Depois de disparar alguma atividade de Mensagem push, o DevTools registra os eventos na tabela.</span><span class="sxs-lookup"><span data-stu-id="92cb8-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Um log de eventos no painel Mensagens por Push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="92cb8-174">Um log de eventos no painel **Mensagens por** Push</span><span class="sxs-lookup"><span data-stu-id="92cb8-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92cb8-175">Escolha um evento para exibir os detalhes no espaço abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="92cb8-175">Choose an event to view the details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Exibir os detalhes de um evento no painel Mensagens por Push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="92cb8-177">Exibir os detalhes de um evento no painel **Mensagens por** Push</span><span class="sxs-lookup"><span data-stu-id="92cb8-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="92cb8-178">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92cb8-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Abra Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Api de notificações | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Push API | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Processo em segundo plano - Wikipédia"  

> [!NOTE]
> <span data-ttu-id="92cb8-183">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92cb8-183">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="92cb8-184">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="92cb8-184">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="92cb8-186">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92cb8-186">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
