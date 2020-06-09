---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: a675bede2e1e509f3cfcc7490ac157da3f6d876c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698309"
---
# <span data-ttu-id="74228-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="74228-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="74228-105">O chamador implementa essa interface para receber os resultados da conclusão do CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="74228-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="74228-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="74228-106">Summary</span></span>

 <span data-ttu-id="74228-107">Parte</span><span class="sxs-lookup"><span data-stu-id="74228-107">Members</span></span>                        | <span data-ttu-id="74228-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="74228-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="74228-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="74228-109">Invoke</span></span>](#invoke) | <span data-ttu-id="74228-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="74228-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="74228-111">Parte</span><span class="sxs-lookup"><span data-stu-id="74228-111">Members</span></span>

#### <span data-ttu-id="74228-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="74228-112">Invoke</span></span> 

<span data-ttu-id="74228-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="74228-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="74228-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="74228-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

