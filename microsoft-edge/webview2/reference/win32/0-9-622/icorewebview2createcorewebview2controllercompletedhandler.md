---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 845c3a3f0241fb66032ecf818c484b6110258327
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011602"
---
# <span data-ttu-id="f4fb5-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f4fb5-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f4fb5-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="f4fb5-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="f4fb5-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f4fb5-106">Summary</span></span>

 <span data-ttu-id="f4fb5-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f4fb5-107">Members</span></span>                        | <span data-ttu-id="f4fb5-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f4fb5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f4fb5-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="f4fb5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f4fb5-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="f4fb5-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f4fb5-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f4fb5-111">Members</span></span>

#### <span data-ttu-id="f4fb5-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="f4fb5-112">Invoke</span></span> 

<span data-ttu-id="f4fb5-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="f4fb5-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f4fb5-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="f4fb5-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

