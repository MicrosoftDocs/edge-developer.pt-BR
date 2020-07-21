---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 8c0ed40c61344fe0a3177fd36d5629953f8801d7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885477"
---
# <span data-ttu-id="361fe-104">0.9.515-ICoreWebView2ExperimentalPointerInfo de interface</span><span class="sxs-lookup"><span data-stu-id="361fe-104">0.9.515 - interface ICoreWebView2ExperimentalPointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="361fe-105">Isso basicamente representa um objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combinado.</span><span class="sxs-lookup"><span data-stu-id="361fe-105">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="361fe-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="361fe-106">Summary</span></span>

 <span data-ttu-id="361fe-107">Parte</span><span class="sxs-lookup"><span data-stu-id="361fe-107">Members</span></span>                        | <span data-ttu-id="361fe-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="361fe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="361fe-109">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="361fe-109">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="361fe-110">Obtenha o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-110">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="361fe-111">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="361fe-111">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="361fe-112">Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-112">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="361fe-113">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="361fe-113">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="361fe-114">Obtenha o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-114">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="361fe-115">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="361fe-115">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="361fe-116">Obtenha o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-116">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="361fe-117">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-117">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="361fe-118">Obtenha o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-118">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="361fe-119">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="361fe-119">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="361fe-120">Obtenha o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-120">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="361fe-121">get_InputData</span><span class="sxs-lookup"><span data-stu-id="361fe-121">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="361fe-122">Obtenha o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-122">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="361fe-123">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="361fe-123">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="361fe-124">Obtenha os Estados de KeyState do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-124">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="361fe-125">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-125">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="361fe-126">Obtenha o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-126">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="361fe-127">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="361fe-127">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="361fe-128">Obtenha o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-128">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="361fe-129">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="361fe-129">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="361fe-130">Obtenha o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-130">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="361fe-131">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="361fe-131">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="361fe-132">Obtenha o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-132">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="361fe-133">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="361fe-133">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="361fe-134">Obtenha o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-134">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="361fe-135">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="361fe-135">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="361fe-136">Obtenha o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-136">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="361fe-137">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="361fe-137">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="361fe-138">Obtenha o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-138">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="361fe-139">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="361fe-139">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="361fe-140">Obtenha o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-140">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="361fe-141">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-141">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="361fe-142">Obtenha o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-142">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="361fe-143">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="361fe-143">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="361fe-144">Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-144">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="361fe-145">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-145">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="361fe-146">Obtenha o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-146">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="361fe-147">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="361fe-147">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="361fe-148">Obtenha o Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-148">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="361fe-149">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="361fe-149">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="361fe-150">Obtenha o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-150">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="361fe-151">get_Time</span><span class="sxs-lookup"><span data-stu-id="361fe-151">get_Time</span></span>](#get_time) | <span data-ttu-id="361fe-152">Obtenha a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-152">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="361fe-153">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="361fe-153">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="361fe-154">Obtenha o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-154">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="361fe-155">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-155">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="361fe-156">Obtenha o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-156">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="361fe-157">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-157">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="361fe-158">Obtenha o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-158">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="361fe-159">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="361fe-159">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="361fe-160">Obtenha o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-160">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="361fe-161">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="361fe-161">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="361fe-162">Obtenha o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-162">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="361fe-163">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="361fe-163">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="361fe-164">Obtenha o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-164">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="361fe-165">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="361fe-165">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="361fe-166">Defina o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-166">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="361fe-167">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="361fe-167">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="361fe-168">Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-168">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="361fe-169">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="361fe-169">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="361fe-170">Defina o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-170">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="361fe-171">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="361fe-171">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="361fe-172">Defina o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-172">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="361fe-173">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-173">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="361fe-174">Defina o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-174">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="361fe-175">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="361fe-175">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="361fe-176">Defina o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-176">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="361fe-177">put_InputData</span><span class="sxs-lookup"><span data-stu-id="361fe-177">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="361fe-178">Defina o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-178">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="361fe-179">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="361fe-179">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="361fe-180">Defina os Estados de um evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-180">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="361fe-181">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-181">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="361fe-182">Defina o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-182">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="361fe-183">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="361fe-183">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="361fe-184">Defina o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-184">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="361fe-185">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="361fe-185">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="361fe-186">Defina o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-186">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="361fe-187">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="361fe-187">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="361fe-188">Defina o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-188">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="361fe-189">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="361fe-189">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="361fe-190">Defina o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-190">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="361fe-191">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="361fe-191">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="361fe-192">Defina o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-192">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="361fe-193">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="361fe-193">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="361fe-194">Defina o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-194">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="361fe-195">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="361fe-195">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="361fe-196">Defina o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-196">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="361fe-197">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-197">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="361fe-198">Defina o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-198">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="361fe-199">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="361fe-199">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="361fe-200">Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-200">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="361fe-201">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-201">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="361fe-202">Defina o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-202">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="361fe-203">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="361fe-203">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="361fe-204">Defina a barra de ponteiros do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-204">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="361fe-205">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="361fe-205">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="361fe-206">Defina o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-206">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="361fe-207">put_Time</span><span class="sxs-lookup"><span data-stu-id="361fe-207">put_Time</span></span>](#put_time) | <span data-ttu-id="361fe-208">Defina a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-208">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="361fe-209">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="361fe-209">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="361fe-210">Defina o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-210">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="361fe-211">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-211">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="361fe-212">Defina o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-212">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="361fe-213">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-213">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="361fe-214">Defina o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-214">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="361fe-215">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="361fe-215">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="361fe-216">Defina o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-216">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="361fe-217">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="361fe-217">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="361fe-218">Defina o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-218">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="361fe-219">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="361fe-219">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="361fe-220">Defina o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-220">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="361fe-221">Ele recebe campos de todos os três e exclui alguns tipos de dados específicos do Win32, como HWND e HANDLE.</span><span class="sxs-lookup"><span data-stu-id="361fe-221">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="361fe-222">Observe que sourceDevice é retirado, mas esperamos que o PointerDeviceRect e o DisplayRect cubram os casos de uso existentes do sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="361fe-222">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="361fe-223">Outra grande diferença é que qualquer um dos locais ponto ou RECT deve estar nas coordenadas físicas da WebView.</span><span class="sxs-lookup"><span data-stu-id="361fe-223">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="361fe-224">Ou seja, as coordenadas relativas ao WebView e ao ajuste de DPI aplicado.</span><span class="sxs-lookup"><span data-stu-id="361fe-224">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="361fe-225">Parte</span><span class="sxs-lookup"><span data-stu-id="361fe-225">Members</span></span>

#### <span data-ttu-id="361fe-226">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="361fe-226">get_ButtonChangeKind</span></span> 

<span data-ttu-id="361fe-227">Obtenha o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-227">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="361fe-228">Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="361fe-228">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="361fe-229">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-229">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="361fe-230">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-230">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-231">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="361fe-231">get_DisplayRect</span></span> 

<span data-ttu-id="361fe-232">Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-232">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="361fe-233">Public HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="361fe-233">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="361fe-234">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="361fe-234">get_FrameId</span></span> 

<span data-ttu-id="361fe-235">Obtenha o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-235">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="361fe-236">[get_FrameId](#get_frameid)público HRESULT (UINT32 \* frameid)</span><span class="sxs-lookup"><span data-stu-id="361fe-236">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="361fe-237">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-237">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-238">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="361fe-238">get_HimetricLocation</span></span> 

<span data-ttu-id="361fe-239">Obtenha o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-239">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="361fe-240">público HRESULT [get_HimetricLocation](#get_himetriclocation)(ponto \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="361fe-240">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="361fe-241">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-241">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-242">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-242">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="361fe-243">Obtenha o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-243">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="361fe-244">público HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(ponto \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="361fe-244">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="361fe-245">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-245">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-246">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="361fe-246">get_HistoryCount</span></span> 

<span data-ttu-id="361fe-247">Obtenha o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-247">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="361fe-248">público HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="361fe-248">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="361fe-249">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-249">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-250">get_InputData</span><span class="sxs-lookup"><span data-stu-id="361fe-250">get_InputData</span></span> 

<span data-ttu-id="361fe-251">Obtenha o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-251">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="361fe-252">Public HRESULT [get_InputData](#get_inputdata)(INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="361fe-252">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="361fe-253">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-253">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-254">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="361fe-254">get_KeyStates</span></span> 

<span data-ttu-id="361fe-255">Obtenha os Estados de KeyState do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-255">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="361fe-256">público HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="361fe-256">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="361fe-257">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-257">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-258">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-258">get_PenFlags</span></span> 

<span data-ttu-id="361fe-259">Obtenha o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-259">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="361fe-260">público HRESULT [get_PenFlags](#get_penflags)(UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="361fe-260">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="361fe-261">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-261">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="361fe-262">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-262">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-263">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="361fe-263">get_PenMask</span></span> 

<span data-ttu-id="361fe-264">Obtenha o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-264">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="361fe-265">público HRESULT [get_PenMask](#get_penmask)(UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="361fe-265">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="361fe-266">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-266">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="361fe-267">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-267">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-268">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="361fe-268">get_PenPressure</span></span> 

<span data-ttu-id="361fe-269">Obtenha o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-269">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="361fe-270">público HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="361fe-270">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="361fe-271">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-271">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-272">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="361fe-272">get_PenRotation</span></span> 

<span data-ttu-id="361fe-273">Obtenha o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-273">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="361fe-274">público HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="361fe-274">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="361fe-275">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-275">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-276">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="361fe-276">get_PenTiltX</span></span> 

<span data-ttu-id="361fe-277">Obtenha o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-277">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="361fe-278">Public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="361fe-278">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="361fe-279">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-279">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-280">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="361fe-280">get_PenTiltY</span></span> 

<span data-ttu-id="361fe-281">Obtenha o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-281">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="361fe-282">Public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="361fe-282">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="361fe-283">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-283">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-284">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="361fe-284">get_PerformanceCount</span></span> 

<span data-ttu-id="361fe-285">Obtenha o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-285">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="361fe-286">público HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="361fe-286">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="361fe-287">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-287">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-288">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="361fe-288">get_PixelLocation</span></span> 

<span data-ttu-id="361fe-289">Obtenha o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-289">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="361fe-290">público HRESULT [get_PixelLocation](#get_pixellocation)(ponto \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="361fe-290">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="361fe-291">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-291">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-292">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-292">get_PixelLocationRaw</span></span> 

<span data-ttu-id="361fe-293">Obtenha o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-293">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="361fe-294">público HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(ponto \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="361fe-294">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="361fe-295">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-295">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-296">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="361fe-296">get_PointerDeviceRect</span></span> 

<span data-ttu-id="361fe-297">Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-297">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="361fe-298">Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="361fe-298">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="361fe-299">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-299">get_PointerFlags</span></span> 

<span data-ttu-id="361fe-300">Obtenha o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-300">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="361fe-301">público HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="361fe-301">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="361fe-302">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-302">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="361fe-303">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-303">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-304">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="361fe-304">get_PointerId</span></span> 

<span data-ttu-id="361fe-305">Obtenha o Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-305">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="361fe-306">[get_PointerId](#get_pointerid)público HRESULT (UINT32 \* pointerid)</span><span class="sxs-lookup"><span data-stu-id="361fe-306">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="361fe-307">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-307">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-308">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="361fe-308">get_PointerKind</span></span> 

<span data-ttu-id="361fe-309">Obtenha o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-309">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="361fe-310">Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="361fe-310">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="361fe-311">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-311">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="361fe-312">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-312">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="361fe-313">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="361fe-313">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="361fe-314">get_Time</span><span class="sxs-lookup"><span data-stu-id="361fe-314">get_Time</span></span> 

<span data-ttu-id="361fe-315">Obtenha a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-315">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="361fe-316">[get_Time](#get_time)público HRESULT (DWORD \* time)</span><span class="sxs-lookup"><span data-stu-id="361fe-316">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="361fe-317">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-317">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-318">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="361fe-318">get_TouchContact</span></span> 

<span data-ttu-id="361fe-319">Obtenha o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-319">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="361fe-320">Public HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="361fe-320">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="361fe-321">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-321">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-322">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-322">get_TouchContactRaw</span></span> 

<span data-ttu-id="361fe-323">Obtenha o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-323">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="361fe-324">Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="361fe-324">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="361fe-325">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-325">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-326">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-326">get_TouchFlags</span></span> 

<span data-ttu-id="361fe-327">Obtenha o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-327">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="361fe-328">público HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="361fe-328">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="361fe-329">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-329">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="361fe-330">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-330">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-331">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="361fe-331">get_TouchMask</span></span> 

<span data-ttu-id="361fe-332">Obtenha o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-332">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="361fe-333">público HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="361fe-333">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="361fe-334">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-334">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="361fe-335">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-335">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-336">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="361fe-336">get_TouchOrientation</span></span> 

<span data-ttu-id="361fe-337">Obtenha o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-337">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="361fe-338">público HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="361fe-338">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="361fe-339">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-339">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-340">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="361fe-340">get_TouchPressure</span></span> 

<span data-ttu-id="361fe-341">Obtenha o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-341">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="361fe-342">público HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="361fe-342">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="361fe-343">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-343">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-344">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="361fe-344">put_ButtonChangeKind</span></span> 

<span data-ttu-id="361fe-345">Defina o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-345">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="361fe-346">[put_ButtonChangeKind](#put_buttonchangekind)público HRESULT (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="361fe-346">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="361fe-347">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-347">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="361fe-348">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-348">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-349">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="361fe-349">put_DisplayRect</span></span> 

<span data-ttu-id="361fe-350">Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-350">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="361fe-351">Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="361fe-351">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="361fe-352">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="361fe-352">put_FrameId</span></span> 

<span data-ttu-id="361fe-353">Defina o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-353">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="361fe-354">[put_FrameId](#put_frameid)público HRESULT (UINT32 frameid)</span><span class="sxs-lookup"><span data-stu-id="361fe-354">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="361fe-355">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-355">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-356">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="361fe-356">put_HimetricLocation</span></span> 

<span data-ttu-id="361fe-357">Defina o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-357">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="361fe-358">público HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="361fe-358">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="361fe-359">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-359">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-360">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-360">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="361fe-361">Defina o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-361">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="361fe-362">público HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="361fe-362">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="361fe-363">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-363">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-364">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="361fe-364">put_HistoryCount</span></span> 

<span data-ttu-id="361fe-365">Defina o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-365">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="361fe-366">público HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="361fe-366">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="361fe-367">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-367">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-368">put_InputData</span><span class="sxs-lookup"><span data-stu-id="361fe-368">put_InputData</span></span> 

<span data-ttu-id="361fe-369">Defina o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-369">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="361fe-370">[put_InputData](#put_inputdata)público HRESULT (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="361fe-370">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="361fe-371">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-371">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-372">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="361fe-372">put_KeyStates</span></span> 

<span data-ttu-id="361fe-373">Defina os Estados de um evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-373">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="361fe-374">público HRESULT [put_KeyStates](#put_keystates)(estado DWORD DWORD)</span><span class="sxs-lookup"><span data-stu-id="361fe-374">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="361fe-375">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-375">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-376">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-376">put_PenFlags</span></span> 

<span data-ttu-id="361fe-377">Defina o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-377">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="361fe-378">público HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="361fe-378">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="361fe-379">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-379">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="361fe-380">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-380">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-381">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="361fe-381">put_PenMask</span></span> 

<span data-ttu-id="361fe-382">Defina o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-382">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="361fe-383">público HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="361fe-383">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="361fe-384">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-384">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="361fe-385">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-385">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-386">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="361fe-386">put_PenPressure</span></span> 

<span data-ttu-id="361fe-387">Defina o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-387">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="361fe-388">público HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="361fe-388">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="361fe-389">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-389">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-390">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="361fe-390">put_PenRotation</span></span> 

<span data-ttu-id="361fe-391">Defina o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-391">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="361fe-392">público HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="361fe-392">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="361fe-393">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-393">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-394">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="361fe-394">put_PenTiltX</span></span> 

<span data-ttu-id="361fe-395">Defina o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-395">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="361fe-396">[put_PenTiltX](#put_pentiltx)público HRESULT (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="361fe-396">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="361fe-397">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-397">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-398">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="361fe-398">put_PenTiltY</span></span> 

<span data-ttu-id="361fe-399">Defina o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-399">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="361fe-400">[put_PenTiltY](#put_pentilty)público HRESULT (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="361fe-400">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="361fe-401">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-401">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-402">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="361fe-402">put_PerformanceCount</span></span> 

<span data-ttu-id="361fe-403">Defina o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-403">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="361fe-404">público HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="361fe-404">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="361fe-405">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-405">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-406">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="361fe-406">put_PixelLocation</span></span> 

<span data-ttu-id="361fe-407">Defina o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-407">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="361fe-408">público HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="361fe-408">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="361fe-409">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-409">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-410">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-410">put_PixelLocationRaw</span></span> 

<span data-ttu-id="361fe-411">Defina o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-411">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="361fe-412">público HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="361fe-412">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="361fe-413">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-413">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-414">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="361fe-414">put_PointerDeviceRect</span></span> 

<span data-ttu-id="361fe-415">Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-415">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="361fe-416">Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="361fe-416">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="361fe-417">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-417">put_PointerFlags</span></span> 

<span data-ttu-id="361fe-418">Defina o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-418">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="361fe-419">público HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="361fe-419">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="361fe-420">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-420">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="361fe-421">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-421">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-422">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="361fe-422">put_PointerId</span></span> 

<span data-ttu-id="361fe-423">Defina a barra de ponteiros do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-423">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="361fe-424">[put_PointerId](#put_pointerid)público HRESULT (ponteiroid UINT32)</span><span class="sxs-lookup"><span data-stu-id="361fe-424">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="361fe-425">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-425">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-426">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="361fe-426">put_PointerKind</span></span> 

<span data-ttu-id="361fe-427">Defina o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-427">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="361fe-428">público HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="361fe-428">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="361fe-429">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-429">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="361fe-430">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-430">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="361fe-431">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="361fe-431">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="361fe-432">put_Time</span><span class="sxs-lookup"><span data-stu-id="361fe-432">put_Time</span></span> 

<span data-ttu-id="361fe-433">Defina a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-433">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="361fe-434">[put_Time](#put_time)público HRESULT (tempo DWORD)</span><span class="sxs-lookup"><span data-stu-id="361fe-434">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="361fe-435">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-435">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-436">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="361fe-436">put_TouchContact</span></span> 

<span data-ttu-id="361fe-437">Defina o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-437">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="361fe-438">Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="361fe-438">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="361fe-439">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-439">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-440">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="361fe-440">put_TouchContactRaw</span></span> 

<span data-ttu-id="361fe-441">Defina o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-441">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="361fe-442">Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="361fe-442">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="361fe-443">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-443">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-444">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="361fe-444">put_TouchFlags</span></span> 

<span data-ttu-id="361fe-445">Defina o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-445">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="361fe-446">público HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="361fe-446">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="361fe-447">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-447">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="361fe-448">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-448">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-449">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="361fe-449">put_TouchMask</span></span> 

<span data-ttu-id="361fe-450">Defina o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-450">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="361fe-451">público HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="361fe-451">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="361fe-452">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="361fe-452">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="361fe-453">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-453">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-454">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="361fe-454">put_TouchOrientation</span></span> 

<span data-ttu-id="361fe-455">Defina o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-455">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="361fe-456">público HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="361fe-456">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="361fe-457">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-457">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="361fe-458">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="361fe-458">put_TouchPressure</span></span> 

<span data-ttu-id="361fe-459">Defina o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="361fe-459">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="361fe-460">público HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="361fe-460">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="361fe-461">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="361fe-461">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

