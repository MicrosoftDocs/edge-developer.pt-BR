---
description: Convenções de API do Win32 C++ WebView2
title: Convenções de API do Win32 C++ WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: c8792133da2b858cfaa456df5a7dce26c3c65154
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895532"
---
# <span data-ttu-id="a06d0-104">Convenções de API do Win32 C++ WebView2</span><span class="sxs-lookup"><span data-stu-id="a06d0-104">Win32 C++ WebView2 API conventions</span></span>  

## <span data-ttu-id="a06d0-105">Métodos assíncronos</span><span class="sxs-lookup"><span data-stu-id="a06d0-105">Async Methods</span></span>  

<span data-ttu-id="a06d0-106">Métodos assíncronos na API Win32 C++ do WebView2 usam uma interface de representante para retornar ao retorno de chamada para indicar quando o método Async foi concluído, o código de êxito ou falha e para alguns, o resultado do método assíncrono.</span><span class="sxs-lookup"><span data-stu-id="a06d0-106">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to callback to you to indicate when the async method has completed, the success or failure code, and for some, the result of the asynchronous method.</span></span>  <span data-ttu-id="a06d0-107">O parâmetro final para todos os métodos assíncronos é um ponteiro para uma interface delegada da qual você fornece uma implementação.</span><span class="sxs-lookup"><span data-stu-id="a06d0-107">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="a06d0-108">A interface do representante tem um único `Invoke` método que assume como primeiro parâmetro um `HRESULT` dos códigos de sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="a06d0-108">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="a06d0-109">Além disso, pode haver um segundo parâmetro que é o resultado do método se o método tiver um resultado.</span><span class="sxs-lookup"><span data-stu-id="a06d0-109">Additionally there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="a06d0-110">Por exemplo, o método [ICoreWebView2:: CapturePreview][Webview2ReferenceWin3209538Icorewebview2CapturePreview] usa como o parâmetro final de um `ICoreWebView2CapturePreviewCompletedHandler` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="a06d0-110">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin3209538Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="a06d0-111">Para enviar uma `CapturePreview` solicitação de método, você fornece uma instância do `ICoreWebView2CapturePreviewCompletedHandler` ponteiro implementada.</span><span class="sxs-lookup"><span data-stu-id="a06d0-111">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="a06d0-112">O trecho de código a seguir usa um método para implementar.</span><span class="sxs-lookup"><span data-stu-id="a06d0-112">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="a06d0-113">Você implementa o `Invoke` método e `CoreWebView2` solicita `Invoke` que seu método quando a `CapturePreview` solicitação for concluída.</span><span class="sxs-lookup"><span data-stu-id="a06d0-113">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="a06d0-114">O único parâmetro é a `HRESULT` Descrição do código de sucesso ou falha da `CapturePreview` solicitação.</span><span class="sxs-lookup"><span data-stu-id="a06d0-114">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="a06d0-115">Ou para `ICoreWebView2::ExecuteScript` , você fornece uma instância que `ICoreWebView2ExecuteScriptCompletedHandler` tem um `Invoke` método que fornece o código de êxito ou falha da `ExecuteScript` solicitação, bem como o segundo parâmetro `resultObjectAsJson` que é o JSON do resultado da execução do script.</span><span class="sxs-lookup"><span data-stu-id="a06d0-115">Or for `ICoreWebView2::ExecuteScript`, you provide an instance of `ICoreWebView2ExecuteScriptCompletedHandler` which has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request as well as the second parameter `resultObjectAsJson` which is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="a06d0-116">Você pode implementar manualmente as `CompleteHandler` interfaces de representante ou pode usar a [função de retorno de chamada WRL][CppCxWrlCallbackFunction].</span><span class="sxs-lookup"><span data-stu-id="a06d0-116">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [WRL Callback function][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="a06d0-117">A função callback é usada em todo o trecho de código WebView2 a seguir.</span><span class="sxs-lookup"><span data-stu-id="a06d0-117">The Callback function is used throughout the following WebView2 code snippet.</span></span>  

```cpp
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

## <span data-ttu-id="a06d0-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="a06d0-118">Events</span></span>  

<span data-ttu-id="a06d0-119">Os eventos na API Win32 C++ do WebView2 usam `add_EventName` o `remove_EventName` par de método e para assinar e cancelar a assinatura de eventos.</span><span class="sxs-lookup"><span data-stu-id="a06d0-119">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="a06d0-120">O `add_EventName` método usa uma interface do representante do manipulador de eventos e retorna um `EventRegistrationToken` parâmetro como out.</span><span class="sxs-lookup"><span data-stu-id="a06d0-120">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` as an out parameter.</span></span>  <span data-ttu-id="a06d0-121">O `remove_EventName` método faz uma `EventRegistrationToken` e cancela a assinatura da assinatura de evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a06d0-121">The `remove_EventName` method takes an `EventRegistrationToken` and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="a06d0-122">As interfaces do representante do manipulador de eventos funcionam de forma muito semelhante ao método Async concluído interfaces de representante do manipulador.</span><span class="sxs-lookup"><span data-stu-id="a06d0-122">Event handler delegate interfaces work very similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="a06d0-123">Você implementa a interface do representante do manipulador de eventos e `CoreWebView2` envia um retorno de chamada sempre que o evento é acionado.</span><span class="sxs-lookup"><span data-stu-id="a06d0-123">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event fires.</span></span>  <span data-ttu-id="a06d0-124">Cada interface do representante do manipulador de eventos tem um único `Invoke` método que tem um parâmetro Sender seguido por um parâmetro args de evento.</span><span class="sxs-lookup"><span data-stu-id="a06d0-124">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="a06d0-125">O remetente é a instância do objeto na qual você assinou eventos.</span><span class="sxs-lookup"><span data-stu-id="a06d0-125">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="a06d0-126">O parâmetro args de evento é uma interface que contém informações sobre o evento de acionamento no momento.</span><span class="sxs-lookup"><span data-stu-id="a06d0-126">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="a06d0-127">Por exemplo `NavigationCompleted` , o evento ativado `ICoreWebView2` tem o `ICoreWebView2::add_NavigationCompleted` par de método e `ICoreWebView2::remove_NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="a06d0-127">For instance the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="a06d0-128">Ao solicitar o complemento, você fornece uma instância do `ICoreWebView2NavigationCompletedEventHandler` método implementado anteriormente `Invoke` .</span><span class="sxs-lookup"><span data-stu-id="a06d0-128">When you request add you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="a06d0-129">Quando o `NavigationCompleted` evento é acionado, seu `Invoke` método é solicitado.</span><span class="sxs-lookup"><span data-stu-id="a06d0-129">When the `NavigationCompleted` event fires, your `Invoke` method is requested.</span></span>  <span data-ttu-id="a06d0-130">O primeiro parâmetro é o `ICoreWebView2` que está acionando o `NavigationCompleted` evento.</span><span class="sxs-lookup"><span data-stu-id="a06d0-130">The first parameter is the `ICoreWebView2` which is firing the `NavigationCompleted` event.</span></span>  <span data-ttu-id="a06d0-131">O segundo parâmetro é o `ICoreWebView2NavigationCompletedEventArgs` que contém informações sobre se a navegação foi concluída com sucesso e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a06d0-131">The second parameter is the `ICoreWebView2NavigationCompletedEventArgs` which contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="a06d0-132">Da mesma forma que o método Async concluiu a interface do representante, você pode implementá-lo diretamente ou pode usar a função de retorno de chamada WRL que é usada no seguinte trecho de código WebView2.</span><span class="sxs-lookup"><span data-stu-id="a06d0-132">Similarly to the async method completed handler delegate interface you are able to implement it yourself directly, or you may use the WRL Callback function that is used in the following WebView2 code snippet.</span></span>  

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
                COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                {
                    // Do something here if you want to handle a specific error case.
                    // In most cases it is not necessary, because the WebView
                    // displays an error page automatically.
                }
            }
            m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
            m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
            return S_OK;
        })
        .Get(),
    &m_navigationCompletedToken));
```  

## <span data-ttu-id="a06d0-133">Seqüências</span><span class="sxs-lookup"><span data-stu-id="a06d0-133">Strings</span></span>  

<span data-ttu-id="a06d0-134">Parâmetros de cadeia de caracteres externa são `LPWSTR` cadeias de caracteres terminadas por nulo.</span><span class="sxs-lookup"><span data-stu-id="a06d0-134">String out parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="a06d0-135">O solicitante aloca a cadeia de caracteres usando `CoTaskMemAlloc` .</span><span class="sxs-lookup"><span data-stu-id="a06d0-135">The requester allocates the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="a06d0-136">A propriedade é transferida para o solicitante e fica até o solicitante liberar a memória usando `CoTaskMemFree` .</span><span class="sxs-lookup"><span data-stu-id="a06d0-136">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="a06d0-137">Cadeia de caracteres em parâmetros são `LPCWSTR` cadeias de caracteres terminadas por nulo.</span><span class="sxs-lookup"><span data-stu-id="a06d0-137">String in parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="a06d0-138">O solicitante garante que a cadeia de caracteres é válida para a duração da solicitação de função síncrona.</span><span class="sxs-lookup"><span data-stu-id="a06d0-138">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="a06d0-139">Se o receptor deve reter esse valor para algum ponto após a conclusão da solicitação de função, o receptor deve atribuir uma cópia associada do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a06d0-139">If the receiver must retain that value to some point after the function request completes, the receiver must allocate an associated copy of the string value.</span></span>  

## <span data-ttu-id="a06d0-140">Análise de URI e JSON</span><span class="sxs-lookup"><span data-stu-id="a06d0-140">URI and JSON parsing</span></span>  

<span data-ttu-id="a06d0-141">Vários métodos fornecem ou aceitam URIs e JSON como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a06d0-141">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="a06d0-142">Use sua própria biblioteca preferida para analisar e gerar as cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a06d0-142">Please use your own preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="a06d0-143">Se o WinRT estiver disponível para o seu aplicativo, você poderá usar os `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` métodos e para analisar ou produzir cadeias de caracteres JSON ou `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` métodos para analisar e produzir URIs.</span><span class="sxs-lookup"><span data-stu-id="a06d0-143">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="a06d0-144">Os dois métodos funcionam em aplicativos Win32.</span><span class="sxs-lookup"><span data-stu-id="a06d0-144">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="a06d0-145">Se você usar `IUri` e `CreateUri` para analisar URIs, talvez queira usar os seguintes sinalizadores de criação de URI para ter `CreateUri` comportamento mais próximo da análise de URI no WebView.</span><span class="sxs-lookup"><span data-stu-id="a06d0-145">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin3209538Icorewebview2CapturePreview]: ../reference/win32/0-9-538/icorewebview2.md#capturepreview "CapturePreview-interface ICoreWebView2 | Documentos da Microsoft"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Função callback (WRL) | Documentos da Microsoft"  
