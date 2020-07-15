---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: e98fdc74a229b90dd4474a1c0d2d18d32d22bd2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880679"
---
# 0.9.515-ICoreWebView2ExperimentalCompositionController de interface 

> [!NOTE]
> Esta é uma API experimental que é fornecida com a versão 0.9.488 do SDK de pré-lançamento.

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

Essa interface é uma extensão da interface ICoreWebView2Controller para dar suporte à hospedagem Visual.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[add_CursorChanged](#add_cursorchanged) | Adicione um manipulador de eventos para o evento CursorChanged.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Uma função auxiliar para converter um ponteiroid recebido do sistema em um [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).
[get_Cursor](#get_cursor) | O cursor atual que o WebView imagina que deveria estar.
[get_RootVisualTarget](#get_rootvisualtarget) | O RootVisualTarget é um Visual na árvore visual do aplicativo de hospedagem.
[get_UIAProvider](#get_uiaprovider) | Retorna o provedor de automação da interface do usuário da WebView.
[put_RootVisualTarget](#put_rootvisualtarget) | Defina a propriedade RootVisualTarget.
[remove_CursorChanged](#remove_cursorchanged) | Remover um manipulador de eventos adicionado anteriormente com add_CursorChanged.
[SendMouseInput](#sendmouseinput) | Se eventKind for COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL ou COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especificará a quantidade de movimento da roda.
[SendPointerInput](#sendpointerinput) | O SendPointerInput aceita entrada de toque ou ponteiro de caneta de tipos definidos em COREWEBVIEW2_POINTER_EVENT_KIND.
[COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4) | Matriz que representa uma transformação 3D.
[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) | Tipo de evento de mouse usado pelo SendMouseInput para transmitir o tipo de evento de mouse sendo enviado ao WebView.
[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) | Teclas virtuais de evento de mouse associadas a um COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.
[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) | Tipo de evento ponteiro usado pelo SendPointerInput para transmitir o tipo de evento ponteiro sendo enviado ao WebView.

Um objeto que implementa a interface ICoreWebView2ExperimentalCompositionController também implementa ICoreWebView2Controller. Espera-se que os chamadores usem ICoreWebView2Controller para redimensionar, visibilidade, foco e assim por diante e, em seguida, usar o ICoreWebView2ExperimentalCompositionController para se conectar a uma árvore de composição e fornecer a entrada para o WebView.

## Parte

#### add_CursorChanged 

Adicione um manipulador de eventos para o evento CursorChanged.

> Public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) * EventHandler, EventRegistrationToken * token)

O evento é acionado quando o WebView pensa que o cursor deve ser alterado. Por exemplo, quando o cursor do mouse é o cursor padrão no momento, mas é movido sobre o texto, ele pode tentar mudar para o cursor IBeam.

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                       IUnknown* args) -> HRESULT {
                    HCURSOR cursor;
                    CHECK_FAILURE(sender->get_Cursor(&cursor));
                    SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                    return S_OK;
                })
                .Get(),
            &m_cursorChangedToken));
```

#### CreateCoreWebView2PointerInfoFromPointerId 

Uma função auxiliar para converter um ponteiroid recebido do sistema em um [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).

> Public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(ponteiroid uint, HWND ParentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * * pointerInfo)

parentWindow é o HWND que contém o WebView. Isso pode ser qualquer HWND na árvore HWND que contém o WebView. O COREWEBVIEW2_MATRIX_4X4 é a transformação daquele HWND para o WebView. O [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) retornado é usado no SendPointerInfo. O tipo de ponteiro deve ser Pen ou touch, ou a função falhará.



#### get_Cursor 

O cursor atual que o WebView imagina que deveria estar.

> público HRESULT [get_Cursor](#get_cursor)(hCursor * cursor)

O cursor deve ser definido em WM_SETCURSOR por meio de:: SetCursor ou definido no HWND pai/ancestral correspondente da WebView a:: SetClassLongPtr. O HCURSOR pode ser liberado para que CopyCursor/DestroyCursor seja recomendado para manter sua própria cópia se você estiver fazendo mais do que configurar imediatamente o cursor.

#### get_RootVisualTarget 

O RootVisualTarget é um Visual na árvore visual do aplicativo de hospedagem.

> público HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown * * destino)

Esse visual é onde o WebView irá conectar sua árvore visual. O aplicativo usa esse visual para posicionar a WebView dentro do aplicativo. O aplicativo ainda precisa usar a propriedade Bounds para dimensionar o WebView. A propriedade RootVisualTarget pode ser uma IDCompositionVisual ou uma Windows:: UI:: composição:: ContainerVisual. O WebView irá conectar sua árvore visual ao Visual fornecido antes de retornar do setter da propriedade. O aplicativo precisa confirmar seu dispositivo definindo a propriedade RootVisualTarget. A propriedade RootVisualTarget dá suporte a ser definida como nullptr para desconectar o WebView da árvore visual do aplicativo. 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### get_UIAProvider 

Retorna o provedor de automação da interface do usuário da WebView.

> público HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown * * provedor)

#### put_RootVisualTarget 

Defina a propriedade RootVisualTarget.

> público HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown * destino)

#### remove_CursorChanged 

Remover um manipulador de eventos adicionado anteriormente com add_CursorChanged.

> [remove_CursorChanged](#remove_cursorchanged)público HRESULT (token EventRegistrationToken)

#### SendMouseInput 

Se eventKind for COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL ou COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especificará a quantidade de movimento da roda.

> Public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, Point Point)

Um valor positivo indica que a roda foi girada para frente, longe do usuário; um valor negativo indica que a roda foi girada para trás, em direção ao usuário. Um clique em roda é definido como WHEEL_DELTA, que é 120. Se eventKind for COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN ou COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, então mouseData especificará quais botões X foram pressionados ou liberados. Esse valor deve ser 1 se o primeiro botão X for pressionado/liberado e 2 se o segundo botão X for pressionado/liberado. Se eventKind for COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, virtualKeys, mouseData e Point deverão ser zero. Se eventKind for qualquer outro valor, então mouseData deve ser zero. O ponto deve estar no espaço de coordenadas do cliente da WebView. Para acompanhar eventos do mouse que começam na WebView e podem ser movidos para fora do WebView e do aplicativo host, é recomendável chamar SetCapture e ReleaseCapture. Para descartar pop-ups de foco, também é recomendável enviar mensagens de WM_MOUSELEAVE. 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### SendPointerInput 

O SendPointerInput aceita entrada de toque ou ponteiro de caneta de tipos definidos em COREWEBVIEW2_POINTER_EVENT_KIND.

> Public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * pointerInfo)

Qualquer entrada de ponteiro do sistema deve ser convertida em um [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) primeiro.

#### COREWEBVIEW2_MATRIX_4X4 

Matriz que representa uma transformação 3D.

> typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)

Essa transformação é usada para calcular as coordenadas corretas ao chamar CreateCoreWebView2PointerInfoFromPointerId. Isso equivale a um D2D1_MATRIX_4X4_F

#### COREWEBVIEW2_MOUSE_EVENT_KIND 

Tipo de evento de mouse usado pelo SendMouseInput para transmitir o tipo de evento de mouse sendo enviado ao WebView.

> Enumeração [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL            | Evento de rolagem da roda horizontal do mouse, WM_MOUSEHWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK            | Botão esquerdo do mouse de clique duplo, WM_LBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN            | Botão esquerdo do mouse, evento WM_LBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP            | Botão esquerdo evento do mouse, WM_LBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE            | Evento Leave do mouse, WM_MOUSELEAVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK            | Botão do meio clique duas vezes em evento de mouse WM_MBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN            | Botão do meio evento do mouse, WM_MBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP            | Botão médio do evento do mouse, WM_MBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE            | Evento de movimentação do mouse, WM_MOUSEMOVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK            | Botão direito do mouse clique duas vezes em evento do mouse WM_RBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN            | Botão direito do mouse sobre o evento WM_RBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP            | Botão direito do mouse sobre o evento WM_RBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL            | Evento de rolagem da roda do mouse, WM_MOUSEWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK            | Primeiro ou segundo botão X clique duas vezes em evento do mouse WM_XBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN            | Botão do mouse sobre o botão primeiro ou segundo X desligado WM_XBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP            | O evento de mouse do primeiro ou segundo botão X para cima WM_XBUTTONUP.

Os valores desse enum são alinhados com as mensagens WM_ * da janela correspondente.

#### COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS 

Teclas virtuais de evento de mouse associadas a um COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.

> Enumeração [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE            | Nenhuma tecla adicional pressionada.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON            | O botão esquerdo do mouse está abaixo MK_LBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON            | O botão direito do mouse está abaixo MK_RBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT            | A tecla SHIFT está inativa, MK_SHIFT.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL            | A tecla CTRL está inoperante, MK_CONTROL.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON            | O botão do meio do mouse está baixo, MK_MBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1            | O primeiro botão X está baixo, MK_XBUTTON1.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2            | O segundo botão X está baixo, MK_XBUTTON2.

Esses valores podem ser combinados em um sinalizador de bit se mais de uma chave virtual for pressionada para o evento. Os valores dessa enumeração se alinham com as teclas de mouse MK_ * correspondentes.

#### COREWEBVIEW2_POINTER_EVENT_KIND 

Tipo de evento ponteiro usado pelo SendPointerInput para transmitir o tipo de evento ponteiro sendo enviado ao WebView.

> Enumeração [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE            | Corresponde a WM_POINTERACTIVATE.
COREWEBVIEW2_POINTER_EVENT_KIND_DOWN            | Corresponde a WM_POINTERDOWN.
COREWEBVIEW2_POINTER_EVENT_KIND_ENTER            | Corresponde a WM_POINTERENTER.
COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE            | Corresponde a WM_POINTERLEAVE.
COREWEBVIEW2_POINTER_EVENT_KIND_UP            | Corresponde a WM_POINTERUP.
COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE            | Corresponde a WM_POINTERUPDATE.

Os valores desse enum são alinhados com as mensagens WM_POINTER * da janela correspondente.

