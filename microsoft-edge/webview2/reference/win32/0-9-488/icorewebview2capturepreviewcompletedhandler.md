---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 6aaac0d062d0e97d3ec0c87bec243c5cf682ad6f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697046"
---
# <span data-ttu-id="0f67d-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="0f67d-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0f67d-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="0f67d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="0f67d-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="0f67d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="0f67d-107">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="0f67d-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="0f67d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="0f67d-108">Summary</span></span>

 <span data-ttu-id="0f67d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0f67d-109">Members</span></span>                        | <span data-ttu-id="0f67d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="0f67d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0f67d-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="0f67d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0f67d-112">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="0f67d-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="0f67d-113">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="0f67d-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="0f67d-114">Parte</span><span class="sxs-lookup"><span data-stu-id="0f67d-114">Members</span></span>

#### <span data-ttu-id="0f67d-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="0f67d-115">Invoke</span></span> 

<span data-ttu-id="0f67d-116">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="0f67d-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="0f67d-117">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="0f67d-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

