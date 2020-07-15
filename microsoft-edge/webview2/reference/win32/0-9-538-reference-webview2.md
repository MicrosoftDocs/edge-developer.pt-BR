---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Referência do Win32 C++ WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 59302f8a1c6f38f2e5688b05faa79d97d51b5409
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879139"
---
# Referência (WebView2 Win32 C++)  

O controle WebView2 do Microsoft Edge permite que você hospede conteúdo da Web em seu aplicativo usando o [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) como mecanismo de renderização.  Para obter mais informações, consulte [visão geral do Microsoft Edge WebView2](../../index.md)) e [introdução ao WebView2](../../gettingstarted/win32.md).  [ICoreWebView2](0-9-538/ICoreWebView2.md) é um ótimo lugar para começar a aprender os detalhes da API.  

## Globais  

*   [Globais](0-9-538/webview2-idl.md)  

## Classes  
*   [ICoreWebView2](0-9-538/icorewebview2.md)
*   [ICoreWebView2Controller](0-9-538/icorewebview2controller.md)
*   [ICoreWebView2Deferral](0-9-538/icorewebview2deferral.md)
*   [ICoreWebView2DevToolsProtocolEventReceiver](0-9-538/icorewebview2devtoolsprotocoleventreceiver.md)
*   [ICoreWebView2Environment](0-9-538/icorewebview2environment.md)
*   [ICoreWebView2EnvironmentOptions](0-9-538/icorewebview2environmentoptions.md)
*   [ICoreWebView2HttpHeadersCollectionIterator](0-9-538/icorewebview2httpheaderscollectioniterator.md)
*   [ICoreWebView2HttpRequestHeaders](0-9-538/icorewebview2httprequestheaders.md)
*   [ICoreWebView2HttpResponseHeaders](0-9-538/icorewebview2httpresponseheaders.md)
*   [ICoreWebView2Settings](0-9-538/icorewebview2settings.md)
*   [ICoreWebView2WebResourceRequest](0-9-538/icorewebview2webresourcerequest.md)
*   [ICoreWebView2WebResourceResponse](0-9-538/icorewebview2webresourceresponse.md)

### Argumentos de evento

*   [ICoreWebView2AcceleratorKeyPressedEventArgs](0-9-538/icorewebview2acceleratorkeypressedeventargs.md)
*   [ICoreWebView2ContentLoadingEventArgs](0-9-538/icorewebview2contentloadingeventargs.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](0-9-538/icorewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [ICoreWebView2MoveFocusRequestedEventArgs](0-9-538/icorewebview2movefocusrequestedeventargs.md)
*   [ICoreWebView2NavigationCompletedEventArgs](0-9-538/icorewebview2navigationcompletedeventargs.md)
*   [ICoreWebView2NavigationStartingEventArgs](0-9-538/icorewebview2navigationstartingeventargs.md)
*   [ICoreWebView2NewWindowRequestedEventArgs](0-9-538/icorewebview2newwindowrequestedeventargs.md)
*   [ICoreWebView2PermissionRequestedEventArgs](0-9-538/icorewebview2permissionrequestedeventargs.md)
*   [ICoreWebView2ProcessFailedEventArgs](0-9-538/icorewebview2processfailedeventargs.md)
*   [ICoreWebView2ScriptDialogOpeningEventArgs](0-9-538/icorewebview2scriptdialogopeningeventargs.md)
*   [ICoreWebView2SourceChangedEventArgs](0-9-538/icorewebview2sourcechangedeventargs.md)
*   [ICoreWebView2WebMessageReceivedEventArgs](0-9-538/icorewebview2webmessagereceivedeventargs.md)
*   [ICoreWebView2WebResourceRequestedEventArgs](0-9-538/icorewebview2webresourcerequestedeventargs.md)

### Delega

*   [ICoreWebView2AcceleratorKeyPressedEventHandler](0-9-538/icorewebview2acceleratorkeypressedeventhandler.md)
*   [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](0-9-538/icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md)
*   [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](0-9-538/icorewebview2calldevtoolsprotocolmethodcompletedhandler.md)
*   [ICoreWebView2CapturePreviewCompletedHandler](0-9-538/icorewebview2capturepreviewcompletedhandler.md)
*   [ICoreWebView2ContainsFullScreenElementChangedEventHandler](0-9-538/icorewebview2containsfullscreenelementchangedeventhandler.md)
*   [ICoreWebView2ContentLoadingEventHandler](0-9-538/icorewebview2contentloadingeventhandler.md)
*   [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](0-9-538/icorewebview2createcorewebview2controllercompletedhandler.md)
*   [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](0-9-538/icorewebview2createcorewebview2environmentcompletedhandler.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventHandler](0-9-538/icorewebview2devtoolsprotocoleventreceivedeventhandler.md)
*   [ICoreWebView2DocumentTitleChangedEventHandler](0-9-538/icorewebview2documenttitlechangedeventhandler.md)
*   [ICoreWebView2ExecuteScriptCompletedHandler](0-9-538/icorewebview2executescriptcompletedhandler.md)
*   [ICoreWebView2FocusChangedEventHandler](0-9-538/icorewebview2focuschangedeventhandler.md)
*   [ICoreWebView2HistoryChangedEventHandler](0-9-538/icorewebview2historychangedeventhandler.md)
*   [ICoreWebView2MoveFocusRequestedEventHandler](0-9-538/icorewebview2movefocusrequestedeventhandler.md)
*   [ICoreWebView2NavigationCompletedEventHandler](0-9-538/icorewebview2navigationcompletedeventhandler.md)
*   [ICoreWebView2NavigationStartingEventHandler](0-9-538/icorewebview2navigationstartingeventhandler.md)
*   [ICoreWebView2NewBrowserVersionAvailableEventHandler](0-9-538/icorewebview2newbrowserversionavailableeventhandler.md)
*   [ICoreWebView2NewWindowRequestedEventHandler](0-9-538/icorewebview2newwindowrequestedeventhandler.md)
*   [ICoreWebView2PermissionRequestedEventHandler](0-9-538/icorewebview2permissionrequestedeventhandler.md)
*   [ICoreWebView2ProcessFailedEventHandler](0-9-538/icorewebview2processfailedeventhandler.md)
*   [ICoreWebView2ScriptDialogOpeningEventHandler](0-9-538/icorewebview2scriptdialogopeningeventhandler.md)
*   [ICoreWebView2SourceChangedEventHandler](0-9-538/icorewebview2sourcechangedeventhandler.md)
*   [ICoreWebView2WebMessageReceivedEventHandler](0-9-538/icorewebview2webmessagereceivedeventhandler.md)
*   [ICoreWebView2WebResourceRequestedEventHandler](0-9-538/icorewebview2webresourcerequestedeventhandler.md)
*   [ICoreWebView2WindowCloseRequestedEventHandler](0-9-538/icorewebview2windowcloserequestedeventhandler.md)
*   [ICoreWebView2ZoomFactorChangedEventHandler](0-9-538/icorewebview2zoomfactorchangedeventhandler.md)

### Experimental

*   [ICoreWebView2ExperimentalCompositionController](0-9-538/icorewebview2experimentalcompositioncontroller.md)
*   [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](0-9-538/icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md)
*   [ICoreWebView2ExperimentalCursorChangedEventHandler](0-9-538/icorewebview2experimentalcursorchangedeventhandler.md)
*   [ICoreWebView2ExperimentalEnvironment](0-9-538/icorewebview2experimentalenvironment.md)
*   [ICoreWebView2ExperimentalNewWindowRequestedEventArgs](0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md)
*   [ICoreWebView2ExperimentalPointerInfo](0-9-538/icorewebview2experimentalpointerinfo.md)
*   [ICoreWebView2ExperimentalWindowFeatures](0-9-538/icorewebview2experimentalwindowfeatures.md)
