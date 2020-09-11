---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: ee740f7d227ae98d451ba1c5e8f1017fe92514a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011367"
---
# <span data-ttu-id="52a7a-104">0.9.579-ICoreWebView2ExperimentalWindowFeatures de interface</span><span class="sxs-lookup"><span data-stu-id="52a7a-104">0.9.579 - interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="52a7a-105">Recursos de janela para uma janela pop-up do WebView.</span><span class="sxs-lookup"><span data-stu-id="52a7a-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="52a7a-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="52a7a-106">Summary</span></span>

 <span data-ttu-id="52a7a-107">Parte</span><span class="sxs-lookup"><span data-stu-id="52a7a-107">Members</span></span>                        | <span data-ttu-id="52a7a-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="52a7a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52a7a-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="52a7a-109">get_Height</span></span>](#get_height) | <span data-ttu-id="52a7a-110">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="52a7a-110">The height of the window.</span></span>
[<span data-ttu-id="52a7a-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="52a7a-111">get_Left</span></span>](#get_left) | <span data-ttu-id="52a7a-112">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="52a7a-112">The left position of the window.</span></span> <span data-ttu-id="52a7a-113">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="52a7a-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="52a7a-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="52a7a-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="52a7a-115">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="52a7a-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="52a7a-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="52a7a-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="52a7a-117">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="52a7a-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="52a7a-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="52a7a-118">get_Status</span></span>](#get_status) | <span data-ttu-id="52a7a-119">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="52a7a-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="52a7a-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="52a7a-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="52a7a-121">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="52a7a-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="52a7a-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="52a7a-122">get_Top</span></span>](#get_top) | <span data-ttu-id="52a7a-123">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="52a7a-123">The top position of the window.</span></span> <span data-ttu-id="52a7a-124">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="52a7a-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="52a7a-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="52a7a-125">get_Width</span></span>](#get_width) | <span data-ttu-id="52a7a-126">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="52a7a-126">The width of the window.</span></span>
[<span data-ttu-id="52a7a-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="52a7a-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="52a7a-128">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="52a7a-128">Has specified left and top values.</span></span>
[<span data-ttu-id="52a7a-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="52a7a-129">HasSize</span></span>](#hassize) | <span data-ttu-id="52a7a-130">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="52a7a-130">Has specified height and width values.</span></span>

<span data-ttu-id="52a7a-131">Esses campos correspondem a ' windowFeatures ' passada para Window. Open conforme especificado na [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="52a7a-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="52a7a-132">Parte</span><span class="sxs-lookup"><span data-stu-id="52a7a-132">Members</span></span>

#### <span data-ttu-id="52a7a-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="52a7a-133">get_Height</span></span> 

<span data-ttu-id="52a7a-134">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="52a7a-134">The height of the window.</span></span>

> <span data-ttu-id="52a7a-135">[get_Height](#get_height)público HRESULT (UINT32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="52a7a-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="52a7a-136">O valor mínimo é 100.</span><span class="sxs-lookup"><span data-stu-id="52a7a-136">Minimum value is 100.</span></span> <span data-ttu-id="52a7a-137">Ocorrerá se HasSize for falso.</span><span class="sxs-lookup"><span data-stu-id="52a7a-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="52a7a-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="52a7a-138">get_Left</span></span> 

<span data-ttu-id="52a7a-139">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="52a7a-139">The left position of the window.</span></span> <span data-ttu-id="52a7a-140">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="52a7a-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="52a7a-141">[get_Left](#get_left)público HRESULT (UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="52a7a-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="52a7a-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="52a7a-142">get_MenuBar</span></span> 

<span data-ttu-id="52a7a-143">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="52a7a-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="52a7a-144">[get_MenuBar](#get_menubar)público HRESULT (bool \* BarraDeMenu)</span><span class="sxs-lookup"><span data-stu-id="52a7a-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="52a7a-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="52a7a-145">get_ScrollBars</span></span> 

<span data-ttu-id="52a7a-146">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="52a7a-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="52a7a-147">público HRESULT [get_ScrollBars](#get_scrollbars)(bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="52a7a-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="52a7a-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="52a7a-148">get_Status</span></span> 

<span data-ttu-id="52a7a-149">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="52a7a-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="52a7a-150">[get_Status](#get_status)público HRESULT (status bool \*)</span><span class="sxs-lookup"><span data-stu-id="52a7a-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="52a7a-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="52a7a-151">get_Toolbar</span></span> 

<span data-ttu-id="52a7a-152">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="52a7a-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="52a7a-153">[get_Toolbar](#get_toolbar)público HRESULT (barra de ferramentas bool \*)</span><span class="sxs-lookup"><span data-stu-id="52a7a-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="52a7a-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="52a7a-154">get_Top</span></span> 

<span data-ttu-id="52a7a-155">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="52a7a-155">The top position of the window.</span></span> <span data-ttu-id="52a7a-156">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="52a7a-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="52a7a-157">[get_Top](#get_top)público HRESULT (UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="52a7a-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="52a7a-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="52a7a-158">get_Width</span></span> 

<span data-ttu-id="52a7a-159">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="52a7a-159">The width of the window.</span></span>

> <span data-ttu-id="52a7a-160">público HRESULT [get_Width](#get_width)(UINT32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="52a7a-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="52a7a-161">O valor mínimo é 100.</span><span class="sxs-lookup"><span data-stu-id="52a7a-161">Minimum value is 100.</span></span> <span data-ttu-id="52a7a-162">Ocorrerá se HasSize for falso.</span><span class="sxs-lookup"><span data-stu-id="52a7a-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="52a7a-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="52a7a-163">HasPosition</span></span> 

<span data-ttu-id="52a7a-164">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="52a7a-164">Has specified left and top values.</span></span>

> <span data-ttu-id="52a7a-165">Public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="52a7a-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="52a7a-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="52a7a-166">HasSize</span></span> 

<span data-ttu-id="52a7a-167">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="52a7a-167">Has specified height and width values.</span></span>

> <span data-ttu-id="52a7a-168">Public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="52a7a-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

