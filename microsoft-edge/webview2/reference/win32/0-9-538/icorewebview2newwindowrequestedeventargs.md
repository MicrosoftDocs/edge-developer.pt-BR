---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: 5486aa66e39e220e819bb00211a79bd449a25bfe
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010058"
---
# <span data-ttu-id="74a57-104">0.9.579-ICoreWebView2NewWindowRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="74a57-104">0.9.579 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="74a57-105">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="74a57-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="74a57-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="74a57-106">Summary</span></span>

 <span data-ttu-id="74a57-107">Parte</span><span class="sxs-lookup"><span data-stu-id="74a57-107">Members</span></span>                        | <span data-ttu-id="74a57-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="74a57-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="74a57-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="74a57-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="74a57-110">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="74a57-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="74a57-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="74a57-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="74a57-112">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="74a57-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="74a57-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="74a57-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="74a57-114">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="74a57-114">Gets the new window.</span></span>
[<span data-ttu-id="74a57-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="74a57-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="74a57-116">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="74a57-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="74a57-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="74a57-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="74a57-118">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="74a57-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="74a57-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="74a57-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="74a57-120">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="74a57-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="74a57-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="74a57-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="74a57-122">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="74a57-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="74a57-123">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="74a57-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="74a57-124">Parte</span><span class="sxs-lookup"><span data-stu-id="74a57-124">Members</span></span>

#### <span data-ttu-id="74a57-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="74a57-125">get_Handled</span></span> 

<span data-ttu-id="74a57-126">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="74a57-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="74a57-127">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="74a57-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="74a57-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="74a57-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="74a57-129">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="74a57-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="74a57-130">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="74a57-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="74a57-131">O bloqueador de borda pop-up está desabilitado para WebView para que o aplicativo possa usar esse sinalizador para bloquear pop-ups que não sejam iniciados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="74a57-131">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="74a57-132">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="74a57-132">get_NewWindow</span></span> 

<span data-ttu-id="74a57-133">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="74a57-133">Gets the new window.</span></span>

> <span data-ttu-id="74a57-134">público HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="74a57-134">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="74a57-135">get_Uri</span><span class="sxs-lookup"><span data-stu-id="74a57-135">get_Uri</span></span> 

<span data-ttu-id="74a57-136">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="74a57-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="74a57-137">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="74a57-137">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="74a57-138">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="74a57-138">GetDeferral</span></span> 

<span data-ttu-id="74a57-139">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="74a57-139">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="74a57-140">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="74a57-140">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="74a57-141">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="74a57-141">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="74a57-142">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="74a57-142">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="74a57-143">put_Handled</span><span class="sxs-lookup"><span data-stu-id="74a57-143">put_Handled</span></span> 

<span data-ttu-id="74a57-144">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="74a57-144">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="74a57-145">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="74a57-145">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="74a57-146">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="74a57-146">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="74a57-147">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="74a57-147">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="74a57-148">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="74a57-148">Default is false.</span></span>

#### <span data-ttu-id="74a57-149">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="74a57-149">put_NewWindow</span></span> 

<span data-ttu-id="74a57-150">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="74a57-150">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="74a57-151">público HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="74a57-151">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="74a57-152">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="74a57-152">The target webview should not be navigated.</span></span> <span data-ttu-id="74a57-153">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="74a57-153">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

