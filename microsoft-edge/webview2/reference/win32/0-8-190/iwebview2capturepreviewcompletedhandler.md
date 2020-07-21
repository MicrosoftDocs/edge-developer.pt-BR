---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 991c09167ba3fe382c74d6244c76ffae25d628a6
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886189"
---
# <span data-ttu-id="b2d02-104">0.8.355-IWebView2CapturePreviewCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="b2d02-104">0.8.355 - interface IWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b2d02-105">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="b2d02-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="b2d02-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b2d02-106">Summary</span></span>

 <span data-ttu-id="b2d02-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b2d02-107">Members</span></span>                        | <span data-ttu-id="b2d02-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b2d02-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b2d02-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="b2d02-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b2d02-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="b2d02-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="b2d02-111">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="b2d02-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="b2d02-112">Parte</span><span class="sxs-lookup"><span data-stu-id="b2d02-112">Members</span></span>

#### <span data-ttu-id="b2d02-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="b2d02-113">Invoke</span></span> 

<span data-ttu-id="b2d02-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="b2d02-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b2d02-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="b2d02-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

