---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 1082ea61b98b953277219d78a2944a2487b47a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884432"
---
# <span data-ttu-id="c4cb7-104">0.9.515-ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="c4cb7-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="c4cb7-105">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="c4cb7-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="c4cb7-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c4cb7-106">Summary</span></span>

 <span data-ttu-id="c4cb7-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c4cb7-107">Members</span></span>                        | <span data-ttu-id="c4cb7-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c4cb7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4cb7-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="c4cb7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c4cb7-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="c4cb7-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="c4cb7-111">Parte</span><span class="sxs-lookup"><span data-stu-id="c4cb7-111">Members</span></span>

#### <span data-ttu-id="c4cb7-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="c4cb7-112">Invoke</span></span> 

<span data-ttu-id="c4cb7-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="c4cb7-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="c4cb7-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="c4cb7-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

