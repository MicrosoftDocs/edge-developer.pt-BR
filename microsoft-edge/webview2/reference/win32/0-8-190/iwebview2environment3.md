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
ms.openlocfilehash: 43becb7f4ec9903557ccd558319e233266ac2ea1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652426"
---
# <span data-ttu-id="39874-104">interface IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="39874-104">interface IWebView2Environment3</span></span> 

> [!NOTE]
> <span data-ttu-id="39874-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="39874-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="39874-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="39874-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="39874-107">Funcionalidades adicionais implementadas pelo objeto Environment.</span><span class="sxs-lookup"><span data-stu-id="39874-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="39874-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="39874-108">Summary</span></span>

 <span data-ttu-id="39874-109">Parte</span><span class="sxs-lookup"><span data-stu-id="39874-109">Members</span></span>                        | <span data-ttu-id="39874-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="39874-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="39874-111">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="39874-111">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="39874-112">O evento NewVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="39874-112">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="39874-113">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="39874-113">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="39874-114">Remover um manipulador de eventos adicionado anteriormente com add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="39874-114">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="39874-115">Consulte a interface [IWebView2Environment](IWebView2Environment.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="39874-115">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="39874-116">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="39874-116">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="39874-117">Parte</span><span class="sxs-lookup"><span data-stu-id="39874-117">Members</span></span>

#### <span data-ttu-id="39874-118">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="39874-118">add_NewVersionAvailable</span></span> 

<span data-ttu-id="39874-119">O evento NewVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="39874-119">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="39874-120">Public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="39874-120">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="39874-121">Para usar a versão mais recente do navegador, você deve criar um novo [IWebView2Environment](IWebView2Environment.md) e [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="39874-121">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="39874-122">O evento só será disparado para a nova versão do mesmo canal de borda em que o código está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="39874-122">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="39874-123">Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="39874-123">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="39874-124">Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, você deve fechar o [IWebView2Environment](IWebView2Environment.md) e o IWebView2WebViews que estão usando a versão mais antiga do navegador primeiro.</span><span class="sxs-lookup"><span data-stu-id="39874-124">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="39874-125">Ou simplesmente solicitar que o usuário reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39874-125">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewVersionAvailable(
        Callback<IWebView2NewVersionAvailableEventHandler>(
            [this](IWebView2Environment* sender, IWebView2NewVersionAvailableEventArgs* args)
                -> HRESULT {
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

#### <span data-ttu-id="39874-126">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="39874-126">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="39874-127">Remover um manipulador de eventos adicionado anteriormente com add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="39874-127">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="39874-128">[remove_NewVersionAvailable](#remove_newversionavailable)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="39874-128">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

