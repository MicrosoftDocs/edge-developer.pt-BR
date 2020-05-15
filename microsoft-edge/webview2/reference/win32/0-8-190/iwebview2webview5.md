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
ms.openlocfilehash: 3c32cd59e75eb81bf69661d01f6044a0628ba35d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652343"
---
# interface IWebView2WebView5 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

Funcionalidades adicionais implementadas pelo objeto WebView primário.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Notifica quando a propriedade ContainsFullScreenElement muda.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Indica se a WebView contém um elemento HTML de tela inteira.
[add_WebResourceRequested](#add_webresourcerequested) | Adicione um manipulador de eventos para o evento WebResourceRequested.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.

Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md). Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.

## Parte

#### add_ContainsFullScreenElementChanged 

Notifica quando a propriedade ContainsFullScreenElement muda.

> Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Isso significa que um elemento HTML dentro do WebView está entrando em tela inteira no tamanho do WebView ou sai do fullscreen. Esse evento é útil quando, por exemplo, um elemento de vídeo solicita a tela inteira. O ouvinte de ContainsFullScreenElementChanged pode então redimensionar a WebView em resposta.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<IWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](IWebView2WebView5* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_ContainsFullScreenElementChanged 

Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.

> [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)público HRESULT (token EventRegistrationToken)

#### get_ContainsFullScreenElement 

Indica se a WebView contém um elemento HTML de tela inteira.

> [get_ContainsFullScreenElement](#get_containsfullscreenelement)público HRESULT (bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Adicione um manipulador de eventos para o evento WebResourceRequested.

> Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Acionado quando o WebView está executando uma solicitação HTTP para uma URL correspondente e um filtro de contexto de recurso que foi adicionado com o AddWebResourceRequestedFilter. Pelo menos um filtro deve ser adicionado para que o evento seja acionado.

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

#### AddWebResourceRequestedFilter 

Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.

> Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(URI const LPCWSTR,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)

O parâmetro URI pode ser uma cadeia de caracteres curinga (' ': zero ou mais, '? ': exatamente um). nullptr é equivalente a L "". Consulte WEBVIEW2_WEB_RESOURCE_CONTEXT enumeração para obter a descrição dos filtros de contexto de recurso.

#### RemoveWebResourceRequestedFilter 

Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.

> Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(URI const LPCWSTR,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)

Se o mesmo filtro tiver sido adicionado várias vezes, será preciso removê-lo quantas vezes forem adicionadas para que a remoção seja efetiva. Retorna E_INVALIDARG para um filtro que nunca foi adicionado.

