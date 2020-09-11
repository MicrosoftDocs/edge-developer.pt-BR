---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: 5e5d16c025dccf788b355280eaa3ac3e910f240d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011478"
---
# <span data-ttu-id="37682-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="37682-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="37682-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="37682-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="37682-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="37682-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="37682-107">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="37682-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="37682-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="37682-108">Summary</span></span>

 <span data-ttu-id="37682-109">Parte</span><span class="sxs-lookup"><span data-stu-id="37682-109">Members</span></span>                        | <span data-ttu-id="37682-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="37682-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="37682-111">Handled</span><span class="sxs-lookup"><span data-stu-id="37682-111">Handled</span></span>](#handled) | <span data-ttu-id="37682-112">Se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="37682-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="37682-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="37682-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="37682-114">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="37682-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="37682-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="37682-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="37682-116">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="37682-116">Gets the new window.</span></span>
[<span data-ttu-id="37682-117">Uri</span><span class="sxs-lookup"><span data-stu-id="37682-117">Uri</span></span>](#uri) | <span data-ttu-id="37682-118">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="37682-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="37682-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="37682-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="37682-120">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="37682-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="37682-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="37682-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="37682-122">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="37682-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="37682-123">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="37682-123">The event is fired when content inside WebView requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="37682-124">Parte</span><span class="sxs-lookup"><span data-stu-id="37682-124">Members</span></span>

#### <span data-ttu-id="37682-125">Handled</span><span class="sxs-lookup"><span data-stu-id="37682-125">Handled</span></span> 

<span data-ttu-id="37682-126">Se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="37682-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="37682-127">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="37682-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="37682-128">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="37682-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="37682-129">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="37682-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="37682-130">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="37682-130">Default is false.</span></span>

#### <span data-ttu-id="37682-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="37682-131">IsUserInitiated</span></span> 

<span data-ttu-id="37682-132">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="37682-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="37682-133">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="37682-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="37682-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="37682-134">NewWindow</span></span> 

<span data-ttu-id="37682-135">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="37682-135">Gets the new window.</span></span>

> <span data-ttu-id="37682-136">CoreWebView2 de [NewWindow](#newwindow) público</span><span class="sxs-lookup"><span data-stu-id="37682-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="37682-137">Uri</span><span class="sxs-lookup"><span data-stu-id="37682-137">Uri</span></span> 

<span data-ttu-id="37682-138">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="37682-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="37682-139">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="37682-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="37682-140">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="37682-140">The target WebView should not be navigated.</span></span> <span data-ttu-id="37682-141">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="37682-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="37682-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="37682-142">WindowFeatures</span></span> 

<span data-ttu-id="37682-143">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="37682-143">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="37682-144">CoreWebView2WindowFeatures público [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="37682-144">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="37682-145">Esses recursos podem ser considerados para o posicionamento e o dimensionamento de novas janelas da WebView.</span><span class="sxs-lookup"><span data-stu-id="37682-145">These features can be considered for positioning and sizing of new WebView windows.</span></span>

#### <span data-ttu-id="37682-146">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="37682-146">GetDeferral</span></span> 

<span data-ttu-id="37682-147">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="37682-147">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="37682-148">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="37682-148">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="37682-149">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="37682-149">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="37682-150">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="37682-150">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

