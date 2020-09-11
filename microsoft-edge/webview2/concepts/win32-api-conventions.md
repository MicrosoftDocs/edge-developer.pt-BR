---
description: Convenções de API do Win32 C++ WebView2
title: Convenções de API do Win32 C++ WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 6c596b038e871caa5a364991351636f51ef7d685
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010681"
---
# Convenções de API do Win32 C++ WebView2  

## Métodos assíncronos  

Métodos assíncronos na API Win32 C++ do WebView2 usam uma interface de representante para retornar ao retorno de chamada para indicar quando o método Async foi concluído, o código de êxito ou falha e para alguns, o resultado do método assíncrono.  O parâmetro final para todos os métodos assíncronos é um ponteiro para uma interface delegada da qual você fornece uma implementação.  

A interface do representante tem um único `Invoke` método que assume como primeiro parâmetro um `HRESULT` dos códigos de sucesso ou falha.  Além disso, pode haver um segundo parâmetro que é o resultado do método se o método tiver um resultado.  Por exemplo, o método [ICoreWebView2:: CapturePreview] [Webview2ReferenceWin3209538Icorewebview2CapturePreview] usa como o parâmetro final de um `ICoreWebView2CapturePreviewCompletedHandler` ponteiro.  Para enviar uma `CapturePreview` solicitação de método, você fornece uma instância do `ICoreWebView2CapturePreviewCompletedHandler` ponteiro implementada.  O trecho de código a seguir usa um método para implementar.  

```cpp
HRESULT Invoke(HRESULT result)
```  

Você implementa o `Invoke` método e `CoreWebView2` solicita `Invoke` que seu método quando a `CapturePreview` solicitação for concluída.  O único parâmetro é a `HRESULT` Descrição do código de sucesso ou falha da `CapturePreview` solicitação.  

Ou para `ICoreWebView2::ExecuteScript` , você fornece uma instância que `ICoreWebView2ExecuteScriptCompletedHandler` tem um `Invoke` método que fornece o código de êxito ou falha da `ExecuteScript` solicitação, bem como o segundo parâmetro `resultObjectAsJson` que é o JSON do resultado da execução do script.  

Você pode implementar manualmente as `CompleteHandler` interfaces de representante ou pode usar a [função de retorno de chamada WRL][CppCxWrlCallbackFunction].  A função callback é usada em todo o trecho de código WebView2 a seguir.  

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

## Eventos  

Os eventos na API Win32 C++ do WebView2 usam `add_EventName` o `remove_EventName` par de método e para assinar e cancelar a assinatura de eventos.  O `add_EventName` método usa uma interface do representante do manipulador de eventos e retorna um `EventRegistrationToken` parâmetro como out.  O `remove_EventName` método faz uma `EventRegistrationToken` e cancela a assinatura da assinatura de evento correspondente.  

As interfaces do representante do manipulador de eventos funcionam de forma muito semelhante ao método Async concluído interfaces de representante do manipulador.  Você implementa a interface do representante do manipulador de eventos e `CoreWebView2` envia um retorno de chamada sempre que o evento é acionado.  Cada interface do representante do manipulador de eventos tem um único `Invoke` método que tem um parâmetro Sender seguido por um parâmetro args de evento.  O remetente é a instância do objeto na qual você assinou eventos.  O parâmetro args de evento é uma interface que contém informações sobre o evento de acionamento no momento.  

Por exemplo `NavigationCompleted` , o evento ativado `ICoreWebView2` tem o `ICoreWebView2::add_NavigationCompleted` par de método e `ICoreWebView2::remove_NavigationCompleted` .  Ao solicitar o complemento, você fornece uma instância do `ICoreWebView2NavigationCompletedEventHandler` método implementado anteriormente `Invoke` .  Quando o `NavigationCompleted` evento é acionado, seu `Invoke` método é solicitado.  O primeiro parâmetro é o `ICoreWebView2` que está acionando o `NavigationCompleted` evento.  O segundo parâmetro é o `ICoreWebView2NavigationCompletedEventArgs` que contém informações sobre se a navegação foi concluída com sucesso e assim por diante.  

Da mesma forma que o método Async concluiu a interface do representante, você pode implementá-lo diretamente ou pode usar a função de retorno de chamada WRL que é usada no seguinte trecho de código WebView2.  

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

## Seqüências  

Parâmetros de cadeia de caracteres externa são `LPWSTR` cadeias de caracteres terminadas por nulo.  O solicitante aloca a cadeia de caracteres usando `CoTaskMemAlloc` .  A propriedade é transferida para o solicitante e fica até o solicitante liberar a memória usando `CoTaskMemFree` .  

Cadeia de caracteres em parâmetros são `LPCWSTR` cadeias de caracteres terminadas por nulo.  O solicitante garante que a cadeia de caracteres é válida para a duração da solicitação de função síncrona.  Se o receptor deve reter esse valor para algum ponto após a conclusão da solicitação de função, o receptor deve atribuir uma cópia associada do valor da cadeia de caracteres.  

## Análise de URI e JSON  

Vários métodos fornecem ou aceitam URIs e JSON como cadeias de caracteres.  Use sua própria biblioteca preferida para analisar e gerar as cadeias de caracteres.  

Se o WinRT estiver disponível para o seu aplicativo, você poderá usar os `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` métodos e para analisar ou produzir cadeias de caracteres JSON ou `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` métodos para analisar e produzir URIs.  Os dois métodos funcionam em aplicativos Win32.  

Se você usar `IUri` e `CreateUri` para analisar URIs, talvez queira usar os seguintes sinalizadores de criação de URI para ter `CreateUri` comportamento mais próximo da análise de URI no WebView.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin3209622Icorewebview2CapturePreview]: ../reference/win32/0-9-622/icorewebview2.md#capturepreview "CapturePreview-interface ICoreWebView2 | Documentos da Microsoft"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Função callback (WRL) | Documentos da Microsoft"  
