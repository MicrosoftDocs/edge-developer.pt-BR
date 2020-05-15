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
ms.openlocfilehash: 793dbde462e25ae0bfe0dc0bc475cc49e7237fb2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652644"
---
# <span data-ttu-id="6a874-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6a874-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6a874-105">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="6a874-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="6a874-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6a874-106">Summary</span></span>

 <span data-ttu-id="6a874-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6a874-107">Members</span></span>                        | <span data-ttu-id="6a874-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6a874-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a874-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="6a874-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6a874-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6a874-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="6a874-111">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="6a874-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="6a874-112">Parte</span><span class="sxs-lookup"><span data-stu-id="6a874-112">Members</span></span>

#### <span data-ttu-id="6a874-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="6a874-113">Invoke</span></span> 

<span data-ttu-id="6a874-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6a874-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6a874-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="6a874-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

