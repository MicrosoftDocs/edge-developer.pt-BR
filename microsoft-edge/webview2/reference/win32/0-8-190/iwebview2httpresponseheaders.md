---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 077c85b2458c2cf843c4d2f0548d17ec01ba4751
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885958"
---
# <span data-ttu-id="be645-104">0.8.355-IWebView2HttpResponseHeaders de interface</span><span class="sxs-lookup"><span data-stu-id="be645-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="be645-105">Cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="be645-105">HTTP response headers.</span></span>

## <span data-ttu-id="be645-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="be645-106">Summary</span></span>

 <span data-ttu-id="be645-107">Parte</span><span class="sxs-lookup"><span data-stu-id="be645-107">Members</span></span>                        | <span data-ttu-id="be645-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="be645-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be645-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="be645-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="be645-110">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="be645-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="be645-111">Contém</span><span class="sxs-lookup"><span data-stu-id="be645-111">Contains</span></span>](#contains) | <span data-ttu-id="be645-112">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="be645-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="be645-113">Getheaders</span><span class="sxs-lookup"><span data-stu-id="be645-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="be645-114">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="be645-114">Gets the header values matching the name.</span></span>
[<span data-ttu-id="be645-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="be645-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="be645-116">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="be645-116">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="be645-117">Usado para construir um WebResourceResponse para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="be645-117">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="be645-118">Parte</span><span class="sxs-lookup"><span data-stu-id="be645-118">Members</span></span>

#### <span data-ttu-id="be645-119">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="be645-119">AppendHeader</span></span> 

<span data-ttu-id="be645-120">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="be645-120">Appends header line with name and value.</span></span>

> <span data-ttu-id="be645-121">Public HRESULT [AppendHeader](#appendheader)(nome LPCWSTR, valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="be645-121">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="be645-122">Contém</span><span class="sxs-lookup"><span data-stu-id="be645-122">Contains</span></span> 

<span data-ttu-id="be645-123">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="be645-123">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="be645-124">a Public HRESULT [contém](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="be645-124">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="be645-125">Getheaders</span><span class="sxs-lookup"><span data-stu-id="be645-125">GetHeaders</span></span> 

<span data-ttu-id="be645-126">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="be645-126">Gets the header values matching the name.</span></span>

> <span data-ttu-id="be645-127">público HRESULT [Getheaders](#getheaders)(LPCWSTR Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* Iteration)</span><span class="sxs-lookup"><span data-stu-id="be645-127">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="be645-128">GetIterator</span><span class="sxs-lookup"><span data-stu-id="be645-128">GetIterator</span></span> 

<span data-ttu-id="be645-129">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="be645-129">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="be645-130">público HRESULT [Getiteration](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="be645-130">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

