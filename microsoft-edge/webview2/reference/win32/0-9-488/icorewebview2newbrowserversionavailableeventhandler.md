---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: aa59efbb0b47977b41236950c47a01d6d95ee123
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886283"
---
# <span data-ttu-id="f5ed1-104">0.9.515-ICoreWebView2NewBrowserVersionAvailableEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="f5ed1-104">0.9.515 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="f5ed1-105">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="f5ed1-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="f5ed1-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f5ed1-106">Summary</span></span>

 <span data-ttu-id="f5ed1-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f5ed1-107">Members</span></span>                        | <span data-ttu-id="f5ed1-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f5ed1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f5ed1-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="f5ed1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f5ed1-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f5ed1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f5ed1-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f5ed1-111">Members</span></span>

#### <span data-ttu-id="f5ed1-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="f5ed1-112">Invoke</span></span> 

<span data-ttu-id="f5ed1-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f5ed1-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f5ed1-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f5ed1-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

