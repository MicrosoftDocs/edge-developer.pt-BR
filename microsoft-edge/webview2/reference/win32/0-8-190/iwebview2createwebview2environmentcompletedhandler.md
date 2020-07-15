---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: fe81be15531cedae7a01355cbb6b6b27b52f15cc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878628"
---
# <span data-ttu-id="4a05c-104">0.8.355-IWebView2CreateWebView2EnvironmentCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="4a05c-104">0.8.355 - interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4a05c-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="4a05c-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="4a05c-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="4a05c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="4a05c-107">O chamador implementa essa interface para receber a WebView2Environment criada via CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="4a05c-107">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="4a05c-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="4a05c-108">Summary</span></span>

 <span data-ttu-id="4a05c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4a05c-109">Members</span></span>                        | <span data-ttu-id="4a05c-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="4a05c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4a05c-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="4a05c-111">Invoke</span></span>](#invoke) | <span data-ttu-id="4a05c-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="4a05c-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="4a05c-113">Parte</span><span class="sxs-lookup"><span data-stu-id="4a05c-113">Members</span></span>

#### <span data-ttu-id="4a05c-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="4a05c-114">Invoke</span></span> 

<span data-ttu-id="4a05c-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="4a05c-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="4a05c-116">[chamada](#invoke)a Public HRESULT (resultado HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="4a05c-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>

