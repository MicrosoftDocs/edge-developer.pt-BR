---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 162d6dde904868ad6a4864b81c0ca76d50638c06
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878453"
---
# <span data-ttu-id="865ce-104">0.8.355-IWebView2HttpRequestHeaders de interface</span><span class="sxs-lookup"><span data-stu-id="865ce-104">0.8.355 - interface IWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="865ce-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="865ce-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="865ce-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="865ce-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="865ce-107">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="865ce-107">HTTP request headers.</span></span>

## <span data-ttu-id="865ce-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="865ce-108">Summary</span></span>

 <span data-ttu-id="865ce-109">Parte</span><span class="sxs-lookup"><span data-stu-id="865ce-109">Members</span></span>                        | <span data-ttu-id="865ce-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="865ce-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="865ce-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="865ce-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="865ce-112">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="865ce-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="865ce-113">Contém</span><span class="sxs-lookup"><span data-stu-id="865ce-113">Contains</span></span>](#contains) | <span data-ttu-id="865ce-114">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="865ce-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="865ce-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="865ce-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="865ce-116">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="865ce-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="865ce-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="865ce-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="865ce-118">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="865ce-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="865ce-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="865ce-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="865ce-120">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="865ce-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="865ce-121">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="865ce-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="865ce-122">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="865ce-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="865ce-123">Parte</span><span class="sxs-lookup"><span data-stu-id="865ce-123">Members</span></span>

#### <span data-ttu-id="865ce-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="865ce-124">GetHeader</span></span> 

<span data-ttu-id="865ce-125">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="865ce-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="865ce-126">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="865ce-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="865ce-127">Contém</span><span class="sxs-lookup"><span data-stu-id="865ce-127">Contains</span></span> 

<span data-ttu-id="865ce-128">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="865ce-128">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="865ce-129">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="865ce-129">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="865ce-130">SetHeader</span><span class="sxs-lookup"><span data-stu-id="865ce-130">SetHeader</span></span> 

<span data-ttu-id="865ce-131">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="865ce-131">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="865ce-132">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="865ce-132">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="865ce-133">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="865ce-133">RemoveHeader</span></span> 

<span data-ttu-id="865ce-134">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="865ce-134">Removes header that matches the name.</span></span>

> <span data-ttu-id="865ce-135">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="865ce-135">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="865ce-136">GetIterator</span><span class="sxs-lookup"><span data-stu-id="865ce-136">GetIterator</span></span> 

<span data-ttu-id="865ce-137">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="865ce-137">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="865ce-138">público HRESULT [Getiteration](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="865ce-138">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

