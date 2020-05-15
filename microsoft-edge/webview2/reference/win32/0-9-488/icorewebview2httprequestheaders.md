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
ms.openlocfilehash: 9f04e05ef77801a571771257f4a5e48077c373fd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652489"
---
# <span data-ttu-id="21f2c-104">interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="21f2c-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="21f2c-105">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="21f2c-105">HTTP request headers.</span></span>

## <span data-ttu-id="21f2c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="21f2c-106">Summary</span></span>

 <span data-ttu-id="21f2c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="21f2c-107">Members</span></span>                        | <span data-ttu-id="21f2c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="21f2c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21f2c-109">Contém</span><span class="sxs-lookup"><span data-stu-id="21f2c-109">Contains</span></span>](#contains) | <span data-ttu-id="21f2c-110">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="21f2c-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="21f2c-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="21f2c-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="21f2c-112">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="21f2c-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="21f2c-113">Getheaders</span><span class="sxs-lookup"><span data-stu-id="21f2c-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="21f2c-114">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="21f2c-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="21f2c-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="21f2c-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="21f2c-116">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="21f2c-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="21f2c-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="21f2c-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="21f2c-118">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="21f2c-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="21f2c-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="21f2c-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="21f2c-120">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="21f2c-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="21f2c-121">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="21f2c-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="21f2c-122">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="21f2c-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="21f2c-123">Parte</span><span class="sxs-lookup"><span data-stu-id="21f2c-123">Members</span></span>

#### <span data-ttu-id="21f2c-124">Contém</span><span class="sxs-lookup"><span data-stu-id="21f2c-124">Contains</span></span> 

<span data-ttu-id="21f2c-125">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="21f2c-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="21f2c-126">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="21f2c-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="21f2c-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="21f2c-127">GetHeader</span></span> 

<span data-ttu-id="21f2c-128">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="21f2c-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="21f2c-129">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="21f2c-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="21f2c-130">Getheaders</span><span class="sxs-lookup"><span data-stu-id="21f2c-130">GetHeaders</span></span> 

<span data-ttu-id="21f2c-131">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="21f2c-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="21f2c-132">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="21f2c-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="21f2c-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="21f2c-133">GetIterator</span></span> 

<span data-ttu-id="21f2c-134">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="21f2c-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="21f2c-135">público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="21f2c-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="21f2c-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="21f2c-136">RemoveHeader</span></span> 

<span data-ttu-id="21f2c-137">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="21f2c-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="21f2c-138">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="21f2c-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="21f2c-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="21f2c-139">SetHeader</span></span> 

<span data-ttu-id="21f2c-140">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="21f2c-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="21f2c-141">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="21f2c-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

