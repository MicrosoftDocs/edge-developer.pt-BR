---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: dbcc5b10ce1973df61554f3f27174f600fb25280
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885978"
---
# <span data-ttu-id="cf54c-104">0.8.355-IWebView2HttpHeadersCollectionIterator de interface</span><span class="sxs-lookup"><span data-stu-id="cf54c-104">0.8.355 - interface IWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="cf54c-105">Iterador para uma coleção de cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="cf54c-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="cf54c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="cf54c-106">Summary</span></span>

 <span data-ttu-id="cf54c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="cf54c-107">Members</span></span>                        | <span data-ttu-id="cf54c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="cf54c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf54c-109">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="cf54c-109">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="cf54c-110">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="cf54c-110">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="cf54c-111">MoveNext</span><span class="sxs-lookup"><span data-stu-id="cf54c-111">MoveNext</span></span>](#movenext) | <span data-ttu-id="cf54c-112">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="cf54c-112">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="cf54c-113">Consulte [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) e [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="cf54c-113">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="cf54c-114">Parte</span><span class="sxs-lookup"><span data-stu-id="cf54c-114">Members</span></span>

#### <span data-ttu-id="cf54c-115">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="cf54c-115">GetCurrentHeader</span></span> 

<span data-ttu-id="cf54c-116">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="cf54c-116">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="cf54c-117">Public HRESULT [GetCurrentHeader](#getcurrentheader)(nome LPWSTR \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="cf54c-117">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="cf54c-118">Esse método irá falhar se a última chamada para MoveNext definir has_next como FALSE.</span><span class="sxs-lookup"><span data-stu-id="cf54c-118">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="cf54c-119">MoveNext</span><span class="sxs-lookup"><span data-stu-id="cf54c-119">MoveNext</span></span> 

<span data-ttu-id="cf54c-120">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="cf54c-120">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="cf54c-121">público HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span><span class="sxs-lookup"><span data-stu-id="cf54c-121">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="cf54c-122">O parâmetro has_next será definido como FALSE se não houver mais cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="cf54c-122">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="cf54c-123">Após isso ocorrer, o método GetCurrentHeader falhará se chamado.</span><span class="sxs-lookup"><span data-stu-id="cf54c-123">After this occurs the GetCurrentHeader method will fail if called.</span></span>

