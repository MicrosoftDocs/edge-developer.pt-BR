---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 772ad4ce7bd1ae0c1f02475206380c146ecabf7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885741"
---
# <span data-ttu-id="546bd-104">0.8.355-IWebView2WebMessageReceivedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="546bd-104">0.8.355 - interface IWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="546bd-105">O chamador implementa essa interface para receber o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="546bd-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="546bd-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="546bd-106">Summary</span></span>

 <span data-ttu-id="546bd-107">Parte</span><span class="sxs-lookup"><span data-stu-id="546bd-107">Members</span></span>                        | <span data-ttu-id="546bd-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="546bd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="546bd-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="546bd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="546bd-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="546bd-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="546bd-111">Parte</span><span class="sxs-lookup"><span data-stu-id="546bd-111">Members</span></span>

#### <span data-ttu-id="546bd-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="546bd-112">Invoke</span></span> 

<span data-ttu-id="546bd-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="546bd-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="546bd-114">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="546bd-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>

