---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2Settings
ms.openlocfilehash: 1ad6754d2ff59a92e107c66644e389582ff6053b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011543"
---
# interface ICoreWebView2Settings 

```
interface ICoreWebView2Settings
  : public IUnknown
```

Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.
[get_AreHostObjectsAllowed](#get_arehostobjectsallowed) | A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.
[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled) | A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.
[get_IsScriptEnabled](#get_isscriptenabled) | Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled controla se a barra de status será exibida.
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.
[get_IsZoomControlEnabled](#get_iszoomcontrolenabled) | A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Defina a propriedade AreDefaultContextMenusEnabled.
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Defina a propriedade AreDefaultScriptDialogsEnabled.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Defina a propriedade AreDevToolsEnabled.
[put_AreHostObjectsAllowed](#put_arehostobjectsallowed) | Defina a propriedade AreHostObjectsAllowed.
[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled) | Defina a propriedade IsBuiltInErrorPageEnabled.
[put_IsScriptEnabled](#put_isscriptenabled) | Defina a propriedade IsScriptEnabled.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Defina a propriedade IsStatusBarEnabled.
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Defina a propriedade IsWebMessageEnabled.
[put_IsZoomControlEnabled](#put_iszoomcontrolenabled) | Defina a propriedade IsZoomControlEnabled.

As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.

## Parte

#### get_AreDefaultContextMenusEnabled 

A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.

> [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool * habilitado)

É verdade por padrão.

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

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.

> [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool * AreDefaultScriptDialogsEnabled)

Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload). Em vez disso, se um manipulador de eventos estiver definido via add_ScriptDialogOpening, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitir que o aplicativo host mostre sua própria interface do usuário personalizada. É verdade por padrão.

#### get_AreDevToolsEnabled 

AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.

> [get_AreDevToolsEnabled](#get_aredevtoolsenabled)público HRESULT (bool * AreDevToolsEnabled)

É verdade por padrão.

#### get_AreHostObjectsAllowed 

A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.

> [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)público HRESULT (bool * allowed)

É verdade por padrão.

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### get_IsBuiltInErrorPageEnabled 

A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.

> [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)público HRESULT (bool * habilitado)

É verdade por padrão. Quando desativado, a página em branco será mostrada quando ocorrer um erro relacionado.

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

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

#### get_IsStatusBarEnabled 

IsStatusBarEnabled controla se a barra de status será exibida.

> [get_IsStatusBarEnabled](#get_isstatusbarenabled)público HRESULT (bool * IsStatusBarEnabled)

A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações. É verdade por padrão.

#### get_IsWebMessageEnabled 

A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.

> [get_IsWebMessageEnabled](#get_iswebmessageenabled)público HRESULT (bool * IsWebMessageEnabled)

Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes). A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de automensagem Window. Chrome. WebView e add_WebMessageReceived método (consulte add_WebMessageReceived documentação para obter detalhes). Se definido como false, a comunicação não será permitida. PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro. É verdade por padrão.

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### get_IsZoomControlEnabled 

A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.

> [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)público HRESULT (bool * habilitado)

É verdade por padrão. Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido por meio da API ZoomFactor.

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### put_AreDefaultContextMenusEnabled 

Defina a propriedade AreDefaultContextMenusEnabled.

> [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)

#### put_AreDefaultScriptDialogsEnabled 

Defina a propriedade AreDefaultScriptDialogsEnabled.

> [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)

#### put_AreDevToolsEnabled 

Defina a propriedade AreDevToolsEnabled.

> [put_AreDevToolsEnabled](#put_aredevtoolsenabled)público HRESULT (bool AreDevToolsEnabled)

#### put_AreHostObjectsAllowed 

Defina a propriedade AreHostObjectsAllowed.

> [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)público HRESULT (bool permitido)

#### put_IsBuiltInErrorPageEnabled 

Defina a propriedade IsBuiltInErrorPageEnabled.

> [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)público HRESULT (bool habilitado)

#### put_IsScriptEnabled 

Defina a propriedade IsScriptEnabled.

> [put_IsScriptEnabled](#put_isscriptenabled)público HRESULT (bool IsScriptEnabled)

#### put_IsStatusBarEnabled 

Defina a propriedade IsStatusBarEnabled.

> [put_IsStatusBarEnabled](#put_isstatusbarenabled)público HRESULT (bool IsStatusBarEnabled)

#### put_IsWebMessageEnabled 

Defina a propriedade IsWebMessageEnabled.

> [put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)

#### put_IsZoomControlEnabled 

Defina a propriedade IsZoomControlEnabled.

> [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)público HRESULT (bool habilitado)

