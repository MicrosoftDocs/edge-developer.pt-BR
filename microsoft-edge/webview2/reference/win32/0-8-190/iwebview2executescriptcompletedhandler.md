---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 9a075cf5e5d3e5222e76b9ba7550636a67e5696a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886007"
---
# <span data-ttu-id="7d9cb-104">0.8.355-IWebView2ExecuteScriptCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="7d9cb-104">0.8.355 - interface IWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7d9cb-105">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="7d9cb-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="7d9cb-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7d9cb-106">Summary</span></span>

 <span data-ttu-id="7d9cb-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7d9cb-107">Members</span></span>                        | <span data-ttu-id="7d9cb-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7d9cb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7d9cb-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="7d9cb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7d9cb-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="7d9cb-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7d9cb-111">Parte</span><span class="sxs-lookup"><span data-stu-id="7d9cb-111">Members</span></span>

#### <span data-ttu-id="7d9cb-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="7d9cb-112">Invoke</span></span> 

<span data-ttu-id="7d9cb-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="7d9cb-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7d9cb-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="7d9cb-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>

