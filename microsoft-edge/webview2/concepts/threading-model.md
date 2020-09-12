---
description: Modelo de threading
title: Modelo de threading
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 61e3b7fc8d25e2a1ce9c60fb84f5f39ba43f281b
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013734"
---
# <span data-ttu-id="5288d-104">Modelo de threading</span><span class="sxs-lookup"><span data-stu-id="5288d-104">Threading model</span></span> 

<span data-ttu-id="5288d-105">O controle WebView2 é baseado no [modelo de objeto componente (com)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) e deve ser executado em um [único thread de Apartments (STA) segmentado](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) .</span><span class="sxs-lookup"><span data-stu-id="5288d-105">The WebView2 control is based on the [Component Object Model (COM)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) and must run on a [Single Threaded Apartments (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) thread.</span></span>

## <span data-ttu-id="5288d-106">Segurança de thread</span><span class="sxs-lookup"><span data-stu-id="5288d-106">Thread safety</span></span>  

<span data-ttu-id="5288d-107">O WebView2 deve ser criado em um thread de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5288d-107">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="5288d-108">Especificamente um thread com um bombeamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5288d-108">Specifically a thread with a message pump.</span></span>  <span data-ttu-id="5288d-109">Todos os retornos de chamada ocorrem nesse thread e as solicitações no WebView2 devem ser feitas nesse thread.</span><span class="sxs-lookup"><span data-stu-id="5288d-109">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="5288d-110">Não é seguro usar o WebView2 de outro thread.</span><span class="sxs-lookup"><span data-stu-id="5288d-110">It is not safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="5288d-111">A única exceção é para a `Content` propriedade `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="5288d-111">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="5288d-112">O `Content` fluxo de propriedades é lido a partir de um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5288d-112">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="5288d-113">O fluxo deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5288d-113">The stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span>  

## <span data-ttu-id="5288d-114">Reentrância</span><span class="sxs-lookup"><span data-stu-id="5288d-114">Reentrancy</span></span>  

<span data-ttu-id="5288d-115">Os retornos de chamada, incluindo manipuladores de eventos e manipuladores de conclusão, são executados em série.</span><span class="sxs-lookup"><span data-stu-id="5288d-115">Callbacks including event handlers and completion handlers run serially.</span></span>  <span data-ttu-id="5288d-116">Se você tiver um manipulador de eventos em execução e iniciar um loop de mensagem, nenhum outro manipulador de eventos ou retornos de chamada de conclusão poderão começar a ser executados de forma reentrante.</span><span class="sxs-lookup"><span data-stu-id="5288d-116">If you have an event handler running and begin a message loop, no other event handlers or completion callbacks are able to begin running in a reentrant manner.</span></span>  

## <span data-ttu-id="5288d-117">Adiamentos</span><span class="sxs-lookup"><span data-stu-id="5288d-117">Deferrals</span></span>  

<span data-ttu-id="5288d-118">Alguns eventos WebView2 lêem valores definidos em seus argumentos de evento ou executam alguma ação após a conclusão do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5288d-118">Some WebView2 events read values set on their event args or perform some action after the event handler completes.</span></span>  <span data-ttu-id="5288d-119">Se você também precisar executar uma operação assíncrona, como um manipulador de eventos, você pode usar o `GetDeferral` método nos argumentos do evento dos eventos associados.</span><span class="sxs-lookup"><span data-stu-id="5288d-119">If you also need to run an asynchronous operation such an event handler, you may use the `GetDeferral` method on the event args of the associated events.</span></span>  <span data-ttu-id="5288d-120">O objeto de adiamento retornado garante que o manipulador de eventos não seja considerado concluído até que o `Complete` método de `Deferral` seja solicitado.</span><span class="sxs-lookup"><span data-stu-id="5288d-120">The returned Deferral object ensures the event handler is not considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="5288d-121">Por exemplo, você pode usar o `NewWindowRequested` evento para fornecer uma `CoreWebView2` janela para conectar-se como uma janela filho quando o manipulador de eventos é concluído.</span><span class="sxs-lookup"><span data-stu-id="5288d-121">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="5288d-122">Mas se você precisar criar assincronamente o `CoreWebView2` , solicite o `GetDeferral` método no `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="5288d-122">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="5288d-123">Depois que você tiver criado assincronamente a `CoreWebView2` e definir a `NewWindow` propriedade no `NewWindowRequestedEventArgs` objeto, a solicitação `Complete` no `Deferral` objeto será retornada usando o `GetDeferral` método.</span><span class="sxs-lookup"><span data-stu-id="5288d-123">After you have asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

<!-- links -->  
