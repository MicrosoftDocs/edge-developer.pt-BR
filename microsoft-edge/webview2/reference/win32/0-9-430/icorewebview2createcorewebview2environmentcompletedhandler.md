---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 5cc3ca23dcababc35a73b44a81c54439d0dbe1a3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884306"
---
# <span data-ttu-id="6271f-104">0.9.430-ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="6271f-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6271f-105">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="6271f-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="6271f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6271f-106">Summary</span></span>

 <span data-ttu-id="6271f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6271f-107">Members</span></span>                        | <span data-ttu-id="6271f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6271f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6271f-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="6271f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6271f-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6271f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6271f-111">Parte</span><span class="sxs-lookup"><span data-stu-id="6271f-111">Members</span></span>

#### <span data-ttu-id="6271f-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="6271f-112">Invoke</span></span> 

<span data-ttu-id="6271f-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="6271f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6271f-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="6271f-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span></span>

