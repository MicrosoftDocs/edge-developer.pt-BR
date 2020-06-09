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
ms.openlocfilehash: 63044cae80aebfb1e759070ec797673b0c9378d2
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697249"
---
# <span data-ttu-id="c148e-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="c148e-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="c148e-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c148e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c148e-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="c148e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="c148e-107">Cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="c148e-107">HTTP response headers.</span></span>

## <span data-ttu-id="c148e-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="c148e-108">Summary</span></span>

 <span data-ttu-id="c148e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c148e-109">Members</span></span>                        | <span data-ttu-id="c148e-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="c148e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c148e-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="c148e-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="c148e-112">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="c148e-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="c148e-113">Contém</span><span class="sxs-lookup"><span data-stu-id="c148e-113">Contains</span></span>](#contains) | <span data-ttu-id="c148e-114">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c148e-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="c148e-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="c148e-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="c148e-116">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="c148e-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="c148e-117">Getheaders</span><span class="sxs-lookup"><span data-stu-id="c148e-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="c148e-118">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="c148e-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="c148e-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="c148e-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="c148e-120">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="c148e-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="c148e-121">Usado para construir um WebResourceResponse para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c148e-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="c148e-122">Parte</span><span class="sxs-lookup"><span data-stu-id="c148e-122">Members</span></span>

#### <span data-ttu-id="c148e-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="c148e-123">AppendHeader</span></span> 

<span data-ttu-id="c148e-124">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="c148e-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="c148e-125">Public HRESULT [AppendHeader](#appendheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="c148e-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="c148e-126">Contém</span><span class="sxs-lookup"><span data-stu-id="c148e-126">Contains</span></span> 

<span data-ttu-id="c148e-127">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c148e-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="c148e-128">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="c148e-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="c148e-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="c148e-129">GetHeader</span></span> 

<span data-ttu-id="c148e-130">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="c148e-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="c148e-131">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="c148e-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="c148e-132">Getheaders</span><span class="sxs-lookup"><span data-stu-id="c148e-132">GetHeaders</span></span> 

<span data-ttu-id="c148e-133">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="c148e-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="c148e-134">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="c148e-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="c148e-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="c148e-135">GetIterator</span></span> 

<span data-ttu-id="c148e-136">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="c148e-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="c148e-137">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="c148e-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

