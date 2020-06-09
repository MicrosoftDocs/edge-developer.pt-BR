---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 54e2c06ef65f64560fbd5687148eace253352203
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698240"
---
# <span data-ttu-id="81586-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="81586-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="81586-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="81586-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="81586-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="81586-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="81586-107">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="81586-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="81586-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="81586-108">Summary</span></span>

 <span data-ttu-id="81586-109">Parte</span><span class="sxs-lookup"><span data-stu-id="81586-109">Members</span></span>                        | <span data-ttu-id="81586-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="81586-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="81586-111">Handled</span><span class="sxs-lookup"><span data-stu-id="81586-111">Handled</span></span>](#handled) | <span data-ttu-id="81586-112">Se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="81586-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="81586-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="81586-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="81586-114">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="81586-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="81586-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="81586-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="81586-116">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="81586-116">Gets the new window.</span></span>
[<span data-ttu-id="81586-117">Uri</span><span class="sxs-lookup"><span data-stu-id="81586-117">Uri</span></span>](#uri) | <span data-ttu-id="81586-118">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="81586-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="81586-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="81586-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="81586-120">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="81586-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="81586-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="81586-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="81586-122">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="81586-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="81586-123">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="81586-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="81586-124">Parte</span><span class="sxs-lookup"><span data-stu-id="81586-124">Members</span></span>

#### <span data-ttu-id="81586-125">Handled</span><span class="sxs-lookup"><span data-stu-id="81586-125">Handled</span></span> 

<span data-ttu-id="81586-126">Se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="81586-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="81586-127">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="81586-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="81586-128">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="81586-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="81586-129">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="81586-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="81586-130">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="81586-130">Default is false.</span></span>

#### <span data-ttu-id="81586-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="81586-131">IsUserInitiated</span></span> 

<span data-ttu-id="81586-132">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="81586-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="81586-133">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="81586-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="81586-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="81586-134">NewWindow</span></span> 

<span data-ttu-id="81586-135">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="81586-135">Gets the new window.</span></span>

> <span data-ttu-id="81586-136">CoreWebView2 de [NewWindow](#newwindow) público</span><span class="sxs-lookup"><span data-stu-id="81586-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="81586-137">Uri</span><span class="sxs-lookup"><span data-stu-id="81586-137">Uri</span></span> 

<span data-ttu-id="81586-138">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="81586-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="81586-139">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="81586-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="81586-140">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="81586-140">The target webview should not be navigated.</span></span> <span data-ttu-id="81586-141">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="81586-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="81586-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="81586-142">WindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="81586-143">Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="81586-143">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="81586-144">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="81586-144">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="81586-145">CoreWebView2WindowFeatures público [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="81586-145">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="81586-146">Esses recursos podem ser considerados para o posicionamento e o dimensionamento de novas janelas da WebView.</span><span class="sxs-lookup"><span data-stu-id="81586-146">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="81586-147">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="81586-147">GetDeferral</span></span> 

<span data-ttu-id="81586-148">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="81586-148">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="81586-149">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="81586-149">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="81586-150">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="81586-150">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="81586-151">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="81586-151">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

