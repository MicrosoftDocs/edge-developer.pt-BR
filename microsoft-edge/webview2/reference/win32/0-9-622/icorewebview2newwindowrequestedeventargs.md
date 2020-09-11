---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: d1cf39fe71c4b00f10a14da8a65428eb24daa71f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011546"
---
# <span data-ttu-id="10bf3-104">interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="10bf3-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="10bf3-105">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="10bf3-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="10bf3-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="10bf3-106">Summary</span></span>

 <span data-ttu-id="10bf3-107">Parte</span><span class="sxs-lookup"><span data-stu-id="10bf3-107">Members</span></span>                        | <span data-ttu-id="10bf3-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="10bf3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10bf3-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="10bf3-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="10bf3-110">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="10bf3-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="10bf3-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="10bf3-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="10bf3-112">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="10bf3-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="10bf3-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="10bf3-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="10bf3-114">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="10bf3-114">Gets the new window.</span></span>
[<span data-ttu-id="10bf3-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="10bf3-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="10bf3-116">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="10bf3-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="10bf3-117">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="10bf3-117">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="10bf3-118">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="10bf3-118">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="10bf3-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="10bf3-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="10bf3-120">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="10bf3-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="10bf3-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="10bf3-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="10bf3-122">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="10bf3-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="10bf3-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="10bf3-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="10bf3-124">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="10bf3-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="10bf3-125">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="10bf3-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="10bf3-126">Parte</span><span class="sxs-lookup"><span data-stu-id="10bf3-126">Members</span></span>

#### <span data-ttu-id="10bf3-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="10bf3-127">get_Handled</span></span> 

<span data-ttu-id="10bf3-128">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="10bf3-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="10bf3-129">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="10bf3-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="10bf3-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="10bf3-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="10bf3-131">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="10bf3-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="10bf3-132">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="10bf3-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="10bf3-133">O bloqueador de borda pop-up está desabilitado para WebView para que o aplicativo possa usar esse sinalizador para bloquear pop-ups que não sejam iniciados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="10bf3-133">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="10bf3-134">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="10bf3-134">get_NewWindow</span></span> 

<span data-ttu-id="10bf3-135">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="10bf3-135">Gets the new window.</span></span>

> <span data-ttu-id="10bf3-136">público HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="10bf3-136">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="10bf3-137">get_Uri</span><span class="sxs-lookup"><span data-stu-id="10bf3-137">get_Uri</span></span> 

<span data-ttu-id="10bf3-138">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="10bf3-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="10bf3-139">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="10bf3-139">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="10bf3-140">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="10bf3-140">get_WindowFeatures</span></span> 

<span data-ttu-id="10bf3-141">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="10bf3-141">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="10bf3-142">Public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="10bf3-142">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="10bf3-143">Esses recursos podem ser considerados para o posicionamento e o dimensionamento de novas janelas da WebView.</span><span class="sxs-lookup"><span data-stu-id="10bf3-143">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="10bf3-144">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="10bf3-144">GetDeferral</span></span> 

<span data-ttu-id="10bf3-145">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="10bf3-145">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="10bf3-146">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="10bf3-146">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="10bf3-147">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="10bf3-147">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="10bf3-148">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="10bf3-148">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="10bf3-149">put_Handled</span><span class="sxs-lookup"><span data-stu-id="10bf3-149">put_Handled</span></span> 

<span data-ttu-id="10bf3-150">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="10bf3-150">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="10bf3-151">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="10bf3-151">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="10bf3-152">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="10bf3-152">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="10bf3-153">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="10bf3-153">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="10bf3-154">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="10bf3-154">Default is false.</span></span>

#### <span data-ttu-id="10bf3-155">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="10bf3-155">put_NewWindow</span></span> 

<span data-ttu-id="10bf3-156">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="10bf3-156">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="10bf3-157">público HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="10bf3-157">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="10bf3-158">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="10bf3-158">The target WebView should not be navigated.</span></span> <span data-ttu-id="10bf3-159">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="10bf3-159">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

