---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebViewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 381f46c6682a77905d9caa720e4ba9b2d1d531b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886142"
---
# <span data-ttu-id="e1084-104">0.8.355-IWebView2CreateWebViewCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="e1084-104">0.8.355 - interface IWebView2CreateWebViewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e1084-105">O chamador implementa essa interface para receber a WebView criada via WebView.</span><span class="sxs-lookup"><span data-stu-id="e1084-105">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="e1084-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e1084-106">Summary</span></span>

 <span data-ttu-id="e1084-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e1084-107">Members</span></span>                        | <span data-ttu-id="e1084-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e1084-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1084-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="e1084-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e1084-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e1084-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e1084-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e1084-111">Members</span></span>

#### <span data-ttu-id="e1084-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="e1084-112">Invoke</span></span> 

<span data-ttu-id="e1084-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e1084-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e1084-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT,[IWebView2WebView](IWebView2WebView.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="e1084-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>

