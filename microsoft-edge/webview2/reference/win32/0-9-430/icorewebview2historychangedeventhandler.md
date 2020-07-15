---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 6afd1983b90b4412fd3011dc35f192809a9583b7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881015"
---
# <span data-ttu-id="21a24-104">0.9.430-ICoreWebView2HistoryChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="21a24-104">0.9.430 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="21a24-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="21a24-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="21a24-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="21a24-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="21a24-107">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="21a24-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="21a24-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="21a24-108">Summary</span></span>

 <span data-ttu-id="21a24-109">Parte</span><span class="sxs-lookup"><span data-stu-id="21a24-109">Members</span></span>                        | <span data-ttu-id="21a24-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="21a24-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21a24-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="21a24-111">Invoke</span></span>](#invoke) | <span data-ttu-id="21a24-112">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="21a24-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="21a24-113">Parte</span><span class="sxs-lookup"><span data-stu-id="21a24-113">Members</span></span>

#### <span data-ttu-id="21a24-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="21a24-114">Invoke</span></span> 

<span data-ttu-id="21a24-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="21a24-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="21a24-116">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="21a24-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>

