---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Host
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 39566c867c28739d21dd99c369d161d29a308946
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885615"
---
# 0.9.430-ICoreWebView2Host de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Host
  : public IUnknown
```

Essa interface é o proprietário do objeto CoreWebView2 e fornece suporte para redimensionar, mostrar e ocultar, enfocar e outras funcionalidades relacionadas à janela e composição.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsVisible](#get_isvisible) | A propriedade IsVisible Determina se deseja mostrar ou ocultar o WebView.
[put_IsVisible](#put_isvisible) | Defina a propriedade IsVisible.
[get_Bounds](#get_bounds) | Os limites da WebView.
[put_Bounds](#put_bounds) | Defina a propriedade Bounds.
[get_ZoomFactor](#get_zoomfactor) | O fator de zoom para o WebView.
[put_ZoomFactor](#put_zoomfactor) | Defina a propriedade ZoomFactor.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Adicione um manipulador de eventos para o evento ZoomFactorChanged.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Remover um manipulador de eventos adicionado anteriormente com add_ZoomFactorChanged.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Atualize as propriedades Bounds e ZoomFactor ao mesmo tempo.
[MoveFocus](#movefocus) | Mover o foco para o WebView.
[add_MoveFocusRequested](#add_movefocusrequested) | Adicione um manipulador de eventos para o evento MoveFocusRequested.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Remover um manipulador de eventos adicionado anteriormente com add_MoveFocusRequested.
[add_GotFocus](#add_gotfocus) | Adicione um manipulador de eventos para o evento GotFocus.
[remove_GotFocus](#remove_gotfocus) | Remover um manipulador de eventos adicionado anteriormente com add_GotFocus.
[add_LostFocus](#add_lostfocus) | Adicione um manipulador de eventos para o evento LostFocus.
[remove_LostFocus](#remove_lostfocus) | Remover um manipulador de eventos adicionado anteriormente com add_LostFocus.
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Adicione um manipulador de eventos para o evento AcceleratorKeyPressed.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Remover um manipulador de eventos adicionado anteriormente com add_AcceleratorKeyPressed.
[get_ParentWindow](#get_parentwindow) | A janela pai fornecida pelo aplicativo que este WebView usa para renderizar o conteúdo.
[put_ParentWindow](#put_parentwindow) | Defina a janela pai para o WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Esta é uma notificação separada da put_Bounds que informa ao WebView o HWND pai (ou qualquer ancestral) movido.
[Fechar](#close) | Fecha a WebView e limpa a instância do navegador subjacente.
[get_CoreWebView2](#get_corewebview2) | Obtém a CoreWebView2 associada a este CoreWebView2Host.
[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) | Motivo para mover o foco.
[CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind) | O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.
[CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status) | Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.

O CoreWebView2Host é proprietário do CoreWebView2 e, se todas as referências à CoreWebView2Host ficarem ausentes, o WebView será fechado.

## Parte

#### get_IsVisible 

A propriedade IsVisible Determina se deseja mostrar ou ocultar o WebView.

> [get_IsVisible](#get_isvisible)público HRESULT (bool * IsVisible)

Se IsVisible estiver definido como false, o WebView será transparente e não será renderizado. No entanto, isso não afetará a janela que contém o WebView (o parâmetro HWND que foi passado para CreateCoreWebView2Host). Se você quiser que essa janela desapareça também, chame o recurso de janela diretamente, além de modificar a propriedade IsVisible. A WebView como uma janela filho não obterá mensagens de janela quando a janela superior for minimizada ou restaurada. Por motivo de desempenho, o desenvolvedor deve definir a propriedade IsVisible do WebView como false quando a janela do aplicativo é minimizada e retomada como true quando a janela do aplicativo for restaurada. A janela do aplicativo pode fazer isso ao manipular SC_MINIMIZE e SC_RESTORE comando ao receber WM_SYSCOMMAND mensagem.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_host->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_host->put_IsVisible(m_isVisible);
}
```

#### put_IsVisible 

Defina a propriedade IsVisible.

> público HRESULT [put_IsVisible](#put_isvisible)(bool IsVisible)

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_host->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_host->put_IsVisible(TRUE);
            }
        }
    }
```

#### get_Bounds 

Os limites da WebView.

> Associação Pública HRESULT [get_Bounds](#get_bounds)(Rect *)

Os limites são relativos ao HWND pai. O aplicativo tem duas maneiras de posicionar um WebView:

1. Crie um HWND filho que seja o HWND pai do WebView. Posicione esta janela onde o WebView deve estar. Nesse caso, use (0, 0) para o canto superior esquerdo Bound's do WebView (o deslocamento).

1. Use a janela mais superior do aplicativo como o HWND pai do WebView. Defina o Bound's canto superior esquerdo da WebView para que o WebView esteja posicionado corretamente no aplicativo. Os valores do limite estão no espaço de coordenadas do host.

#### put_Bounds 

Defina a propriedade Bounds.

> [put_Bounds](#put_bounds)público HRESULT (limites Rect)

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_host->put_Bounds(desiredBounds);
}
```

#### get_ZoomFactor 

O fator de zoom para o WebView.

> público HRESULT [get_ZoomFactor](#get_zoomfactor)(duplo * ZoomFactor)

Observe que a alteração do fator de zoom pode fazer com que o `window.innerWidth/innerHeight` layout da página seja alterado. Um fator de zoom aplicado pelo host chamando put_ZoomFactor se torna o novo zoom padrão para o WebView. Esse fator de zoom se aplica a navegações e é o fator de zoom que é retornado quando o usuário pressiona Ctrl + 0. Quando o fator de zoom é alterado pelo usuário (resultante do aplicativo que recebe ZoomFactorChanged), esse zoom se aplica apenas à página atual. O zoom aplicado pelo usuário é somente para a página atual e é redefinido em uma navegação. Não é permitido especificar um zoomFactor menor ou igual a 0. WebView também tem um intervalo de fator de zoom interno com suporte. Quando um fator de zoom especificado estiver fora desse intervalo, ele será normalizado para estar dentro do intervalo, e um evento ZoomFactorChanged será acionado para o fator de zoom aplicado real. Quando essa faixa de normalização acontece, a propriedade ZoomFactor relata o fator de zoom especificado durante a modificação anterior da propriedade ZoomFactor até que o evento ZoomFactorChanged seja recebido após o WebView se aplicar o fator de zoom normalizado.

#### put_ZoomFactor 

Defina a propriedade ZoomFactor.

> público HRESULT [put_ZoomFactor](#put_zoomfactor)(ZoomFactor duplo)

#### add_ZoomFactorChanged 

Adicione um manipulador de eventos para o evento ZoomFactorChanged.

> Public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

O evento é acionado quando a propriedade ZoomFactor da WebView é alterada. O evento pode ser acionado porque o chamador modificou a propriedade ZoomFactor ou porque o usuário modificou manualmente o zoom. Quando ela é modificada pelo chamador por meio da propriedade ZoomFactor, o fator de zoom interno é atualizado imediatamente e não haverá um evento ZoomFactorChanged. O WebView associa o último fator de zoom usado para cada site. Portanto, é possível que o fator de zoom mude ao navegar para uma página diferente. Quando o fator de zoom muda devido a isso, o evento ZoomFactorChanged é acionado logo após o evento ContentLoading.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_host->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Host* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### remove_ZoomFactorChanged 

Remover um manipulador de eventos adicionado anteriormente com add_ZoomFactorChanged.

> [remove_ZoomFactorChanged](#remove_zoomfactorchanged)público HRESULT (token EventRegistrationToken)

#### SetBoundsAndZoomFactor 

Atualize as propriedades Bounds e ZoomFactor ao mesmo tempo.

> Public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(limites Rect, zoomFactor duplo)

Esta operação é atômica a partir da perspecry do host. Após retornar dessa função, as propriedades Bounds e ZoomFactor terão ambos sido atualizadas se a função for bem-sucedida ou nenhuma será atualizada se a função falhar. Se os limites e ZoomFactor forem atualizados com a mesma escala (ou seja, os limites e ZoomFactor forem ambos duplicados), a página não verá uma alteração em Window. innerWidth/innerHeight e o WebView renderizará o conteúdo no novo tamanho e será aplicado sem renderizações intermediárias. Essa função também pode ser usada para atualizar apenas um de ZoomFactor ou limites passando o novo valor para um e o valor atual para o outro.

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_host->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_host->SetBoundsAndZoomFactor(bounds, scale);
}
```

#### MoveFocus 

Mover o foco para o WebView.

> Public HRESULT [MoveFocus](#movefocus)(motivo[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) )

O WebView receberá o foco e o foco será definido como elemento correspondente na página hospedada na WebView. Para motivo programático, o foco é definido como elemento prefoco anteriormente ou o elemento padrão se não houver nenhum elemento focalizado anteriormente. Para o próximo motivo, o foco é definido como o primeiro elemento. Para o motivo anterior, o foco é definido como o último elemento. A WebView também pode ter o foco por meio da interação do usuário, como clicar em um WebView ou Tab. Para tabulação, o aplicativo pode chamar MoveFocus com o próximo ou o anterior para alinhar-se com Tab e Shift + Tab, respectivamente, quando decide que o WebView é o próximo elemento que pode ser tabulado. Ou, o aplicativo pode chamar IsDialogMessage como parte de seu loop de mensagem para permitir que a plataforma manipule a Tabulação automaticamente. A plataforma irá girar por todas as janelas com WS_TABSTOP. Quando a WebView se concentrar no IsDialogMessage, o foco será inserido internamente no primeiro ou último elemento para Tab e Shift + Tab respectivamente.

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (int i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### add_MoveFocusRequested 

Adicione um manipulador de eventos para o evento MoveFocusRequested.

> Public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

MoveFocusRequested é acionado quando o usuário tenta Tab no WebView. O foco da WebView não mudou quando esse evento é acionado.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_host->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    CORE_WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### remove_MoveFocusRequested 

Remover um manipulador de eventos adicionado anteriormente com add_MoveFocusRequested.

> [remove_MoveFocusRequested](#remove_movefocusrequested)público HRESULT (token EventRegistrationToken)

#### add_GotFocus 

Adicione um manipulador de eventos para o evento GotFocus.

> Public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

GotFocus é acionado quando o WebView tem foco.

#### remove_GotFocus 

Remover um manipulador de eventos adicionado anteriormente com add_GotFocus.

> [remove_GotFocus](#remove_gotfocus)público HRESULT (token EventRegistrationToken)

#### add_LostFocus 

Adicione um manipulador de eventos para o evento LostFocus.

> Public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

LostFocus é acionado quando o WebView perdeu o foco. No caso em que o evento MoveFocusRequested é acionado, o foco continua no WebView quando o evento MoveFocusRequested é acionado. O foco perdido só será acionado depois que o código do aplicativo ou a ação padrão do conjunto de eventos MoveFocusRequested se concentrar em uma exibição de exibição ausente.

#### remove_LostFocus 

Remover um manipulador de eventos adicionado anteriormente com add_LostFocus.

> [remove_LostFocus](#remove_lostfocus)público HRESULT (token EventRegistrationToken)

#### add_AcceleratorKeyPressed 

Adicione um manipulador de eventos para o evento AcceleratorKeyPressed.

> Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) * EventHandler, EventRegistrationToken * token)

AcceleratorKeyPressed é acionado quando uma tecla de aceleração ou combinação de teclas é pressionada ou lançada enquanto o WebView está focalizado. Uma tecla é considerada um acelerador se:

1. A tecla CTRL ou Alt está sendo mantida no momento ou

1. a tecla pressionada não é mapeada para um caractere. Algumas teclas específicas nunca são consideradas aceleradores, como Shift. A tecla escape é sempre considerada um acelerador.

Os eventos chave repetido com repetição causada pela manutenção da tecla para baixo também acionarão esse evento. Você pode filtrá-los verificando os argumentos do evento KeyEventLParam ou PhysicalKeyStatus.

No modo de janela, esse manipulador de eventos é chamado sincronicamente. Até que você chame Handle () nos argumentos do evento ou o manipulador de eventos seja retornado, o processo do navegador será bloqueado e as chamadas COM saída cruzada de processo não funcionarão com RPC_E_CANTCALLOUT_ININPUTSYNCCALL. No entanto, todos os métodos de API CoreWebView2 funcionarão.

No modo sem janela, o manipulador de eventos é chamado de forma assíncrona. A entrada adicional não entrará em contato com o navegador até que o manipulador de eventos retorne ou manipule () seja chamado, mas o processo do navegador em si não será bloqueado, e as chamadas COM de saída funcionarão normalmente.

É recomendável chamar Handle (TRUE), como o mais cedo possível, se souber que deseja manipular a tecla aceleradora.

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_host->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                CORE_WEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        CORE_WEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### remove_AcceleratorKeyPressed 

Remover um manipulador de eventos adicionado anteriormente com add_AcceleratorKeyPressed.

> [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)público HRESULT (token EventRegistrationToken)

#### get_ParentWindow 

A janela pai fornecida pelo aplicativo que este WebView usa para renderizar o conteúdo.

> Public HRESULT [get_ParentWindow](#get_parentwindow)(HWND * topLevelWindow)

Esta API inicialmente retorna a janela passada para CreateCoreWebView2Host.

#### put_ParentWindow 

Defina a janela pai para o WebView.

> [put_ParentWindow](#put_parentwindow)público HRESULT (HWND topLevelWindow)

Isso fará com que o WebView retenha o pai da janela para a janela recém fornecida.

#### NotifyParentWindowPositionChanged 

Esta é uma notificação separada da put_Bounds que informa ao WebView o HWND pai (ou qualquer ancestral) movido.

> Public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Isso é necessário para acessibilidade e determinadas caixas de diálogo no WebView para funcionar corretamente. 

```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_host->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### Fechar 

Fecha a WebView e limpa a instância do navegador subjacente.

> público HRESULT [fechar](#close)()

A limpeza do navegador instace liberará os recursos que reabrirão o WebView. A instância do navegador será encerrada se não houver outros webviews que o usam.

Depois de chamar Close, todas as chamadas de método falharão e os manipuladores de eventos deixarão de ser acionados. Especificamente, a WebView liberará suas referências a seus manipuladores de eventos quando Close for chamado.

Fechar é chamado implicitamente quando o CoreWebView2Host perde sua referência final e é destruido. Mas é uma prática recomendada chamar o fechamento explicitamente para evitar qualquer ciclo acidental de referências entre o WebView e o código do aplicativo. Especificamente, se você capturar uma referência ao WebView em um manipulador de eventos, criará um ciclo de referência entre o WebView e o manipulador de eventos. Chamar Close irá interromper esse ciclo liberando todos os manipuladores de eventos. Mas para evitar essa situação, é recomendável que a chamada seja fechada explicitamente no WebView e não Capture uma referência para o WebView para garantir que o WebView possa ser limpo corretamente.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_host)
    {
        m_host->Close();
        m_host = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2.idl#createwebview2environmentwithdetails
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instnaces.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### get_CoreWebView2 

Obtém a CoreWebView2 associada a este CoreWebView2Host.

> Public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) * * CoreWebView2)

#### CORE_WEBVIEW2_MOVE_FOCUS_REASON 

Motivo para mover o foco.

> Enumeração [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | Configuração de código focalizada no WebView.
CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Movendo o foco devido à guia passagem para frente.
CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Movendo o foco devido a Tabulação de passagem para trás.

#### CORE_WEBVIEW2_KEY_EVENT_KIND 

O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.

> Enumeração [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN            | Corresponde à mensagem do Window WM_KEYDOWN.
CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP            | Corresponde à mensagem do Window WM_KEYUP.
CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN            | Corresponde à mensagem do Window WM_SYSKEYDOWN.
CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP            | Corresponde à mensagem do Window WM_SYSKEYUP.

#### CORE_WEBVIEW2_PHYSICAL_KEY_STATUS 

Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.

> typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)

Consulte a documentação do WM_KEYDOWN para obter detalhes em[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)

