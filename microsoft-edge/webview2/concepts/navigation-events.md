---
description: Navegação
title: Navegação
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895539"
---
# <span data-ttu-id="77429-104">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="77429-104">Navigation events</span></span>  

<span data-ttu-id="77429-105">A sequência normal de eventos de navegação é `NavigationStarting` , `SourceChanged` ,, `ContentLoading` `HistoryChanged` e `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="77429-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="77429-106">Os eventos a seguir descrevem o estado de WebView2 durante cada navegação.</span><span class="sxs-lookup"><span data-stu-id="77429-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="77429-107">Ordena</span><span class="sxs-lookup"><span data-stu-id="77429-107">Sequence</span></span> | <span data-ttu-id="77429-108">Nome do evento</span><span class="sxs-lookup"><span data-stu-id="77429-108">Event name</span></span> | <span data-ttu-id="77429-109">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77429-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77429-110">um</span><span class="sxs-lookup"><span data-stu-id="77429-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="77429-111">O WebView2 começa a navegar e a navegação resulta em uma solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="77429-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="77429-112">O host pode impedir a solicitação durante o evento.</span><span class="sxs-lookup"><span data-stu-id="77429-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="77429-113">2</span><span class="sxs-lookup"><span data-stu-id="77429-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="77429-114">A fonte de WebView2 muda para uma nova URL.</span><span class="sxs-lookup"><span data-stu-id="77429-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="77429-115">O evento pode resultar de uma navegação que não causa uma solicitação de rede, como uma navegação de fragmento.</span><span class="sxs-lookup"><span data-stu-id="77429-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="77429-116">3D</span><span class="sxs-lookup"><span data-stu-id="77429-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="77429-117">O histórico de atualizações do WebView2 como resultado da navegação.</span><span class="sxs-lookup"><span data-stu-id="77429-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="77429-118">4</span><span class="sxs-lookup"><span data-stu-id="77429-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="77429-119">O WebView começa a carregar o conteúdo da nova página.</span><span class="sxs-lookup"><span data-stu-id="77429-119">WebView starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="77429-120">5</span><span class="sxs-lookup"><span data-stu-id="77429-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="77429-121">O WebView2 conclui o carregamento do conteúdo na nova página.</span><span class="sxs-lookup"><span data-stu-id="77429-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="77429-122">Acompanhe `navigations` cada novo documento usando a identificação de navegação \ ( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="77429-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="77429-123">O `NavigationId` do WebView muda a cada vez que há uma navegação com êxito para um novo documento.</span><span class="sxs-lookup"><span data-stu-id="77429-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="Os eventos de navegação do Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="77429-125">Os eventos de navegação do Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="77429-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="77429-126">A figura anterior representa eventos de navegação com a mesma `NavigationId` propriedade no argumento de evento respectiva.</span><span class="sxs-lookup"><span data-stu-id="77429-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="77429-127">eventos com diferentes instâncias de `NavigationId` evento podem sobrepor-se.</span><span class="sxs-lookup"><span data-stu-id="77429-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="77429-128">Por exemplo, quando você inicia uma navegação, é preciso aguardar o `NavigationStarting` evento relacionado.</span><span class="sxs-lookup"><span data-stu-id="77429-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="77429-129">Se, em seguida, você iniciar outra navegação, verá o `NavigationStarting` evento para a primeira navegação acompanhada pelo `NavigationStarting` evento para a segunda navegação, seguida do `NavigationCompleted` evento para a primeira navegação e todos os demais eventos de navegação apropriados para a segunda navegação.</span><span class="sxs-lookup"><span data-stu-id="77429-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="77429-130">Em casos de erro, pode ou não ser um `ContentLoading` evento, dependendo se a navegação é continuada para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="77429-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="77429-131">No caso de um redirecionamento HTTP, há vários `NavigationStarting` eventos em uma linha, onde os args de eventos subsequentes têm a `IsRedirect` propriedade definida, no entanto, o `NavigationId` restante é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="77429-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="77429-132">O mesmo documento `navigations` , como navegar para um fragmento, não resulta no `NavigationStarting` evento e não aumenta o `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="77429-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="77429-133">Para monitorar ou cancelar `navigations` subquadros dentro do WebView, use os `FrameNavigationStarting` eventos e os `FrameNavigationCompleted` eventos que atuam exatamente como os eventos equivalentes sem quadro correspondente.</span><span class="sxs-lookup"><span data-stu-id="77429-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  
