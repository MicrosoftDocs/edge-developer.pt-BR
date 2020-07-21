---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: b8501c7287d5160f0fac980752721c83a0f48de7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886231"
---
# <span data-ttu-id="23448-104">0.8.355-IWebView2CallDevToolsProtocolMethodCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="23448-104">0.8.355 - interface IWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="23448-105">O chamador implementa essa interface para receber os resultados da conclusão do CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="23448-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="23448-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="23448-106">Summary</span></span>

 <span data-ttu-id="23448-107">Parte</span><span class="sxs-lookup"><span data-stu-id="23448-107">Members</span></span>                        | <span data-ttu-id="23448-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="23448-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="23448-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="23448-109">Invoke</span></span>](#invoke) | <span data-ttu-id="23448-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="23448-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="23448-111">Parte</span><span class="sxs-lookup"><span data-stu-id="23448-111">Members</span></span>

#### <span data-ttu-id="23448-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="23448-112">Invoke</span></span> 

<span data-ttu-id="23448-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="23448-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="23448-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="23448-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>

