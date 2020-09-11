---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: 42ea3beb51dc315ed7ab3b7b0c04c7414adab2db
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011440"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Um receptor é criado para um determinado evento de protocolo DevTools e permite que você assine e cancele a assinatura desse evento.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived) | Assine um evento DevToolsProtocol.

Obtido do objeto WebView via GetDevToolsProtocolEventReceiver.

## Parte

#### DevToolsProtocolEventReceived 

Assine um evento DevToolsProtocol.

> < do evento público EventHandler [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)

O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado. Invoke será chamado com um objeto args de evento que contém o objeto de parâmetro do evento de protocolo DevTools como uma cadeia de caracteres JSON.

