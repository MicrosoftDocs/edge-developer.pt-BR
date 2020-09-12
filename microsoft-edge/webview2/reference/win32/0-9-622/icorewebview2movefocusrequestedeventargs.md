---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: 8de2eaf6046b41df46b516694162471d22cafac3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011486"
---
# <span data-ttu-id="381b0-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="381b0-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="381b0-105">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="381b0-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="381b0-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="381b0-106">Summary</span></span>

 <span data-ttu-id="381b0-107">Parte</span><span class="sxs-lookup"><span data-stu-id="381b0-107">Members</span></span>                        | <span data-ttu-id="381b0-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="381b0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="381b0-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="381b0-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="381b0-110">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="381b0-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="381b0-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="381b0-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="381b0-112">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="381b0-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="381b0-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="381b0-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="381b0-114">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="381b0-114">Set the Handled property.</span></span>

## <span data-ttu-id="381b0-115">Parte</span><span class="sxs-lookup"><span data-stu-id="381b0-115">Members</span></span>

#### <span data-ttu-id="381b0-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="381b0-116">get_Handled</span></span> 

<span data-ttu-id="381b0-117">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="381b0-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="381b0-118">[get_Handled](#get_handled)público HRESULT (valor bool \*)</span><span class="sxs-lookup"><span data-stu-id="381b0-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="381b0-119">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="381b0-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="381b0-120">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="381b0-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="381b0-121">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="381b0-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="381b0-122">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="381b0-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="381b0-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="381b0-123">get_Reason</span></span> 

<span data-ttu-id="381b0-124">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="381b0-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="381b0-125">público HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* motivo)</span><span class="sxs-lookup"><span data-stu-id="381b0-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* reason)</span></span>

#### <span data-ttu-id="381b0-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="381b0-126">put_Handled</span></span> 

<span data-ttu-id="381b0-127">Defina a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="381b0-127">Set the Handled property.</span></span>

> <span data-ttu-id="381b0-128">[put_Handled](#put_handled)público HRESULT (valor bool)</span><span class="sxs-lookup"><span data-stu-id="381b0-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>
