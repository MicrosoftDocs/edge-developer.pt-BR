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
ms.openlocfilehash: da49c1762ad7b7f3f366754bb9b05b7d16b861b7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652623"
---
# <span data-ttu-id="21972-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="21972-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="21972-105">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="21972-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="21972-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="21972-106">Summary</span></span>

 <span data-ttu-id="21972-107">Parte</span><span class="sxs-lookup"><span data-stu-id="21972-107">Members</span></span>                        | <span data-ttu-id="21972-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="21972-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21972-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="21972-109">Invoke</span></span>](#invoke) | <span data-ttu-id="21972-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="21972-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="21972-111">Parte</span><span class="sxs-lookup"><span data-stu-id="21972-111">Members</span></span>

#### <span data-ttu-id="21972-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="21972-112">Invoke</span></span> 

<span data-ttu-id="21972-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="21972-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="21972-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="21972-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

