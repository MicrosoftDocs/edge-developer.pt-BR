---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2623dad17d8e8b34348bdb21a38e900c28eaeebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885440"
---
# <span data-ttu-id="d67e3-104">0.9.515-ICoreWebView2NewWindowRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="d67e3-104">0.9.515 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="d67e3-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d67e3-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="d67e3-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="d67e3-106">Summary</span></span>

 <span data-ttu-id="d67e3-107">Parte</span><span class="sxs-lookup"><span data-stu-id="d67e3-107">Members</span></span>                        | <span data-ttu-id="d67e3-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="d67e3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d67e3-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="d67e3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d67e3-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d67e3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d67e3-111">Parte</span><span class="sxs-lookup"><span data-stu-id="d67e3-111">Members</span></span>

#### <span data-ttu-id="d67e3-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="d67e3-112">Invoke</span></span> 

<span data-ttu-id="d67e3-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d67e3-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d67e3-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d67e3-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

