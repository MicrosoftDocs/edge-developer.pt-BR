---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: da7b12d382776bb1755e90b0ce1c2728b555c8c8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652658"
---
# <span data-ttu-id="e8138-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e8138-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e8138-105">O chamador implementa essa interface para receber o resultado do método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="e8138-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="e8138-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e8138-106">Summary</span></span>

 <span data-ttu-id="e8138-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e8138-107">Members</span></span>                        | <span data-ttu-id="e8138-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e8138-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e8138-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="e8138-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e8138-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e8138-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e8138-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e8138-111">Members</span></span>

#### <span data-ttu-id="e8138-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="e8138-112">Invoke</span></span> 

<span data-ttu-id="e8138-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e8138-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e8138-114">[chamada](#invoke)a Public HRESULT (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e8138-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

