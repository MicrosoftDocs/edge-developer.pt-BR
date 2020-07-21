---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 1e0148c0d1e27cb4f1c52fb6ad55cc2e7613a94b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885965"
---
# <span data-ttu-id="1080b-104">0.8.355-IWebView2HttpRequestHeaders de interface</span><span class="sxs-lookup"><span data-stu-id="1080b-104">0.8.355 - interface IWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="1080b-105">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="1080b-105">HTTP request headers.</span></span>

## <span data-ttu-id="1080b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1080b-106">Summary</span></span>

 <span data-ttu-id="1080b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1080b-107">Members</span></span>                        | <span data-ttu-id="1080b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1080b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1080b-109">GetHeader</span><span class="sxs-lookup"><span data-stu-id="1080b-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="1080b-110">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="1080b-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="1080b-111">Contém</span><span class="sxs-lookup"><span data-stu-id="1080b-111">Contains</span></span>](#contains) | <span data-ttu-id="1080b-112">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="1080b-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="1080b-113">SetHeader</span><span class="sxs-lookup"><span data-stu-id="1080b-113">SetHeader</span></span>](#setheader) | <span data-ttu-id="1080b-114">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="1080b-114">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="1080b-115">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="1080b-115">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="1080b-116">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="1080b-116">Removes header that matches the name.</span></span>
[<span data-ttu-id="1080b-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="1080b-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="1080b-118">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="1080b-118">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="1080b-119">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="1080b-119">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="1080b-120">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="1080b-120">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="1080b-121">Parte</span><span class="sxs-lookup"><span data-stu-id="1080b-121">Members</span></span>

#### <span data-ttu-id="1080b-122">GetHeader</span><span class="sxs-lookup"><span data-stu-id="1080b-122">GetHeader</span></span> 

<span data-ttu-id="1080b-123">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="1080b-123">Gets the header value matching the name.</span></span>

> <span data-ttu-id="1080b-124">público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="1080b-124">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="1080b-125">Contém</span><span class="sxs-lookup"><span data-stu-id="1080b-125">Contains</span></span> 

<span data-ttu-id="1080b-126">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="1080b-126">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="1080b-127">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="1080b-127">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="1080b-128">SetHeader</span><span class="sxs-lookup"><span data-stu-id="1080b-128">SetHeader</span></span> 

<span data-ttu-id="1080b-129">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="1080b-129">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="1080b-130">Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="1080b-130">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="1080b-131">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="1080b-131">RemoveHeader</span></span> 

<span data-ttu-id="1080b-132">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="1080b-132">Removes header that matches the name.</span></span>

> <span data-ttu-id="1080b-133">Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="1080b-133">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="1080b-134">GetIterator</span><span class="sxs-lookup"><span data-stu-id="1080b-134">GetIterator</span></span> 

<span data-ttu-id="1080b-135">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="1080b-135">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="1080b-136">público HRESULT [Getiteration](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="1080b-136">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

