---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: fe0c0fae0ec33cbc5ba50ca163b3f4fc8baa61b9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880952"
---
# <span data-ttu-id="6e940-104">0.9.430-ICoreWebView2MoveFocusRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="6e940-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="6e940-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6e940-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6e940-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="6e940-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="6e940-107">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="6e940-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="6e940-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="6e940-108">Summary</span></span>

 <span data-ttu-id="6e940-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6e940-109">Members</span></span>                        | <span data-ttu-id="6e940-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="6e940-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6e940-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="6e940-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="6e940-112">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="6e940-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="6e940-113">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6e940-113">get_Handled</span></span>](#get_handled) | <span data-ttu-id="6e940-114">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6e940-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="6e940-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6e940-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="6e940-116">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="6e940-116">Set the Handled property.</span></span>

## <span data-ttu-id="6e940-117">Parte</span><span class="sxs-lookup"><span data-stu-id="6e940-117">Members</span></span>

#### <span data-ttu-id="6e940-118">get_Reason</span><span class="sxs-lookup"><span data-stu-id="6e940-118">get_Reason</span></span> 

<span data-ttu-id="6e940-119">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="6e940-119">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="6e940-120">[get_Reason](#get_reason)público HRESULT (CORE_WEBVIEW2_MOVE_FOCUS_REASON \* valor)</span><span class="sxs-lookup"><span data-stu-id="6e940-120">public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="6e940-121">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6e940-121">get_Handled</span></span> 

<span data-ttu-id="6e940-122">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6e940-122">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="6e940-123">[get_Handled](#get_handled)público HRESULT (valor bool \*)</span><span class="sxs-lookup"><span data-stu-id="6e940-123">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="6e940-124">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="6e940-124">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="6e940-125">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="6e940-125">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="6e940-126">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="6e940-126">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="6e940-127">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="6e940-127">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="6e940-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6e940-128">put_Handled</span></span> 

<span data-ttu-id="6e940-129">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="6e940-129">Set the Handled property.</span></span>

> <span data-ttu-id="6e940-130">[put_Handled](#put_handled)público HRESULT (valor bool)</span><span class="sxs-lookup"><span data-stu-id="6e940-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

