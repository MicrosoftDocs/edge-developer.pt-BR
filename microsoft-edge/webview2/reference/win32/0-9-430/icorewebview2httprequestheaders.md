---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: a67c5c267178ea873cd12d8a22dea7409b260d52
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880994"
---
# <span data-ttu-id="fe3f6-104">0.9.430-ICoreWebView2HttpRequestHeaders de interface</span><span class="sxs-lookup"><span data-stu-id="fe3f6-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="fe3f6-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="fe3f6-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="fe3f6-107">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-107">HTTP request headers.</span></span>

## <span data-ttu-id="fe3f6-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="fe3f6-108">Summary</span></span>

 <span data-ttu-id="fe3f6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fe3f6-109">Members</span></span>                        | <span data-ttu-id="fe3f6-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="fe3f6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fe3f6-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="fe3f6-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="fe3f6-112">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="fe3f6-113">Getheaders</span><span class="sxs-lookup"><span data-stu-id="fe3f6-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="fe3f6-114">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="fe3f6-115">Contém</span><span class="sxs-lookup"><span data-stu-id="fe3f6-115">Contains</span></span>](#contains) | <span data-ttu-id="fe3f6-116">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="fe3f6-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="fe3f6-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="fe3f6-118">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="fe3f6-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="fe3f6-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="fe3f6-120">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="fe3f6-121">GetIterator</span><span class="sxs-lookup"><span data-stu-id="fe3f6-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="fe3f6-122">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="fe3f6-123">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="fe3f6-124">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="fe3f6-125">Parte</span><span class="sxs-lookup"><span data-stu-id="fe3f6-125">Members</span></span>

#### <span data-ttu-id="fe3f6-126">GetHeader</span><span class="sxs-lookup"><span data-stu-id="fe3f6-126">GetHeader</span></span> 

<span data-ttu-id="fe3f6-127">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="fe3f6-128">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="fe3f6-129">Getheaders</span><span class="sxs-lookup"><span data-stu-id="fe3f6-129">GetHeaders</span></span> 

<span data-ttu-id="fe3f6-130">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="fe3f6-131">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="fe3f6-132">Contém</span><span class="sxs-lookup"><span data-stu-id="fe3f6-132">Contains</span></span> 

<span data-ttu-id="fe3f6-133">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="fe3f6-134">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="fe3f6-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="fe3f6-135">SetHeader</span></span> 

<span data-ttu-id="fe3f6-136">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="fe3f6-137">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="fe3f6-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="fe3f6-138">RemoveHeader</span></span> 

<span data-ttu-id="fe3f6-139">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="fe3f6-140">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="fe3f6-141">GetIterator</span><span class="sxs-lookup"><span data-stu-id="fe3f6-141">GetIterator</span></span> 

<span data-ttu-id="fe3f6-142">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="fe3f6-143">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="fe3f6-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

