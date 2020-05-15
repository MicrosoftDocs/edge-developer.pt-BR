---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 77eb48773a963775e00d4dec50368564af5678b0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652771"
---
# interface ICoreWebView2 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface ICoreWebView2
  : public IUnknown
```

O WebView2 permite que você hospede conteúdo da Web usando a tecnologia de navegador da Web mais recente do Edge.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | O objeto ICoreWebView2Settings contém várias configurações modificáveis para a execução do WebView.
[get_Source](#get_source) | O URI do documento de nível superior atual.
[Navegar](#navigate) | Fazer uma navegação do documento de nível superior para o URI especificado.
[NavigateToString](#navigatetostring) | Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.
[add_NavigationStarting](#add_navigationstarting) | Adicione um manipulador de eventos para o evento NavigationStarting.
[remove_NavigationStarting](#remove_navigationstarting) | Remover um manipulador de eventos adicionado anteriormente com add_NavigationStarting.
[add_ContentLoading](#add_contentloading) | Adicione um manipulador de eventos para o evento ContentLoading.
[remove_ContentLoading](#remove_contentloading) | Remover um manipulador de eventos adicionado anteriormente com add_ContentLoading.
[add_SourceChanged](#add_sourcechanged) | SourceChanged é acionado quando a propriedade Source muda.
[remove_SourceChanged](#remove_sourcechanged) | Remover um manipulador de eventos adicionado anteriormente com add_SourceChanged.
[add_HistoryChanged](#add_historychanged) | Cobrançaalterar Ouça a alteração do histórico de navegação do documento de nível superior.
[remove_HistoryChanged](#remove_historychanged) | Remover um manipulador de eventos adicionado anteriormente com add_HistoryChanged.
[add_NavigationCompleted](#add_navigationcompleted) | Adicione um manipulador de eventos para o evento NavigationCompleted.
[remove_NavigationCompleted](#remove_navigationcompleted) | Remover um manipulador de eventos adicionado anteriormente com add_NavigationCompleted.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Adicione um manipulador de eventos para o evento FrameNavigationStarting.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationStarting.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Adicione um manipulador de eventos para o evento ScriptDialogOpening.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Remover um manipulador de eventos adicionado anteriormente com add_ScriptDialogOpening.
[add_PermissionRequested](#add_permissionrequested) | Adicione um manipulador de eventos para o evento PermissionRequested.
[remove_PermissionRequested](#remove_permissionrequested) | Remover um manipulador de eventos adicionado anteriormente com add_PermissionRequested.
[add_ProcessFailed](#add_processfailed) | Adicione um manipulador de eventos para o evento ProcessFailed.
[remove_ProcessFailed](#remove_processfailed) | Remover um manipulador de eventos adicionado anteriormente com add_ProcessFailed.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated.
[ExecuteScript](#executescript) | Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.
[CapturePreview](#capturepreview) | Capture uma imagem do que o WebView está exibindo.
[Recarregar](#reload) | Recarregar a página atual.
[PostWebMessageAsJson](#postwebmessageasjson) | Postar a WebMessage especificada no documento de nível superior neste WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.
[add_WebMessageReceived](#add_webmessagereceived) | Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Remover um manipulador de eventos adicionado anteriormente com add_WebMessageReceived.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Chame um método DevToolsProtocol assíncrono.
[get_BrowserProcessId](#get_browserprocessid) | A ID do processo do navegador que hospeda o WebView.
[get_CanGoBack](#get_cangoback) | Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.
[get_CanGoForward](#get_cangoforward) | Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.
[GoBack](#goback) | Navega o WebView para a página anterior no histórico de navegação.
[GoForward](#goforward) | Navega o WebView para a próxima página no histórico de navegação.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Obtenha um receptor de evento de protocolo DevTools que permite que você se inscreva em um evento de protocolo DevTools.
[Parar](#stop) | Interrompa todas as navegações e buscas de recursos pendentes.
[add_NewWindowRequested](#add_newwindowrequested) | Adicione um manipulador de eventos para o evento NewWindowRequested.
[remove_NewWindowRequested](#remove_newwindowrequested) | Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Adicione um manipulador de eventos para o evento DocumentTitleChanged.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.
[get_DocumentTitle](#get_documenttitle) | O título do documento atual de nível superior.
[Addremoteobject](#addremoteobject) | Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.
[RemoveRemoteObject](#removeremoteobject) | Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.
[OpenDevToolsWindow](#opendevtoolswindow) | Abre a janela do DevTools para o documento atual no WebView.
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Notifica quando a propriedade ContainsFullScreenElement muda.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Indica se a WebView contém um elemento HTML de tela inteira.
[add_WebResourceRequested](#add_webresourcerequested) | Adicione um manipulador de eventos para o evento WebResourceRequested.
[remove_WebResourceRequested](#remove_webresourcerequested) | Remover um manipulador de eventos adicionado anteriormente com add_WebResourceRequested.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.
[add_WindowCloseRequested](#add_windowcloserequested) | Adicione um manipulador de eventos para o evento WindowCloseRequested.
[remove_WindowCloseRequested](#remove_windowcloserequested) | Remover um manipulador de eventos adicionado anteriormente com add_WindowCloseRequested.
[CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) | Formato de imagem usado pelo método ICoreWebView2:: CapturePreview.
[CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) | Tipo de caixa de diálogo JavaScript usada na interface ICoreWebView2ScriptDialogOpeningEventHandler.
[CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) | Tipo de falha de processo usada na interface ICoreWebView2ProcessFailedEventHandler.
[CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) | O tipo de uma solicitação de permissão.
[CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) | Resposta a uma solicitação de permissão.
[CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) | Valores de status de erro para navegações na Web.
[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) | Enumeração para contextos de solicitação de recurso da Web.

## Eventos de navegação

A sequência normal de eventos de navegação é NavigationStarting, SourceChanged, ContentLoading e, em seguida, NavigationCompleted.

![Dot-inline-dotgraph-1. png](media/dot-inline-dotgraph-1.png)

Observe que isso se destina a eventos de navegação com o mesmo evento Navigationid ARG. Navegação eventos com diferentes args de eventos Navigationid podem sobrepor-se. Por exemplo, se você iniciar um evento de navegação e, em seguida, iniciar uma outra navegação, verá o NavigationStarting para a primeira navegação acompanhada pela NavigationStarting da segunda navegação, seguida da NavigationCompleted para a primeira navegação e, em seguida, todos os demais eventos de navegação apropriados para a segunda navegação. Em casos de erro, pode ou não ser um evento ContentLoading dependendo se a navegação é continuada para uma página de erro. No caso de um redirecionamento HTTP, haverá vários eventos NavigationStarting em uma linha, com os seguintes, o sinalizador isredirect definido.

Para monitorar ou cancelar navegações dentro de subquadros no WebView, use FrameNavigationStarting.

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

Abra o DevTools com os atalhos normais: `F12` ou `Ctrl+Shift+I` . Você pode usar o `--auto-open-devtools-for-tabs` argumento de comando switch para que a janela do devtools seja aberta imediatamente ao criar a primeira vez uma WebView. Consulte a documentação do CreateCoreWebView2Host para saber como fornecer argumentos adicionais de linha de comando para o processo do navegador. Confira a chave do registro LoaderOverride para experimentar versões diferentes do WebView2 sem modificar seu aplicativo na documentação do CreateCoreWebView2Host.

## Controle de versão

Depois de usar uma versão específica do SDK para criar seu aplicativo, seu aplicativo pode acabar sendo executado com uma versão mais antiga ou mais recente dos binários instalados do navegador. Até a versão 1.0.0.0 do WebView2, pode haver alterações significativas durante as atualizações que impedem que o SDK funcione com versões diferentes dos binários instalados do navegador. Após a versão 1.0.0.0 versões diferentes do SDK podem funcionar com versões diferentes do navegador instalado seguindo estas práticas recomendadas:

Para fazer a conta de alterações significativas na API, verifique se há uma falha ao chamar a DLL de exportação CreateCoreWebView2Environment e ao chamar QueryInterface em qualquer objeto CoreWebView2. Um valor de retorno de E_NOINTERFACE pode indicar que o SDK não é compatível com os binários do navegador Edge.

Verificar a falha de QueryInterface também contará em casos em que o SDK é mais recente do que a versão do navegador Edge e seu aplicativo tenta usar uma interface do qual o navegador Edge não reconhece.

Quando uma interface não está disponível, você pode considerar a possibilidade de desabilitar o recurso associado, se possível, ou informar ao usuário final que ele precisa atualizar o navegador.

## Parte

#### get_Settings 

O objeto ICoreWebView2Settings contém várias configurações modificáveis para a execução do WebView.

> público HRESULT [get_Settings](#get_settings)(configurações ICoreWebView2Settings * *)

#### get_Source 

O URI do documento de nível superior atual.

> [get_Source](#get_source)público HRESULT (URI LPWSTR *)

Esse valor potencialmente muda como parte do acionamento do evento SourceChanged para alguns casos, como navegar para diferentes navegação de site ou de fragmento. Ele permanecerá o mesmo para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual.

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### Navegar 

Fazer uma navegação do documento de nível superior para o URI especificado.

> público- [navegação](#navigate)HRESULT (URI LPCWSTR)

Consulte os eventos de navegação para obter mais informações. Observe que isso iniciará uma navegação e o evento NavigationStarting correspondente será acionado algum tempo após a conclusão dessa chamada de navegação.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
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

> Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * token)

NavigationStarting é acionado quando o quadro principal do WebView está solicitando permissão para navegar para um URI diferente. Isso também será acionado para redirecionamentos.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
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

#### add_ContentLoading 

Adicione um manipulador de eventos para o evento ContentLoading.

> Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) * EventHandler, EventRegistrationToken * token)

ContentLoading é acionado antes que qualquer conteúdo seja carregado, incluindo scripts adicionados com AddScriptToExecuteOnDocumentCreated ContentLoading não será acionado se ocorrer uma mesma navegação de página (por exemplo, por meio de navegações de fragmento ou de histórico. pushstate). Isso segue os eventos NavigationStarting e SourceChanged e precede os eventos Historychanged e NavigationCompleted.

#### remove_ContentLoading 

Remover um manipulador de eventos adicionado anteriormente com add_ContentLoading.

> [remove_ContentLoading](#remove_contentloading)público HRESULT (token EventRegistrationToken)

#### add_SourceChanged 

SourceChanged é acionado quando a propriedade Source muda.

> Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

SourceChanged é acionado para navegar para um site ou navegação de fragmento diferente. Ele não será acionado para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual. SourceChanged é acionado antes de ContentLoading para navegação para um novo documento. Adicione um manipulador de eventos para o evento SourceChanged. 

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### remove_SourceChanged 

Remover um manipulador de eventos adicionado anteriormente com add_SourceChanged.

> [remove_SourceChanged](#remove_sourcechanged)público HRESULT (token EventRegistrationToken)

#### add_HistoryChanged 

Cobrançaalterar Ouça a alteração do histórico de navegação do documento de nível superior.

> Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Use Cobrançaalterar para verificar se get_CanGoBack/get_CanGoForward valor mudou. Historychanged também é acionado para usar o GoBack/GoForward. Historychanged é acionado após SourceChanged e ContentLoading. Adicione um manipulador de eventos para o evento Historychanged. 

```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### remove_HistoryChanged 

Remover um manipulador de eventos adicionado anteriormente com add_HistoryChanged.

> [remove_HistoryChanged](#remove_historychanged)público HRESULT (token EventRegistrationToken)

#### add_NavigationCompleted 

Adicione um manipulador de eventos para o evento NavigationCompleted.

> Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) * EventHandler, EventRegistrationToken * token)

O evento NavigationCompleted é acionado quando o WebView foi completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
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

> Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * token)

FrameNavigationStarting é acionado quando um quadro filho na WebView solicita permissão para navegar para um URI diferente. Isso também será acionado para redirecionamentos.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### add_ScriptDialogOpening 

Adicione um manipulador de eventos para o evento ScriptDialogOpening.

> Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) * EventHandler, EventRegistrationToken * token)

O evento é acionado quando uma caixa de diálogo JavaScript (alerta, confirmação ou prompt) aparecerá para o WebView. Esse evento só será acionado se a propriedade ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled estiver definida como false. O evento ScriptDialogOpening pode ser usado para suprimir caixas de diálogo ou substituir caixas de diálogo padrão por caixas de diálogo personalizadas.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
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

#### add_PermissionRequested 

Adicione um manipulador de eventos para o evento PermissionRequested.

> Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Acionado quando o conteúdo de uma WebView solicita permissão para acessar alguns recursos privilegiados.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Remover um manipulador de eventos adicionado anteriormente com add_PermissionRequested.

> [remove_PermissionRequested](#remove_permissionrequested)público HRESULT (token EventRegistrationToken)

#### add_ProcessFailed 

Adicione um manipulador de eventos para o evento ProcessFailed.

> Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Acionado quando um processo da WebView termina inesperadamente ou não responde.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
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

> Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) * Handler)

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
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
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

> Public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) * Handler)

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
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
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

> Public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) ImageFormat, IStream * imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) * Handler)

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
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

#### PostWebMessageAsJson 

Postar a WebMessage especificada no documento de nível superior neste WebView.

> Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

O evento Message da janela do documento de nível superior. Chrome. WebView será acionado. O JavaScript nesse documento pode assinar e cancelar a assinatura do evento por meio do seguinte: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 Os argumentos do evento é uma instância de `MessageEvent` . A configuração ICoreWebView2Settings:: IsWebMessageEnabled deve ser true ou esse método irá falhar com E_INVALIDARG. A propriedade data do ARG do evento é o parâmetro da cadeia de caracteres WebMessage analisado como uma cadeia de caracteres JSON em um objeto JavaScript. A propriedade de origem do ARG do evento é uma referência ao `window.chrome.webview` objeto. Consulte SetWebMessageReceivedEventHandler para obter informações sobre como enviar mensagens do documento HTML no WebView para o host. Esta mensagem é enviada de forma assíncrona. Se ocorrer uma navegação antes que a mensagem seja postada na página, a mensagem não será enviada.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

> [add_WebMessageReceived](#add_webmessagereceived)público HRESULT (manipulador[ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) *, EventRegistrationToken * token)

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

 Quando a "CreateMessage" é chamado, o conjunto de [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) por meio desse método SetWebMessageReceivedEventHandler será invocado com o parâmetro de objeto da createmessagestring convertido em uma cadeia de caracteres JSON.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

#### CallDevToolsProtocolMethod 

Chame um método DevToolsProtocol assíncrono.

> Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) * Handler)

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
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### get_BrowserProcessId 

A ID do processo do navegador que hospeda o WebView.

> [get_BrowserProcessId](#get_browserprocessid)público HRESULT (valor UINT32 *)

#### get_CanGoBack 

Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.

> [get_CanGoBack](#get_cangoback)público HRESULT (bool * CanGoBack)

O evento Historychanged será acionado se get_CanGoBack alterar o valor.

#### get_CanGoForward 

Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.

> [get_CanGoForward](#get_cangoforward)público HRESULT (bool * CanGoForward)

O evento Historychanged será acionado se get_CanGoForward alterar o valor.

#### GoBack 

Navega o WebView para a página anterior no histórico de navegação.

> público HRESULT [GoBack](#goback)()

#### GoForward 

Navega o WebView para a próxima página no histórico de navegação.

> Public HRESULT [GoForward](#goforward)()

#### GetDevToolsProtocolEventReceiver 

Obtenha um receptor de evento de protocolo DevTools que permite que você se inscreva em um evento de protocolo DevTools.

> Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) * * Receiver)

O parâmetro EventName é o nome completo do evento no formato `{domain}.{event}` . Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista da descrição de eventos de protocolo devtools e argumentos de evento.

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
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### Parar 

Interrompa todas as navegações e buscas de recursos pendentes.

> público- [limite](#stop)HRESULT ()

Não interrompe scripts.

#### add_NewWindowRequested 

Adicione um manipulador de eventos para o evento NewWindowRequested.

> Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Acionado quando o conteúdo dentro do WebView solicitado para abrir uma nova janela, por exemplo, por meio de Window. Open. O aplicativo pode passar um WebView de destino que será considerado a janela aberta.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewWindowRequested 

Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.

> [remove_NewWindowRequested](#remove_newwindowrequested)público HRESULT (token EventRegistrationToken)

#### add_DocumentTitleChanged 

Adicione um manipulador de eventos para o evento DocumentTitleChanged.

> Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

O evento é acionado quando a propriedade DocumentTitle da WebView muda e pode ser acionada antes ou depois do evento NavigationCompleted.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### remove_DocumentTitleChanged 

Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.

> [remove_DocumentTitleChanged](#remove_documenttitlechanged)público HRESULT (token EventRegistrationToken)

#### get_DocumentTitle 

O título do documento atual de nível superior.

> público HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR * title)

Se o documento não tiver um título explícito ou estiver vazio, um padrão que pode ou não corresponder ao URI do documento será usado.

#### Addremoteobject 

Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.

> Public HRESULT [Addremoteobject](#addremoteobject)(nome do LPCWSTR, objeto Variant *)

Os objetos de host são expostos como proxies de objeto remoto via `window.chrome.webview.remoteObjects.<name>` . Proxies de objeto remoto são promessas e serão resolvidos para um objeto que representa o objeto host. A promessa será recusada se o aplicativo não adicionar um objeto com o nome. Quando o código JavaScript acessa uma propriedade ou método do objeto, uma promessa é retornada, que será resolvida para o valor retornado do host para a propriedade ou método, ou recusada em caso de erro, pois não há tal propriedade ou método no objeto ou parâmetros são inválidos. Por exemplo, quando o código do aplicativo faz o seguinte: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 O código JavaScript na WebView poderá acessar o appObject da seguinte forma e, em seguida, acessar atributos e métodos de appObject: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Observe que, enquanto tipos simples, IDispatch e matriz são compatíveis, IUnknown Generic, VT_DECIMAL ou Variant VT_RECORD não é suportada. Objetos JavaScript remotos como funções de retorno de chamada são representados como uma variante VT_DISPATCH com o objeto que implementa IDispatch. O método de retorno de chamada JavaScript pode ser invocado usando DISPID_VALUE para o DISPID. Há suporte para matrizes aninhadas até uma profundidade de 3. Matrizes de tipos de referência não são suportadas. VT_EMPTY e VT_NULL são mapeados para JavaScript como nulo. Em JavaScript nulo e indefinido são mapeados para VT_EMPTY.

Além disso, todos os objetos remotos são expostos como `window.chrome.webview.remoteObjects.sync.<name>` . Aqui, os objetos do host são expostos como proxies síncronos de objeto remoto. Elas não são promessas e chamadas para funções ou acesso à propriedade o bloqueio síncrono de script em execução, aguardando a comunicação de processo cruzado para o código do host ser executado. Portanto, isso pode resultar em problemas de confiabilidade e é recomendável que você use a API assíncrona baseada em promessa `window.chrome.webview.remoteObjects.<name>` descrita acima.

Proxies de objetos remotos síncronos e proxies de objeto remoto assíncrono podem proxy para o mesmo objeto remoto. As alterações remotas feitas por um proxy serão refletidas em qualquer outro proxy do mesmo objeto remoto, seja os outros proxies e síncronos ou assíncronos.

Embora o JavaScript seja bloqueado em uma chamada síncrona para o código nativo, esse código nativo não pode retornar a chamada para JavaScript. As tentativas de fazer isso falharão com o HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Proxies de objeto remoto são objetos de proxy JavaScript que interceptam todas as invocações de propriedade, conjunto de propriedades e invocação de propriedade. Propriedades ou métodos que fazem parte da função ou do protótipo do objeto são executados localmente. Além disso, qualquer propriedade ou método na matriz `chrome.webview.remoteObjects.options.forceLocalProperties` também será executado localmente. Isso assume como padrão os métodos opcionais que têm significado em JavaScript como `toJSON` e `Symbol.toPrimitive` . Você pode adicionar mais à matriz, conforme necessário.

Há um método `chrome.webview.remoteObjects.cleanupSome` que melhor esforço coletará os proxies de objetos remotos.

Os proxies de objetos remotos também têm os seguintes métodos que são executados localmente:

* applyRemote, getRemote, SetRemote: execute uma invocação de método, uma propriedade get ou uma propriedade definida no objeto remoto. Você pode usá-los para forçar explicitamente um método ou uma propriedade para execução remota se houver um método ou uma propriedade local conflitante. Por exemplo, ele `proxy.toString()` executará o método ToString local no objeto proxy. Mas `proxy.applyRemote('toString')` é executado `toString` no objeto em proxy remoto.

* getLocal, setlocal: executar propriedade get ou Property definido localmente. Você pode usar esses métodos para forçar a obtenção ou configuração de uma propriedade no próprio proxy de objeto remoto, em vez de no objeto remoto que ele representa. Por exemplo, receberá `proxy.unknownProperty` a propriedade nomeada `unknownProperty` do objeto com proxy remoto. Mas receberá `proxy.getLocal('unknownProperty')` o valor da propriedade `unknownProperty` no próprio objeto proxy.

* sincronização: proxies de objetos remotos assíncronos expõem um método de sincronização que retorna uma promessa para um proxy síncrono de objeto remoto para o mesmo objeto remoto. Por exemplo, `chrome.webview.remoteObjects.sample.methodCall()` retorna um proxy de objeto remoto assíncrono. Você pode usar o `sync` método para obter um proxy de objeto remoto síncrono em vez disso: `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: proxies de objetos remotos síncronos expõem um método Async que bloqueia e retorna um proxy de objeto remoto assíncrono para o mesmo objeto remoto. Por exemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` retorna um proxy síncrono de objeto remoto. Chamar o `async` método nesse bloco e, em seguida, retorna um proxy de objeto remoto assíncrono para o mesmo objeto remoto: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* em seguida: proxies de objetos remotos assíncronos têm um método Where. Isso permite que eles sejam awaitable. `then` retornará uma promessa que será resolvida com uma representação do objeto remoto. Se o proxy representar um literal JavaScript, uma cópia dele será retornada localmente. Se o proxy representar uma função, um proxy não awaitable será retornado. Se o proxy representar um objeto JavaScript com uma mistura de propriedades literais e propriedades de função, a cópia do objeto será retornada com algumas propriedades como proxies de objeto remoto.

Todas as outras invocações de método e Propriedade (além dos métodos de proxy de objeto remoto acima, lista de forceLocalProperties e propriedades em protótipos de objeto e função) são executadas remotamente. Proxies assíncronos de objetos remotos retornam uma promessa que representa a conclusão assíncrona da invocação remota do método ou a obtenção da propriedade. A promessa é resolvida após a conclusão das operações remotas e as promessas são resolvidas para o valor resultante da operação. Os proxies de objetos remotos síncronos funcionam da mesma forma, mas bloqueiam a execução de JavaScript e aguardam a conclusão da operação remota.

A configuração de uma propriedade em um proxy de objeto remoto assíncrono funciona de forma ligeiramente diferente. O conjunto retorna imediatamente e o valor de retorno é o valor que será definido. Isso é uma exigência do objeto proxy JavaScript. Se você precisar esperar assincronamente o conjunto de propriedades para concluir, use o método SetRemote que retorna uma promessa conforme descrito acima. Propriedade de conjunto de propriedades de objeto síncrono bloqueia sincronamente, até que a propriedade seja definida.

Por exemplo, suponha que você tenha um objeto COM com a seguinte interface

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 Poderemos adicionar uma instância dessa interface ao nosso JavaScript com `AddRemoteObject` . Nesse caso, podemos nomeá-lo `sample` :

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 Em seguida, no documento HTML, podemos usar esse objeto COM via `chrome.webview.remoteObjects.sample` :

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### RemoveRemoteObject 

Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.

> Public HRESULT [RemoveRemoteObject](#removeremoteobject)(nome LPCWSTR)

Embora novas tentativas de acesso sejam negadas, se o objeto já for obtido por código JavaScript na WebView, o código JavaScript continuará a ter acesso a esse objeto. Chamar este método para um nome que já foi removido ou nunca adicionado falhará.

#### OpenDevToolsWindow 

Abre a janela do DevTools para o documento atual no WebView.

> Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Não faz nada se for chamado quando a janela do DevTools já estiver aberta

#### add_ContainsFullScreenElementChanged 

Notifica quando a propriedade ContainsFullScreenElement muda.

> Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Isso significa que um elemento HTML dentro do WebView está entrando em tela inteira no tamanho do WebView ou sai do fullscreen. Esse evento é útil quando, por exemplo, um elemento de vídeo solicita a tela inteira. O ouvinte de ContainsFullScreenElementChanged pode então redimensionar a WebView em resposta.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_ContainsFullScreenElementChanged 

Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.

> [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)público HRESULT (token EventRegistrationToken)

#### get_ContainsFullScreenElement 

Indica se a WebView contém um elemento HTML de tela inteira.

> [get_ContainsFullScreenElement](#get_containsfullscreenelement)público HRESULT (bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Adicione um manipulador de eventos para o evento WebResourceRequested.

> Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Acionado quando o WebView está executando uma solicitação HTTP para uma URL correspondente e um filtro de contexto de recurso que foi adicionado com o AddWebResourceRequestedFilter. Pelo menos um filtro deve ser adicionado para que o evento seja acionado.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
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

#### AddWebResourceRequestedFilter 

Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.

> Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(URI const LPCWSTR,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)

O parâmetro URI pode ser uma cadeia de caracteres curinga (' ': zero ou mais, '? ': exatamente um). nullptr é equivalente a L "". Consulte CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enumeração para obter a descrição dos filtros de contexto de recurso.

#### RemoveWebResourceRequestedFilter 

Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.

> Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(URI const LPCWSTR,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)

Se o mesmo filtro tiver sido adicionado várias vezes, será preciso removê-lo quantas vezes forem adicionadas para que a remoção seja efetiva. Retorna E_INVALIDARG para um filtro que nunca foi adicionado.

#### add_WindowCloseRequested 

Adicione um manipulador de eventos para o evento WindowCloseRequested.

> Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Dispara quando o conteúdo dentro do WebView solicitado para fechar a janela, como After Window. Close, é chamado. O aplicativo deve fechar a janela da WebView e do aplicativo relacionado se isso fizer sentido com o aplicativo.

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_WindowCloseRequested 

Remover um manipulador de eventos adicionado anteriormente com add_WindowCloseRequested.

> [remove_WindowCloseRequested](#remove_windowcloserequested)público HRESULT (token EventRegistrationToken)

#### CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Formato de imagem usado pelo método ICoreWebView2:: CapturePreview.

> Enumeração [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | Formato de imagem PNG.
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | Formato de imagem JPEG.

#### CORE_WEBVIEW2_SCRIPT_DIALOG_KIND 

Tipo de caixa de diálogo JavaScript usada na interface ICoreWebView2ScriptDialogOpeningEventHandler.

> Enumeração [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Uma caixa de diálogo chamada por meio da função JavaScript Window. Alert.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Uma caixa de diálogo invocada pela janela. confirmar a função JavaScript.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Uma caixa de diálogo chamada por meio da função de JavaScript Window. prompt.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD            | Uma caixa de diálogo chamada pelo evento JavaScript beforeunload.

#### CORE_WEBVIEW2_PROCESS_FAILED_KIND 

Tipo de falha de processo usada na interface ICoreWebView2ProcessFailedEventHandler.

> Enumeração [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Indica que o processo do navegador foi encerrado inesperadamente.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Indica que o processo de renderização terminou inesperadamente.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Indica que o processo de renderização se torna não responsivo.

#### CORE_WEBVIEW2_PERMISSION_KIND 

O tipo de uma solicitação de permissão.

> Enumeração [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION            | Permissões desconhecidas.
CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE            | Permissão para capturar o áudio.
CORE_WEBVIEW2_PERMISSION_KIND_CAMERA            | Permissão para capturar vídeo.
CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION            | Permissão para acessar a localização geográfica.
CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS            | Permissão para enviar notificações da Web.
CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS            | Permissão para acessar o sensor genérico.
CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ            | Permissão para ler a área de transferência do sistema sem um gesto do usuário.

#### CORE_WEBVIEW2_PERMISSION_STATE 

Resposta a uma solicitação de permissão.

> Enumeração [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT            | Use o comportamento padrão do navegador, que normalmente solicita aos usuários a decisão.
CORE_WEBVIEW2_PERMISSION_STATE_ALLOW            | Conceder a solicitação de permissão.
CORE_WEBVIEW2_PERMISSION_STATE_DENY            | Negue a solicitação de permissão.

#### CORE_WEBVIEW2_WEB_ERROR_STATUS 

Valores de status de erro para navegações na Web.

> Enumeração [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Ocorreu um erro desconhecido.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | O nome comum do certificado SSL não corresponde ao endereço Web.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | O certificado SSL venceu.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | O certificado do cliente SSL contém erros.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | A revogação do certificado SSL foi cancelada.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | O certificado SSL é inválido &ndash; isso significa que o certificado não correspondia aos pins da chave pública para o nome do host, o certificado é assinado por uma autoridade não confiável ou por meio de um algoritmo de sinal fraco, o certificado declarado pelos nomes DNS viola restrições de nome, o certificado contém uma chave fraca, o período de validade do certificado é muito longo, falta de informações sobre a revogação ou o mecanismo de revogação, o nome do host não exclusivo, a falta de informações [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)de transparência do certificado
CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | Não é possível acessar o host.
CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | A conexão expirou.
CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | O servidor retornou uma resposta inválida ou não reconhecida.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | A conexão foi anulada.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | A conexão foi redefinida.
CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | A conexão à Internet foi perdida.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Não é possível se conectar ao destino.
CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Não foi possível resolver o nome de host fornecido.
CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | A operação foi cancelada.
CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Falha no redirecionamento de solicitação.
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Ocorreu um erro inesperado.

#### CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT 

Enumeração para contextos de solicitação de recurso da Web.

> Enumeração [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Todos os recursos.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Recursos de documento.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | Recursos CSS.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Recursos de imagem.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Outros recursos de mídia, como vídeos.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Recursos de fonte.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Recursos de script.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | Solicitações HTTP XML.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Busque a comunicação da API.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Recursos do texttrack.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | Comunicação de API de EventSource.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | Comunicação de API WebSocket.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | Manifestos do aplicativo Web.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | Trocas HTTP assinadas.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | Solicitações de ping.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | Relatórios de violação de CSP.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Outros recursos.