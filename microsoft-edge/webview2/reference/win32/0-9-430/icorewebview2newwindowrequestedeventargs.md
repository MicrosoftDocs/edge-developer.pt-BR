---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 73f62e7130d50028b527353c6ba1a238f694dcda
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885678"
---
# <span data-ttu-id="ca217-104">0.9.430-ICoreWebView2NewWindowRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="ca217-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="ca217-105">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="ca217-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="ca217-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ca217-106">Summary</span></span>

 <span data-ttu-id="ca217-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ca217-107">Members</span></span>                        | <span data-ttu-id="ca217-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ca217-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca217-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ca217-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ca217-110">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="ca217-110">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="ca217-111">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="ca217-111">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="ca217-112">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="ca217-112">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="ca217-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="ca217-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="ca217-114">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="ca217-114">Gets the new window.</span></span>
[<span data-ttu-id="ca217-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="ca217-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="ca217-116">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="ca217-116">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="ca217-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="ca217-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="ca217-118">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="ca217-118">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="ca217-119">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ca217-119">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="ca217-120">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="ca217-120">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="ca217-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ca217-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ca217-122">Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="ca217-122">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="ca217-123">O evento é acionado quando o conteúdo de WebView solicitado para abrir uma nova janela (por meio de Window. Open () etc.)</span><span class="sxs-lookup"><span data-stu-id="ca217-123">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="ca217-124">Parte</span><span class="sxs-lookup"><span data-stu-id="ca217-124">Members</span></span>

#### <span data-ttu-id="ca217-125">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ca217-125">get_Uri</span></span> 

<span data-ttu-id="ca217-126">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="ca217-126">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="ca217-127">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ca217-127">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ca217-128">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="ca217-128">put_NewWindow</span></span> 

<span data-ttu-id="ca217-129">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="ca217-129">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="ca217-130">público HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="ca217-130">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="ca217-131">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="ca217-131">The target webview should not be navigated.</span></span> <span data-ttu-id="ca217-132">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="ca217-132">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="ca217-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="ca217-133">get_NewWindow</span></span> 

<span data-ttu-id="ca217-134">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="ca217-134">Gets the new window.</span></span>

> <span data-ttu-id="ca217-135">público HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="ca217-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="ca217-136">put_Handled</span><span class="sxs-lookup"><span data-stu-id="ca217-136">put_Handled</span></span> 

<span data-ttu-id="ca217-137">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="ca217-137">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="ca217-138">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="ca217-138">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="ca217-139">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="ca217-139">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="ca217-140">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="ca217-140">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="ca217-141">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="ca217-141">Default is false.</span></span>

#### <span data-ttu-id="ca217-142">get_Handled</span><span class="sxs-lookup"><span data-stu-id="ca217-142">get_Handled</span></span> 

<span data-ttu-id="ca217-143">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="ca217-143">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="ca217-144">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="ca217-144">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="ca217-145">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ca217-145">get_IsUserInitiated</span></span> 

<span data-ttu-id="ca217-146">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="ca217-146">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="ca217-147">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="ca217-147">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="ca217-148">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ca217-148">GetDeferral</span></span> 

<span data-ttu-id="ca217-149">Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="ca217-149">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="ca217-150">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="ca217-150">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="ca217-151">Você pode usar o objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="ca217-151">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="ca217-152">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="ca217-152">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

