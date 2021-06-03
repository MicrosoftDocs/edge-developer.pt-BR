---
description: Convenções de API Do Win32 C++ WebView2
title: Convenções de API Do Win32 C++ WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: b5a86751bfe3386058812ca166fa7cf9e0e201dc
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535640"
---
# <a name="win32-c-webview2-api-conventions"></a><span data-ttu-id="73564-104">Convenções de API Do Win32 C++ WebView2</span><span class="sxs-lookup"><span data-stu-id="73564-104">Win32 C++ WebView2 API conventions</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="73564-105">Plataformas com suporte:</span><span class="sxs-lookup"><span data-stu-id="73564-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73564-106">Win32</span><span class="sxs-lookup"><span data-stu-id="73564-106">Win32</span></span>
   :::column-end:::
:::row-end:::  

## <a name="prerequisites"></a><span data-ttu-id="73564-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="73564-107">Prerequisites</span></span>  

*   <span data-ttu-id="73564-108">Experiência usando a API Win32</span><span class="sxs-lookup"><span data-stu-id="73564-108">Experience using Win32 API</span></span>  

## <a name="async-methods"></a><span data-ttu-id="73564-109">Métodos Async</span><span class="sxs-lookup"><span data-stu-id="73564-109">Async methods</span></span>  

<span data-ttu-id="73564-110">Métodos assíncronos na API Do WebView2 Win32 C++ usam uma interface delegada para entrar em contato com você pelos seguintes motivos.</span><span class="sxs-lookup"><span data-stu-id="73564-110">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to contact you for the following reasons.</span></span>  

*   <span data-ttu-id="73564-111">O método assíncrono foi concluído.</span><span class="sxs-lookup"><span data-stu-id="73564-111">The async method has completed.</span></span>  
*   <span data-ttu-id="73564-112">O código de sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="73564-112">The success or failure code.</span></span>  
*   <span data-ttu-id="73564-113">O resultado do método assíncrono.</span><span class="sxs-lookup"><span data-stu-id="73564-113">The result of the asynchronous method.</span></span>  

<span data-ttu-id="73564-114">O parâmetro final para todos os métodos assíncronos é um ponteiro para uma interface delegada da qual você fornece uma implementação.</span><span class="sxs-lookup"><span data-stu-id="73564-114">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="73564-115">A interface delegada tem um único `Invoke` método que tem como primeiro parâmetro um do código de sucesso ou `HRESULT` falha.</span><span class="sxs-lookup"><span data-stu-id="73564-115">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="73564-116">Além disso, pode haver um segundo parâmetro que é o resultado do método se o método tiver um resultado.</span><span class="sxs-lookup"><span data-stu-id="73564-116">Additionally, there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="73564-117">Por exemplo, o [método ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] assume como o parâmetro final um `ICoreWebView2CapturePreviewCompletedHandler` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="73564-117">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="73564-118">Para enviar uma `CapturePreview` solicitação de método, você fornece uma instância do `ICoreWebView2CapturePreviewCompletedHandler` ponteiro que você implementa.</span><span class="sxs-lookup"><span data-stu-id="73564-118">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="73564-119">O trecho de código a seguir usa um método para implementar.</span><span class="sxs-lookup"><span data-stu-id="73564-119">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="73564-120">Implemente o `Invoke` método e `CoreWebView2` solicite seu método quando a `Invoke` `CapturePreview` solicitação for concluída.</span><span class="sxs-lookup"><span data-stu-id="73564-120">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="73564-121">O parâmetro único é `HRESULT` a descrição do código de sucesso ou falha da `CapturePreview` solicitação.</span><span class="sxs-lookup"><span data-stu-id="73564-121">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="73564-122">Como alternativa, para , você fornece uma instância que tem um método que fornece o código de sucesso ou `ICoreWebView2::ExecuteScript` `Invoke` falha da `ExecuteScript` solicitação.</span><span class="sxs-lookup"><span data-stu-id="73564-122">Alternately, for `ICoreWebView2::ExecuteScript`, you provide an instance that has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request.</span></span>  <span data-ttu-id="73564-123">Também forneça o segundo parâmetro que é o JSON do resultado da execução do script.</span><span class="sxs-lookup"><span data-stu-id="73564-123">Also provide the second parameter that is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="73564-124">Você pode implementar manualmente as `CompleteHandler` interfaces delegar ou usar a função [Callback (WRL)][CppCxWrlCallbackFunction].</span><span class="sxs-lookup"><span data-stu-id="73564-124">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [Callback function (WRL)][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="73564-125">A [função De retorno de chamada (WRL)][CppCxWrlCallbackFunction] é usada em todo o trecho de código WebView2 a seguir.</span><span class="sxs-lookup"><span data-stu-id="73564-125">The [Callback function (WRL)][CppCxWrlCallbackFunction] is used throughout the following WebView2 code snippet.</span></span>  

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

## <a name="events"></a><span data-ttu-id="73564-126">Eventos</span><span class="sxs-lookup"><span data-stu-id="73564-126">Events</span></span>  

<span data-ttu-id="73564-127">Os eventos na API WebView2 Win32 C++ usam o par de métodos e `add_EventName` para assinar e cancelar a assinatura de `remove_EventName` eventos.</span><span class="sxs-lookup"><span data-stu-id="73564-127">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="73564-128">O método pega uma interface de representante do manipulador de `add_EventName` eventos e devolve um token como um parâmetro de `EventRegistrationToken` saída.</span><span class="sxs-lookup"><span data-stu-id="73564-128">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` token as an output parameter.</span></span>  <span data-ttu-id="73564-129">O `remove_EventName` método pega um token e `EventRegistrationToken` cancela a assinatura de evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="73564-129">The `remove_EventName` method takes an `EventRegistrationToken` token and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="73564-130">As interfaces do representante do manipulador de eventos funcionam da mesma forma com as interfaces de representante concluídas do método assíncrono.</span><span class="sxs-lookup"><span data-stu-id="73564-130">Event handler delegate interfaces work similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="73564-131">Você implementa a interface delegada do manipulador de eventos e `CoreWebView2` envia um retorno de chamada sempre que o evento é executado.</span><span class="sxs-lookup"><span data-stu-id="73564-131">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event runs.</span></span>  <span data-ttu-id="73564-132">Cada interface delegada do manipulador de eventos tem um único método que tem um parâmetro `Invoke` de remetente seguido por um parâmetro args de evento.</span><span class="sxs-lookup"><span data-stu-id="73564-132">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="73564-133">O remetente é a instância do objeto no qual você se inscreve para eventos.</span><span class="sxs-lookup"><span data-stu-id="73564-133">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="73564-134">O parâmetro event args é uma interface que contém informações sobre o evento de disparo no momento.</span><span class="sxs-lookup"><span data-stu-id="73564-134">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="73564-135">Por exemplo, o `NavigationCompleted` evento on tem o par e `ICoreWebView2` `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` método.</span><span class="sxs-lookup"><span data-stu-id="73564-135">For instance, the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="73564-136">Ao enviar uma solicitação, você fornece uma instância da `ICoreWebView2NavigationCompletedEventHandler` qual você implementou `Invoke` anteriormente o método.</span><span class="sxs-lookup"><span data-stu-id="73564-136">When you send a request, you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="73564-137">Quando o `NavigationCompleted` evento é executado, seu `Invoke` método é solicitado.</span><span class="sxs-lookup"><span data-stu-id="73564-137">When the `NavigationCompleted` event runs, your `Invoke` method is requested.</span></span>  <span data-ttu-id="73564-138">O primeiro parâmetro executa o `NavigationCompleted` evento.</span><span class="sxs-lookup"><span data-stu-id="73564-138">The first parameter runs the `NavigationCompleted` event.</span></span>  <span data-ttu-id="73564-139">O segundo parâmetro contém informações sobre se a navegação foi concluída com êxito e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="73564-139">The second parameter contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="73564-140">Semelhante à interface de representante do manipulador concluída do método assíncrono, use uma das seguintes ações para defini-la.</span><span class="sxs-lookup"><span data-stu-id="73564-140">Similar to the async method completed handler delegate interface, use one of the following actions to set it up.</span></span>  

*   <span data-ttu-id="73564-141">Implemente-o diretamente.</span><span class="sxs-lookup"><span data-stu-id="73564-141">Implement it directly.</span></span>  
*   <span data-ttu-id="73564-142">Use a função De retorno de chamada [(WRL)][CppCxWrlCallbackFunction] usada no trecho de código WebView2 a seguir.</span><span class="sxs-lookup"><span data-stu-id="73564-142">Use the [Callback function (WRL)][CppCxWrlCallbackFunction] function that is used in the following WebView2 code snippet.</span></span>  

<!-- todo:  what is async method completed handler delegate interface?  Is there a shorter name for it?  -->  

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

## <a name="strings"></a><span data-ttu-id="73564-143">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="73564-143">Strings</span></span>  

<span data-ttu-id="73564-144">Parâmetros de saída de cadeia de caracteres `LPWSTR` são cadeias de caracteres terminadas nulos.</span><span class="sxs-lookup"><span data-stu-id="73564-144">String output parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="73564-145">O solicitante fornece a cadeia de caracteres usando `CoTaskMemAlloc` .</span><span class="sxs-lookup"><span data-stu-id="73564-145">The requester provides the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="73564-146">A propriedade é transferida para o solicitante e é responsabilidade do solicitante liberar a memória usando `CoTaskMemFree` .</span><span class="sxs-lookup"><span data-stu-id="73564-146">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="73564-147">Parâmetros de entrada de cadeia de caracteres `LPCWSTR` são cadeias de caracteres terminadas nulos.</span><span class="sxs-lookup"><span data-stu-id="73564-147">String input parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="73564-148">O solicitante garante que a cadeia de caracteres seja válida durante a solicitação da função síncrona.</span><span class="sxs-lookup"><span data-stu-id="73564-148">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="73564-149">Se o receptor deve armazenar o valor em algum ponto após a conclusão da solicitação de função, o receptor deve dar uma cópia associada do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="73564-149">If the receiver must store the value to some point after the function request completes, the receiver must give an associated copy of the string value.</span></span>  

## <a name="uri-and-json-parsing"></a><span data-ttu-id="73564-150">Análise de URI e JSON</span><span class="sxs-lookup"><span data-stu-id="73564-150">URI and JSON parsing</span></span>  

<span data-ttu-id="73564-151">Vários métodos fornecem ou aceitam URIs e JSON como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="73564-151">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="73564-152">Use sua biblioteca preferencial para analisar e gerar as cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="73564-152">Use your preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="73564-153">Se WinRT estiver disponível para seu aplicativo, você poderá usar os métodos e para analisar ou produzir cadeias de caracteres JSON ou métodos para analisar e `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` produzir `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` URIs.</span><span class="sxs-lookup"><span data-stu-id="73564-153">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="73564-154">Ambos os métodos funcionam em aplicativos Win32.</span><span class="sxs-lookup"><span data-stu-id="73564-154">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="73564-155">Se você usar e analisar URIs, talvez você queira usar os seguintes sinalizadores de criação de URI para ter um comportamento mais próximo da análise de URI no `IUri` `CreateUri` `CreateUri` WebView.</span><span class="sxs-lookup"><span data-stu-id="73564-155">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

## <a name="see-also"></a><span data-ttu-id="73564-156">Consulte também</span><span class="sxs-lookup"><span data-stu-id="73564-156">See also</span></span>  

*   <span data-ttu-id="73564-157">Para começar a usar WebView2 Win32 C/C++, navegue até [Começar com guias webView2][Webview2IndexGetStarted].</span><span class="sxs-lookup"><span data-stu-id="73564-157">To get started using WebView2 Win32 C/C++, navigate to [Get started with WebView2][Webview2IndexGetStarted] guides.</span></span>  
*   <span data-ttu-id="73564-158">Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="73564-158">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="73564-159">Entrar em contato com a equipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="73564-159">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2GetStartedWin32]: ../get-started/win32.md "Começar com WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview - interface ICoreWebView2 | Microsoft Docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Função de retorno de chamada (WRL) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  
