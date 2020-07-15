---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 61805f34ac3ef3a51dcd5b746b77a7bdad8cdb5c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877599"
---
# <span data-ttu-id="4053c-104">interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4053c-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="4053c-105">Args de evento para o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="4053c-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="4053c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4053c-106">Summary</span></span>

 <span data-ttu-id="4053c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4053c-107">Members</span></span>                        | <span data-ttu-id="4053c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4053c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4053c-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="4053c-109">get_Source</span></span>](#get_source) | <span data-ttu-id="4053c-110">O URI do documento que enviou esta mensagem da Web.</span><span class="sxs-lookup"><span data-stu-id="4053c-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="4053c-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="4053c-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="4053c-112">A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="4053c-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="4053c-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="4053c-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="4053c-114">Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4053c-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="4053c-115">Parte</span><span class="sxs-lookup"><span data-stu-id="4053c-115">Members</span></span>

#### <span data-ttu-id="4053c-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="4053c-116">get_Source</span></span> 

<span data-ttu-id="4053c-117">O URI do documento que enviou esta mensagem da Web.</span><span class="sxs-lookup"><span data-stu-id="4053c-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="4053c-118">[get_Source](#get_source)público HRESULT (fonte LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="4053c-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="4053c-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="4053c-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="4053c-120">A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="4053c-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="4053c-121">público HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="4053c-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="4053c-122">Use isso para se comunicar por objetos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4053c-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="4053c-123">Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="4053c-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="4053c-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="4053c-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="4053c-125">Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4053c-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="4053c-126">Public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="4053c-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="4053c-127">Se a mensagem publicada for outro tipo de tipo JavaScript, esse método falhará com E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="4053c-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="4053c-128">Use isso para se comunicar por meio de cadeias de caracteres simples.</span><span class="sxs-lookup"><span data-stu-id="4053c-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="4053c-129">Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="4053c-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

