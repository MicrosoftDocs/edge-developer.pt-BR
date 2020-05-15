---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 519ef71db87d49aaf5a8a80970ff0cda61dfebbf
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652441"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled) | A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.
[AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.
[AreDevToolsEnabled](#aredevtoolsenabled) | AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.
[AreRemoteObjectsAllowed](#areremoteobjectsallowed) | A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos remotos podem ser acessados na página do WebView.
[IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled) | A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.
[IsScriptEnabled](#isscriptenabled) | Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.
[IsStatusBarEnabled](#isstatusbarenabled) | IsStatusBarEnabled controla se a barra de status será exibida.
[IsWebMessageEnabled](#iswebmessageenabled) | A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.
[IsZoomControlEnabled](#iszoomcontrolenabled) | A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.

As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.

## Parte

#### AreDefaultContextMenusEnabled 

A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.

> Public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)

O padrão é TRUE.

#### AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.

> Public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)

Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload). Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.

#### AreDevToolsEnabled 

AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.

> Public bool [AreDevToolsEnabled](#aredevtoolsenabled)

É verdade por padrão.

#### AreRemoteObjectsAllowed 

A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos remotos podem ser acessados na página do WebView.

> Public bool [AreRemoteObjectsAllowed](#areremoteobjectsallowed)

O padrão é TRUE.

#### IsBuiltInErrorPageEnabled 

A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.

> Public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)

O padrão é TRUE. Quando desativado, a página em branco será mostrada quando ocorrer um erro relacionado.

#### IsScriptEnabled 

Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.

> Public bool [IsScriptEnabled](#isscriptenabled)

Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado. É verdade por padrão.

#### IsStatusBarEnabled 

IsStatusBarEnabled controla se a barra de status será exibida.

> Public bool [IsStatusBarEnabled](#isstatusbarenabled)

A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações. É verdade por padrão.

#### IsWebMessageEnabled 

A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.

> Public bool [IsWebMessageEnabled](#iswebmessageenabled)

Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes). A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes). Se definido como false, a comunicação não será permitida. PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro. É verdade por padrão.

#### IsZoomControlEnabled 

A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.

> Public bool [IsZoomControlEnabled](#iszoomcontrolenabled)

O padrão é TRUE. Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido por meio da API ZoomFactor.

