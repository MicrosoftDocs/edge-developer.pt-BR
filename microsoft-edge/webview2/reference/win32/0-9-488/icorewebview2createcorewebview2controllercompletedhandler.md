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
ms.openlocfilehash: 0fb633a45df15c5b5116d69f74f6d12894bc91c1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698089"
---
# <span data-ttu-id="44b83-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="44b83-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="44b83-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="44b83-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="44b83-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="44b83-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="44b83-107">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="44b83-107">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="44b83-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="44b83-108">Summary</span></span>

 <span data-ttu-id="44b83-109">Parte</span><span class="sxs-lookup"><span data-stu-id="44b83-109">Members</span></span>                        | <span data-ttu-id="44b83-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="44b83-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="44b83-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="44b83-111">Invoke</span></span>](#invoke) | <span data-ttu-id="44b83-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="44b83-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="44b83-113">Parte</span><span class="sxs-lookup"><span data-stu-id="44b83-113">Members</span></span>

#### <span data-ttu-id="44b83-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="44b83-114">Invoke</span></span> 

<span data-ttu-id="44b83-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="44b83-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="44b83-116">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="44b83-116">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

