---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 7a983d313e242cc163fb16a9c0d0068a9d6663d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883928"
---
# <span data-ttu-id="d9475-104">0.9.515-ICoreWebView2CallDevToolsProtocolMethodCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="d9475-104">0.9.515 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="d9475-105">O chamador implementa essa interface para receber os resultados da conclusão do CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="d9475-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="d9475-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="d9475-106">Summary</span></span>

 <span data-ttu-id="d9475-107">Parte</span><span class="sxs-lookup"><span data-stu-id="d9475-107">Members</span></span>                        | <span data-ttu-id="d9475-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="d9475-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9475-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="d9475-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d9475-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="d9475-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="d9475-111">Parte</span><span class="sxs-lookup"><span data-stu-id="d9475-111">Members</span></span>

#### <span data-ttu-id="d9475-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="d9475-112">Invoke</span></span> 

<span data-ttu-id="d9475-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="d9475-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="d9475-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="d9475-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

