---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 701237096845ac99579265ebca3b37ef7247f33b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886476"
---
# <span data-ttu-id="2ec86-104">0.9.515-ICoreWebView2 de interface</span><span class="sxs-lookup"><span data-stu-id="2ec86-104">0.9.515 - interface ICoreWebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="2ec86-105">O WebView2 permite que você hospede conteúdo da Web usando a tecnologia de navegador da Web mais recente do Edge.</span><span class="sxs-lookup"><span data-stu-id="2ec86-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="2ec86-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="2ec86-106">Summary</span></span>

 <span data-ttu-id="2ec86-107">Parte</span><span class="sxs-lookup"><span data-stu-id="2ec86-107">Members</span></span>                        | <span data-ttu-id="2ec86-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2ec86-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="2ec86-110">Notifica quando a propriedade ContainsFullScreenElement muda.</span><span class="sxs-lookup"><span data-stu-id="2ec86-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="2ec86-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="2ec86-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="2ec86-112">Adicione um manipulador de eventos para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="2ec86-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="2ec86-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="2ec86-114">Adicione um manipulador de eventos para o evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="2ec86-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2ec86-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="2ec86-116">Adicione um manipulador de eventos para o evento FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="2ec86-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2ec86-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="2ec86-118">Adicione um manipulador de eventos para o evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="2ec86-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="2ec86-120">Cobrançaalterar Ouça a alteração do histórico de navegação do documento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2ec86-120">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="2ec86-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2ec86-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="2ec86-122">Adicione um manipulador de eventos para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="2ec86-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2ec86-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="2ec86-124">Adicione um manipulador de eventos para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="2ec86-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="2ec86-126">Adicione um manipulador de eventos para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="2ec86-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="2ec86-128">Adicione um manipulador de eventos para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="2ec86-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="2ec86-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="2ec86-130">Adicione um manipulador de eventos para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2ec86-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="2ec86-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="2ec86-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="2ec86-132">Adicione um manipulador de eventos para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2ec86-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="2ec86-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="2ec86-134">SourceChanged é acionado quando a propriedade Source muda.</span><span class="sxs-lookup"><span data-stu-id="2ec86-134">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="2ec86-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2ec86-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="2ec86-136">Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-136">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="2ec86-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="2ec86-138">Adicione um manipulador de eventos para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="2ec86-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="2ec86-140">Adicione um manipulador de eventos para o evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="2ec86-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="2ec86-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="2ec86-142">Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="2ec86-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="2ec86-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="2ec86-144">Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="2ec86-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="2ec86-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="2ec86-146">Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="2ec86-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="2ec86-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="2ec86-148">Chame um método DevToolsProtocol assíncrono.</span><span class="sxs-lookup"><span data-stu-id="2ec86-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="2ec86-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="2ec86-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="2ec86-150">Capture uma imagem do que o WebView está exibindo.</span><span class="sxs-lookup"><span data-stu-id="2ec86-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="2ec86-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="2ec86-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="2ec86-152">Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="2ec86-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="2ec86-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="2ec86-154">A ID do processo do navegador que hospeda o WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="2ec86-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="2ec86-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="2ec86-156">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-156">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="2ec86-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="2ec86-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="2ec86-158">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-158">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="2ec86-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="2ec86-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="2ec86-160">Indica se a WebView contém um elemento HTML de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="2ec86-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="2ec86-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="2ec86-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="2ec86-162">O título do documento atual de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2ec86-162">The title for the current top level document.</span></span>
[<span data-ttu-id="2ec86-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="2ec86-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="2ec86-164">O objeto [ICoreWebView2Settings](icorewebview2settings.md) contém várias configurações modificáveis para a execução do WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="2ec86-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="2ec86-165">get_Source</span></span>](#get_source) | <span data-ttu-id="2ec86-166">O URI do documento de nível superior atual.</span><span class="sxs-lookup"><span data-stu-id="2ec86-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="2ec86-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="2ec86-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="2ec86-168">Obtenha um receptor de evento de protocolo DevTools que permite que você se inscreva em um evento de protocolo DevTools.</span><span class="sxs-lookup"><span data-stu-id="2ec86-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="2ec86-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="2ec86-169">GoBack</span></span>](#goback) | <span data-ttu-id="2ec86-170">Navega o WebView para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="2ec86-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="2ec86-171">GoForward</span></span>](#goforward) | <span data-ttu-id="2ec86-172">Navega o WebView para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="2ec86-173">Navegar</span><span class="sxs-lookup"><span data-stu-id="2ec86-173">Navigate</span></span>](#navigate) | <span data-ttu-id="2ec86-174">Fazer uma navegação do documento de nível superior para o URI especificado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="2ec86-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="2ec86-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="2ec86-176">Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.</span><span class="sxs-lookup"><span data-stu-id="2ec86-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="2ec86-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="2ec86-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="2ec86-178">Abre a janela do DevTools para o documento atual no WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="2ec86-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="2ec86-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="2ec86-180">Postar a WebMessage especificada no documento de nível superior neste WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="2ec86-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="2ec86-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="2ec86-182">Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ec86-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="2ec86-183">Recarregar</span><span class="sxs-lookup"><span data-stu-id="2ec86-183">Reload</span></span>](#reload) | <span data-ttu-id="2ec86-184">Recarregar a página atual.</span><span class="sxs-lookup"><span data-stu-id="2ec86-184">Reload the current page.</span></span>
[<span data-ttu-id="2ec86-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="2ec86-186">Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-186">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="2ec86-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="2ec86-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="2ec86-188">Remover um manipulador de eventos adicionado anteriormente com add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="2ec86-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="2ec86-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="2ec86-190">Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="2ec86-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2ec86-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="2ec86-192">Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="2ec86-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2ec86-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="2ec86-194">Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="2ec86-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="2ec86-196">Remover um manipulador de eventos adicionado anteriormente com add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="2ec86-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2ec86-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="2ec86-198">Remover um manipulador de eventos adicionado anteriormente com add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="2ec86-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2ec86-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="2ec86-200">Remover um manipulador de eventos adicionado anteriormente com add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="2ec86-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="2ec86-202">Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="2ec86-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="2ec86-204">Remover um manipulador de eventos adicionado anteriormente com add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="2ec86-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="2ec86-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="2ec86-206">Remover um manipulador de eventos adicionado anteriormente com add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2ec86-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="2ec86-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="2ec86-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="2ec86-208">Remover um manipulador de eventos adicionado anteriormente com add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2ec86-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="2ec86-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="2ec86-210">Remover um manipulador de eventos adicionado anteriormente com add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="2ec86-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2ec86-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="2ec86-212">Remover um manipulador de eventos adicionado anteriormente com add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="2ec86-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="2ec86-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="2ec86-214">Remover um manipulador de eventos adicionado anteriormente com add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="2ec86-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="2ec86-216">Remover um manipulador de eventos adicionado anteriormente com add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="2ec86-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="2ec86-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="2ec86-218">Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="2ec86-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="2ec86-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="2ec86-220">Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2ec86-220">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="2ec86-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="2ec86-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="2ec86-222">Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="2ec86-223">Parar</span><span class="sxs-lookup"><span data-stu-id="2ec86-223">Stop</span></span>](#stop) | <span data-ttu-id="2ec86-224">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="2ec86-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="2ec86-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="2ec86-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="2ec86-226">Formato de imagem usado pelo método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="2ec86-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="2ec86-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="2ec86-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="2ec86-228">O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="2ec86-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="2ec86-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="2ec86-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="2ec86-230">Motivo para mover o foco.</span><span class="sxs-lookup"><span data-stu-id="2ec86-230">Reason for moving focus.</span></span>
[<span data-ttu-id="2ec86-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="2ec86-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="2ec86-232">O tipo de uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="2ec86-232">The type of a permission request.</span></span>
[<span data-ttu-id="2ec86-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="2ec86-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="2ec86-234">Resposta a uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="2ec86-234">Response to a permission request.</span></span>
[<span data-ttu-id="2ec86-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="2ec86-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="2ec86-236">Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.</span><span class="sxs-lookup"><span data-stu-id="2ec86-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="2ec86-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="2ec86-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="2ec86-238">Tipo de falha de processo usada na interface ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="2ec86-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="2ec86-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="2ec86-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="2ec86-240">Tipo de caixa de diálogo JavaScript usada na interface ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="2ec86-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="2ec86-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="2ec86-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="2ec86-242">Valores de status de erro para navegações na Web.</span><span class="sxs-lookup"><span data-stu-id="2ec86-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="2ec86-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="2ec86-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="2ec86-244">Enumeração para contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="2ec86-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="2ec86-245">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="2ec86-245">Navigation events</span></span>

<span data-ttu-id="2ec86-246">A sequência normal de eventos de navegação é NavigationStarting, SourceChanged, ContentLoading e, em seguida, NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-246">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="2ec86-248">Observe que isso se destina a eventos de navegação com o mesmo evento Navigationid ARG.</span><span class="sxs-lookup"><span data-stu-id="2ec86-248">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="2ec86-249">Navegação eventos com diferentes args de eventos Navigationid podem sobrepor-se.</span><span class="sxs-lookup"><span data-stu-id="2ec86-249">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="2ec86-250">Por exemplo, se você iniciar um evento de navegação e, em seguida, iniciar uma outra navegação, verá o NavigationStarting para a primeira navegação acompanhada pela NavigationStarting da segunda navegação, seguida da NavigationCompleted para a primeira navegação e, em seguida, todos os demais eventos de navegação apropriados para a segunda navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-250">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="2ec86-251">Em casos de erro, pode ou não ser um evento ContentLoading dependendo se a navegação é continuada para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="2ec86-251">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="2ec86-252">No caso de um redirecionamento HTTP, haverá vários eventos NavigationStarting em uma linha, com os seguintes, o sinalizador isredirect definido.</span><span class="sxs-lookup"><span data-stu-id="2ec86-252">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="2ec86-253">Para monitorar ou cancelar navegações dentro de subquadros no WebView, use FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-253">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="2ec86-254">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="2ec86-254">Process model</span></span>

<span data-ttu-id="2ec86-255">O WebView2 usa o mesmo modelo de processo que o navegador da Web Edge.</span><span class="sxs-lookup"><span data-stu-id="2ec86-255">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="2ec86-256">Há um processo do navegador Edge por diretório de dados do usuário especificado em uma sessão do usuário que servirá qualquer processo de chamadas do WebView2 que especifique esse diretório de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="2ec86-256">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="2ec86-257">Isso significa que um processo do navegador Edge pode estar servindo vários processos de chamadas e um processo de chamada pode estar usando vários processos do navegador do Edge.</span><span class="sxs-lookup"><span data-stu-id="2ec86-257">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="2ec86-259">Fora de um processo de navegador, haverá alguns processos de processamento.</span><span class="sxs-lookup"><span data-stu-id="2ec86-259">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="2ec86-260">Elas são criadas, conforme necessário, para atender a vários quadros potencialmente em diferentes modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="2ec86-260">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="2ec86-261">O número de processos de renderização varia de acordo com o recurso de navegador de isolamento de site e o número de origens discadas discadas renderizadas em webviews associadas.</span><span class="sxs-lookup"><span data-stu-id="2ec86-261">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="2ec86-263">Você pode reagir a falhas e travamentos nesses processos do navegador e do renderizador usando o evento ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="2ec86-263">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="2ec86-264">Você pode desligar com segurança os processos do navegador e do renderizador associados usando o método Close.</span><span class="sxs-lookup"><span data-stu-id="2ec86-264">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="2ec86-265">Modelo de Threading</span><span class="sxs-lookup"><span data-stu-id="2ec86-265">Threading model</span></span>

<span data-ttu-id="2ec86-266">O WebView2 deve ser criado em um thread de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2ec86-266">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="2ec86-267">Especificamente um thread com um bombeamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ec86-267">Specifically a thread with a message pump.</span></span> <span data-ttu-id="2ec86-268">Todos os retornos de chamada ocorrerão nesse thread e as chamadas para o WebView deverão ser feitas nesse thread.</span><span class="sxs-lookup"><span data-stu-id="2ec86-268">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="2ec86-269">Não é seguro usar a WebView a partir de outro thread.</span><span class="sxs-lookup"><span data-stu-id="2ec86-269">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="2ec86-270">Os retornos de chamada, incluindo manipuladores de eventos e manipuladores de conclusão, são executados em série.</span><span class="sxs-lookup"><span data-stu-id="2ec86-270">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="2ec86-271">Ou seja, se você tiver um manipulador de eventos em execução e iniciar um loop de mensagem, nenhum outro manipulador de eventos ou chamadas de retorno de conclusão começarão a ser executados de forma reentrada.</span><span class="sxs-lookup"><span data-stu-id="2ec86-271">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="2ec86-272">Segurança</span><span class="sxs-lookup"><span data-stu-id="2ec86-272">Security</span></span>

<span data-ttu-id="2ec86-273">Sempre verifique a propriedade Source da WebView antes de usar ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString ou qualquer outro método para enviar informações para o WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-273">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="2ec86-274">A WebView pode ter navegado para outra página por meio do usuário final interagindo com a página ou o script na página que está causando a navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-274">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="2ec86-275">Da mesma forma, tenha muito cuidado com o AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2ec86-275">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="2ec86-276">Todas as navegações futuras executarão esse script e, se ele fornecer acesso às informações destinadas apenas a determinada origem, qualquer documento HTML poderá ter acesso.</span><span class="sxs-lookup"><span data-stu-id="2ec86-276">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="2ec86-277">Ao examinar o resultado de uma chamada de método ExecuteScript, um evento WebMessageReceived, sempre verifique a fonte do remetente ou qualquer outro mecanismo de recebimento de informações de um documento HTML em uma WebView validar o URI do documento HTML é o que você espera.</span><span class="sxs-lookup"><span data-stu-id="2ec86-277">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="2ec86-278">Ao construir uma mensagem para enviar para um WebView, prefira usar PostWebMessageAsJson e construir o parâmetro de cadeia de caracteres JSON usando uma biblioteca JSON.</span><span class="sxs-lookup"><span data-stu-id="2ec86-278">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="2ec86-279">Isso evitará possíveis acidentes de codificar informações em uma cadeia de caracteres ou script JSON e garantir que nenhuma entrada controlada pelo invasor possa modificar o restante da mensagem JSON ou executar um script arbitrário.</span><span class="sxs-lookup"><span data-stu-id="2ec86-279">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="2ec86-280">Tipos de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="2ec86-280">String types</span></span>

<span data-ttu-id="2ec86-281">Parâmetros de cadeia de caracteres de saída são cadeias de caracteres de terminação NULL</span><span class="sxs-lookup"><span data-stu-id="2ec86-281">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="2ec86-282">O chamado aloca a cadeia de caracteres usando CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="2ec86-282">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="2ec86-283">A propriedade é transferida para o chamador e fica até o chamador liberar a memória usando o CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="2ec86-283">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="2ec86-284">Cadeias de caracteres em parâmetros são cadeias de caracteres terminadas LPCWSTR nulas.</span><span class="sxs-lookup"><span data-stu-id="2ec86-284">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="2ec86-285">O chamador garante que a cadeia de caracteres é válida para a duração da chamada de função síncrona.</span><span class="sxs-lookup"><span data-stu-id="2ec86-285">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="2ec86-286">Se o chamador precisa reter esse valor para algum ponto após a conclusão da chamada de função, o Calle deve alocar sua própria cópia do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2ec86-286">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="2ec86-287">Análise de URI e JSON</span><span class="sxs-lookup"><span data-stu-id="2ec86-287">URI and JSON parsing</span></span>

<span data-ttu-id="2ec86-288">Vários métodos fornecem ou aceitam URIs e JSON como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2ec86-288">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="2ec86-289">Use sua própria biblioteca preferida para analisar e gerar essas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2ec86-289">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="2ec86-290">Se o WinRT estiver disponível para seu aplicativo, você pode usar `RuntimeClass_Windows_Data_Json_JsonObject` e `IJsonObjectStatics` analisar ou produzir cadeias de caracteres JSON ou `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analisar e produzir URIs.</span><span class="sxs-lookup"><span data-stu-id="2ec86-290">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="2ec86-291">Ambos trabalham em aplicativos Win32.</span><span class="sxs-lookup"><span data-stu-id="2ec86-291">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="2ec86-292">Se você usar o IUri e o CreateUri para analisar URIs, talvez queira usar os seguintes sinalizadores de criação de URI para que o comportamento de CreateUri corresponda melhor à análise de URI no WebView:</span><span class="sxs-lookup"><span data-stu-id="2ec86-292">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="2ec86-293">Depuração</span><span class="sxs-lookup"><span data-stu-id="2ec86-293">Debugging</span></span>

<span data-ttu-id="2ec86-294">Abra o DevTools com os atalhos normais: `F12` ou `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-294">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="2ec86-295">Você pode usar o `--auto-open-devtools-for-tabs` argumento de comando switch para que a janela do devtools seja aberta imediatamente ao criar a primeira vez uma WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-295">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="2ec86-296">Consulte a documentação do CreateCoreWebView2Controller para saber como fornecer argumentos adicionais de linha de comando para o processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="2ec86-296">See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="2ec86-297">Confira a chave do registro LoaderOverride para experimentar versões diferentes do WebView2 sem modificar seu aplicativo na documentação do CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="2ec86-297">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.</span></span>

## <span data-ttu-id="2ec86-298">Controle de versão</span><span class="sxs-lookup"><span data-stu-id="2ec86-298">Versioning</span></span>

<span data-ttu-id="2ec86-299">Depois de usar uma versão específica do SDK para criar seu aplicativo, seu aplicativo pode acabar sendo executado com uma versão mais antiga ou mais recente dos binários instalados do navegador.</span><span class="sxs-lookup"><span data-stu-id="2ec86-299">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="2ec86-300">Até a versão 1.0.0.0 do WebView2, pode haver alterações significativas durante as atualizações que impedem que o SDK funcione com versões diferentes dos binários instalados do navegador.</span><span class="sxs-lookup"><span data-stu-id="2ec86-300">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="2ec86-301">Após a versão 1.0.0.0 versões diferentes do SDK podem funcionar com versões diferentes do navegador instalado seguindo estas práticas recomendadas:</span><span class="sxs-lookup"><span data-stu-id="2ec86-301">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="2ec86-302">Para fazer a conta de alterações significativas na API, verifique se há uma falha ao chamar a DLL de exportação CreateCoreWebView2Environment e ao chamar QueryInterface em qualquer objeto CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2ec86-302">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="2ec86-303">Um valor de retorno de E_NOINTERFACE pode indicar que o SDK não é compatível com os binários do navegador Edge.</span><span class="sxs-lookup"><span data-stu-id="2ec86-303">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="2ec86-304">Verificar a falha de QueryInterface também contará em casos em que o SDK é mais recente do que a versão do navegador Edge e seu aplicativo tenta usar uma interface do qual o navegador Edge não reconhece.</span><span class="sxs-lookup"><span data-stu-id="2ec86-304">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="2ec86-305">Quando uma interface não está disponível, você pode considerar a possibilidade de desabilitar o recurso associado, se possível, ou informar ao usuário final que ele precisa atualizar o navegador.</span><span class="sxs-lookup"><span data-stu-id="2ec86-305">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="2ec86-306">Parte</span><span class="sxs-lookup"><span data-stu-id="2ec86-306">Members</span></span>

#### <span data-ttu-id="2ec86-307">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-307">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="2ec86-308">Notifica quando a propriedade ContainsFullScreenElement muda.</span><span class="sxs-lookup"><span data-stu-id="2ec86-308">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="2ec86-309">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-309">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-310">Isso significa que um elemento HTML dentro do WebView está entrando em tela inteira no tamanho do WebView ou sai do fullscreen.</span><span class="sxs-lookup"><span data-stu-id="2ec86-310">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="2ec86-311">Esse evento é útil quando, por exemplo, um elemento de vídeo solicita a tela inteira.</span><span class="sxs-lookup"><span data-stu-id="2ec86-311">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="2ec86-312">O ouvinte de ContainsFullScreenElementChanged pode então redimensionar a WebView em resposta.</span><span class="sxs-lookup"><span data-stu-id="2ec86-312">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="2ec86-313">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="2ec86-313">add_ContentLoading</span></span> 

<span data-ttu-id="2ec86-314">Adicione um manipulador de eventos para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="2ec86-314">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="2ec86-315">Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-315">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-316">ContentLoading é acionado antes que qualquer conteúdo seja carregado, incluindo scripts adicionados com AddScriptToExecuteOnDocumentCreated ContentLoading não será acionado se ocorrer uma mesma navegação de página (por exemplo, por meio de navegações de fragmento ou de histórico. pushstate).</span><span class="sxs-lookup"><span data-stu-id="2ec86-316">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="2ec86-317">Isso segue os eventos NavigationStarting e SourceChanged e precede os eventos Historychanged e NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-317">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="2ec86-318">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-318">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="2ec86-319">Adicione um manipulador de eventos para o evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-319">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="2ec86-320">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-320">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-321">O evento é acionado quando a propriedade DocumentTitle da WebView muda e pode ser acionada antes ou depois do evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-321">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="2ec86-322">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2ec86-322">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="2ec86-323">Adicione um manipulador de eventos para o evento FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-323">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="2ec86-324">Public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-324">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-325">O evento FrameNavigationCompleted é acionado quando um quadro filho é completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.</span><span class="sxs-lookup"><span data-stu-id="2ec86-325">FrameNavigationCompleted event fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the FrameNavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    CHECK_FAILURE(m_webView->add_FrameNavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    std::wstring error_msg = WebErrorStatusToString(webErrorStatus);
                    MessageBox(nullptr,
                       (std::wstring(L"IFrame navigation failed with the ") +
                         L"give in error " + error_msg).c_str(),
                       L"Navigation Failure", MB_OK);
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_frameNavigationCompletedToken));
```

#### <span data-ttu-id="2ec86-326">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2ec86-326">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="2ec86-327">Adicione um manipulador de eventos para o evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-327">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="2ec86-328">Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-328">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-329">FrameNavigationStarting é acionado quando um quadro filho na WebView solicita permissão para navegar para um URI diferente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-329">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="2ec86-330">Isso também será acionado para redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="2ec86-330">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### <span data-ttu-id="2ec86-331">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-331">add_HistoryChanged</span></span> 

<span data-ttu-id="2ec86-332">Cobrançaalterar Ouça a alteração do histórico de navegação do documento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2ec86-332">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="2ec86-333">Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-333">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-334">Use Cobrançaalterar para verificar se o valor CanGoBack/CanGoForward foi alterado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-334">Use HistoryChange to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="2ec86-335">Historychanged também é acionado para usar o GoBack/GoForward.</span><span class="sxs-lookup"><span data-stu-id="2ec86-335">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="2ec86-336">Historychanged é acionado após SourceChanged e ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="2ec86-336">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="2ec86-337">Adicione um manipulador de eventos para o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-337">Add an event handler for the HistoryChanged event.</span></span> 
```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="2ec86-338">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2ec86-338">add_NavigationCompleted</span></span> 

<span data-ttu-id="2ec86-339">Adicione um manipulador de eventos para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-339">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="2ec86-340">Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-340">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-341">O evento NavigationCompleted é acionado quando o WebView foi completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.</span><span class="sxs-lookup"><span data-stu-id="2ec86-341">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="2ec86-342">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2ec86-342">add_NavigationStarting</span></span> 

<span data-ttu-id="2ec86-343">Adicione um manipulador de eventos para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-343">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="2ec86-344">Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-344">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-345">NavigationStarting é acionado quando o quadro principal do WebView está solicitando permissão para navegar para um URI diferente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-345">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="2ec86-346">Isso também será acionado para redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="2ec86-346">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
        }
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
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### <span data-ttu-id="2ec86-347">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-347">add_NewWindowRequested</span></span> 

<span data-ttu-id="2ec86-348">Adicione um manipulador de eventos para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-348">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="2ec86-349">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-349">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-350">Acionado quando o conteúdo dentro do WebView solicitado para abrir uma nova janela, por exemplo, por meio de Window. Open.</span><span class="sxs-lookup"><span data-stu-id="2ec86-350">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="2ec86-351">O aplicativo pode passar um WebView de destino que será considerado a janela aberta.</span><span class="sxs-lookup"><span data-stu-id="2ec86-351">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));
                AppWindow* newAppWindow;

                newAppWindow = new AppWindow(m_creationModeId, L"");
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="2ec86-352">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-352">add_PermissionRequested</span></span> 

<span data-ttu-id="2ec86-353">Adicione um manipulador de eventos para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-353">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="2ec86-354">Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-354">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-355">Acionado quando o conteúdo de uma WebView solicita permissão para acessar alguns recursos privilegiados.</span><span class="sxs-lookup"><span data-stu-id="2ec86-355">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        COREWEBVIEW2_PERMISSION_KIND kind = COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        COREWEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? COREWEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? COREWEBVIEW2_PERMISSION_STATE_DENY
            :                     COREWEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="2ec86-356">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="2ec86-356">add_ProcessFailed</span></span> 

<span data-ttu-id="2ec86-357">Adicione um manipulador de eventos para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2ec86-357">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="2ec86-358">Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-358">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-359">Acionado quando um processo da WebView termina inesperadamente ou não responde.</span><span class="sxs-lookup"><span data-stu-id="2ec86-359">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        COREWEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process exited unexpectedly. Reload page?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                CHECK_FAILURE(m_webView->Reload());
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="2ec86-360">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="2ec86-360">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="2ec86-361">Adicione um manipulador de eventos para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2ec86-361">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="2ec86-362">Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-362">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-363">O evento é acionado quando uma caixa de diálogo JavaScript (alerta, confirmação ou prompt) aparecerá para o WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-363">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="2ec86-364">Esse evento só será acionado se a propriedade ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled estiver definida como false.</span><span class="sxs-lookup"><span data-stu-id="2ec86-364">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="2ec86-365">O evento ScriptDialogOpening pode ser usado para suprimir caixas de diálogo ou substituir caixas de diálogo padrão por caixas de diálogo personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2ec86-365">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            COREWEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### <span data-ttu-id="2ec86-366">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-366">add_SourceChanged</span></span> 

<span data-ttu-id="2ec86-367">SourceChanged é acionado quando a propriedade Source muda.</span><span class="sxs-lookup"><span data-stu-id="2ec86-367">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="2ec86-368">Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-368">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-369">SourceChanged é acionado para navegar para um site ou navegação de fragmento diferente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-369">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="2ec86-370">Ele não será acionado para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual.</span><span class="sxs-lookup"><span data-stu-id="2ec86-370">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="2ec86-371">SourceChanged é acionado antes de ContentLoading para navegação para um novo documento.</span><span class="sxs-lookup"><span data-stu-id="2ec86-371">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="2ec86-372">Adicione um manipulador de eventos para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-372">Add an event handler for the SourceChanged event.</span></span> 
```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="2ec86-373">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2ec86-373">add_WebMessageReceived</span></span> 

<span data-ttu-id="2ec86-374">Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-374">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="2ec86-375">[add_WebMessageReceived](#add_webmessagereceived)público HRESULT (manipulador[ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-375">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-376">A função CreateMessage é `void postMessage(object)` onde o objeto é qualquer objeto compatível com a conversão JSON.</span><span class="sxs-lookup"><span data-stu-id="2ec86-376">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```html
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```
 <span data-ttu-id="2ec86-377">Quando a "CreateMessage" é chamado, o conjunto de [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) por meio desse método SetWebMessageReceivedEventHandler será invocado com o parâmetro de objeto da createmessagestring convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="2ec86-377">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="2ec86-378">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-378">add_WebResourceRequested</span></span> 

<span data-ttu-id="2ec86-379">Adicione um manipulador de eventos para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-379">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="2ec86-380">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-380">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-381">Acionado quando o WebView está executando uma solicitação HTTP para uma URL correspondente e um filtro de contexto de recurso que foi adicionado com o AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="2ec86-381">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="2ec86-382">Pelo menos um filtro deve ser adicionado para que o evento seja acionado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-382">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="2ec86-383">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-383">add_WindowCloseRequested</span></span> 

<span data-ttu-id="2ec86-384">Adicione um manipulador de eventos para o evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-384">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="2ec86-385">Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="2ec86-385">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="2ec86-386">Dispara quando o conteúdo dentro do WebView solicitado para fechar a janela, como After Window. Close, é chamado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-386">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="2ec86-387">O aplicativo deve fechar a janela da WebView e do aplicativo relacionado se isso fizer sentido com o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2ec86-387">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>([this](
                                                                    ICoreWebView2* sender,
                                                                    IUnknown* args) {
            if (m_isPopupWindow)
            {
                CloseAppWindow();
            }
            return S_OK;
        }).Get(),
        nullptr));
```

#### <span data-ttu-id="2ec86-388">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="2ec86-388">AddHostObjectToScript</span></span> 

<span data-ttu-id="2ec86-389">Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-389">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="2ec86-390">Public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(nome LPCWSTR, objeto Variant \*)</span><span class="sxs-lookup"><span data-stu-id="2ec86-390">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="2ec86-391">Os objetos host são expostos como proxies do objeto host via `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-391">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="2ec86-392">Os proxies do objeto host são promessas e serão resolvidos para um objeto que representa o objeto host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-392">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="2ec86-393">A promessa será recusada se o aplicativo não adicionar um objeto com o nome.</span><span class="sxs-lookup"><span data-stu-id="2ec86-393">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="2ec86-394">Quando o código JavaScript acessa uma propriedade ou método do objeto, uma promessa é retornada, que será resolvida para o valor retornado do host para a propriedade ou método, ou recusada em caso de erro, pois não há tal propriedade ou método no objeto ou parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="2ec86-394">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="2ec86-395">Por exemplo, quando o código do aplicativo faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2ec86-395">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="2ec86-396">O código JavaScript na WebView poderá acessar o appObject da seguinte forma e, em seguida, acessar atributos e métodos de appObject:</span><span class="sxs-lookup"><span data-stu-id="2ec86-396">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="2ec86-397">Observe que, enquanto tipos simples, IDispatch e matriz são compatíveis, IUnknown Generic, VT_DECIMAL ou Variant VT_RECORD não é suportada.</span><span class="sxs-lookup"><span data-stu-id="2ec86-397">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="2ec86-398">Objetos JavaScript remotos como funções de retorno de chamada são representados como uma variante VT_DISPATCH com o objeto que implementa IDispatch.</span><span class="sxs-lookup"><span data-stu-id="2ec86-398">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="2ec86-399">O método de retorno de chamada JavaScript pode ser invocado usando DISPID_VALUE para o DISPID.</span><span class="sxs-lookup"><span data-stu-id="2ec86-399">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="2ec86-400">Há suporte para matrizes aninhadas até uma profundidade de 3.</span><span class="sxs-lookup"><span data-stu-id="2ec86-400">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="2ec86-401">Matrizes de tipos de referência não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="2ec86-401">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="2ec86-402">VT_EMPTY e VT_NULL são mapeados para JavaScript como nulo.</span><span class="sxs-lookup"><span data-stu-id="2ec86-402">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="2ec86-403">Em JavaScript nulo e indefinido são mapeados para VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="2ec86-403">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="2ec86-404">Além disso, todos os objetos de host são expostos como `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-404">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="2ec86-405">Aqui, os objetos do host são expostos como proxies síncronos do objeto de host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-405">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="2ec86-406">Elas não são promessas e chamadas para funções ou acesso à propriedade o bloqueio síncrono de script em execução, aguardando a comunicação de processo cruzado para o código do host ser executado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-406">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="2ec86-407">Portanto, isso pode resultar em problemas de confiabilidade e é recomendável que você use a API assíncrona baseada em promessa `window.chrome.webview.hostObjects.<name>` descrita acima.</span><span class="sxs-lookup"><span data-stu-id="2ec86-407">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="2ec86-408">Proxies síncronos de objeto de host síncrono e proxies de objeto de host assíncrono podem proxy para o mesmo objeto host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-408">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="2ec86-409">As alterações remotas feitas por um proxy serão refletidas em qualquer outro proxy do mesmo objeto host se os outros proxies e síncronos ou assíncronos.</span><span class="sxs-lookup"><span data-stu-id="2ec86-409">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="2ec86-410">Embora o JavaScript seja bloqueado em uma chamada síncrona para o código nativo, esse código nativo não pode retornar a chamada para JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ec86-410">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="2ec86-411">As tentativas de fazer isso falharão com o HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="2ec86-411">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="2ec86-412">Os proxies do objeto de host são objetos de proxy JavaScript que interceptam todas as chamadas de propriedade, conjunto de propriedades e método.</span><span class="sxs-lookup"><span data-stu-id="2ec86-412">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="2ec86-413">Propriedades ou métodos que fazem parte da função ou do protótipo do objeto são executados localmente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-413">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="2ec86-414">Além disso, qualquer propriedade ou método na matriz `chrome.webview.hostObjects.options.forceLocalProperties` também será executado localmente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-414">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="2ec86-415">Isso assume como padrão os métodos opcionais que têm significado em JavaScript como `toJSON` e `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-415">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="2ec86-416">Você pode adicionar mais à matriz, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="2ec86-416">You can add more to this array as required.</span></span>

<span data-ttu-id="2ec86-417">Há um método `chrome.webview.hostObjects.cleanupSome` que melhor irá melhorar os proxies do objeto do host de coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="2ec86-417">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="2ec86-418">Os proxies de objetos host também têm os seguintes métodos que são executados localmente:</span><span class="sxs-lookup"><span data-stu-id="2ec86-418">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="2ec86-419">applyHostFunction, gethostproperty, sethostproperty: realize uma invocação de método, uma propriedade get ou um conjunto de propriedades no objeto host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-419">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="2ec86-420">Você pode usá-los para forçar explicitamente um método ou uma propriedade para execução remota se houver um método ou uma propriedade local conflitante.</span><span class="sxs-lookup"><span data-stu-id="2ec86-420">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="2ec86-421">Por exemplo, ele `proxy.toString()` executará o método ToString local no objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="2ec86-421">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="2ec86-422">Mas `proxy.applyHostFunction('toString')` é executado `toString` no objeto de proxy do host em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2ec86-422">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="2ec86-423">getlocalproperty, setlocalproperty: executar propriedade get ou Property definido localmente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-423">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="2ec86-424">Você pode usar esses métodos para forçar a obtenção ou configuração de uma propriedade no próprio proxy do objeto host, em vez de no objeto host que ele representa.</span><span class="sxs-lookup"><span data-stu-id="2ec86-424">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="2ec86-425">Por exemplo, receberá `proxy.unknownProperty` a propriedade nomeada `unknownProperty` do objeto host com proxy.</span><span class="sxs-lookup"><span data-stu-id="2ec86-425">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="2ec86-426">Mas receberá `proxy.getLocalProperty('unknownProperty')` o valor da propriedade `unknownProperty` no próprio objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="2ec86-426">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="2ec86-427">sincronização: proxies de objeto de host assíncronos expõem um método Sync que retorna uma promessa para um proxy de objeto de host síncrono para o mesmo objeto host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-427">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="2ec86-428">Por exemplo, `chrome.webview.hostObjects.sample.methodCall()` retorna um proxy de objeto de host assíncrono.</span><span class="sxs-lookup"><span data-stu-id="2ec86-428">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="2ec86-429">Você pode usar o `sync` método para obter um proxy de objeto de host síncrono em vez disso:</span><span class="sxs-lookup"><span data-stu-id="2ec86-429">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="2ec86-430">Async: proxies de objeto de host síncronos expõem um método Async que bloqueia e retorna um proxy de objeto de host assíncrono para o mesmo objeto host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-430">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="2ec86-431">Por exemplo, `chrome.webview.hostObjects.sync.sample.methodCall()` retorna um proxy de objeto de host síncrono.</span><span class="sxs-lookup"><span data-stu-id="2ec86-431">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="2ec86-432">Chamar o `async` método nesse bloco e, em seguida, retorna um proxy de objeto de host assíncrono para o mesmo objeto host:</span><span class="sxs-lookup"><span data-stu-id="2ec86-432">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="2ec86-433">em seguida: proxies de objetos de host assíncronos têm um método Where.</span><span class="sxs-lookup"><span data-stu-id="2ec86-433">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="2ec86-434">Isso permite que eles sejam awaitable.</span><span class="sxs-lookup"><span data-stu-id="2ec86-434">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="2ec86-435">retornará uma promessa que será resolvida com uma representação do objeto host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-435">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="2ec86-436">Se o proxy representar um literal JavaScript, uma cópia dele será retornada localmente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-436">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="2ec86-437">Se o proxy representar uma função, um proxy não awaitable será retornado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-437">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="2ec86-438">Se o proxy representar um objeto JavaScript com uma mistura de propriedades literais e propriedades de função, a cópia do objeto será retornada com algumas propriedades como proxies de objeto host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-438">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="2ec86-439">Todas as outras invocações de método e Propriedade (além dos métodos de proxy de objeto remoto acima, lista de forceLocalProperties e propriedades em protótipos de objeto e função) são executadas remotamente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-439">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="2ec86-440">Proxies de objetos de host assíncronos retornam uma promessa que representa a conclusão assíncrona da invocação remota do método ou a obtenção da propriedade.</span><span class="sxs-lookup"><span data-stu-id="2ec86-440">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="2ec86-441">A promessa é resolvida após a conclusão das operações remotas e as promessas são resolvidas para o valor resultante da operação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-441">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="2ec86-442">Os proxies de objeto de host síncrono funcionam da mesma forma, mas bloqueiam a execução de JavaScript e aguardam a conclusão da operação remota.</span><span class="sxs-lookup"><span data-stu-id="2ec86-442">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="2ec86-443">A configuração de uma propriedade em um proxy de objeto de host assíncrono funciona de forma ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-443">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="2ec86-444">O conjunto retorna imediatamente e o valor de retorno é o valor que será definido.</span><span class="sxs-lookup"><span data-stu-id="2ec86-444">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="2ec86-445">Isso é uma exigência do objeto proxy JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ec86-445">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="2ec86-446">Se você precisar esperar assincronamente o conjunto de propriedades para concluir, use o método sethostproperty que retorna uma promessa conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="2ec86-446">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="2ec86-447">Propriedade de conjunto de propriedades de objeto síncrono bloqueia sincronamente, até que a propriedade seja definida.</span><span class="sxs-lookup"><span data-stu-id="2ec86-447">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="2ec86-448">Por exemplo, suponha que você tenha um objeto COM com a seguinte interface</span><span class="sxs-lookup"><span data-stu-id="2ec86-448">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IHostObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        [propget] HRESULT IndexedProperty(INT index, [out, retval] BSTR * stringResult);
        [propput] HRESULT IndexedProperty(INT index, [in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);

    };
```
 <span data-ttu-id="2ec86-449">Poderemos adicionar uma instância dessa interface ao nosso JavaScript com `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-449">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="2ec86-450">Nesse caso, podemos nomeá-lo `sample` :</span><span class="sxs-lookup"><span data-stu-id="2ec86-450">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_hostObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddHostObjectToScript multiple times in a row without
            // calling RemoveHostObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(
                m_webView->AddHostObjectToScript(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```
 <span data-ttu-id="2ec86-451">Em seguida, no documento HTML, podemos usar esse objeto COM via `chrome.webview.hostObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="2ec86-451">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

```html
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = await chrome.webview.hostObjects.sample.property;
        document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
        const propertyValue = chrome.webview.hostObjects.sync.sample.property;
        document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyAsyncInput").value;
        // The following line will work but it will return immediately before the property value has actually been set.
        // If you need to set the property and wait for the property to change value, use the setRemote function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setRemote function.
        await chrome.webview.hostObjects.sample.setRemote("property", propertyValue);
        document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
        const propertyValue = document.getElementById("setPropertySyncInput").value;
        chrome.webview.hostObjects.sync.sample.property = propertyValue;
        document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("getIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("getIndexedPropertyAsyncParam").value);
        const resultValue = await chrome.webview.hostObjects.sample.IndexedProperty[index];
        document.getElementById("getIndexedPropertyAsyncOutput").textContent = resultValue;
        });
        document.getElementById("setIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("setIndexedPropertyAsyncParam1").value);
        const value = document.getElementById("setIndexedPropertyAsyncParam2").value;;
        chrome.webview.hostObjects.sample.IndexedProperty[index] = value;
        document.getElementById("setIndexedPropertyAsyncOutput").textContent = "Set";
        });
        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
        const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
        const resultValue = await chrome.webview.hostObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
        const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
        const resultValue = chrome.webview.hostObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
        chrome.webview.hostObjects.sample.CallCallbackAsynchronously(() => {
        document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
        });
        });
```

#### <span data-ttu-id="2ec86-452">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="2ec86-452">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="2ec86-453">Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-453">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="2ec86-454">Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="2ec86-454">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="2ec86-455">O script injetado se aplicará a todas as futuras navegações de documento de nível superior e quadro filho até que sejam removidas com o RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2ec86-455">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="2ec86-456">Isso é aplicado de forma assíncrona e você deve aguardar até que o manipulador de conclusão seja executado antes de poder ter certeza de que o script está pronto para ser executado em navegações futuras.</span><span class="sxs-lookup"><span data-stu-id="2ec86-456">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="2ec86-457">Observe que, se um documento HTML tiver uma área restrita de algum tipo via propriedades de [área restrita](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) ou o [cabeçalho HTTP de política de segurança de conteúdo](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) , isso afetará o script ser executado aqui.</span><span class="sxs-lookup"><span data-stu-id="2ec86-457">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="2ec86-458">Portanto, por exemplo, se a palavra-chave ' allow-janelarestritas ' não estiver definida, as chamadas para a `alert` função serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="2ec86-458">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="2ec86-459">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="2ec86-459">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="2ec86-460">Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-460">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="2ec86-461">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(URI const LPCWSTR, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="2ec86-461">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="2ec86-462">O parâmetro URI pode ser uma cadeia de caracteres curinga (' ': zero ou mais, '? ': exatamente um).</span><span class="sxs-lookup"><span data-stu-id="2ec86-462">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="2ec86-463">nullptr é equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="2ec86-463">nullptr is equivalent to L"".</span></span> <span data-ttu-id="2ec86-464">Consulte COREWEBVIEW2_WEB_RESOURCE_CONTEXT enumeração para obter a descrição dos filtros de contexto de recurso.</span><span class="sxs-lookup"><span data-stu-id="2ec86-464">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="2ec86-465">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="2ec86-465">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="2ec86-466">Chame um método DevToolsProtocol assíncrono.</span><span class="sxs-lookup"><span data-stu-id="2ec86-466">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="2ec86-467">Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="2ec86-467">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="2ec86-468">Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista e a descrição dos métodos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2ec86-468">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="2ec86-469">O parâmetro methodName é o nome completo do método no formato `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-469">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="2ec86-470">O parâmetro parametersAsJson é uma cadeia de caracteres JSON formatada que contém os parâmetros para o método correspondente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-470">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="2ec86-471">O método Invoke do manipulador será chamado quando o método for concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2ec86-471">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="2ec86-472">Invoke será chamado com o objeto Return do método como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="2ec86-472">Invoke will be called with the method's return object as a JSON string.</span></span>

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="2ec86-473">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="2ec86-473">CapturePreview</span></span> 

<span data-ttu-id="2ec86-474">Capture uma imagem do que o WebView está exibindo.</span><span class="sxs-lookup"><span data-stu-id="2ec86-474">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="2ec86-475">Public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) ImageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="2ec86-475">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="2ec86-476">Especifique o formato da imagem com o parâmetro imageFormat.</span><span class="sxs-lookup"><span data-stu-id="2ec86-476">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="2ec86-477">Os dados binários da imagem resultante são gravados no parâmetro imageStream fornecido.</span><span class="sxs-lookup"><span data-stu-id="2ec86-477">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="2ec86-478">Quando o CapturePreview termina de gravar no fluxo, o método Invoke no parâmetro do manipulador fornecido é chamado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-478">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="2ec86-479">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="2ec86-479">ExecuteScript</span></span> 

<span data-ttu-id="2ec86-480">Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-480">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="2ec86-481">Public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="2ec86-481">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="2ec86-482">Isso será executado de forma assíncrona e, quando concluída, se um manipulador for fornecido no parâmetro ExecuteScriptCompletedHandler, seu método Invoke será chamado com o resultado da avaliação do JavaScript fornecido.</span><span class="sxs-lookup"><span data-stu-id="2ec86-482">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="2ec86-483">O valor do resultado é uma cadeia de caracteres codificada JSON.</span><span class="sxs-lookup"><span data-stu-id="2ec86-483">The result value is a JSON encoded string.</span></span> <span data-ttu-id="2ec86-484">Se o resultado for indefinido, contiver um ciclo de referência ou não puder ser codificado em JSON, o valor NULL JSON será retornado como a cadeia de caracteres ' NULL '.</span><span class="sxs-lookup"><span data-stu-id="2ec86-484">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="2ec86-485">Observe que uma função sem valor de retorno explícito retorna indefinida.</span><span class="sxs-lookup"><span data-stu-id="2ec86-485">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="2ec86-486">Se o script executado lançar uma exceção não tratada, o resultado também será ' nulo '.</span><span class="sxs-lookup"><span data-stu-id="2ec86-486">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="2ec86-487">Esse método é aplicado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2ec86-487">This method is applied asynchronously.</span></span> <span data-ttu-id="2ec86-488">Se o método for chamado após o evento NavigationStarting durante a navegação, o script será executado no novo documento ao carregá-lo, ao lado do tempo em que ContentLoading é disparado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-488">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="2ec86-489">ExecuteScript funcionará mesmo se IsScriptEnabled estiver definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="2ec86-489">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### <span data-ttu-id="2ec86-490">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="2ec86-490">get_BrowserProcessId</span></span> 

<span data-ttu-id="2ec86-491">A ID do processo do navegador que hospeda o WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-491">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="2ec86-492">[get_BrowserProcessId](#get_browserprocessid)público HRESULT (valor UINT32 \*)</span><span class="sxs-lookup"><span data-stu-id="2ec86-492">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="2ec86-493">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="2ec86-493">get_CanGoBack</span></span> 

<span data-ttu-id="2ec86-494">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-494">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="2ec86-495">[get_CanGoBack](#get_cangoback)público HRESULT (bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="2ec86-495">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="2ec86-496">O evento Historychanged será acionado se CanGoBack alterar Value.</span><span class="sxs-lookup"><span data-stu-id="2ec86-496">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="2ec86-497">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="2ec86-497">get_CanGoForward</span></span> 

<span data-ttu-id="2ec86-498">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-498">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="2ec86-499">[get_CanGoForward](#get_cangoforward)público HRESULT (bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="2ec86-499">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="2ec86-500">O evento Historychanged será acionado se CanGoForward alterar Value.</span><span class="sxs-lookup"><span data-stu-id="2ec86-500">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="2ec86-501">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="2ec86-501">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="2ec86-502">Indica se a WebView contém um elemento HTML de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="2ec86-502">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="2ec86-503">[get_ContainsFullScreenElement](#get_containsfullscreenelement)público HRESULT (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="2ec86-503">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="2ec86-504">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="2ec86-504">get_DocumentTitle</span></span> 

<span data-ttu-id="2ec86-505">O título do documento atual de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2ec86-505">The title for the current top level document.</span></span>

> <span data-ttu-id="2ec86-506">público HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span><span class="sxs-lookup"><span data-stu-id="2ec86-506">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="2ec86-507">Se o documento não tiver um título explícito ou estiver vazio, um padrão que pode ou não corresponder ao URI do documento será usado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-507">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="2ec86-508">get_Settings</span><span class="sxs-lookup"><span data-stu-id="2ec86-508">get_Settings</span></span> 

<span data-ttu-id="2ec86-509">O objeto [ICoreWebView2Settings](icorewebview2settings.md) contém várias configurações modificáveis para a execução do WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-509">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="2ec86-510">público HRESULT [get_Settings](#get_settings)(configurações[ICoreWebView2Settings](icorewebview2settings.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="2ec86-510">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="2ec86-511">get_Source</span><span class="sxs-lookup"><span data-stu-id="2ec86-511">get_Source</span></span> 

<span data-ttu-id="2ec86-512">O URI do documento de nível superior atual.</span><span class="sxs-lookup"><span data-stu-id="2ec86-512">The URI of the current top level document.</span></span>

> <span data-ttu-id="2ec86-513">[get_Source](#get_source)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="2ec86-513">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="2ec86-514">Esse valor potencialmente muda como parte do acionamento do evento SourceChanged para alguns casos, como navegar para diferentes navegação de site ou de fragmento.</span><span class="sxs-lookup"><span data-stu-id="2ec86-514">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="2ec86-515">Ele permanecerá o mesmo para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual.</span><span class="sxs-lookup"><span data-stu-id="2ec86-515">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="2ec86-516">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="2ec86-516">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="2ec86-517">Obtenha um receptor de evento de protocolo DevTools que permite que você se inscreva em um evento de protocolo DevTools.</span><span class="sxs-lookup"><span data-stu-id="2ec86-517">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="2ec86-518">Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="2ec86-518">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="2ec86-519">O parâmetro EventName é o nome completo do evento no formato `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-519">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="2ec86-520">Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista da descrição de eventos de protocolo devtools e argumentos de evento.</span><span class="sxs-lookup"><span data-stu-id="2ec86-520">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="2ec86-521">GoBack</span><span class="sxs-lookup"><span data-stu-id="2ec86-521">GoBack</span></span> 

<span data-ttu-id="2ec86-522">Navega o WebView para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-522">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="2ec86-523">público HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="2ec86-523">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="2ec86-524">GoForward</span><span class="sxs-lookup"><span data-stu-id="2ec86-524">GoForward</span></span> 

<span data-ttu-id="2ec86-525">Navega o WebView para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-525">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="2ec86-526">Public HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="2ec86-526">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="2ec86-527">Navegar</span><span class="sxs-lookup"><span data-stu-id="2ec86-527">Navigate</span></span> 

<span data-ttu-id="2ec86-528">Fazer uma navegação do documento de nível superior para o URI especificado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-528">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="2ec86-529">público- [navegação](#navigate)HRESULT (URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2ec86-529">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="2ec86-530">Consulte os eventos de navegação para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="2ec86-530">See the navigation events for more information.</span></span> <span data-ttu-id="2ec86-531">Observe que isso iniciará uma navegação e o evento NavigationStarting correspondente será acionado algum tempo após a conclusão dessa chamada de navegação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-531">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
}
```

#### <span data-ttu-id="2ec86-532">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="2ec86-532">NavigateToString</span></span> 

<span data-ttu-id="2ec86-533">Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.</span><span class="sxs-lookup"><span data-stu-id="2ec86-533">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="2ec86-534">Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="2ec86-534">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="2ec86-535">O parâmetro htmlContent não pode ter mais de 2 MB de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2ec86-535">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="2ec86-536">A origem da nova página será: em branco.</span><span class="sxs-lookup"><span data-stu-id="2ec86-536">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="2ec86-537">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="2ec86-537">OpenDevToolsWindow</span></span> 

<span data-ttu-id="2ec86-538">Abre a janela do DevTools para o documento atual no WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-538">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="2ec86-539">Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="2ec86-539">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="2ec86-540">Não faz nada se for chamado quando a janela do DevTools já estiver aberta</span><span class="sxs-lookup"><span data-stu-id="2ec86-540">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="2ec86-541">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="2ec86-541">PostWebMessageAsJson</span></span> 

<span data-ttu-id="2ec86-542">Postar a WebMessage especificada no documento de nível superior neste WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-542">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="2ec86-543">Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="2ec86-543">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="2ec86-544">O evento Message da janela do documento de nível superior. Chrome. WebView será acionado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-544">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="2ec86-545">O JavaScript nesse documento pode assinar e cancelar a assinatura do evento por meio do seguinte:</span><span class="sxs-lookup"><span data-stu-id="2ec86-545">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="2ec86-546">Os argumentos do evento é uma instância de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="2ec86-546">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="2ec86-547">A configuração ICoreWebView2Settings:: IsWebMessageEnabled deve ser true ou esse método irá falhar com E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="2ec86-547">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="2ec86-548">A propriedade data do ARG do evento é o parâmetro da cadeia de caracteres WebMessage analisado como uma cadeia de caracteres JSON em um objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ec86-548">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="2ec86-549">A propriedade de origem do ARG do evento é uma referência ao `window.chrome.webview` objeto.</span><span class="sxs-lookup"><span data-stu-id="2ec86-549">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="2ec86-550">Consulte SetWebMessageReceivedEventHandler para obter informações sobre como enviar mensagens do documento HTML no WebView para o host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-550">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="2ec86-551">Esta mensagem é enviada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2ec86-551">This message is sent asynchronously.</span></span> <span data-ttu-id="2ec86-552">Se ocorrer uma navegação antes que a mensagem seja postada na página, a mensagem não será enviada.</span><span class="sxs-lookup"><span data-stu-id="2ec86-552">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="2ec86-553">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="2ec86-553">PostWebMessageAsString</span></span> 

<span data-ttu-id="2ec86-554">Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ec86-554">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="2ec86-555">Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="2ec86-555">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="2ec86-556">Isso se comporta exatamente da mesma maneira que PostWebMessageAsJson, mas a `window.chrome.webview` propriedade data do ARG (evento de mensagem) será uma cadeia de caracteres com o mesmo valor de webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="2ec86-556">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="2ec86-557">Use isso em vez de PostWebMessageAsJson se você quiser se comunicar por cadeias de caracteres simples em vez de objetos JSON.</span><span class="sxs-lookup"><span data-stu-id="2ec86-557">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="2ec86-558">Recarregar</span><span class="sxs-lookup"><span data-stu-id="2ec86-558">Reload</span></span> 

<span data-ttu-id="2ec86-559">Recarregar a página atual.</span><span class="sxs-lookup"><span data-stu-id="2ec86-559">Reload the current page.</span></span>

> <span data-ttu-id="2ec86-560">HRESULT ( [recarregamento](#reload)) público</span><span class="sxs-lookup"><span data-stu-id="2ec86-560">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="2ec86-561">Isso é semelhante a navegar para o URI do documento de nível superior atual, incluindo todos os eventos de navegação que estão sendo acionados e como respeitar as entradas no cache HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ec86-561">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="2ec86-562">Mas o histórico de back/forward não será modificado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-562">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="2ec86-563">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-563">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="2ec86-564">Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-564">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="2ec86-565">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-565">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-566">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="2ec86-566">remove_ContentLoading</span></span> 

<span data-ttu-id="2ec86-567">Remover um manipulador de eventos adicionado anteriormente com add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="2ec86-567">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="2ec86-568">[remove_ContentLoading](#remove_contentloading)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-568">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-569">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-569">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="2ec86-570">Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-570">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="2ec86-571">[remove_DocumentTitleChanged](#remove_documenttitlechanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-571">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-572">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2ec86-572">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="2ec86-573">Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-573">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="2ec86-574">[remove_FrameNavigationCompleted](#remove_framenavigationcompleted)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-574">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-575">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2ec86-575">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="2ec86-576">Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-576">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="2ec86-577">[remove_FrameNavigationStarting](#remove_framenavigationstarting)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-577">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-578">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-578">remove_HistoryChanged</span></span> 

<span data-ttu-id="2ec86-579">Remover um manipulador de eventos adicionado anteriormente com add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-579">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="2ec86-580">[remove_HistoryChanged](#remove_historychanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-580">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-581">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2ec86-581">remove_NavigationCompleted</span></span> 

<span data-ttu-id="2ec86-582">Remover um manipulador de eventos adicionado anteriormente com add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ec86-582">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="2ec86-583">[remove_NavigationCompleted](#remove_navigationcompleted)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-583">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-584">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2ec86-584">remove_NavigationStarting</span></span> 

<span data-ttu-id="2ec86-585">Remover um manipulador de eventos adicionado anteriormente com add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2ec86-585">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="2ec86-586">[remove_NavigationStarting](#remove_navigationstarting)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-586">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-587">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-587">remove_NewWindowRequested</span></span> 

<span data-ttu-id="2ec86-588">Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-588">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="2ec86-589">[remove_NewWindowRequested](#remove_newwindowrequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-589">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-590">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-590">remove_PermissionRequested</span></span> 

<span data-ttu-id="2ec86-591">Remover um manipulador de eventos adicionado anteriormente com add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-591">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="2ec86-592">[remove_PermissionRequested](#remove_permissionrequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-592">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-593">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="2ec86-593">remove_ProcessFailed</span></span> 

<span data-ttu-id="2ec86-594">Remover um manipulador de eventos adicionado anteriormente com add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2ec86-594">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="2ec86-595">[remove_ProcessFailed](#remove_processfailed)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-595">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-596">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="2ec86-596">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="2ec86-597">Remover um manipulador de eventos adicionado anteriormente com add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2ec86-597">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="2ec86-598">[remove_ScriptDialogOpening](#remove_scriptdialogopening)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-598">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-599">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="2ec86-599">remove_SourceChanged</span></span> 

<span data-ttu-id="2ec86-600">Remover um manipulador de eventos adicionado anteriormente com add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="2ec86-600">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="2ec86-601">[remove_SourceChanged](#remove_sourcechanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-601">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-602">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2ec86-602">remove_WebMessageReceived</span></span> 

<span data-ttu-id="2ec86-603">Remover um manipulador de eventos adicionado anteriormente com add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="2ec86-603">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="2ec86-604">[remove_WebMessageReceived](#remove_webmessagereceived)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-604">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-605">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-605">remove_WebResourceRequested</span></span> 

<span data-ttu-id="2ec86-606">Remover um manipulador de eventos adicionado anteriormente com add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-606">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="2ec86-607">[remove_WebResourceRequested](#remove_webresourcerequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-607">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-608">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="2ec86-608">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="2ec86-609">Remover um manipulador de eventos adicionado anteriormente com add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-609">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="2ec86-610">[remove_WindowCloseRequested](#remove_windowcloserequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="2ec86-610">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="2ec86-611">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="2ec86-611">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="2ec86-612">Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-612">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="2ec86-613">Public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2ec86-613">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="2ec86-614">Embora novas tentativas de acesso sejam negadas, se o objeto já for obtido por código JavaScript na WebView, o código JavaScript continuará a ter acesso a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="2ec86-614">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="2ec86-615">Chamar este método para um nome que já foi removido ou nunca adicionado falhará.</span><span class="sxs-lookup"><span data-stu-id="2ec86-615">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="2ec86-616">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="2ec86-616">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="2ec86-617">Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="2ec86-617">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="2ec86-618">Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2ec86-618">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="2ec86-619">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="2ec86-619">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="2ec86-620">Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ec86-620">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="2ec86-621">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(URI const LPCWSTR, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="2ec86-621">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="2ec86-622">Se o mesmo filtro tiver sido adicionado várias vezes, será preciso removê-lo quantas vezes forem adicionadas para que a remoção seja efetiva.</span><span class="sxs-lookup"><span data-stu-id="2ec86-622">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="2ec86-623">Retorna E_INVALIDARG para um filtro que nunca foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-623">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="2ec86-624">Parar</span><span class="sxs-lookup"><span data-stu-id="2ec86-624">Stop</span></span> 

<span data-ttu-id="2ec86-625">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="2ec86-625">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="2ec86-626">público- [limite](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="2ec86-626">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="2ec86-627">Não interrompe scripts.</span><span class="sxs-lookup"><span data-stu-id="2ec86-627">Does not stop scripts.</span></span>

#### <span data-ttu-id="2ec86-628">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="2ec86-628">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="2ec86-629">Formato de imagem usado pelo método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="2ec86-629">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="2ec86-630">Enumeração [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="2ec86-630">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="2ec86-631">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-631">Values</span></span>                         | <span data-ttu-id="2ec86-632">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-632">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-633">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="2ec86-633">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="2ec86-634">Formato de imagem PNG.</span><span class="sxs-lookup"><span data-stu-id="2ec86-634">PNG image format.</span></span>
<span data-ttu-id="2ec86-635">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="2ec86-635">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="2ec86-636">Formato de imagem JPEG.</span><span class="sxs-lookup"><span data-stu-id="2ec86-636">JPEG image format.</span></span>

#### <span data-ttu-id="2ec86-637">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="2ec86-637">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="2ec86-638">O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="2ec86-638">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="2ec86-639">Enumeração [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span><span class="sxs-lookup"><span data-stu-id="2ec86-639">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="2ec86-640">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-640">Values</span></span>                         | <span data-ttu-id="2ec86-641">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-641">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-642">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="2ec86-642">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="2ec86-643">Corresponde à mensagem do Window WM_KEYDOWN.</span><span class="sxs-lookup"><span data-stu-id="2ec86-643">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="2ec86-644">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="2ec86-644">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="2ec86-645">Corresponde à mensagem do Window WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="2ec86-645">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="2ec86-646">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="2ec86-646">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="2ec86-647">Corresponde à mensagem do Window WM_SYSKEYDOWN.</span><span class="sxs-lookup"><span data-stu-id="2ec86-647">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="2ec86-648">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="2ec86-648">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="2ec86-649">Corresponde à mensagem do Window WM_SYSKEYUP.</span><span class="sxs-lookup"><span data-stu-id="2ec86-649">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="2ec86-650">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="2ec86-650">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="2ec86-651">Motivo para mover o foco.</span><span class="sxs-lookup"><span data-stu-id="2ec86-651">Reason for moving focus.</span></span>

> <span data-ttu-id="2ec86-652">Enumeração [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span><span class="sxs-lookup"><span data-stu-id="2ec86-652">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="2ec86-653">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-653">Values</span></span>                         | <span data-ttu-id="2ec86-654">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-654">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-655">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="2ec86-655">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="2ec86-656">Configuração de código focalizada no WebView.</span><span class="sxs-lookup"><span data-stu-id="2ec86-656">Code setting focus into WebView.</span></span>
<span data-ttu-id="2ec86-657">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="2ec86-657">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="2ec86-658">Movendo o foco devido à guia passagem para frente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-658">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="2ec86-659">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="2ec86-659">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="2ec86-660">Movendo o foco devido a Tabulação de passagem para trás.</span><span class="sxs-lookup"><span data-stu-id="2ec86-660">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="2ec86-661">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="2ec86-661">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="2ec86-662">O tipo de uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="2ec86-662">The type of a permission request.</span></span>

> <span data-ttu-id="2ec86-663">Enumeração [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span><span class="sxs-lookup"><span data-stu-id="2ec86-663">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="2ec86-664">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-664">Values</span></span>                         | <span data-ttu-id="2ec86-665">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-665">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-666">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="2ec86-666">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="2ec86-667">Permissões desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="2ec86-667">Unknown permission.</span></span>
<span data-ttu-id="2ec86-668">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="2ec86-668">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="2ec86-669">Permissão para capturar o áudio.</span><span class="sxs-lookup"><span data-stu-id="2ec86-669">Permission to capture audio.</span></span>
<span data-ttu-id="2ec86-670">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="2ec86-670">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="2ec86-671">Permissão para capturar vídeo.</span><span class="sxs-lookup"><span data-stu-id="2ec86-671">Permission to capture video.</span></span>
<span data-ttu-id="2ec86-672">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="2ec86-672">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="2ec86-673">Permissão para acessar a localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="2ec86-673">Permission to access geolocation.</span></span>
<span data-ttu-id="2ec86-674">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="2ec86-674">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="2ec86-675">Permissão para enviar notificações da Web.</span><span class="sxs-lookup"><span data-stu-id="2ec86-675">Permission to send web notifications.</span></span>
<span data-ttu-id="2ec86-676">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="2ec86-676">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="2ec86-677">Permissão para acessar o sensor genérico.</span><span class="sxs-lookup"><span data-stu-id="2ec86-677">Permission to access generic sensor.</span></span>
<span data-ttu-id="2ec86-678">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="2ec86-678">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="2ec86-679">Permissão para ler a área de transferência do sistema sem um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="2ec86-679">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="2ec86-680">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="2ec86-680">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="2ec86-681">Resposta a uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="2ec86-681">Response to a permission request.</span></span>

> <span data-ttu-id="2ec86-682">Enumeração [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="2ec86-682">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="2ec86-683">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-683">Values</span></span>                         | <span data-ttu-id="2ec86-684">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-684">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-685">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2ec86-685">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="2ec86-686">Use o comportamento padrão do navegador, que normalmente solicita aos usuários a decisão.</span><span class="sxs-lookup"><span data-stu-id="2ec86-686">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="2ec86-687">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="2ec86-687">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="2ec86-688">Conceder a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="2ec86-688">Grant the permission request.</span></span>
<span data-ttu-id="2ec86-689">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="2ec86-689">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="2ec86-690">Negue a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="2ec86-690">Deny the permission request.</span></span>

#### <span data-ttu-id="2ec86-691">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="2ec86-691">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="2ec86-692">Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.</span><span class="sxs-lookup"><span data-stu-id="2ec86-692">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="2ec86-693">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="2ec86-693">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="2ec86-694">Consulte a documentação do WM_KEYDOWN para obter detalhes em[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="2ec86-694">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="2ec86-695">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="2ec86-695">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="2ec86-696">Tipo de falha de processo usada na interface ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="2ec86-696">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="2ec86-697">Enumeração [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="2ec86-697">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="2ec86-698">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-698">Values</span></span>                         | <span data-ttu-id="2ec86-699">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-699">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-700">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="2ec86-700">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="2ec86-701">Indica que o processo do navegador foi encerrado inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-701">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="2ec86-702">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="2ec86-702">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="2ec86-703">Indica que o processo de renderização terminou inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="2ec86-703">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="2ec86-704">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="2ec86-704">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="2ec86-705">Indica que o processo de renderização se torna não responsivo.</span><span class="sxs-lookup"><span data-stu-id="2ec86-705">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="2ec86-706">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="2ec86-706">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="2ec86-707">Tipo de caixa de diálogo JavaScript usada na interface ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="2ec86-707">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="2ec86-708">Enumeração [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="2ec86-708">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="2ec86-709">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-709">Values</span></span>                         | <span data-ttu-id="2ec86-710">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-710">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-711">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="2ec86-711">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="2ec86-712">Uma caixa de diálogo chamada por meio da função JavaScript Window. Alert.</span><span class="sxs-lookup"><span data-stu-id="2ec86-712">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="2ec86-713">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="2ec86-713">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="2ec86-714">Uma caixa de diálogo invocada pela janela. confirmar a função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ec86-714">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="2ec86-715">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="2ec86-715">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="2ec86-716">Uma caixa de diálogo chamada por meio da função de JavaScript Window. prompt.</span><span class="sxs-lookup"><span data-stu-id="2ec86-716">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="2ec86-717">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="2ec86-717">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="2ec86-718">Uma caixa de diálogo chamada pelo evento JavaScript beforeunload.</span><span class="sxs-lookup"><span data-stu-id="2ec86-718">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="2ec86-719">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="2ec86-719">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="2ec86-720">Valores de status de erro para navegações na Web.</span><span class="sxs-lookup"><span data-stu-id="2ec86-720">Error status values for web navigations.</span></span>

> <span data-ttu-id="2ec86-721">Enumeração [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="2ec86-721">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="2ec86-722">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-722">Values</span></span>                         | <span data-ttu-id="2ec86-723">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-723">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-724">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="2ec86-724">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="2ec86-725">Ocorreu um erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2ec86-725">An unknown error occurred.</span></span>
<span data-ttu-id="2ec86-726">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="2ec86-726">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="2ec86-727">O nome comum do certificado SSL não corresponde ao endereço Web.</span><span class="sxs-lookup"><span data-stu-id="2ec86-727">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="2ec86-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="2ec86-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="2ec86-729">O certificado SSL venceu.</span><span class="sxs-lookup"><span data-stu-id="2ec86-729">The SSL certificate has expired.</span></span>
<span data-ttu-id="2ec86-730">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2ec86-730">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="2ec86-731">O certificado do cliente SSL contém erros.</span><span class="sxs-lookup"><span data-stu-id="2ec86-731">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="2ec86-732">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="2ec86-732">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="2ec86-733">A revogação do certificado SSL foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="2ec86-733">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="2ec86-734">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="2ec86-734">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="2ec86-735">O certificado SSL é inválido &ndash; isso significa que o certificado não correspondia aos pins da chave pública para o nome do host, o certificado é assinado por uma autoridade não confiável ou por meio de um algoritmo de sinal fraco, o certificado declarado pelos nomes DNS viola restrições de nome, o certificado contém uma chave fraca, o período de validade do certificado é muito longo, falta de informações sobre a revogação ou o mecanismo de revogação, o nome do host não exclusivo, a falta de informações [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)de transparência do certificado</span><span class="sxs-lookup"><span data-stu-id="2ec86-735">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="2ec86-736">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="2ec86-736">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="2ec86-737">Não é possível acessar o host.</span><span class="sxs-lookup"><span data-stu-id="2ec86-737">The host is unreachable.</span></span>
<span data-ttu-id="2ec86-738">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2ec86-738">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="2ec86-739">A conexão expirou.</span><span class="sxs-lookup"><span data-stu-id="2ec86-739">The connection has timed out.</span></span>
<span data-ttu-id="2ec86-740">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="2ec86-740">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="2ec86-741">O servidor retornou uma resposta inválida ou não reconhecida.</span><span class="sxs-lookup"><span data-stu-id="2ec86-741">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="2ec86-742">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="2ec86-742">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="2ec86-743">A conexão foi anulada.</span><span class="sxs-lookup"><span data-stu-id="2ec86-743">The connection was aborted.</span></span>
<span data-ttu-id="2ec86-744">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="2ec86-744">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="2ec86-745">A conexão foi redefinida.</span><span class="sxs-lookup"><span data-stu-id="2ec86-745">The connection was reset.</span></span>
<span data-ttu-id="2ec86-746">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="2ec86-746">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="2ec86-747">A conexão à Internet foi perdida.</span><span class="sxs-lookup"><span data-stu-id="2ec86-747">The Internet connection has been lost.</span></span>
<span data-ttu-id="2ec86-748">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="2ec86-748">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="2ec86-749">Não é possível se conectar ao destino.</span><span class="sxs-lookup"><span data-stu-id="2ec86-749">Cannot connect to destination.</span></span>
<span data-ttu-id="2ec86-750">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="2ec86-750">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="2ec86-751">Não foi possível resolver o nome de host fornecido.</span><span class="sxs-lookup"><span data-stu-id="2ec86-751">Could not resolve provided host name.</span></span>
<span data-ttu-id="2ec86-752">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="2ec86-752">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="2ec86-753">A operação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="2ec86-753">The operation was canceled.</span></span>
<span data-ttu-id="2ec86-754">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="2ec86-754">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="2ec86-755">Falha no redirecionamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="2ec86-755">The request redirect failed.</span></span>
<span data-ttu-id="2ec86-756">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="2ec86-756">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="2ec86-757">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="2ec86-757">An unexpected error occurred.</span></span>

#### <span data-ttu-id="2ec86-758">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="2ec86-758">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="2ec86-759">Enumeração para contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="2ec86-759">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="2ec86-760">Enumeração [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="2ec86-760">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="2ec86-761">Valores</span><span class="sxs-lookup"><span data-stu-id="2ec86-761">Values</span></span>                         | <span data-ttu-id="2ec86-762">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ec86-762">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="2ec86-763">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="2ec86-763">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="2ec86-764">Todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="2ec86-764">All resources.</span></span>
<span data-ttu-id="2ec86-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="2ec86-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="2ec86-766">Recursos de documento.</span><span class="sxs-lookup"><span data-stu-id="2ec86-766">Document resources.</span></span>
<span data-ttu-id="2ec86-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="2ec86-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="2ec86-768">Recursos CSS.</span><span class="sxs-lookup"><span data-stu-id="2ec86-768">CSS resources.</span></span>
<span data-ttu-id="2ec86-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="2ec86-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="2ec86-770">Recursos de imagem.</span><span class="sxs-lookup"><span data-stu-id="2ec86-770">Image resources.</span></span>
<span data-ttu-id="2ec86-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="2ec86-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="2ec86-772">Outros recursos de mídia, como vídeos.</span><span class="sxs-lookup"><span data-stu-id="2ec86-772">Other media resources such as videos.</span></span>
<span data-ttu-id="2ec86-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="2ec86-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="2ec86-774">Recursos de fonte.</span><span class="sxs-lookup"><span data-stu-id="2ec86-774">Font resources.</span></span>
<span data-ttu-id="2ec86-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="2ec86-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="2ec86-776">Recursos de script.</span><span class="sxs-lookup"><span data-stu-id="2ec86-776">Script resources.</span></span>
<span data-ttu-id="2ec86-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="2ec86-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="2ec86-778">Solicitações HTTP XML.</span><span class="sxs-lookup"><span data-stu-id="2ec86-778">XML HTTP requests.</span></span>
<span data-ttu-id="2ec86-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="2ec86-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="2ec86-780">Busque a comunicação da API.</span><span class="sxs-lookup"><span data-stu-id="2ec86-780">Fetch API communication.</span></span>
<span data-ttu-id="2ec86-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="2ec86-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="2ec86-782">Recursos do texttrack.</span><span class="sxs-lookup"><span data-stu-id="2ec86-782">TextTrack resources.</span></span>
<span data-ttu-id="2ec86-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="2ec86-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="2ec86-784">Comunicação de API de EventSource.</span><span class="sxs-lookup"><span data-stu-id="2ec86-784">EventSource API communication.</span></span>
<span data-ttu-id="2ec86-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="2ec86-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="2ec86-786">Comunicação de API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="2ec86-786">WebSocket API communication.</span></span>
<span data-ttu-id="2ec86-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="2ec86-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="2ec86-788">Manifestos do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="2ec86-788">Web App Manifests.</span></span>
<span data-ttu-id="2ec86-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="2ec86-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="2ec86-790">Trocas HTTP assinadas.</span><span class="sxs-lookup"><span data-stu-id="2ec86-790">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="2ec86-791">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="2ec86-791">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="2ec86-792">Solicitações de ping.</span><span class="sxs-lookup"><span data-stu-id="2ec86-792">Ping requests.</span></span>
<span data-ttu-id="2ec86-793">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="2ec86-793">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="2ec86-794">Relatórios de violação de CSP.</span><span class="sxs-lookup"><span data-stu-id="2ec86-794">CSP Violation Reports.</span></span>
<span data-ttu-id="2ec86-795">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="2ec86-795">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="2ec86-796">Outros recursos.</span><span class="sxs-lookup"><span data-stu-id="2ec86-796">Other resources.</span></span>

