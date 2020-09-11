---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
ms.openlocfilehash: 4cd8f4ab3904bd1a8c2277ba012bb5e6c32cf1d9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011122"
---
# <span data-ttu-id="6ec63-104">0.9.579-ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="6ec63-104">0.9.579 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6ec63-105">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="6ec63-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="6ec63-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6ec63-106">Summary</span></span>

 <span data-ttu-id="6ec63-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6ec63-107">Members</span></span>                        | <span data-ttu-id="6ec63-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6ec63-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6ec63-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="6ec63-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6ec63-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6ec63-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6ec63-111">Parte</span><span class="sxs-lookup"><span data-stu-id="6ec63-111">Members</span></span>

#### <span data-ttu-id="6ec63-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="6ec63-112">Invoke</span></span> 

<span data-ttu-id="6ec63-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6ec63-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6ec63-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="6ec63-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

