---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 97a0d8f2afda5f6391a574e6ad62fbd2e17abcc1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884936"
---
# <span data-ttu-id="86452-104">0.8.355-IWebView2ProcessFailedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="86452-104">0.8.355 - interface IWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="86452-105">O chamador implementa essa interface para receber eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="86452-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="86452-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="86452-106">Summary</span></span>

 <span data-ttu-id="86452-107">Parte</span><span class="sxs-lookup"><span data-stu-id="86452-107">Members</span></span>                        | <span data-ttu-id="86452-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="86452-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="86452-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="86452-109">Invoke</span></span>](#invoke) | <span data-ttu-id="86452-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="86452-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="86452-111">Parte</span><span class="sxs-lookup"><span data-stu-id="86452-111">Members</span></span>

#### <span data-ttu-id="86452-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="86452-112">Invoke</span></span> 

<span data-ttu-id="86452-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="86452-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="86452-114">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="86452-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span></span>

