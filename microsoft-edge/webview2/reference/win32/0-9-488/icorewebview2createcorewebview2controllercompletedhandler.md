---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 49b2baf825d65b97b4b1fa62d06b2f6d6b7bd26d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652627"
---
# <span data-ttu-id="3424d-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="3424d-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="3424d-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="3424d-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="3424d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3424d-106">Summary</span></span>

 <span data-ttu-id="3424d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3424d-107">Members</span></span>                        | <span data-ttu-id="3424d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3424d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3424d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3424d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3424d-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="3424d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="3424d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="3424d-111">Members</span></span>

#### <span data-ttu-id="3424d-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="3424d-112">Invoke</span></span> 

<span data-ttu-id="3424d-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="3424d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="3424d-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="3424d-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

