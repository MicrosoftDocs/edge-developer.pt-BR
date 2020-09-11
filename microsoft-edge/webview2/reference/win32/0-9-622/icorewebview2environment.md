---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2Environment
ms.openlocfilehash: 3552de59b8b349c62d61ca165141d9adddd2a5a9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011435"
---
# interface ICoreWebView2Environment 

```
interface ICoreWebView2Environment
  : public IUnknown
```

Isso representa o ambiente WebView2.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[add_NewBrowserVersionAvailable](#add_newbrowserversionavailable) | Adicione um manipulador de eventos para o evento NewBrowserVersionAvailable.
[CreateCoreWebView2Controller](#createcorewebview2controller) | Criar de forma assíncrona um novo WebView.
[CreateWebResourceResponse](#createwebresourceresponse) | Crie um novo objeto de resposta de recurso da Web.
[get_BrowserVersionString](#get_browserversionstring) | As informações de versão do navegador do [ICoreWebView2Environment]()atual, incluindo o nome do canal, se não for o canal estável.
[remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable) | Remover um manipulador de eventos adicionado anteriormente com add_NewBrowserVersionAvailable.

Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente. Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.

## Parte

#### add_NewBrowserVersionAvailable 

Adicione um manipulador de eventos para o evento NewBrowserVersionAvailable.

> Public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) * EventHandler, EventRegistrationToken * token)

NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso por meio do WebView2. Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView. Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado. Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.

Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro. Ou simplesmente solicitar que o usuário reinicie o aplicativo.

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](ICoreWebView2Environment* sender, IUnknown* args) -> HRESULT {
                std::wstring message = L"We detected there is a new version for the browser.";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### CreateCoreWebView2Controller 

Criar de forma assíncrona um novo WebView.

> Public HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND ParentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) * Handler)

parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada. O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView. A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.

É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo. Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow. 
```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();
    m_dcompDevice = nullptr;
    m_wincompCompositor = nullptr;
    LPCWSTR subFolder = nullptr;

    if (m_creationModeId == IDM_CREATION_MODE_VISUAL_DCOMP ||
        m_creationModeId == IDM_CREATION_MODE_TARGET_DCOMP)
    {
        HRESULT hr = DCompositionCreateDevice2(nullptr, IID_PPV_ARGS(&m_dcompDevice));
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using DComp Visual is not supported.\r\n"
                "DComp device creation failed.\r\n"
                "Current OS may not support DComp.",
                L"Create with Windowless DComp Visual Failed", MB_OK);
            return;
        }
    }
    else if (m_creationModeId == IDM_CREATION_MODE_VISUAL_WINCOMP)
    {
        HRESULT hr = TryCreateDispatcherQueue();
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using WinComp Visual is not supported.\r\n"
                "WinComp compositor creation failed.\r\n"
                "Current OS may not support WinComp.",
                L"Create with Windowless WinComp Visual Failed", MB_OK);
            return;
        }
        m_wincompCompositor = winrtComp::Compositor();
    }
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    CHECK_FAILURE(options->put_AllowSingleSignOnUsingOSPrimaryAccount(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
    if (!SUCCEEDED(hr))
    {
        if (hr == HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND))
        {
            MessageBox(
                m_mainWindow,
                L"Couldn't find Edge installation. "
                "Do you have a version installed that's compatible with this "
                "WebView2 SDK version?",
                nullptr, MB_OK);
        }
        else
        {
            ShowFailure(hr, L"Failed to create webview environment");
        }
    }
}
// This is the callback passed to CreateWebViewEnvironmentWithOptions.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);
    m_webViewEnvironment = environment;

    auto webViewExperimentalEnvironment =
        m_webViewEnvironment.try_query<ICoreWebView2ExperimentalEnvironment>();
    if (webViewExperimentalEnvironment && (m_dcompDevice || m_wincompCompositor))
    {
        CHECK_FAILURE(webViewExperimentalEnvironment->CreateCoreWebView2CompositionController(
            m_mainWindow,
            Callback<
                ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler>(
                [this](
                    HRESULT result,
                    ICoreWebView2ExperimentalCompositionController* compositionController) -> HRESULT {
                    auto controller =
                        wil::com_ptr<ICoreWebView2ExperimentalCompositionController>(compositionController)
                            .query<ICoreWebView2Controller>();
                    return OnCreateCoreWebView2ControllerCompleted(result, controller.get());
                })
                .Get()));
    }
    else
    {
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Controller(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2ControllerCompleted)
                              .Get()));
    }

    return S_OK;
}
```
 É recomendável que o aplicativo manipule as mensagens do Gerenciador de reinicialização para que ele possa ser reiniciado normalmente quando o aplicativo estiver usando o Edge for WebView a partir de uma determinada instalação e essa instalação estiver sendo desinstalada. Por exemplo, se um usuário instalar o Edge do canal de desenvolvimento e optar por usar o Edge desse canal para testar o aplicativo e, em seguida, desinstalar o Edge desse canal sem fechar o aplicativo, o aplicativo será reiniciado para permitir a desinstalação do canal de desenvolvimento ser bem-sucedida. 
```cpp
    case WM_QUERYENDSESSION:
    {
        // yes, we can shut down
        // Register how we might be restarted
        RegisterApplicationRestart(L"--restore", RESTART_NO_CRASH | RESTART_NO_HANG);
        *result = TRUE;
        return true;
    }
    break;
    case WM_ENDSESSION:
    {
        if (wParam == TRUE)
        {
            // save app state and exit.
            PostQuitMessage(0);
            return true;
        }
    }
    break;
```
 Quando o aplicativo tenta novamente CreateCoreWebView2Controller após a falha, é recomendável que o aplicativo seja reiniciado a partir da criação de um novo ambiente WebView2. Se ocorrer uma atualização de borda, a versão associada a um ambiente de WebView2 pode ter sido removida e fazer com que o objeto não funcione mais. A criação de um novo ambiente de WebView2 funcionará, pois ele usa a versão mais recente.

A criação do WebView falhará se já houver uma instância em execução usando a mesma pasta de dados do usuário, e os objetos de ambiente tiverem diferentesoptions de ambiente. Por exemplo, se já houver um WebView criado com um idioma, tentar criar uma WebView com um idioma diferente usando a mesma pasta de dados do usuário falhará.

#### CreateWebResourceResponse 

Crie um novo objeto de resposta de recurso da Web.

> Public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo IStream *, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR cabeçalhos, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * resposta)

Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha. Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) para construir os cabeçalhos linha por linha. Para obter informações sobre outros parâmetros, consulte [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
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

#### get_BrowserVersionString 

As informações de versão do navegador do [ICoreWebView2Environment]()atual, incluindo o nome do canal, se não for o canal estável.

> público HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR * versionInfo)

Isso corresponde ao formato da API GetAvailableCoreWebView2BrowserVersionString. Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionString(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### remove_NewBrowserVersionAvailable 

Remover um manipulador de eventos adicionado anteriormente com add_NewBrowserVersionAvailable.

> [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)público HRESULT (token EventRegistrationToken)

