---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 826bca5300957e9e135abb74cf591245b78b4644
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652723"
---
# <span data-ttu-id="3e333-104">interface IWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="3e333-104">interface IWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3e333-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3e333-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3e333-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="3e333-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="3e333-107">O chamador implementa essa interface para receber os resultados da conclusão do CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="3e333-107">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="3e333-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="3e333-108">Summary</span></span>

 <span data-ttu-id="3e333-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3e333-109">Members</span></span>                        | <span data-ttu-id="3e333-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="3e333-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3e333-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="3e333-111">Invoke</span></span>](#invoke) | <span data-ttu-id="3e333-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="3e333-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="3e333-113">Parte</span><span class="sxs-lookup"><span data-stu-id="3e333-113">Members</span></span>

#### <span data-ttu-id="3e333-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="3e333-114">Invoke</span></span> 

<span data-ttu-id="3e333-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="3e333-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="3e333-116">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="3e333-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>

