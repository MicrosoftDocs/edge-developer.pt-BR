---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 013a7076648b93bf259d28422f418365d988a586
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877431"
---
# <span data-ttu-id="68fef-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="68fef-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="68fef-105">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="68fef-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="68fef-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="68fef-106">Summary</span></span>

 <span data-ttu-id="68fef-107">Parte</span><span class="sxs-lookup"><span data-stu-id="68fef-107">Members</span></span>                        | <span data-ttu-id="68fef-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="68fef-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="68fef-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="68fef-109">Invoke</span></span>](#invoke) | <span data-ttu-id="68fef-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="68fef-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="68fef-111">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="68fef-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="68fef-112">Parte</span><span class="sxs-lookup"><span data-stu-id="68fef-112">Members</span></span>

#### <span data-ttu-id="68fef-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="68fef-113">Invoke</span></span> 

<span data-ttu-id="68fef-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="68fef-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="68fef-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="68fef-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

