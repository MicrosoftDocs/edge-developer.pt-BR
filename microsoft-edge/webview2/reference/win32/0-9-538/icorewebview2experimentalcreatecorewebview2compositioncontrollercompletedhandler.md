---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: 8fc3efa6bf1ba9a9e721dcba67e8350ded38cc62
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011130"
---
# <span data-ttu-id="b7070-104">0.9.579-ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="b7070-104">0.9.579 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b7070-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="b7070-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="b7070-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b7070-106">Summary</span></span>

 <span data-ttu-id="b7070-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b7070-107">Members</span></span>                        | <span data-ttu-id="b7070-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b7070-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b7070-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="b7070-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b7070-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="b7070-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b7070-111">Parte</span><span class="sxs-lookup"><span data-stu-id="b7070-111">Members</span></span>

#### <span data-ttu-id="b7070-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="b7070-112">Invoke</span></span> 

<span data-ttu-id="b7070-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="b7070-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b7070-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="b7070-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

