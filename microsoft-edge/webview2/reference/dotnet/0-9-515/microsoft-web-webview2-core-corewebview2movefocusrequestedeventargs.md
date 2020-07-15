---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 37d64a18589df936383efe05317c1a625b841a6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877655"
---
# <span data-ttu-id="0feb5-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0feb5-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="0feb5-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="0feb5-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="0feb5-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="0feb5-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="0feb5-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0feb5-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0feb5-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="0feb5-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0feb5-109">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0feb5-109">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="0feb5-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="0feb5-110">Summary</span></span>

 <span data-ttu-id="0feb5-111">Parte</span><span class="sxs-lookup"><span data-stu-id="0feb5-111">Members</span></span>                        | <span data-ttu-id="0feb5-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="0feb5-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0feb5-113">Handled</span><span class="sxs-lookup"><span data-stu-id="0feb5-113">Handled</span></span>](#handled) | <span data-ttu-id="0feb5-114">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0feb5-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="0feb5-115">Motivo</span><span class="sxs-lookup"><span data-stu-id="0feb5-115">Reason</span></span>](#reason) | <span data-ttu-id="0feb5-116">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="0feb5-116">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="0feb5-117">Parte</span><span class="sxs-lookup"><span data-stu-id="0feb5-117">Members</span></span>

#### <span data-ttu-id="0feb5-118">Handled</span><span class="sxs-lookup"><span data-stu-id="0feb5-118">Handled</span></span> 

<span data-ttu-id="0feb5-119">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0feb5-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="0feb5-120">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="0feb5-120">public bool [Handled](#handled)</span></span>

<span data-ttu-id="0feb5-121">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="0feb5-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="0feb5-122">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="0feb5-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="0feb5-123">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="0feb5-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="0feb5-124">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="0feb5-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="0feb5-125">Motivo</span><span class="sxs-lookup"><span data-stu-id="0feb5-125">Reason</span></span> 

<span data-ttu-id="0feb5-126">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="0feb5-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="0feb5-127">[motivo](#reason) CoreWebView2MoveFocusReason público</span><span class="sxs-lookup"><span data-stu-id="0feb5-127">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

