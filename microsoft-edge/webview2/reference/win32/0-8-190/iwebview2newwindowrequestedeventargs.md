---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: cbcac385546c44e776ed48b8ae4d3ab754b614e0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885881"
---
# <span data-ttu-id="f531a-104">0.8.355-IWebView2NewWindowRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="f531a-104">0.8.355 - interface IWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="f531a-105">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f531a-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="f531a-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f531a-106">Summary</span></span>

 <span data-ttu-id="f531a-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f531a-107">Members</span></span>                        | <span data-ttu-id="f531a-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f531a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f531a-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f531a-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="f531a-110">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f531a-110">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="f531a-111">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f531a-111">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="f531a-112">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f531a-112">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="f531a-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f531a-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="f531a-114">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="f531a-114">Gets the new window.</span></span>
[<span data-ttu-id="f531a-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="f531a-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="f531a-116">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="f531a-116">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="f531a-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="f531a-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="f531a-118">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="f531a-118">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="f531a-119">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f531a-119">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="f531a-120">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="f531a-120">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="f531a-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f531a-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f531a-122">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="f531a-122">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="f531a-123">O evento é acionado quando o conteúdo de WebView solicitado para abrir uma nova janela (por meio de Window. Open () etc.)</span><span class="sxs-lookup"><span data-stu-id="f531a-123">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="f531a-124">Parte</span><span class="sxs-lookup"><span data-stu-id="f531a-124">Members</span></span>

#### <span data-ttu-id="f531a-125">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f531a-125">get_Uri</span></span> 

<span data-ttu-id="f531a-126">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f531a-126">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="f531a-127">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="f531a-127">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="f531a-128">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f531a-128">put_NewWindow</span></span> 

<span data-ttu-id="f531a-129">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f531a-129">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="f531a-130">público HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="f531a-130">public HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* newWindow)</span></span>

<span data-ttu-id="f531a-131">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="f531a-131">The target webview should not be navigated.</span></span> <span data-ttu-id="f531a-132">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="f531a-132">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="f531a-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f531a-133">get_NewWindow</span></span> 

<span data-ttu-id="f531a-134">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="f531a-134">Gets the new window.</span></span>

> <span data-ttu-id="f531a-135">público HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="f531a-135">public HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="f531a-136">put_Handled</span><span class="sxs-lookup"><span data-stu-id="f531a-136">put_Handled</span></span> 

<span data-ttu-id="f531a-137">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="f531a-137">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="f531a-138">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="f531a-138">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="f531a-139">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="f531a-139">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="f531a-140">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="f531a-140">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="f531a-141">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="f531a-141">Default is false.</span></span>

#### <span data-ttu-id="f531a-142">get_Handled</span><span class="sxs-lookup"><span data-stu-id="f531a-142">get_Handled</span></span> 

<span data-ttu-id="f531a-143">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="f531a-143">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="f531a-144">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="f531a-144">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="f531a-145">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f531a-145">get_IsUserInitiated</span></span> 

<span data-ttu-id="f531a-146">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="f531a-146">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="f531a-147">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="f531a-147">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="f531a-148">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f531a-148">GetDeferral</span></span> 

<span data-ttu-id="f531a-149">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="f531a-149">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="f531a-150">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="f531a-150">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f531a-151">Você pode usar o objeto [IWebView2Deferral](IWebView2Deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="f531a-151">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="f531a-152">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="f531a-152">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

