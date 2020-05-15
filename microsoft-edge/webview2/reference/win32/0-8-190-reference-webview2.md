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
ms.openlocfilehash: ba3103037db60674d1d3887ac43a8fce5be02bdd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652555"
---
# 0.8.190-Reference (WebView2)  

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.  Consulte a [referência](../../webview2-api-reference.md) para obter a referência da API mais recente.

O controle WebView2 do Microsoft Edge permite que você hospede conteúdo da Web em seu aplicativo usando o [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) como mecanismo de renderização.  Para obter mais informações, consulte [visão geral do Microsoft Edge WebView2](../../index.md)) e [introdução ao WebView2](../../gettingstarted/win32.md).  [IWebView2WebView](0-8-190/IWebView2WebView.md) é um ótimo lugar para começar a aprender os detalhes da API.  

## Globais  

*   [Globais](0-8-190/webview2-idl.md)  

## Classes  
*   [IWebView2Deferral](0-8-190/IWebView2Deferral.md)
*   [IWebView2Environment](0-8-190/IWebView2Environment.md)
*   [IWebView2Environment2](0-8-190/IWebView2Environment2.md)
*   [IWebView2Environment3](0-8-190/IWebView2Environment3.md)
*   [IWebView2HttpHeadersCollectionIterator](0-8-190/IWebView2HttpHeadersCollectionIterator.md)
*   [IWebView2HttpRequestHeaders](0-8-190/IWebView2HttpRequestHeaders.md)
*   [IWebView2HttpResponseHeaders](0-8-190/IWebView2HttpResponseHeaders.md)
*   [IWebView2Settings](0-8-190/IWebView2Settings.md)
*   [IWebView2Settings2](0-8-190/IWebView2Settings2.md)
*   [IWebView2WebResourceRequest](0-8-190/IWebView2WebResourceRequest.md)
*   [IWebView2WebResourceRequestedEventArgs2](0-8-190/IWebView2WebResourceRequestedEventArgs2.md)
*   [IWebView2WebResourceResponse](0-8-190/IWebView2WebResourceResponse.md)
*   [IWebView2WebView](0-8-190/IWebView2WebView.md)
*   [IWebView2WebView2](0-8-190/IWebView2WebView2.md)
*   [IWebView2WebView3](0-8-190/IWebView2WebView3.md)
*   [IWebView2WebView4](0-8-190/IWebView2WebView4.md)
*   [IWebView2WebView5](0-8-190/IWebView2WebView5.md)

### Interfaces de argumento de evento

*   [IWebView2AcceleratorKeyPressedEventArgs](0-8-190/IWebView2AcceleratorKeyPressedEventArgs.md)
*   [IWebView2DevToolsProtocolEventReceivedEventArgs](0-8-190/IWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [IWebView2DocumentStateChangedEventArgs](0-8-190/IWebView2DocumentStateChangedEventArgs.md)
*   [IWebView2MoveFocusRequestedEventArgs](0-8-190/IWebView2MoveFocusRequestedEventArgs.md)
*   [IWebView2NavigationCompletedEventArgs](0-8-190/IWebView2NavigationCompletedEventArgs.md)
*   [IWebView2NavigationStartingEventArgs](0-8-190/IWebView2NavigationStartingEventArgs.md)
*   [IWebView2NewVersionAvailableEventArgs](0-8-190/IWebView2NewVersionAvailableEventArgs.md)
*   [IWebView2NewWindowRequestedEventArgs](0-8-190/IWebView2NewWindowRequestedEventArgs.md)
*   [IWebView2PermissionRequestedEventArgs](0-8-190/IWebView2PermissionRequestedEventArgs.md)
*   [IWebView2ProcessFailedEventArgs](0-8-190/IWebView2ProcessFailedEventArgs.md)
*   [IWebView2ScriptDialogOpeningEventArgs](0-8-190/IWebView2ScriptDialogOpeningEventArgs.md)
*   [IWebView2WebMessageReceivedEventArgs](0-8-190/IWebView2WebMessageReceivedEventArgs.md)
*   [IWebView2WebResourceRequestedEventArgs](0-8-190/IWebView2WebResourceRequestedEventArgs.md)

### Interfaces do representante

*   [IWebView2AcceleratorKeyPressedEventHandler](0-8-190/IWebView2AcceleratorKeyPressedEventHandler.md)
*   [IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](0-8-190/IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [IWebView2CallDevToolsProtocolMethodCompletedHandler](0-8-190/IWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [IWebView2CapturePreviewCompletedHandler](0-8-190/IWebView2CapturePreviewCompletedHandler.md)
*   [IWebView2ContainsFullScreenElementChangedEventHandler](0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [IWebView2CreateWebView2EnvironmentCompletedHandler](0-8-190/IWebView2CreateWebView2EnvironmentCompletedHandler.md)
*   [IWebView2CreateWebViewCompletedHandler](0-8-190/IWebView2CreateWebViewCompletedHandler.md)
*   [IWebView2DevToolsProtocolEventReceivedEventHandler](0-8-190/IWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [IWebView2DocumentStateChangedEventHandler](0-8-190/IWebView2DocumentStateChangedEventHandler.md)
*   [IWebView2DocumentTitleChangedEventHandler](0-8-190/IWebView2DocumentTitleChangedEventHandler.md)
*   [IWebView2ExecuteScriptCompletedHandler](0-8-190/IWebView2ExecuteScriptCompletedHandler.md)
*   [IWebView2FocusChangedEventHandler](0-8-190/IWebView2FocusChangedEventHandler.md)
*   [IWebView2MoveFocusRequestedEventHandler](0-8-190/IWebView2MoveFocusRequestedEventHandler.md)
*   [IWebView2NavigationCompletedEventHandler](0-8-190/IWebView2NavigationCompletedEventHandler.md)
*   [IWebView2NavigationStartingEventHandler](0-8-190/IWebView2NavigationStartingEventHandler.md)
*   [IWebView2NewVersionAvailableEventHandler](0-8-190/IWebView2NewVersionAvailableEventHandler.md)
*   [IWebView2NewWindowRequestedEventHandler](0-8-190/IWebView2NewWindowRequestedEventHandler.md)
*   [IWebView2PermissionRequestedEventHandler](0-8-190/IWebView2PermissionRequestedEventHandler.md)
*   [IWebView2ProcessFailedEventHandler](0-8-190/IWebView2ProcessFailedEventHandler.md)
*   [IWebView2ScriptDialogOpeningEventHandler](0-8-190/IWebView2ScriptDialogOpeningEventHandler.md)
*   [IWebView2WebMessageReceivedEventHandler](0-8-190/IWebView2WebMessageReceivedEventHandler.md)
*   [IWebView2WebResourceRequestedEventHandler](0-8-190/IWebView2WebResourceRequestedEventHandler.md)
*   [IWebView2ZoomFactorChangedEventHandler](0-8-190/IWebView2ZoomFactorChangedEventHandler.md)
