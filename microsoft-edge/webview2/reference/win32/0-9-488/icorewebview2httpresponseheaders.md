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
ms.openlocfilehash: fe03c3ab6d951ecd54bd76cd7abc89de637496ea
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652574"
---
# <span data-ttu-id="b0742-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="b0742-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="b0742-105">Cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0742-105">HTTP response headers.</span></span>

## <span data-ttu-id="b0742-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b0742-106">Summary</span></span>

 <span data-ttu-id="b0742-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b0742-107">Members</span></span>                        | <span data-ttu-id="b0742-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b0742-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b0742-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="b0742-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="b0742-110">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="b0742-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="b0742-111">Contém</span><span class="sxs-lookup"><span data-stu-id="b0742-111">Contains</span></span>](#contains) | <span data-ttu-id="b0742-112">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b0742-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="b0742-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="b0742-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="b0742-114">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="b0742-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="b0742-115">Getheaders</span><span class="sxs-lookup"><span data-stu-id="b0742-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="b0742-116">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="b0742-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="b0742-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="b0742-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="b0742-118">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="b0742-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="b0742-119">Usado para construir um WebResourceResponse para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b0742-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="b0742-120">Parte</span><span class="sxs-lookup"><span data-stu-id="b0742-120">Members</span></span>

#### <span data-ttu-id="b0742-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="b0742-121">AppendHeader</span></span> 

<span data-ttu-id="b0742-122">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="b0742-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="b0742-123">Public HRESULT [AppendHeader](#appendheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b0742-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="b0742-124">Contém</span><span class="sxs-lookup"><span data-stu-id="b0742-124">Contains</span></span> 

<span data-ttu-id="b0742-125">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b0742-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="b0742-126">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="b0742-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="b0742-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="b0742-127">GetHeader</span></span> 

<span data-ttu-id="b0742-128">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="b0742-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="b0742-129">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="b0742-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="b0742-130">Getheaders</span><span class="sxs-lookup"><span data-stu-id="b0742-130">GetHeaders</span></span> 

<span data-ttu-id="b0742-131">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="b0742-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="b0742-132">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="b0742-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="b0742-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="b0742-133">GetIterator</span></span> 

<span data-ttu-id="b0742-134">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="b0742-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="b0742-135">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="b0742-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

