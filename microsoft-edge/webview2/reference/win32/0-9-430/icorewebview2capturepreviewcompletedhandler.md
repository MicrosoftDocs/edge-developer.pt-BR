---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 7e7a4173cec86cd6278d53074bff6a6e51b82710
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884313"
---
# <span data-ttu-id="686df-104">0.9.430-ICoreWebView2CapturePreviewCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="686df-104">0.9.430 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="686df-105">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="686df-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="686df-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="686df-106">Summary</span></span>

 <span data-ttu-id="686df-107">Parte</span><span class="sxs-lookup"><span data-stu-id="686df-107">Members</span></span>                        | <span data-ttu-id="686df-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="686df-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="686df-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="686df-109">Invoke</span></span>](#invoke) | <span data-ttu-id="686df-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="686df-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="686df-111">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="686df-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="686df-112">Parte</span><span class="sxs-lookup"><span data-stu-id="686df-112">Members</span></span>

#### <span data-ttu-id="686df-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="686df-113">Invoke</span></span> 

<span data-ttu-id="686df-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="686df-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="686df-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="686df-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

