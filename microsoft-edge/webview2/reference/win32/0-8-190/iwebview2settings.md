---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 94c6d6c424d715d3b6b57b366b71cf8e5fb8ec42
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878208"
---
# 0.8.355-IWebView2Settings de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2Settings
  : public IUnknown
```

Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsScriptEnabled](#get_isscriptenabled) | Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.
[put_IsScriptEnabled](#put_isscriptenabled) | Defina a propriedade IsScriptEnabled.
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Defina a propriedade IsWebMessageEnabled.
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Defina a propriedade AreDefaultScriptDialogsEnabled.
[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated) | Essa configuração é preterida e sempre retornará false.
[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated) | Essa configuração é preterida e não terá efeito.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled controla se a barra de status será exibida.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Defina a propriedade IsStatusBarEnabled.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Defina a propriedade AreDevToolsEnabled.

As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.

## Parte

#### get_IsScriptEnabled 

Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.

> [get_IsScriptEnabled](#get_isscriptenabled)público HRESULT (bool * IsScriptEnabled)

Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado. É verdade por padrão.

```cpp
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
```

#### put_IsScriptEnabled 

Defina a propriedade IsScriptEnabled.

> [put_IsScriptEnabled](#put_isscriptenabled)público HRESULT (bool IsScriptEnabled)

#### get_IsWebMessageEnabled 

A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.

> [get_IsWebMessageEnabled](#get_iswebmessageenabled)público HRESULT (bool * IsWebMessageEnabled)

Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes). A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes). Se definido como false, a comunicação não será permitida. PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro. É verdade por padrão.

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### put_IsWebMessageEnabled 

Defina a propriedade IsWebMessageEnabled.

> [put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.

> [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool * AreDefaultScriptDialogsEnabled)

Se definido como false, o WebView não renderizará a caixa de diálogo padrão do JavaScript (especificamente as mostradas pelas funções de alerta, confirmação e prompt do JavaScript). Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.

#### put_AreDefaultScriptDialogsEnabled 

Defina a propriedade AreDefaultScriptDialogsEnabled.

> [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)

#### get_IsFullscreenAllowed_deprecated 

Essa configuração é preterida e sempre retornará false.

> [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)público HRESULT (bool * IsFullscreenAllowed)

Isso significa que os elementos da WebView só preencherão os limites da WebView. Essa propriedade será completamente removida. Em vez disso, ouça o evento ContainsFullScreenElementChanged.

Controla se o fullscreen é permitido para os elementos no WebView. Quando é permitido, o conteúdo da Web, como um elemento de vídeo na WebView, pode ser exibido em tela cheia. Quando não for permitido, o elemento preencherá os limites da WebView quando o elemento exigir a tela inteira. É verdade por padrão.

#### put_IsFullscreenAllowed_deprecated 

Essa configuração é preterida e não terá efeito.

> [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)público HRESULT (bool IsFullscreenAllowed)

Em vez disso, ouça o evento ContainsFullScreenElementChanged.

Defina a propriedade IsFullscreenAllowed.

#### get_IsStatusBarEnabled 

IsStatusBarEnabled controla se a barra de status será exibida.

> [get_IsStatusBarEnabled](#get_isstatusbarenabled)público HRESULT (bool * IsStatusBarEnabled)

A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações. É verdade por padrão.

#### put_IsStatusBarEnabled 

Defina a propriedade IsStatusBarEnabled.

> [put_IsStatusBarEnabled](#put_isstatusbarenabled)público HRESULT (bool IsStatusBarEnabled)

#### get_AreDevToolsEnabled 

AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.

> [get_AreDevToolsEnabled](#get_aredevtoolsenabled)público HRESULT (bool * AreDevToolsEnabled)

É verdade por padrão.

#### put_AreDevToolsEnabled 

Defina a propriedade AreDevToolsEnabled.

> [put_AreDevToolsEnabled](#put_aredevtoolsenabled)público HRESULT (bool AreDevToolsEnabled)

