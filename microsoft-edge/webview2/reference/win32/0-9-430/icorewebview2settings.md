---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 70ccef9e99b3649ceca49b736570ba416cf73ebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883977"
---
# 0.9.430-ICoreWebView2Settings de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
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
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled controla se a barra de status será exibida.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Defina a propriedade IsStatusBarEnabled.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Defina a propriedade AreDevToolsEnabled.
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Defina a propriedade AreDefaultContextMenusEnabled.
[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed) | A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos remotos podem ser acessados na página do WebView.
[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed) | Defina a propriedade AreRemoteObjectsAllowed.
[get_IsZoomControlEnabled](#get_iszoomcontrolenabled) | A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.
[put_IsZoomControlEnabled](#put_iszoomcontrolenabled) | Defina a propriedade IsZoomControlEnabled.

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
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### put_IsWebMessageEnabled 

Defina a propriedade IsWebMessageEnabled.

> [put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.

> [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool * AreDefaultScriptDialogsEnabled)

Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload). Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.

#### put_AreDefaultScriptDialogsEnabled 

Defina a propriedade AreDefaultScriptDialogsEnabled.

> [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)

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

#### get_AreDefaultContextMenusEnabled 

A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.

> [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool * habilitado)

O padrão é TRUE.

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### put_AreDefaultContextMenusEnabled 

Defina a propriedade AreDefaultContextMenusEnabled.

> [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)

#### get_AreRemoteObjectsAllowed 

A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos remotos podem ser acessados na página do WebView.

> [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)público HRESULT (bool * allowed)

O padrão é TRUE.

```cpp
            BOOL allowRemoteObjects;
            CHECK_FAILURE(m_settings->get_AreRemoteObjectsAllowed(&allowRemoteObjects));
            if (allowRemoteObjects)
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to remote objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to remote objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### put_AreRemoteObjectsAllowed 

Defina a propriedade AreRemoteObjectsAllowed.

> [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)público HRESULT (bool permitido)

#### get_IsZoomControlEnabled 

A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.

> [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)público HRESULT (bool * habilitado)

O padrão é TRUE. Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido via API put_ZoomFactor.

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control is disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control is enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### put_IsZoomControlEnabled 

Defina a propriedade IsZoomControlEnabled.

> [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)público HRESULT (bool habilitado)

