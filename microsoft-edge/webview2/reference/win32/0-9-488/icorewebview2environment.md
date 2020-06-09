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
ms.openlocfilehash: d8cc43e7535be94448ae100e3298e35ec47f94d3
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698047"
---
# <span data-ttu-id="7cc62-104">interface ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="7cc62-104">interface ICoreWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="7cc62-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7cc62-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7cc62-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="7cc62-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Environment
  : public IUnknown
```

<span data-ttu-id="7cc62-107">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cc62-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="7cc62-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7cc62-108">Summary</span></span>

 <span data-ttu-id="7cc62-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7cc62-109">Members</span></span>                        | <span data-ttu-id="7cc62-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7cc62-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7cc62-111">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="7cc62-111">add_NewBrowserVersionAvailable</span></span>](#add_newbrowserversionavailable) | <span data-ttu-id="7cc62-112">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cc62-112">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="7cc62-113">CreateCoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="7cc62-113">CreateCoreWebView2Controller</span></span>](#createcorewebview2controller) | <span data-ttu-id="7cc62-114">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="7cc62-114">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="7cc62-115">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="7cc62-115">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="7cc62-116">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="7cc62-116">Create a new web resource response object.</span></span>
[<span data-ttu-id="7cc62-117">get_BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="7cc62-117">get_BrowserVersionString</span></span>](#get_browserversionstring) | <span data-ttu-id="7cc62-118">As informações de versão do navegador do [ICoreWebView2Environment]()atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="7cc62-118">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="7cc62-119">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="7cc62-119">remove_NewBrowserVersionAvailable</span></span>](#remove_newbrowserversionavailable) | <span data-ttu-id="7cc62-120">Remover um manipulador de eventos adicionado anteriormente com add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="7cc62-120">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

<span data-ttu-id="7cc62-121">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="7cc62-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="7cc62-122">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="7cc62-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="7cc62-123">Parte</span><span class="sxs-lookup"><span data-stu-id="7cc62-123">Members</span></span>

#### <span data-ttu-id="7cc62-124">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="7cc62-124">add_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="7cc62-125">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cc62-125">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="7cc62-126">Public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7cc62-126">public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7cc62-127">Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView.</span><span class="sxs-lookup"><span data-stu-id="7cc62-127">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="7cc62-128">Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="7cc62-128">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="7cc62-129">Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="7cc62-129">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="7cc62-130">Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro.</span><span class="sxs-lookup"><span data-stu-id="7cc62-130">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="7cc62-131">Ou simplesmente solicitar que o usuário reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7cc62-131">Or simply prompt the user to restart the app.</span></span>

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

#### <span data-ttu-id="7cc62-132">CreateCoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="7cc62-132">CreateCoreWebView2Controller</span></span> 

<span data-ttu-id="7cc62-133">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="7cc62-133">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="7cc62-134">Public HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND ParentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="7cc62-134">public HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND parentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="7cc62-135">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="7cc62-135">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="7cc62-136">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="7cc62-136">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="7cc62-137">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="7cc62-137">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="7cc62-138">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7cc62-138">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="7cc62-139">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="7cc62-139">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();
    m_dcompDevice = nullptr;
    m_wincompHelper = nullptr;

    LPCWSTR subFolder = nullptr;

    if (m_creationModeId == IDM_CREATION_MODE_VISUAL_DCOMP)
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
        HRESULT hr = CreateWinCompCompositor();
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
    }
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
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
    if (webViewExperimentalEnvironment && (m_dcompDevice || m_wincompHelper))
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
 <span data-ttu-id="7cc62-140">É recomendável que o aplicativo manipule as mensagens do Gerenciador de reinicialização para que ele possa ser reiniciado normalmente quando o aplicativo estiver usando o Edge for WebView a partir de uma determinada instalação e essa instalação estiver sendo desinstalada.</span><span class="sxs-lookup"><span data-stu-id="7cc62-140">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="7cc62-141">Por exemplo, se um usuário instalar o Edge do canal de desenvolvimento e optar por usar o Edge desse canal para testar o aplicativo e, em seguida, desinstalar o Edge desse canal sem fechar o aplicativo, o aplicativo será reiniciado para permitir a desinstalação do canal de desenvolvimento ser bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7cc62-141">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
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
 <span data-ttu-id="7cc62-142">Quando o aplicativo tenta novamente CreateCoreWebView2Controller após a falha, é recomendável que o aplicativo seja reiniciado a partir da criação de um novo ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cc62-142">When the application retries CreateCoreWebView2Controller upon failure, it is recommended that the application restarts from creating a new WebView2 Environment.</span></span> <span data-ttu-id="7cc62-143">Se ocorrer uma atualização de borda, a versão associada a um ambiente de WebView2 pode ter sido removida e fazer com que o objeto não funcione mais.</span><span class="sxs-lookup"><span data-stu-id="7cc62-143">If an Edge update happens, the version associated with a WebView2 Environment could have been removed and causing the object to no longer work.</span></span> <span data-ttu-id="7cc62-144">A criação de um novo ambiente de WebView2 funcionará, pois ele usa a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="7cc62-144">Creating a new WebView2 Environment will work as it uses the latest version.</span></span>

<span data-ttu-id="7cc62-145">A criação do WebView falhará se já houver uma instância em execução usando a mesma pasta de dados do usuário, e os objetos de ambiente tiverem diferentesoptions de ambiente.</span><span class="sxs-lookup"><span data-stu-id="7cc62-145">WebView creation will fail if there is already a running instance using the same user data folder, and the Environment objects have different EnvironmentOptions.</span></span> <span data-ttu-id="7cc62-146">Por exemplo, se já houver um WebView criado com um idioma, tentar criar uma WebView com um idioma diferente usando a mesma pasta de dados do usuário falhará.</span><span class="sxs-lookup"><span data-stu-id="7cc62-146">For example, if there is already a WebView created with one language, trying to create a WebView with a different language using the same user data folder will fail.</span></span>

#### <span data-ttu-id="7cc62-147">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="7cc62-147">CreateWebResourceResponse</span></span> 

<span data-ttu-id="7cc62-148">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="7cc62-148">Create a new web resource response object.</span></span>

> <span data-ttu-id="7cc62-149">Public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo IStream \*, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR cabeçalhos, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="7cc62-149">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content, int statusCode, LPCWSTR reasonPhrase, LPCWSTR headers, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="7cc62-150">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="7cc62-150">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="7cc62-151">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="7cc62-151">It's also possible to create this object with empty headers string and then use the [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="7cc62-152">Para obter informações sobre outros parâmetros, consulte [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).</span><span class="sxs-lookup"><span data-stu-id="7cc62-152">For information on other parameters see [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).</span></span>

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

#### <span data-ttu-id="7cc62-153">get_BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="7cc62-153">get_BrowserVersionString</span></span> 

<span data-ttu-id="7cc62-154">As informações de versão do navegador do [ICoreWebView2Environment]()atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="7cc62-154">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="7cc62-155">público HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="7cc62-155">public HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="7cc62-156">Isso corresponde ao formato da API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="7cc62-156">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="7cc62-157">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="7cc62-157">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionString(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### <span data-ttu-id="7cc62-158">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="7cc62-158">remove_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="7cc62-159">Remover um manipulador de eventos adicionado anteriormente com add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="7cc62-159">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

> <span data-ttu-id="7cc62-160">[remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7cc62-160">public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken token)</span></span>

