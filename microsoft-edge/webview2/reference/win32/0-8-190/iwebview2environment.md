---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 81b6d9814af84995909112ea79f11fbfcf93b488
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886077"
---
# <span data-ttu-id="9c359-104">0.8.355-IWebView2Environment de interface</span><span class="sxs-lookup"><span data-stu-id="9c359-104">0.8.355 - interface IWebView2Environment</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment
  : public IUnknown
```

<span data-ttu-id="9c359-105">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="9c359-105">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="9c359-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="9c359-106">Summary</span></span>

 <span data-ttu-id="9c359-107">Parte</span><span class="sxs-lookup"><span data-stu-id="9c359-107">Members</span></span>                        | <span data-ttu-id="9c359-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="9c359-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9c359-109">WebView</span><span class="sxs-lookup"><span data-stu-id="9c359-109">CreateWebView</span></span>](#createwebview) | <span data-ttu-id="9c359-110">Crie assincronamente um novo [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="9c359-110">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>
[<span data-ttu-id="9c359-111">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="9c359-111">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="9c359-112">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="9c359-112">Create a new web resource response object.</span></span>

<span data-ttu-id="9c359-113">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="9c359-113">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="9c359-114">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="9c359-114">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="9c359-115">Parte</span><span class="sxs-lookup"><span data-stu-id="9c359-115">Members</span></span>

#### <span data-ttu-id="9c359-116">WebView</span><span class="sxs-lookup"><span data-stu-id="9c359-116">CreateWebView</span></span> 

<span data-ttu-id="9c359-117">Crie assincronamente um novo [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="9c359-117">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>

> <span data-ttu-id="9c359-118">público HRESULT [WebView](#createwebview)(HWND ParentWindow, manipulador[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="9c359-118">public HRESULT [CreateWebView](#createwebview)(HWND parentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="9c359-119">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="9c359-119">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="9c359-120">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="9c359-120">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="9c359-121">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="9c359-121">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="9c359-122">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c359-122">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="9c359-123">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="9c359-123">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

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

 <span data-ttu-id="9c359-124">É recomendável que o aplicativo manipule as mensagens do Gerenciador de reinicialização para que ele possa ser reiniciado normalmente quando o aplicativo estiver usando o Edge for WebView a partir de uma determinada instalação e essa instalação estiver sendo desinstalada.</span><span class="sxs-lookup"><span data-stu-id="9c359-124">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="9c359-125">Por exemplo, se um usuário instalar o Edge do canal de desenvolvimento e optar por usar o Edge desse canal para testar o aplicativo e, em seguida, desinstalar o Edge desse canal sem fechar o aplicativo, o aplicativo será reiniciado para permitir a desinstalação do canal de desenvolvimento ser bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9c359-125">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

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

#### <span data-ttu-id="9c359-126">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="9c359-126">CreateWebResourceResponse</span></span> 

<span data-ttu-id="9c359-127">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="9c359-127">Create a new web resource response object.</span></span>

> <span data-ttu-id="9c359-128">Public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo IStream \*, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR cabeçalhos,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="9c359-128">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="9c359-129">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="9c359-129">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="9c359-130">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="9c359-130">It's also possible to create this object with empty headers string and then use the [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="9c359-131">Para obter informações sobre outros parâmetros, consulte [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="9c359-131">For information on other parameters see [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span></span>

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

