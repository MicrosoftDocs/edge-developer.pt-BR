---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: de0319060b6e618c30fc685815bcbcc41e8c3005
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697844"
---
# <span data-ttu-id="a10da-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a10da-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a10da-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a10da-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a10da-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a10da-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="a10da-107">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="a10da-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="a10da-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a10da-108">Summary</span></span>

 <span data-ttu-id="a10da-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a10da-109">Members</span></span>                        | <span data-ttu-id="a10da-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a10da-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a10da-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a10da-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="a10da-112">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a10da-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="a10da-113">get_Reason</span><span class="sxs-lookup"><span data-stu-id="a10da-113">get_Reason</span></span>](#get_reason) | <span data-ttu-id="a10da-114">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="a10da-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="a10da-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a10da-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="a10da-116">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="a10da-116">Set the Handled property.</span></span>

## <span data-ttu-id="a10da-117">Parte</span><span class="sxs-lookup"><span data-stu-id="a10da-117">Members</span></span>

#### <span data-ttu-id="a10da-118">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a10da-118">get_Handled</span></span> 

<span data-ttu-id="a10da-119">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a10da-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="a10da-120">[get_Handled](#get_handled)público HRESULT (valor bool \*)</span><span class="sxs-lookup"><span data-stu-id="a10da-120">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="a10da-121">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="a10da-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="a10da-122">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="a10da-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="a10da-123">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="a10da-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="a10da-124">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="a10da-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="a10da-125">get_Reason</span><span class="sxs-lookup"><span data-stu-id="a10da-125">get_Reason</span></span> 

<span data-ttu-id="a10da-126">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="a10da-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="a10da-127">[get_Reason](#get_reason)público HRESULT (COREWEBVIEW2_MOVE_FOCUS_REASON \* valor)</span><span class="sxs-lookup"><span data-stu-id="a10da-127">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="a10da-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a10da-128">put_Handled</span></span> 

<span data-ttu-id="a10da-129">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="a10da-129">Set the Handled property.</span></span>

> <span data-ttu-id="a10da-130">[put_Handled](#put_handled)público HRESULT (valor bool)</span><span class="sxs-lookup"><span data-stu-id="a10da-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

