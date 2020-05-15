---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: cca15ccc5292f5eaf6f317ffb657f46fcd84b4a9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652722"
---
# <span data-ttu-id="47ea0-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="47ea0-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="47ea0-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="47ea0-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="47ea0-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="47ea0-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="47ea0-107">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="47ea0-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="47ea0-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="47ea0-108">Summary</span></span>

 <span data-ttu-id="47ea0-109">Parte</span><span class="sxs-lookup"><span data-stu-id="47ea0-109">Members</span></span>                        | <span data-ttu-id="47ea0-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="47ea0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="47ea0-111">Handled</span><span class="sxs-lookup"><span data-stu-id="47ea0-111">Handled</span></span>](#handled) | <span data-ttu-id="47ea0-112">Se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="47ea0-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="47ea0-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="47ea0-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="47ea0-114">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="47ea0-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="47ea0-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="47ea0-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="47ea0-116">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="47ea0-116">Gets the new window.</span></span>
[<span data-ttu-id="47ea0-117">Uri</span><span class="sxs-lookup"><span data-stu-id="47ea0-117">Uri</span></span>](#uri) | <span data-ttu-id="47ea0-118">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="47ea0-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="47ea0-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="47ea0-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="47ea0-120">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="47ea0-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="47ea0-121">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="47ea0-121">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="47ea0-122">Parte</span><span class="sxs-lookup"><span data-stu-id="47ea0-122">Members</span></span>

#### <span data-ttu-id="47ea0-123">Handled</span><span class="sxs-lookup"><span data-stu-id="47ea0-123">Handled</span></span> 

<span data-ttu-id="47ea0-124">Se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="47ea0-124">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="47ea0-125">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="47ea0-125">public bool [Handled](#handled)</span></span>

<span data-ttu-id="47ea0-126">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="47ea0-126">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="47ea0-127">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="47ea0-127">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="47ea0-128">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="47ea0-128">Default is false.</span></span>

#### <span data-ttu-id="47ea0-129">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="47ea0-129">IsUserInitiated</span></span> 

<span data-ttu-id="47ea0-130">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="47ea0-130">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="47ea0-131">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="47ea0-131">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="47ea0-132">NewWindow</span><span class="sxs-lookup"><span data-stu-id="47ea0-132">NewWindow</span></span> 

<span data-ttu-id="47ea0-133">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="47ea0-133">Gets the new window.</span></span>

> <span data-ttu-id="47ea0-134">CoreWebView2 de [NewWindow](#newwindow) público</span><span class="sxs-lookup"><span data-stu-id="47ea0-134">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="47ea0-135">Uri</span><span class="sxs-lookup"><span data-stu-id="47ea0-135">Uri</span></span> 

<span data-ttu-id="47ea0-136">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="47ea0-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="47ea0-137">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="47ea0-137">public string [Uri](#uri)</span></span>

<span data-ttu-id="47ea0-138">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="47ea0-138">The target webview should not be navigated.</span></span> <span data-ttu-id="47ea0-139">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="47ea0-139">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="47ea0-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="47ea0-140">GetDeferral</span></span> 

<span data-ttu-id="47ea0-141">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="47ea0-141">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="47ea0-142">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="47ea0-142">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="47ea0-143">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="47ea0-143">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="47ea0-144">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="47ea0-144">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

