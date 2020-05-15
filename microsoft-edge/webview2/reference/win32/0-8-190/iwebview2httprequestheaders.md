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
ms.openlocfilehash: aea00f37f28034e1b7a33d4fd11c5ed78f779d00
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652638"
---
# <span data-ttu-id="64ce6-104">interface IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="64ce6-104">interface IWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="64ce6-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="64ce6-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="64ce6-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="64ce6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="64ce6-107">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="64ce6-107">HTTP request headers.</span></span>

## <span data-ttu-id="64ce6-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="64ce6-108">Summary</span></span>

 <span data-ttu-id="64ce6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="64ce6-109">Members</span></span>                        | <span data-ttu-id="64ce6-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="64ce6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64ce6-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="64ce6-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="64ce6-112">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="64ce6-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="64ce6-113">Contém</span><span class="sxs-lookup"><span data-stu-id="64ce6-113">Contains</span></span>](#contains) | <span data-ttu-id="64ce6-114">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="64ce6-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="64ce6-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="64ce6-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="64ce6-116">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="64ce6-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="64ce6-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="64ce6-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="64ce6-118">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="64ce6-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="64ce6-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="64ce6-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="64ce6-120">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="64ce6-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="64ce6-121">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64ce6-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="64ce6-122">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="64ce6-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="64ce6-123">Parte</span><span class="sxs-lookup"><span data-stu-id="64ce6-123">Members</span></span>

#### <span data-ttu-id="64ce6-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="64ce6-124">GetHeader</span></span> 

<span data-ttu-id="64ce6-125">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="64ce6-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="64ce6-126">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="64ce6-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="64ce6-127">Contém</span><span class="sxs-lookup"><span data-stu-id="64ce6-127">Contains</span></span> 

<span data-ttu-id="64ce6-128">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="64ce6-128">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="64ce6-129">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="64ce6-129">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="64ce6-130">SetHeader</span><span class="sxs-lookup"><span data-stu-id="64ce6-130">SetHeader</span></span> 

<span data-ttu-id="64ce6-131">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="64ce6-131">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="64ce6-132">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="64ce6-132">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="64ce6-133">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="64ce6-133">RemoveHeader</span></span> 

<span data-ttu-id="64ce6-134">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="64ce6-134">Removes header that matches the name.</span></span>

> <span data-ttu-id="64ce6-135">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="64ce6-135">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="64ce6-136">GetIterator</span><span class="sxs-lookup"><span data-stu-id="64ce6-136">GetIterator</span></span> 

<span data-ttu-id="64ce6-137">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="64ce6-137">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="64ce6-138">público HRESULT [Getiteration](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="64ce6-138">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

