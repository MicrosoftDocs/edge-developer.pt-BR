---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: c3ce6a49be1abf12d66f69da6d2ff6ff9d9f5b68
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652781"
---
# <span data-ttu-id="09649-104">interface IWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="09649-104">interface IWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="09649-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="09649-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="09649-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="09649-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment
  : public IUnknown
```

<span data-ttu-id="09649-107">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="09649-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="09649-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="09649-108">Summary</span></span>

 <span data-ttu-id="09649-109">Parte</span><span class="sxs-lookup"><span data-stu-id="09649-109">Members</span></span>                        | <span data-ttu-id="09649-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="09649-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09649-111">WebView</span><span class="sxs-lookup"><span data-stu-id="09649-111">CreateWebView</span></span>](#createwebview) | <span data-ttu-id="09649-112">Crie assincronamente um novo [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="09649-112">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>
[<span data-ttu-id="09649-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="09649-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="09649-114">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="09649-114">Create a new web resource response object.</span></span>

<span data-ttu-id="09649-115">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="09649-115">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="09649-116">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="09649-116">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="09649-117">Parte</span><span class="sxs-lookup"><span data-stu-id="09649-117">Members</span></span>

#### <span data-ttu-id="09649-118">WebView</span><span class="sxs-lookup"><span data-stu-id="09649-118">CreateWebView</span></span> 

<span data-ttu-id="09649-119">Crie assincronamente um novo [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="09649-119">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>

> <span data-ttu-id="09649-120">público HRESULT [WebView](#createwebview)(HWND ParentWindow, manipulador[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="09649-120">public HRESULT [CreateWebView](#createwebview)(HWND parentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="09649-121">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="09649-121">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="09649-122">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="09649-122">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="09649-123">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="09649-123">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="09649-124">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="09649-124">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="09649-125">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="09649-125">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView(InitializeWebViewFlags webviewInitFlags)
{
    m_lastUsedInitFlags = webviewInitFlags;
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<IWebView2CreateWebView2EnvironmentCompletedHandler>(
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
    HRESULT result, IWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateWebView(
            m_mainWindow, Callback<IWebView2CreateWebViewCompletedHandler>(
                              this, &AppWindow::OnCreateWebViewCompleted)
                              .Get()));
    return S_OK;
}
```

 <span data-ttu-id="09649-126">É recomendável que o aplicativo manipule as mensagens do Gerenciador de reinicialização para que ele possa ser reiniciado normalmente quando o aplicativo estiver usando o Edge for WebView a partir de uma determinada instalação e essa instalação estiver sendo desinstalada.</span><span class="sxs-lookup"><span data-stu-id="09649-126">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="09649-127">Por exemplo, se um usuário instalar o Edge do canal de desenvolvimento e optar por usar o Edge desse canal para testar o aplicativo e, em seguida, desinstalar o Edge desse canal sem fechar o aplicativo, o aplicativo será reiniciado para permitir a desinstalação do canal de desenvolvimento ser bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="09649-127">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

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

#### <span data-ttu-id="09649-128">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="09649-128">CreateWebResourceResponse</span></span> 

<span data-ttu-id="09649-129">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="09649-129">Create a new web resource response object.</span></span>

> <span data-ttu-id="09649-130">Public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo IStream \*, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR cabeçalhos,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="09649-130">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="09649-131">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="09649-131">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="09649-132">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="09649-132">It's also possible to create this object with empty headers string and then use the [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="09649-133">Para obter informações sobre outros parâmetros, consulte [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="09649-133">For information on other parameters see [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span></span>

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

