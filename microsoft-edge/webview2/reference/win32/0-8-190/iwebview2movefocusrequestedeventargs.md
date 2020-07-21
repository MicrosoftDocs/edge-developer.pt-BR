---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 5d8d447bced6bbbb51ae33220e74ebcf47f11ce5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885918"
---
# <span data-ttu-id="99364-104">0.8.355-IWebView2MoveFocusRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="99364-104">0.8.355 - interface IWebView2MoveFocusRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="99364-105">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="99364-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="99364-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="99364-106">Summary</span></span>

 <span data-ttu-id="99364-107">Parte</span><span class="sxs-lookup"><span data-stu-id="99364-107">Members</span></span>                        | <span data-ttu-id="99364-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="99364-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99364-109">get_Reason</span><span class="sxs-lookup"><span data-stu-id="99364-109">get_Reason</span></span>](#get_reason) | <span data-ttu-id="99364-110">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="99364-110">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="99364-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="99364-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="99364-112">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99364-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="99364-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="99364-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="99364-114">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="99364-114">Set the Handled property.</span></span>

## <span data-ttu-id="99364-115">Parte</span><span class="sxs-lookup"><span data-stu-id="99364-115">Members</span></span>

#### <span data-ttu-id="99364-116">get_Reason</span><span class="sxs-lookup"><span data-stu-id="99364-116">get_Reason</span></span> 

<span data-ttu-id="99364-117">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="99364-117">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="99364-118">[get_Reason](#get_reason)público HRESULT (WEBVIEW2_MOVE_FOCUS_REASON \* valor)</span><span class="sxs-lookup"><span data-stu-id="99364-118">public HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="99364-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="99364-119">get_Handled</span></span> 

<span data-ttu-id="99364-120">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99364-120">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="99364-121">[get_Handled](#get_handled)público HRESULT (valor bool \*)</span><span class="sxs-lookup"><span data-stu-id="99364-121">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="99364-122">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="99364-122">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="99364-123">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="99364-123">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="99364-124">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="99364-124">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="99364-125">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="99364-125">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="99364-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="99364-126">put_Handled</span></span> 

<span data-ttu-id="99364-127">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="99364-127">Set the Handled property.</span></span>

> <span data-ttu-id="99364-128">[put_Handled](#put_handled)público HRESULT (valor bool)</span><span class="sxs-lookup"><span data-stu-id="99364-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

