---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: dc6c904150605dc05b2fef00600785b9840f0eb8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880525"
---
# <span data-ttu-id="fc399-104">0.9.515-ICoreWebView2MoveFocusRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="fc399-104">0.9.515 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="fc399-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="fc399-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="fc399-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="fc399-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="fc399-107">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="fc399-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="fc399-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="fc399-108">Summary</span></span>

 <span data-ttu-id="fc399-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fc399-109">Members</span></span>                        | <span data-ttu-id="fc399-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="fc399-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc399-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="fc399-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="fc399-112">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc399-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="fc399-113">get_Reason</span><span class="sxs-lookup"><span data-stu-id="fc399-113">get_Reason</span></span>](#get_reason) | <span data-ttu-id="fc399-114">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="fc399-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="fc399-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="fc399-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="fc399-116">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="fc399-116">Set the Handled property.</span></span>

## <span data-ttu-id="fc399-117">Parte</span><span class="sxs-lookup"><span data-stu-id="fc399-117">Members</span></span>

#### <span data-ttu-id="fc399-118">get_Handled</span><span class="sxs-lookup"><span data-stu-id="fc399-118">get_Handled</span></span> 

<span data-ttu-id="fc399-119">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc399-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="fc399-120">[get_Handled](#get_handled)público HRESULT (valor bool \*)</span><span class="sxs-lookup"><span data-stu-id="fc399-120">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="fc399-121">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="fc399-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="fc399-122">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="fc399-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="fc399-123">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="fc399-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="fc399-124">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="fc399-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="fc399-125">get_Reason</span><span class="sxs-lookup"><span data-stu-id="fc399-125">get_Reason</span></span> 

<span data-ttu-id="fc399-126">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="fc399-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="fc399-127">[get_Reason](#get_reason)público HRESULT (COREWEBVIEW2_MOVE_FOCUS_REASON \* valor)</span><span class="sxs-lookup"><span data-stu-id="fc399-127">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="fc399-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="fc399-128">put_Handled</span></span> 

<span data-ttu-id="fc399-129">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="fc399-129">Set the Handled property.</span></span>

> <span data-ttu-id="fc399-130">[put_Handled](#put_handled)público HRESULT (valor bool)</span><span class="sxs-lookup"><span data-stu-id="fc399-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

