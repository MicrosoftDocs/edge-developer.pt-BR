---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 4d1ce0723ecd1ce79cd2a3f95ccd5af9561e6f0b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878404"
---
# <span data-ttu-id="a342b-104">0.8.355-IWebView2NavigationCompletedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="a342b-104">0.8.355 - interface IWebView2NavigationCompletedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a342b-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a342b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a342b-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a342b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="a342b-107">O chamador implementa essa interface para receber o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="a342b-107">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="a342b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a342b-108">Summary</span></span>

 <span data-ttu-id="a342b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a342b-109">Members</span></span>                        | <span data-ttu-id="a342b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a342b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a342b-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="a342b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a342b-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a342b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a342b-113">Parte</span><span class="sxs-lookup"><span data-stu-id="a342b-113">Members</span></span>

#### <span data-ttu-id="a342b-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="a342b-114">Invoke</span></span> 

<span data-ttu-id="a342b-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a342b-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a342b-116">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a342b-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span></span>

