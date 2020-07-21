---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 9a96e18b8c0b56cd75d4f0fe7b0c90c0634fe68b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884194"
---
# <span data-ttu-id="e3ef8-104">0.9.430-ICoreWebView2ExecuteScriptCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="e3ef8-104">0.9.430 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e3ef8-105">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="e3ef8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e3ef8-106">Summary</span></span>

 <span data-ttu-id="e3ef8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e3ef8-107">Members</span></span>                        | <span data-ttu-id="e3ef8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e3ef8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e3ef8-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="e3ef8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e3ef8-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e3ef8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e3ef8-111">Members</span></span>

#### <span data-ttu-id="e3ef8-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="e3ef8-112">Invoke</span></span> 

<span data-ttu-id="e3ef8-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e3ef8-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e3ef8-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>

