---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: a095b1ed085cd49a597195e01da21cde53b9095d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884740"
---
# 0.8.355-IWebView2WebView3 de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView3
  : public IWebView2WebView
```

Funcionalidades adicionais implementadas pelo objeto WebView primário.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Parar](#stop) | Interrompa todas as navegações e buscas de recursos pendentes.
[add_NewWindowRequested](#add_newwindowrequested) | Adicione um manipulador de eventos para o evento NewWindowRequested.
[remove_NewWindowRequested](#remove_newwindowrequested) | Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Adicione um manipulador de eventos para o evento DocumentTitleChanged.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.
[get_DocumentTitle](#get_documenttitle) | O título do documento atual de nível superior.

Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md). Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.

## Parte

#### Parar 

Interrompa todas as navegações e buscas de recursos pendentes.

> público- [limite](#stop)HRESULT ()

#### add_NewWindowRequested 

Adicione um manipulador de eventos para o evento NewWindowRequested.

> Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Acionado quando o conteúdo dentro do WebView solicitado para abrir uma nova janela, por exemplo, por meio de Window. Open. O aplicativo pode passar um WebView de destino que será considerado a janela aberta.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<IWebView2NewWindowRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<IWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewWindowRequested 

Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.

> [remove_NewWindowRequested](#remove_newwindowrequested)público HRESULT (token EventRegistrationToken)

#### add_DocumentTitleChanged 

Adicione um manipulador de eventos para o evento DocumentTitleChanged.

> Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

O evento é acionado quando a propriedade DocumentTitle da WebView muda e pode ser acionada antes ou depois do evento NavigationCompleted.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<IWebView2DocumentTitleChangedEventHandler>(
            [this](IWebView2WebView3* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### remove_DocumentTitleChanged 

Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.

> [remove_DocumentTitleChanged](#remove_documenttitlechanged)público HRESULT (token EventRegistrationToken)

#### get_DocumentTitle 

O título do documento atual de nível superior.

> público HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR * title)

Se o documento não tiver um título explícito ou estiver vazio, um padrão que pode ou não corresponder ao URI do documento será usado.

