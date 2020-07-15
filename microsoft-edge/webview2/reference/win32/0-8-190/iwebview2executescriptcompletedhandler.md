---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: ecd3215c343925614b81d5da96fbf996350fd5a5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878502"
---
# <span data-ttu-id="c7ff4-104">0.8.355-IWebView2ExecuteScriptCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="c7ff4-104">0.8.355 - interface IWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c7ff4-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="c7ff4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c7ff4-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="c7ff4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="c7ff4-107">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="c7ff4-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="c7ff4-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="c7ff4-108">Summary</span></span>

 <span data-ttu-id="c7ff4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c7ff4-109">Members</span></span>                        | <span data-ttu-id="c7ff4-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="c7ff4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c7ff4-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="c7ff4-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c7ff4-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="c7ff4-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="c7ff4-113">Parte</span><span class="sxs-lookup"><span data-stu-id="c7ff4-113">Members</span></span>

#### <span data-ttu-id="c7ff4-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="c7ff4-114">Invoke</span></span> 

<span data-ttu-id="c7ff4-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="c7ff4-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="c7ff4-116">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="c7ff4-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>

