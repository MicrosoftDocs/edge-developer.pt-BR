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
ms.openlocfilehash: e8563bdd77972945a1e4b81662071d07d1efeb02
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698265"
---
# <span data-ttu-id="9d219-104">Struct Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4</span><span class="sxs-lookup"><span data-stu-id="9d219-104">Microsoft.Web.WebView2.Core.CoreWebView2Matrix4x4 struct</span></span> 

> [!NOTE]
> <span data-ttu-id="9d219-105">Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="9d219-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="9d219-106">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9d219-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9d219-107">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="9d219-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9d219-108">Essa transformação é usada para calcular as coordenadas corretas ao chamar CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="9d219-108">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span>

## <span data-ttu-id="9d219-109">Resumo</span><span class="sxs-lookup"><span data-stu-id="9d219-109">Summary</span></span>

 <span data-ttu-id="9d219-110">Parte</span><span class="sxs-lookup"><span data-stu-id="9d219-110">Members</span></span>                        | <span data-ttu-id="9d219-111">Descrições</span><span class="sxs-lookup"><span data-stu-id="9d219-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d219-112">_11</span><span class="sxs-lookup"><span data-stu-id="9d219-112">_11</span></span>](#_11) | <span data-ttu-id="9d219-113">O valor na primeira linha e primeira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-113">The value in the first row and first column of the matrix.</span></span>
[<span data-ttu-id="9d219-114">_12</span><span class="sxs-lookup"><span data-stu-id="9d219-114">_12</span></span>](#_12) | <span data-ttu-id="9d219-115">O valor na primeira linha e segunda coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-115">The value in the first row and second column of the matrix.</span></span>
[<span data-ttu-id="9d219-116">_13</span><span class="sxs-lookup"><span data-stu-id="9d219-116">_13</span></span>](#_13) | <span data-ttu-id="9d219-117">O valor na primeira linha e terceira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-117">The value in the first row and third column of the matrix.</span></span>
[<span data-ttu-id="9d219-118">_14</span><span class="sxs-lookup"><span data-stu-id="9d219-118">_14</span></span>](#_14) | <span data-ttu-id="9d219-119">O valor na primeira linha e na quarta coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-119">The value in the first row and fourth column of the matrix.</span></span>
[<span data-ttu-id="9d219-120">_21</span><span class="sxs-lookup"><span data-stu-id="9d219-120">_21</span></span>](#_21) | <span data-ttu-id="9d219-121">O valor na segunda linha e primeira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-121">The value in the second row and first column of the matrix.</span></span>
[<span data-ttu-id="9d219-122">_22</span><span class="sxs-lookup"><span data-stu-id="9d219-122">_22</span></span>](#_22) | <span data-ttu-id="9d219-123">O valor na segunda linha e na segunda coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-123">The value in the second row and second column of the matrix.</span></span>
[<span data-ttu-id="9d219-124">_23</span><span class="sxs-lookup"><span data-stu-id="9d219-124">_23</span></span>](#_23) | <span data-ttu-id="9d219-125">O valor na segunda linha e na terceira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-125">The value in the second row and third column of the matrix.</span></span>
[<span data-ttu-id="9d219-126">_24</span><span class="sxs-lookup"><span data-stu-id="9d219-126">_24</span></span>](#_24) | <span data-ttu-id="9d219-127">O valor na segunda linha e na quarta coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-127">The value in the second row and fourth column of the matrix.</span></span>
[<span data-ttu-id="9d219-128">_31</span><span class="sxs-lookup"><span data-stu-id="9d219-128">_31</span></span>](#_31) | <span data-ttu-id="9d219-129">O valor na terceira linha e primeira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-129">The value in the third row and first column of the matrix.</span></span>
[<span data-ttu-id="9d219-130">_32</span><span class="sxs-lookup"><span data-stu-id="9d219-130">_32</span></span>](#_32) | <span data-ttu-id="9d219-131">O valor na terceira linha e na segunda coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-131">The value in the third row and second column of the matrix.</span></span>
[<span data-ttu-id="9d219-132">_33</span><span class="sxs-lookup"><span data-stu-id="9d219-132">_33</span></span>](#_33) | <span data-ttu-id="9d219-133">O valor na terceira linha e na terceira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-133">The value in the third row and third column of the matrix.</span></span>
[<span data-ttu-id="9d219-134">_34</span><span class="sxs-lookup"><span data-stu-id="9d219-134">_34</span></span>](#_34) | <span data-ttu-id="9d219-135">O valor na terceira linha e na quarta coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-135">The value in the third row and fourth column of the matrix.</span></span>
[<span data-ttu-id="9d219-136">_41</span><span class="sxs-lookup"><span data-stu-id="9d219-136">_41</span></span>](#_41) | <span data-ttu-id="9d219-137">O valor na quarta linha e primeira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-137">The value in the fourth row and first column of the matrix.</span></span>
[<span data-ttu-id="9d219-138">_42</span><span class="sxs-lookup"><span data-stu-id="9d219-138">_42</span></span>](#_42) | <span data-ttu-id="9d219-139">O valor na quarta linha e na segunda coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-139">The value in the fourth row and second column of the matrix.</span></span>
[<span data-ttu-id="9d219-140">_43</span><span class="sxs-lookup"><span data-stu-id="9d219-140">_43</span></span>](#_43) | <span data-ttu-id="9d219-141">O valor na quarta linha e na terceira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-141">The value in the fourth row and third column of the matrix.</span></span>
[<span data-ttu-id="9d219-142">_44</span><span class="sxs-lookup"><span data-stu-id="9d219-142">_44</span></span>](#_44) | <span data-ttu-id="9d219-143">O valor na quarta linha e na quarta coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-143">The value in the fourth row and fourth column of the matrix.</span></span>

<span data-ttu-id="9d219-144">Isso equivale a um D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="9d219-144">This is equivalent to a D2D1_MATRIX_4X4_F.</span></span>

## <span data-ttu-id="9d219-145">Parte</span><span class="sxs-lookup"><span data-stu-id="9d219-145">Members</span></span>

#### <span data-ttu-id="9d219-146">_11</span><span class="sxs-lookup"><span data-stu-id="9d219-146">_11</span></span> 

<span data-ttu-id="9d219-147">O valor na primeira linha e primeira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-147">The value in the first row and first column of the matrix.</span></span>

> <span data-ttu-id="9d219-148">Único [_11](#_11) público</span><span class="sxs-lookup"><span data-stu-id="9d219-148">public Single [_11](#_11)</span></span>

#### <span data-ttu-id="9d219-149">_12</span><span class="sxs-lookup"><span data-stu-id="9d219-149">_12</span></span> 

<span data-ttu-id="9d219-150">O valor na primeira linha e segunda coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-150">The value in the first row and second column of the matrix.</span></span>

> <span data-ttu-id="9d219-151">Único [_12](#_12) público</span><span class="sxs-lookup"><span data-stu-id="9d219-151">public Single [_12](#_12)</span></span>

#### <span data-ttu-id="9d219-152">_13</span><span class="sxs-lookup"><span data-stu-id="9d219-152">_13</span></span> 

<span data-ttu-id="9d219-153">O valor na primeira linha e terceira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-153">The value in the first row and third column of the matrix.</span></span>

> <span data-ttu-id="9d219-154">Único [_13](#_13) público</span><span class="sxs-lookup"><span data-stu-id="9d219-154">public Single [_13](#_13)</span></span>

#### <span data-ttu-id="9d219-155">_14</span><span class="sxs-lookup"><span data-stu-id="9d219-155">_14</span></span> 

<span data-ttu-id="9d219-156">O valor na primeira linha e na quarta coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-156">The value in the first row and fourth column of the matrix.</span></span>

> <span data-ttu-id="9d219-157">Único [_14](#_14) público</span><span class="sxs-lookup"><span data-stu-id="9d219-157">public Single [_14](#_14)</span></span>

#### <span data-ttu-id="9d219-158">_21</span><span class="sxs-lookup"><span data-stu-id="9d219-158">_21</span></span> 

<span data-ttu-id="9d219-159">O valor na segunda linha e primeira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-159">The value in the second row and first column of the matrix.</span></span>

> <span data-ttu-id="9d219-160">Único [_21](#_21) público</span><span class="sxs-lookup"><span data-stu-id="9d219-160">public Single [_21](#_21)</span></span>

#### <span data-ttu-id="9d219-161">_22</span><span class="sxs-lookup"><span data-stu-id="9d219-161">_22</span></span> 

<span data-ttu-id="9d219-162">O valor na segunda linha e na segunda coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-162">The value in the second row and second column of the matrix.</span></span>

> <span data-ttu-id="9d219-163">Único [_22](#_22) público</span><span class="sxs-lookup"><span data-stu-id="9d219-163">public Single [_22](#_22)</span></span>

#### <span data-ttu-id="9d219-164">_23</span><span class="sxs-lookup"><span data-stu-id="9d219-164">_23</span></span> 

<span data-ttu-id="9d219-165">O valor na segunda linha e na terceira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-165">The value in the second row and third column of the matrix.</span></span>

> <span data-ttu-id="9d219-166">Único [_23](#_23) público</span><span class="sxs-lookup"><span data-stu-id="9d219-166">public Single [_23](#_23)</span></span>

#### <span data-ttu-id="9d219-167">_24</span><span class="sxs-lookup"><span data-stu-id="9d219-167">_24</span></span> 

<span data-ttu-id="9d219-168">O valor na segunda linha e na quarta coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-168">The value in the second row and fourth column of the matrix.</span></span>

> <span data-ttu-id="9d219-169">Único [_24](#_24) público</span><span class="sxs-lookup"><span data-stu-id="9d219-169">public Single [_24](#_24)</span></span>

#### <span data-ttu-id="9d219-170">_31</span><span class="sxs-lookup"><span data-stu-id="9d219-170">_31</span></span> 

<span data-ttu-id="9d219-171">O valor na terceira linha e primeira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-171">The value in the third row and first column of the matrix.</span></span>

> <span data-ttu-id="9d219-172">Único [_31](#_31) público</span><span class="sxs-lookup"><span data-stu-id="9d219-172">public Single [_31](#_31)</span></span>

#### <span data-ttu-id="9d219-173">_32</span><span class="sxs-lookup"><span data-stu-id="9d219-173">_32</span></span> 

<span data-ttu-id="9d219-174">O valor na terceira linha e na segunda coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-174">The value in the third row and second column of the matrix.</span></span>

> <span data-ttu-id="9d219-175">Único [_32](#_32) público</span><span class="sxs-lookup"><span data-stu-id="9d219-175">public Single [_32](#_32)</span></span>

#### <span data-ttu-id="9d219-176">_33</span><span class="sxs-lookup"><span data-stu-id="9d219-176">_33</span></span> 

<span data-ttu-id="9d219-177">O valor na terceira linha e na terceira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-177">The value in the third row and third column of the matrix.</span></span>

> <span data-ttu-id="9d219-178">Único [_33](#_33) público</span><span class="sxs-lookup"><span data-stu-id="9d219-178">public Single [_33](#_33)</span></span>

#### <span data-ttu-id="9d219-179">_34</span><span class="sxs-lookup"><span data-stu-id="9d219-179">_34</span></span> 

<span data-ttu-id="9d219-180">O valor na terceira linha e na quarta coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-180">The value in the third row and fourth column of the matrix.</span></span>

> <span data-ttu-id="9d219-181">Único [_34](#_34) público</span><span class="sxs-lookup"><span data-stu-id="9d219-181">public Single [_34](#_34)</span></span>

#### <span data-ttu-id="9d219-182">_41</span><span class="sxs-lookup"><span data-stu-id="9d219-182">_41</span></span> 

<span data-ttu-id="9d219-183">O valor na quarta linha e primeira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-183">The value in the fourth row and first column of the matrix.</span></span>

> <span data-ttu-id="9d219-184">Único [_41](#_41) público</span><span class="sxs-lookup"><span data-stu-id="9d219-184">public Single [_41](#_41)</span></span>

#### <span data-ttu-id="9d219-185">_42</span><span class="sxs-lookup"><span data-stu-id="9d219-185">_42</span></span> 

<span data-ttu-id="9d219-186">O valor na quarta linha e na segunda coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-186">The value in the fourth row and second column of the matrix.</span></span>

> <span data-ttu-id="9d219-187">Único [_42](#_42) público</span><span class="sxs-lookup"><span data-stu-id="9d219-187">public Single [_42](#_42)</span></span>

#### <span data-ttu-id="9d219-188">_43</span><span class="sxs-lookup"><span data-stu-id="9d219-188">_43</span></span> 

<span data-ttu-id="9d219-189">O valor na quarta linha e na terceira coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-189">The value in the fourth row and third column of the matrix.</span></span>

> <span data-ttu-id="9d219-190">Único [_43](#_43) público</span><span class="sxs-lookup"><span data-stu-id="9d219-190">public Single [_43](#_43)</span></span>

#### <span data-ttu-id="9d219-191">_44</span><span class="sxs-lookup"><span data-stu-id="9d219-191">_44</span></span> 

<span data-ttu-id="9d219-192">O valor na quarta linha e na quarta coluna da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d219-192">The value in the fourth row and fourth column of the matrix.</span></span>

> <span data-ttu-id="9d219-193">Único [_44](#_44) público</span><span class="sxs-lookup"><span data-stu-id="9d219-193">public Single [_44](#_44)</span></span>

