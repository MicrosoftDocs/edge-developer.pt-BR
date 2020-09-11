---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 9ce4c9c3f076d54f03295ffda84c5fb0f03b4166
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010898"
---
# classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Isso basicamente representa um objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combinado.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[ButtonChangeKind](#buttonchangekind) | O ButtonChangeKind do evento de ponteiro.
[DisplayRect](#displayrect) | O DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).
[Frameid](#frameid) | O Frameid do evento ponteiro.
[HimetricLocation](#himetriclocation) | O HimetricLocation do evento de ponteiro.
[HimetricLocationRaw](#himetriclocationraw) | O HimetricLocationRaw do evento de ponteiro.
[HistoryCount](#historycount) | O HistoryCount do evento de ponteiro.
[InputData](#inputdata) | O InputData do evento de ponteiro.
[Estado da subsessão](#keystates) | O estado do evento ponteiro.
[PenFlags](#penflags) | O PenFlags do evento de ponteiro.
[PenMask](#penmask) | O PenMask do evento de ponteiro.
[PenPressure](#penpressure) | O PenPressure do evento de ponteiro.
[PenRotation](#penrotation) | O PenRotation do evento de ponteiro.
[PenTiltX](#pentiltx) | O PenTiltX do evento de ponteiro.
[PenTiltY](#pentilty) | O PenTiltY do evento de ponteiro.
[PerformanceCount](#performancecount) | O PerformanceCount do evento de ponteiro.
[PixelLocation](#pixellocation) | O PixelLocation do evento de ponteiro.
[PixelLocationRaw](#pixellocationraw) | O PixelLocationRaw do evento de ponteiro.
[PointerDeviceRect](#pointerdevicerect) | O PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).
[PointerFlags](#pointerflags) | O PointerFlags do evento de ponteiro.
[Ponteiroid](#pointerid) | O Ponteiroid do evento ponteiro.
[PointerKind](#pointerkind) | O PointerKind do evento de ponteiro.
[Hora](#time) | A hora do evento de ponteiro.
[TouchContact](#touchcontact) | O TouchContact do evento de ponteiro.
[TouchContactRaw](#touchcontactraw) | O TouchContactRaw do evento de ponteiro.
[TouchFlags](#touchflags) | O TouchFlags do evento de ponteiro.
[TouchMask](#touchmask) | O TouchMask do evento de ponteiro.
[TouchOrientation](#touchorientation) | O TouchOrientation do evento de ponteiro.
[TouchPressure](#touchpressure) | O TouchPressure do evento de ponteiro.

## Parte

#### ButtonChangeKind 

O ButtonChangeKind do evento de ponteiro.

> public int [ButtonChangeKind](#buttonchangekind)

Isso corresponde à propriedade ButtonChangeKind do struct POINTER_INFO. Os valores são definidos pela enumeração POINTER_BUTTON_CHANGE_KIND no SDK do Windows (WinUser. h).

#### DisplayRect 

O DisplayRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

> Public Rect [DisplayRect](#displayrect)

#### Frameid 

O Frameid do evento ponteiro.

> [frameid](#frameid) uint público

Isso corresponde à propriedade frameid do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### HimetricLocation 

O HimetricLocation do evento de ponteiro.

> [HimetricLocation](#himetriclocation) de ponto público

Isso corresponde à propriedade ptHimetricLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### HimetricLocationRaw 

O HimetricLocationRaw do evento de ponteiro.

> [HimetricLocationRaw](#himetriclocationraw) de ponto público

Isso corresponde à propriedade ptHimetricLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### HistoryCount 

O HistoryCount do evento de ponteiro.

> Public uint [HistoryCount](#historycount)

Isso corresponde à propriedade historyCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### InputData 

O InputData do evento de ponteiro.

> public int [InputData](#inputdata)

Isso corresponde à propriedade InputData do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### Estado da subsessão 

O estado do evento ponteiro.

> [Estados](#keystates) uint públicos

Isso corresponde à propriedade dwKeyStates do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### PenFlags 

O PenFlags do evento de ponteiro.

> Public uint [PenFlags](#penflags)

Isso corresponde à propriedade penFlags do struct POINTER_PEN_INFO. Os valores são definidos pelas constantes PEN_FLAGS no SDK do Windows (WinUser. h).

#### PenMask 

O PenMask do evento de ponteiro.

> Public uint [PenMask](#penmask)

Isso corresponde à propriedade penMask do struct POINTER_PEN_INFO. Os valores são definidos pelas constantes PEN_MASK no SDK do Windows (WinUser. h).

#### PenPressure 

O PenPressure do evento de ponteiro.

> Public uint [PenPressure](#penpressure)

Isso corresponde à propriedade pressão do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### PenRotation 

O PenRotation do evento de ponteiro.

> Public uint [PenRotation](#penrotation)

Isso corresponde à propriedade Rotation do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### PenTiltX 

O PenTiltX do evento de ponteiro.

> public int [PenTiltX](#pentiltx)

Isso corresponde à propriedade tiltX do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### PenTiltY 

O PenTiltY do evento de ponteiro.

> public int [PenTiltY](#pentilty)

Isso corresponde à propriedade inclinação do struct POINTER_PEN_INFO conforme definido no SDK do Windows (WinUser. h).

#### PerformanceCount 

O PerformanceCount do evento de ponteiro.

> [PerformanceCountdor](#performancecount) ULONG público

Isso corresponde à propriedade PerformanceCount do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### PixelLocation 

O PixelLocation do evento de ponteiro.

> [PixelLocation](#pixellocation) de ponto público

Isso corresponde à propriedade ptPixelLocation do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### PixelLocationRaw 

O PixelLocationRaw do evento de ponteiro.

> [PixelLocationRaw](#pixellocationraw) de ponto público

Isso corresponde à propriedade ptPixelLocationRaw do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### PointerDeviceRect 

O PointerDeviceRect da propriedade sourceDevice do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

> Public Rect [PointerDeviceRect](#pointerdevicerect)

#### PointerFlags 

O PointerFlags do evento de ponteiro.

> Public uint [PointerFlags](#pointerflags)

Isso corresponde à propriedade pointerFlags do struct POINTER_INFO. Os valores são definidos pelas constantes POINTER_FLAGS no SDK do Windows (WinUser. h).

#### Ponteiroid 

O Ponteiroid do evento ponteiro.

> Ponteiro de [ponteiro](#pointerid) uint público

Isso corresponde à propriedade pointerid da estrutura POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### PointerKind 

O PointerKind do evento de ponteiro.

> Public uint [PointerKind](#pointerkind)

Isso corresponde à propriedade pointerKind do struct POINTER_INFO. Os valores são definidos pela enumeração POINTER_INPUT_KIND no SDK do Windows (WinUser. h). Suporta PT_PEN e PT_TOUCH.

#### Hora 

A hora do evento de ponteiro.

> [hora](#time) do uint público

Isso corresponde à propriedade dwTime do struct POINTER_INFO conforme definido no SDK do Windows (WinUser. h).

#### TouchContact 

O TouchContact do evento de ponteiro.

> Public Rect [TouchContact](#touchcontact)

Isso corresponde à propriedade rcContact do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

#### TouchContactRaw 

O TouchContactRaw do evento de ponteiro.

> Public Rect [TouchContactRaw](#touchcontactraw)

Isso corresponde à propriedade rcContactRaw do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

#### TouchFlags 

O TouchFlags do evento de ponteiro.

> Public uint [TouchFlags](#touchflags)

Isso corresponde à propriedade touchFlags do struct POINTER_TOUCH_INFO. Os valores são definidos pelas constantes TOUCH_FLAGS no SDK do Windows (WinUser. h).

#### TouchMask 

O TouchMask do evento de ponteiro.

> Public uint [TouchMask](#touchmask)

Isso corresponde à propriedade touchMask do struct POINTER_TOUCH_INFO. Os valores são definidos pelas constantes TOUCH_MASK no SDK do Windows (WinUser. h).

#### TouchOrientation 

O TouchOrientation do evento de ponteiro.

> Public uint [TouchOrientation](#touchorientation)

Isso corresponde à Propriedade Orientation do POINTER_TOUCH_INFO struct conforme definido no SDK do Windows (WinUser. h).

#### TouchPressure 

O TouchPressure do evento de ponteiro.

> Public uint [TouchPressure](#touchpressure)

Isso corresponde à propriedade pressão do struct POINTER_TOUCH_INFO conforme definido no SDK do Windows (WinUser. h).

