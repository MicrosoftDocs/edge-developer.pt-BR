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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698378"
---
# <span data-ttu-id="408a2-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="408a2-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="408a2-105">Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="408a2-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="408a2-106">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="408a2-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="408a2-107">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="408a2-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="408a2-108">Recursos de janela para uma janela pop-up do WebView.</span><span class="sxs-lookup"><span data-stu-id="408a2-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="408a2-109">Resumo</span><span class="sxs-lookup"><span data-stu-id="408a2-109">Summary</span></span>

 <span data-ttu-id="408a2-110">Parte</span><span class="sxs-lookup"><span data-stu-id="408a2-110">Members</span></span>                        | <span data-ttu-id="408a2-111">Descrições</span><span class="sxs-lookup"><span data-stu-id="408a2-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="408a2-112">Comprimento</span><span class="sxs-lookup"><span data-stu-id="408a2-112">Height</span></span>](#height) | <span data-ttu-id="408a2-113">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="408a2-113">The height of the window.</span></span>
[<span data-ttu-id="408a2-114">Esquerda</span><span class="sxs-lookup"><span data-stu-id="408a2-114">Left</span></span>](#left) | <span data-ttu-id="408a2-115">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="408a2-115">The left position of the window.</span></span>
[<span data-ttu-id="408a2-116">Menus</span><span class="sxs-lookup"><span data-stu-id="408a2-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="408a2-117">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="408a2-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="408a2-118">Barras</span><span class="sxs-lookup"><span data-stu-id="408a2-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="408a2-119">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="408a2-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="408a2-120">Status</span><span class="sxs-lookup"><span data-stu-id="408a2-120">Status</span></span>](#status) | <span data-ttu-id="408a2-121">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="408a2-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="408a2-122">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="408a2-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="408a2-123">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="408a2-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="408a2-124">Superior</span><span class="sxs-lookup"><span data-stu-id="408a2-124">Top</span></span>](#top) | <span data-ttu-id="408a2-125">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="408a2-125">The top position of the window.</span></span>
[<span data-ttu-id="408a2-126">Largura</span><span class="sxs-lookup"><span data-stu-id="408a2-126">Width</span></span>](#width) | <span data-ttu-id="408a2-127">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="408a2-127">The width of the window.</span></span>
[<span data-ttu-id="408a2-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="408a2-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="408a2-129">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="408a2-129">Has specified left and top values.</span></span>
[<span data-ttu-id="408a2-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="408a2-130">HasSize</span></span>](#hassize) | <span data-ttu-id="408a2-131">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="408a2-131">Has specified height and width values.</span></span>

## <span data-ttu-id="408a2-132">Parte</span><span class="sxs-lookup"><span data-stu-id="408a2-132">Members</span></span>

#### <span data-ttu-id="408a2-133">Comprimento</span><span class="sxs-lookup"><span data-stu-id="408a2-133">Height</span></span> 

<span data-ttu-id="408a2-134">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="408a2-134">The height of the window.</span></span>

> <span data-ttu-id="408a2-135">[altura](#height) do uint público</span><span class="sxs-lookup"><span data-stu-id="408a2-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="408a2-136">Esquerda</span><span class="sxs-lookup"><span data-stu-id="408a2-136">Left</span></span> 

<span data-ttu-id="408a2-137">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="408a2-137">The left position of the window.</span></span>

> <span data-ttu-id="408a2-138">público uint [esquerdo](#left)</span><span class="sxs-lookup"><span data-stu-id="408a2-138">public uint [Left](#left)</span></span>

<span data-ttu-id="408a2-139">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="408a2-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="408a2-140">Menus</span><span class="sxs-lookup"><span data-stu-id="408a2-140">MenuBar</span></span> 

<span data-ttu-id="408a2-141">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="408a2-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="408a2-142">[menus](#menubar) int público</span><span class="sxs-lookup"><span data-stu-id="408a2-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="408a2-143">Barras</span><span class="sxs-lookup"><span data-stu-id="408a2-143">ScrollBars</span></span> 

<span data-ttu-id="408a2-144">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="408a2-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="408a2-145">Barras de [rolagem](#scrollbars) públicas de int</span><span class="sxs-lookup"><span data-stu-id="408a2-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="408a2-146">Status</span><span class="sxs-lookup"><span data-stu-id="408a2-146">Status</span></span> 

<span data-ttu-id="408a2-147">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="408a2-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="408a2-148">[status](#status) de int público</span><span class="sxs-lookup"><span data-stu-id="408a2-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="408a2-149">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="408a2-149">Toolbar</span></span> 

<span data-ttu-id="408a2-150">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="408a2-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="408a2-151">Barra de [ferramentas](#toolbar) público int</span><span class="sxs-lookup"><span data-stu-id="408a2-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="408a2-152">Superior</span><span class="sxs-lookup"><span data-stu-id="408a2-152">Top</span></span> 

<span data-ttu-id="408a2-153">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="408a2-153">The top position of the window.</span></span>

> <span data-ttu-id="408a2-154">pública uint [superior](#top)</span><span class="sxs-lookup"><span data-stu-id="408a2-154">public uint [Top](#top)</span></span>

<span data-ttu-id="408a2-155">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="408a2-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="408a2-156">Largura</span><span class="sxs-lookup"><span data-stu-id="408a2-156">Width</span></span> 

<span data-ttu-id="408a2-157">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="408a2-157">The width of the window.</span></span>

> <span data-ttu-id="408a2-158">[largura](#width) do uint público</span><span class="sxs-lookup"><span data-stu-id="408a2-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="408a2-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="408a2-159">HasPosition</span></span> 

<span data-ttu-id="408a2-160">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="408a2-160">Has specified left and top values.</span></span>

> <span data-ttu-id="408a2-161">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="408a2-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="408a2-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="408a2-162">HasSize</span></span> 

<span data-ttu-id="408a2-163">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="408a2-163">Has specified height and width values.</span></span>

> <span data-ttu-id="408a2-164">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="408a2-164">public int [HasSize](#hassize)()</span></span>

