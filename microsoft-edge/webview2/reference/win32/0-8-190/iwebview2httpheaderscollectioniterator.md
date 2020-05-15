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
ms.openlocfilehash: 4b9ad48d9b09343bad04d4acbe7c49750e76427d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652709"
---
# <span data-ttu-id="1dafb-104">interface IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="1dafb-104">interface IWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="1dafb-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="1dafb-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="1dafb-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="1dafb-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="1dafb-107">Iterador para uma coleção de cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="1dafb-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="1dafb-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="1dafb-108">Summary</span></span>

 <span data-ttu-id="1dafb-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1dafb-109">Members</span></span>                        | <span data-ttu-id="1dafb-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="1dafb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1dafb-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="1dafb-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="1dafb-112">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="1dafb-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="1dafb-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="1dafb-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="1dafb-114">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="1dafb-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="1dafb-115">Consulte [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) e [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="1dafb-115">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="1dafb-116">Parte</span><span class="sxs-lookup"><span data-stu-id="1dafb-116">Members</span></span>

#### <span data-ttu-id="1dafb-117">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="1dafb-117">GetCurrentHeader</span></span> 

<span data-ttu-id="1dafb-118">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="1dafb-118">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="1dafb-119">Public HRESULT [GetCurrentHeader](#getcurrentheader)(nome LPWSTR \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="1dafb-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="1dafb-120">Esse método irá falhar se a última chamada para MoveNext definir has_next como FALSE.</span><span class="sxs-lookup"><span data-stu-id="1dafb-120">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="1dafb-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="1dafb-121">MoveNext</span></span> 

<span data-ttu-id="1dafb-122">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="1dafb-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="1dafb-123">público HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span><span class="sxs-lookup"><span data-stu-id="1dafb-123">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="1dafb-124">O parâmetro has_next será definido como FALSE se não houver mais cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="1dafb-124">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="1dafb-125">Após isso ocorrer, o método GetCurrentHeader falhará se chamado.</span><span class="sxs-lookup"><span data-stu-id="1dafb-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>

