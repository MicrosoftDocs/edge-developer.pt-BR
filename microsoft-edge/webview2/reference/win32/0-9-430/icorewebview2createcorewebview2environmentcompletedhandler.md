---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 4cac9892e150f64b02b0a08c1164dcaa0aac4b7c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652518"
---
# <span data-ttu-id="6ada8-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6ada8-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="6ada8-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6ada8-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6ada8-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="6ada8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6ada8-107">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="6ada8-107">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="6ada8-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="6ada8-108">Summary</span></span>

 <span data-ttu-id="6ada8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6ada8-109">Members</span></span>                        | <span data-ttu-id="6ada8-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="6ada8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6ada8-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="6ada8-111">Invoke</span></span>](#invoke) | <span data-ttu-id="6ada8-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6ada8-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6ada8-113">Parte</span><span class="sxs-lookup"><span data-stu-id="6ada8-113">Members</span></span>

#### <span data-ttu-id="6ada8-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="6ada8-114">Invoke</span></span> 

<span data-ttu-id="6ada8-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6ada8-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6ada8-116">[chamada](#invoke)a Public HRESULT (resultado HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="6ada8-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span></span>

