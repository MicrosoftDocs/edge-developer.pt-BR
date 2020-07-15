---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: bacd1cff4406caffd4d7c3e1ca4c3e320c051443
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878320"
---
# <span data-ttu-id="fcce0-104">0.8.355-IWebView2NewWindowRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="fcce0-104">0.8.355 - interface IWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="fcce0-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="fcce0-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="fcce0-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="fcce0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="fcce0-107">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="fcce0-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="fcce0-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="fcce0-108">Summary</span></span>

 <span data-ttu-id="fcce0-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fcce0-109">Members</span></span>                        | <span data-ttu-id="fcce0-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="fcce0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fcce0-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="fcce0-111">Invoke</span></span>](#invoke) | <span data-ttu-id="fcce0-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="fcce0-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fcce0-113">Parte</span><span class="sxs-lookup"><span data-stu-id="fcce0-113">Members</span></span>

#### <span data-ttu-id="fcce0-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="fcce0-114">Invoke</span></span> 

<span data-ttu-id="fcce0-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="fcce0-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fcce0-116">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fcce0-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>

