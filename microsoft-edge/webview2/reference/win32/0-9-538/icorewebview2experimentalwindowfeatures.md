---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 576f54f2a7ecc2e1e99758719e80cc589c5bc791
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698398"
---
# <span data-ttu-id="9aa58-104">interface ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="9aa58-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="9aa58-105">Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="9aa58-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="9aa58-106">Recursos de janela para uma janela pop-up do WebView.</span><span class="sxs-lookup"><span data-stu-id="9aa58-106">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="9aa58-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="9aa58-107">Summary</span></span>

 <span data-ttu-id="9aa58-108">Parte</span><span class="sxs-lookup"><span data-stu-id="9aa58-108">Members</span></span>                        | <span data-ttu-id="9aa58-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="9aa58-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9aa58-110">get_Height</span><span class="sxs-lookup"><span data-stu-id="9aa58-110">get_Height</span></span>](#get_height) | <span data-ttu-id="9aa58-111">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="9aa58-111">The height of the window.</span></span>
[<span data-ttu-id="9aa58-112">get_Left</span><span class="sxs-lookup"><span data-stu-id="9aa58-112">get_Left</span></span>](#get_left) | <span data-ttu-id="9aa58-113">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="9aa58-113">The left position of the window.</span></span> <span data-ttu-id="9aa58-114">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="9aa58-114">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="9aa58-115">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="9aa58-115">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="9aa58-116">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="9aa58-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="9aa58-117">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="9aa58-117">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="9aa58-118">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="9aa58-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="9aa58-119">get_Status</span><span class="sxs-lookup"><span data-stu-id="9aa58-119">get_Status</span></span>](#get_status) | <span data-ttu-id="9aa58-120">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="9aa58-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="9aa58-121">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="9aa58-121">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="9aa58-122">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="9aa58-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="9aa58-123">get_Top</span><span class="sxs-lookup"><span data-stu-id="9aa58-123">get_Top</span></span>](#get_top) | <span data-ttu-id="9aa58-124">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="9aa58-124">The top position of the window.</span></span> <span data-ttu-id="9aa58-125">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="9aa58-125">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="9aa58-126">get_Width</span><span class="sxs-lookup"><span data-stu-id="9aa58-126">get_Width</span></span>](#get_width) | <span data-ttu-id="9aa58-127">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="9aa58-127">The width of the window.</span></span>
[<span data-ttu-id="9aa58-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="9aa58-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="9aa58-129">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="9aa58-129">Has specified left and top values.</span></span>
[<span data-ttu-id="9aa58-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="9aa58-130">HasSize</span></span>](#hassize) | <span data-ttu-id="9aa58-131">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="9aa58-131">Has specified height and width values.</span></span>

<span data-ttu-id="9aa58-132">Esses campos correspondem a ' windowFeatures ' passada para Window. Open conforme especificado na[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="9aa58-132">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="9aa58-133">Parte</span><span class="sxs-lookup"><span data-stu-id="9aa58-133">Members</span></span>

#### <span data-ttu-id="9aa58-134">get_Height</span><span class="sxs-lookup"><span data-stu-id="9aa58-134">get_Height</span></span> 

<span data-ttu-id="9aa58-135">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="9aa58-135">The height of the window.</span></span>

> <span data-ttu-id="9aa58-136">[get_Height](#get_height)público HRESULT (UINT32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="9aa58-136">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="9aa58-137">O valor mínimo é 100.</span><span class="sxs-lookup"><span data-stu-id="9aa58-137">Minimum value is 100.</span></span> <span data-ttu-id="9aa58-138">Ocorrerá se HasSize for falso.</span><span class="sxs-lookup"><span data-stu-id="9aa58-138">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="9aa58-139">get_Left</span><span class="sxs-lookup"><span data-stu-id="9aa58-139">get_Left</span></span> 

<span data-ttu-id="9aa58-140">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="9aa58-140">The left position of the window.</span></span> <span data-ttu-id="9aa58-141">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="9aa58-141">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="9aa58-142">[get_Left](#get_left)público HRESULT (UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="9aa58-142">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="9aa58-143">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="9aa58-143">get_MenuBar</span></span> 

<span data-ttu-id="9aa58-144">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="9aa58-144">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="9aa58-145">[get_MenuBar](#get_menubar)público HRESULT (bool \* BarraDeMenu)</span><span class="sxs-lookup"><span data-stu-id="9aa58-145">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="9aa58-146">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="9aa58-146">get_ScrollBars</span></span> 

<span data-ttu-id="9aa58-147">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="9aa58-147">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="9aa58-148">público HRESULT [get_ScrollBars](#get_scrollbars)(bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="9aa58-148">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="9aa58-149">get_Status</span><span class="sxs-lookup"><span data-stu-id="9aa58-149">get_Status</span></span> 

<span data-ttu-id="9aa58-150">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="9aa58-150">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="9aa58-151">[get_Status](#get_status)público HRESULT (status bool \*)</span><span class="sxs-lookup"><span data-stu-id="9aa58-151">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="9aa58-152">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="9aa58-152">get_Toolbar</span></span> 

<span data-ttu-id="9aa58-153">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="9aa58-153">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="9aa58-154">[get_Toolbar](#get_toolbar)público HRESULT (barra de ferramentas bool \*)</span><span class="sxs-lookup"><span data-stu-id="9aa58-154">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="9aa58-155">get_Top</span><span class="sxs-lookup"><span data-stu-id="9aa58-155">get_Top</span></span> 

<span data-ttu-id="9aa58-156">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="9aa58-156">The top position of the window.</span></span> <span data-ttu-id="9aa58-157">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="9aa58-157">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="9aa58-158">[get_Top](#get_top)público HRESULT (UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="9aa58-158">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="9aa58-159">get_Width</span><span class="sxs-lookup"><span data-stu-id="9aa58-159">get_Width</span></span> 

<span data-ttu-id="9aa58-160">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="9aa58-160">The width of the window.</span></span>

> <span data-ttu-id="9aa58-161">público HRESULT [get_Width](#get_width)(UINT32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="9aa58-161">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="9aa58-162">O valor mínimo é 100.</span><span class="sxs-lookup"><span data-stu-id="9aa58-162">Minimum value is 100.</span></span> <span data-ttu-id="9aa58-163">Ocorrerá se HasSize for falso.</span><span class="sxs-lookup"><span data-stu-id="9aa58-163">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="9aa58-164">HasPosition</span><span class="sxs-lookup"><span data-stu-id="9aa58-164">HasPosition</span></span> 

<span data-ttu-id="9aa58-165">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="9aa58-165">Has specified left and top values.</span></span>

> <span data-ttu-id="9aa58-166">Public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="9aa58-166">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="9aa58-167">HasSize</span><span class="sxs-lookup"><span data-stu-id="9aa58-167">HasSize</span></span> 

<span data-ttu-id="9aa58-168">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="9aa58-168">Has specified height and width values.</span></span>

> <span data-ttu-id="9aa58-169">Public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="9aa58-169">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

