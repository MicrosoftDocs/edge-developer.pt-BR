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
ms.openlocfilehash: e838c851df54a7af5e4afe6352abef6d1044c8be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698082"
---
# <span data-ttu-id="8bc98-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8bc98-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8bc98-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="8bc98-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="8bc98-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="8bc98-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="8bc98-107">O chamador implementa essa interface para receber a WebView2Environment criada via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="8bc98-107">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="8bc98-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="8bc98-108">Summary</span></span>

 <span data-ttu-id="8bc98-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8bc98-109">Members</span></span>                        | <span data-ttu-id="8bc98-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="8bc98-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8bc98-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="8bc98-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8bc98-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="8bc98-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="8bc98-113">Parte</span><span class="sxs-lookup"><span data-stu-id="8bc98-113">Members</span></span>

#### <span data-ttu-id="8bc98-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="8bc98-114">Invoke</span></span> 

<span data-ttu-id="8bc98-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="8bc98-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="8bc98-116">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="8bc98-116">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

