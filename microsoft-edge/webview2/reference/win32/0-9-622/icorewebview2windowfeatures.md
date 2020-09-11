---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WindowFeatures
ms.openlocfilehash: 90b5a09a752250dc342e7eefad031c9b5b83d345
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011537"
---
# <span data-ttu-id="eeea9-104">interface ICoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="eeea9-104">interface ICoreWebView2WindowFeatures</span></span> 

```
interface ICoreWebView2WindowFeatures
  : public IUnknown
```

<span data-ttu-id="eeea9-105">Recursos de janela para uma janela pop-up do WebView.</span><span class="sxs-lookup"><span data-stu-id="eeea9-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="eeea9-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="eeea9-106">Summary</span></span>

 <span data-ttu-id="eeea9-107">Parte</span><span class="sxs-lookup"><span data-stu-id="eeea9-107">Members</span></span>                        | <span data-ttu-id="eeea9-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="eeea9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eeea9-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="eeea9-109">get_Height</span></span>](#get_height) | <span data-ttu-id="eeea9-110">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="eeea9-110">The height of the window.</span></span>
[<span data-ttu-id="eeea9-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="eeea9-111">get_Left</span></span>](#get_left) | <span data-ttu-id="eeea9-112">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="eeea9-112">The left position of the window.</span></span> <span data-ttu-id="eeea9-113">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="eeea9-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="eeea9-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="eeea9-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="eeea9-115">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="eeea9-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="eeea9-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="eeea9-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="eeea9-117">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="eeea9-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="eeea9-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="eeea9-118">get_Status</span></span>](#get_status) | <span data-ttu-id="eeea9-119">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="eeea9-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="eeea9-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="eeea9-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="eeea9-121">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="eeea9-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="eeea9-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="eeea9-122">get_Top</span></span>](#get_top) | <span data-ttu-id="eeea9-123">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="eeea9-123">The top position of the window.</span></span> <span data-ttu-id="eeea9-124">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="eeea9-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="eeea9-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="eeea9-125">get_Width</span></span>](#get_width) | <span data-ttu-id="eeea9-126">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="eeea9-126">The width of the window.</span></span>
[<span data-ttu-id="eeea9-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="eeea9-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="eeea9-128">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="eeea9-128">Has specified left and top values.</span></span>
[<span data-ttu-id="eeea9-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="eeea9-129">HasSize</span></span>](#hassize) | <span data-ttu-id="eeea9-130">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="eeea9-130">Has specified height and width values.</span></span>

<span data-ttu-id="eeea9-131">Esses campos correspondem a ' windowFeatures ' passada para Window. Open conforme especificado na [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="eeea9-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="eeea9-132">Parte</span><span class="sxs-lookup"><span data-stu-id="eeea9-132">Members</span></span>

#### <span data-ttu-id="eeea9-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="eeea9-133">get_Height</span></span> 

<span data-ttu-id="eeea9-134">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="eeea9-134">The height of the window.</span></span>

> <span data-ttu-id="eeea9-135">[get_Height](#get_height)público HRESULT (UINT32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="eeea9-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="eeea9-136">O valor mínimo é 100.</span><span class="sxs-lookup"><span data-stu-id="eeea9-136">Minimum value is 100.</span></span> <span data-ttu-id="eeea9-137">Ocorrerá se HasSize for falso.</span><span class="sxs-lookup"><span data-stu-id="eeea9-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="eeea9-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="eeea9-138">get_Left</span></span> 

<span data-ttu-id="eeea9-139">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="eeea9-139">The left position of the window.</span></span> <span data-ttu-id="eeea9-140">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="eeea9-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="eeea9-141">[get_Left](#get_left)público HRESULT (UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="eeea9-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="eeea9-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="eeea9-142">get_MenuBar</span></span> 

<span data-ttu-id="eeea9-143">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="eeea9-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="eeea9-144">[get_MenuBar](#get_menubar)público HRESULT (bool \* BarraDeMenu)</span><span class="sxs-lookup"><span data-stu-id="eeea9-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="eeea9-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="eeea9-145">get_ScrollBars</span></span> 

<span data-ttu-id="eeea9-146">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="eeea9-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="eeea9-147">público HRESULT [get_ScrollBars](#get_scrollbars)(bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="eeea9-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="eeea9-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="eeea9-148">get_Status</span></span> 

<span data-ttu-id="eeea9-149">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="eeea9-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="eeea9-150">[get_Status](#get_status)público HRESULT (status bool \*)</span><span class="sxs-lookup"><span data-stu-id="eeea9-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="eeea9-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="eeea9-151">get_Toolbar</span></span> 

<span data-ttu-id="eeea9-152">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="eeea9-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="eeea9-153">[get_Toolbar](#get_toolbar)público HRESULT (barra de ferramentas bool \*)</span><span class="sxs-lookup"><span data-stu-id="eeea9-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="eeea9-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="eeea9-154">get_Top</span></span> 

<span data-ttu-id="eeea9-155">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="eeea9-155">The top position of the window.</span></span> <span data-ttu-id="eeea9-156">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="eeea9-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="eeea9-157">[get_Top](#get_top)público HRESULT (UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="eeea9-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="eeea9-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="eeea9-158">get_Width</span></span> 

<span data-ttu-id="eeea9-159">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="eeea9-159">The width of the window.</span></span>

> <span data-ttu-id="eeea9-160">público HRESULT [get_Width](#get_width)(UINT32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="eeea9-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="eeea9-161">O valor mínimo é 100.</span><span class="sxs-lookup"><span data-stu-id="eeea9-161">Minimum value is 100.</span></span> <span data-ttu-id="eeea9-162">Ocorrerá se HasSize for falso.</span><span class="sxs-lookup"><span data-stu-id="eeea9-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="eeea9-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="eeea9-163">HasPosition</span></span> 

<span data-ttu-id="eeea9-164">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="eeea9-164">Has specified left and top values.</span></span>

> <span data-ttu-id="eeea9-165">Public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="eeea9-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="eeea9-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="eeea9-166">HasSize</span></span> 

<span data-ttu-id="eeea9-167">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="eeea9-167">Has specified height and width values.</span></span>

> <span data-ttu-id="eeea9-168">Public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="eeea9-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

