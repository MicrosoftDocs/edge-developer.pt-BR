---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: c991e9e9520bd696c579fdca379295afe253ba5d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877508"
---
# <span data-ttu-id="adc82-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="adc82-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="adc82-105">O chamador implementa essa interface para receber os resultados da conclusão do CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="adc82-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="adc82-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="adc82-106">Summary</span></span>

 <span data-ttu-id="adc82-107">Parte</span><span class="sxs-lookup"><span data-stu-id="adc82-107">Members</span></span>                        | <span data-ttu-id="adc82-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="adc82-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="adc82-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="adc82-109">Invoke</span></span>](#invoke) | <span data-ttu-id="adc82-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="adc82-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="adc82-111">Parte</span><span class="sxs-lookup"><span data-stu-id="adc82-111">Members</span></span>

#### <span data-ttu-id="adc82-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="adc82-112">Invoke</span></span> 

<span data-ttu-id="adc82-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="adc82-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="adc82-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="adc82-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

