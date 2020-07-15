---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: e26d711c24758f82d42067fa28e71bc6ac1177ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877410"
---
# <span data-ttu-id="84d0d-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="84d0d-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="84d0d-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="84d0d-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="84d0d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="84d0d-106">Summary</span></span>

 <span data-ttu-id="84d0d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="84d0d-107">Members</span></span>                        | <span data-ttu-id="84d0d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="84d0d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="84d0d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="84d0d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="84d0d-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="84d0d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="84d0d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="84d0d-111">Members</span></span>

#### <span data-ttu-id="84d0d-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="84d0d-112">Invoke</span></span> 

<span data-ttu-id="84d0d-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="84d0d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="84d0d-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="84d0d-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

