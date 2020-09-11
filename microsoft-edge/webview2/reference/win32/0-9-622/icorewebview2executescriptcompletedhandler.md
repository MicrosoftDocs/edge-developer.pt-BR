---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: 4a3b5999d38f74fb6b78063e32b3abb0cb59c6b6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011489"
---
# <span data-ttu-id="6cd71-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6cd71-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6cd71-105">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="6cd71-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="6cd71-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6cd71-106">Summary</span></span>

 <span data-ttu-id="6cd71-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6cd71-107">Members</span></span>                        | <span data-ttu-id="6cd71-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6cd71-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6cd71-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="6cd71-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6cd71-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6cd71-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6cd71-111">Parte</span><span class="sxs-lookup"><span data-stu-id="6cd71-111">Members</span></span>

#### <span data-ttu-id="6cd71-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="6cd71-112">Invoke</span></span> 

<span data-ttu-id="6cd71-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6cd71-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6cd71-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="6cd71-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

