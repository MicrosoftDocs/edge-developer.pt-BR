---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: 098ca5199d6797510cdc0535a02a58c795b5ce54
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010954"
---
# <span data-ttu-id="c6f41-104">classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c6f41-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="c6f41-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c6f41-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c6f41-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="c6f41-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c6f41-107">Args de evento para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="c6f41-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="c6f41-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="c6f41-108">Summary</span></span>

 <span data-ttu-id="c6f41-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c6f41-109">Members</span></span>                        | <span data-ttu-id="c6f41-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="c6f41-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c6f41-111">Handled</span><span class="sxs-lookup"><span data-stu-id="c6f41-111">Handled</span></span>](#handled) | <span data-ttu-id="c6f41-112">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6f41-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="c6f41-113">Motivo</span><span class="sxs-lookup"><span data-stu-id="c6f41-113">Reason</span></span>](#reason) | <span data-ttu-id="c6f41-114">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="c6f41-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="c6f41-115">Parte</span><span class="sxs-lookup"><span data-stu-id="c6f41-115">Members</span></span>

#### <span data-ttu-id="c6f41-116">Handled</span><span class="sxs-lookup"><span data-stu-id="c6f41-116">Handled</span></span> 

<span data-ttu-id="c6f41-117">Indique se o evento foi manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6f41-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="c6f41-118">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="c6f41-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="c6f41-119">Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE.</span><span class="sxs-lookup"><span data-stu-id="c6f41-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="c6f41-120">Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada.</span><span class="sxs-lookup"><span data-stu-id="c6f41-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="c6f41-121">A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="c6f41-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="c6f41-122">Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.</span><span class="sxs-lookup"><span data-stu-id="c6f41-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="c6f41-123">Motivo</span><span class="sxs-lookup"><span data-stu-id="c6f41-123">Reason</span></span> 

<span data-ttu-id="c6f41-124">O motivo do WebView disparar o evento MoveFocus solicitado.</span><span class="sxs-lookup"><span data-stu-id="c6f41-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="c6f41-125">[motivo](#reason) CoreWebView2MoveFocusReason público</span><span class="sxs-lookup"><span data-stu-id="c6f41-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

