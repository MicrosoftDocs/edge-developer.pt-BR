---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 06f7f664acb5f169215b603841d935730532b62b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652523"
---
# <span data-ttu-id="501c5-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="501c5-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="501c5-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="501c5-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="501c5-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="501c5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="501c5-107">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="501c5-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="501c5-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="501c5-108">Summary</span></span>

 <span data-ttu-id="501c5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="501c5-109">Members</span></span>                        | <span data-ttu-id="501c5-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="501c5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="501c5-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="501c5-111">Invoke</span></span>](#invoke) | <span data-ttu-id="501c5-112">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="501c5-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="501c5-113">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="501c5-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="501c5-114">Parte</span><span class="sxs-lookup"><span data-stu-id="501c5-114">Members</span></span>

#### <span data-ttu-id="501c5-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="501c5-115">Invoke</span></span> 

<span data-ttu-id="501c5-116">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="501c5-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="501c5-117">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="501c5-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

