---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 2f376cdd7098c512a8c7a0a3a463f5302f0bfbd7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652782"
---
# <span data-ttu-id="55479-104">interface ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="55479-104">interface ICoreWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="55479-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="55479-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="55479-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="55479-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Environment
  : public IUnknown
```

<span data-ttu-id="55479-107">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="55479-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="55479-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="55479-108">Summary</span></span>

 <span data-ttu-id="55479-109">Parte</span><span class="sxs-lookup"><span data-stu-id="55479-109">Members</span></span>                        | <span data-ttu-id="55479-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="55479-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="55479-111">CreateCoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="55479-111">CreateCoreWebView2Host</span></span>](#createcorewebview2host) | <span data-ttu-id="55479-112">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="55479-112">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="55479-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="55479-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="55479-114">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="55479-114">Create a new web resource response object.</span></span>
[<span data-ttu-id="55479-115">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="55479-115">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="55479-116">As informações de versão do navegador do [ICoreWebView2Environment]()atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="55479-116">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="55479-117">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="55479-117">add_NewBrowserVersionAvailable</span></span>](#add_newbrowserversionavailable) | <span data-ttu-id="55479-118">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="55479-118">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="55479-119">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="55479-119">remove_NewBrowserVersionAvailable</span></span>](#remove_newbrowserversionavailable) | <span data-ttu-id="55479-120">Remover um manipulador de eventos adicionado anteriormente com add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="55479-120">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

<span data-ttu-id="55479-121">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="55479-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="55479-122">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="55479-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="55479-123">Parte</span><span class="sxs-lookup"><span data-stu-id="55479-123">Members</span></span>

#### <span data-ttu-id="55479-124">CreateCoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="55479-124">CreateCoreWebView2Host</span></span> 

<span data-ttu-id="55479-125">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="55479-125">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="55479-126">Public HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND ParentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="55479-126">public HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND parentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="55479-127">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="55479-127">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="55479-128">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="55479-128">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="55479-129">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="55479-129">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="55479-130">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55479-130">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="55479-131">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="55479-131">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateCoreWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
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

// This is the callback passed to CreateWebViewEnvironmnetWithDetails.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Host(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2HostCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2HostCompleted)
                              .Get()));
    return S_OK;
}
```

 <span data-ttu-id="55479-132">É recomendável que o aplicativo manipule as mensagens do Gerenciador de reinicialização para que ele possa ser reiniciado normalmente quando o aplicativo estiver usando o Edge for WebView a partir de uma determinada instalação e essa instalação estiver sendo desinstalada.</span><span class="sxs-lookup"><span data-stu-id="55479-132">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="55479-133">Por exemplo, se um usuário instalar o Edge do canal de desenvolvimento e optar por usar o Edge desse canal para testar o aplicativo e, em seguida, desinstalar o Edge desse canal sem fechar o aplicativo, o aplicativo será reiniciado para permitir a desinstalação do canal de desenvolvimento ser bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="55479-133">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

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

#### <span data-ttu-id="55479-134">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="55479-134">CreateWebResourceResponse</span></span> 

<span data-ttu-id="55479-135">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="55479-135">Create a new web resource response object.</span></span>

> <span data-ttu-id="55479-136">Public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo IStream \*, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR cabeçalhos,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="55479-136">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="55479-137">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="55479-137">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="55479-138">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="55479-138">It's also possible to create this object with empty headers string and then use the [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="55479-139">Para obter informações sobre outros parâmetros, consulte [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="55479-139">For information on other parameters see [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).</span></span>

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

#### <span data-ttu-id="55479-140">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="55479-140">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="55479-141">As informações de versão do navegador do [ICoreWebView2Environment]()atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="55479-141">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="55479-142">público HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="55479-142">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="55479-143">Isso corresponde ao formato da API GetCoreWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="55479-143">This matches the format of the GetCoreWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="55479-144">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="55479-144">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### <span data-ttu-id="55479-145">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="55479-145">add_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="55479-146">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="55479-146">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="55479-147">Public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="55479-147">public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="55479-148">Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView.</span><span class="sxs-lookup"><span data-stu-id="55479-148">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="55479-149">Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="55479-149">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="55479-150">Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="55479-150">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="55479-151">Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro.</span><span class="sxs-lookup"><span data-stu-id="55479-151">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="55479-152">Ou simplesmente solicitar que o usuário reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55479-152">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](
                ICoreWebView2Environment* sender,
                ICoreWebView2NewBrowserVersionAvailableEventArgs* args) -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
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

#### <span data-ttu-id="55479-153">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="55479-153">remove_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="55479-154">Remover um manipulador de eventos adicionado anteriormente com add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="55479-154">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

> <span data-ttu-id="55479-155">[remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="55479-155">public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken token)</span></span>

