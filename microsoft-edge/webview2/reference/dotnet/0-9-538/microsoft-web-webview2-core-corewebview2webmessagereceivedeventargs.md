---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 9babcaff5b90e22ea6bac5d5703a54caef6d349d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698402"
---
# <span data-ttu-id="f69ac-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f69ac-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

<span data-ttu-id="f69ac-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f69ac-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f69ac-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="f69ac-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f69ac-107">Args de evento para o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="f69ac-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="f69ac-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f69ac-108">Summary</span></span>

 <span data-ttu-id="f69ac-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f69ac-109">Members</span></span>                        | <span data-ttu-id="f69ac-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="f69ac-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f69ac-111">Origem</span><span class="sxs-lookup"><span data-stu-id="f69ac-111">Source</span></span>](#source) | <span data-ttu-id="f69ac-112">O URI do documento que enviou esta mensagem da Web.</span><span class="sxs-lookup"><span data-stu-id="f69ac-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="f69ac-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="f69ac-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="f69ac-114">A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="f69ac-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="f69ac-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="f69ac-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="f69ac-116">Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f69ac-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="f69ac-117">Parte</span><span class="sxs-lookup"><span data-stu-id="f69ac-117">Members</span></span>

#### <span data-ttu-id="f69ac-118">Origem</span><span class="sxs-lookup"><span data-stu-id="f69ac-118">Source</span></span> 

<span data-ttu-id="f69ac-119">O URI do documento que enviou esta mensagem da Web.</span><span class="sxs-lookup"><span data-stu-id="f69ac-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="f69ac-120">[fonte](#source) de cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="f69ac-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="f69ac-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="f69ac-121">WebMessageAsJson</span></span> 

<span data-ttu-id="f69ac-122">A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="f69ac-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="f69ac-123">Cadeia de caracteres pública [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="f69ac-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="f69ac-124">Use isso para se comunicar por objetos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f69ac-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="f69ac-125">Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="f69ac-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="f69ac-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="f69ac-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="f69ac-127">Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f69ac-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="f69ac-128">[TryGetWebMessageAsString](#trygetwebmessageasstring)de cadeia de caracteres pública ()</span><span class="sxs-lookup"><span data-stu-id="f69ac-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="f69ac-129">Se a mensagem publicada for outro tipo de tipo JavaScript, esse método falhará com E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="f69ac-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="f69ac-130">Use isso para se comunicar por meio de cadeias de caracteres simples.</span><span class="sxs-lookup"><span data-stu-id="f69ac-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="f69ac-131">Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="f69ac-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

