---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalEnvironment
ms.openlocfilehash: e7ccb108c137e54635c6e5b69f9bc615ff8ff018
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011129"
---
# <span data-ttu-id="983bc-104">0.9.579-ICoreWebView2ExperimentalEnvironment de interface</span><span class="sxs-lookup"><span data-stu-id="983bc-104">0.9.579 - interface ICoreWebView2ExperimentalEnvironment</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironment
  : public IUnknown
```

<span data-ttu-id="983bc-105">Essa interface é uma extensão da [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="983bc-105">This interface is an extension of the [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="983bc-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="983bc-106">Summary</span></span>

 <span data-ttu-id="983bc-107">Parte</span><span class="sxs-lookup"><span data-stu-id="983bc-107">Members</span></span>                        | <span data-ttu-id="983bc-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="983bc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="983bc-109">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="983bc-109">CreateCoreWebView2CompositionController</span></span>](#createcorewebview2compositioncontroller) | <span data-ttu-id="983bc-110">Crie assincronamente um novo WebView para uso com hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="983bc-110">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="983bc-111">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="983bc-111">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="983bc-112">Crie uma [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vazia.</span><span class="sxs-lookup"><span data-stu-id="983bc-112">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="983bc-113">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="983bc-113">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="983bc-114">Retorna o provedor de automação da interface do usuário para o ICoreWebView2CompositionController que corresponde ao HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="983bc-114">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="983bc-115">Um objeto que implementa a interface [ICoreWebView2ExperimentalEnvironment]() também implementa [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="983bc-115">An object implementing the [ICoreWebView2ExperimentalEnvironment]() interface will also implement [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="983bc-116">Parte</span><span class="sxs-lookup"><span data-stu-id="983bc-116">Members</span></span>

#### <span data-ttu-id="983bc-117">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="983bc-117">CreateCoreWebView2CompositionController</span></span> 

<span data-ttu-id="983bc-118">Crie assincronamente um novo WebView para uso com hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="983bc-118">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="983bc-119">Public HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND ParentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="983bc-119">public HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND parentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="983bc-120">parentWindow é o HWND no qual o aplicativo conectará a árvore visual do WebView.</span><span class="sxs-lookup"><span data-stu-id="983bc-120">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="983bc-121">Esse será o HWND que o aplicativo receberá a entrada de ponteiro/mouse para o WebView (e será necessário usar SendMouseInput/SendPointerInput para encaminhar).</span><span class="sxs-lookup"><span data-stu-id="983bc-121">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="983bc-122">Se o aplicativo mover a árvore visual da WebView para abaixo de uma janela diferente, então precisará chamar put_ParentWindow para atualizar o novo HWND pai da árvore visual.</span><span class="sxs-lookup"><span data-stu-id="983bc-122">If the app moves the WebView visual tree to underneath a different window, then it needs to call put_ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="983bc-123">Use put_RootVisualTarget no CoreWebView2CompositionController criado para fornecer um Visual para hospedar a árvore visual do navegador.</span><span class="sxs-lookup"><span data-stu-id="983bc-123">Use put_RootVisualTarget on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="983bc-124">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="983bc-124">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="983bc-125">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="983bc-125">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
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
    auto options = Microsoft::WRL::Make<CoreWebView2ExperimentalEnvironmentOptions>();
    CHECK_FAILURE(options->put_IsSingleSignOnUsingOSPrimaryAccountEnabled(
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
 <span data-ttu-id="983bc-126">É recomendável que o aplicativo manipule as mensagens do Gerenciador de reinicialização para que ele possa ser reiniciado normalmente quando o aplicativo estiver usando o Edge for WebView a partir de uma determinada instalação e essa instalação estiver sendo desinstalada.</span><span class="sxs-lookup"><span data-stu-id="983bc-126">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="983bc-127">Por exemplo, se um usuário instalar o Edge do canal de desenvolvimento e optar por usar o Edge desse canal para testar o aplicativo e, em seguida, desinstalar o Edge desse canal sem fechar o aplicativo, o aplicativo será reiniciado para permitir a desinstalação do canal de desenvolvimento ser bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="983bc-127">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
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

#### <span data-ttu-id="983bc-128">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="983bc-128">CreateCoreWebView2PointerInfo</span></span> 

<span data-ttu-id="983bc-129">Crie uma [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vazia.</span><span class="sxs-lookup"><span data-stu-id="983bc-129">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="983bc-130">Public HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="983bc-130">public HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="983bc-131">O [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) retornado precisa ser preenchido com todas as informações relevantes antes de chamar SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="983bc-131">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="983bc-132">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="983bc-132">GetProviderForHwnd</span></span> 

<span data-ttu-id="983bc-133">Retorna o provedor de automação da interface do usuário para o ICoreWebView2CompositionController que corresponde ao HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="983bc-133">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="983bc-134">Public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hWnd, IUnknown \* \* Provider)</span><span class="sxs-lookup"><span data-stu-id="983bc-134">public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hwnd, IUnknown \*\* provider)</span></span>

