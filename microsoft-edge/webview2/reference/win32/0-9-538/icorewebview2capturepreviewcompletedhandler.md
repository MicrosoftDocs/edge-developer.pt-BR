---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 290d82666e5b9c5062132e1eb7515e39e2deb978
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698307"
---
# <span data-ttu-id="dc9a6-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="dc9a6-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="dc9a6-105">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="dc9a6-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="dc9a6-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="dc9a6-106">Summary</span></span>

 <span data-ttu-id="dc9a6-107">Parte</span><span class="sxs-lookup"><span data-stu-id="dc9a6-107">Members</span></span>                        | <span data-ttu-id="dc9a6-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="dc9a6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc9a6-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="dc9a6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dc9a6-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="dc9a6-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="dc9a6-111">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="dc9a6-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="dc9a6-112">Parte</span><span class="sxs-lookup"><span data-stu-id="dc9a6-112">Members</span></span>

#### <span data-ttu-id="dc9a6-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="dc9a6-113">Invoke</span></span> 

<span data-ttu-id="dc9a6-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="dc9a6-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="dc9a6-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="dc9a6-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

