---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 8a5e5f4188b5115e1c6b836f80aad69c4bf2da7e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878754"
---
# <span data-ttu-id="28dd9-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="28dd9-104">Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

<span data-ttu-id="28dd9-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="28dd9-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="28dd9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="28dd9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="28dd9-107">Isso basicamente representa um objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combinado.</span><span class="sxs-lookup"><span data-stu-id="28dd9-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="28dd9-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="28dd9-108">Summary</span></span>

 <span data-ttu-id="28dd9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="28dd9-109">Members</span></span>                        | <span data-ttu-id="28dd9-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="28dd9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="28dd9-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="28dd9-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="28dd9-112">O ButtonChangeKind do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="28dd9-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="28dd9-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="28dd9-114">O DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="28dd9-115">Frameid</span><span class="sxs-lookup"><span data-stu-id="28dd9-115">FrameId</span></span>](#frameid) | <span data-ttu-id="28dd9-116">O Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="28dd9-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="28dd9-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="28dd9-118">O HimetricLocation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="28dd9-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="28dd9-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="28dd9-120">O HimetricLocationRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="28dd9-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="28dd9-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="28dd9-122">O HistoryCount do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="28dd9-123">InputData</span><span class="sxs-lookup"><span data-stu-id="28dd9-123">InputData</span></span>](#inputdata) | <span data-ttu-id="28dd9-124">O InputData do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="28dd9-125">Estado da subsessão</span><span class="sxs-lookup"><span data-stu-id="28dd9-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="28dd9-126">O estado do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="28dd9-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="28dd9-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="28dd9-128">O PenFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="28dd9-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="28dd9-129">PenMask</span></span>](#penmask) | <span data-ttu-id="28dd9-130">O PenMask do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="28dd9-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="28dd9-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="28dd9-132">O PenPressure do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="28dd9-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="28dd9-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="28dd9-134">O PenRotation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="28dd9-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="28dd9-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="28dd9-136">O PenTiltX do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="28dd9-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="28dd9-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="28dd9-138">O PenTiltY do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="28dd9-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="28dd9-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="28dd9-140">O PerformanceCount do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="28dd9-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="28dd9-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="28dd9-142">O PixelLocation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="28dd9-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="28dd9-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="28dd9-144">O PixelLocationRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="28dd9-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="28dd9-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="28dd9-146">O PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="28dd9-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="28dd9-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="28dd9-148">O PointerFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="28dd9-149">Ponteiroid</span><span class="sxs-lookup"><span data-stu-id="28dd9-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="28dd9-150">O Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="28dd9-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="28dd9-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="28dd9-152">O PointerKind do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="28dd9-153">Hora</span><span class="sxs-lookup"><span data-stu-id="28dd9-153">Time</span></span>](#time) | <span data-ttu-id="28dd9-154">A hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="28dd9-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="28dd9-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="28dd9-156">O TouchContact do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="28dd9-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="28dd9-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="28dd9-158">O TouchContactRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="28dd9-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="28dd9-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="28dd9-160">O TouchFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="28dd9-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="28dd9-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="28dd9-162">O TouchMask do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="28dd9-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="28dd9-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="28dd9-164">O TouchOrientation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="28dd9-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="28dd9-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="28dd9-166">O TouchPressure do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="28dd9-167">Parte</span><span class="sxs-lookup"><span data-stu-id="28dd9-167">Members</span></span>

#### <span data-ttu-id="28dd9-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="28dd9-168">ButtonChangeKind</span></span> 

<span data-ttu-id="28dd9-169">O ButtonChangeKind do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="28dd9-170">public int [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="28dd9-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="28dd9-171">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="28dd9-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="28dd9-172">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="28dd9-173">DisplayRect</span></span> 

<span data-ttu-id="28dd9-174">O DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="28dd9-175">Public Rect [DisplayRect](#displayrect)</span><span class="sxs-lookup"><span data-stu-id="28dd9-175">public Rect [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="28dd9-176">Frameid</span><span class="sxs-lookup"><span data-stu-id="28dd9-176">FrameId</span></span> 

<span data-ttu-id="28dd9-177">O Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="28dd9-178">[frameid](#frameid) uint público</span><span class="sxs-lookup"><span data-stu-id="28dd9-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="28dd9-179">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="28dd9-180">HimetricLocation</span></span> 

<span data-ttu-id="28dd9-181">O HimetricLocation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="28dd9-182">[HimetricLocation](#himetriclocation) de ponto público</span><span class="sxs-lookup"><span data-stu-id="28dd9-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="28dd9-183">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="28dd9-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="28dd9-185">O HimetricLocationRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="28dd9-186">[HimetricLocationRaw](#himetriclocationraw) de ponto público</span><span class="sxs-lookup"><span data-stu-id="28dd9-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="28dd9-187">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="28dd9-188">HistoryCount</span></span> 

<span data-ttu-id="28dd9-189">O HistoryCount do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="28dd9-190">Public uint [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="28dd9-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="28dd9-191">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-192">InputData</span><span class="sxs-lookup"><span data-stu-id="28dd9-192">InputData</span></span> 

<span data-ttu-id="28dd9-193">O InputData do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="28dd9-194">public int [InputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="28dd9-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="28dd9-195">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-196">Estado da subsessão</span><span class="sxs-lookup"><span data-stu-id="28dd9-196">KeyStates</span></span> 

<span data-ttu-id="28dd9-197">O estado do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="28dd9-198">[Estados](#keystates) uint públicos</span><span class="sxs-lookup"><span data-stu-id="28dd9-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="28dd9-199">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="28dd9-200">PenFlags</span></span> 

<span data-ttu-id="28dd9-201">O PenFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="28dd9-202">Public uint [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="28dd9-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="28dd9-203">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="28dd9-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="28dd9-204">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="28dd9-205">PenMask</span></span> 

<span data-ttu-id="28dd9-206">O PenMask do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="28dd9-207">Public uint [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="28dd9-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="28dd9-208">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="28dd9-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="28dd9-209">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="28dd9-210">PenPressure</span></span> 

<span data-ttu-id="28dd9-211">O PenPressure do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="28dd9-212">Public uint [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="28dd9-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="28dd9-213">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="28dd9-214">PenRotation</span></span> 

<span data-ttu-id="28dd9-215">O PenRotation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="28dd9-216">Public uint [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="28dd9-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="28dd9-217">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="28dd9-218">PenTiltX</span></span> 

<span data-ttu-id="28dd9-219">O PenTiltX do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="28dd9-220">public int [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="28dd9-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="28dd9-221">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="28dd9-222">PenTiltY</span></span> 

<span data-ttu-id="28dd9-223">O PenTiltY do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="28dd9-224">public int [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="28dd9-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="28dd9-225">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="28dd9-226">PerformanceCount</span></span> 

<span data-ttu-id="28dd9-227">O PerformanceCount do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="28dd9-228">[PerformanceCountdor](#performancecount) ULONG público</span><span class="sxs-lookup"><span data-stu-id="28dd9-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="28dd9-229">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="28dd9-230">PixelLocation</span></span> 

<span data-ttu-id="28dd9-231">O PixelLocation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="28dd9-232">[PixelLocation](#pixellocation) de ponto público</span><span class="sxs-lookup"><span data-stu-id="28dd9-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="28dd9-233">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="28dd9-234">PixelLocationRaw</span></span> 

<span data-ttu-id="28dd9-235">O PixelLocationRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="28dd9-236">[PixelLocationRaw](#pixellocationraw) de ponto público</span><span class="sxs-lookup"><span data-stu-id="28dd9-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="28dd9-237">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="28dd9-238">PointerDeviceRect</span></span> 

<span data-ttu-id="28dd9-239">O PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="28dd9-240">Public Rect [PointerDeviceRect](#pointerdevicerect)</span><span class="sxs-lookup"><span data-stu-id="28dd9-240">public Rect [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="28dd9-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="28dd9-241">PointerFlags</span></span> 

<span data-ttu-id="28dd9-242">O PointerFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="28dd9-243">Public uint [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="28dd9-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="28dd9-244">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="28dd9-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="28dd9-245">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-246">Ponteiroid</span><span class="sxs-lookup"><span data-stu-id="28dd9-246">PointerId</span></span> 

<span data-ttu-id="28dd9-247">O Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="28dd9-248">Ponteiro de [ponteiro](#pointerid) uint público</span><span class="sxs-lookup"><span data-stu-id="28dd9-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="28dd9-249">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="28dd9-250">PointerKind</span></span> 

<span data-ttu-id="28dd9-251">O PointerKind do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="28dd9-252">Public uint [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="28dd9-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="28dd9-253">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="28dd9-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="28dd9-254">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="28dd9-255">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="28dd9-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="28dd9-256">Hora</span><span class="sxs-lookup"><span data-stu-id="28dd9-256">Time</span></span> 

<span data-ttu-id="28dd9-257">A hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="28dd9-258">[hora](#time) do uint público</span><span class="sxs-lookup"><span data-stu-id="28dd9-258">public uint [Time](#time)</span></span>

<span data-ttu-id="28dd9-259">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="28dd9-260">TouchContact</span></span> 

<span data-ttu-id="28dd9-261">O TouchContact do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="28dd9-262">Public Rect [TouchContact](#touchcontact)</span><span class="sxs-lookup"><span data-stu-id="28dd9-262">public Rect [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="28dd9-263">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="28dd9-264">TouchContactRaw</span></span> 

<span data-ttu-id="28dd9-265">O TouchContactRaw do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="28dd9-266">Public Rect [TouchContactRaw](#touchcontactraw)</span><span class="sxs-lookup"><span data-stu-id="28dd9-266">public Rect [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="28dd9-267">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="28dd9-268">TouchFlags</span></span> 

<span data-ttu-id="28dd9-269">O TouchFlags do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="28dd9-270">Public uint [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="28dd9-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="28dd9-271">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="28dd9-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="28dd9-272">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="28dd9-273">TouchMask</span></span> 

<span data-ttu-id="28dd9-274">O TouchMask do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="28dd9-275">Public uint [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="28dd9-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="28dd9-276">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="28dd9-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="28dd9-277">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="28dd9-278">TouchOrientation</span></span> 

<span data-ttu-id="28dd9-279">O TouchOrientation do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="28dd9-280">Public uint [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="28dd9-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="28dd9-281">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="28dd9-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="28dd9-282">TouchPressure</span></span> 

<span data-ttu-id="28dd9-283">O TouchPressure do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="28dd9-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="28dd9-284">Public uint [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="28dd9-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="28dd9-285">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="28dd9-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

