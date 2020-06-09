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
ms.openlocfilehash: a3dde4581692fb30cada16d9166bda62a0d69179
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698279"
---
# <span data-ttu-id="90a0d-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="90a0d-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="90a0d-105">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="90a0d-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="90a0d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="90a0d-106">Summary</span></span>

 <span data-ttu-id="90a0d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="90a0d-107">Members</span></span>                        | <span data-ttu-id="90a0d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="90a0d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="90a0d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="90a0d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="90a0d-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="90a0d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="90a0d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="90a0d-111">Members</span></span>

#### <span data-ttu-id="90a0d-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="90a0d-112">Invoke</span></span> 

<span data-ttu-id="90a0d-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="90a0d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="90a0d-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="90a0d-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

