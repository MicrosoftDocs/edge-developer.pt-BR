---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalPointerInfo
ms.openlocfilehash: db966ad087e22bc6b8d3865c416f8feba15e434a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011395"
---
# <span data-ttu-id="fb3f0-104">0.9.579-ICoreWebView2ExperimentalPointerInfo de interface</span><span class="sxs-lookup"><span data-stu-id="fb3f0-104">0.9.579 - interface ICoreWebView2ExperimentalPointerInfo</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="fb3f0-105">Isso basicamente representa um objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combinado.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-105">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="fb3f0-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="fb3f0-106">Summary</span></span>

 <span data-ttu-id="fb3f0-107">Parte</span><span class="sxs-lookup"><span data-stu-id="fb3f0-107">Members</span></span>                        | <span data-ttu-id="fb3f0-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="fb3f0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fb3f0-109">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="fb3f0-109">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="fb3f0-110">Obtenha o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-110">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-111">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="fb3f0-111">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="fb3f0-112">Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-112">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="fb3f0-113">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="fb3f0-113">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="fb3f0-114">Obtenha o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-114">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-115">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-115">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="fb3f0-116">Obtenha o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-116">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-117">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-117">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="fb3f0-118">Obtenha o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-118">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-119">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="fb3f0-119">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="fb3f0-120">Obtenha o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-120">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-121">get_InputData</span><span class="sxs-lookup"><span data-stu-id="fb3f0-121">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="fb3f0-122">Obtenha o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-122">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-123">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="fb3f0-123">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="fb3f0-124">Obtenha os Estados de KeyState do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-124">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-125">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-125">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="fb3f0-126">Obtenha o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-126">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-127">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="fb3f0-127">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="fb3f0-128">Obtenha o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-128">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-129">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="fb3f0-129">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="fb3f0-130">Obtenha o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-130">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-131">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-131">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="fb3f0-132">Obtenha o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-132">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-133">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="fb3f0-133">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="fb3f0-134">Obtenha o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-134">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-135">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="fb3f0-135">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="fb3f0-136">Obtenha o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-136">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-137">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="fb3f0-137">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="fb3f0-138">Obtenha o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-138">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-139">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-139">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="fb3f0-140">Obtenha o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-140">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-141">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-141">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="fb3f0-142">Obtenha o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-142">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-143">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="fb3f0-143">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="fb3f0-144">Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-144">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="fb3f0-145">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-145">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="fb3f0-146">Obtenha o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-146">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-147">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="fb3f0-147">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="fb3f0-148">Obtenha o Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-148">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-149">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="fb3f0-149">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="fb3f0-150">Obtenha o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-150">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-151">get_Time</span><span class="sxs-lookup"><span data-stu-id="fb3f0-151">get_Time</span></span>](#get_time) | <span data-ttu-id="fb3f0-152">Obtenha a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-152">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-153">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="fb3f0-153">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="fb3f0-154">Obtenha o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-154">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-155">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-155">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="fb3f0-156">Obtenha o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-156">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-157">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-157">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="fb3f0-158">Obtenha o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-158">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-159">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="fb3f0-159">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="fb3f0-160">Obtenha o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-160">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-161">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-161">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="fb3f0-162">Obtenha o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-162">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-163">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="fb3f0-163">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="fb3f0-164">Obtenha o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-164">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-165">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="fb3f0-165">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="fb3f0-166">Defina o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-166">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-167">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="fb3f0-167">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="fb3f0-168">Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-168">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="fb3f0-169">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="fb3f0-169">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="fb3f0-170">Defina o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-170">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-171">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-171">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="fb3f0-172">Defina o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-172">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-173">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-173">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="fb3f0-174">Defina o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-174">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-175">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="fb3f0-175">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="fb3f0-176">Defina o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-176">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-177">put_InputData</span><span class="sxs-lookup"><span data-stu-id="fb3f0-177">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="fb3f0-178">Defina o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-178">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-179">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="fb3f0-179">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="fb3f0-180">Defina os Estados de um evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-180">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-181">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-181">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="fb3f0-182">Defina o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-182">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-183">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="fb3f0-183">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="fb3f0-184">Defina o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-184">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-185">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="fb3f0-185">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="fb3f0-186">Defina o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-186">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-187">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-187">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="fb3f0-188">Defina o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-188">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-189">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="fb3f0-189">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="fb3f0-190">Defina o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-190">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-191">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="fb3f0-191">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="fb3f0-192">Defina o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-192">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-193">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="fb3f0-193">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="fb3f0-194">Defina o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-194">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-195">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-195">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="fb3f0-196">Defina o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-196">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-197">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-197">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="fb3f0-198">Defina o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-198">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-199">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="fb3f0-199">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="fb3f0-200">Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-200">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="fb3f0-201">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-201">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="fb3f0-202">Defina o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-202">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-203">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="fb3f0-203">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="fb3f0-204">Defina a barra de ponteiros do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-204">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-205">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="fb3f0-205">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="fb3f0-206">Defina o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-206">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-207">put_Time</span><span class="sxs-lookup"><span data-stu-id="fb3f0-207">put_Time</span></span>](#put_time) | <span data-ttu-id="fb3f0-208">Defina a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-208">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-209">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="fb3f0-209">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="fb3f0-210">Defina o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-210">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-211">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-211">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="fb3f0-212">Defina o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-212">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-213">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-213">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="fb3f0-214">Defina o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-214">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-215">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="fb3f0-215">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="fb3f0-216">Defina o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-216">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-217">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-217">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="fb3f0-218">Defina o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-218">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="fb3f0-219">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="fb3f0-219">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="fb3f0-220">Defina o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-220">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="fb3f0-221">Ele recebe campos de todos os três e exclui alguns tipos de dados específicos do Win32, como HWND e HANDLE.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-221">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="fb3f0-222">Observe que sourceDevice é retirado, mas esperamos que o PointerDeviceRect e o DisplayRect cubram os casos de uso existentes do sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-222">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="fb3f0-223">Outra grande diferença é que qualquer um dos locais ponto ou RECT deve estar nas coordenadas físicas da WebView.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-223">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="fb3f0-224">Ou seja, as coordenadas relativas ao WebView e ao ajuste de DPI aplicado.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-224">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="fb3f0-225">Parte</span><span class="sxs-lookup"><span data-stu-id="fb3f0-225">Members</span></span>

#### <span data-ttu-id="fb3f0-226">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="fb3f0-226">get_ButtonChangeKind</span></span> 

<span data-ttu-id="fb3f0-227">Obtenha o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-227">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-228">Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-228">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="fb3f0-229">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-229">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fb3f0-230">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-230">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-231">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="fb3f0-231">get_DisplayRect</span></span> 

<span data-ttu-id="fb3f0-232">Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-232">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="fb3f0-233">Public HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-233">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="fb3f0-234">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="fb3f0-234">get_FrameId</span></span> 

<span data-ttu-id="fb3f0-235">Obtenha o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-235">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-236">[get_FrameId](#get_frameid)público HRESULT (UINT32 \* frameid)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-236">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="fb3f0-237">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-237">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-238">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-238">get_HimetricLocation</span></span> 

<span data-ttu-id="fb3f0-239">Obtenha o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-239">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-240">público HRESULT [get_HimetricLocation](#get_himetriclocation)(ponto \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-240">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="fb3f0-241">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-241">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-242">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-242">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="fb3f0-243">Obtenha o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-243">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-244">público HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(ponto \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-244">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="fb3f0-245">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-245">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-246">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="fb3f0-246">get_HistoryCount</span></span> 

<span data-ttu-id="fb3f0-247">Obtenha o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-247">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-248">público HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-248">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="fb3f0-249">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-249">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-250">get_InputData</span><span class="sxs-lookup"><span data-stu-id="fb3f0-250">get_InputData</span></span> 

<span data-ttu-id="fb3f0-251">Obtenha o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-251">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-252">Public HRESULT [get_InputData](#get_inputdata)(INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-252">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="fb3f0-253">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-253">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-254">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="fb3f0-254">get_KeyStates</span></span> 

<span data-ttu-id="fb3f0-255">Obtenha os Estados de KeyState do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-255">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-256">público HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-256">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="fb3f0-257">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-257">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-258">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-258">get_PenFlags</span></span> 

<span data-ttu-id="fb3f0-259">Obtenha o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-259">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-260">público HRESULT [get_PenFlags](#get_penflags)(UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-260">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="fb3f0-261">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-261">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="fb3f0-262">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-262">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-263">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="fb3f0-263">get_PenMask</span></span> 

<span data-ttu-id="fb3f0-264">Obtenha o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-264">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-265">público HRESULT [get_PenMask](#get_penmask)(UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-265">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="fb3f0-266">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-266">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="fb3f0-267">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-267">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-268">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="fb3f0-268">get_PenPressure</span></span> 

<span data-ttu-id="fb3f0-269">Obtenha o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-269">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-270">público HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-270">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="fb3f0-271">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-271">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-272">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-272">get_PenRotation</span></span> 

<span data-ttu-id="fb3f0-273">Obtenha o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-273">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-274">público HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-274">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="fb3f0-275">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-275">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-276">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="fb3f0-276">get_PenTiltX</span></span> 

<span data-ttu-id="fb3f0-277">Obtenha o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-277">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-278">Public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-278">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="fb3f0-279">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-279">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-280">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="fb3f0-280">get_PenTiltY</span></span> 

<span data-ttu-id="fb3f0-281">Obtenha o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-281">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-282">Public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-282">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="fb3f0-283">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-283">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-284">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="fb3f0-284">get_PerformanceCount</span></span> 

<span data-ttu-id="fb3f0-285">Obtenha o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-285">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-286">público HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-286">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="fb3f0-287">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-287">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-288">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-288">get_PixelLocation</span></span> 

<span data-ttu-id="fb3f0-289">Obtenha o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-289">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-290">público HRESULT [get_PixelLocation](#get_pixellocation)(ponto \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-290">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="fb3f0-291">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-291">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-292">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-292">get_PixelLocationRaw</span></span> 

<span data-ttu-id="fb3f0-293">Obtenha o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-293">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-294">público HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(ponto \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-294">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="fb3f0-295">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-295">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-296">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="fb3f0-296">get_PointerDeviceRect</span></span> 

<span data-ttu-id="fb3f0-297">Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-297">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="fb3f0-298">Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-298">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="fb3f0-299">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-299">get_PointerFlags</span></span> 

<span data-ttu-id="fb3f0-300">Obtenha o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-300">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-301">público HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-301">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="fb3f0-302">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-302">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fb3f0-303">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-303">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-304">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="fb3f0-304">get_PointerId</span></span> 

<span data-ttu-id="fb3f0-305">Obtenha o Ponteiroid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-305">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-306">[get_PointerId](#get_pointerid)público HRESULT (UINT32 \* pointerid)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-306">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="fb3f0-307">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-307">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-308">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="fb3f0-308">get_PointerKind</span></span> 

<span data-ttu-id="fb3f0-309">Obtenha o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-309">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-310">Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-310">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="fb3f0-311">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-311">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fb3f0-312">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-312">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="fb3f0-313">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-313">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="fb3f0-314">get_Time</span><span class="sxs-lookup"><span data-stu-id="fb3f0-314">get_Time</span></span> 

<span data-ttu-id="fb3f0-315">Obtenha a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-315">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-316">[get_Time](#get_time)público HRESULT (DWORD \* time)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-316">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="fb3f0-317">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-317">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-318">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="fb3f0-318">get_TouchContact</span></span> 

<span data-ttu-id="fb3f0-319">Obtenha o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-319">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-320">Public HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-320">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="fb3f0-321">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-321">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-322">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-322">get_TouchContactRaw</span></span> 

<span data-ttu-id="fb3f0-323">Obtenha o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-323">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-324">Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-324">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="fb3f0-325">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-325">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-326">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-326">get_TouchFlags</span></span> 

<span data-ttu-id="fb3f0-327">Obtenha o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-327">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-328">público HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-328">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="fb3f0-329">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-329">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="fb3f0-330">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-330">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-331">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="fb3f0-331">get_TouchMask</span></span> 

<span data-ttu-id="fb3f0-332">Obtenha o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-332">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-333">público HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-333">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="fb3f0-334">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-334">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="fb3f0-335">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-335">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-336">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-336">get_TouchOrientation</span></span> 

<span data-ttu-id="fb3f0-337">Obtenha o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-337">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-338">público HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-338">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="fb3f0-339">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-339">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-340">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="fb3f0-340">get_TouchPressure</span></span> 

<span data-ttu-id="fb3f0-341">Obtenha o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-341">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-342">público HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-342">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="fb3f0-343">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-343">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-344">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="fb3f0-344">put_ButtonChangeKind</span></span> 

<span data-ttu-id="fb3f0-345">Defina o ButtonChangeKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-345">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-346">[put_ButtonChangeKind](#put_buttonchangekind)público HRESULT (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-346">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="fb3f0-347">Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-347">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fb3f0-348">Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-348">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-349">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="fb3f0-349">put_DisplayRect</span></span> 

<span data-ttu-id="fb3f0-350">Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-350">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="fb3f0-351">Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-351">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="fb3f0-352">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="fb3f0-352">put_FrameId</span></span> 

<span data-ttu-id="fb3f0-353">Defina o Frameid do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-353">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-354">[put_FrameId](#put_frameid)público HRESULT (UINT32 frameid)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-354">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="fb3f0-355">Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-355">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-356">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-356">put_HimetricLocation</span></span> 

<span data-ttu-id="fb3f0-357">Defina o HimetricLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-357">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-358">público HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-358">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="fb3f0-359">Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-359">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-360">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-360">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="fb3f0-361">Defina o HimetricLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-361">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-362">público HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-362">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="fb3f0-363">Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-363">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-364">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="fb3f0-364">put_HistoryCount</span></span> 

<span data-ttu-id="fb3f0-365">Defina o HistoryCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-365">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-366">público HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-366">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="fb3f0-367">Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-367">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-368">put_InputData</span><span class="sxs-lookup"><span data-stu-id="fb3f0-368">put_InputData</span></span> 

<span data-ttu-id="fb3f0-369">Defina o InputData do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-369">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-370">[put_InputData](#put_inputdata)público HRESULT (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-370">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="fb3f0-371">Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-371">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-372">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="fb3f0-372">put_KeyStates</span></span> 

<span data-ttu-id="fb3f0-373">Defina os Estados de um evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-373">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-374">público HRESULT [put_KeyStates](#put_keystates)(estado DWORD DWORD)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-374">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="fb3f0-375">Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-375">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-376">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-376">put_PenFlags</span></span> 

<span data-ttu-id="fb3f0-377">Defina o PenFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-377">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-378">público HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-378">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="fb3f0-379">Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-379">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="fb3f0-380">Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-380">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-381">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="fb3f0-381">put_PenMask</span></span> 

<span data-ttu-id="fb3f0-382">Defina o PenMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-382">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-383">público HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-383">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="fb3f0-384">Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-384">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="fb3f0-385">Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-385">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-386">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="fb3f0-386">put_PenPressure</span></span> 

<span data-ttu-id="fb3f0-387">Defina o PenPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-387">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-388">público HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-388">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="fb3f0-389">Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-389">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-390">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-390">put_PenRotation</span></span> 

<span data-ttu-id="fb3f0-391">Defina o PenRotation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-391">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-392">público HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-392">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="fb3f0-393">Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-393">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-394">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="fb3f0-394">put_PenTiltX</span></span> 

<span data-ttu-id="fb3f0-395">Defina o PenTiltX do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-395">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-396">[put_PenTiltX](#put_pentiltx)público HRESULT (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-396">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="fb3f0-397">Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-397">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-398">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="fb3f0-398">put_PenTiltY</span></span> 

<span data-ttu-id="fb3f0-399">Defina o PenTiltY do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-399">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-400">[put_PenTiltY](#put_pentilty)público HRESULT (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-400">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="fb3f0-401">Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-401">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-402">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="fb3f0-402">put_PerformanceCount</span></span> 

<span data-ttu-id="fb3f0-403">Defina o PerformanceCount do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-403">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-404">público HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-404">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="fb3f0-405">Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-405">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-406">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-406">put_PixelLocation</span></span> 

<span data-ttu-id="fb3f0-407">Defina o PixelLocation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-407">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-408">público HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-408">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="fb3f0-409">Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-409">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-410">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-410">put_PixelLocationRaw</span></span> 

<span data-ttu-id="fb3f0-411">Defina o PixelLocationRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-411">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-412">público HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-412">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="fb3f0-413">Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-413">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-414">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="fb3f0-414">put_PointerDeviceRect</span></span> 

<span data-ttu-id="fb3f0-415">Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-415">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="fb3f0-416">Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-416">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="fb3f0-417">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-417">put_PointerFlags</span></span> 

<span data-ttu-id="fb3f0-418">Defina o PointerFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-418">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-419">público HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-419">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="fb3f0-420">Isso corresponde à propriedade pointerFlags do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-420">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fb3f0-421">Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-421">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-422">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="fb3f0-422">put_PointerId</span></span> 

<span data-ttu-id="fb3f0-423">Defina a barra de ponteiros do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-423">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-424">[put_PointerId](#put_pointerid)público HRESULT (ponteiroid UINT32)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-424">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="fb3f0-425">Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-425">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-426">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="fb3f0-426">put_PointerKind</span></span> 

<span data-ttu-id="fb3f0-427">Defina o PointerKind do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-427">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-428">público HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-428">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="fb3f0-429">Isso corresponde à propriedade pointerKind do struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-429">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fb3f0-430">Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-430">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="fb3f0-431">Suporta PT_PEN e PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-431">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="fb3f0-432">put_Time</span><span class="sxs-lookup"><span data-stu-id="fb3f0-432">put_Time</span></span> 

<span data-ttu-id="fb3f0-433">Defina a hora do evento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-433">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-434">[put_Time](#put_time)público HRESULT (tempo DWORD)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-434">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="fb3f0-435">Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-435">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-436">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="fb3f0-436">put_TouchContact</span></span> 

<span data-ttu-id="fb3f0-437">Defina o TouchContact do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-437">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-438">Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-438">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="fb3f0-439">Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-439">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-440">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="fb3f0-440">put_TouchContactRaw</span></span> 

<span data-ttu-id="fb3f0-441">Defina o TouchContactRaw do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-441">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-442">Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-442">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="fb3f0-443">Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-443">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-444">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="fb3f0-444">put_TouchFlags</span></span> 

<span data-ttu-id="fb3f0-445">Defina o TouchFlags do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-445">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-446">público HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-446">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="fb3f0-447">Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-447">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="fb3f0-448">Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-448">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-449">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="fb3f0-449">put_TouchMask</span></span> 

<span data-ttu-id="fb3f0-450">Defina o TouchMask do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-450">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-451">público HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-451">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="fb3f0-452">Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-452">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="fb3f0-453">Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-453">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-454">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="fb3f0-454">put_TouchOrientation</span></span> 

<span data-ttu-id="fb3f0-455">Defina o TouchOrientation do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-455">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-456">público HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-456">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="fb3f0-457">Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-457">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fb3f0-458">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="fb3f0-458">put_TouchPressure</span></span> 

<span data-ttu-id="fb3f0-459">Defina o TouchPressure do evento ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fb3f0-459">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="fb3f0-460">público HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="fb3f0-460">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="fb3f0-461">Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).</span><span class="sxs-lookup"><span data-stu-id="fb3f0-461">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

