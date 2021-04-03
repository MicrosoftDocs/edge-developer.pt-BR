---
description: Navegação
title: Navegação | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: e87994d6205f81e01385a131e17091d0c8b001d5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470841"
---
# <a name="navigation-events"></a><span data-ttu-id="d722a-104">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="d722a-104">Navigation events</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="d722a-105">Plataformas com suporte:</span><span class="sxs-lookup"><span data-stu-id="d722a-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d722a-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="d722a-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d722a-107">Os eventos de navegação são executados quando ações assíncronas específicas ocorrem no conteúdo exibido em uma instância do WebView2.</span><span class="sxs-lookup"><span data-stu-id="d722a-107">Navigation events run when specific asynchronous actions occur to the content displayed in a WebView2 instance.</span></span>  <span data-ttu-id="d722a-108">Por exemplo, quando um usuário webView2 navega para um novo site, o conteúdo nativo escuta a alteração usando o `NavigationStarting` evento.</span><span class="sxs-lookup"><span data-stu-id="d722a-108">For example, when a WebView2 user navigates to a new website, the native content listens for the change using `NavigationStarting` event.</span></span>  <span data-ttu-id="d722a-109">Quando a ação de navegação for concluída, `NavigationCompleted` será executado.</span><span class="sxs-lookup"><span data-stu-id="d722a-109">When the navigation action completes, `NavigationCompleted` runs.</span></span>  <span data-ttu-id="d722a-110">Para obter um bom exemplo de eventos de navegação, navegue até [WebView2 guia de início.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="d722a-110">For a good example of navigation events, navigate to [WebView2 getting started guide][Webview2IndexGettingStarted].</span></span>  

<!--todo:  Move the relevant information out of the getting started guide to better focus the content and leave the most concise elements in the getting started guide.  -->   

<span data-ttu-id="d722a-111">A sequência normal de eventos de navegação `NavigationStarting` `SourceChanged` é , , `ContentLoading` `HistoryChanged` e, em `NavigationCompleted` seguida.</span><span class="sxs-lookup"><span data-stu-id="d722a-111">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="d722a-112">Os eventos a seguir descrevem o estado de WebView2 durante cada navegação.</span><span class="sxs-lookup"><span data-stu-id="d722a-112">The following events describe the state of WebView2 during each navigation.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Eventos de navegação do Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
         <span data-ttu-id="d722a-114">Eventos de navegação do Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="d722a-114">The Microsoft Edge WebView2 Navigation Events</span></span>  
      :::image-end:::  
      
      > [!NOTE]
      > <span data-ttu-id="d722a-115">A figura representa eventos de navegação com a mesma `NavigationId` propriedade no argumento de evento respectivo.</span><span class="sxs-lookup"><span data-stu-id="d722a-115">The figure represents navigation events with the same `NavigationId` property on the respective event argument.</span></span>  
   :::column-end:::
   :::column span="2":::
      | <span data-ttu-id="d722a-116">Sequence</span><span class="sxs-lookup"><span data-stu-id="d722a-116">Sequence</span></span> | <span data-ttu-id="d722a-117">Nome do evento</span><span class="sxs-lookup"><span data-stu-id="d722a-117">Event name</span></span> | <span data-ttu-id="d722a-118">Detalhes</span><span class="sxs-lookup"><span data-stu-id="d722a-118">Details</span></span> |  
      |:--- |:--- |:--- |  
      | <span data-ttu-id="d722a-119">1</span><span class="sxs-lookup"><span data-stu-id="d722a-119">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="d722a-120">WebView2 começa a navegar e a navegação resulta em uma solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="d722a-120">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="d722a-121">O host pode não permitir a solicitação durante o evento.</span><span class="sxs-lookup"><span data-stu-id="d722a-121">The host may disallow the request during the event.</span></span>  |  
      | <span data-ttu-id="d722a-122">2</span><span class="sxs-lookup"><span data-stu-id="d722a-122">2</span></span> | `SourceChanged`  |  <span data-ttu-id="d722a-123">A origem do WebView2 muda para uma nova URL.</span><span class="sxs-lookup"><span data-stu-id="d722a-123">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="d722a-124">O evento pode resultar de uma ação de navegação que não causa uma solicitação de rede, como uma navegação de fragmento.</span><span class="sxs-lookup"><span data-stu-id="d722a-124">The event may result from a navigation action that does not cause a network request such as a fragment navigation.</span></span>  |  
      | <span data-ttu-id="d722a-125">3</span><span class="sxs-lookup"><span data-stu-id="d722a-125">3</span></span> | `ContentLoading`  |  <span data-ttu-id="d722a-126">O WebView começa a carregar conteúdo para a nova página.</span><span class="sxs-lookup"><span data-stu-id="d722a-126">WebView starts loading content for the new page.</span></span>  |  
      | <span data-ttu-id="d722a-127">4</span><span class="sxs-lookup"><span data-stu-id="d722a-127">4</span></span> | `HistoryChanged`  |  <span data-ttu-id="d722a-128">A navegação faz com que o histórico de WebView2 seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="d722a-128">The navigation causes the history of WebView2 to update.</span></span>  |  
      | <span data-ttu-id="d722a-129">5</span><span class="sxs-lookup"><span data-stu-id="d722a-129">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="d722a-130">WebView2 conclui o carregamento de conteúdo na nova página.</span><span class="sxs-lookup"><span data-stu-id="d722a-130">WebView2 completes loading content on the new page.</span></span>  |  
   :::column-end:::
:::row-end:::

<span data-ttu-id="d722a-131">Rastrear eventos de navegação para cada novo documento usando a ID de navegação \( `NavigationId` event\).</span><span class="sxs-lookup"><span data-stu-id="d722a-131">Track navigation events to each new document using the navigation ID \(`NavigationId` event\).</span></span>  <span data-ttu-id="d722a-132">O `NavigationId` evento do WebView muda sempre que uma navegação bem-sucedida para um novo documento é concluída.</span><span class="sxs-lookup"><span data-stu-id="d722a-132">The `NavigationId` event of WebView changes every time a successful navigation to a new document completes.</span></span>  

 <span data-ttu-id="d722a-133">Eventos de navegação com instâncias diferentes `NavigationId` de evento podem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="d722a-133">Navigation events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="d722a-134">Por exemplo, ao iniciar um evento de navegação, você deve aguardar o evento `NavigationStarting` relacionado.</span><span class="sxs-lookup"><span data-stu-id="d722a-134">For instance, when you start a navigation event, you must wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="d722a-135">Se você, em seguida, iniciar outra navegação, verá o evento para a primeira navegação seguida pelo evento para a segunda navegação, seguido pelo evento para a primeira navegação e, em seguida, todo o restante dos eventos de navegação apropriados para a segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegação.</span><span class="sxs-lookup"><span data-stu-id="d722a-135">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="d722a-136">Em casos de erro, pode haver ou não um evento, dependendo se a navegação `ContentLoading` é continuada para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="d722a-136">In error cases, there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="d722a-137">Se ocorrer um redirecionamento HTTP, haverá vários eventos em uma linha, onde argumentos de evento posteriores têm a propriedade definida, no entanto, o evento `NavigationStarting` `IsRedirect` permanece o `NavigationId` mesmo.</span><span class="sxs-lookup"><span data-stu-id="d722a-137">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row, where later event arguments have the `IsRedirect` property set, however the `NavigationId` event remains the same.</span></span>  
 
 <span data-ttu-id="d722a-138">Os mesmos eventos de navegação de documento, como navegar para um fragmento, não resultam no evento e `NavigationStarting` não incrementam o `NavigationId` evento.</span><span class="sxs-lookup"><span data-stu-id="d722a-138">Same document navigation events, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId` event.</span></span>  

<span data-ttu-id="d722a-139">Para monitorar ou cancelar eventos de navegação dentro de subframes em uma instância webView2, use os eventos e que agem da mesma forma que os eventos equivalentes de contraparte não `FrameNavigationStarting` `FrameNavigationCompleted` quadro.</span><span class="sxs-lookup"><span data-stu-id="d722a-139">To monitor or cancel navigation events inside subframes in a WebView2 instance, use the `FrameNavigationStarting` and `FrameNavigationCompleted` events that act just like the equivalent non-frame counterpart events.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d722a-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d722a-140">See also</span></span>  

*   <span data-ttu-id="d722a-141">Para começar a usar o WebView2, navegue até Guias de Guia [de Iniciação da WebView2.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="d722a-141">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="d722a-142">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples no][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="d722a-142">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="d722a-143">Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="d722a-143">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="d722a-144">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="d722a-144">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="d722a-145">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="d722a-145">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Introdução - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
