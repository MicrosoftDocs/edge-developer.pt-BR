---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: fe84f29798b01aed2787559c717f2893c9eda7f9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885937"
---
# <span data-ttu-id="3ecb1-104">0.8.355-IWebView2MoveFocusRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="3ecb1-104">0.8.355 - interface IWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="3ecb1-105">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="3ecb1-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="3ecb1-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3ecb1-106">Summary</span></span>

 <span data-ttu-id="3ecb1-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3ecb1-107">Members</span></span>                        | <span data-ttu-id="3ecb1-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3ecb1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3ecb1-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3ecb1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3ecb1-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3ecb1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3ecb1-111">Parte</span><span class="sxs-lookup"><span data-stu-id="3ecb1-111">Members</span></span>

#### <span data-ttu-id="3ecb1-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="3ecb1-112">Invoke</span></span> 

<span data-ttu-id="3ecb1-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3ecb1-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3ecb1-114">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3ecb1-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

