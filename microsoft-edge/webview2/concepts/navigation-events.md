---
description: Navegação
title: Navegação | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: d133bfb99808d0e036c4b46be9ef82039aee49eb
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535703"
---
# <a name="navigation-events"></a><span data-ttu-id="9c501-104">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="9c501-104">Navigation events</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="9c501-105">Plataformas com suporte:</span><span class="sxs-lookup"><span data-stu-id="9c501-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9c501-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="9c501-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="9c501-107">Os eventos de navegação são executados quando ações assíncronas específicas ocorrem no conteúdo exibido em uma instância do WebView2.</span><span class="sxs-lookup"><span data-stu-id="9c501-107">Navigation events run when specific asynchronous actions occur to the content displayed in a WebView2 instance.</span></span>  <span data-ttu-id="9c501-108">Por exemplo, quando um usuário webView2 navega para um novo site, o conteúdo nativo escuta a alteração usando o `NavigationStarting` evento.</span><span class="sxs-lookup"><span data-stu-id="9c501-108">For example, when a WebView2 user navigates to a new website, the native content listens for the change using `NavigationStarting` event.</span></span>  <span data-ttu-id="9c501-109">Quando a ação de navegação for concluída, `NavigationCompleted` será executado.</span><span class="sxs-lookup"><span data-stu-id="9c501-109">When the navigation action completes, `NavigationCompleted` runs.</span></span>  <span data-ttu-id="9c501-110">Para um bom exemplo de eventos de navegação, navegue até [WebView2 Introdução guia][Webview2IndexGetStarted].</span><span class="sxs-lookup"><span data-stu-id="9c501-110">For a good example of navigation events, navigate to [WebView2 Get Started guide][Webview2IndexGetStarted].</span></span>  

<!--todo:  Move the relevant information out of the get started guide to better focus the content and leave the most concise elements in the get started guide.  -->   

<span data-ttu-id="9c501-111">A sequência normal de eventos de navegação `NavigationStarting` `SourceChanged` é , , `ContentLoading` `HistoryChanged` e, em `NavigationCompleted` seguida.</span><span class="sxs-lookup"><span data-stu-id="9c501-111">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="9c501-112">Os eventos a seguir descrevem o estado de WebView2 durante cada navegação.</span><span class="sxs-lookup"><span data-stu-id="9c501-112">The following events describe the state of WebView2 during each navigation.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Os Microsoft Edge webview2 eventos de navegação" lightbox="../media/navigation-graph.png":::
         <span data-ttu-id="9c501-114">Os Microsoft Edge webview2 eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="9c501-114">The Microsoft Edge WebView2 Navigation Events</span></span>  
      :::image-end:::  
      
      > [!NOTE]
      > <span data-ttu-id="9c501-115">A figura representa eventos de navegação com a mesma `NavigationId` propriedade no argumento de evento respectivo.</span><span class="sxs-lookup"><span data-stu-id="9c501-115">The figure represents navigation events with the same `NavigationId` property on the respective event argument.</span></span>  
   :::column-end:::
   :::column span="2":::
      | <span data-ttu-id="9c501-116">Sequence</span><span class="sxs-lookup"><span data-stu-id="9c501-116">Sequence</span></span> | <span data-ttu-id="9c501-117">Nome do evento</span><span class="sxs-lookup"><span data-stu-id="9c501-117">Event name</span></span> | <span data-ttu-id="9c501-118">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9c501-118">Details</span></span> |  
      |:--- |:--- |:--- |  
      | <span data-ttu-id="9c501-119">1</span><span class="sxs-lookup"><span data-stu-id="9c501-119">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="9c501-120">WebView2 começa a navegar e a navegação resulta em uma solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="9c501-120">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="9c501-121">O host pode não permitir a solicitação durante o evento.</span><span class="sxs-lookup"><span data-stu-id="9c501-121">The host may disallow the request during the event.</span></span>  |  
      | <span data-ttu-id="9c501-122">2</span><span class="sxs-lookup"><span data-stu-id="9c501-122">2</span></span> | `SourceChanged`  |  <span data-ttu-id="9c501-123">A origem do WebView2 muda para uma nova URL.</span><span class="sxs-lookup"><span data-stu-id="9c501-123">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="9c501-124">O evento pode resultar de uma ação de navegação que não causa uma solicitação de rede, como uma navegação de fragmento.</span><span class="sxs-lookup"><span data-stu-id="9c501-124">The event may result from a navigation action that does not cause a network request such as a fragment navigation.</span></span>  |  
      | <span data-ttu-id="9c501-125">3</span><span class="sxs-lookup"><span data-stu-id="9c501-125">3</span></span> | `ContentLoading`  |  <span data-ttu-id="9c501-126">O WebView começa a carregar conteúdo para a nova página.</span><span class="sxs-lookup"><span data-stu-id="9c501-126">WebView starts loading content for the new page.</span></span>  |  
      | <span data-ttu-id="9c501-127">4</span><span class="sxs-lookup"><span data-stu-id="9c501-127">4</span></span> | `HistoryChanged`  |  <span data-ttu-id="9c501-128">A navegação faz com que o histórico de WebView2 seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="9c501-128">The navigation causes the history of WebView2 to update.</span></span>  |  
      | <span data-ttu-id="9c501-129">5</span><span class="sxs-lookup"><span data-stu-id="9c501-129">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="9c501-130">WebView2 conclui o carregamento de conteúdo na nova página.</span><span class="sxs-lookup"><span data-stu-id="9c501-130">WebView2 completes loading content on the new page.</span></span>  |  
   :::column-end:::
:::row-end:::

<span data-ttu-id="9c501-131">Rastrear eventos de navegação para cada novo documento usando a ID de navegação \( `NavigationId` event\).</span><span class="sxs-lookup"><span data-stu-id="9c501-131">Track navigation events to each new document using the navigation ID \(`NavigationId` event\).</span></span>  <span data-ttu-id="9c501-132">O `NavigationId` evento do WebView muda sempre que uma navegação bem-sucedida para um novo documento é concluída.</span><span class="sxs-lookup"><span data-stu-id="9c501-132">The `NavigationId` event of WebView changes every time a successful navigation to a new document completes.</span></span>  

 <span data-ttu-id="9c501-133">Eventos de navegação com instâncias diferentes `NavigationId` de evento podem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="9c501-133">Navigation events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="9c501-134">Por exemplo, ao iniciar um evento de navegação, você deve aguardar o evento `NavigationStarting` relacionado.</span><span class="sxs-lookup"><span data-stu-id="9c501-134">For instance, when you start a navigation event, you must wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="9c501-135">Se você, em seguida, iniciar outra navegação, verá o evento para a primeira navegação seguida pelo evento para a segunda navegação, seguido pelo evento para a primeira navegação e, em seguida, todo o restante dos eventos de navegação apropriados para a segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegação.</span><span class="sxs-lookup"><span data-stu-id="9c501-135">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="9c501-136">Em casos de erro, pode haver ou não um evento, dependendo se a navegação `ContentLoading` é continuada para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="9c501-136">In error cases, there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="9c501-137">Se ocorrer um redirecionamento HTTP, haverá vários eventos em uma linha, onde argumentos de evento posteriores têm a propriedade definida, no entanto, o evento `NavigationStarting` `IsRedirect` permanece o `NavigationId` mesmo.</span><span class="sxs-lookup"><span data-stu-id="9c501-137">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row, where later event arguments have the `IsRedirect` property set, however the `NavigationId` event remains the same.</span></span>  
 
 <span data-ttu-id="9c501-138">Os mesmos eventos de navegação de documento, como navegar para um fragmento, não resultam no evento e `NavigationStarting` não incrementam o `NavigationId` evento.</span><span class="sxs-lookup"><span data-stu-id="9c501-138">Same document navigation events, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId` event.</span></span>  

<span data-ttu-id="9c501-139">Para monitorar ou cancelar eventos de navegação dentro de subframes em uma instância webView2, use os eventos e que agem da mesma forma que os eventos equivalentes de contraparte não `FrameNavigationStarting` `FrameNavigationCompleted` quadro.</span><span class="sxs-lookup"><span data-stu-id="9c501-139">To monitor or cancel navigation events inside subframes in a WebView2 instance, use the `FrameNavigationStarting` and `FrameNavigationCompleted` events that act just like the equivalent non-frame counterpart events.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9c501-140">Ver também</span><span class="sxs-lookup"><span data-stu-id="9c501-140">See also</span></span>  

*   <span data-ttu-id="9c501-141">Para começar a usar WebView2, navegue até [WebView2 Introdução Guias.][Webview2IndexGetStarted]</span><span class="sxs-lookup"><span data-stu-id="9c501-141">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2IndexGetStarted] guides.</span></span>  
*   <span data-ttu-id="9c501-142">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] em GitHub.</span><span class="sxs-lookup"><span data-stu-id="9c501-142">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="9c501-143">Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="9c501-143">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="9c501-144">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="9c501-144">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="9c501-145">Entrar em contato com a equipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="9c501-145">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
