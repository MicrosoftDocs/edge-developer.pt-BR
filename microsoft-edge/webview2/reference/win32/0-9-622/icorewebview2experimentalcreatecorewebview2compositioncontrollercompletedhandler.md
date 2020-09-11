---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: fd762c994d4c42e5e92dec09add2aa3b85b0ec80
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011487"
---
# <span data-ttu-id="d37a4-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="d37a4-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="d37a4-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="d37a4-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="d37a4-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="d37a4-106">Summary</span></span>

 <span data-ttu-id="d37a4-107">Parte</span><span class="sxs-lookup"><span data-stu-id="d37a4-107">Members</span></span>                        | <span data-ttu-id="d37a4-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="d37a4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d37a4-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="d37a4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d37a4-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="d37a4-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="d37a4-111">Parte</span><span class="sxs-lookup"><span data-stu-id="d37a4-111">Members</span></span>

#### <span data-ttu-id="d37a4-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="d37a4-112">Invoke</span></span> 

<span data-ttu-id="d37a4-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="d37a4-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="d37a4-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="d37a4-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

