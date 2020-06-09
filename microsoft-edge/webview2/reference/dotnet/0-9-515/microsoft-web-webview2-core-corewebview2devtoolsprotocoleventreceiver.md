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
ms.openlocfilehash: 9b54f9f519c76440d3556bb67f5ab7ad186ba290
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697662"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado. Invoke será chamado com o objeto do evento args que contém o objeto de parâmetro do evento de protocolo DevTools como uma cadeia de caracteres JSON.

