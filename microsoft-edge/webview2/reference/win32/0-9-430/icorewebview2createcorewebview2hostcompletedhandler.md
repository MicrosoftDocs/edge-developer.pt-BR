---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 9c2b5568e6a276b07dc91bd639c730b2009aa9e5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884278"
---
# <span data-ttu-id="9baf8-104">0.9.430-ICoreWebView2CreateCoreWebView2HostCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="9baf8-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9baf8-105">O chamador implementa essa interface para receber a CoreWebView2Host criada via CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="9baf8-105">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="9baf8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="9baf8-106">Summary</span></span>

 <span data-ttu-id="9baf8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="9baf8-107">Members</span></span>                        | <span data-ttu-id="9baf8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="9baf8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9baf8-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="9baf8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9baf8-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="9baf8-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="9baf8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="9baf8-111">Members</span></span>

#### <span data-ttu-id="9baf8-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="9baf8-112">Invoke</span></span> 

<span data-ttu-id="9baf8-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="9baf8-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9baf8-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="9baf8-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>

