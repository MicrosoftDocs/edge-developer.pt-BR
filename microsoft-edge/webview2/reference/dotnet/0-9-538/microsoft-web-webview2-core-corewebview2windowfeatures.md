---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: d6d6f52456823488c07288c8ed07b9655a29883a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884434"
---
# <span data-ttu-id="7a48e-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="7a48e-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="7a48e-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7a48e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7a48e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="7a48e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7a48e-107">Recursos de janela para uma janela pop-up do WebView.</span><span class="sxs-lookup"><span data-stu-id="7a48e-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="7a48e-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7a48e-108">Summary</span></span>

 <span data-ttu-id="7a48e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7a48e-109">Members</span></span>                        | <span data-ttu-id="7a48e-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7a48e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a48e-111">Comprimento</span><span class="sxs-lookup"><span data-stu-id="7a48e-111">Height</span></span>](#height) | <span data-ttu-id="7a48e-112">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="7a48e-112">The height of the window.</span></span>
[<span data-ttu-id="7a48e-113">Esquerda</span><span class="sxs-lookup"><span data-stu-id="7a48e-113">Left</span></span>](#left) | <span data-ttu-id="7a48e-114">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="7a48e-114">The left position of the window.</span></span>
[<span data-ttu-id="7a48e-115">Menus</span><span class="sxs-lookup"><span data-stu-id="7a48e-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="7a48e-116">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7a48e-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="7a48e-117">Barras</span><span class="sxs-lookup"><span data-stu-id="7a48e-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="7a48e-118">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="7a48e-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="7a48e-119">Status</span><span class="sxs-lookup"><span data-stu-id="7a48e-119">Status</span></span>](#status) | <span data-ttu-id="7a48e-120">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7a48e-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="7a48e-121">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="7a48e-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="7a48e-122">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7a48e-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="7a48e-123">Superior</span><span class="sxs-lookup"><span data-stu-id="7a48e-123">Top</span></span>](#top) | <span data-ttu-id="7a48e-124">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="7a48e-124">The top position of the window.</span></span>
[<span data-ttu-id="7a48e-125">Largura</span><span class="sxs-lookup"><span data-stu-id="7a48e-125">Width</span></span>](#width) | <span data-ttu-id="7a48e-126">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="7a48e-126">The width of the window.</span></span>
[<span data-ttu-id="7a48e-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="7a48e-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="7a48e-128">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="7a48e-128">Has specified left and top values.</span></span>
[<span data-ttu-id="7a48e-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="7a48e-129">HasSize</span></span>](#hassize) | <span data-ttu-id="7a48e-130">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="7a48e-130">Has specified height and width values.</span></span>

## <span data-ttu-id="7a48e-131">Parte</span><span class="sxs-lookup"><span data-stu-id="7a48e-131">Members</span></span>

#### <span data-ttu-id="7a48e-132">Comprimento</span><span class="sxs-lookup"><span data-stu-id="7a48e-132">Height</span></span> 

<span data-ttu-id="7a48e-133">A altura da janela.</span><span class="sxs-lookup"><span data-stu-id="7a48e-133">The height of the window.</span></span>

> <span data-ttu-id="7a48e-134">[altura](#height) do uint público</span><span class="sxs-lookup"><span data-stu-id="7a48e-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="7a48e-135">Esquerda</span><span class="sxs-lookup"><span data-stu-id="7a48e-135">Left</span></span> 

<span data-ttu-id="7a48e-136">A posição esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="7a48e-136">The left position of the window.</span></span>

> <span data-ttu-id="7a48e-137">público uint [esquerdo](#left)</span><span class="sxs-lookup"><span data-stu-id="7a48e-137">public uint [Left](#left)</span></span>

<span data-ttu-id="7a48e-138">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="7a48e-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="7a48e-139">Menus</span><span class="sxs-lookup"><span data-stu-id="7a48e-139">MenuBar</span></span> 

<span data-ttu-id="7a48e-140">Se a barra de menus deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7a48e-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="7a48e-141">[menus](#menubar) int público</span><span class="sxs-lookup"><span data-stu-id="7a48e-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="7a48e-142">Barras</span><span class="sxs-lookup"><span data-stu-id="7a48e-142">ScrollBars</span></span> 

<span data-ttu-id="7a48e-143">Se as barras de rolagem devem ou não ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="7a48e-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="7a48e-144">Barras de [rolagem](#scrollbars) públicas de int</span><span class="sxs-lookup"><span data-stu-id="7a48e-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="7a48e-145">Status</span><span class="sxs-lookup"><span data-stu-id="7a48e-145">Status</span></span> 

<span data-ttu-id="7a48e-146">Se a barra de status deve ou não ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7a48e-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="7a48e-147">[status](#status) de int público</span><span class="sxs-lookup"><span data-stu-id="7a48e-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="7a48e-148">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="7a48e-148">Toolbar</span></span> 

<span data-ttu-id="7a48e-149">Se a barra de ferramentas do navegador deve ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7a48e-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="7a48e-150">Barra de [ferramentas](#toolbar) público int</span><span class="sxs-lookup"><span data-stu-id="7a48e-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="7a48e-151">Superior</span><span class="sxs-lookup"><span data-stu-id="7a48e-151">Top</span></span> 

<span data-ttu-id="7a48e-152">A posição superior da janela.</span><span class="sxs-lookup"><span data-stu-id="7a48e-152">The top position of the window.</span></span>

> <span data-ttu-id="7a48e-153">pública uint [superior](#top)</span><span class="sxs-lookup"><span data-stu-id="7a48e-153">public uint [Top](#top)</span></span>

<span data-ttu-id="7a48e-154">Ocorrerá se HasPosition for falso.</span><span class="sxs-lookup"><span data-stu-id="7a48e-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="7a48e-155">Largura</span><span class="sxs-lookup"><span data-stu-id="7a48e-155">Width</span></span> 

<span data-ttu-id="7a48e-156">A largura da janela.</span><span class="sxs-lookup"><span data-stu-id="7a48e-156">The width of the window.</span></span>

> <span data-ttu-id="7a48e-157">[largura](#width) do uint público</span><span class="sxs-lookup"><span data-stu-id="7a48e-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="7a48e-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="7a48e-158">HasPosition</span></span> 

<span data-ttu-id="7a48e-159">Especificou valores Left e Top.</span><span class="sxs-lookup"><span data-stu-id="7a48e-159">Has specified left and top values.</span></span>

> <span data-ttu-id="7a48e-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="7a48e-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="7a48e-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="7a48e-161">HasSize</span></span> 

<span data-ttu-id="7a48e-162">Tem valores de altura e largura especificados.</span><span class="sxs-lookup"><span data-stu-id="7a48e-162">Has specified height and width values.</span></span>

> <span data-ttu-id="7a48e-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="7a48e-163">public int [HasSize](#hassize)()</span></span>

