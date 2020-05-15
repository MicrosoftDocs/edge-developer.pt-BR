---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 8baa7b1f571d62fad21a30441f47835bff3da96a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652648"
---
# 0.9.430-Reference (WebView2)  

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../webview2-api-reference.md) para obter a referência da API mais recente.

O controle WebView2 do Microsoft Edge permite que você hospede conteúdo da Web em seu aplicativo usando o [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) como mecanismo de renderização.  Para obter mais informações, consulte [visão geral do Microsoft Edge WebView2](../../index.md)) e [introdução ao WebView2](../../gettingstarted/win32.md).  [ICoreWebView2](0-9-430/ICoreWebView2.md) é um ótimo lugar para começar a aprender os detalhes da API.  

## Globais  

*   [Globais](0-9-430/webview2-idl.md)  

## Classes  
*   [ICoreWebView2](0-9-430/ICoreWebView2.md)
*   [ICoreWebView2Deferral](0-9-430/ICoreWebView2Deferral.md)
*   [ICoreWebView2DevToolsProtocolEventReceiver](0-9-430/ICoreWebView2DevToolsProtocolEventReceiver.md)
*   [ICoreWebView2Environment](0-9-430/ICoreWebView2Environment.md)
*   [ICoreWebView2Host](0-9-430/ICoreWebView2Host.md)
*   [ICoreWebView2HttpHeadersCollectionIterator](0-9-430/ICoreWebView2HttpHeadersCollectionIterator.md)
*   [ICoreWebView2HttpRequestHeaders](0-9-430/ICoreWebView2HttpRequestHeaders.md)
*   [ICoreWebView2HttpResponseHeaders](0-9-430/ICoreWebView2HttpResponseHeaders.md)
*   [ICoreWebView2Settings](0-9-430/ICoreWebView2Settings.md)
*   [ICoreWebView2WebResourceRequest](0-9-430/ICoreWebView2WebResourceRequest.md)
*   [ICoreWebView2WebResourceResponse](0-9-430/ICoreWebView2WebResourceResponse.md)

### Interfaces de argumento de evento

*   [ICoreWebView2AcceleratorKeyPressedEventArgs](0-9-430/ICoreWebView2AcceleratorKeyPressedEventArgs.md)
*   [ICoreWebView2ContentLoadingEventArgs](0-9-430/ICoreWebView2ContentLoadingEventArgs.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [ICoreWebView2MoveFocusRequestedEventArgs](0-9-430/ICoreWebView2MoveFocusRequestedEventArgs.md)
*   [ICoreWebView2NavigationCompletedEventArgs](0-9-430/ICoreWebView2NavigationCompletedEventArgs.md)
*   [ICoreWebView2NavigationStartingEventArgs](0-9-430/ICoreWebView2NavigationStartingEventArgs.md)
*   [ICoreWebView2NewBrowserVersionAvailableEventArgs](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventArgs.md)
*   [ICoreWebView2NewWindowRequestedEventArgs](0-9-430/ICoreWebView2NewWindowRequestedEventArgs.md)
*   [ICoreWebView2PermissionRequestedEventArgs](0-9-430/ICoreWebView2PermissionRequestedEventArgs.md)
*   [ICoreWebView2ProcessFailedEventArgs](0-9-430/ICoreWebView2ProcessFailedEventArgs.md)
*   [ICoreWebView2ScriptDialogOpeningEventArgs](0-9-430/ICoreWebView2ScriptDialogOpeningEventArgs.md)
*   [ICoreWebView2SourceChangedEventArgs](0-9-430/ICoreWebView2SourceChangedEventArgs.md)
*   [ICoreWebView2WebMessageReceivedEventArgs](0-9-430/ICoreWebView2WebMessageReceivedEventArgs.md)
*   [ICoreWebView2WebResourceRequestedEventArgs](0-9-430/ICoreWebView2WebResourceRequestedEventArgs.md)

### Interfaces do representante

*   [ICoreWebView2AcceleratorKeyPressedEventHandler](0-9-430/ICoreWebView2AcceleratorKeyPressedEventHandler.md)
*   [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](0-9-430/ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](0-9-430/ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [ICoreWebView2CapturePreviewCompletedHandler](0-9-430/ICoreWebView2CapturePreviewCompletedHandler.md)
*   [ICoreWebView2ContainsFullScreenElementChangedEventHandler](0-9-430/ICoreWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [ICoreWebView2ContentLoadingEventHandler](0-9-430/ICoreWebView2ContentLoadingEventHandler.md)
*   [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](0-9-430/ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler.md)
*   [ICoreWebView2CreateCoreWebView2HostCompletedHandler](0-9-430/ICoreWebView2CreateCoreWebView2HostCompletedHandler.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventHandler](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [ICoreWebView2DocumentTitleChangedEventHandler](0-9-430/ICoreWebView2DocumentTitleChangedEventHandler.md)
*   [ICoreWebView2ExecuteScriptCompletedHandler](0-9-430/ICoreWebView2ExecuteScriptCompletedHandler.md)
*   [ICoreWebView2FocusChangedEventHandler](0-9-430/ICoreWebView2FocusChangedEventHandler.md)
*   [ICoreWebView2HistoryChangedEventHandler](0-9-430/ICoreWebView2HistoryChangedEventHandler.md)
*   [ICoreWebView2MoveFocusRequestedEventHandler](0-9-430/ICoreWebView2MoveFocusRequestedEventHandler.md)
*   [ICoreWebView2NavigationCompletedEventHandler](0-9-430/ICoreWebView2NavigationCompletedEventHandler.md)
*   [ICoreWebView2NavigationStartingEventHandler](0-9-430/ICoreWebView2NavigationStartingEventHandler.md)
*   [ICoreWebView2NewBrowserVersionAvailableEventHandler](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventHandler.md)
*   [ICoreWebView2NewWindowRequestedEventHandler](0-9-430/ICoreWebView2NewWindowRequestedEventHandler.md)
*   [ICoreWebView2PermissionRequestedEventHandler](0-9-430/ICoreWebView2PermissionRequestedEventHandler.md)
*   [ICoreWebView2ProcessFailedEventHandler](0-9-430/ICoreWebView2ProcessFailedEventHandler.md)
*   [ICoreWebView2ScriptDialogOpeningEventHandler](0-9-430/ICoreWebView2ScriptDialogOpeningEventHandler.md)
*   [ICoreWebView2SourceChangedEventHandler](0-9-430/ICoreWebView2SourceChangedEventHandler.md)
*   [ICoreWebView2WebMessageReceivedEventHandler](0-9-430/ICoreWebView2WebMessageReceivedEventHandler.md)
*   [ICoreWebView2WebResourceRequestedEventHandler](0-9-430/ICoreWebView2WebResourceRequestedEventHandler.md)
*   [ICoreWebView2WindowCloseRequestedEventHandler](0-9-430/ICoreWebView2WindowCloseRequestedEventHandler.md)
*   [ICoreWebView2ZoomFactorChangedEventHandler](0-9-430/ICoreWebView2ZoomFactorChangedEventHandler.md)
