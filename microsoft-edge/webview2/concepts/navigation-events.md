---
description: Navegação
title: Navegação
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314794"
---
# <span data-ttu-id="8ee32-104">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="8ee32-104">Navigation events</span></span>  

<span data-ttu-id="8ee32-105">A sequência normal de eventos de navegação `NavigationStarting` `SourceChanged` é , `ContentLoading` `HistoryChanged` e, em seguida `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="8ee32-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="8ee32-106">Os eventos a seguir descrevem o estado de WebView2 durante cada navegação.</span><span class="sxs-lookup"><span data-stu-id="8ee32-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="8ee32-107">Sequence</span><span class="sxs-lookup"><span data-stu-id="8ee32-107">Sequence</span></span> | <span data-ttu-id="8ee32-108">Nome do evento</span><span class="sxs-lookup"><span data-stu-id="8ee32-108">Event name</span></span> | <span data-ttu-id="8ee32-109">Detalhes</span><span class="sxs-lookup"><span data-stu-id="8ee32-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8ee32-110">1</span><span class="sxs-lookup"><span data-stu-id="8ee32-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="8ee32-111">WebView2 começa a navegar e os resultados de navegação em uma solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="8ee32-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="8ee32-112">O host é capaz de não permitir a solicitação durante o evento.</span><span class="sxs-lookup"><span data-stu-id="8ee32-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="8ee32-113">2</span><span class="sxs-lookup"><span data-stu-id="8ee32-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="8ee32-114">A origem de WebView2 muda para uma nova URL.</span><span class="sxs-lookup"><span data-stu-id="8ee32-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="8ee32-115">O evento pode resultar de uma navegação que não causa uma solicitação de rede, como uma navegação de fragmento.</span><span class="sxs-lookup"><span data-stu-id="8ee32-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="8ee32-116">3</span><span class="sxs-lookup"><span data-stu-id="8ee32-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="8ee32-117">O histórico de atualizações de WebView2 como resultado da navegação.</span><span class="sxs-lookup"><span data-stu-id="8ee32-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="8ee32-118">4</span><span class="sxs-lookup"><span data-stu-id="8ee32-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="8ee32-119">WebView2 começa a carregar conteúdo para a nova página.</span><span class="sxs-lookup"><span data-stu-id="8ee32-119">WebView2 starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="8ee32-120">5</span><span class="sxs-lookup"><span data-stu-id="8ee32-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="8ee32-121">WebView2 conclui o carregamento de conteúdo na nova página.</span><span class="sxs-lookup"><span data-stu-id="8ee32-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="8ee32-122">Acompanhe `navigations` cada novo documento usando a ID de navegação \( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="8ee32-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="8ee32-123">O `NavigationId` WebView muda sempre que há uma navegação bem-sucedida para um novo documento.</span><span class="sxs-lookup"><span data-stu-id="8ee32-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="Os eventos de navegação do Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="8ee32-125">Eventos de navegação do Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="8ee32-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8ee32-126">A figura anterior representa eventos de navegação com a mesma `NavigationId` propriedade no respectivo arg de evento.</span><span class="sxs-lookup"><span data-stu-id="8ee32-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="8ee32-127">com instâncias diferentes de `NavigationId` evento podem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="8ee32-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="8ee32-128">Por exemplo, quando você inicia uma navegação, precisa aguardar o evento `NavigationStarting` relacionado.</span><span class="sxs-lookup"><span data-stu-id="8ee32-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="8ee32-129">Se você iniciar outra navegação, deverá ver o evento da primeira navegação seguido do evento para a segunda navegação, seguido do evento para a primeira navegação e, em seguida, todos os outros eventos de navegação apropriados para a segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegação.</span><span class="sxs-lookup"><span data-stu-id="8ee32-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="8ee32-130">Em casos de erro, pode haver ou não um evento, dependendo se a `ContentLoading` navegação continua para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="8ee32-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="8ee32-131">No caso de um redirecionamento HTTP, há vários eventos em uma linha, onde os args de evento subsequentes têm a propriedade definida, no entanto, os `NavigationStarting` `IsRedirect` mesmos permanecem os `NavigationId` mesmos.</span><span class="sxs-lookup"><span data-stu-id="8ee32-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="8ee32-132">Mesmo documento , como navegar para `navigations` um fragmento, não resultam no evento e não `NavigationStarting` incrementam o `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="8ee32-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="8ee32-133">Para monitorar ou cancelar dentro de subframes no WebView, use os eventos que atuam exatamente como os eventos equivalentes que não são `navigations` `FrameNavigationStarting` de `FrameNavigationCompleted` quadro.</span><span class="sxs-lookup"><span data-stu-id="8ee32-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  
