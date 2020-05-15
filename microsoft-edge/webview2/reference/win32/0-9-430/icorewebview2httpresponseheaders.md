---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: b23b724977b9d164c48dc99d0da2e64d61539549
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652705"
---
# <span data-ttu-id="d2773-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="d2773-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="d2773-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d2773-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d2773-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="d2773-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="d2773-107">Cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d2773-107">HTTP response headers.</span></span>

## <span data-ttu-id="d2773-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d2773-108">Summary</span></span>

 <span data-ttu-id="d2773-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d2773-109">Members</span></span>                        | <span data-ttu-id="d2773-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d2773-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d2773-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="d2773-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="d2773-112">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="d2773-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="d2773-113">Contém</span><span class="sxs-lookup"><span data-stu-id="d2773-113">Contains</span></span>](#contains) | <span data-ttu-id="d2773-114">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d2773-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="d2773-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="d2773-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="d2773-116">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="d2773-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="d2773-117">Getheaders</span><span class="sxs-lookup"><span data-stu-id="d2773-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="d2773-118">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="d2773-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="d2773-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="d2773-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="d2773-120">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="d2773-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="d2773-121">Usado para construir um WebResourceResponse para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d2773-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="d2773-122">Parte</span><span class="sxs-lookup"><span data-stu-id="d2773-122">Members</span></span>

#### <span data-ttu-id="d2773-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="d2773-123">AppendHeader</span></span> 

<span data-ttu-id="d2773-124">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="d2773-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="d2773-125">Public HRESULT [AppendHeader](#appendheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d2773-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="d2773-126">Contém</span><span class="sxs-lookup"><span data-stu-id="d2773-126">Contains</span></span> 

<span data-ttu-id="d2773-127">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d2773-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="d2773-128">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="d2773-128">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="d2773-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="d2773-129">GetHeader</span></span> 

<span data-ttu-id="d2773-130">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="d2773-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="d2773-131">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="d2773-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="d2773-132">Getheaders</span><span class="sxs-lookup"><span data-stu-id="d2773-132">GetHeaders</span></span> 

<span data-ttu-id="d2773-133">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="d2773-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="d2773-134">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="d2773-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="d2773-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="d2773-135">GetIterator</span></span> 

<span data-ttu-id="d2773-136">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="d2773-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="d2773-137">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="d2773-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

