---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: effceb6fafb062b1747f39876b8d2a5e02721aa8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697270"
---
# <span data-ttu-id="d41dd-104">interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="d41dd-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="d41dd-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="d41dd-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d41dd-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="d41dd-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="d41dd-107">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="d41dd-107">HTTP request headers.</span></span>

## <span data-ttu-id="d41dd-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d41dd-108">Summary</span></span>

 <span data-ttu-id="d41dd-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d41dd-109">Members</span></span>                        | <span data-ttu-id="d41dd-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d41dd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d41dd-111">Contém</span><span class="sxs-lookup"><span data-stu-id="d41dd-111">Contains</span></span>](#contains) | <span data-ttu-id="d41dd-112">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d41dd-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="d41dd-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="d41dd-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="d41dd-114">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="d41dd-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="d41dd-115">Getheaders</span><span class="sxs-lookup"><span data-stu-id="d41dd-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="d41dd-116">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="d41dd-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="d41dd-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="d41dd-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="d41dd-118">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="d41dd-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="d41dd-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="d41dd-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="d41dd-120">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="d41dd-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="d41dd-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="d41dd-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="d41dd-122">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="d41dd-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="d41dd-123">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d41dd-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="d41dd-124">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d41dd-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="d41dd-125">Parte</span><span class="sxs-lookup"><span data-stu-id="d41dd-125">Members</span></span>

#### <span data-ttu-id="d41dd-126">Contém</span><span class="sxs-lookup"><span data-stu-id="d41dd-126">Contains</span></span> 

<span data-ttu-id="d41dd-127">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d41dd-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="d41dd-128">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="d41dd-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="d41dd-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="d41dd-129">GetHeader</span></span> 

<span data-ttu-id="d41dd-130">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="d41dd-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="d41dd-131">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="d41dd-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="d41dd-132">Getheaders</span><span class="sxs-lookup"><span data-stu-id="d41dd-132">GetHeaders</span></span> 

<span data-ttu-id="d41dd-133">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="d41dd-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="d41dd-134">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="d41dd-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="d41dd-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="d41dd-135">GetIterator</span></span> 

<span data-ttu-id="d41dd-136">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="d41dd-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="d41dd-137">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="d41dd-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="d41dd-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="d41dd-138">RemoveHeader</span></span> 

<span data-ttu-id="d41dd-139">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="d41dd-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="d41dd-140">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d41dd-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="d41dd-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="d41dd-141">SetHeader</span></span> 

<span data-ttu-id="d41dd-142">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="d41dd-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="d41dd-143">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d41dd-143">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

