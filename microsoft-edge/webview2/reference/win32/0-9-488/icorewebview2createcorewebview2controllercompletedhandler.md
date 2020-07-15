---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 9baf172a112f7fa84dae3a38cdbc0b0e0324473f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880798"
---
# <span data-ttu-id="f5d97-104">0.9.515-ICoreWebView2CreateCoreWebView2ControllerCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="f5d97-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f5d97-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f5d97-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f5d97-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="f5d97-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f5d97-107">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="f5d97-107">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="f5d97-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f5d97-108">Summary</span></span>

 <span data-ttu-id="f5d97-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f5d97-109">Members</span></span>                        | <span data-ttu-id="f5d97-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="f5d97-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f5d97-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="f5d97-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f5d97-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="f5d97-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f5d97-113">Parte</span><span class="sxs-lookup"><span data-stu-id="f5d97-113">Members</span></span>

#### <span data-ttu-id="f5d97-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="f5d97-114">Invoke</span></span> 

<span data-ttu-id="f5d97-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="f5d97-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f5d97-116">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="f5d97-116">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

