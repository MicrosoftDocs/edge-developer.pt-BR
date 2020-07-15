---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 9dbf6ee630db1e99a74506f377fb4e01018c340f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877592"
---
# <span data-ttu-id="957ea-104">0.9.430-ICoreWebView2ProcessFailedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="957ea-104">0.9.430 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="957ea-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="957ea-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="957ea-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="957ea-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="957ea-107">O chamador implementa essa interface para receber eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="957ea-107">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="957ea-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="957ea-108">Summary</span></span>

 <span data-ttu-id="957ea-109">Parte</span><span class="sxs-lookup"><span data-stu-id="957ea-109">Members</span></span>                        | <span data-ttu-id="957ea-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="957ea-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="957ea-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="957ea-111">Invoke</span></span>](#invoke) | <span data-ttu-id="957ea-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="957ea-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="957ea-113">Parte</span><span class="sxs-lookup"><span data-stu-id="957ea-113">Members</span></span>

#### <span data-ttu-id="957ea-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="957ea-114">Invoke</span></span> 

<span data-ttu-id="957ea-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="957ea-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="957ea-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2ProcessFailedEventArgs](ICoreWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="957ea-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ProcessFailedEventArgs](ICoreWebView2ProcessFailedEventArgs.md) \* args)</span></span>

