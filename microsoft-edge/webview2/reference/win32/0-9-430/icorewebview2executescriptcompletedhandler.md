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
ms.openlocfilehash: 480b79cce673be530219718fb7f4920f5d1e80ae
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652680"
---
# <span data-ttu-id="78a3f-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="78a3f-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="78a3f-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="78a3f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="78a3f-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="78a3f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="78a3f-107">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="78a3f-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="78a3f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="78a3f-108">Summary</span></span>

 <span data-ttu-id="78a3f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="78a3f-109">Members</span></span>                        | <span data-ttu-id="78a3f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="78a3f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="78a3f-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="78a3f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="78a3f-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="78a3f-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="78a3f-113">Parte</span><span class="sxs-lookup"><span data-stu-id="78a3f-113">Members</span></span>

#### <span data-ttu-id="78a3f-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="78a3f-114">Invoke</span></span> 

<span data-ttu-id="78a3f-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="78a3f-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="78a3f-116">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="78a3f-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>

