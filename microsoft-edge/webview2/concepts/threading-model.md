---
description: Modelo de threading
title: Threading model | WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 9a7ce3d66e53b832d4430afb153e6539d97e5db7
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535605"
---
# <a name="threading-model"></a><span data-ttu-id="746f2-104">Modelo de threading</span><span class="sxs-lookup"><span data-stu-id="746f2-104">Threading model</span></span> 

:::row:::
   :::column span="1":::
      <span data-ttu-id="746f2-105">Plataformas com suporte:</span><span class="sxs-lookup"><span data-stu-id="746f2-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="746f2-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="746f2-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="746f2-107">O controle WebView2 baseia-se no Modelo de Objeto de Componente [(COM)][WindowsWin32ComTheComponentObjectModel] e deve ser executado em um thread STA [(Single Threaded Apartments).][WindowsWin32ComSingleThreadedApartments]</span><span class="sxs-lookup"><span data-stu-id="746f2-107">The WebView2 control is based on the [Component Object Model (COM)][WindowsWin32ComTheComponentObjectModel] and must run on a [Single Threaded Apartments (STA)][WindowsWin32ComSingleThreadedApartments] thread.</span></span>  

## <a name="thread-safety"></a><span data-ttu-id="746f2-108">Segurança de thread</span><span class="sxs-lookup"><span data-stu-id="746f2-108">Thread safety</span></span>  

<span data-ttu-id="746f2-109">O WebView2 deve ser criado em um thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="746f2-109">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="746f2-110">Especificamente, um thread com uma bomba de mensagem.</span><span class="sxs-lookup"><span data-stu-id="746f2-110">Specifically, a thread with a message pump.</span></span>  <span data-ttu-id="746f2-111">Todos os retornos de chamada ocorrem nesse thread e as solicitações no WebView2 devem ser feitas nesse thread.</span><span class="sxs-lookup"><span data-stu-id="746f2-111">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="746f2-112">Não é seguro usar o WebView2 de outro thread.</span><span class="sxs-lookup"><span data-stu-id="746f2-112">It isn't safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="746f2-113">A única exceção é para a `Content` propriedade `CoreWebView2WebResourceRequest` de .</span><span class="sxs-lookup"><span data-stu-id="746f2-113">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="746f2-114">O `Content` fluxo de propriedades é lido de um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="746f2-114">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="746f2-115">O fluxo deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar a degradação de desempenho para o thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="746f2-115">The stream should be agile or be created from a background STA to prevent performance degradation to the UI thread.</span></span>  

## <a name="re-entrancy"></a><span data-ttu-id="746f2-116">Re-entrada</span><span class="sxs-lookup"><span data-stu-id="746f2-116">Re-entrancy</span></span>  

<span data-ttu-id="746f2-117">Os retornos de chamada, incluindo manipuladores de eventos e manipuladores de conclusão, são executados em série.</span><span class="sxs-lookup"><span data-stu-id="746f2-117">Callbacks including event handlers and completion handlers run serially.</span></span>  
<span data-ttu-id="746f2-118">Depois de executar um manipulador de eventos e iniciar um loop de mensagem, você não poderá executar qualquer manipulador de eventos ou retorno de chamada de conclusão de uma maneira de nova entrada.</span><span class="sxs-lookup"><span data-stu-id="746f2-118">After you run an event handler and begin a message loop, you're unable to run any event handler or completion callback in a re-entrant manner.</span></span>  

## <a name="deferrals"></a><span data-ttu-id="746f2-119">Adiamentos</span><span class="sxs-lookup"><span data-stu-id="746f2-119">Deferrals</span></span>  

<span data-ttu-id="746f2-120">Alguns eventos WebView2 leem valores definidos nos argumentos de evento relacionados ou iniciam alguma ação depois que o manipulador de eventos é concluído.</span><span class="sxs-lookup"><span data-stu-id="746f2-120">Some WebView2 events read values set on the related event arguments or start some action after the event handler completes.</span></span>  <span data-ttu-id="746f2-121">Se você também precisar executar uma operação assíncrona como um manipulador de eventos, use o método nos argumentos de evento `GetDeferral` dos eventos associados.</span><span class="sxs-lookup"><span data-stu-id="746f2-121">If you also need to run an asynchronous operation such an event handler, use the `GetDeferral` method on the event arguments of the associated events.</span></span>  <span data-ttu-id="746f2-122">O objeto retornado garante que o manipulador de eventos não seja considerado concluído até que o `Deferral` `Complete` método do seja `Deferral` solicitado.</span><span class="sxs-lookup"><span data-stu-id="746f2-122">The returned `Deferral` object ensures the event handler isn't considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="746f2-123">Por exemplo, você pode usar o evento para fornecer um para se conectar como uma janela filha quando o manipulador `NewWindowRequested` `CoreWebView2` de eventos for concluído.</span><span class="sxs-lookup"><span data-stu-id="746f2-123">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="746f2-124">Mas se você precisar criar de forma assíncrona o método , solicite o `CoreWebView2` método no `GetDeferral` `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="746f2-124">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="746f2-125">Depois de criar de forma assíncrona e definir a propriedade na solicitação , no objeto, será retornado `CoreWebView2` `NewWindow` usando o `NewWindowRequestedEventArgs` `Complete` `Deferral` `GetDeferral` método.</span><span class="sxs-lookup"><span data-stu-id="746f2-125">After you've asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

## <a name="block-the-ui-thread"></a><span data-ttu-id="746f2-126">Bloquear o thread da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="746f2-126">Block the UI thread</span></span>  

<span data-ttu-id="746f2-127">O WebView2 depende da mensagem do thread da interface do usuário para executar retornos de chamada do manipulador de eventos e retornos de chamada de conclusão do método assíncrono.</span><span class="sxs-lookup"><span data-stu-id="746f2-127">The WebView2 relies on the message pump of the UI thread to run event handler callbacks and async method completion callbacks.</span></span>  <span data-ttu-id="746f2-128">Se você usar métodos que bloqueiam a mensagem, como ou , seus manipuladores de eventos WebView2 e manipuladores de conclusão do método `Task.Result` `WaitForSingleObject` assíncrono não são executados.</span><span class="sxs-lookup"><span data-stu-id="746f2-128">If you use methods that block the message pump such as `Task.Result` or `WaitForSingleObject`, then your WebView2 event handlers and async method completion handlers don't run.</span></span>  <span data-ttu-id="746f2-129">Por exemplo, o código a seguir não é concluído, porque interrompe a mensagem enquanto `Task.Result` aguarda a `ExecuteScriptAsync` conclusão.</span><span class="sxs-lookup"><span data-stu-id="746f2-129">For example, the following code doesn't complete, because `Task.Result` stops the message pump while it waits for `ExecuteScriptAsync` to complete.</span></span>  <span data-ttu-id="746f2-130">Como a mensagem está bloqueada, `ExecuteScriptAsync` o não é capaz de ser concluído.</span><span class="sxs-lookup"><span data-stu-id="746f2-130">Since the message pump is blocked, the `ExecuteScriptAsync` isn't able to complete.</span></span>   

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

<span data-ttu-id="746f2-131">Use um mecanismo assíncrono como e , que não bloqueia a mensagem ou `await` o thread da interface do `async` `await` usuário.</span><span class="sxs-lookup"><span data-stu-id="746f2-131">Use an asynchronous `await` mechanism such as `async` and `await`, which doesn't block the message pump or the UI thread.</span></span>  

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

## <a name="see-also"></a><span data-ttu-id="746f2-132">Ver também</span><span class="sxs-lookup"><span data-stu-id="746f2-132">See also</span></span>  

*   <span data-ttu-id="746f2-133">Para começar a usar o WebView2, navegue até Guias de Início [da WebView2.][Webview2IndexGetStarted]</span><span class="sxs-lookup"><span data-stu-id="746f2-133">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2IndexGetStarted] guides.</span></span>  
*   <span data-ttu-id="746f2-134">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples no][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="746f2-134">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="746f2-135">Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="746f2-135">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="746f2-136">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="746f2-136">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="746f2-137">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="746f2-137">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Apartamentos com thread único | Microsoft Docs"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "O modelo de objeto component | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
