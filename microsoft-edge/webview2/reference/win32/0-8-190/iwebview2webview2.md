---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 52218ddcbecdaf3bdb736af877493c85d4460c10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878040"
---
# <span data-ttu-id="688c1-104">0.8.355-IWebView2WebView2 de interface</span><span class="sxs-lookup"><span data-stu-id="688c1-104">0.8.355 - interface IWebView2WebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="688c1-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="688c1-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="688c1-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="688c1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="688c1-107">Funcionalidades adicionais implementadas pelo objeto WebView primário.</span><span class="sxs-lookup"><span data-stu-id="688c1-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="688c1-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="688c1-108">Summary</span></span>

 <span data-ttu-id="688c1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="688c1-109">Members</span></span>                        | <span data-ttu-id="688c1-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="688c1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="688c1-111">Parar</span><span class="sxs-lookup"><span data-stu-id="688c1-111">Stop</span></span>](#stop) | <span data-ttu-id="688c1-112">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="688c1-112">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="688c1-113">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="688c1-113">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="688c1-114">Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="688c1-114">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="688c1-115">Parte</span><span class="sxs-lookup"><span data-stu-id="688c1-115">Members</span></span>

#### <span data-ttu-id="688c1-116">Parar</span><span class="sxs-lookup"><span data-stu-id="688c1-116">Stop</span></span> 

<span data-ttu-id="688c1-117">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="688c1-117">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="688c1-118">público- [limite](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="688c1-118">public HRESULT [Stop](#stop)()</span></span>

