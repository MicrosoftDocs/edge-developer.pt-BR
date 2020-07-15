---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 82b60e43d059cca25c9c3f44cf6136e32a4469ae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880658"
---
# <span data-ttu-id="4bc4a-104">0.9.515-ICoreWebView2ExecuteScriptCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="4bc4a-104">0.9.515 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4bc4a-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4bc4a-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="4bc4a-107">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="4bc4a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="4bc4a-108">Summary</span></span>

 <span data-ttu-id="4bc4a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4bc4a-109">Members</span></span>                        | <span data-ttu-id="4bc4a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="4bc4a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4bc4a-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="4bc4a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="4bc4a-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="4bc4a-113">Parte</span><span class="sxs-lookup"><span data-stu-id="4bc4a-113">Members</span></span>

#### <span data-ttu-id="4bc4a-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="4bc4a-114">Invoke</span></span> 

<span data-ttu-id="4bc4a-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="4bc4a-116">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="4bc4a-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

