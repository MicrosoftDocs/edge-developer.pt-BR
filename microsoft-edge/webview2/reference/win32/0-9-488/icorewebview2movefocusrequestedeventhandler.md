---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 77ed5641aad191ee7d0cbbd9aa12a8b5e84bf7cd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880449"
---
# <span data-ttu-id="7a14f-104">0.9.515-ICoreWebView2MoveFocusRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="7a14f-104">0.9.515 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7a14f-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7a14f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7a14f-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="7a14f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="7a14f-107">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7a14f-107">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="7a14f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7a14f-108">Summary</span></span>

 <span data-ttu-id="7a14f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7a14f-109">Members</span></span>                        | <span data-ttu-id="7a14f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7a14f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a14f-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="7a14f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7a14f-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7a14f-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="7a14f-113">Parte</span><span class="sxs-lookup"><span data-stu-id="7a14f-113">Members</span></span>

#### <span data-ttu-id="7a14f-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="7a14f-114">Invoke</span></span> 

<span data-ttu-id="7a14f-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7a14f-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7a14f-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7a14f-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

