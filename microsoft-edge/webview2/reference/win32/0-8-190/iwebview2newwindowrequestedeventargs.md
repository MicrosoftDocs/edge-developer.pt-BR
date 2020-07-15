---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: a90727949fa9a64004527236e6c5f016afe018e0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878362"
---
# <span data-ttu-id="06b19-104">0.8.355-IWebView2NewWindowRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="06b19-104">0.8.355 - interface IWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="06b19-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="06b19-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="06b19-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="06b19-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="06b19-107">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="06b19-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="06b19-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="06b19-108">Summary</span></span>

 <span data-ttu-id="06b19-109">Parte</span><span class="sxs-lookup"><span data-stu-id="06b19-109">Members</span></span>                        | <span data-ttu-id="06b19-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="06b19-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06b19-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="06b19-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="06b19-112">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="06b19-112">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="06b19-113">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="06b19-113">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="06b19-114">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="06b19-114">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="06b19-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="06b19-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="06b19-116">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="06b19-116">Gets the new window.</span></span>
[<span data-ttu-id="06b19-117">put_Handled</span><span class="sxs-lookup"><span data-stu-id="06b19-117">put_Handled</span></span>](#put_handled) | <span data-ttu-id="06b19-118">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="06b19-118">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="06b19-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="06b19-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="06b19-120">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="06b19-120">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="06b19-121">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="06b19-121">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="06b19-122">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="06b19-122">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="06b19-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="06b19-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="06b19-124">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="06b19-124">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="06b19-125">O evento é acionado quando o conteúdo de WebView solicitado para abrir uma nova janela (por meio de Window. Open () etc.)</span><span class="sxs-lookup"><span data-stu-id="06b19-125">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="06b19-126">Parte</span><span class="sxs-lookup"><span data-stu-id="06b19-126">Members</span></span>

#### <span data-ttu-id="06b19-127">get_Uri</span><span class="sxs-lookup"><span data-stu-id="06b19-127">get_Uri</span></span> 

<span data-ttu-id="06b19-128">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="06b19-128">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="06b19-129">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="06b19-129">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="06b19-130">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="06b19-130">put_NewWindow</span></span> 

<span data-ttu-id="06b19-131">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="06b19-131">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="06b19-132">público HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="06b19-132">public HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* newWindow)</span></span>

<span data-ttu-id="06b19-133">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="06b19-133">The target webview should not be navigated.</span></span> <span data-ttu-id="06b19-134">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="06b19-134">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="06b19-135">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="06b19-135">get_NewWindow</span></span> 

<span data-ttu-id="06b19-136">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="06b19-136">Gets the new window.</span></span>

> <span data-ttu-id="06b19-137">público HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="06b19-137">public HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="06b19-138">put_Handled</span><span class="sxs-lookup"><span data-stu-id="06b19-138">put_Handled</span></span> 

<span data-ttu-id="06b19-139">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="06b19-139">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="06b19-140">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="06b19-140">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="06b19-141">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="06b19-141">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="06b19-142">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="06b19-142">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="06b19-143">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="06b19-143">Default is false.</span></span>

#### <span data-ttu-id="06b19-144">get_Handled</span><span class="sxs-lookup"><span data-stu-id="06b19-144">get_Handled</span></span> 

<span data-ttu-id="06b19-145">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="06b19-145">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="06b19-146">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="06b19-146">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="06b19-147">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="06b19-147">get_IsUserInitiated</span></span> 

<span data-ttu-id="06b19-148">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="06b19-148">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="06b19-149">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="06b19-149">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="06b19-150">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="06b19-150">GetDeferral</span></span> 

<span data-ttu-id="06b19-151">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="06b19-151">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="06b19-152">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="06b19-152">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="06b19-153">Você pode usar o objeto [IWebView2Deferral](IWebView2Deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="06b19-153">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="06b19-154">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="06b19-154">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

