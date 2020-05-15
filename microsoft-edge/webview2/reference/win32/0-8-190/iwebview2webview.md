---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 5c84cfb703c8901560307b7bba8bc7887cb19377
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652354"
---
# interface IWebView2WebView 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebView
  : public IUnknown
```

O WebView2 permite que você hospede conteúdo da Web usando a tecnologia de navegador da Web mais recente do Edge.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | O objeto [IWebView2Settings](IWebView2Settings.md) contém várias configurações modificáveis para a execução do WebView.
[get_Source](#get_source) | O URI do documento de nível superior atual.
[Navegar](#navigate) | Fazer uma navegação do documento de nível superior para o URI especificado.
[MoveFocus](#movefocus) | Mover o foco para o WebView.
[NavigateToString](#navigatetostring) | Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.
[add_NavigationStarting](#add_navigationstarting) | Adicione um manipulador de eventos para o evento NavigationStarting.
[remove_NavigationStarting](#remove_navigationstarting) | Remover um manipulador de eventos adicionado anteriormente com add_NavigationStarting.
[add_DocumentStateChanged](#add_documentstatechanged) | Adicione um manipulador de eventos para o evento DocumentStateChanged.
[remove_DocumentStateChanged](#remove_documentstatechanged) | Remover um manipulador de eventos adicionado anteriormente com add_DocumentStateChanged.
[add_NavigationCompleted](#add_navigationcompleted) | Adicione um manipulador de eventos para o evento NavigationCompleted.
[remove_NavigationCompleted](#remove_navigationcompleted) | Remover um manipulador de eventos adicionado anteriormente com add_NavigationCompleted.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Adicione um manipulador de eventos para o evento FrameNavigationStarting.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationStarting.
[add_MoveFocusRequested](#add_movefocusrequested) | Adicione um manipulador de eventos para o evento MoveFocusRequested.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Remover um manipulador de eventos adicionado anteriormente com add_MoveFocusRequested.
[add_GotFocus](#add_gotfocus) | Adicione um manipulador de eventos para o evento GotFocus.
[remove_GotFocus](#remove_gotfocus) | Remover um manipulador de eventos adicionado anteriormente com add_GotFocus.
[add_LostFocus](#add_lostfocus) | Adicione um manipulador de eventos para o evento LostFocus.
[remove_LostFocus](#remove_lostfocus) | Remover um manipulador de eventos adicionado anteriormente com add_LostFocus.
[add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated) | Esta API será preterida, use a nova API de add_WebResourceRequested.
[remove_WebResourceRequested](#remove_webresourcerequested) | Remover um manipulador de eventos adicionado anteriormente com add_WebResourceRequested.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Adicione um manipulador de eventos para o evento ScriptDialogOpening.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Remover um manipulador de eventos adicionado anteriormente com add_ScriptDialogOpening.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Adicione um manipulador de eventos para o evento ZoomFactorChanged.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Remover um manipulador de eventos adicionado anteriormente com add_ZoomFactorChanged.
[add_PermissionRequested](#add_permissionrequested) | Adicione um manipulador de eventos para o evento PermissionRequested.
[remove_PermissionRequested](#remove_permissionrequested) | Remover um manipulador de eventos adicionado anteriormente com add_PermissionRequested.
[add_ProcessFailed](#add_processfailed) | Adicione um manipulador de eventos para o evento ProcessFailed.
[remove_ProcessFailed](#remove_processfailed) | Remover um manipulador de eventos adicionado anteriormente com add_ProcessFailed.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated.
[ExecuteScript](#executescript) | Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.
[CapturePreview](#capturepreview) | Capture uma imagem do que o WebView está exibindo.
[Recarregar](#reload) | Recarregar a página atual.
[get_Bounds](#get_bounds) | Os limites da WebView.
[put_Bounds](#put_bounds) | Defina a propriedade Bounds.
[get_ZoomFactor](#get_zoomfactor) | O fator de zoom para a página atual no WebView.
[put_ZoomFactor](#put_zoomfactor) | Defina a propriedade ZoomFactor.
[get_IsVisible](#get_isvisible) | A propriedade IsVisible Determina se deseja mostrar ou ocultar o WebView.
[put_IsVisible](#put_isvisible) | Defina a propriedade IsVisible.
[PostWebMessageAsJson](#postwebmessageasjson) | Poste a WebMessage especificada no documento de nível superior neste [IWebView2WebView]().
[PostWebMessageAsString](#postwebmessageasstring) | Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.
[add_WebMessageReceived](#add_webmessagereceived) | Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Remover um manipulador de eventos adicionado anteriormente com add_WebMessageReceived.
[Fechar](#close) | Fecha a WebView e limpa a instância do navegador subjacente.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Chame um método DevToolsProtocol assíncrono.
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | Assine um evento DevToolsProtocol.
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Remover um manipulador de eventos adicionado anteriormente com add_DevToolsProtocolEventReceived.
[get_BrowserProcessId](#get_browserprocessid) | A ID do processo do navegador que hospeda o WebView.
[get_CanGoBack](#get_cangoback) | Pode navegar pelo WebView para a página anterior no histórico de navegação.
[get_CanGoForward](#get_cangoforward) | Pode navegar pelo WebView para a próxima página no histórico de navegação.
[GoBack](#goback) | Navega o WebView para a página anterior no histórico de navegação.
[GoForward](#goforward) | Navega o WebView para a próxima página no histórico de navegação.
[WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) | Formato de imagem usado pelo método [IWebView2WebView:: CapturePreview](#capturepreview) .
[WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) | Tipo de caixa de diálogo JavaScript usada na interface [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .
[WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) | Tipo de falha de processo usada na interface [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .
[WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) | O tipo de uma solicitação de permissão.
[WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) | Resposta a uma solicitação de permissão.
[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) | Motivo para mover o foco.
[WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) | Valores de status de erro para navegações na Web.
[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) | Enumeração para contextos de solicitação de recurso da Web.

## Eventos de navegação

A sequência normal de eventos de navegação é NavigationStarting, DocumentStateChanged e NavigationCompleted.

![Dot-inline-dotgraph-1. png](media/dot-inline-dotgraph-1.png)

Observe que isso se destina a eventos de navegação com o mesmo evento Navigationid ARG. Navegação eventos com diferentes args de eventos Navigationid podem sobrepor-se. Por exemplo, se você iniciar um evento de navegação e, em seguida, iniciar uma outra navegação, verá o NavigationStarting para a primeira navegação acompanhada pela NavigationStarting da segunda navegação, seguida da NavigationCompleted para a primeira navegação e, em seguida, todos os demais eventos de navegação apropriados para a segunda navegação. Em casos de erro, pode ou não ser um evento DocumentStateChanged dependendo se a navegação é continuada para uma página de erro. No caso de um redirecionamento HTTP, haverá vários eventos NavigationStarting em uma linha, com os seguintes, o sinalizador isredirect definido.

Para subquadros dentro do WebView, o único evento de navegação acionado é o evento NavigationStarting que fornece ao host a capacidade de bloquear as navegações do subquadro.

## Modelo de processo

O WebView2 usa o mesmo modelo de processo que o navegador da Web Edge. Há um processo do navegador Edge por diretório de dados do usuário especificado em uma sessão do usuário que servirá qualquer processo de chamadas do WebView2 que especifique esse diretório de dados do usuário. Isso significa que um processo do navegador Edge pode estar servindo vários processos de chamadas e um processo de chamada pode estar usando vários processos do navegador do Edge.

![Dot-inline-dotgraph-2. png](media/dot-inline-dotgraph-2.png)

Fora de um processo de navegador, haverá alguns processos de processamento. Elas são criadas, conforme necessário, para atender a vários quadros potencialmente em diferentes modos de exibição. O número de processos de renderização varia de acordo com o recurso de navegador de isolamento de site e o número de origens discadas discadas renderizadas em webviews associadas.

![Dot-inline-dotgraph-3. png](media/dot-inline-dotgraph-3.png)

Você pode reagir a falhas e travamentos nesses processos do navegador e do renderizador usando o evento ProcessFailure.

Você pode desligar com segurança os processos do navegador e do renderizador associados usando o método Close.

## Modelo de Threading

O WebView2 deve ser criado em um thread de interface do usuário. Especificamente um thread com um bombeamento de mensagem. Todos os retornos de chamada ocorrerão nesse thread e as chamadas para o WebView deverão ser feitas nesse thread. Não é seguro usar a WebView a partir de outro thread.

Os retornos de chamada, incluindo manipuladores de eventos e manipuladores de conclusão, são executados em série. Ou seja, se você tiver um manipulador de eventos em execução e iniciar um loop de mensagem, nenhum outro manipulador de eventos ou chamadas de retorno de conclusão começarão a ser executados de forma reentrada.

## Segurança

Sempre verifique a propriedade Source da WebView antes de usar ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString ou qualquer outro método para enviar informações para o WebView. A WebView pode ter navegado para outra página por meio do usuário final interagindo com a página ou o script na página que está causando a navegação. Da mesma forma, tenha muito cuidado com o AddScriptToExecuteOnDocumentCreated. Todas as navegações futuras executarão esse script e, se ele fornecer acesso às informações destinadas apenas a determinada origem, qualquer documento HTML poderá ter acesso.

Ao examinar o resultado de uma chamada de método ExecuteScript, um evento WebMessageReceived, sempre verifique a fonte do remetente ou qualquer outro mecanismo de recebimento de informações de um documento HTML em uma WebView validar o URI do documento HTML é o que você espera.

Ao construir uma mensagem para enviar para um WebView, prefira usar PostWebMessageAsJson e construir o parâmetro de cadeia de caracteres JSON usando uma biblioteca JSON. Isso evitará possíveis acidentes de codificar informações em uma cadeia de caracteres ou script JSON e garantir que nenhuma entrada controlada pelo invasor possa modificar o restante da mensagem JSON ou executar um script arbitrário.

## Tipos de cadeias de caracteres

Parâmetros de cadeia de caracteres de saída são cadeias de caracteres de terminação NULL O chamado aloca a cadeia de caracteres usando CoTaskMemAlloc. A propriedade é transferida para o chamador e fica até o chamador liberar a memória usando o CoTaskMemFree.

Cadeias de caracteres em parâmetros são cadeias de caracteres terminadas LPCWSTR nulas. O chamador garante que a cadeia de caracteres é válida para a duração da chamada de função síncrona. Se o chamador precisa reter esse valor para algum ponto após a conclusão da chamada de função, o Calle deve alocar sua própria cópia do valor da cadeia de caracteres.

## Análise de URI e JSON

Vários métodos fornecem ou aceitam URIs e JSON como cadeias de caracteres. Use sua própria biblioteca preferida para analisar e gerar essas cadeias de caracteres.

Se o WinRT estiver disponível para seu aplicativo, você pode usar `RuntimeClass_Windows_Data_Json_JsonObject` e `IJsonObjectStatics` analisar ou produzir cadeias de caracteres JSON ou `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analisar e produzir URIs. Ambos trabalham em aplicativos Win32.

Se você usar o IUri e o CreateUri para analisar URIs, talvez queira usar os seguintes sinalizadores de criação de URI para que o comportamento de CreateUri corresponda melhor à análise de URI no WebView: `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## Depuração

Abra o DevTools com os atalhos normais: `F12` ou `Ctrl+Shift+I` . Você pode usar o `--auto-open-devtools-for-tabs` argumento de comando switch para que a janela do devtools seja aberta imediatamente ao criar a primeira vez uma WebView. Consulte a documentação de WebView para obter mais argumentos de linha de comando para o processo do navegador. Confira a chave do registro LoaderOverride para experimentar versões diferentes do WebView2 sem modificar seu aplicativo na documentação da WebView.

## Controle de versão

Depois de usar uma versão específica do SDK para criar seu aplicativo, seu aplicativo pode acabar sendo executado com uma versão mais antiga ou mais recente dos binários instalados do navegador. Até a versão 1.0.0.0 do WebView2, pode haver alterações significativas durante as atualizações que impedem que o SDK funcione com versões diferentes dos binários instalados do navegador. Após a versão 1.0.0.0 versões diferentes do SDK podem funcionar com versões diferentes do navegador instalado seguindo estas práticas recomendadas:

Para fazer a conta de alterações significativas na API, verifique se há uma falha ao chamar a DLL de exportação CreateWebView2Environment e ao chamar QueryInterface em qualquer objeto WebView2. Um valor de retorno de E_NOINTERFACE pode indicar que o SDK não é compatível com os binários do navegador Edge.

Verificar a falha de QueryInterface também contará em casos em que o SDK é mais recente do que a versão do navegador Edge e seu aplicativo tenta usar uma interface do qual o navegador Edge não reconhece.

Quando uma interface não está disponível, você pode considerar a possibilidade de desabilitar o recurso associado, se possível, ou informar ao usuário final que ele precisa atualizar o navegador.

## Parte

#### get_Settings 

O objeto [IWebView2Settings](IWebView2Settings.md) contém várias configurações modificáveis para a execução do WebView.

> público HRESULT [get_Settings](#get_settings)(configurações[IWebView2Settings](IWebView2Settings.md) * *)

#### get_Source 

O URI do documento de nível superior atual.

> [get_Source](#get_source)público HRESULT (URI LPWSTR *)

Esse valor potencialmente muda como parte do acionamento do evento DocumentStateChanged para alguns casos, como navegar para diferentes navegações em sites ou fragmentadores. Ele permanecerá o mesmo para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### Navegar 

Fazer uma navegação do documento de nível superior para o URI especificado.

> público- [navegação](#navigate)HRESULT (URI LPCWSTR)

Consulte os eventos de navegação para obter mais informações. Observe que isso iniciará uma navegação e o evento NavigationStarting correspondente será acionado algum tempo após a conclusão dessa chamada de navegação.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### MoveFocus 

Mover o foco para o WebView.

> Public HRESULT [MoveFocus](#movefocus)(motivo[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) )

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
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
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
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### NavigateToString 

Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.

> Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)

O parâmetro htmlContent não pode ter mais de 2 MB de caracteres. A origem da nova página será: em branco.

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### add_NavigationStarting 

Adicione um manipulador de eventos para o evento NavigationStarting.

> Public HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * token)

NavigationStarting é acionado quando o quadro principal do WebView está solicitando permissão para navegar para um URI diferente. Isso também será acionado para redirecionamentos.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
        }
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### remove_NavigationStarting 

Remover um manipulador de eventos adicionado anteriormente com add_NavigationStarting.

> [remove_NavigationStarting](#remove_navigationstarting)público HRESULT (token EventRegistrationToken)

#### add_DocumentStateChanged 

Adicione um manipulador de eventos para o evento DocumentStateChanged.

> Public HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

DocumentStateChanged é acionado quando o novo conteúdo começa a ser carregado no quadro principal do WebView ou se ocorre uma mesma navegação de página (por exemplo, por meio de navegações de fragmento ou de histórico. pushstate). Isso segue o evento NavigationStarting e precede o evento NavigationCompleted.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### remove_DocumentStateChanged 

Remover um manipulador de eventos adicionado anteriormente com add_DocumentStateChanged.

> [remove_DocumentStateChanged](#remove_documentstatechanged)público HRESULT (token EventRegistrationToken)

#### add_NavigationCompleted 

Adicione um manipulador de eventos para o evento NavigationCompleted.

> Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) * EventHandler, EventRegistrationToken * token)

O evento NavigationCompleted é acionado quando o WebView foi completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### remove_NavigationCompleted 

Remover um manipulador de eventos adicionado anteriormente com add_NavigationCompleted.

> [remove_NavigationCompleted](#remove_navigationcompleted)público HRESULT (token EventRegistrationToken)

#### add_FrameNavigationStarting 

Adicione um manipulador de eventos para o evento FrameNavigationStarting.

> Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * token)

FrameNavigationStarting é acionado quando um quadro filho na WebView solicita permissão para navegar para um URI diferente. Isso também será acionado para redirecionamentos.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### remove_FrameNavigationStarting 

Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationStarting.

> [remove_FrameNavigationStarting](#remove_framenavigationstarting)público HRESULT (token EventRegistrationToken)

#### add_MoveFocusRequested 

Adicione um manipulador de eventos para o evento MoveFocusRequested.

> Public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

MoveFocusRequested é acionado quando o usuário tenta Tab no WebView. O foco da WebView não mudou quando esse evento é acionado.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
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

> Public HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

GotFocus é acionado quando o WebView tem foco.

#### remove_GotFocus 

Remover um manipulador de eventos adicionado anteriormente com add_GotFocus.

> [remove_GotFocus](#remove_gotfocus)público HRESULT (token EventRegistrationToken)

#### add_LostFocus 

Adicione um manipulador de eventos para o evento LostFocus.

> Public HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

LostFocus é acionado quando o WebView perdeu o foco. No caso em que o evento MoveFocusRequested é acionado, o foco continua no WebView quando o evento MoveFocusRequested é acionado. O foco perdido só será acionado depois que o código do aplicativo ou a ação padrão do conjunto de eventos MoveFocusRequested se concentrar em uma exibição de exibição ausente.

#### remove_LostFocus 

Remover um manipulador de eventos adicionado anteriormente com add_LostFocus.

> [remove_LostFocus](#remove_lostfocus)público HRESULT (token EventRegistrationToken)

#### add_WebResourceRequested_deprecated 

Esta API será preterida, use a nova API de add_WebResourceRequested.

> Public HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR * const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) * const resourceContextFilter, size_t filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Adicione um manipulador de eventos para o evento WebResourceRequested. Acionado quando o WebView executa qualquer solicitação HTTP. Use urlFilter para passar uma lista com tamanho filterLength de URLs a serem escutadas. Cada entrada de URL também dá suporte a caracteres curinga: ' * ' corresponde a zero ou mais caracteres e '? ' corresponde exatamente a um caractere. Para cada entrada urlFilter, forneça um resourceContextFilter correspondente que representa os tipos de recursos para os quais o WebResourceRequested deve ser acionado. Se filterLength for 0, o evento será acionado para todas as solicitações de rede. Os contextos de recursos com suporte são: Document, StyleSheet, Image, Media, Font, script, XHR, Fetch.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### remove_WebResourceRequested 

Remover um manipulador de eventos adicionado anteriormente com add_WebResourceRequested.

> [remove_WebResourceRequested](#remove_webresourcerequested)público HRESULT (token EventRegistrationToken)

#### add_ScriptDialogOpening 

Adicione um manipulador de eventos para o evento ScriptDialogOpening.

> Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) * EventHandler, EventRegistrationToken * token)

O evento é acionado quando uma caixa de diálogo JavaScript (alerta, confirmação ou prompt) aparecerá para o WebView. Esse evento só será acionado se a propriedade IWebView2Settings:: AreDefaultScriptDialogsEnabled estiver definida como false.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### remove_ScriptDialogOpening 

Remover um manipulador de eventos adicionado anteriormente com add_ScriptDialogOpening.

> [remove_ScriptDialogOpening](#remove_scriptdialogopening)público HRESULT (token EventRegistrationToken)

#### add_ZoomFactorChanged 

Adicione um manipulador de eventos para o evento ZoomFactorChanged.

> Public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

O evento é acionado quando a propriedade ZoomFactor da WebView é alterada. O evento pode ser acionado porque o chamador modificou a propriedade ZoomFactor ou porque o usuário modificou manualmente o zoom. Quando ela é modificada pelo chamador por meio da propriedade ZoomFactor, o fator de zoom interno é atualizado imediatamente e não haverá um evento ZoomFactorChanged. O WebView associa o último fator de zoom usado para cada site. Portanto, é possível que o fator de zoom mude ao navegar para uma página diferente. Quando o fator de zoom muda devido a isso, o evento ZoomFactorChanged é acionado logo após o evento DocumentStateChanged.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
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

#### add_PermissionRequested 

Adicione um manipulador de eventos para o evento PermissionRequested.

> Public HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Acionado quando o conteúdo de uma WebView solicita permissão para acessar alguns recursos privilegiados.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Remover um manipulador de eventos adicionado anteriormente com add_PermissionRequested.

> [remove_PermissionRequested](#remove_permissionrequested)público HRESULT (token EventRegistrationToken)

#### add_ProcessFailed 

Adicione um manipulador de eventos para o evento ProcessFailed.

> Public HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Acionado quando um processo da WebView termina inesperadamente ou não responde.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### remove_ProcessFailed 

Remover um manipulador de eventos adicionado anteriormente com add_ProcessFailed.

> [remove_ProcessFailed](#remove_processfailed)público HRESULT (token EventRegistrationToken)

#### AddScriptToExecuteOnDocumentCreated 

Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.

> Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) * Handler)

O script injetado se aplicará a todas as futuras navegações de documento de nível superior e quadro filho até que sejam removidas com o RemoveScriptToExecuteOnDocumentCreated. Isso é aplicado de forma assíncrona e você deve aguardar até que o manipulador de conclusão seja executado antes de poder ter certeza de que o script está pronto para ser executado em navegações futuras.

Observe que, se um documento HTML tiver uma área restrita de algum tipo via propriedades de [área restrita](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) ou o [cabeçalho HTTP de política de segurança de conteúdo](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , isso afetará o script ser executado aqui. Portanto, por exemplo, se a palavra-chave ' allow-janelarestritas ' não estiver definida, as chamadas para a `alert` função serão ignoradas.

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### RemoveScriptToExecuteOnDocumentCreated 

Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated.

> Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID LPCWSTR)

#### ExecuteScript 

Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.

> Public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) * Handler)

Isso será executado de forma assíncrona e, quando concluída, se um manipulador for fornecido no parâmetro ExecuteScriptCompletedHandler, seu método Invoke será chamado com o resultado da avaliação do JavaScript fornecido. O valor do resultado é uma cadeia de caracteres codificada JSON. Se o resultado for indefinido, contiver um ciclo de referência ou não puder ser codificado em JSON, o valor NULL JSON será retornado como a cadeia de caracteres ' NULL '. Observe que uma função sem valor de retorno explícito retorna indefinida. Se o script executado lançar uma exceção não tratada, o resultado também será ' nulo '. Esse método é aplicado de forma assíncrona. Se a chamada for feita enquanto o WebView estiver em um documento e ocorrer uma navegação após a chamada ser feita, mas antes que o JavaScript seja executado, o script não será executado e o manipulador será chamado com E_FAIL para o parâmetro errorCode. ExecuteScript funcionará mesmo se IsScriptEnabled estiver definido como FALSE.

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<IWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### CapturePreview 

Capture uma imagem do que o WebView está exibindo.

> Public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) ImageFormat, IStream * imageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) * Handler)

Especifique o formato da imagem com o parâmetro imageFormat. Os dados binários da imagem resultante são gravados no parâmetro imageStream fornecido. Quando o CapturePreview termina de gravar no fluxo, o método Invoke no parâmetro do manipulador fornecido é chamado.

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### Recarregar 

Recarregar a página atual.

> HRESULT ( [recarregamento](#reload)) público

Isso é semelhante a navegar para o URI do documento de nível superior atual, incluindo todos os eventos de navegação que estão sendo acionados e como respeitar as entradas no cache HTTP. Mas o histórico de back/forward não será modificado.

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
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### get_ZoomFactor 

O fator de zoom para a página atual no WebView.

> público HRESULT [get_ZoomFactor](#get_zoomfactor)(duplo * ZoomFactor)

O fator de zoom é mantido por site. Observe que a alteração do fator de zoom pode fazer com que o `window.innerWidth/innerHeight` layout da página seja alterado. Quando a WebView navegar para uma página de um site diferente, o fator de zoom definido para a página anterior não será aplicado. Se o aplicativo quiser definir o fator de zoom para uma determinada página, o primeiro local para fazer isso é no manipulador de eventos DocumentStateChanged. Observe que, se isso for o caso, poderá receber um evento ZoomFactorChanged para o fator de zoom persistente antes de receber o evento ZoomFactorChanged do fator de zoom especificado. Não é permitido especificar um zoomFactor menor ou igual a 0. WebView também tem um intervalo de fator de zoom interno com suporte. Quando um fator de zoom especificado estiver fora desse intervalo, ele será normalizado para estar dentro do intervalo, e um evento ZoomFactorChanged será acionado para o fator de zoom aplicado real. Quando essa faixa de normalização acontece, a propriedade ZoomFactor relata o fator de zoom especificado durante a modificação anterior da propriedade ZoomFactor até que o evento ZoomFactorChanged seja recebido após o WebView se aplicar o fator de zoom normalizado.

#### put_ZoomFactor 

Defina a propriedade ZoomFactor.

> público HRESULT [put_ZoomFactor](#put_zoomfactor)(ZoomFactor duplo)

#### get_IsVisible 

A propriedade IsVisible Determina se deseja mostrar ou ocultar o WebView.

> [get_IsVisible](#get_isvisible)público HRESULT (bool * IsVisible)

Se IsVisible estiver definido como false, o WebView será transparente e não será renderizado. No entanto, isso não afetará a janela que contém o WebView (o parâmetro hWnd que foi passado para WebView). Se você quiser que essa janela desapareça também, chame o recurso de janela diretamente, além de modificar a propriedade IsVisible. A WebView como uma janela filho não obterá mensagens de janela quando a janela superior for minimizada ou restaurada. Por motivo de desempenho, o desenvolvedor deve definir a propriedade IsVisible do WebView como false quando a janela do aplicativo é minimizada e retomada como true quando a janela do aplicativo for restaurada. A janela do aplicativo pode fazer isso ao manipular SC_MINIMIZE e SC_RESTORE comando ao receber WM_SYSCOMMAND mensagem.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
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
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### PostWebMessageAsJson 

Poste a WebMessage especificada no documento de nível superior neste [IWebView2WebView]().

> Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

O evento Message da janela do documento de nível superior. Chrome. WebView será acionado. O JavaScript nesse documento pode assinar e cancelar a assinatura do evento por meio do seguinte: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 Os argumentos do evento é uma instância de `MessageEvent` . A configuração IWebView2Settings:: IsWebMessageEnabled deve ser true ou esse método irá falhar com E_INVALIDARG. A propriedade data do ARG do evento é o parâmetro da cadeia de caracteres WebMessage analisado como uma cadeia de caracteres JSON em um objeto JavaScript. A propriedade de origem do ARG do evento é uma referência ao `window.chrome.webview` objeto. Consulte SetWebMessageReceivedEventHandler para obter informações sobre como enviar mensagens do documento HTML no WebView para o host. Esta mensagem é enviada de forma assíncrona. Se ocorrer uma navegação antes que a mensagem seja postada na página, a mensagem não será enviada.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### PostWebMessageAsString 

Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.

> Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)

Isso se comporta exatamente da mesma maneira que PostWebMessageAsJson, mas a `window.chrome.webview` propriedade data do ARG (evento de mensagem) será uma cadeia de caracteres com o mesmo valor de webMessageAsString. Use isso em vez de PostWebMessageAsJson se você quiser se comunicar por cadeias de caracteres simples em vez de objetos JSON.

#### add_WebMessageReceived 

Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .

> [add_WebMessageReceived](#add_webmessagereceived)público HRESULT (manipulador[IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) *, EventRegistrationToken * token)

A função CreateMessage é `void postMessage(object)` onde o objeto é qualquer objeto compatível com a conversão JSON.

```cpp
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```

 Quando a "CreateMessage" é chamado, o conjunto de [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) por meio desse método SetWebMessageReceivedEventHandler será invocado com o parâmetro de objeto da createmessagestring convertido em uma cadeia de caracteres JSON.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### remove_WebMessageReceived 

Remover um manipulador de eventos adicionado anteriormente com add_WebMessageReceived.

> [remove_WebMessageReceived](#remove_webmessagereceived)público HRESULT (token EventRegistrationToken)

#### Fechar 

Fecha a WebView e limpa a instância do navegador subjacente.

> público HRESULT [fechar](#close)()

A limpeza do navegador instace liberará os recursos que reabrirão o WebView. A instância do navegador será encerrada se não houver outros webviews que o usam.

Depois de chamar Close, todas as chamadas de método falharão e os manipuladores de eventos deixarão de ser acionados. Especificamente, a WebView liberará suas referências a seus manipuladores de eventos quando Close for chamado.

Fechar é chamado implicitamente quando o WebView perde sua referência final e é destruido. Mas é uma prática recomendada chamar o fechamento explicitamente para evitar qualquer ciclo acidental de referências entre o WebView e o código do aplicativo. Especificamente, se você capturar uma referência ao WebView em um manipulador de eventos, criará um ciclo de referência entre o WebView e o manipulador de eventos. Fechar irá interromper esse ciclo liberando todos os manipuladores de eventos. Mas para evitar essa situação, é recomendável fazer chamadas explícitas para fechar na WebView e não capturar uma referência para o WebView para garantir que o WebView possa ser limpo corretamente.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### CallDevToolsProtocolMethod 

Chame um método DevToolsProtocol assíncrono.

> Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) * Handler)

Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista e a descrição dos métodos disponíveis. O parâmetro methodName é o nome completo do método no formato `{domain}.{method}` . O parâmetro parametersAsJson é uma cadeia de caracteres JSON formatada que contém os parâmetros para o método correspondente. O método Invoke do manipulador será chamado quando o método for concluído de forma assíncrona. Invoke será chamado com o objeto Return do método como uma cadeia de caracteres JSON.

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### add_DevToolsProtocolEventReceived 

Assine um evento DevToolsProtocol.

> Public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR EventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) * Handler, EventRegistrationToken * token)

Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista e a descrição de eventos disponíveis. O parâmetro EventName é o nome completo do evento no formato `{domain}.{event}` . O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado. Invoke será chamado com o objeto do evento args que contém o objeto Parameter do evento CDP como uma cadeia de caracteres JSON.

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### remove_DevToolsProtocolEventReceived 

Remover um manipulador de eventos adicionado anteriormente com add_DevToolsProtocolEventReceived.

> Public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR EventName, EventRegistrationToken token)

#### get_BrowserProcessId 

A ID do processo do navegador que hospeda o WebView.

> [get_BrowserProcessId](#get_browserprocessid)público HRESULT (valor UINT32 *)

#### get_CanGoBack 

Pode navegar pelo WebView para a página anterior no histórico de navegação.

> [get_CanGoBack](#get_cangoback)público HRESULT (bool * CanGoBack)

get_CanGoBack alterar o valor com o evento DocumentStateChanged.

#### get_CanGoForward 

Pode navegar pelo WebView para a próxima página no histórico de navegação.

> [get_CanGoForward](#get_cangoforward)público HRESULT (bool * CanGoForward)

get_CanGoForward alterar o valor com o evento DocumentStateChanged.

#### GoBack 

Navega o WebView para a página anterior no histórico de navegação.

> público HRESULT [GoBack](#goback)()

#### GoForward 

Navega o WebView para a próxima página no histórico de navegação.

> Public HRESULT [GoForward](#goforward)()

#### WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Formato de imagem usado pelo método [IWebView2WebView:: CapturePreview](#capturepreview) .

> Enumeração [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | Formato de imagem PNG.
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | Formato de imagem JPEG.

#### WEBVIEW2_SCRIPT_DIALOG_KIND 

Tipo de caixa de diálogo JavaScript usada na interface [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .

> Enumeração [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Uma caixa de diálogo chamada por meio da função JavaScript Window. Alert.
WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Uma caixa de diálogo invocada pela janela. confirmar a função JavaScript.
WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Uma caixa de diálogo chamada por meio da função de JavaScript Window. prompt.

#### WEBVIEW2_PROCESS_FAILED_KIND 

Tipo de falha de processo usada na interface [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .

> Enumeração [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Indica que o processo do navegador foi encerrado inesperadamente.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Indica que o processo de renderização terminou inesperadamente.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Indica que o processo de renderização se torna não responsivo.

#### WEBVIEW2_PERMISSION_TYPE 

O tipo de uma solicitação de permissão.

> Enumeração [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION            | Permissões desconhecidas.
WEBVIEW2_PERMISSION_TYPE_MICROPHONE            | Permissão para capturar o áudio.
WEBVIEW2_PERMISSION_TYPE_CAMERA            | Permissão para capturar vídeo.
WEBVIEW2_PERMISSION_TYPE_GEOLOCATION            | Permissão para acessar a localização geográfica.
WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS            | Permissão para enviar notificações da Web.
WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS            | Permissão para acessar o sensor genérico.
WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ            | Permissão para ler a área de transferência do sistema sem um gesto do usuário.

#### WEBVIEW2_PERMISSION_STATE 

Resposta a uma solicitação de permissão.

> Enumeração [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_STATE_DEFAULT            | Use o comportamento padrão do navegador, que normalmente solicita aos usuários a decisão.
WEBVIEW2_PERMISSION_STATE_ALLOW            | Conceder a solicitação de permissão.
WEBVIEW2_PERMISSION_STATE_DENY            | Negue a solicitação de permissão.

#### WEBVIEW2_MOVE_FOCUS_REASON 

Motivo para mover o foco.

> Enumeração [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | Configuração de código focalizada no WebView.
WEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Movendo o foco devido à guia passagem para frente.
WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Movendo o foco devido a Tabulação de passagem para trás.

#### WEBVIEW2_WEB_ERROR_STATUS 

Valores de status de erro para navegações na Web.

> Enumeração [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Ocorreu um erro desconhecido.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | O nome comum do certificado SSL não corresponde ao endereço Web.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | O certificado SSL venceu.
WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | O certificado do cliente SSL contém erros.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | A revogação do certificado SSL foi cancelada.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | O certificado SSL é inválido.
WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | Não é possível acessar o host.
WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | A conexão expirou.
WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | O servidor retornou uma resposta inválida ou não reconhecida.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | A conexão foi anulada.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | A conexão foi redefinida.
WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | A conexão à Internet foi perdida.
WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Não é possível se conectar ao destino.
WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Não foi possível resolver o nome de host fornecido.
WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | A operação foi cancelada.
WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Falha no redirecionamento de solicitação.
WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Ocorreu um erro inesperado.

#### WEBVIEW2_WEB_RESOURCE_CONTEXT 

Enumeração para contextos de solicitação de recurso da Web.

> Enumeração [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Todos os recursos.
WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Recursos de documento.
WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | Recursos CSS.
WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Recursos de imagem.
WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Outros recursos de mídia, como vídeos.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Recursos de fonte.
WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Recursos de script.
WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | Solicitações HTTP XML.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Busque a comunicação da API.
WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Recursos do texttrack.
WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Outros recursos.
