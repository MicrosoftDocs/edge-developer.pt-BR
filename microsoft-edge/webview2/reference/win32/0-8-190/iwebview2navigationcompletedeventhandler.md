---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: cf799ae12b977f66bfba4d1b7664e3abc6241304
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885916"
---
# <span data-ttu-id="6255c-104">0.8.355-IWebView2NavigationCompletedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="6255c-104">0.8.355 - interface IWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="6255c-105">O chamador implementa essa interface para receber o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="6255c-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="6255c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6255c-106">Summary</span></span>

 <span data-ttu-id="6255c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6255c-107">Members</span></span>                        | <span data-ttu-id="6255c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6255c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6255c-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="6255c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6255c-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6255c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6255c-111">Parte</span><span class="sxs-lookup"><span data-stu-id="6255c-111">Members</span></span>

#### <span data-ttu-id="6255c-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="6255c-112">Invoke</span></span> 

<span data-ttu-id="6255c-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6255c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6255c-114">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="6255c-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span></span>

