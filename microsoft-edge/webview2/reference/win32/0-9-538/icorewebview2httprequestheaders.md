---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 7a59511e9d899fe4a66f2671f67f7c7cd7f101df
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011314"
---
# <span data-ttu-id="6be31-104">0.9.579-ICoreWebView2HttpRequestHeaders de interface</span><span class="sxs-lookup"><span data-stu-id="6be31-104">0.9.579 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="6be31-105">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="6be31-105">HTTP request headers.</span></span>

## <span data-ttu-id="6be31-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6be31-106">Summary</span></span>

 <span data-ttu-id="6be31-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6be31-107">Members</span></span>                        | <span data-ttu-id="6be31-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6be31-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6be31-109">Contém</span><span class="sxs-lookup"><span data-stu-id="6be31-109">Contains</span></span>](#contains) | <span data-ttu-id="6be31-110">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6be31-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="6be31-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6be31-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="6be31-112">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="6be31-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="6be31-113">Getheaders</span><span class="sxs-lookup"><span data-stu-id="6be31-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="6be31-114">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="6be31-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="6be31-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6be31-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="6be31-116">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="6be31-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="6be31-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="6be31-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="6be31-118">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="6be31-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="6be31-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="6be31-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="6be31-120">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="6be31-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="6be31-121">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6be31-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="6be31-122">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6be31-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="6be31-123">Parte</span><span class="sxs-lookup"><span data-stu-id="6be31-123">Members</span></span>

#### <span data-ttu-id="6be31-124">Contém</span><span class="sxs-lookup"><span data-stu-id="6be31-124">Contains</span></span> 

<span data-ttu-id="6be31-125">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6be31-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="6be31-126">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="6be31-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="6be31-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6be31-127">GetHeader</span></span> 

<span data-ttu-id="6be31-128">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="6be31-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="6be31-129">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="6be31-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="6be31-130">Getheaders</span><span class="sxs-lookup"><span data-stu-id="6be31-130">GetHeaders</span></span> 

<span data-ttu-id="6be31-131">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="6be31-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="6be31-132">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="6be31-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6be31-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6be31-133">GetIterator</span></span> 

<span data-ttu-id="6be31-134">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="6be31-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="6be31-135">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="6be31-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6be31-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="6be31-136">RemoveHeader</span></span> 

<span data-ttu-id="6be31-137">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="6be31-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="6be31-138">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="6be31-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="6be31-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="6be31-139">SetHeader</span></span> 

<span data-ttu-id="6be31-140">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="6be31-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="6be31-141">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="6be31-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

