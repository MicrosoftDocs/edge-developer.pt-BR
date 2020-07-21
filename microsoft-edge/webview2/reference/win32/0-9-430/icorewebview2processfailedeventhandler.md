---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: ed9b94b5bd9015b07cf44cf2cbeec330688242ff
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884103"
---
# <span data-ttu-id="d1fc8-104">0.9.430-ICoreWebView2ProcessFailedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="d1fc8-104">0.9.430 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="d1fc8-105">O chamador implementa essa interface para receber eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="d1fc8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="d1fc8-106">Summary</span></span>

 <span data-ttu-id="d1fc8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="d1fc8-107">Members</span></span>                        | <span data-ttu-id="d1fc8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1fc8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d1fc8-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="d1fc8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d1fc8-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d1fc8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="d1fc8-111">Members</span></span>

#### <span data-ttu-id="d1fc8-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="d1fc8-112">Invoke</span></span> 

<span data-ttu-id="d1fc8-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d1fc8-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2ProcessFailedEventArgs](ICoreWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d1fc8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ProcessFailedEventArgs](ICoreWebView2ProcessFailedEventArgs.md) \* args)</span></span>

