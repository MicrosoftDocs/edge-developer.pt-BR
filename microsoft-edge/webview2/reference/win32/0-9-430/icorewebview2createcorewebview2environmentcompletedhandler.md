---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: b1ef893b559933d3cc507b09257a884b8646046d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877991"
---
# <span data-ttu-id="04bf1-104">0.9.430-ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="04bf1-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="04bf1-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="04bf1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="04bf1-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="04bf1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="04bf1-107">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="04bf1-107">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="04bf1-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="04bf1-108">Summary</span></span>

 <span data-ttu-id="04bf1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="04bf1-109">Members</span></span>                        | <span data-ttu-id="04bf1-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="04bf1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04bf1-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="04bf1-111">Invoke</span></span>](#invoke) | <span data-ttu-id="04bf1-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="04bf1-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="04bf1-113">Parte</span><span class="sxs-lookup"><span data-stu-id="04bf1-113">Members</span></span>

#### <span data-ttu-id="04bf1-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="04bf1-114">Invoke</span></span> 

<span data-ttu-id="04bf1-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="04bf1-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="04bf1-116">[chamada](#invoke)a Public HRESULT (resultado HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="04bf1-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span></span>

