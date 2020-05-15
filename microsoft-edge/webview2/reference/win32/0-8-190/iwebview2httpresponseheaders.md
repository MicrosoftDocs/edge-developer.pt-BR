---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 0f3564fa96bc1c13527cbf3b26ce92114d44eae4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652552"
---
# <span data-ttu-id="ed3ee-104">interface IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="ed3ee-104">interface IWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="ed3ee-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="ed3ee-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="ed3ee-107">Cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-107">HTTP response headers.</span></span>

## <span data-ttu-id="ed3ee-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ed3ee-108">Summary</span></span>

 <span data-ttu-id="ed3ee-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ed3ee-109">Members</span></span>                        | <span data-ttu-id="ed3ee-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ed3ee-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ed3ee-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="ed3ee-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="ed3ee-112">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="ed3ee-113">Contém</span><span class="sxs-lookup"><span data-stu-id="ed3ee-113">Contains</span></span>](#contains) | <span data-ttu-id="ed3ee-114">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="ed3ee-115">Getheaders</span><span class="sxs-lookup"><span data-stu-id="ed3ee-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="ed3ee-116">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="ed3ee-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="ed3ee-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="ed3ee-118">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="ed3ee-119">Usado para construir um WebResourceResponse para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="ed3ee-120">Parte</span><span class="sxs-lookup"><span data-stu-id="ed3ee-120">Members</span></span>

#### <span data-ttu-id="ed3ee-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="ed3ee-121">AppendHeader</span></span> 

<span data-ttu-id="ed3ee-122">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="ed3ee-123">Public HRESULT [AppendHeader](#appendheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ed3ee-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="ed3ee-124">Contém</span><span class="sxs-lookup"><span data-stu-id="ed3ee-124">Contains</span></span> 

<span data-ttu-id="ed3ee-125">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="ed3ee-126">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="ed3ee-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="ed3ee-127">Getheaders</span><span class="sxs-lookup"><span data-stu-id="ed3ee-127">GetHeaders</span></span> 

<span data-ttu-id="ed3ee-128">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-128">Gets the header values matching the name.</span></span>

> <span data-ttu-id="ed3ee-129">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="ed3ee-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="ed3ee-130">GetIterator</span><span class="sxs-lookup"><span data-stu-id="ed3ee-130">GetIterator</span></span> 

<span data-ttu-id="ed3ee-131">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="ed3ee-131">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="ed3ee-132">público HRESULT [Getiteration](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="ed3ee-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

