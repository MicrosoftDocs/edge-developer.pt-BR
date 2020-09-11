---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 8455db6adccf2d3d10e9934fee940d00bba7377c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011497"
---
# <span data-ttu-id="8c333-104">interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="8c333-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="8c333-105">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c333-105">HTTP request headers.</span></span>

## <span data-ttu-id="8c333-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="8c333-106">Summary</span></span>

 <span data-ttu-id="8c333-107">Parte</span><span class="sxs-lookup"><span data-stu-id="8c333-107">Members</span></span>                        | <span data-ttu-id="8c333-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="8c333-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8c333-109">Contém</span><span class="sxs-lookup"><span data-stu-id="8c333-109">Contains</span></span>](#contains) | <span data-ttu-id="8c333-110">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="8c333-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="8c333-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="8c333-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="8c333-112">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="8c333-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="8c333-113">Getheaders</span><span class="sxs-lookup"><span data-stu-id="8c333-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="8c333-114">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="8c333-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="8c333-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="8c333-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="8c333-116">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="8c333-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="8c333-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="8c333-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="8c333-118">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="8c333-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="8c333-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="8c333-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="8c333-120">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="8c333-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="8c333-121">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="8c333-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="8c333-122">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="8c333-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="8c333-123">Parte</span><span class="sxs-lookup"><span data-stu-id="8c333-123">Members</span></span>

#### <span data-ttu-id="8c333-124">Contém</span><span class="sxs-lookup"><span data-stu-id="8c333-124">Contains</span></span> 

<span data-ttu-id="8c333-125">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="8c333-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="8c333-126">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="8c333-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="8c333-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="8c333-127">GetHeader</span></span> 

<span data-ttu-id="8c333-128">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="8c333-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="8c333-129">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="8c333-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="8c333-130">Getheaders</span><span class="sxs-lookup"><span data-stu-id="8c333-130">GetHeaders</span></span> 

<span data-ttu-id="8c333-131">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="8c333-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="8c333-132">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="8c333-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="8c333-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="8c333-133">GetIterator</span></span> 

<span data-ttu-id="8c333-134">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="8c333-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="8c333-135">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="8c333-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="8c333-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="8c333-136">RemoveHeader</span></span> 

<span data-ttu-id="8c333-137">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="8c333-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="8c333-138">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="8c333-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="8c333-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="8c333-139">SetHeader</span></span> 

<span data-ttu-id="8c333-140">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="8c333-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="8c333-141">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="8c333-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

