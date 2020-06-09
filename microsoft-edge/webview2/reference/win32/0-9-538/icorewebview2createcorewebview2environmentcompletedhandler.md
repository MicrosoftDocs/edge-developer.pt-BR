---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: dbc1a3e05f9cdc5b5ced2e0b7d489b06392e6100
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698292"
---
# <span data-ttu-id="13165-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="13165-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="13165-105">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="13165-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="13165-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="13165-106">Summary</span></span>

 <span data-ttu-id="13165-107">Parte</span><span class="sxs-lookup"><span data-stu-id="13165-107">Members</span></span>                        | <span data-ttu-id="13165-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="13165-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="13165-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="13165-109">Invoke</span></span>](#invoke) | <span data-ttu-id="13165-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="13165-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="13165-111">Parte</span><span class="sxs-lookup"><span data-stu-id="13165-111">Members</span></span>

#### <span data-ttu-id="13165-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="13165-112">Invoke</span></span> 

<span data-ttu-id="13165-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="13165-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="13165-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="13165-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

