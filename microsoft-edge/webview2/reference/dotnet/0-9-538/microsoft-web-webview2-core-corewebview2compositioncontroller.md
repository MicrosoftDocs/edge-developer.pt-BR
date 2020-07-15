---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2CompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2CompositionController
ms.openlocfilehash: 45ac5406cea804aa5b5db748cecaae7104dccb00
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878985"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2CompositionController 

> [!NOTE]
> Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Essa classe é uma extensão da classe CoreWebView2Controller para dar suporte à hospedagem Visual.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Cursor](#cursor) | O cursor atual que o WebView imagina que deveria estar.
[CursorChanged](#cursorchanged) | O evento é acionado quando o WebView pensa que o cursor deve ser alterado.
[RootVisualTarget](#rootvisualtarget) | O RootVisualTarget é um Visual na árvore visual do aplicativo de hospedagem.
[UIAProvider](#uiaprovider) | Retorna o provedor de automação da interface do usuário da WebView.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Uma função auxiliar para converter um ponteiroid recebido do sistema em um CoreWebView2ExperimentalPointerInfo.
[SendMouseInput](#sendmouseinput) | Se eventKind for CoreWebView2MouseEventKind. HorizontalWheel ou CoreWebView2MouseEventKind. wheel, mouseData especificará a quantidade de movimento da roda.
[SendPointerInput](#sendpointerinput) | SendPointerInput aceita entrada de ponteiro de toque ou caneta de tipos definidos em CoreWebView2PointerEventKind.

## Parte

#### Cursor 

O cursor atual que o WebView imagina que deveria estar.

> [cursor](#cursor) de IntPtr público

O cursor deve ser definido no WM_SETCURSOR pelo mouse. SetCursor ou definido no HWND pai/ancestral correspondente da WebView a SetClassLongPtr. O HCURSOR pode ser liberado para que CopyCursor/DestroyCursor seja recomendado para manter sua própria cópia se você estiver fazendo mais do que configurar imediatamente o cursor.

#### CursorChanged 

O evento é acionado quando o WebView pensa que o cursor deve ser alterado.

> objeto<-EventHandler de evento público > [CursorChanged](#cursorchanged)

Por exemplo, quando o cursor do mouse é o cursor padrão no momento, mas é movido sobre o texto, ele pode tentar mudar para o cursor IBeam.

#### RootVisualTarget 

O RootVisualTarget é um Visual na árvore visual do aplicativo de hospedagem.

> [RootVisualTarget](#rootvisualtarget) de objeto público

Esse visual é onde o WebView irá conectar sua árvore visual. O aplicativo usa esse visual para posicionar a WebView dentro do aplicativo. O aplicativo ainda precisa usar a propriedade Bounds para dimensionar o WebView. A propriedade RootVisualTarget pode ser uma IDCompositionVisual ou uma Windows:: UI:: composição:: ContainerVisual. O WebView irá conectar sua árvore visual ao Visual fornecido antes de retornar do setter da propriedade. O aplicativo precisa confirmar seu dispositivo definindo a propriedade RootVisualTarget. A propriedade RootVisualTarget dá suporte a ser definida como nullptr para desconectar o WebView da árvore visual do aplicativo.

#### UIAProvider 

Retorna o provedor de automação da interface do usuário da WebView.

> [UIAProvider](#uiaprovider) de objeto público

#### CreateCoreWebView2PointerInfoFromPointerId 

Uma função auxiliar para converter um ponteiroid recebido do sistema em um CoreWebView2ExperimentalPointerInfo.

> Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(Ponteiroid uint, IntPtr ParentWindow, Matrix4x4 Transform)

parentWindow é o HWND que contém o WebView. Isso pode ser qualquer HWND na árvore HWND que contém o WebView. O CoreWebView2Matrix4x4 é a transformação desse HWND para o WebView. O CoreWebView2ExperimentalPointerInfo retornado é usado no SendPointerInfo. O tipo de ponteiro deve ser Pen ou touch, ou a função falhará.

#### SendMouseInput 

Se eventKind for CoreWebView2MouseEventKind. HorizontalWheel ou CoreWebView2MouseEventKind. wheel, mouseData especificará a quantidade de movimento da roda.

> public void [SendMouseInput](#sendmouseinput)([CoreWebView2MouseEventKind](./namespace-microsoft-web-webview2-core.md) eventKind, [CoreWebView2MouseEventVirtualKeys](./namespace-microsoft-web-webview2-core.md) virtualKeys, uint mouseData, Point Point)

Um valor positivo indica que a roda foi girada para frente, longe do usuário; um valor negativo indica que a roda foi girada para trás, em direção ao usuário. Um clique em roda é definido como WHEEL_DELTA, que é 120. Se eventKind for CoreWebView2MouseEventKind. XButtonDoubleClick CoreWebView2MouseEventKind. XButtonDown ou CoreWebView2MouseEventKind. XButtonUp, mouseData especificará quais botões X foram pressionados ou liberados. Esse valor deve ser 1 se o primeiro botão X for pressionado/liberado e 2 se o segundo botão X for pressionado/liberado. Se eventKind for CoreWebView2MouseEventKind. leave, virtualKeys, mouseData e Point deverão ser zero. Se eventKind for qualquer outro valor, então mouseData deve ser zero. O ponto deve estar no espaço de coordenadas do cliente da WebView. Para acompanhar eventos do mouse que começam na WebView e podem ser movidos para fora do WebView e do aplicativo host, é recomendável chamar SetCapture e ReleaseCapture. Para descartar pop-ups de foco, também é recomendável enviar mensagens de WM_MOUSELEAVE.

#### SendPointerInput 

SendPointerInput aceita entrada de ponteiro de toque ou caneta de tipos definidos em CoreWebView2PointerEventKind.

> public void [SendPointerInput](#sendpointerinput)([CoreWebView2PointerEventKind](./namespace-microsoft-web-webview2-core.md) EventType, [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) pointerInfo)

Qualquer entrada de ponteiro do sistema deve ser convertida em um CoreWebView2ExperimentalPointerInfo primeiro.

