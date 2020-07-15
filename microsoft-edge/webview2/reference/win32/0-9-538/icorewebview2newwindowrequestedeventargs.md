---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: bb18b6662fd5921406e19b3c333c97f8a1cd0dbc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879433"
---
# <span data-ttu-id="54f91-104">interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="54f91-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="54f91-105">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="54f91-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="54f91-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="54f91-106">Summary</span></span>

 <span data-ttu-id="54f91-107">Parte</span><span class="sxs-lookup"><span data-stu-id="54f91-107">Members</span></span>                        | <span data-ttu-id="54f91-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="54f91-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="54f91-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="54f91-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="54f91-110">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="54f91-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="54f91-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="54f91-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="54f91-112">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="54f91-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="54f91-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="54f91-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="54f91-114">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="54f91-114">Gets the new window.</span></span>
[<span data-ttu-id="54f91-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="54f91-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="54f91-116">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="54f91-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="54f91-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="54f91-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="54f91-118">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="54f91-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="54f91-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="54f91-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="54f91-120">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="54f91-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="54f91-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="54f91-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="54f91-122">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="54f91-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="54f91-123">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="54f91-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="54f91-124">Parte</span><span class="sxs-lookup"><span data-stu-id="54f91-124">Members</span></span>

#### <span data-ttu-id="54f91-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="54f91-125">get_Handled</span></span> 

<span data-ttu-id="54f91-126">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="54f91-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="54f91-127">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="54f91-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="54f91-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="54f91-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="54f91-129">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="54f91-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="54f91-130">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="54f91-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="54f91-131">O bloqueador de borda pop-up está desabilitado para WebView para que o aplicativo possa usar esse sinalizador para bloquear pop-ups que não sejam iniciados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="54f91-131">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="54f91-132">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="54f91-132">get_NewWindow</span></span> 

<span data-ttu-id="54f91-133">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="54f91-133">Gets the new window.</span></span>

> <span data-ttu-id="54f91-134">público HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="54f91-134">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="54f91-135">get_Uri</span><span class="sxs-lookup"><span data-stu-id="54f91-135">get_Uri</span></span> 

<span data-ttu-id="54f91-136">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="54f91-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="54f91-137">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="54f91-137">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="54f91-138">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="54f91-138">GetDeferral</span></span> 

<span data-ttu-id="54f91-139">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="54f91-139">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="54f91-140">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="54f91-140">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="54f91-141">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="54f91-141">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="54f91-142">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="54f91-142">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="54f91-143">put_Handled</span><span class="sxs-lookup"><span data-stu-id="54f91-143">put_Handled</span></span> 

<span data-ttu-id="54f91-144">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="54f91-144">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="54f91-145">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="54f91-145">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="54f91-146">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="54f91-146">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="54f91-147">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="54f91-147">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="54f91-148">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="54f91-148">Default is false.</span></span>

#### <span data-ttu-id="54f91-149">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="54f91-149">put_NewWindow</span></span> 

<span data-ttu-id="54f91-150">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="54f91-150">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="54f91-151">público HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="54f91-151">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="54f91-152">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="54f91-152">The target webview should not be navigated.</span></span> <span data-ttu-id="54f91-153">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="54f91-153">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

