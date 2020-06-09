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
ms.openlocfilehash: ef0546c03e2d2ccc87677125772b1663f2ec6362
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698342"
---
# <span data-ttu-id="82d07-104">interface ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="82d07-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="82d07-105">Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="82d07-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="82d07-106">Isso basicamente representa um objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combinado.</span><span class="sxs-lookup"><span data-stu-id="82d07-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="82d07-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="82d07-107">Summary</span></span>

 <span data-ttu-id="82d07-108">Parte</span><span class="sxs-lookup"><span data-stu-id="82d07-108">Members</span></span>                        | <span data-ttu-id="82d07-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="82d07-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82d07-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="82d07-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="82d07-111">Obtenha o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="82d07-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="82d07-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="82d07-113">Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="82d07-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="82d07-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="82d07-115">Obtenha o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="82d07-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="82d07-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="82d07-117">Obtenha o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="82d07-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="82d07-119">Obtenha o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="82d07-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="82d07-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="82d07-121">Obtenha o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="82d07-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="82d07-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="82d07-123">Obtenha o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="82d07-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="82d07-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="82d07-125">Obtenha os Estados de KeyState do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="82d07-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="82d07-127">Obtenha o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="82d07-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="82d07-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="82d07-129">Obtenha o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="82d07-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="82d07-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="82d07-131">Obtenha o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="82d07-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="82d07-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="82d07-133">Obtenha o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="82d07-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="82d07-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="82d07-135">Obtenha o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="82d07-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="82d07-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="82d07-137">Obtenha o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="82d07-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="82d07-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="82d07-139">Obtenha o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="82d07-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="82d07-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="82d07-141">Obtenha o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="82d07-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="82d07-143">Obtenha o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="82d07-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="82d07-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="82d07-145">Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="82d07-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="82d07-147">Obtenha o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="82d07-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="82d07-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="82d07-149">Obtenha o Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="82d07-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="82d07-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="82d07-151">Obtenha o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="82d07-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="82d07-152">get_Time</span></span>](#get_time) | <span data-ttu-id="82d07-153">Obtenha a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="82d07-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="82d07-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="82d07-155">Obtenha o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="82d07-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="82d07-157">Obtenha o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="82d07-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="82d07-159">Obtenha o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="82d07-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="82d07-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="82d07-161">Obtenha o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="82d07-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="82d07-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="82d07-163">Obtenha o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="82d07-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="82d07-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="82d07-165">Obtenha o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="82d07-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="82d07-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="82d07-167">Defina o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="82d07-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="82d07-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="82d07-169">Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="82d07-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="82d07-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="82d07-171">Defina o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="82d07-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="82d07-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="82d07-173">Defina o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="82d07-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="82d07-175">Defina o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="82d07-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="82d07-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="82d07-177">Defina o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="82d07-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="82d07-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="82d07-179">Defina o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="82d07-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="82d07-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="82d07-181">Defina os Estados de um evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="82d07-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="82d07-183">Defina o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="82d07-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="82d07-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="82d07-185">Defina o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="82d07-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="82d07-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="82d07-187">Defina o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="82d07-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="82d07-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="82d07-189">Defina o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="82d07-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="82d07-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="82d07-191">Defina o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="82d07-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="82d07-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="82d07-193">Defina o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="82d07-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="82d07-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="82d07-195">Defina o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="82d07-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="82d07-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="82d07-197">Defina o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="82d07-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="82d07-199">Defina o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="82d07-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="82d07-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="82d07-201">Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="82d07-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="82d07-203">Defina o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="82d07-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="82d07-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="82d07-205">Defina a barra de ponteiros do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="82d07-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="82d07-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="82d07-207">Defina o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="82d07-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="82d07-208">put_Time</span></span>](#put_time) | <span data-ttu-id="82d07-209">Defina a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="82d07-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="82d07-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="82d07-211">Defina o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="82d07-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="82d07-213">Defina o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="82d07-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="82d07-215">Defina o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="82d07-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="82d07-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="82d07-217">Defina o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="82d07-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="82d07-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="82d07-219">Defina o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="82d07-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="82d07-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="82d07-221">Defina o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="82d07-222">Ele recebe campos de todos os três e exclui alguns tipos de dados específicos do Win32, como HWND e HANDLE.</span><span class="sxs-lookup"><span data-stu-id="82d07-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="82d07-223">Observe que sourceDevice é retirado, mas esperamos que o PointerDeviceRect e o DisplayRect cubram os casos de uso existentes do sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="82d07-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="82d07-224">Outra grande diferença é que qualquer um dos locais ponto ou RECT deve estar nas coordenadas físicas da WebView.</span><span class="sxs-lookup"><span data-stu-id="82d07-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="82d07-225">Ou seja, as coordenadas relativas ao WebView e ao ajuste de DPI aplicado.</span><span class="sxs-lookup"><span data-stu-id="82d07-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="82d07-226">Parte</span><span class="sxs-lookup"><span data-stu-id="82d07-226">Members</span></span>

#### <span data-ttu-id="82d07-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="82d07-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="82d07-228">Obtenha o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="82d07-229">Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="82d07-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="82d07-230">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="82d07-231">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="82d07-232">get_DisplayRect</span></span> 

<span data-ttu-id="82d07-233">Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="82d07-234">Public HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="82d07-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="82d07-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="82d07-235">get_FrameId</span></span> 

<span data-ttu-id="82d07-236">Obtenha o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="82d07-237">[get_FrameId](#get_frameid)público HRESULT (UINT32 \* frameid)</span><span class="sxs-lookup"><span data-stu-id="82d07-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="82d07-238">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="82d07-239">get_HimetricLocation</span></span> 

<span data-ttu-id="82d07-240">Obtenha o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="82d07-241">público HRESULT [get_HimetricLocation](#get_himetriclocation)(ponto \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="82d07-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="82d07-242">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="82d07-244">Obtenha o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="82d07-245">público HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(ponto \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="82d07-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="82d07-246">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="82d07-247">get_HistoryCount</span></span> 

<span data-ttu-id="82d07-248">Obtenha o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="82d07-249">público HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="82d07-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="82d07-250">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="82d07-251">get_InputData</span></span> 

<span data-ttu-id="82d07-252">Obtenha o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="82d07-253">Public HRESULT [get_InputData](#get_inputdata)(INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="82d07-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="82d07-254">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="82d07-255">get_KeyStates</span></span> 

<span data-ttu-id="82d07-256">Obtenha os Estados de KeyState do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="82d07-257">público HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="82d07-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="82d07-258">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-259">get_PenFlags</span></span> 

<span data-ttu-id="82d07-260">Obtenha o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="82d07-261">público HRESULT [get_PenFlags](#get_penflags)(UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="82d07-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="82d07-262">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="82d07-263">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="82d07-264">get_PenMask</span></span> 

<span data-ttu-id="82d07-265">Obtenha o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="82d07-266">público HRESULT [get_PenMask](#get_penmask)(UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="82d07-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="82d07-267">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="82d07-268">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="82d07-269">get_PenPressure</span></span> 

<span data-ttu-id="82d07-270">Obtenha o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="82d07-271">público HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="82d07-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="82d07-272">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="82d07-273">get_PenRotation</span></span> 

<span data-ttu-id="82d07-274">Obtenha o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="82d07-275">público HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="82d07-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="82d07-276">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="82d07-277">get_PenTiltX</span></span> 

<span data-ttu-id="82d07-278">Obtenha o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="82d07-279">Public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="82d07-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="82d07-280">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="82d07-281">get_PenTiltY</span></span> 

<span data-ttu-id="82d07-282">Obtenha o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="82d07-283">Public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="82d07-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="82d07-284">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="82d07-285">get_PerformanceCount</span></span> 

<span data-ttu-id="82d07-286">Obtenha o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="82d07-287">público HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="82d07-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="82d07-288">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="82d07-289">get_PixelLocation</span></span> 

<span data-ttu-id="82d07-290">Obtenha o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="82d07-291">público HRESULT [get_PixelLocation](#get_pixellocation)(ponto \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="82d07-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="82d07-292">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="82d07-294">Obtenha o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="82d07-295">público HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(ponto \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="82d07-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="82d07-296">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="82d07-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="82d07-298">Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="82d07-299">Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="82d07-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="82d07-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-300">get_PointerFlags</span></span> 

<span data-ttu-id="82d07-301">Obtenha o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="82d07-302">público HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="82d07-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="82d07-303">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="82d07-304">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="82d07-305">get_PointerId</span></span> 

<span data-ttu-id="82d07-306">Obtenha o Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="82d07-307">[get_PointerId](#get_pointerid)público HRESULT (UINT32 \* pointerid)</span><span class="sxs-lookup"><span data-stu-id="82d07-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="82d07-308">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="82d07-309">get_PointerKind</span></span> 

<span data-ttu-id="82d07-310">Obtenha o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="82d07-311">Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="82d07-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="82d07-312">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="82d07-313">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="82d07-314">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="82d07-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="82d07-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="82d07-315">get_Time</span></span> 

<span data-ttu-id="82d07-316">Obtenha a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="82d07-317">[get_Time](#get_time)público HRESULT (DWORD \* time)</span><span class="sxs-lookup"><span data-stu-id="82d07-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="82d07-318">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="82d07-319">get_TouchContact</span></span> 

<span data-ttu-id="82d07-320">Obtenha o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="82d07-321">Public HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="82d07-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="82d07-322">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="82d07-324">Obtenha o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="82d07-325">Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="82d07-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="82d07-326">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-327">get_TouchFlags</span></span> 

<span data-ttu-id="82d07-328">Obtenha o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="82d07-329">público HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="82d07-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="82d07-330">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="82d07-331">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="82d07-332">get_TouchMask</span></span> 

<span data-ttu-id="82d07-333">Obtenha o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="82d07-334">público HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="82d07-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="82d07-335">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="82d07-336">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="82d07-337">get_TouchOrientation</span></span> 

<span data-ttu-id="82d07-338">Obtenha o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="82d07-339">público HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="82d07-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="82d07-340">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="82d07-341">get_TouchPressure</span></span> 

<span data-ttu-id="82d07-342">Obtenha o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="82d07-343">público HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="82d07-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="82d07-344">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="82d07-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="82d07-346">Defina o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="82d07-347">[put_ButtonChangeKind](#put_buttonchangekind)público HRESULT (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="82d07-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="82d07-348">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="82d07-349">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="82d07-350">put_DisplayRect</span></span> 

<span data-ttu-id="82d07-351">Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="82d07-352">Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="82d07-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="82d07-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="82d07-353">put_FrameId</span></span> 

<span data-ttu-id="82d07-354">Defina o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="82d07-355">[put_FrameId](#put_frameid)público HRESULT (UINT32 frameid)</span><span class="sxs-lookup"><span data-stu-id="82d07-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="82d07-356">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="82d07-357">put_HimetricLocation</span></span> 

<span data-ttu-id="82d07-358">Defina o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="82d07-359">público HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="82d07-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="82d07-360">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="82d07-362">Defina o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="82d07-363">público HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="82d07-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="82d07-364">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="82d07-365">put_HistoryCount</span></span> 

<span data-ttu-id="82d07-366">Defina o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="82d07-367">público HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="82d07-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="82d07-368">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="82d07-369">put_InputData</span></span> 

<span data-ttu-id="82d07-370">Defina o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="82d07-371">[put_InputData](#put_inputdata)público HRESULT (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="82d07-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="82d07-372">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="82d07-373">put_KeyStates</span></span> 

<span data-ttu-id="82d07-374">Defina os Estados de um evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="82d07-375">público HRESULT [put_KeyStates](#put_keystates)(estado DWORD DWORD)</span><span class="sxs-lookup"><span data-stu-id="82d07-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="82d07-376">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-377">put_PenFlags</span></span> 

<span data-ttu-id="82d07-378">Defina o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="82d07-379">público HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="82d07-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="82d07-380">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="82d07-381">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="82d07-382">put_PenMask</span></span> 

<span data-ttu-id="82d07-383">Defina o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="82d07-384">público HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="82d07-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="82d07-385">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="82d07-386">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="82d07-387">put_PenPressure</span></span> 

<span data-ttu-id="82d07-388">Defina o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="82d07-389">público HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="82d07-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="82d07-390">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="82d07-391">put_PenRotation</span></span> 

<span data-ttu-id="82d07-392">Defina o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="82d07-393">público HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="82d07-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="82d07-394">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="82d07-395">put_PenTiltX</span></span> 

<span data-ttu-id="82d07-396">Defina o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="82d07-397">[put_PenTiltX](#put_pentiltx)público HRESULT (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="82d07-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="82d07-398">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="82d07-399">put_PenTiltY</span></span> 

<span data-ttu-id="82d07-400">Defina o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="82d07-401">[put_PenTiltY](#put_pentilty)público HRESULT (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="82d07-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="82d07-402">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="82d07-403">put_PerformanceCount</span></span> 

<span data-ttu-id="82d07-404">Defina o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="82d07-405">público HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="82d07-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="82d07-406">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="82d07-407">put_PixelLocation</span></span> 

<span data-ttu-id="82d07-408">Defina o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="82d07-409">público HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="82d07-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="82d07-410">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="82d07-412">Defina o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="82d07-413">público HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="82d07-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="82d07-414">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="82d07-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="82d07-416">Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="82d07-417">Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="82d07-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="82d07-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-418">put_PointerFlags</span></span> 

<span data-ttu-id="82d07-419">Defina o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="82d07-420">público HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="82d07-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="82d07-421">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="82d07-422">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="82d07-423">put_PointerId</span></span> 

<span data-ttu-id="82d07-424">Defina a barra de ponteiros do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="82d07-425">[put_PointerId](#put_pointerid)público HRESULT (ponteiroid UINT32)</span><span class="sxs-lookup"><span data-stu-id="82d07-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="82d07-426">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="82d07-427">put_PointerKind</span></span> 

<span data-ttu-id="82d07-428">Defina o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="82d07-429">público HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="82d07-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="82d07-430">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="82d07-431">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="82d07-432">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="82d07-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="82d07-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="82d07-433">put_Time</span></span> 

<span data-ttu-id="82d07-434">Defina a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="82d07-435">[put_Time](#put_time)público HRESULT (tempo DWORD)</span><span class="sxs-lookup"><span data-stu-id="82d07-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="82d07-436">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="82d07-437">put_TouchContact</span></span> 

<span data-ttu-id="82d07-438">Defina o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="82d07-439">Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="82d07-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="82d07-440">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="82d07-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="82d07-442">Defina o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="82d07-443">Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="82d07-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="82d07-444">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="82d07-445">put_TouchFlags</span></span> 

<span data-ttu-id="82d07-446">Defina o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="82d07-447">público HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="82d07-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="82d07-448">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="82d07-449">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="82d07-450">put_TouchMask</span></span> 

<span data-ttu-id="82d07-451">Defina o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="82d07-452">público HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="82d07-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="82d07-453">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="82d07-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="82d07-454">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="82d07-455">put_TouchOrientation</span></span> 

<span data-ttu-id="82d07-456">Defina o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="82d07-457">público HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="82d07-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="82d07-458">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="82d07-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="82d07-459">put_TouchPressure</span></span> 

<span data-ttu-id="82d07-460">Defina o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="82d07-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="82d07-461">público HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="82d07-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="82d07-462">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="82d07-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

