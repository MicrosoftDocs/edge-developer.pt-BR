---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 1622d2c19159bca76e036408810e2ca145d30e85
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011496"
---
# <span data-ttu-id="4d674-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="4d674-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="4d674-105">Cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d674-105">HTTP response headers.</span></span>

## <span data-ttu-id="4d674-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4d674-106">Summary</span></span>

 <span data-ttu-id="4d674-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4d674-107">Members</span></span>                        | <span data-ttu-id="4d674-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4d674-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d674-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="4d674-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="4d674-110">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="4d674-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="4d674-111">Contém</span><span class="sxs-lookup"><span data-stu-id="4d674-111">Contains</span></span>](#contains) | <span data-ttu-id="4d674-112">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4d674-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="4d674-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4d674-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="4d674-114">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4d674-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="4d674-115">Getheaders</span><span class="sxs-lookup"><span data-stu-id="4d674-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="4d674-116">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="4d674-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="4d674-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4d674-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="4d674-118">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="4d674-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="4d674-119">Usado para construir um WebResourceResponse para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="4d674-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="4d674-120">Parte</span><span class="sxs-lookup"><span data-stu-id="4d674-120">Members</span></span>

#### <span data-ttu-id="4d674-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="4d674-121">AppendHeader</span></span> 

<span data-ttu-id="4d674-122">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="4d674-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="4d674-123">Public HRESULT [AppendHeader](#appendheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="4d674-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="4d674-124">Contém</span><span class="sxs-lookup"><span data-stu-id="4d674-124">Contains</span></span> 

<span data-ttu-id="4d674-125">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4d674-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="4d674-126">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="4d674-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="4d674-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4d674-127">GetHeader</span></span> 

<span data-ttu-id="4d674-128">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="4d674-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="4d674-129">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="4d674-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="4d674-130">Getheaders</span><span class="sxs-lookup"><span data-stu-id="4d674-130">GetHeaders</span></span> 

<span data-ttu-id="4d674-131">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="4d674-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="4d674-132">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="4d674-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="4d674-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4d674-133">GetIterator</span></span> 

<span data-ttu-id="4d674-134">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="4d674-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="4d674-135">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="4d674-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

