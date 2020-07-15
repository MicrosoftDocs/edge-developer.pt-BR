---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
ms.openlocfilehash: c41da3c6f88c06d0642d00f38a8181acb079a009
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877403"
---
# <span data-ttu-id="be91f-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="be91f-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="be91f-105">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="be91f-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="be91f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="be91f-106">Summary</span></span>

 <span data-ttu-id="be91f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="be91f-107">Members</span></span>                        | <span data-ttu-id="be91f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="be91f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be91f-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="be91f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="be91f-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="be91f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="be91f-111">Parte</span><span class="sxs-lookup"><span data-stu-id="be91f-111">Members</span></span>

#### <span data-ttu-id="be91f-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="be91f-112">Invoke</span></span> 

<span data-ttu-id="be91f-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="be91f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="be91f-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="be91f-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

