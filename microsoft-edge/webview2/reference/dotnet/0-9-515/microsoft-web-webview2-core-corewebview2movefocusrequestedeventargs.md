---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 1d3cae59c0906a94414ff135ef8d84fac7cc89b4
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885069"
---
# <span data-ttu-id="2f3d5-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2f3d5-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="2f3d5-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2f3d5-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2f3d5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="2f3d5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2f3d5-107">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="2f3d5-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="2f3d5-108">Summary</span></span>

 <span data-ttu-id="2f3d5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2f3d5-109">Members</span></span>                        | <span data-ttu-id="2f3d5-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="2f3d5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2f3d5-111">Handled</span><span class="sxs-lookup"><span data-stu-id="2f3d5-111">Handled</span></span>](#handled) | <span data-ttu-id="2f3d5-112">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="2f3d5-113">Motivo</span><span class="sxs-lookup"><span data-stu-id="2f3d5-113">Reason</span></span>](#reason) | <span data-ttu-id="2f3d5-114">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="2f3d5-115">Parte</span><span class="sxs-lookup"><span data-stu-id="2f3d5-115">Members</span></span>

#### <span data-ttu-id="2f3d5-116">Handled</span><span class="sxs-lookup"><span data-stu-id="2f3d5-116">Handled</span></span> 

<span data-ttu-id="2f3d5-117">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="2f3d5-118">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="2f3d5-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="2f3d5-119">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="2f3d5-120">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="2f3d5-121">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="2f3d5-122">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="2f3d5-123">Motivo</span><span class="sxs-lookup"><span data-stu-id="2f3d5-123">Reason</span></span> 

<span data-ttu-id="2f3d5-124">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="2f3d5-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="2f3d5-125">[motivo](#reason) CoreWebView2MoveFocusReason público</span><span class="sxs-lookup"><span data-stu-id="2f3d5-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

