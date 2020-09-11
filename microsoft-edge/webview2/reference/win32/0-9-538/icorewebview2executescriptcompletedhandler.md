---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: 0b257cef4ed4a85fcd41cd401ef00eea01a4d8b6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010226"
---
# <span data-ttu-id="911d3-104">0.9.579-ICoreWebView2ExecuteScriptCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="911d3-104">0.9.579 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="911d3-105">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="911d3-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="911d3-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="911d3-106">Summary</span></span>

 <span data-ttu-id="911d3-107">Parte</span><span class="sxs-lookup"><span data-stu-id="911d3-107">Members</span></span>                        | <span data-ttu-id="911d3-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="911d3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="911d3-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="911d3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="911d3-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="911d3-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="911d3-111">Parte</span><span class="sxs-lookup"><span data-stu-id="911d3-111">Members</span></span>

#### <span data-ttu-id="911d3-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="911d3-112">Invoke</span></span> 

<span data-ttu-id="911d3-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="911d3-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="911d3-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="911d3-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

