---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 48a04ea60dff4cf9b6b52377927ee9085fb8bea2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878432"
---
# <span data-ttu-id="6aa53-104">0.8.355-IWebView2HttpResponseHeaders de interface</span><span class="sxs-lookup"><span data-stu-id="6aa53-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="6aa53-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="6aa53-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="6aa53-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="6aa53-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="6aa53-107">Cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6aa53-107">HTTP response headers.</span></span>

## <span data-ttu-id="6aa53-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="6aa53-108">Summary</span></span>

 <span data-ttu-id="6aa53-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6aa53-109">Members</span></span>                        | <span data-ttu-id="6aa53-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="6aa53-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6aa53-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="6aa53-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="6aa53-112">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="6aa53-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="6aa53-113">Contém</span><span class="sxs-lookup"><span data-stu-id="6aa53-113">Contains</span></span>](#contains) | <span data-ttu-id="6aa53-114">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6aa53-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="6aa53-115">Getheaders</span><span class="sxs-lookup"><span data-stu-id="6aa53-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="6aa53-116">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="6aa53-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="6aa53-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6aa53-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="6aa53-118">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="6aa53-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="6aa53-119">Usado para construir um WebResourceResponse para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="6aa53-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="6aa53-120">Parte</span><span class="sxs-lookup"><span data-stu-id="6aa53-120">Members</span></span>

#### <span data-ttu-id="6aa53-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="6aa53-121">AppendHeader</span></span> 

<span data-ttu-id="6aa53-122">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="6aa53-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="6aa53-123">Public HRESULT [AppendHeader](#appendheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="6aa53-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="6aa53-124">Contém</span><span class="sxs-lookup"><span data-stu-id="6aa53-124">Contains</span></span> 

<span data-ttu-id="6aa53-125">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6aa53-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="6aa53-126">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="6aa53-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="6aa53-127">Getheaders</span><span class="sxs-lookup"><span data-stu-id="6aa53-127">GetHeaders</span></span> 

<span data-ttu-id="6aa53-128">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="6aa53-128">Gets the header values matching the name.</span></span>

> <span data-ttu-id="6aa53-129">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="6aa53-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6aa53-130">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6aa53-130">GetIterator</span></span> 

<span data-ttu-id="6aa53-131">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="6aa53-131">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="6aa53-132">público HRESULT [Getiteration](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="6aa53-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

