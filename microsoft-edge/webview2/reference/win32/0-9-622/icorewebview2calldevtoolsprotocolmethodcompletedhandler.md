---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: f6c0037177843d65ce5fe7cc56f206d5661d4b2a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011611"
---
# <span data-ttu-id="f3bc0-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f3bc0-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f3bc0-105">O chamador implementa essa interface para receber os resultados da conclusão do CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="f3bc0-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f3bc0-106">Summary</span></span>

 <span data-ttu-id="f3bc0-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f3bc0-107">Members</span></span>                        | <span data-ttu-id="f3bc0-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f3bc0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f3bc0-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="f3bc0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f3bc0-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f3bc0-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f3bc0-111">Members</span></span>

#### <span data-ttu-id="f3bc0-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="f3bc0-112">Invoke</span></span> 

<span data-ttu-id="f3bc0-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f3bc0-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="f3bc0-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

