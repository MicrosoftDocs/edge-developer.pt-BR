---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: e5df472e6b69b93fd41e73b96ae238176b64b6d9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878439"
---
# <span data-ttu-id="48169-104">0.8.355-IWebView2MoveFocusRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="48169-104">0.8.355 - interface IWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="48169-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="48169-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="48169-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="48169-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="48169-107">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="48169-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="48169-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="48169-108">Summary</span></span>

 <span data-ttu-id="48169-109">Parte</span><span class="sxs-lookup"><span data-stu-id="48169-109">Members</span></span>                        | <span data-ttu-id="48169-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="48169-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="48169-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="48169-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="48169-112">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="48169-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="48169-113">get_Handled</span><span class="sxs-lookup"><span data-stu-id="48169-113">get_Handled</span></span>](#get_handled) | <span data-ttu-id="48169-114">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48169-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="48169-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="48169-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="48169-116">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="48169-116">Set the Handled property.</span></span>

## <span data-ttu-id="48169-117">Parte</span><span class="sxs-lookup"><span data-stu-id="48169-117">Members</span></span>

#### <span data-ttu-id="48169-118">get_Reason</span><span class="sxs-lookup"><span data-stu-id="48169-118">get_Reason</span></span> 

<span data-ttu-id="48169-119">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="48169-119">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="48169-120">[get_Reason](#get_reason)público HRESULT (WEBVIEW2_MOVE_FOCUS_REASON \* valor)</span><span class="sxs-lookup"><span data-stu-id="48169-120">public HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="48169-121">get_Handled</span><span class="sxs-lookup"><span data-stu-id="48169-121">get_Handled</span></span> 

<span data-ttu-id="48169-122">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48169-122">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="48169-123">[get_Handled](#get_handled)público HRESULT (valor bool \*)</span><span class="sxs-lookup"><span data-stu-id="48169-123">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="48169-124">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="48169-124">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="48169-125">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="48169-125">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="48169-126">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="48169-126">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="48169-127">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="48169-127">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="48169-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="48169-128">put_Handled</span></span> 

<span data-ttu-id="48169-129">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="48169-129">Set the Handled property.</span></span>

> <span data-ttu-id="48169-130">[put_Handled](#put_handled)público HRESULT (valor bool)</span><span class="sxs-lookup"><span data-stu-id="48169-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

