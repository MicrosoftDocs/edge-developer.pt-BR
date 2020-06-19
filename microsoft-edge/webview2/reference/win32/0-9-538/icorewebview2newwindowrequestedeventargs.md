---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 03c943c87f07344ab4e3d1a7c707a993a795cdba
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751846"
---
# <span data-ttu-id="65f7b-104">interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="65f7b-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="65f7b-105">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="65f7b-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="65f7b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="65f7b-106">Summary</span></span>

 <span data-ttu-id="65f7b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="65f7b-107">Members</span></span>                        | <span data-ttu-id="65f7b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="65f7b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65f7b-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="65f7b-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="65f7b-110">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="65f7b-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="65f7b-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="65f7b-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="65f7b-112">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="65f7b-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="65f7b-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="65f7b-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="65f7b-114">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="65f7b-114">Gets the new window.</span></span>
[<span data-ttu-id="65f7b-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="65f7b-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="65f7b-116">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="65f7b-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="65f7b-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="65f7b-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="65f7b-118">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="65f7b-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="65f7b-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="65f7b-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="65f7b-120">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="65f7b-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="65f7b-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="65f7b-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="65f7b-122">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="65f7b-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="65f7b-123">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="65f7b-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="65f7b-124">Parte</span><span class="sxs-lookup"><span data-stu-id="65f7b-124">Members</span></span>

#### <span data-ttu-id="65f7b-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="65f7b-125">get_Handled</span></span> 

<span data-ttu-id="65f7b-126">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="65f7b-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="65f7b-127">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="65f7b-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="65f7b-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="65f7b-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="65f7b-129">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="65f7b-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="65f7b-130">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="65f7b-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="65f7b-131">Os controles WebView2 podem exibir janelas pop-up porque o bloqueador de pop-ups está desativado.</span><span class="sxs-lookup"><span data-stu-id="65f7b-131">WebView2 controls may display pop-up windows because the Pop-Up blocker is turned off.</span></span> <span data-ttu-id="65f7b-132">Para bloquear a exibição de janelas pop-up não iniciadas pelo usuário, use `get_IsUserInitiated` .</span><span class="sxs-lookup"><span data-stu-id="65f7b-132">To block non-user initiated pop-up windows from being displayed, use `get_IsUserInitiated`.</span></span>

#### <span data-ttu-id="65f7b-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="65f7b-133">get_NewWindow</span></span> 

<span data-ttu-id="65f7b-134">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="65f7b-134">Gets the new window.</span></span>

> <span data-ttu-id="65f7b-135">público HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="65f7b-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="65f7b-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="65f7b-136">get_Uri</span></span> 

<span data-ttu-id="65f7b-137">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="65f7b-137">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="65f7b-138">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="65f7b-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="65f7b-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="65f7b-139">GetDeferral</span></span> 

<span data-ttu-id="65f7b-140">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="65f7b-140">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="65f7b-141">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="65f7b-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="65f7b-142">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="65f7b-142">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="65f7b-143">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="65f7b-143">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="65f7b-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="65f7b-144">put_Handled</span></span> 

<span data-ttu-id="65f7b-145">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="65f7b-145">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="65f7b-146">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="65f7b-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="65f7b-147">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="65f7b-147">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="65f7b-148">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="65f7b-148">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="65f7b-149">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="65f7b-149">Default is false.</span></span>

#### <span data-ttu-id="65f7b-150">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="65f7b-150">put_NewWindow</span></span> 

<span data-ttu-id="65f7b-151">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="65f7b-151">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="65f7b-152">público HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="65f7b-152">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="65f7b-153">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="65f7b-153">The target webview should not be navigated.</span></span> <span data-ttu-id="65f7b-154">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="65f7b-154">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>
