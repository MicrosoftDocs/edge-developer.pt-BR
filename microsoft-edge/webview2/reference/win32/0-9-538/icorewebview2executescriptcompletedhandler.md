---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: ee59ef42852fc8f0b0529b9a3ca08e53972dee1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879937"
---
# <span data-ttu-id="5e49f-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5e49f-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5e49f-105">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="5e49f-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="5e49f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5e49f-106">Summary</span></span>

 <span data-ttu-id="5e49f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5e49f-107">Members</span></span>                        | <span data-ttu-id="5e49f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5e49f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5e49f-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="5e49f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5e49f-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="5e49f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="5e49f-111">Parte</span><span class="sxs-lookup"><span data-stu-id="5e49f-111">Members</span></span>

#### <span data-ttu-id="5e49f-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="5e49f-112">Invoke</span></span> 

<span data-ttu-id="5e49f-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="5e49f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5e49f-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="5e49f-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

