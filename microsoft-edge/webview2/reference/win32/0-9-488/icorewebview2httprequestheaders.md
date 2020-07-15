---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2587a3e07869076be659e29d484a647b74c2bd7f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880546"
---
# <span data-ttu-id="4a410-104">0.9.515-ICoreWebView2HttpRequestHeaders de interface</span><span class="sxs-lookup"><span data-stu-id="4a410-104">0.9.515 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="4a410-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="4a410-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4a410-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="4a410-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="4a410-107">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="4a410-107">HTTP request headers.</span></span>

## <span data-ttu-id="4a410-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="4a410-108">Summary</span></span>

 <span data-ttu-id="4a410-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4a410-109">Members</span></span>                        | <span data-ttu-id="4a410-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="4a410-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4a410-111">Contém</span><span class="sxs-lookup"><span data-stu-id="4a410-111">Contains</span></span>](#contains) | <span data-ttu-id="4a410-112">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4a410-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="4a410-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4a410-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="4a410-114">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4a410-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="4a410-115">Getheaders</span><span class="sxs-lookup"><span data-stu-id="4a410-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="4a410-116">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="4a410-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="4a410-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4a410-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="4a410-118">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="4a410-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="4a410-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="4a410-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="4a410-120">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4a410-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="4a410-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="4a410-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="4a410-122">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4a410-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="4a410-123">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="4a410-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="4a410-124">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="4a410-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="4a410-125">Parte</span><span class="sxs-lookup"><span data-stu-id="4a410-125">Members</span></span>

#### <span data-ttu-id="4a410-126">Contém</span><span class="sxs-lookup"><span data-stu-id="4a410-126">Contains</span></span> 

<span data-ttu-id="4a410-127">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4a410-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="4a410-128">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="4a410-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="4a410-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4a410-129">GetHeader</span></span> 

<span data-ttu-id="4a410-130">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4a410-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="4a410-131">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="4a410-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="4a410-132">Getheaders</span><span class="sxs-lookup"><span data-stu-id="4a410-132">GetHeaders</span></span> 

<span data-ttu-id="4a410-133">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="4a410-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="4a410-134">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="4a410-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="4a410-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4a410-135">GetIterator</span></span> 

<span data-ttu-id="4a410-136">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="4a410-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="4a410-137">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="4a410-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="4a410-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="4a410-138">RemoveHeader</span></span> 

<span data-ttu-id="4a410-139">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4a410-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="4a410-140">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="4a410-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="4a410-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="4a410-141">SetHeader</span></span> 

<span data-ttu-id="4a410-142">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4a410-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="4a410-143">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="4a410-143">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

