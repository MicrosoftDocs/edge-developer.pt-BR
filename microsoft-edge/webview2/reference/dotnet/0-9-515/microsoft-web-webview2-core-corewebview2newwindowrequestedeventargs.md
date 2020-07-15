---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: d10154fbaeb8dca0247dc721a2144899feba38df
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880007"
---
# <span data-ttu-id="b86dc-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b86dc-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="b86dc-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b86dc-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b86dc-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="b86dc-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="b86dc-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b86dc-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b86dc-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b86dc-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b86dc-109">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="b86dc-109">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="b86dc-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="b86dc-110">Summary</span></span>

 <span data-ttu-id="b86dc-111">Parte</span><span class="sxs-lookup"><span data-stu-id="b86dc-111">Members</span></span>                        | <span data-ttu-id="b86dc-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="b86dc-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b86dc-113">Handled</span><span class="sxs-lookup"><span data-stu-id="b86dc-113">Handled</span></span>](#handled) | <span data-ttu-id="b86dc-114">Se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="b86dc-114">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="b86dc-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b86dc-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="b86dc-116">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="b86dc-116">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="b86dc-117">NewWindow</span><span class="sxs-lookup"><span data-stu-id="b86dc-117">NewWindow</span></span>](#newwindow) | <span data-ttu-id="b86dc-118">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="b86dc-118">Gets the new window.</span></span>
[<span data-ttu-id="b86dc-119">Uri</span><span class="sxs-lookup"><span data-stu-id="b86dc-119">Uri</span></span>](#uri) | <span data-ttu-id="b86dc-120">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="b86dc-120">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="b86dc-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b86dc-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b86dc-122">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="b86dc-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="b86dc-123">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="b86dc-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="b86dc-124">Parte</span><span class="sxs-lookup"><span data-stu-id="b86dc-124">Members</span></span>

#### <span data-ttu-id="b86dc-125">Handled</span><span class="sxs-lookup"><span data-stu-id="b86dc-125">Handled</span></span> 

<span data-ttu-id="b86dc-126">Se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="b86dc-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="b86dc-127">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="b86dc-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="b86dc-128">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="b86dc-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="b86dc-129">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="b86dc-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="b86dc-130">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="b86dc-130">Default is false.</span></span>

#### <span data-ttu-id="b86dc-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b86dc-131">IsUserInitiated</span></span> 

<span data-ttu-id="b86dc-132">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="b86dc-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="b86dc-133">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="b86dc-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="b86dc-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="b86dc-134">NewWindow</span></span> 

<span data-ttu-id="b86dc-135">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="b86dc-135">Gets the new window.</span></span>

> <span data-ttu-id="b86dc-136">CoreWebView2 de [NewWindow](#newwindow) público</span><span class="sxs-lookup"><span data-stu-id="b86dc-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="b86dc-137">Uri</span><span class="sxs-lookup"><span data-stu-id="b86dc-137">Uri</span></span> 

<span data-ttu-id="b86dc-138">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="b86dc-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="b86dc-139">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="b86dc-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="b86dc-140">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="b86dc-140">The target webview should not be navigated.</span></span> <span data-ttu-id="b86dc-141">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="b86dc-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="b86dc-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b86dc-142">GetDeferral</span></span> 

<span data-ttu-id="b86dc-143">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="b86dc-143">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="b86dc-144">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="b86dc-144">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="b86dc-145">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="b86dc-145">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="b86dc-146">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="b86dc-146">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

