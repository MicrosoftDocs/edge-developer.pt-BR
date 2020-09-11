---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: e526b723f111d7212a5da4b25840c89b69eb2e52
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011424"
---
# <span data-ttu-id="9b63b-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="9b63b-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9b63b-105">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="9b63b-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="9b63b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="9b63b-106">Summary</span></span>

 <span data-ttu-id="9b63b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="9b63b-107">Members</span></span>                        | <span data-ttu-id="9b63b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="9b63b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9b63b-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="9b63b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9b63b-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="9b63b-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="9b63b-111">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="9b63b-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="9b63b-112">Parte</span><span class="sxs-lookup"><span data-stu-id="9b63b-112">Members</span></span>

#### <span data-ttu-id="9b63b-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="9b63b-113">Invoke</span></span> 

<span data-ttu-id="9b63b-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="9b63b-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9b63b-115">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode)</span><span class="sxs-lookup"><span data-stu-id="9b63b-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>

