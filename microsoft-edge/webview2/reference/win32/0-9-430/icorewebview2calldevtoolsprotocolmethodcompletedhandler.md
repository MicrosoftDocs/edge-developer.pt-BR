---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: d7f44614e7322759446812481c9fa05c807b5eac
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652524"
---
# <span data-ttu-id="c23b9-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="c23b9-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c23b9-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c23b9-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c23b9-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="c23b9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="c23b9-107">O chamador implementa essa interface para receber os resultados da conclusão do CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="c23b9-107">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="c23b9-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="c23b9-108">Summary</span></span>

 <span data-ttu-id="c23b9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c23b9-109">Members</span></span>                        | <span data-ttu-id="c23b9-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="c23b9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c23b9-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="c23b9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c23b9-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="c23b9-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="c23b9-113">Parte</span><span class="sxs-lookup"><span data-stu-id="c23b9-113">Members</span></span>

#### <span data-ttu-id="c23b9-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="c23b9-114">Invoke</span></span> 

<span data-ttu-id="c23b9-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="c23b9-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="c23b9-116">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="c23b9-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>

