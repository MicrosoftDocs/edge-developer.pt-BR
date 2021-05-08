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
# <a name="win32-c-webview2-api-conventions"></a>Convenções de API Do Win32 C++ WebView2  

:::row:::
   :::column span="1":::
      Plataformas com suporte:
   :::column-end:::
   :::column span="2":::
      Win32
   :::column-end:::
:::row-end:::  

## <a name="prerequisites"></a>Pré-requisitos  

*   Experiência usando a API Win32  

## <a name="async-methods"></a>Métodos Async  

Métodos assíncronos na API Do WebView2 Win32 C++ usam uma interface delegada para entrar em contato com você pelos seguintes motivos.  

*   O método assíncrono foi concluído.  
*   O código de sucesso ou falha.  
*   O resultado do método assíncrono.  

O parâmetro final para todos os métodos assíncronos é um ponteiro para uma interface delegada da qual você fornece uma implementação.  

A interface delegada tem um único `Invoke` método que tem como primeiro parâmetro um do código de sucesso ou `HRESULT` falha.  Além disso, pode haver um segundo parâmetro que é o resultado do método se o método tiver um resultado.  Por exemplo, o [método ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] assume como o parâmetro final um `ICoreWebView2CapturePreviewCompletedHandler` ponteiro.  Para enviar uma `CapturePreview` solicitação de método, você fornece uma instância do `ICoreWebView2CapturePreviewCompletedHandler` ponteiro que você implementa.  O trecho de código a seguir usa um método para implementar.  

```cpp
HRESULT Invoke(HRESULT result)
```  

Implemente o `Invoke` método e `CoreWebView2` solicite seu método quando a `Invoke` `CapturePreview` solicitação for concluída.  O parâmetro único é `HRESULT` a descrição do código de sucesso ou falha da `CapturePreview` solicitação.  

Como alternativa, para , você fornece uma instância que tem um método que fornece o código de sucesso ou `ICoreWebView2::ExecuteScript` `Invoke` falha da `ExecuteScript` solicitação.  Também forneça o segundo parâmetro que é o JSON do resultado da execução do script.  

Você pode implementar manualmente as `CompleteHandler` interfaces delegar ou usar a função [Callback (WRL)][CppCxWrlCallbackFunction].  A [função De retorno de chamada (WRL)][CppCxWrlCallbackFunction] é usada em todo o trecho de código WebView2 a seguir.  

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

## <a name="events"></a>Eventos  

Os eventos na API WebView2 Win32 C++ usam o par de métodos e `add_EventName` para assinar e cancelar a assinatura de `remove_EventName` eventos.  O método pega uma interface de representante do manipulador de `add_EventName` eventos e devolve um token como um parâmetro de `EventRegistrationToken` saída.  O `remove_EventName` método pega um token e `EventRegistrationToken` cancela a assinatura de evento correspondente.  

As interfaces do representante do manipulador de eventos funcionam da mesma forma com as interfaces de representante concluídas do método assíncrono.  Você implementa a interface delegada do manipulador de eventos e `CoreWebView2` envia um retorno de chamada sempre que o evento é executado.  Cada interface delegada do manipulador de eventos tem um único método que tem um parâmetro `Invoke` de remetente seguido por um parâmetro args de evento.  O remetente é a instância do objeto no qual você se inscreve para eventos.  O parâmetro event args é uma interface que contém informações sobre o evento de disparo no momento.  

Por exemplo, o `NavigationCompleted` evento on tem o par e `ICoreWebView2` `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` método.  Ao enviar uma solicitação, você fornece uma instância da `ICoreWebView2NavigationCompletedEventHandler` qual você implementou `Invoke` anteriormente o método.  Quando o `NavigationCompleted` evento é executado, seu `Invoke` método é solicitado.  O primeiro parâmetro executa o `NavigationCompleted` evento.  O segundo parâmetro contém informações sobre se a navegação foi concluída com êxito e assim por diante.  

Semelhante à interface de representante do manipulador concluída do método assíncrono, use uma das seguintes ações para defini-la.  

*   Implemente-o diretamente.  
*   Use a função De retorno de chamada [(WRL)][CppCxWrlCallbackFunction] usada no trecho de código WebView2 a seguir.  

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

## <a name="strings"></a>Cadeias de caracteres  

Parâmetros de saída de cadeia de caracteres `LPWSTR` são cadeias de caracteres terminadas nulos.  O solicitante fornece a cadeia de caracteres usando `CoTaskMemAlloc` .  A propriedade é transferida para o solicitante e é responsabilidade do solicitante liberar a memória usando `CoTaskMemFree` .  

Parâmetros de entrada de cadeia de caracteres `LPCWSTR` são cadeias de caracteres terminadas nulos.  O solicitante garante que a cadeia de caracteres seja válida durante a solicitação da função síncrona.  Se o receptor deve armazenar o valor em algum ponto após a conclusão da solicitação de função, o receptor deve dar uma cópia associada do valor da cadeia de caracteres.  

## <a name="uri-and-json-parsing"></a>Análise de URI e JSON  

Vários métodos fornecem ou aceitam URIs e JSON como cadeias de caracteres.  Use sua biblioteca preferencial para analisar e gerar as cadeias de caracteres.  

Se WinRT estiver disponível para seu aplicativo, você poderá usar os métodos e para analisar ou produzir cadeias de caracteres JSON ou métodos para analisar e `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` produzir `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` URIs.  Ambos os métodos funcionam em aplicativos Win32.  

Se você usar e analisar URIs, talvez você queira usar os seguintes sinalizadores de criação de URI para ter um comportamento mais próximo da análise de URI no `IUri` `CreateUri` `CreateUri` WebView.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

## <a name="see-also"></a>Ver também  

*   Para começar a usar WebView2 Win32 C/C++, navegue até [Começar com guias webView2][Webview2IndexGetStarted].  
*   Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2GetStartedWin32]: ../get-started/win32.md "Começar com WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview - interface ICoreWebView2 | Microsoft Docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Função de retorno de chamada (WRL) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  
