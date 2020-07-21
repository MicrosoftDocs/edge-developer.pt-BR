---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: f85444231cb04857326d1662b2b4fb957e5305fe
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884495"
---
# <span data-ttu-id="3f7b9-104">0.9.515-ICoreWebView2CreateCoreWebView2ControllerCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="3f7b9-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="3f7b9-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="3f7b9-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3f7b9-106">Summary</span></span>

 <span data-ttu-id="3f7b9-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3f7b9-107">Members</span></span>                        | <span data-ttu-id="3f7b9-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3f7b9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f7b9-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3f7b9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3f7b9-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="3f7b9-111">Parte</span><span class="sxs-lookup"><span data-stu-id="3f7b9-111">Members</span></span>

#### <span data-ttu-id="3f7b9-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="3f7b9-112">Invoke</span></span> 

<span data-ttu-id="3f7b9-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="3f7b9-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="3f7b9-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

