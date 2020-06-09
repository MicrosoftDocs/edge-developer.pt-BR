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
ms.openlocfilehash: 92eab98dfbd5f4c9239a5263e524daa2e7346eb5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698277"
---
# <span data-ttu-id="ba73b-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ba73b-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ba73b-105">Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="ba73b-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ba73b-106">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="ba73b-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="ba73b-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="ba73b-107">Summary</span></span>

 <span data-ttu-id="ba73b-108">Parte</span><span class="sxs-lookup"><span data-stu-id="ba73b-108">Members</span></span>                        | <span data-ttu-id="ba73b-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="ba73b-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ba73b-110">Invocar</span><span class="sxs-lookup"><span data-stu-id="ba73b-110">Invoke</span></span>](#invoke) | <span data-ttu-id="ba73b-111">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="ba73b-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ba73b-112">Parte</span><span class="sxs-lookup"><span data-stu-id="ba73b-112">Members</span></span>

#### <span data-ttu-id="ba73b-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="ba73b-113">Invoke</span></span> 

<span data-ttu-id="ba73b-114">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="ba73b-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ba73b-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="ba73b-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

