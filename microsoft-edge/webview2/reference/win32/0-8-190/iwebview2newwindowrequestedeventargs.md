---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: e1917a4383e6e5d8aaf79464c4607d8f2d4f0cdc
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652384"
---
# <span data-ttu-id="47b72-104">interface IWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="47b72-104">interface IWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="47b72-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="47b72-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="47b72-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="47b72-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="47b72-107">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="47b72-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="47b72-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="47b72-108">Summary</span></span>

 <span data-ttu-id="47b72-109">Parte</span><span class="sxs-lookup"><span data-stu-id="47b72-109">Members</span></span>                        | <span data-ttu-id="47b72-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="47b72-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="47b72-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="47b72-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="47b72-112">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="47b72-112">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="47b72-113">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="47b72-113">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="47b72-114">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="47b72-114">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="47b72-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="47b72-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="47b72-116">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="47b72-116">Gets the new window.</span></span>
[<span data-ttu-id="47b72-117">put_Handled</span><span class="sxs-lookup"><span data-stu-id="47b72-117">put_Handled</span></span>](#put_handled) | <span data-ttu-id="47b72-118">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="47b72-118">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="47b72-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="47b72-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="47b72-120">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="47b72-120">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="47b72-121">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="47b72-121">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="47b72-122">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="47b72-122">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="47b72-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="47b72-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="47b72-124">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="47b72-124">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="47b72-125">O evento é acionado quando o conteúdo de WebView solicitado para abrir uma nova janela (por meio de Window. Open () etc.)</span><span class="sxs-lookup"><span data-stu-id="47b72-125">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="47b72-126">Parte</span><span class="sxs-lookup"><span data-stu-id="47b72-126">Members</span></span>

#### <span data-ttu-id="47b72-127">get_Uri</span><span class="sxs-lookup"><span data-stu-id="47b72-127">get_Uri</span></span> 

<span data-ttu-id="47b72-128">O URI de destino do NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="47b72-128">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="47b72-129">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="47b72-129">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="47b72-130">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="47b72-130">put_NewWindow</span></span> 

<span data-ttu-id="47b72-131">Define uma WebView como resultado da NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="47b72-131">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="47b72-132">público HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="47b72-132">public HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* newWindow)</span></span>

<span data-ttu-id="47b72-133">O WebView de destino não deve ser navegado.</span><span class="sxs-lookup"><span data-stu-id="47b72-133">The target webview should not be navigated.</span></span> <span data-ttu-id="47b72-134">Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="47b72-134">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="47b72-135">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="47b72-135">get_NewWindow</span></span> 

<span data-ttu-id="47b72-136">Obtém a nova janela.</span><span class="sxs-lookup"><span data-stu-id="47b72-136">Gets the new window.</span></span>

> <span data-ttu-id="47b72-137">público HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="47b72-137">public HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="47b72-138">put_Handled</span><span class="sxs-lookup"><span data-stu-id="47b72-138">put_Handled</span></span> 

<span data-ttu-id="47b72-139">Define se o NewWindowRequestedEvent é manipulado pelo host.</span><span class="sxs-lookup"><span data-stu-id="47b72-139">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="47b72-140">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="47b72-140">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="47b72-141">Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto.</span><span class="sxs-lookup"><span data-stu-id="47b72-141">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="47b72-142">Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada.</span><span class="sxs-lookup"><span data-stu-id="47b72-142">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="47b72-143">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="47b72-143">Default is false.</span></span>

#### <span data-ttu-id="47b72-144">get_Handled</span><span class="sxs-lookup"><span data-stu-id="47b72-144">get_Handled</span></span> 

<span data-ttu-id="47b72-145">Obtém se a NewWindowRequestedEvent é manipulada pelo host.</span><span class="sxs-lookup"><span data-stu-id="47b72-145">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="47b72-146">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="47b72-146">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="47b72-147">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="47b72-147">get_IsUserInitiated</span></span> 

<span data-ttu-id="47b72-148">IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="47b72-148">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="47b72-149">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="47b72-149">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="47b72-150">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="47b72-150">GetDeferral</span></span> 

<span data-ttu-id="47b72-151">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="47b72-151">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="47b72-152">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="47b72-152">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="47b72-153">Você pode usar o objeto [IWebView2Deferral](IWebView2Deferral.md) para concluir a solicitação de abertura de janela posteriormente.</span><span class="sxs-lookup"><span data-stu-id="47b72-153">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="47b72-154">Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="47b72-154">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

