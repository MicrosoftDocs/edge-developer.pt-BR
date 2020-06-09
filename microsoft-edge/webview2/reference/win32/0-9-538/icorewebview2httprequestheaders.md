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
ms.openlocfilehash: 19018ff63b62b0d76bed6dcce9cf1dbce2a37b11
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698276"
---
# <span data-ttu-id="4e5e6-104">interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="4e5e6-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="4e5e6-105">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-105">HTTP request headers.</span></span>

## <span data-ttu-id="4e5e6-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4e5e6-106">Summary</span></span>

 <span data-ttu-id="4e5e6-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4e5e6-107">Members</span></span>                        | <span data-ttu-id="4e5e6-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4e5e6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4e5e6-109">Contém</span><span class="sxs-lookup"><span data-stu-id="4e5e6-109">Contains</span></span>](#contains) | <span data-ttu-id="4e5e6-110">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="4e5e6-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4e5e6-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="4e5e6-112">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="4e5e6-113">Getheaders</span><span class="sxs-lookup"><span data-stu-id="4e5e6-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="4e5e6-114">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="4e5e6-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4e5e6-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="4e5e6-116">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="4e5e6-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="4e5e6-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="4e5e6-118">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="4e5e6-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="4e5e6-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="4e5e6-120">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="4e5e6-121">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="4e5e6-122">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="4e5e6-123">Parte</span><span class="sxs-lookup"><span data-stu-id="4e5e6-123">Members</span></span>

#### <span data-ttu-id="4e5e6-124">Contém</span><span class="sxs-lookup"><span data-stu-id="4e5e6-124">Contains</span></span> 

<span data-ttu-id="4e5e6-125">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="4e5e6-126">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="4e5e6-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="4e5e6-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4e5e6-127">GetHeader</span></span> 

<span data-ttu-id="4e5e6-128">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="4e5e6-129">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="4e5e6-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="4e5e6-130">Getheaders</span><span class="sxs-lookup"><span data-stu-id="4e5e6-130">GetHeaders</span></span> 

<span data-ttu-id="4e5e6-131">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="4e5e6-132">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="4e5e6-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="4e5e6-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4e5e6-133">GetIterator</span></span> 

<span data-ttu-id="4e5e6-134">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="4e5e6-135">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="4e5e6-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="4e5e6-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="4e5e6-136">RemoveHeader</span></span> 

<span data-ttu-id="4e5e6-137">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="4e5e6-138">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="4e5e6-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="4e5e6-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="4e5e6-139">SetHeader</span></span> 

<span data-ttu-id="4e5e6-140">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4e5e6-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="4e5e6-141">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="4e5e6-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

