---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: f3002c6e7941cea1f632e1df4ee42a8f38a468b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652733"
---
# <span data-ttu-id="5ea70-104">interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5ea70-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="5ea70-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="5ea70-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="5ea70-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="5ea70-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="5ea70-107">Args de evento para o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="5ea70-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="5ea70-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="5ea70-108">Summary</span></span>

 <span data-ttu-id="5ea70-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5ea70-109">Members</span></span>                        | <span data-ttu-id="5ea70-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="5ea70-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5ea70-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="5ea70-111">get_Source</span></span>](#get_source) | <span data-ttu-id="5ea70-112">O URI do documento que enviou esta mensagem da Web.</span><span class="sxs-lookup"><span data-stu-id="5ea70-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="5ea70-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="5ea70-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="5ea70-114">A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="5ea70-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="5ea70-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="5ea70-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="5ea70-116">Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ea70-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="5ea70-117">Parte</span><span class="sxs-lookup"><span data-stu-id="5ea70-117">Members</span></span>

#### <span data-ttu-id="5ea70-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="5ea70-118">get_Source</span></span> 

<span data-ttu-id="5ea70-119">O URI do documento que enviou esta mensagem da Web.</span><span class="sxs-lookup"><span data-stu-id="5ea70-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="5ea70-120">[get_Source](#get_source)público HRESULT (fonte LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="5ea70-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="5ea70-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="5ea70-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="5ea70-122">A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="5ea70-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="5ea70-123">público HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="5ea70-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="5ea70-124">Use isso para se comunicar por objetos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5ea70-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="5ea70-125">Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="5ea70-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="5ea70-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="5ea70-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="5ea70-127">Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ea70-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="5ea70-128">Public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="5ea70-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="5ea70-129">Se a mensagem publicada for outro tipo de tipo JavaScript, esse método falhará com E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5ea70-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="5ea70-130">Use isso para se comunicar por meio de cadeias de caracteres simples.</span><span class="sxs-lookup"><span data-stu-id="5ea70-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="5ea70-131">Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="5ea70-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

