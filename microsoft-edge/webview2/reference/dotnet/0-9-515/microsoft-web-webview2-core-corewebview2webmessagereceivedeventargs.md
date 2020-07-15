---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: ff4ebd8dc3a1c78424d57f6c7b5e6f7fc8e99049
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879314"
---
# <span data-ttu-id="34e6d-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="34e6d-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="34e6d-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="34e6d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="34e6d-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="34e6d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="34e6d-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="34e6d-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="34e6d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="34e6d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="34e6d-109">Args de evento para o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="34e6d-109">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="34e6d-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="34e6d-110">Summary</span></span>

 <span data-ttu-id="34e6d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="34e6d-111">Members</span></span>                        | <span data-ttu-id="34e6d-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="34e6d-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="34e6d-113">Origem</span><span class="sxs-lookup"><span data-stu-id="34e6d-113">Source</span></span>](#source) | <span data-ttu-id="34e6d-114">O URI do documento que enviou esta mensagem da Web.</span><span class="sxs-lookup"><span data-stu-id="34e6d-114">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="34e6d-115">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="34e6d-115">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="34e6d-116">A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="34e6d-116">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="34e6d-117">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="34e6d-117">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="34e6d-118">Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="34e6d-118">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="34e6d-119">Parte</span><span class="sxs-lookup"><span data-stu-id="34e6d-119">Members</span></span>

#### <span data-ttu-id="34e6d-120">Origem</span><span class="sxs-lookup"><span data-stu-id="34e6d-120">Source</span></span> 

<span data-ttu-id="34e6d-121">O URI do documento que enviou esta mensagem da Web.</span><span class="sxs-lookup"><span data-stu-id="34e6d-121">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="34e6d-122">[fonte](#source) de cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="34e6d-122">public string [Source](#source)</span></span>

#### <span data-ttu-id="34e6d-123">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="34e6d-123">WebMessageAsJson</span></span> 

<span data-ttu-id="34e6d-124">A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="34e6d-124">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="34e6d-125">Cadeia de caracteres pública [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="34e6d-125">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="34e6d-126">Use isso para se comunicar por objetos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="34e6d-126">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="34e6d-127">Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="34e6d-127">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="34e6d-128">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="34e6d-128">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="34e6d-129">Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="34e6d-129">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="34e6d-130">[TryGetWebMessageAsString](#trygetwebmessageasstring)de cadeia de caracteres pública ()</span><span class="sxs-lookup"><span data-stu-id="34e6d-130">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="34e6d-131">Se a mensagem publicada for outro tipo de tipo JavaScript, esse método falhará com E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="34e6d-131">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="34e6d-132">Use isso para se comunicar por meio de cadeias de caracteres simples.</span><span class="sxs-lookup"><span data-stu-id="34e6d-132">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="34e6d-133">Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="34e6d-133">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

