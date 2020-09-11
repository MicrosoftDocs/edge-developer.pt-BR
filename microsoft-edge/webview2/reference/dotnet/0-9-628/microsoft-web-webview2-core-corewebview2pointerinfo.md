---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 34ffa5fe0eabfe8e822db2792d2b25ab5106442a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011475"
---
# <span data-ttu-id="3d4d7-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="3d4d7-104">Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

<span data-ttu-id="3d4d7-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3d4d7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3d4d7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="3d4d7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3d4d7-107">Isso basicamente representa um objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combinado.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="3d4d7-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="3d4d7-108">Summary</span></span>

 <span data-ttu-id="3d4d7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3d4d7-109">Members</span></span>                        | <span data-ttu-id="3d4d7-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="3d4d7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d4d7-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="3d4d7-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="3d4d7-112">O ButtonChangeKind do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="3d4d7-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="3d4d7-114">O DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="3d4d7-115">Frameid</span><span class="sxs-lookup"><span data-stu-id="3d4d7-115">FrameId</span></span>](#frameid) | <span data-ttu-id="3d4d7-116">O Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="3d4d7-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="3d4d7-118">O HimetricLocation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="3d4d7-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="3d4d7-120">O HimetricLocationRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="3d4d7-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="3d4d7-122">O HistoryCount do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-123">InputData</span><span class="sxs-lookup"><span data-stu-id="3d4d7-123">InputData</span></span>](#inputdata) | <span data-ttu-id="3d4d7-124">O InputData do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-125">Estado da subsessão</span><span class="sxs-lookup"><span data-stu-id="3d4d7-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="3d4d7-126">O estado do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="3d4d7-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="3d4d7-128">O PenFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="3d4d7-129">PenMask</span></span>](#penmask) | <span data-ttu-id="3d4d7-130">O PenMask do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="3d4d7-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="3d4d7-132">O PenPressure do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="3d4d7-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="3d4d7-134">O PenRotation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="3d4d7-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="3d4d7-136">O PenTiltX do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="3d4d7-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="3d4d7-138">O PenTiltY do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="3d4d7-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="3d4d7-140">O PerformanceCount do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="3d4d7-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="3d4d7-142">O PixelLocation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="3d4d7-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="3d4d7-144">O PixelLocationRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="3d4d7-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="3d4d7-146">O PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="3d4d7-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="3d4d7-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="3d4d7-148">O PointerFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-149">Ponteiroid</span><span class="sxs-lookup"><span data-stu-id="3d4d7-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="3d4d7-150">O Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="3d4d7-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="3d4d7-152">O PointerKind do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-153">Hora</span><span class="sxs-lookup"><span data-stu-id="3d4d7-153">Time</span></span>](#time) | <span data-ttu-id="3d4d7-154">A hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="3d4d7-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="3d4d7-156">O TouchContact do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="3d4d7-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="3d4d7-158">O TouchContactRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="3d4d7-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="3d4d7-160">O TouchFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="3d4d7-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="3d4d7-162">O TouchMask do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="3d4d7-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="3d4d7-164">O TouchOrientation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="3d4d7-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="3d4d7-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="3d4d7-166">O TouchPressure do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="3d4d7-167">Parte</span><span class="sxs-lookup"><span data-stu-id="3d4d7-167">Members</span></span>

#### <span data-ttu-id="3d4d7-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="3d4d7-168">ButtonChangeKind</span></span> 

<span data-ttu-id="3d4d7-169">O ButtonChangeKind do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-170">public int [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="3d4d7-171">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="3d4d7-172">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="3d4d7-173">DisplayRect</span></span> 

<span data-ttu-id="3d4d7-174">O DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="3d4d7-175">[DisplayRect](#displayrect) de retângulo público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-175">public Rectangle [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="3d4d7-176">Frameid</span><span class="sxs-lookup"><span data-stu-id="3d4d7-176">FrameId</span></span> 

<span data-ttu-id="3d4d7-177">O Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-178">[frameid](#frameid) uint público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="3d4d7-179">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="3d4d7-180">HimetricLocation</span></span> 

<span data-ttu-id="3d4d7-181">O HimetricLocation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-182">[HimetricLocation](#himetriclocation) de ponto público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="3d4d7-183">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="3d4d7-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="3d4d7-185">O HimetricLocationRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-186">[HimetricLocationRaw](#himetriclocationraw) de ponto público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="3d4d7-187">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="3d4d7-188">HistoryCount</span></span> 

<span data-ttu-id="3d4d7-189">O HistoryCount do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-190">Public uint [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="3d4d7-191">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-192">InputData</span><span class="sxs-lookup"><span data-stu-id="3d4d7-192">InputData</span></span> 

<span data-ttu-id="3d4d7-193">O InputData do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-194">public int [InputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="3d4d7-195">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-196">Estado da subsessão</span><span class="sxs-lookup"><span data-stu-id="3d4d7-196">KeyStates</span></span> 

<span data-ttu-id="3d4d7-197">O estado do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-198">[Estados](#keystates) uint públicos</span><span class="sxs-lookup"><span data-stu-id="3d4d7-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="3d4d7-199">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="3d4d7-200">PenFlags</span></span> 

<span data-ttu-id="3d4d7-201">O PenFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-202">Public uint [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="3d4d7-203">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="3d4d7-204">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="3d4d7-205">PenMask</span></span> 

<span data-ttu-id="3d4d7-206">O PenMask do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-207">Public uint [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="3d4d7-208">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="3d4d7-209">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="3d4d7-210">PenPressure</span></span> 

<span data-ttu-id="3d4d7-211">O PenPressure do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-212">Public uint [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="3d4d7-213">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="3d4d7-214">PenRotation</span></span> 

<span data-ttu-id="3d4d7-215">O PenRotation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-216">Public uint [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="3d4d7-217">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="3d4d7-218">PenTiltX</span></span> 

<span data-ttu-id="3d4d7-219">O PenTiltX do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-220">public int [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="3d4d7-221">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="3d4d7-222">PenTiltY</span></span> 

<span data-ttu-id="3d4d7-223">O PenTiltY do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-224">public int [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="3d4d7-225">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="3d4d7-226">PerformanceCount</span></span> 

<span data-ttu-id="3d4d7-227">O PerformanceCount do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-228">[PerformanceCountdor](#performancecount) ULONG público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="3d4d7-229">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="3d4d7-230">PixelLocation</span></span> 

<span data-ttu-id="3d4d7-231">O PixelLocation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-232">[PixelLocation](#pixellocation) de ponto público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="3d4d7-233">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="3d4d7-234">PixelLocationRaw</span></span> 

<span data-ttu-id="3d4d7-235">O PixelLocationRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-236">[PixelLocationRaw](#pixellocationraw) de ponto público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="3d4d7-237">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="3d4d7-238">PointerDeviceRect</span></span> 

<span data-ttu-id="3d4d7-239">O PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="3d4d7-240">[PointerDeviceRect](#pointerdevicerect) de retângulo público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-240">public Rectangle [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="3d4d7-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="3d4d7-241">PointerFlags</span></span> 

<span data-ttu-id="3d4d7-242">O PointerFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-243">Public uint [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="3d4d7-244">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="3d4d7-245">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-246">Ponteiroid</span><span class="sxs-lookup"><span data-stu-id="3d4d7-246">PointerId</span></span> 

<span data-ttu-id="3d4d7-247">O Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-248">Ponteiro de [ponteiro](#pointerid) uint público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="3d4d7-249">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="3d4d7-250">PointerKind</span></span> 

<span data-ttu-id="3d4d7-251">O PointerKind do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-252">Public uint [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="3d4d7-253">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="3d4d7-254">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="3d4d7-255">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="3d4d7-256">Hora</span><span class="sxs-lookup"><span data-stu-id="3d4d7-256">Time</span></span> 

<span data-ttu-id="3d4d7-257">A hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-258">[hora](#time) do uint público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-258">public uint [Time](#time)</span></span>

<span data-ttu-id="3d4d7-259">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="3d4d7-260">TouchContact</span></span> 

<span data-ttu-id="3d4d7-261">O TouchContact do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-262">[TouchContact](#touchcontact) de retângulo público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-262">public Rectangle [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="3d4d7-263">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="3d4d7-264">TouchContactRaw</span></span> 

<span data-ttu-id="3d4d7-265">O TouchContactRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-266">[TouchContactRaw](#touchcontactraw) de retângulo público</span><span class="sxs-lookup"><span data-stu-id="3d4d7-266">public Rectangle [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="3d4d7-267">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="3d4d7-268">TouchFlags</span></span> 

<span data-ttu-id="3d4d7-269">O TouchFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-270">Public uint [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="3d4d7-271">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="3d4d7-272">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="3d4d7-273">TouchMask</span></span> 

<span data-ttu-id="3d4d7-274">O TouchMask do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-275">Public uint [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="3d4d7-276">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="3d4d7-277">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="3d4d7-278">TouchOrientation</span></span> 

<span data-ttu-id="3d4d7-279">O TouchOrientation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-280">Public uint [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="3d4d7-281">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="3d4d7-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="3d4d7-282">TouchPressure</span></span> 

<span data-ttu-id="3d4d7-283">O TouchPressure do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3d4d7-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="3d4d7-284">Public uint [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="3d4d7-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="3d4d7-285">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="3d4d7-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

