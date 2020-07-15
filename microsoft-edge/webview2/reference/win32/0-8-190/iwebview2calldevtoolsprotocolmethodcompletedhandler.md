---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 66ce887cd70b14d51091f630e9631783dc02d397
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878684"
---
# <span data-ttu-id="e1a7d-104">0.8.355-IWebView2CallDevToolsProtocolMethodCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="e1a7d-104">0.8.355 - interface IWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e1a7d-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e1a7d-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e1a7d-107">O chamador implementa essa interface para receber os resultados da conclusão do CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-107">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="e1a7d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e1a7d-108">Summary</span></span>

 <span data-ttu-id="e1a7d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e1a7d-109">Members</span></span>                        | <span data-ttu-id="e1a7d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e1a7d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1a7d-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="e1a7d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e1a7d-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e1a7d-113">Parte</span><span class="sxs-lookup"><span data-stu-id="e1a7d-113">Members</span></span>

#### <span data-ttu-id="e1a7d-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="e1a7d-114">Invoke</span></span> 

<span data-ttu-id="e1a7d-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e1a7d-116">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e1a7d-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>

