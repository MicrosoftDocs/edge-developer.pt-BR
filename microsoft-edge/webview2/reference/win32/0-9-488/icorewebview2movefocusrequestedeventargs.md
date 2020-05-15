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
ms.openlocfilehash: 8ca8de3c430eda3bde089ca53501d880f4d8e35e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652573"
---
# <span data-ttu-id="1b20b-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1b20b-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="1b20b-105">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="1b20b-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="1b20b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1b20b-106">Summary</span></span>

 <span data-ttu-id="1b20b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1b20b-107">Members</span></span>                        | <span data-ttu-id="1b20b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1b20b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b20b-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="1b20b-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="1b20b-110">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b20b-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="1b20b-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="1b20b-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="1b20b-112">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="1b20b-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="1b20b-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="1b20b-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="1b20b-114">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="1b20b-114">Set the Handled property.</span></span>

## <span data-ttu-id="1b20b-115">Parte</span><span class="sxs-lookup"><span data-stu-id="1b20b-115">Members</span></span>

#### <span data-ttu-id="1b20b-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="1b20b-116">get_Handled</span></span> 

<span data-ttu-id="1b20b-117">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b20b-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="1b20b-118">[get_Handled](#get_handled)público HRESULT (valor bool \*)</span><span class="sxs-lookup"><span data-stu-id="1b20b-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="1b20b-119">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="1b20b-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="1b20b-120">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="1b20b-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="1b20b-121">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="1b20b-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="1b20b-122">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="1b20b-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="1b20b-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="1b20b-123">get_Reason</span></span> 

<span data-ttu-id="1b20b-124">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="1b20b-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="1b20b-125">[get_Reason](#get_reason)público HRESULT (COREWEBVIEW2_MOVE_FOCUS_REASON \* valor)</span><span class="sxs-lookup"><span data-stu-id="1b20b-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="1b20b-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="1b20b-126">put_Handled</span></span> 

<span data-ttu-id="1b20b-127">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="1b20b-127">Set the Handled property.</span></span>

> <span data-ttu-id="1b20b-128">[put_Handled](#put_handled)público HRESULT (valor bool)</span><span class="sxs-lookup"><span data-stu-id="1b20b-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

