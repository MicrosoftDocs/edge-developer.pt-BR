---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalPointerInfo
ms.openlocfilehash: bc35ebaf3f1b5acf12a1d379336cd006f962390e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011572"
---
# interface ICoreWebView2ExperimentalPointerInfo 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

Isso basicamente representa um objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combinado.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_ButtonChangeKind](#get_buttonchangekind) | Obtenha o ButtonChangeKind do evento ponteiro.
[get_DisplayRect](#get_displayrect) | Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).
[get_FrameId](#get_frameid) | Obtenha o Frameid do evento ponteiro.
[get_HimetricLocation](#get_himetriclocation) | Obtenha o HimetricLocation do evento ponteiro.
[get_HimetricLocationRaw](#get_himetriclocationraw) | Obtenha o HimetricLocationRaw do evento ponteiro.
[get_HistoryCount](#get_historycount) | Obtenha o HistoryCount do evento ponteiro.
[get_InputData](#get_inputdata) | Obtenha o InputData do evento ponteiro.
[get_KeyStates](#get_keystates) | Obtenha os Estados de KeyState do evento ponteiro.
[get_PenFlags](#get_penflags) | Obtenha o PenFlags do evento ponteiro.
[get_PenMask](#get_penmask) | Obtenha o PenMask do evento ponteiro.
[get_PenPressure](#get_penpressure) | Obtenha o PenPressure do evento ponteiro.
[get_PenRotation](#get_penrotation) | Obtenha o PenRotation do evento ponteiro.
[get_PenTiltX](#get_pentiltx) | Obtenha o PenTiltX do evento ponteiro.
[get_PenTiltY](#get_pentilty) | Obtenha o PenTiltY do evento ponteiro.
[get_PerformanceCount](#get_performancecount) | Obtenha o PerformanceCount do evento ponteiro.
[get_PixelLocation](#get_pixellocation) | Obtenha o PixelLocation do evento ponteiro.
[get_PixelLocationRaw](#get_pixellocationraw) | Obtenha o PixelLocationRaw do evento ponteiro.
[get_PointerDeviceRect](#get_pointerdevicerect) | Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).
[get_PointerFlags](#get_pointerflags) | Obtenha o PointerFlags do evento ponteiro.
[get_PointerId](#get_pointerid) | Obtenha o Ponteiroid do evento ponteiro.
[get_PointerKind](#get_pointerkind) | Obtenha o PointerKind do evento ponteiro.
[get_Time](#get_time) | Obtenha a hora do evento de ponteiro.
[get_TouchContact](#get_touchcontact) | Obtenha o TouchContact do evento ponteiro.
[get_TouchContactRaw](#get_touchcontactraw) | Obtenha o TouchContactRaw do evento ponteiro.
[get_TouchFlags](#get_touchflags) | Obtenha o TouchFlags do evento ponteiro.
[get_TouchMask](#get_touchmask) | Obtenha o TouchMask do evento ponteiro.
[get_TouchOrientation](#get_touchorientation) | Obtenha o TouchOrientation do evento ponteiro.
[get_TouchPressure](#get_touchpressure) | Obtenha o TouchPressure do evento ponteiro.
[put_ButtonChangeKind](#put_buttonchangekind) | Defina o ButtonChangeKind do evento ponteiro.
[put_DisplayRect](#put_displayrect) | Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).
[put_FrameId](#put_frameid) | Defina o Frameid do evento ponteiro.
[put_HimetricLocation](#put_himetriclocation) | Defina o HimetricLocation do evento ponteiro.
[put_HimetricLocationRaw](#put_himetriclocationraw) | Defina o HimetricLocationRaw do evento ponteiro.
[put_HistoryCount](#put_historycount) | Defina o HistoryCount do evento ponteiro.
[put_InputData](#put_inputdata) | Defina o InputData do evento ponteiro.
[put_KeyStates](#put_keystates) | Defina os Estados de um evento de ponteiro.
[put_PenFlags](#put_penflags) | Defina o PenFlags do evento ponteiro.
[put_PenMask](#put_penmask) | Defina o PenMask do evento ponteiro.
[put_PenPressure](#put_penpressure) | Defina o PenPressure do evento ponteiro.
[put_PenRotation](#put_penrotation) | Defina o PenRotation do evento ponteiro.
[put_PenTiltX](#put_pentiltx) | Defina o PenTiltX do evento ponteiro.
[put_PenTiltY](#put_pentilty) | Defina o PenTiltY do evento ponteiro.
[put_PerformanceCount](#put_performancecount) | Defina o PerformanceCount do evento ponteiro.
[put_PixelLocation](#put_pixellocation) | Defina o PixelLocation do evento ponteiro.
[put_PixelLocationRaw](#put_pixellocationraw) | Defina o PixelLocationRaw do evento ponteiro.
[put_PointerDeviceRect](#put_pointerdevicerect) | Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).
[put_PointerFlags](#put_pointerflags) | Defina o PointerFlags do evento ponteiro.
[put_PointerId](#put_pointerid) | Defina a barra de ponteiros do evento ponteiro.
[put_PointerKind](#put_pointerkind) | Defina o PointerKind do evento ponteiro.
[put_Time](#put_time) | Defina a hora do evento de ponteiro.
[put_TouchContact](#put_touchcontact) | Defina o TouchContact do evento ponteiro.
[put_TouchContactRaw](#put_touchcontactraw) | Defina o TouchContactRaw do evento ponteiro.
[put_TouchFlags](#put_touchflags) | Defina o TouchFlags do evento ponteiro.
[put_TouchMask](#put_touchmask) | Defina o TouchMask do evento ponteiro.
[put_TouchOrientation](#put_touchorientation) | Defina o TouchOrientation do evento ponteiro.
[put_TouchPressure](#put_touchpressure) | Defina o TouchPressure do evento ponteiro.

Ele recebe campos de todos os três e exclui alguns tipos de dados específicos do Win32, como HWND e HANDLE. Observe que sourceDevice é retirado, mas esperamos que o PointerDeviceRect e o DisplayRect cubram os casos de uso existentes do sourceDevice. Outra grande diferença é que qualquer um dos locais ponto ou RECT deve estar nas coordenadas físicas da WebView. Ou seja, as coordenadas relativas ao WebView e ao ajuste de DPI aplicado.

## Parte

#### get_ButtonChangeKind 

Obtenha o ButtonChangeKind do evento ponteiro.

> Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 * ButtonChangeKind)

Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO. Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).

#### get_DisplayRect 

Obtenha o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

> Public HRESULT [get_DisplayRect](#get_displayrect)(Rect * DisplayRect)

#### get_FrameId 

Obtenha o Frameid do evento ponteiro.

> [get_FrameId](#get_frameid)público HRESULT (UINT32 * frameid)

Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_HimetricLocation 

Obtenha o HimetricLocation do evento ponteiro.

> público HRESULT [get_HimetricLocation](#get_himetriclocation)(ponto * HimetricLocation)

Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_HimetricLocationRaw 

Obtenha o HimetricLocationRaw do evento ponteiro.

> público HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(ponto * HimetricLocationRaw)

Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_HistoryCount 

Obtenha o HistoryCount do evento ponteiro.

> público HRESULT [get_HistoryCount](#get_historycount)(UINT32 * HistoryCount)

Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_InputData 

Obtenha o InputData do evento ponteiro.

> Public HRESULT [get_InputData](#get_inputdata)(INT32 * InputData)

Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_KeyStates 

Obtenha os Estados de KeyState do evento ponteiro.

> público HRESULT [get_KeyStates](#get_keystates)(DWORD * KeyStates)

Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PenFlags 

Obtenha o PenFlags do evento ponteiro.

> público HRESULT [get_PenFlags](#get_penflags)(UINT32 * PenFlags)

Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO. Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).

#### get_PenMask 

Obtenha o PenMask do evento ponteiro.

> público HRESULT [get_PenMask](#get_penmask)(UINT32 * PenMask)

Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO. Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).

#### get_PenPressure 

Obtenha o PenPressure do evento ponteiro.

> público HRESULT [get_PenPressure](#get_penpressure)(UINT32 * PenPressure)

Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PenRotation 

Obtenha o PenRotation do evento ponteiro.

> público HRESULT [get_PenRotation](#get_penrotation)(UINT32 * PenRotation)

Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PenTiltX 

Obtenha o PenTiltX do evento ponteiro.

> Public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 * PenTiltX)

Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PenTiltY 

Obtenha o PenTiltY do evento ponteiro.

> Public HRESULT [get_PenTiltY](#get_pentilty)(INT32 * PenTiltY)

Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PerformanceCount 

Obtenha o PerformanceCount do evento ponteiro.

> público HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 * PerformanceCount)

Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PixelLocation 

Obtenha o PixelLocation do evento ponteiro.

> público HRESULT [get_PixelLocation](#get_pixellocation)(ponto * PixelLocation)

Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PixelLocationRaw 

Obtenha o PixelLocationRaw do evento ponteiro.

> público HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(ponto * PixelLocationRaw)

Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PointerDeviceRect 

Obtenha o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

> Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect * PointerDeviceRect)

#### get_PointerFlags 

Obtenha o PointerFlags do evento ponteiro.

> público HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 * PointerFlags)

Isso corresponde à propriedade pointerFlags do struct POINTER_INFO. Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).

#### get_PointerId 

Obtenha o Ponteiroid do evento ponteiro.

> [get_PointerId](#get_pointerid)público HRESULT (UINT32 * pointerid)

Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_PointerKind 

Obtenha o PointerKind do evento ponteiro.

> Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD * PointerKind)

Isso corresponde à propriedade pointerKind do struct POINTER_INFO. Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h). Suporta PT_PEN e PT_TOUCH.

#### get_Time 

Obtenha a hora do evento de ponteiro.

> [get_Time](#get_time)público HRESULT (DWORD * time)

Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_TouchContact 

Obtenha o TouchContact do evento ponteiro.

> Public HRESULT [get_TouchContact](#get_touchcontact)(Rect * TouchContact)

Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_TouchContactRaw 

Obtenha o TouchContactRaw do evento ponteiro.

> Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect * TouchContactRaw)

Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

#### get_TouchFlags 

Obtenha o TouchFlags do evento ponteiro.

> público HRESULT [get_TouchFlags](#get_touchflags)(UINT32 * TouchFlags)

Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO. Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).

#### get_TouchMask 

Obtenha o TouchMask do evento ponteiro.

> público HRESULT [get_TouchMask](#get_touchmask)(UINT32 * TouchMask)

Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO. Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).

#### get_TouchOrientation 

Obtenha o TouchOrientation do evento ponteiro.

> público HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 * TouchOrientation)

Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).

#### get_TouchPressure 

Obtenha o TouchPressure do evento ponteiro.

> público HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 * TouchPressure)

Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_ButtonChangeKind 

Defina o ButtonChangeKind do evento ponteiro.

> [put_ButtonChangeKind](#put_buttonchangekind)público HRESULT (INT32 ButtonChangeKind)

Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO. Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).

#### put_DisplayRect 

Defina o DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

> Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)

#### put_FrameId 

Defina o Frameid do evento ponteiro.

> [put_FrameId](#put_frameid)público HRESULT (UINT32 frameid)

Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_HimetricLocation 

Defina o HimetricLocation do evento ponteiro.

> público HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)

Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_HimetricLocationRaw 

Defina o HimetricLocationRaw do evento ponteiro.

> público HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)

Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_HistoryCount 

Defina o HistoryCount do evento ponteiro.

> público HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)

Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_InputData 

Defina o InputData do evento ponteiro.

> [put_InputData](#put_inputdata)público HRESULT (INT32 InputData)

Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_KeyStates 

Defina os Estados de um evento de ponteiro.

> público HRESULT [put_KeyStates](#put_keystates)(estado DWORD DWORD)

Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PenFlags 

Defina o PenFlags do evento ponteiro.

> público HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)

Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO. Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).

#### put_PenMask 

Defina o PenMask do evento ponteiro.

> público HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)

Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO. Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).

#### put_PenPressure 

Defina o PenPressure do evento ponteiro.

> público HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)

Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PenRotation 

Defina o PenRotation do evento ponteiro.

> público HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)

Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PenTiltX 

Defina o PenTiltX do evento ponteiro.

> [put_PenTiltX](#put_pentiltx)público HRESULT (INT32 PenTiltX)

Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PenTiltY 

Defina o PenTiltY do evento ponteiro.

> [put_PenTiltY](#put_pentilty)público HRESULT (INT32 PenTiltY)

Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PerformanceCount 

Defina o PerformanceCount do evento ponteiro.

> público HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)

Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PixelLocation 

Defina o PixelLocation do evento ponteiro.

> público HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)

Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PixelLocationRaw 

Defina o PixelLocationRaw do evento ponteiro.

> público HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)

Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PointerDeviceRect 

Defina o PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

> Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)

#### put_PointerFlags 

Defina o PointerFlags do evento ponteiro.

> público HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)

Isso corresponde à propriedade pointerFlags do struct POINTER_INFO. Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).

#### put_PointerId 

Defina a barra de ponteiros do evento ponteiro.

> [put_PointerId](#put_pointerid)público HRESULT (ponteiroid UINT32)

Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_PointerKind 

Defina o PointerKind do evento ponteiro.

> público HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)

Isso corresponde à propriedade pointerKind do struct POINTER_INFO. Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h). Suporta PT_PEN e PT_TOUCH.

#### put_Time 

Defina a hora do evento de ponteiro.

> [put_Time](#put_time)público HRESULT (tempo DWORD)

Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_TouchContact 

Defina o TouchContact do evento ponteiro.

> Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)

Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_TouchContactRaw 

Defina o TouchContactRaw do evento ponteiro.

> Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)

Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

#### put_TouchFlags 

Defina o TouchFlags do evento ponteiro.

> público HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)

Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO. Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).

#### put_TouchMask 

Defina o TouchMask do evento ponteiro.

> público HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)

Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO. Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).

#### put_TouchOrientation 

Defina o TouchOrientation do evento ponteiro.

> público HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)

Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).

#### put_TouchPressure 

Defina o TouchPressure do evento ponteiro.

> público HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)

Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

