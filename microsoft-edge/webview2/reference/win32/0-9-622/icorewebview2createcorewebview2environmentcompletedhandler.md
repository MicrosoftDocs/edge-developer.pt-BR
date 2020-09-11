---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
ms.openlocfilehash: 3f6b6b9a2d4df2a450b4589c351c3ea98f7cc28f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011601"
---
# <span data-ttu-id="c71be-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="c71be-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="c71be-105">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="c71be-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="c71be-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c71be-106">Summary</span></span>

 <span data-ttu-id="c71be-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c71be-107">Members</span></span>                        | <span data-ttu-id="c71be-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c71be-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c71be-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="c71be-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c71be-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="c71be-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="c71be-111">Parte</span><span class="sxs-lookup"><span data-stu-id="c71be-111">Members</span></span>

#### <span data-ttu-id="c71be-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="c71be-112">Invoke</span></span> 

<span data-ttu-id="c71be-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="c71be-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="c71be-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, [ICoreWebView2Environment](icorewebview2environment.md) \* createdEnvironment)</span><span class="sxs-lookup"><span data-stu-id="c71be-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2Environment](icorewebview2environment.md) \* createdEnvironment)</span></span>

