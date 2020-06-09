---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: d99c05026257116dd5c6c7119325e00227d9a6d0
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697809"
---
# <span data-ttu-id="bec0c-104">interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="bec0c-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="bec0c-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="bec0c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="bec0c-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="bec0c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="bec0c-107">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="bec0c-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="bec0c-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="bec0c-108">Summary</span></span>

 <span data-ttu-id="bec0c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bec0c-109">Members</span></span>                        | <span data-ttu-id="bec0c-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="bec0c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bec0c-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="bec0c-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="bec0c-112">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="bec0c-112">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="bec0c-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="bec0c-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="bec0c-114">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="bec0c-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="bec0c-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="bec0c-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="bec0c-116">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="bec0c-116">Gets the new window.</span></span>
[<span data-ttu-id="bec0c-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="bec0c-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="bec0c-118">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="bec0c-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="bec0c-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="bec0c-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="bec0c-120">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="bec0c-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="bec0c-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="bec0c-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="bec0c-122">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="bec0c-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="bec0c-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="bec0c-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="bec0c-124">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="bec0c-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="bec0c-125">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="bec0c-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="bec0c-126">Parte</span><span class="sxs-lookup"><span data-stu-id="bec0c-126">Members</span></span>

#### <span data-ttu-id="bec0c-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="bec0c-127">get_Handled</span></span> 

<span data-ttu-id="bec0c-128">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="bec0c-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="bec0c-129">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="bec0c-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="bec0c-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="bec0c-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="bec0c-131">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="bec0c-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="bec0c-132">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="bec0c-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="bec0c-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="bec0c-133">get_NewWindow</span></span> 

<span data-ttu-id="bec0c-134">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="bec0c-134">Gets the new window.</span></span>

> <span data-ttu-id="bec0c-135">público HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="bec0c-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="bec0c-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="bec0c-136">get_Uri</span></span> 

<span data-ttu-id="bec0c-137">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="bec0c-137">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="bec0c-138">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="bec0c-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="bec0c-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="bec0c-139">GetDeferral</span></span> 

<span data-ttu-id="bec0c-140">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="bec0c-140">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="bec0c-141">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="bec0c-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="bec0c-142">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="bec0c-142">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="bec0c-143">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="bec0c-143">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="bec0c-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="bec0c-144">put_Handled</span></span> 

<span data-ttu-id="bec0c-145">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="bec0c-145">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="bec0c-146">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="bec0c-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="bec0c-147">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="bec0c-147">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="bec0c-148">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="bec0c-148">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="bec0c-149">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="bec0c-149">Default is false.</span></span>

#### <span data-ttu-id="bec0c-150">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="bec0c-150">put_NewWindow</span></span> 

<span data-ttu-id="bec0c-151">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="bec0c-151">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="bec0c-152">público HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="bec0c-152">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="bec0c-153">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="bec0c-153">The target webview should not be navigated.</span></span> <span data-ttu-id="bec0c-154">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="bec0c-154">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

