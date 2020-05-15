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
ms.openlocfilehash: e12809d1db7e8c7764ad75e9a10f44ac3f445fa4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652503"
---
# <span data-ttu-id="ce57f-104">interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ce57f-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="ce57f-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="ce57f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="ce57f-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ce57f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="ce57f-107">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="ce57f-107">HTTP request headers.</span></span>

## <span data-ttu-id="ce57f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ce57f-108">Summary</span></span>

 <span data-ttu-id="ce57f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ce57f-109">Members</span></span>                        | <span data-ttu-id="ce57f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ce57f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ce57f-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="ce57f-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="ce57f-112">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="ce57f-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="ce57f-113">Getheaders</span><span class="sxs-lookup"><span data-stu-id="ce57f-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="ce57f-114">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="ce57f-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="ce57f-115">Contém</span><span class="sxs-lookup"><span data-stu-id="ce57f-115">Contains</span></span>](#contains) | <span data-ttu-id="ce57f-116">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ce57f-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="ce57f-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="ce57f-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="ce57f-118">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="ce57f-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="ce57f-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="ce57f-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="ce57f-120">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="ce57f-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="ce57f-121">GetIterator</span><span class="sxs-lookup"><span data-stu-id="ce57f-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="ce57f-122">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="ce57f-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="ce57f-123">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ce57f-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="ce57f-124">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ce57f-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="ce57f-125">Parte</span><span class="sxs-lookup"><span data-stu-id="ce57f-125">Members</span></span>

#### <span data-ttu-id="ce57f-126">GetHeader</span><span class="sxs-lookup"><span data-stu-id="ce57f-126">GetHeader</span></span> 

<span data-ttu-id="ce57f-127">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="ce57f-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="ce57f-128">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ce57f-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="ce57f-129">Getheaders</span><span class="sxs-lookup"><span data-stu-id="ce57f-129">GetHeaders</span></span> 

<span data-ttu-id="ce57f-130">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="ce57f-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="ce57f-131">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="ce57f-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="ce57f-132">Contém</span><span class="sxs-lookup"><span data-stu-id="ce57f-132">Contains</span></span> 

<span data-ttu-id="ce57f-133">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ce57f-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="ce57f-134">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="ce57f-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="ce57f-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="ce57f-135">SetHeader</span></span> 

<span data-ttu-id="ce57f-136">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="ce57f-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="ce57f-137">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ce57f-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="ce57f-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="ce57f-138">RemoveHeader</span></span> 

<span data-ttu-id="ce57f-139">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="ce57f-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="ce57f-140">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ce57f-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="ce57f-141">GetIterator</span><span class="sxs-lookup"><span data-stu-id="ce57f-141">GetIterator</span></span> 

<span data-ttu-id="ce57f-142">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="ce57f-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="ce57f-143">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="ce57f-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

