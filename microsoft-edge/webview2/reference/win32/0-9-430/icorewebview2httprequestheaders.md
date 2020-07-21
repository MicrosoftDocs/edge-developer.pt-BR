---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 04a8bf376ad7649021c4ab1555c3090cce5b52fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885608"
---
# <span data-ttu-id="cf5d4-104">0.9.430-ICoreWebView2HttpRequestHeaders de interface</span><span class="sxs-lookup"><span data-stu-id="cf5d4-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="cf5d4-105">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-105">HTTP request headers.</span></span>

## <span data-ttu-id="cf5d4-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="cf5d4-106">Summary</span></span>

 <span data-ttu-id="cf5d4-107">Parte</span><span class="sxs-lookup"><span data-stu-id="cf5d4-107">Members</span></span>                        | <span data-ttu-id="cf5d4-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="cf5d4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf5d4-109">GetHeader</span><span class="sxs-lookup"><span data-stu-id="cf5d4-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="cf5d4-110">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="cf5d4-111">Getheaders</span><span class="sxs-lookup"><span data-stu-id="cf5d4-111">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="cf5d4-112">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-112">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="cf5d4-113">Contém</span><span class="sxs-lookup"><span data-stu-id="cf5d4-113">Contains</span></span>](#contains) | <span data-ttu-id="cf5d4-114">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="cf5d4-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="cf5d4-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="cf5d4-116">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="cf5d4-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="cf5d4-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="cf5d4-118">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="cf5d4-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="cf5d4-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="cf5d4-120">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="cf5d4-121">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="cf5d4-122">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="cf5d4-123">Parte</span><span class="sxs-lookup"><span data-stu-id="cf5d4-123">Members</span></span>

#### <span data-ttu-id="cf5d4-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="cf5d4-124">GetHeader</span></span> 

<span data-ttu-id="cf5d4-125">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="cf5d4-126">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="cf5d4-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="cf5d4-127">Getheaders</span><span class="sxs-lookup"><span data-stu-id="cf5d4-127">GetHeaders</span></span> 

<span data-ttu-id="cf5d4-128">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-128">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="cf5d4-129">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="cf5d4-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="cf5d4-130">Contém</span><span class="sxs-lookup"><span data-stu-id="cf5d4-130">Contains</span></span> 

<span data-ttu-id="cf5d4-131">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-131">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="cf5d4-132">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="cf5d4-132">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="cf5d4-133">SetHeader</span><span class="sxs-lookup"><span data-stu-id="cf5d4-133">SetHeader</span></span> 

<span data-ttu-id="cf5d4-134">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-134">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="cf5d4-135">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="cf5d4-135">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="cf5d4-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="cf5d4-136">RemoveHeader</span></span> 

<span data-ttu-id="cf5d4-137">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="cf5d4-138">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="cf5d4-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="cf5d4-139">GetIterator</span><span class="sxs-lookup"><span data-stu-id="cf5d4-139">GetIterator</span></span> 

<span data-ttu-id="cf5d4-140">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="cf5d4-140">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="cf5d4-141">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="cf5d4-141">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

