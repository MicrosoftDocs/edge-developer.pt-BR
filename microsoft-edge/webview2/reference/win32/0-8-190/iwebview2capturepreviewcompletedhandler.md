---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 9e8b1cc973eefbd41c1fac0d7d9723ba35ec7302
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878677"
---
# <span data-ttu-id="a2476-104">0.8.355-IWebView2CapturePreviewCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="a2476-104">0.8.355 - interface IWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a2476-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a2476-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a2476-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a2476-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a2476-107">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="a2476-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="a2476-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a2476-108">Summary</span></span>

 <span data-ttu-id="a2476-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a2476-109">Members</span></span>                        | <span data-ttu-id="a2476-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a2476-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a2476-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="a2476-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a2476-112">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="a2476-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="a2476-113">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="a2476-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="a2476-114">Parte</span><span class="sxs-lookup"><span data-stu-id="a2476-114">Members</span></span>

#### <span data-ttu-id="a2476-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="a2476-115">Invoke</span></span> 

<span data-ttu-id="a2476-116">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="a2476-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a2476-117">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="a2476-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

