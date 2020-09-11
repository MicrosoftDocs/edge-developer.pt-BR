---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Settings
ms.openlocfilehash: 87b78956c29dac74bd023556a8c495222d248e9f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011469"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled) | A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.
[AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.
[AreDevToolsEnabled](#aredevtoolsenabled) | AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.
[AreHostObjectsAllowed](#arehostobjectsallowed) | A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.
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

É verdade por padrão.

#### AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.

> Public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)

Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload). Se definido como true, um também poderá se inscrever para o evento ScriptDialogOpening que conterá todas as informações da caixa de diálogo e permitir que o aplicativo host mostre sua própria interface do usuário personalizada. É verdade por padrão.

#### AreDevToolsEnabled 

AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.

> Public bool [AreDevToolsEnabled](#aredevtoolsenabled)

É verdade por padrão.

#### AreHostObjectsAllowed 

A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.

> Public bool [AreHostObjectsAllowed](#arehostobjectsallowed)

É verdade por padrão.

#### IsBuiltInErrorPageEnabled 

A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.

> Public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)

É verdade por padrão. Quando desativado, a página em branco será mostrada quando ocorrer um erro relacionado.

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

Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes). A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de mensagem de automensagem do Window. Chrome. WebView e do evento WebMessageReceived (consulte a documentação do WebMessageReceived para obter detalhes). Se definido como false, a comunicação não será permitida. PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro. É verdade por padrão.

#### IsZoomControlEnabled 

A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.

> Public bool [IsZoomControlEnabled](#iszoomcontrolenabled)

É verdade por padrão. Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido por meio da API ZoomFactor.

