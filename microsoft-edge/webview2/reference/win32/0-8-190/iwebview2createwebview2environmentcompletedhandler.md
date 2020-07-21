---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 9937fe08f440ce468f178e4ac17935bbb8a1a8ed
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886168"
---
# <span data-ttu-id="be6ee-104">0.8.355-IWebView2CreateWebView2EnvironmentCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="be6ee-104">0.8.355 - interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="be6ee-105">O chamador implementa essa interface para receber a WebView2Environment criada via CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="be6ee-105">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="be6ee-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="be6ee-106">Summary</span></span>

 <span data-ttu-id="be6ee-107">Parte</span><span class="sxs-lookup"><span data-stu-id="be6ee-107">Members</span></span>                        | <span data-ttu-id="be6ee-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="be6ee-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be6ee-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="be6ee-109">Invoke</span></span>](#invoke) | <span data-ttu-id="be6ee-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="be6ee-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="be6ee-111">Parte</span><span class="sxs-lookup"><span data-stu-id="be6ee-111">Members</span></span>

#### <span data-ttu-id="be6ee-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="be6ee-112">Invoke</span></span> 

<span data-ttu-id="be6ee-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="be6ee-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="be6ee-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="be6ee-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>

