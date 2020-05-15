---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2141dff54b44fe6d9a2758f571e61b81877079da
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652579"
---
# <span data-ttu-id="ac9d4-104">interface ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="ac9d4-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="ac9d4-105">Esta é uma API experimental que é fornecida com a versão 0.9.488 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="ac9d4-106">Isso basicamente representa um objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combinado.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="ac9d4-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="ac9d4-107">Summary</span></span>

 <span data-ttu-id="ac9d4-108">Parte</span><span class="sxs-lookup"><span data-stu-id="ac9d4-108">Members</span></span>                        | <span data-ttu-id="ac9d4-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="ac9d4-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac9d4-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ac9d4-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="ac9d4-111">Obtenha o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ac9d4-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="ac9d4-113">Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ac9d4-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="ac9d4-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="ac9d4-115">Obtenha o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="ac9d4-117">Obtenha o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="ac9d4-119">Obtenha o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ac9d4-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="ac9d4-121">Obtenha o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="ac9d4-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="ac9d4-123">Obtenha o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ac9d4-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="ac9d4-125">Obtenha os Estados de KeyState do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="ac9d4-127">Obtenha o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="ac9d4-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="ac9d4-129">Obtenha o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ac9d4-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="ac9d4-131">Obtenha o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="ac9d4-133">Obtenha o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ac9d4-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="ac9d4-135">Obtenha o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ac9d4-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="ac9d4-137">Obtenha o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ac9d4-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="ac9d4-139">Obtenha o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="ac9d4-141">Obtenha o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="ac9d4-143">Obtenha o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ac9d4-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="ac9d4-145">Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ac9d4-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="ac9d4-147">Obtenha o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="ac9d4-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="ac9d4-149">Obtenha o Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ac9d4-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="ac9d4-151">Obtenha o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="ac9d4-152">get_Time</span></span>](#get_time) | <span data-ttu-id="ac9d4-153">Obtenha a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ac9d4-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="ac9d4-155">Obtenha o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="ac9d4-157">Obtenha o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="ac9d4-159">Obtenha o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ac9d4-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="ac9d4-161">Obtenha o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="ac9d4-163">Obtenha o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ac9d4-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="ac9d4-165">Obtenha o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ac9d4-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="ac9d4-167">Defina o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ac9d4-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="ac9d4-169">Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ac9d4-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="ac9d4-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="ac9d4-171">Defina o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="ac9d4-173">Defina o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="ac9d4-175">Defina o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ac9d4-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="ac9d4-177">Defina o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="ac9d4-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="ac9d4-179">Defina o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ac9d4-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="ac9d4-181">Defina os Estados de um evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="ac9d4-183">Defina o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="ac9d4-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="ac9d4-185">Defina o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ac9d4-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="ac9d4-187">Defina o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="ac9d4-189">Defina o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ac9d4-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="ac9d4-191">Defina o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ac9d4-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="ac9d4-193">Defina o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ac9d4-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="ac9d4-195">Defina o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="ac9d4-197">Defina o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="ac9d4-199">Defina o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ac9d4-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="ac9d4-201">Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ac9d4-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="ac9d4-203">Defina o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="ac9d4-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="ac9d4-205">Defina a barra de ponteiros do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ac9d4-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="ac9d4-207">Defina o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="ac9d4-208">put_Time</span></span>](#put_time) | <span data-ttu-id="ac9d4-209">Defina a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ac9d4-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="ac9d4-211">Defina o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="ac9d4-213">Defina o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="ac9d4-215">Defina o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ac9d4-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="ac9d4-217">Defina o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="ac9d4-219">Defina o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="ac9d4-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ac9d4-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="ac9d4-221">Defina o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="ac9d4-222">Ele recebe campos de todos os três e exclui alguns tipos de dados específicos do Win32, como HWND e HANDLE.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="ac9d4-223">Observe que sourceDevice é retirado, mas esperamos que o PointerDeviceRect e o DisplayRect cubram os casos de uso existentes do sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="ac9d4-224">Outra grande diferença é que qualquer um dos locais ponto ou RECT deve estar nas coordenadas físicas da WebView.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="ac9d4-225">Ou seja, as coordenadas relativas ao WebView e ao ajuste de DPI aplicado.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="ac9d4-226">Parte</span><span class="sxs-lookup"><span data-stu-id="ac9d4-226">Members</span></span>

#### <span data-ttu-id="ac9d4-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ac9d4-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="ac9d4-228">Obtenha o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-229">Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="ac9d4-230">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac9d4-231">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ac9d4-232">get_DisplayRect</span></span> 

<span data-ttu-id="ac9d4-233">Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ac9d4-234">Public HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="ac9d4-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="ac9d4-235">get_FrameId</span></span> 

<span data-ttu-id="ac9d4-236">Obtenha o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-237">[get_FrameId](#get_frameid)público HRESULT (UINT32 \* frameid)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="ac9d4-238">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-239">get_HimetricLocation</span></span> 

<span data-ttu-id="ac9d4-240">Obtenha o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-241">público HRESULT [get_HimetricLocation](#get_himetriclocation)(ponto \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="ac9d4-242">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="ac9d4-244">Obtenha o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-245">público HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(ponto \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="ac9d4-246">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ac9d4-247">get_HistoryCount</span></span> 

<span data-ttu-id="ac9d4-248">Obtenha o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-249">público HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="ac9d4-250">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="ac9d4-251">get_InputData</span></span> 

<span data-ttu-id="ac9d4-252">Obtenha o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-253">Public HRESULT [get_InputData](#get_inputdata)(INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="ac9d4-254">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ac9d4-255">get_KeyStates</span></span> 

<span data-ttu-id="ac9d4-256">Obtenha os Estados de KeyState do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-257">público HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="ac9d4-258">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-259">get_PenFlags</span></span> 

<span data-ttu-id="ac9d4-260">Obtenha o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-261">público HRESULT [get_PenFlags](#get_penflags)(UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="ac9d4-262">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ac9d4-263">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="ac9d4-264">get_PenMask</span></span> 

<span data-ttu-id="ac9d4-265">Obtenha o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-266">público HRESULT [get_PenMask](#get_penmask)(UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="ac9d4-267">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ac9d4-268">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ac9d4-269">get_PenPressure</span></span> 

<span data-ttu-id="ac9d4-270">Obtenha o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-271">público HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="ac9d4-272">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-273">get_PenRotation</span></span> 

<span data-ttu-id="ac9d4-274">Obtenha o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-275">público HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="ac9d4-276">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ac9d4-277">get_PenTiltX</span></span> 

<span data-ttu-id="ac9d4-278">Obtenha o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-279">Public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="ac9d4-280">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ac9d4-281">get_PenTiltY</span></span> 

<span data-ttu-id="ac9d4-282">Obtenha o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-283">Public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="ac9d4-284">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ac9d4-285">get_PerformanceCount</span></span> 

<span data-ttu-id="ac9d4-286">Obtenha o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-287">público HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="ac9d4-288">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-289">get_PixelLocation</span></span> 

<span data-ttu-id="ac9d4-290">Obtenha o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-291">público HRESULT [get_PixelLocation](#get_pixellocation)(ponto \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="ac9d4-292">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="ac9d4-294">Obtenha o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-295">público HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(ponto \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="ac9d4-296">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ac9d4-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="ac9d4-298">Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ac9d4-299">Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="ac9d4-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-300">get_PointerFlags</span></span> 

<span data-ttu-id="ac9d4-301">Obtenha o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-302">público HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="ac9d4-303">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac9d4-304">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="ac9d4-305">get_PointerId</span></span> 

<span data-ttu-id="ac9d4-306">Obtenha o Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-307">[get_PointerId](#get_pointerid)público HRESULT (UINT32 \* pointerid)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="ac9d4-308">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ac9d4-309">get_PointerKind</span></span> 

<span data-ttu-id="ac9d4-310">Obtenha o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-311">Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="ac9d4-312">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac9d4-313">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="ac9d4-314">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="ac9d4-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="ac9d4-315">get_Time</span></span> 

<span data-ttu-id="ac9d4-316">Obtenha a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-317">[get_Time](#get_time)público HRESULT (DWORD \* time)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="ac9d4-318">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ac9d4-319">get_TouchContact</span></span> 

<span data-ttu-id="ac9d4-320">Obtenha o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-321">Public HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="ac9d4-322">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="ac9d4-324">Obtenha o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-325">Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="ac9d4-326">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-327">get_TouchFlags</span></span> 

<span data-ttu-id="ac9d4-328">Obtenha o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-329">público HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="ac9d4-330">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ac9d4-331">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ac9d4-332">get_TouchMask</span></span> 

<span data-ttu-id="ac9d4-333">Obtenha o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-334">público HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="ac9d4-335">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ac9d4-336">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-337">get_TouchOrientation</span></span> 

<span data-ttu-id="ac9d4-338">Obtenha o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-339">público HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="ac9d4-340">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ac9d4-341">get_TouchPressure</span></span> 

<span data-ttu-id="ac9d4-342">Obtenha o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-343">público HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="ac9d4-344">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ac9d4-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="ac9d4-346">Defina o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-347">[put_ButtonChangeKind](#put_buttonchangekind)público HRESULT (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="ac9d4-348">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac9d4-349">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ac9d4-350">put_DisplayRect</span></span> 

<span data-ttu-id="ac9d4-351">Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ac9d4-352">Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="ac9d4-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="ac9d4-353">put_FrameId</span></span> 

<span data-ttu-id="ac9d4-354">Defina o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-355">[put_FrameId](#put_frameid)público HRESULT (UINT32 frameid)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="ac9d4-356">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-357">put_HimetricLocation</span></span> 

<span data-ttu-id="ac9d4-358">Defina o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-359">público HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="ac9d4-360">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="ac9d4-362">Defina o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-363">público HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="ac9d4-364">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ac9d4-365">put_HistoryCount</span></span> 

<span data-ttu-id="ac9d4-366">Defina o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-367">público HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="ac9d4-368">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="ac9d4-369">put_InputData</span></span> 

<span data-ttu-id="ac9d4-370">Defina o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-371">[put_InputData](#put_inputdata)público HRESULT (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="ac9d4-372">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ac9d4-373">put_KeyStates</span></span> 

<span data-ttu-id="ac9d4-374">Defina os Estados de um evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-375">público HRESULT [put_KeyStates](#put_keystates)(estado DWORD DWORD)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="ac9d4-376">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-377">put_PenFlags</span></span> 

<span data-ttu-id="ac9d4-378">Defina o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-379">público HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="ac9d4-380">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ac9d4-381">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="ac9d4-382">put_PenMask</span></span> 

<span data-ttu-id="ac9d4-383">Defina o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-384">público HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="ac9d4-385">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ac9d4-386">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ac9d4-387">put_PenPressure</span></span> 

<span data-ttu-id="ac9d4-388">Defina o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-389">público HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="ac9d4-390">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-391">put_PenRotation</span></span> 

<span data-ttu-id="ac9d4-392">Defina o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-393">público HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="ac9d4-394">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ac9d4-395">put_PenTiltX</span></span> 

<span data-ttu-id="ac9d4-396">Defina o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-397">[put_PenTiltX](#put_pentiltx)público HRESULT (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="ac9d4-398">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ac9d4-399">put_PenTiltY</span></span> 

<span data-ttu-id="ac9d4-400">Defina o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-401">[put_PenTiltY](#put_pentilty)público HRESULT (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="ac9d4-402">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ac9d4-403">put_PerformanceCount</span></span> 

<span data-ttu-id="ac9d4-404">Defina o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-405">público HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="ac9d4-406">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-407">put_PixelLocation</span></span> 

<span data-ttu-id="ac9d4-408">Defina o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-409">público HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="ac9d4-410">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="ac9d4-412">Defina o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-413">público HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="ac9d4-414">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ac9d4-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="ac9d4-416">Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ac9d4-417">Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="ac9d4-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-418">put_PointerFlags</span></span> 

<span data-ttu-id="ac9d4-419">Defina o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-420">público HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="ac9d4-421">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac9d4-422">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="ac9d4-423">put_PointerId</span></span> 

<span data-ttu-id="ac9d4-424">Defina a barra de ponteiros do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-425">[put_PointerId](#put_pointerid)público HRESULT (ponteiroid UINT32)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="ac9d4-426">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ac9d4-427">put_PointerKind</span></span> 

<span data-ttu-id="ac9d4-428">Defina o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-429">público HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="ac9d4-430">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac9d4-431">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="ac9d4-432">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="ac9d4-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="ac9d4-433">put_Time</span></span> 

<span data-ttu-id="ac9d4-434">Defina a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-435">[put_Time](#put_time)público HRESULT (tempo DWORD)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="ac9d4-436">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ac9d4-437">put_TouchContact</span></span> 

<span data-ttu-id="ac9d4-438">Defina o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-439">Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="ac9d4-440">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ac9d4-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="ac9d4-442">Defina o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-443">Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="ac9d4-444">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ac9d4-445">put_TouchFlags</span></span> 

<span data-ttu-id="ac9d4-446">Defina o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-447">público HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="ac9d4-448">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ac9d4-449">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ac9d4-450">put_TouchMask</span></span> 

<span data-ttu-id="ac9d4-451">Defina o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-452">público HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="ac9d4-453">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ac9d4-454">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ac9d4-455">put_TouchOrientation</span></span> 

<span data-ttu-id="ac9d4-456">Defina o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-457">público HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="ac9d4-458">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac9d4-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ac9d4-459">put_TouchPressure</span></span> 

<span data-ttu-id="ac9d4-460">Defina o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ac9d4-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="ac9d4-461">público HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="ac9d4-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="ac9d4-462">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="ac9d4-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

