---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 4866626111908eae9800da0baabec0356d5d4bf8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879650"
---
# <span data-ttu-id="64c88-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="64c88-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="64c88-105">Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="64c88-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="64c88-106">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="64c88-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="64c88-107">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="64c88-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="64c88-108">Recursos de janela para uma janela pop-up do WebView.</span><span class="sxs-lookup"><span data-stu-id="64c88-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="64c88-109">Resumo</span><span class="sxs-lookup"><span data-stu-id="64c88-109">Summary</span></span>

 <span data-ttu-id="64c88-110">Parte</span><span class="sxs-lookup"><span data-stu-id="64c88-110">Members</span></span>                        | <span data-ttu-id="64c88-111">Descrições</span><span class="sxs-lookup"><span data-stu-id="64c88-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64c88-112">Comprimento</span><span class="sxs-lookup"><span data-stu-id="64c88-112">Height</span></span>](#height) | <span data-ttu-id="64c88-113">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="64c88-113">The height of the window.</span></span>
[<span data-ttu-id="64c88-114">Esquerda</span><span class="sxs-lookup"><span data-stu-id="64c88-114">Left</span></span>](#left) | <span data-ttu-id="64c88-115">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="64c88-115">The left position of the window.</span></span>
[<span data-ttu-id="64c88-116">Menus</span><span class="sxs-lookup"><span data-stu-id="64c88-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="64c88-117">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="64c88-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="64c88-118">Barras</span><span class="sxs-lookup"><span data-stu-id="64c88-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="64c88-119">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="64c88-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="64c88-120">Status</span><span class="sxs-lookup"><span data-stu-id="64c88-120">Status</span></span>](#status) | <span data-ttu-id="64c88-121">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="64c88-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="64c88-122">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="64c88-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="64c88-123">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="64c88-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="64c88-124">Superior</span><span class="sxs-lookup"><span data-stu-id="64c88-124">Top</span></span>](#top) | <span data-ttu-id="64c88-125">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="64c88-125">The top position of the window.</span></span>
[<span data-ttu-id="64c88-126">Largura</span><span class="sxs-lookup"><span data-stu-id="64c88-126">Width</span></span>](#width) | <span data-ttu-id="64c88-127">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="64c88-127">The width of the window.</span></span>
[<span data-ttu-id="64c88-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="64c88-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="64c88-129">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="64c88-129">Has specified left and top values.</span></span>
[<span data-ttu-id="64c88-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="64c88-130">HasSize</span></span>](#hassize) | <span data-ttu-id="64c88-131">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="64c88-131">Has specified height and width values.</span></span>

## <span data-ttu-id="64c88-132">Parte</span><span class="sxs-lookup"><span data-stu-id="64c88-132">Members</span></span>

#### <span data-ttu-id="64c88-133">Comprimento</span><span class="sxs-lookup"><span data-stu-id="64c88-133">Height</span></span> 

<span data-ttu-id="64c88-134">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="64c88-134">The height of the window.</span></span>

> <span data-ttu-id="64c88-135">[altura](#height) do uint público</span><span class="sxs-lookup"><span data-stu-id="64c88-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="64c88-136">Esquerda</span><span class="sxs-lookup"><span data-stu-id="64c88-136">Left</span></span> 

<span data-ttu-id="64c88-137">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="64c88-137">The left position of the window.</span></span>

> <span data-ttu-id="64c88-138">público uint [esquerdo](#left)</span><span class="sxs-lookup"><span data-stu-id="64c88-138">public uint [Left](#left)</span></span>

<span data-ttu-id="64c88-139">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="64c88-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="64c88-140">Menus</span><span class="sxs-lookup"><span data-stu-id="64c88-140">MenuBar</span></span> 

<span data-ttu-id="64c88-141">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="64c88-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="64c88-142">[menus](#menubar) int público</span><span class="sxs-lookup"><span data-stu-id="64c88-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="64c88-143">Barras</span><span class="sxs-lookup"><span data-stu-id="64c88-143">ScrollBars</span></span> 

<span data-ttu-id="64c88-144">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="64c88-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="64c88-145">Barras de [rolagem](#scrollbars) públicas de int</span><span class="sxs-lookup"><span data-stu-id="64c88-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="64c88-146">Status</span><span class="sxs-lookup"><span data-stu-id="64c88-146">Status</span></span> 

<span data-ttu-id="64c88-147">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="64c88-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="64c88-148">[status](#status) de int público</span><span class="sxs-lookup"><span data-stu-id="64c88-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="64c88-149">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="64c88-149">Toolbar</span></span> 

<span data-ttu-id="64c88-150">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="64c88-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="64c88-151">Barra de [ferramentas](#toolbar) público int</span><span class="sxs-lookup"><span data-stu-id="64c88-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="64c88-152">Superior</span><span class="sxs-lookup"><span data-stu-id="64c88-152">Top</span></span> 

<span data-ttu-id="64c88-153">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="64c88-153">The top position of the window.</span></span>

> <span data-ttu-id="64c88-154">pública uint [superior](#top)</span><span class="sxs-lookup"><span data-stu-id="64c88-154">public uint [Top](#top)</span></span>

<span data-ttu-id="64c88-155">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="64c88-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="64c88-156">Largura</span><span class="sxs-lookup"><span data-stu-id="64c88-156">Width</span></span> 

<span data-ttu-id="64c88-157">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="64c88-157">The width of the window.</span></span>

> <span data-ttu-id="64c88-158">[largura](#width) do uint público</span><span class="sxs-lookup"><span data-stu-id="64c88-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="64c88-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="64c88-159">HasPosition</span></span> 

<span data-ttu-id="64c88-160">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="64c88-160">Has specified left and top values.</span></span>

> <span data-ttu-id="64c88-161">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="64c88-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="64c88-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="64c88-162">HasSize</span></span> 

<span data-ttu-id="64c88-163">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="64c88-163">Has specified height and width values.</span></span>

> <span data-ttu-id="64c88-164">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="64c88-164">public int [HasSize](#hassize)()</span></span>

