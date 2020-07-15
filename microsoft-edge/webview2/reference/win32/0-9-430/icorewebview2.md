---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 6fce29c2df69abc8d55d91c267b282702e567453
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881204"
---
# <span data-ttu-id="d1c59-104">0.9.430-ICoreWebView2 de interface</span><span class="sxs-lookup"><span data-stu-id="d1c59-104">0.9.430 - interface ICoreWebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="d1c59-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d1c59-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d1c59-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="d1c59-107">O WebView2 permite que você hospede conteúdo da Web usando a tecnologia de navegador da Web mais recente do Edge.</span><span class="sxs-lookup"><span data-stu-id="d1c59-107">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="d1c59-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d1c59-108">Summary</span></span>

 <span data-ttu-id="d1c59-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d1c59-109">Members</span></span>                        | <span data-ttu-id="d1c59-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1c59-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d1c59-111">get_Settings</span><span class="sxs-lookup"><span data-stu-id="d1c59-111">get_Settings</span></span>](#get_settings) | <span data-ttu-id="d1c59-112">O objeto ICoreWebView2Settings contém várias configurações modificáveis para a execução do WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-112">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="d1c59-113">get_Source</span><span class="sxs-lookup"><span data-stu-id="d1c59-113">get_Source</span></span>](#get_source) | <span data-ttu-id="d1c59-114">O URI do documento de nível superior atual.</span><span class="sxs-lookup"><span data-stu-id="d1c59-114">The URI of the current top level document.</span></span>
[<span data-ttu-id="d1c59-115">Navegar</span><span class="sxs-lookup"><span data-stu-id="d1c59-115">Navigate</span></span>](#navigate) | <span data-ttu-id="d1c59-116">Fazer uma navegação do documento de nível superior para o URI especificado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-116">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="d1c59-117">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="d1c59-117">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="d1c59-118">Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.</span><span class="sxs-lookup"><span data-stu-id="d1c59-118">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="d1c59-119">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d1c59-119">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="d1c59-120">Adicione um manipulador de eventos para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-120">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="d1c59-121">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d1c59-121">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="d1c59-122">Remover um manipulador de eventos adicionado anteriormente com add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-122">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="d1c59-123">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="d1c59-123">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="d1c59-124">Adicione um manipulador de eventos para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d1c59-124">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="d1c59-125">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="d1c59-125">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="d1c59-126">Remover um manipulador de eventos adicionado anteriormente com add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d1c59-126">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="d1c59-127">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-127">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="d1c59-128">SourceChanged é acionado quando a propriedade Source muda.</span><span class="sxs-lookup"><span data-stu-id="d1c59-128">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="d1c59-129">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-129">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="d1c59-130">Remover um manipulador de eventos adicionado anteriormente com add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-130">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="d1c59-131">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-131">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="d1c59-132">Cobrançaalterar Ouça a alteração do histórico de navegação do documento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="d1c59-132">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="d1c59-133">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-133">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="d1c59-134">Remover um manipulador de eventos adicionado anteriormente com add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-134">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="d1c59-135">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="d1c59-135">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="d1c59-136">Adicione um manipulador de eventos para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d1c59-136">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="d1c59-137">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="d1c59-137">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="d1c59-138">Remover um manipulador de eventos adicionado anteriormente com add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d1c59-138">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="d1c59-139">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d1c59-139">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="d1c59-140">Adicione um manipulador de eventos para o evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-140">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="d1c59-141">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d1c59-141">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="d1c59-142">Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-142">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="d1c59-143">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="d1c59-143">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="d1c59-144">Adicione um manipulador de eventos para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d1c59-144">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="d1c59-145">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="d1c59-145">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="d1c59-146">Remover um manipulador de eventos adicionado anteriormente com add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d1c59-146">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="d1c59-147">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-147">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="d1c59-148">Adicione um manipulador de eventos para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-148">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="d1c59-149">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-149">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="d1c59-150">Remover um manipulador de eventos adicionado anteriormente com add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-150">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="d1c59-151">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="d1c59-151">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="d1c59-152">Adicione um manipulador de eventos para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d1c59-152">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="d1c59-153">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="d1c59-153">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="d1c59-154">Remover um manipulador de eventos adicionado anteriormente com add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d1c59-154">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="d1c59-155">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="d1c59-155">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="d1c59-156">Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-156">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="d1c59-157">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="d1c59-157">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="d1c59-158">Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d1c59-158">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="d1c59-159">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="d1c59-159">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="d1c59-160">Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-160">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="d1c59-161">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="d1c59-161">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="d1c59-162">Capture uma imagem do que o WebView está exibindo.</span><span class="sxs-lookup"><span data-stu-id="d1c59-162">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="d1c59-163">Recarregar</span><span class="sxs-lookup"><span data-stu-id="d1c59-163">Reload</span></span>](#reload) | <span data-ttu-id="d1c59-164">Recarregar a página atual.</span><span class="sxs-lookup"><span data-stu-id="d1c59-164">Reload the current page.</span></span>
[<span data-ttu-id="d1c59-165">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="d1c59-165">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="d1c59-166">Postar a WebMessage especificada no documento de nível superior neste WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-166">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="d1c59-167">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="d1c59-167">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="d1c59-168">Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1c59-168">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="d1c59-169">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="d1c59-169">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="d1c59-170">Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-170">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="d1c59-171">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="d1c59-171">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="d1c59-172">Remover um manipulador de eventos adicionado anteriormente com add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="d1c59-172">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="d1c59-173">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="d1c59-173">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="d1c59-174">Chame um método DevToolsProtocol assíncrono.</span><span class="sxs-lookup"><span data-stu-id="d1c59-174">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="d1c59-175">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="d1c59-175">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="d1c59-176">A ID do processo do navegador que hospeda o WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-176">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="d1c59-177">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="d1c59-177">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="d1c59-178">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-178">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="d1c59-179">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="d1c59-179">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="d1c59-180">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-180">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="d1c59-181">GoBack</span><span class="sxs-lookup"><span data-stu-id="d1c59-181">GoBack</span></span>](#goback) | <span data-ttu-id="d1c59-182">Navega o WebView para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-182">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="d1c59-183">GoForward</span><span class="sxs-lookup"><span data-stu-id="d1c59-183">GoForward</span></span>](#goforward) | <span data-ttu-id="d1c59-184">Navega o WebView para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-184">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="d1c59-185">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="d1c59-185">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="d1c59-186">Obtenha um receptor de evento de protocolo DevTools que permite que você se inscreva em um evento de protocolo DevTools.</span><span class="sxs-lookup"><span data-stu-id="d1c59-186">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="d1c59-187">Parar</span><span class="sxs-lookup"><span data-stu-id="d1c59-187">Stop</span></span>](#stop) | <span data-ttu-id="d1c59-188">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="d1c59-188">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="d1c59-189">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-189">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="d1c59-190">Adicione um manipulador de eventos para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-190">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="d1c59-191">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-191">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="d1c59-192">Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-192">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="d1c59-193">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-193">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="d1c59-194">Adicione um manipulador de eventos para o evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-194">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="d1c59-195">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-195">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="d1c59-196">Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-196">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="d1c59-197">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="d1c59-197">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="d1c59-198">O título do documento atual de nível superior.</span><span class="sxs-lookup"><span data-stu-id="d1c59-198">The title for the current top level document.</span></span>
[<span data-ttu-id="d1c59-199">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="d1c59-199">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="d1c59-200">Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-200">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="d1c59-201">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d1c59-201">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="d1c59-202">Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-202">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="d1c59-203">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="d1c59-203">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="d1c59-204">Abre a janela do DevTools para o documento atual no WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-204">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="d1c59-205">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-205">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="d1c59-206">Notifica quando a propriedade ContainsFullScreenElement muda.</span><span class="sxs-lookup"><span data-stu-id="d1c59-206">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="d1c59-207">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-207">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="d1c59-208">Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-208">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="d1c59-209">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="d1c59-209">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="d1c59-210">Indica se a WebView contém um elemento HTML de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="d1c59-210">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="d1c59-211">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-211">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="d1c59-212">Adicione um manipulador de eventos para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-212">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="d1c59-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="d1c59-214">Remover um manipulador de eventos adicionado anteriormente com add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="d1c59-215">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="d1c59-215">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="d1c59-216">Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-216">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="d1c59-217">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="d1c59-217">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="d1c59-218">Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-218">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="d1c59-219">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-219">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="d1c59-220">Adicione um manipulador de eventos para o evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-220">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="d1c59-221">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-221">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="d1c59-222">Remover um manipulador de eventos adicionado anteriormente com add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-222">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="d1c59-223">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="d1c59-223">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#core_webview2_capture_preview_image_format) | <span data-ttu-id="d1c59-224">Formato de imagem usado pelo método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="d1c59-224">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="d1c59-225">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="d1c59-225">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#core_webview2_script_dialog_kind) | <span data-ttu-id="d1c59-226">Tipo de caixa de diálogo JavaScript usada na interface ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d1c59-226">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="d1c59-227">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="d1c59-227">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#core_webview2_process_failed_kind) | <span data-ttu-id="d1c59-228">Tipo de falha de processo usada na interface ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d1c59-228">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="d1c59-229">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="d1c59-229">CORE_WEBVIEW2_PERMISSION_KIND</span></span>](#core_webview2_permission_kind) | <span data-ttu-id="d1c59-230">O tipo de uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="d1c59-230">The type of a permission request.</span></span>
[<span data-ttu-id="d1c59-231">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="d1c59-231">CORE_WEBVIEW2_PERMISSION_STATE</span></span>](#core_webview2_permission_state) | <span data-ttu-id="d1c59-232">Resposta a uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="d1c59-232">Response to a permission request.</span></span>
[<span data-ttu-id="d1c59-233">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="d1c59-233">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span>](#core_webview2_web_error_status) | <span data-ttu-id="d1c59-234">Valores de status de erro para navegações na Web.</span><span class="sxs-lookup"><span data-stu-id="d1c59-234">Error status values for web navigations.</span></span>
[<span data-ttu-id="d1c59-235">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="d1c59-235">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#core_webview2_web_resource_context) | <span data-ttu-id="d1c59-236">Enumeração para contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="d1c59-236">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="d1c59-237">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="d1c59-237">Navigation events</span></span>

<span data-ttu-id="d1c59-238">A sequência normal de eventos de navegação é NavigationStarting, SourceChanged, ContentLoading e, em seguida, NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d1c59-238">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="d1c59-240">Observe que isso se destina a eventos de navegação com o mesmo evento Navigationid ARG.</span><span class="sxs-lookup"><span data-stu-id="d1c59-240">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="d1c59-241">Navegação eventos com diferentes args de eventos Navigationid podem sobrepor-se.</span><span class="sxs-lookup"><span data-stu-id="d1c59-241">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="d1c59-242">Por exemplo, se você iniciar um evento de navegação e, em seguida, iniciar uma outra navegação, verá o NavigationStarting para a primeira navegação acompanhada pela NavigationStarting da segunda navegação, seguida da NavigationCompleted para a primeira navegação e, em seguida, todos os demais eventos de navegação apropriados para a segunda navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-242">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="d1c59-243">Em casos de erro, pode ou não ser um evento ContentLoading dependendo se a navegação é continuada para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="d1c59-243">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="d1c59-244">No caso de um redirecionamento HTTP, haverá vários eventos NavigationStarting em uma linha, com os seguintes, o sinalizador isredirect definido.</span><span class="sxs-lookup"><span data-stu-id="d1c59-244">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="d1c59-245">Para monitorar ou cancelar navegações dentro de subquadros no WebView, use FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-245">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="d1c59-246">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="d1c59-246">Process model</span></span>

<span data-ttu-id="d1c59-247">O WebView2 usa o mesmo modelo de processo que o navegador da Web Edge.</span><span class="sxs-lookup"><span data-stu-id="d1c59-247">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="d1c59-248">Há um processo do navegador Edge por diretório de dados do usuário especificado em uma sessão do usuário que servirá qualquer processo de chamadas do WebView2 que especifique esse diretório de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="d1c59-248">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="d1c59-249">Isso significa que um processo do navegador Edge pode estar servindo vários processos de chamadas e um processo de chamada pode estar usando vários processos do navegador do Edge.</span><span class="sxs-lookup"><span data-stu-id="d1c59-249">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="d1c59-251">Fora de um processo de navegador, haverá alguns processos de processamento.</span><span class="sxs-lookup"><span data-stu-id="d1c59-251">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="d1c59-252">Elas são criadas, conforme necessário, para atender a vários quadros potencialmente em diferentes modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="d1c59-252">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="d1c59-253">O número de processos de renderização varia de acordo com o recurso de navegador de isolamento de site e o número de origens discadas discadas renderizadas em webviews associadas.</span><span class="sxs-lookup"><span data-stu-id="d1c59-253">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="d1c59-255">Você pode reagir a falhas e travamentos nesses processos do navegador e do renderizador usando o evento ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="d1c59-255">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="d1c59-256">Você pode desligar com segurança os processos do navegador e do renderizador associados usando o método Close.</span><span class="sxs-lookup"><span data-stu-id="d1c59-256">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="d1c59-257">Modelo de Threading</span><span class="sxs-lookup"><span data-stu-id="d1c59-257">Threading model</span></span>

<span data-ttu-id="d1c59-258">O WebView2 deve ser criado em um thread de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d1c59-258">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="d1c59-259">Especificamente um thread com um bombeamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d1c59-259">Specifically a thread with a message pump.</span></span> <span data-ttu-id="d1c59-260">Todos os retornos de chamada ocorrerão nesse thread e as chamadas para o WebView deverão ser feitas nesse thread.</span><span class="sxs-lookup"><span data-stu-id="d1c59-260">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="d1c59-261">Não é seguro usar a WebView a partir de outro thread.</span><span class="sxs-lookup"><span data-stu-id="d1c59-261">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="d1c59-262">Os retornos de chamada, incluindo manipuladores de eventos e manipuladores de conclusão, são executados em série.</span><span class="sxs-lookup"><span data-stu-id="d1c59-262">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="d1c59-263">Ou seja, se você tiver um manipulador de eventos em execução e iniciar um loop de mensagem, nenhum outro manipulador de eventos ou chamadas de retorno de conclusão começarão a ser executados de forma reentrada.</span><span class="sxs-lookup"><span data-stu-id="d1c59-263">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="d1c59-264">Segurança</span><span class="sxs-lookup"><span data-stu-id="d1c59-264">Security</span></span>

<span data-ttu-id="d1c59-265">Sempre verifique a propriedade Source da WebView antes de usar ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString ou qualquer outro método para enviar informações para o WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-265">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="d1c59-266">A WebView pode ter navegado para outra página por meio do usuário final interagindo com a página ou o script na página que está causando a navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-266">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="d1c59-267">Da mesma forma, tenha muito cuidado com o AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d1c59-267">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="d1c59-268">Todas as navegações futuras executarão esse script e, se ele fornecer acesso às informações destinadas apenas a determinada origem, qualquer documento HTML poderá ter acesso.</span><span class="sxs-lookup"><span data-stu-id="d1c59-268">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="d1c59-269">Ao examinar o resultado de uma chamada de método ExecuteScript, um evento WebMessageReceived, sempre verifique a fonte do remetente ou qualquer outro mecanismo de recebimento de informações de um documento HTML em uma WebView validar o URI do documento HTML é o que você espera.</span><span class="sxs-lookup"><span data-stu-id="d1c59-269">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="d1c59-270">Ao construir uma mensagem para enviar para um WebView, prefira usar PostWebMessageAsJson e construir o parâmetro de cadeia de caracteres JSON usando uma biblioteca JSON.</span><span class="sxs-lookup"><span data-stu-id="d1c59-270">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="d1c59-271">Isso evitará possíveis acidentes de codificar informações em uma cadeia de caracteres ou script JSON e garantir que nenhuma entrada controlada pelo invasor possa modificar o restante da mensagem JSON ou executar um script arbitrário.</span><span class="sxs-lookup"><span data-stu-id="d1c59-271">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="d1c59-272">Tipos de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="d1c59-272">String types</span></span>

<span data-ttu-id="d1c59-273">Parâmetros de cadeia de caracteres de saída são cadeias de caracteres de terminação NULL</span><span class="sxs-lookup"><span data-stu-id="d1c59-273">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="d1c59-274">O chamado aloca a cadeia de caracteres usando CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="d1c59-274">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="d1c59-275">A propriedade é transferida para o chamador e fica até o chamador liberar a memória usando o CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="d1c59-275">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="d1c59-276">Cadeias de caracteres em parâmetros são cadeias de caracteres terminadas LPCWSTR nulas.</span><span class="sxs-lookup"><span data-stu-id="d1c59-276">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="d1c59-277">O chamador garante que a cadeia de caracteres é válida para a duração da chamada de função síncrona.</span><span class="sxs-lookup"><span data-stu-id="d1c59-277">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="d1c59-278">Se o chamador precisa reter esse valor para algum ponto após a conclusão da chamada de função, o Calle deve alocar sua própria cópia do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1c59-278">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="d1c59-279">Análise de URI e JSON</span><span class="sxs-lookup"><span data-stu-id="d1c59-279">URI and JSON parsing</span></span>

<span data-ttu-id="d1c59-280">Vários métodos fornecem ou aceitam URIs e JSON como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1c59-280">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="d1c59-281">Use sua própria biblioteca preferida para analisar e gerar essas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1c59-281">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="d1c59-282">Se o WinRT estiver disponível para seu aplicativo, você pode usar `RuntimeClass_Windows_Data_Json_JsonObject` e `IJsonObjectStatics` analisar ou produzir cadeias de caracteres JSON ou `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analisar e produzir URIs.</span><span class="sxs-lookup"><span data-stu-id="d1c59-282">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="d1c59-283">Ambos trabalham em aplicativos Win32.</span><span class="sxs-lookup"><span data-stu-id="d1c59-283">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="d1c59-284">Se você usar o IUri e o CreateUri para analisar URIs, talvez queira usar os seguintes sinalizadores de criação de URI para que o comportamento de CreateUri corresponda melhor à análise de URI no WebView:</span><span class="sxs-lookup"><span data-stu-id="d1c59-284">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="d1c59-285">Depuração</span><span class="sxs-lookup"><span data-stu-id="d1c59-285">Debugging</span></span>

<span data-ttu-id="d1c59-286">Abra o DevTools com os atalhos normais: `F12` ou `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-286">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="d1c59-287">Você pode usar o `--auto-open-devtools-for-tabs` argumento de comando switch para que a janela do devtools seja aberta imediatamente ao criar a primeira vez uma WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-287">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="d1c59-288">Consulte a documentação do CreateCoreWebView2Host para saber como fornecer argumentos adicionais de linha de comando para o processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="d1c59-288">See CreateCoreWebView2Host documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="d1c59-289">Confira a chave do registro LoaderOverride para experimentar versões diferentes do WebView2 sem modificar seu aplicativo na documentação do CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="d1c59-289">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Host documentation.</span></span>

## <span data-ttu-id="d1c59-290">Controle de versão</span><span class="sxs-lookup"><span data-stu-id="d1c59-290">Versioning</span></span>

<span data-ttu-id="d1c59-291">Depois de usar uma versão específica do SDK para criar seu aplicativo, seu aplicativo pode acabar sendo executado com uma versão mais antiga ou mais recente dos binários instalados do navegador.</span><span class="sxs-lookup"><span data-stu-id="d1c59-291">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="d1c59-292">Até a versão 1.0.0.0 do WebView2, pode haver alterações significativas durante as atualizações que impedem que o SDK funcione com versões diferentes dos binários instalados do navegador.</span><span class="sxs-lookup"><span data-stu-id="d1c59-292">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="d1c59-293">Após a versão 1.0.0.0 versões diferentes do SDK podem funcionar com versões diferentes do navegador instalado seguindo estas práticas recomendadas:</span><span class="sxs-lookup"><span data-stu-id="d1c59-293">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="d1c59-294">Para fazer a conta de alterações significativas na API, verifique se há uma falha ao chamar a DLL de exportação CreateCoreWebView2Environment e ao chamar QueryInterface em qualquer objeto CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="d1c59-294">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="d1c59-295">Um valor de retorno de E_NOINTERFACE pode indicar que o SDK não é compatível com os binários do navegador Edge.</span><span class="sxs-lookup"><span data-stu-id="d1c59-295">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="d1c59-296">Verificar a falha de QueryInterface também contará em casos em que o SDK é mais recente do que a versão do navegador Edge e seu aplicativo tenta usar uma interface do qual o navegador Edge não reconhece.</span><span class="sxs-lookup"><span data-stu-id="d1c59-296">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="d1c59-297">Quando uma interface não está disponível, você pode considerar a possibilidade de desabilitar o recurso associado, se possível, ou informar ao usuário final que ele precisa atualizar o navegador.</span><span class="sxs-lookup"><span data-stu-id="d1c59-297">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="d1c59-298">Parte</span><span class="sxs-lookup"><span data-stu-id="d1c59-298">Members</span></span>

#### <span data-ttu-id="d1c59-299">get_Settings</span><span class="sxs-lookup"><span data-stu-id="d1c59-299">get_Settings</span></span> 

<span data-ttu-id="d1c59-300">O objeto ICoreWebView2Settings contém várias configurações modificáveis para a execução do WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-300">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="d1c59-301">público HRESULT [get_Settings](#get_settings)(configurações ICoreWebView2Settings \* \*)</span><span class="sxs-lookup"><span data-stu-id="d1c59-301">public HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings \*\* settings)</span></span>

#### <span data-ttu-id="d1c59-302">get_Source</span><span class="sxs-lookup"><span data-stu-id="d1c59-302">get_Source</span></span> 

<span data-ttu-id="d1c59-303">O URI do documento de nível superior atual.</span><span class="sxs-lookup"><span data-stu-id="d1c59-303">The URI of the current top level document.</span></span>

> <span data-ttu-id="d1c59-304">[get_Source](#get_source)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="d1c59-304">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="d1c59-305">Esse valor potencialmente muda como parte do acionamento do evento SourceChanged para alguns casos, como navegar para diferentes navegação de site ou de fragmento.</span><span class="sxs-lookup"><span data-stu-id="d1c59-305">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="d1c59-306">Ele permanecerá o mesmo para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual.</span><span class="sxs-lookup"><span data-stu-id="d1c59-306">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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

#### <span data-ttu-id="d1c59-307">Navegar</span><span class="sxs-lookup"><span data-stu-id="d1c59-307">Navigate</span></span> 

<span data-ttu-id="d1c59-308">Fazer uma navegação do documento de nível superior para o URI especificado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-308">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="d1c59-309">público- [navegação](#navigate)HRESULT (URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d1c59-309">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="d1c59-310">Consulte os eventos de navegação para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d1c59-310">See the navigation events for more information.</span></span> <span data-ttu-id="d1c59-311">Observe que isso iniciará uma navegação e o evento NavigationStarting correspondente será acionado algum tempo após a conclusão dessa chamada de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-311">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

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

#### <span data-ttu-id="d1c59-312">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="d1c59-312">NavigateToString</span></span> 

<span data-ttu-id="d1c59-313">Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.</span><span class="sxs-lookup"><span data-stu-id="d1c59-313">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="d1c59-314">Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="d1c59-314">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="d1c59-315">O parâmetro htmlContent não pode ter mais de 2 MB de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1c59-315">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="d1c59-316">A origem da nova página será: em branco.</span><span class="sxs-lookup"><span data-stu-id="d1c59-316">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="d1c59-317">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d1c59-317">add_NavigationStarting</span></span> 

<span data-ttu-id="d1c59-318">Adicione um manipulador de eventos para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-318">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="d1c59-319">Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-319">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-320">NavigationStarting é acionado quando o quadro principal do WebView está solicitando permissão para navegar para um URI diferente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-320">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="d1c59-321">Isso também será acionado para redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="d1c59-321">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="d1c59-322">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d1c59-322">remove_NavigationStarting</span></span> 

<span data-ttu-id="d1c59-323">Remover um manipulador de eventos adicionado anteriormente com add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-323">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="d1c59-324">[remove_NavigationStarting](#remove_navigationstarting)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-324">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-325">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="d1c59-325">add_ContentLoading</span></span> 

<span data-ttu-id="d1c59-326">Adicione um manipulador de eventos para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d1c59-326">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="d1c59-327">Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-327">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-328">ContentLoading é acionado antes que qualquer conteúdo seja carregado, incluindo scripts adicionados com AddScriptToExecuteOnDocumentCreated ContentLoading não será acionado se ocorrer uma mesma navegação de página (por exemplo, por meio de navegações de fragmento ou de histórico. pushstate).</span><span class="sxs-lookup"><span data-stu-id="d1c59-328">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="d1c59-329">Isso segue os eventos NavigationStarting e SourceChanged e precede os eventos Historychanged e NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d1c59-329">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="d1c59-330">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="d1c59-330">remove_ContentLoading</span></span> 

<span data-ttu-id="d1c59-331">Remover um manipulador de eventos adicionado anteriormente com add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d1c59-331">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="d1c59-332">[remove_ContentLoading](#remove_contentloading)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-332">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-333">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-333">add_SourceChanged</span></span> 

<span data-ttu-id="d1c59-334">SourceChanged é acionado quando a propriedade Source muda.</span><span class="sxs-lookup"><span data-stu-id="d1c59-334">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="d1c59-335">Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-335">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-336">SourceChanged é acionado para navegar para um site ou navegação de fragmento diferente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-336">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="d1c59-337">Ele não será acionado para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual.</span><span class="sxs-lookup"><span data-stu-id="d1c59-337">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="d1c59-338">SourceChanged é acionado antes de ContentLoading para navegação para um novo documento.</span><span class="sxs-lookup"><span data-stu-id="d1c59-338">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="d1c59-339">Adicione um manipulador de eventos para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-339">Add an event handler for the SourceChanged event.</span></span> 

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

#### <span data-ttu-id="d1c59-340">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-340">remove_SourceChanged</span></span> 

<span data-ttu-id="d1c59-341">Remover um manipulador de eventos adicionado anteriormente com add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-341">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="d1c59-342">[remove_SourceChanged](#remove_sourcechanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-342">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-343">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-343">add_HistoryChanged</span></span> 

<span data-ttu-id="d1c59-344">Cobrançaalterar Ouça a alteração do histórico de navegação do documento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="d1c59-344">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="d1c59-345">Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-345">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-346">Use Cobrançaalterar para verificar se get_CanGoBack/get_CanGoForward valor mudou.</span><span class="sxs-lookup"><span data-stu-id="d1c59-346">Use HistoryChange to check if get_CanGoBack/get_CanGoForward value has changed.</span></span> <span data-ttu-id="d1c59-347">Historychanged também é acionado para usar o GoBack/GoForward.</span><span class="sxs-lookup"><span data-stu-id="d1c59-347">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="d1c59-348">Historychanged é acionado após SourceChanged e ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d1c59-348">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="d1c59-349">Adicione um manipulador de eventos para o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-349">Add an event handler for the HistoryChanged event.</span></span> 

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

#### <span data-ttu-id="d1c59-350">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-350">remove_HistoryChanged</span></span> 

<span data-ttu-id="d1c59-351">Remover um manipulador de eventos adicionado anteriormente com add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-351">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="d1c59-352">[remove_HistoryChanged](#remove_historychanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-352">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-353">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="d1c59-353">add_NavigationCompleted</span></span> 

<span data-ttu-id="d1c59-354">Adicione um manipulador de eventos para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d1c59-354">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="d1c59-355">Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-355">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-356">O evento NavigationCompleted é acionado quando o WebView foi completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.</span><span class="sxs-lookup"><span data-stu-id="d1c59-356">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
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

#### <span data-ttu-id="d1c59-357">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="d1c59-357">remove_NavigationCompleted</span></span> 

<span data-ttu-id="d1c59-358">Remover um manipulador de eventos adicionado anteriormente com add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d1c59-358">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="d1c59-359">[remove_NavigationCompleted](#remove_navigationcompleted)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-359">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-360">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d1c59-360">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="d1c59-361">Adicione um manipulador de eventos para o evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-361">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="d1c59-362">Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-362">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-363">FrameNavigationStarting é acionado quando um quadro filho na WebView solicita permissão para navegar para um URI diferente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-363">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="d1c59-364">Isso também será acionado para redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="d1c59-364">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="d1c59-365">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="d1c59-365">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="d1c59-366">Remover um manipulador de eventos adicionado anteriormente com add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d1c59-366">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="d1c59-367">[remove_FrameNavigationStarting](#remove_framenavigationstarting)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-367">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-368">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="d1c59-368">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="d1c59-369">Adicione um manipulador de eventos para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d1c59-369">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="d1c59-370">Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-370">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-371">O evento é acionado quando uma caixa de diálogo JavaScript (alerta, confirmação ou prompt) aparecerá para o WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-371">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="d1c59-372">Esse evento só será acionado se a propriedade ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled estiver definida como false.</span><span class="sxs-lookup"><span data-stu-id="d1c59-372">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="d1c59-373">O evento ScriptDialogOpening pode ser usado para suprimir caixas de diálogo ou substituir caixas de diálogo padrão por caixas de diálogo personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d1c59-373">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
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

#### <span data-ttu-id="d1c59-374">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="d1c59-374">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="d1c59-375">Remover um manipulador de eventos adicionado anteriormente com add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d1c59-375">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="d1c59-376">[remove_ScriptDialogOpening](#remove_scriptdialogopening)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-376">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-377">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-377">add_PermissionRequested</span></span> 

<span data-ttu-id="d1c59-378">Adicione um manipulador de eventos para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-378">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="d1c59-379">Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-379">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-380">Acionado quando o conteúdo de uma WebView solicita permissão para acessar alguns recursos privilegiados.</span><span class="sxs-lookup"><span data-stu-id="d1c59-380">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
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

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="d1c59-381">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-381">remove_PermissionRequested</span></span> 

<span data-ttu-id="d1c59-382">Remover um manipulador de eventos adicionado anteriormente com add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-382">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="d1c59-383">[remove_PermissionRequested](#remove_permissionrequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-383">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-384">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="d1c59-384">add_ProcessFailed</span></span> 

<span data-ttu-id="d1c59-385">Adicione um manipulador de eventos para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d1c59-385">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="d1c59-386">Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-386">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-387">Acionado quando um processo da WebView termina inesperadamente ou não responde.</span><span class="sxs-lookup"><span data-stu-id="d1c59-387">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
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
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="d1c59-388">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="d1c59-388">remove_ProcessFailed</span></span> 

<span data-ttu-id="d1c59-389">Remover um manipulador de eventos adicionado anteriormente com add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d1c59-389">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="d1c59-390">[remove_ProcessFailed](#remove_processfailed)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-390">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-391">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="d1c59-391">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="d1c59-392">Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-392">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="d1c59-393">Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="d1c59-393">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="d1c59-394">O script injetado se aplicará a todas as futuras navegações de documento de nível superior e quadro filho até que sejam removidas com o RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d1c59-394">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="d1c59-395">Isso é aplicado de forma assíncrona e você deve aguardar até que o manipulador de conclusão seja executado antes de poder ter certeza de que o script está pronto para ser executado em navegações futuras.</span><span class="sxs-lookup"><span data-stu-id="d1c59-395">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="d1c59-396">Observe que, se um documento HTML tiver uma área restrita de algum tipo via propriedades de [área restrita](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) ou o [cabeçalho HTTP de política de segurança de conteúdo](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , isso afetará o script ser executado aqui.</span><span class="sxs-lookup"><span data-stu-id="d1c59-396">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="d1c59-397">Portanto, por exemplo, se a palavra-chave ' allow-janelarestritas ' não estiver definida, as chamadas para a `alert` função serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="d1c59-397">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="d1c59-398">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="d1c59-398">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="d1c59-399">Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d1c59-399">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="d1c59-400">Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d1c59-400">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="d1c59-401">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="d1c59-401">ExecuteScript</span></span> 

<span data-ttu-id="d1c59-402">Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-402">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="d1c59-403">Public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="d1c59-403">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="d1c59-404">Isso será executado de forma assíncrona e, quando concluída, se um manipulador for fornecido no parâmetro ExecuteScriptCompletedHandler, seu método Invoke será chamado com o resultado da avaliação do JavaScript fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1c59-404">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="d1c59-405">O valor do resultado é uma cadeia de caracteres codificada JSON.</span><span class="sxs-lookup"><span data-stu-id="d1c59-405">The result value is a JSON encoded string.</span></span> <span data-ttu-id="d1c59-406">Se o resultado for indefinido, contiver um ciclo de referência ou não puder ser codificado em JSON, o valor NULL JSON será retornado como a cadeia de caracteres ' NULL '.</span><span class="sxs-lookup"><span data-stu-id="d1c59-406">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="d1c59-407">Observe que uma função sem valor de retorno explícito retorna indefinida.</span><span class="sxs-lookup"><span data-stu-id="d1c59-407">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="d1c59-408">Se o script executado lançar uma exceção não tratada, o resultado também será ' nulo '.</span><span class="sxs-lookup"><span data-stu-id="d1c59-408">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="d1c59-409">Esse método é aplicado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d1c59-409">This method is applied asynchronously.</span></span> <span data-ttu-id="d1c59-410">Se a chamada for feita enquanto o WebView estiver em um documento e ocorrer uma navegação após a chamada ser feita, mas antes que o JavaScript seja executado, o script não será executado e o manipulador será chamado com E_FAIL para o parâmetro errorCode.</span><span class="sxs-lookup"><span data-stu-id="d1c59-410">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="d1c59-411">ExecuteScript funcionará mesmo se IsScriptEnabled estiver definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="d1c59-411">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="d1c59-412">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="d1c59-412">CapturePreview</span></span> 

<span data-ttu-id="d1c59-413">Capture uma imagem do que o WebView está exibindo.</span><span class="sxs-lookup"><span data-stu-id="d1c59-413">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="d1c59-414">Public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) ImageFormat, IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="d1c59-414">public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="d1c59-415">Especifique o formato da imagem com o parâmetro imageFormat.</span><span class="sxs-lookup"><span data-stu-id="d1c59-415">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="d1c59-416">Os dados binários da imagem resultante são gravados no parâmetro imageStream fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1c59-416">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="d1c59-417">Quando o CapturePreview termina de gravar no fluxo, o método Invoke no parâmetro do manipulador fornecido é chamado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-417">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
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

#### <span data-ttu-id="d1c59-418">Recarregar</span><span class="sxs-lookup"><span data-stu-id="d1c59-418">Reload</span></span> 

<span data-ttu-id="d1c59-419">Recarregar a página atual.</span><span class="sxs-lookup"><span data-stu-id="d1c59-419">Reload the current page.</span></span>

> <span data-ttu-id="d1c59-420">HRESULT ( [recarregamento](#reload)) público</span><span class="sxs-lookup"><span data-stu-id="d1c59-420">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="d1c59-421">Isso é semelhante a navegar para o URI do documento de nível superior atual, incluindo todos os eventos de navegação que estão sendo acionados e como respeitar as entradas no cache HTTP.</span><span class="sxs-lookup"><span data-stu-id="d1c59-421">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="d1c59-422">Mas o histórico de back/forward não será modificado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-422">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="d1c59-423">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="d1c59-423">PostWebMessageAsJson</span></span> 

<span data-ttu-id="d1c59-424">Postar a WebMessage especificada no documento de nível superior neste WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-424">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="d1c59-425">Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="d1c59-425">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="d1c59-426">O evento Message da janela do documento de nível superior. Chrome. WebView será acionado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-426">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="d1c59-427">O JavaScript nesse documento pode assinar e cancelar a assinatura do evento por meio do seguinte:</span><span class="sxs-lookup"><span data-stu-id="d1c59-427">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="d1c59-428">Os argumentos do evento é uma instância de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-428">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="d1c59-429">A configuração ICoreWebView2Settings:: IsWebMessageEnabled deve ser true ou esse método irá falhar com E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d1c59-429">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="d1c59-430">A propriedade data do ARG do evento é o parâmetro da cadeia de caracteres WebMessage analisado como uma cadeia de caracteres JSON em um objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1c59-430">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="d1c59-431">A propriedade de origem do ARG do evento é uma referência ao `window.chrome.webview` objeto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-431">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="d1c59-432">Consulte SetWebMessageReceivedEventHandler para obter informações sobre como enviar mensagens do documento HTML no WebView para o host.</span><span class="sxs-lookup"><span data-stu-id="d1c59-432">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="d1c59-433">Esta mensagem é enviada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d1c59-433">This message is sent asynchronously.</span></span> <span data-ttu-id="d1c59-434">Se ocorrer uma navegação antes que a mensagem seja postada na página, a mensagem não será enviada.</span><span class="sxs-lookup"><span data-stu-id="d1c59-434">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="d1c59-435">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="d1c59-435">PostWebMessageAsString</span></span> 

<span data-ttu-id="d1c59-436">Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1c59-436">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="d1c59-437">Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="d1c59-437">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="d1c59-438">Isso se comporta exatamente da mesma maneira que PostWebMessageAsJson, mas a `window.chrome.webview` propriedade data do ARG (evento de mensagem) será uma cadeia de caracteres com o mesmo valor de webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="d1c59-438">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="d1c59-439">Use isso em vez de PostWebMessageAsJson se você quiser se comunicar por cadeias de caracteres simples em vez de objetos JSON.</span><span class="sxs-lookup"><span data-stu-id="d1c59-439">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="d1c59-440">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="d1c59-440">add_WebMessageReceived</span></span> 

<span data-ttu-id="d1c59-441">Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-441">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="d1c59-442">[add_WebMessageReceived](#add_webmessagereceived)público HRESULT (manipulador[ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-442">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-443">A função CreateMessage é `void postMessage(object)` onde o objeto é qualquer objeto compatível com a conversão JSON.</span><span class="sxs-lookup"><span data-stu-id="d1c59-443">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```cpp
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

 <span data-ttu-id="d1c59-444">Quando a "CreateMessage" é chamado, o conjunto de [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) por meio desse método SetWebMessageReceivedEventHandler será invocado com o parâmetro de objeto da createmessagestring convertido em uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="d1c59-444">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="d1c59-445">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="d1c59-445">remove_WebMessageReceived</span></span> 

<span data-ttu-id="d1c59-446">Remover um manipulador de eventos adicionado anteriormente com add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="d1c59-446">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="d1c59-447">[remove_WebMessageReceived](#remove_webmessagereceived)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-447">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-448">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="d1c59-448">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="d1c59-449">Chame um método DevToolsProtocol assíncrono.</span><span class="sxs-lookup"><span data-stu-id="d1c59-449">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="d1c59-450">Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="d1c59-450">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="d1c59-451">Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista e a descrição dos métodos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d1c59-451">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="d1c59-452">O parâmetro methodName é o nome completo do método no formato `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-452">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="d1c59-453">O parâmetro parametersAsJson é uma cadeia de caracteres JSON formatada que contém os parâmetros para o método correspondente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-453">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="d1c59-454">O método Invoke do manipulador será chamado quando o método for concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d1c59-454">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="d1c59-455">Invoke será chamado com o objeto Return do método como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="d1c59-455">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="d1c59-456">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="d1c59-456">get_BrowserProcessId</span></span> 

<span data-ttu-id="d1c59-457">A ID do processo do navegador que hospeda o WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-457">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="d1c59-458">[get_BrowserProcessId](#get_browserprocessid)público HRESULT (valor UINT32 \*)</span><span class="sxs-lookup"><span data-stu-id="d1c59-458">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="d1c59-459">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="d1c59-459">get_CanGoBack</span></span> 

<span data-ttu-id="d1c59-460">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-460">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="d1c59-461">[get_CanGoBack](#get_cangoback)público HRESULT (bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="d1c59-461">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="d1c59-462">O evento Historychanged será acionado se get_CanGoBack alterar o valor.</span><span class="sxs-lookup"><span data-stu-id="d1c59-462">The HistoryChanged event will fire if get_CanGoBack changes value.</span></span>

#### <span data-ttu-id="d1c59-463">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="d1c59-463">get_CanGoForward</span></span> 

<span data-ttu-id="d1c59-464">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-464">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="d1c59-465">[get_CanGoForward](#get_cangoforward)público HRESULT (bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="d1c59-465">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="d1c59-466">O evento Historychanged será acionado se get_CanGoForward alterar o valor.</span><span class="sxs-lookup"><span data-stu-id="d1c59-466">The HistoryChanged event will fire if get_CanGoForward changes value.</span></span>

#### <span data-ttu-id="d1c59-467">GoBack</span><span class="sxs-lookup"><span data-stu-id="d1c59-467">GoBack</span></span> 

<span data-ttu-id="d1c59-468">Navega o WebView para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-468">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="d1c59-469">público HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="d1c59-469">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="d1c59-470">GoForward</span><span class="sxs-lookup"><span data-stu-id="d1c59-470">GoForward</span></span> 

<span data-ttu-id="d1c59-471">Navega o WebView para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-471">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="d1c59-472">Public HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="d1c59-472">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="d1c59-473">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="d1c59-473">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="d1c59-474">Obtenha um receptor de evento de protocolo DevTools que permite que você se inscreva em um evento de protocolo DevTools.</span><span class="sxs-lookup"><span data-stu-id="d1c59-474">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="d1c59-475">Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="d1c59-475">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="d1c59-476">O parâmetro EventName é o nome completo do evento no formato `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-476">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="d1c59-477">Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista da descrição de eventos de protocolo devtools e argumentos de evento.</span><span class="sxs-lookup"><span data-stu-id="d1c59-477">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="d1c59-478">Parar</span><span class="sxs-lookup"><span data-stu-id="d1c59-478">Stop</span></span> 

<span data-ttu-id="d1c59-479">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="d1c59-479">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="d1c59-480">público- [limite](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="d1c59-480">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="d1c59-481">Não interrompe scripts.</span><span class="sxs-lookup"><span data-stu-id="d1c59-481">Does not stop scripts.</span></span>

#### <span data-ttu-id="d1c59-482">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-482">add_NewWindowRequested</span></span> 

<span data-ttu-id="d1c59-483">Adicione um manipulador de eventos para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-483">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="d1c59-484">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-484">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-485">Acionado quando o conteúdo dentro do WebView solicitado para abrir uma nova janela, por exemplo, por meio de Window. Open.</span><span class="sxs-lookup"><span data-stu-id="d1c59-485">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="d1c59-486">O aplicativo pode passar um WebView de destino que será considerado a janela aberta.</span><span class="sxs-lookup"><span data-stu-id="d1c59-486">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
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

#### <span data-ttu-id="d1c59-487">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-487">remove_NewWindowRequested</span></span> 

<span data-ttu-id="d1c59-488">Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-488">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="d1c59-489">[remove_NewWindowRequested](#remove_newwindowrequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-489">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-490">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-490">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="d1c59-491">Adicione um manipulador de eventos para o evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-491">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="d1c59-492">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-492">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-493">O evento é acionado quando a propriedade DocumentTitle da WebView muda e pode ser acionada antes ou depois do evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d1c59-493">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="d1c59-494">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-494">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="d1c59-495">Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="d1c59-495">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="d1c59-496">[remove_DocumentTitleChanged](#remove_documenttitlechanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-496">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-497">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="d1c59-497">get_DocumentTitle</span></span> 

<span data-ttu-id="d1c59-498">O título do documento atual de nível superior.</span><span class="sxs-lookup"><span data-stu-id="d1c59-498">The title for the current top level document.</span></span>

> <span data-ttu-id="d1c59-499">público HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span><span class="sxs-lookup"><span data-stu-id="d1c59-499">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="d1c59-500">Se o documento não tiver um título explícito ou estiver vazio, um padrão que pode ou não corresponder ao URI do documento será usado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-500">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="d1c59-501">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="d1c59-501">AddRemoteObject</span></span> 

<span data-ttu-id="d1c59-502">Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-502">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="d1c59-503">Public HRESULT [Addremoteobject](#addremoteobject)(nome do LPCWSTR, objeto Variant \*)</span><span class="sxs-lookup"><span data-stu-id="d1c59-503">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="d1c59-504">Os objetos de host são expostos como proxies de objeto remoto via `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-504">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="d1c59-505">Proxies de objeto remoto são promessas e serão resolvidos para um objeto que representa o objeto host.</span><span class="sxs-lookup"><span data-stu-id="d1c59-505">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="d1c59-506">A promessa será recusada se o aplicativo não adicionar um objeto com o nome.</span><span class="sxs-lookup"><span data-stu-id="d1c59-506">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="d1c59-507">Quando o código JavaScript acessa uma propriedade ou método do objeto, uma promessa é retornada, que será resolvida para o valor retornado do host para a propriedade ou método, ou recusada em caso de erro, pois não há tal propriedade ou método no objeto ou parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="d1c59-507">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="d1c59-508">Por exemplo, quando o código do aplicativo faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d1c59-508">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="d1c59-509">O código JavaScript na WebView poderá acessar o appObject da seguinte forma e, em seguida, acessar atributos e métodos de appObject:</span><span class="sxs-lookup"><span data-stu-id="d1c59-509">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="d1c59-510">Observe que, enquanto tipos simples, IDispatch e matriz são compatíveis, IUnknown Generic, VT_DECIMAL ou Variant VT_RECORD não é suportada.</span><span class="sxs-lookup"><span data-stu-id="d1c59-510">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="d1c59-511">Objetos JavaScript remotos como funções de retorno de chamada são representados como uma variante VT_DISPATCH com o objeto que implementa IDispatch.</span><span class="sxs-lookup"><span data-stu-id="d1c59-511">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="d1c59-512">O método de retorno de chamada JavaScript pode ser invocado usando DISPID_VALUE para o DISPID.</span><span class="sxs-lookup"><span data-stu-id="d1c59-512">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="d1c59-513">Há suporte para matrizes aninhadas até uma profundidade de 3.</span><span class="sxs-lookup"><span data-stu-id="d1c59-513">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="d1c59-514">Matrizes de tipos de referência não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="d1c59-514">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="d1c59-515">VT_EMPTY e VT_NULL são mapeados para JavaScript como nulo.</span><span class="sxs-lookup"><span data-stu-id="d1c59-515">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="d1c59-516">Em JavaScript nulo e indefinido são mapeados para VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="d1c59-516">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="d1c59-517">Além disso, todos os objetos remotos são expostos como `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-517">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="d1c59-518">Aqui, os objetos do host são expostos como proxies síncronos de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-518">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="d1c59-519">Elas não são promessas e chamadas para funções ou acesso à propriedade o bloqueio síncrono de script em execução, aguardando a comunicação de processo cruzado para o código do host ser executado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-519">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="d1c59-520">Portanto, isso pode resultar em problemas de confiabilidade e é recomendável que você use a API assíncrona baseada em promessa `window.chrome.webview.remoteObjects.<name>` descrita acima.</span><span class="sxs-lookup"><span data-stu-id="d1c59-520">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="d1c59-521">Proxies de objetos remotos síncronos e proxies de objeto remoto assíncrono podem proxy para o mesmo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-521">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="d1c59-522">As alterações remotas feitas por um proxy serão refletidas em qualquer outro proxy do mesmo objeto remoto, seja os outros proxies e síncronos ou assíncronos.</span><span class="sxs-lookup"><span data-stu-id="d1c59-522">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="d1c59-523">Embora o JavaScript seja bloqueado em uma chamada síncrona para o código nativo, esse código nativo não pode retornar a chamada para JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1c59-523">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="d1c59-524">As tentativas de fazer isso falharão com o HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="d1c59-524">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="d1c59-525">Proxies de objeto remoto são objetos de proxy JavaScript que interceptam todas as invocações de propriedade, conjunto de propriedades e invocação de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d1c59-525">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="d1c59-526">Propriedades ou métodos que fazem parte da função ou do protótipo do objeto são executados localmente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-526">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="d1c59-527">Além disso, qualquer propriedade ou método na matriz `chrome.webview.remoteObjects.options.forceLocalProperties` também será executado localmente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-527">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="d1c59-528">Isso assume como padrão os métodos opcionais que têm significado em JavaScript como `toJSON` e `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-528">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="d1c59-529">Você pode adicionar mais à matriz, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="d1c59-529">You can add more to this array as required.</span></span>

<span data-ttu-id="d1c59-530">Há um método `chrome.webview.remoteObjects.cleanupSome` que melhor esforço coletará os proxies de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="d1c59-530">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="d1c59-531">Os proxies de objetos remotos também têm os seguintes métodos que são executados localmente:</span><span class="sxs-lookup"><span data-stu-id="d1c59-531">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="d1c59-532">applyRemote, getRemote, SetRemote: execute uma invocação de método, uma propriedade get ou uma propriedade definida no objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-532">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="d1c59-533">Você pode usá-los para forçar explicitamente um método ou uma propriedade para execução remota se houver um método ou uma propriedade local conflitante.</span><span class="sxs-lookup"><span data-stu-id="d1c59-533">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="d1c59-534">Por exemplo, ele `proxy.toString()` executará o método ToString local no objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="d1c59-534">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="d1c59-535">Mas `proxy.applyRemote('toString')` é executado `toString` no objeto em proxy remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-535">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="d1c59-536">getLocal, setlocal: executar propriedade get ou Property definido localmente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-536">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="d1c59-537">Você pode usar esses métodos para forçar a obtenção ou configuração de uma propriedade no próprio proxy de objeto remoto, em vez de no objeto remoto que ele representa.</span><span class="sxs-lookup"><span data-stu-id="d1c59-537">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="d1c59-538">Por exemplo, receberá `proxy.unknownProperty` a propriedade nomeada `unknownProperty` do objeto com proxy remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-538">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="d1c59-539">Mas receberá `proxy.getLocal('unknownProperty')` o valor da propriedade `unknownProperty` no próprio objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="d1c59-539">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="d1c59-540">sincronização: proxies de objetos remotos assíncronos expõem um método de sincronização que retorna uma promessa para um proxy síncrono de objeto remoto para o mesmo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-540">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="d1c59-541">Por exemplo, `chrome.webview.remoteObjects.sample.methodCall()` retorna um proxy de objeto remoto assíncrono.</span><span class="sxs-lookup"><span data-stu-id="d1c59-541">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="d1c59-542">Você pode usar o `sync` método para obter um proxy de objeto remoto síncrono em vez disso:</span><span class="sxs-lookup"><span data-stu-id="d1c59-542">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="d1c59-543">Async: proxies de objetos remotos síncronos expõem um método Async que bloqueia e retorna um proxy de objeto remoto assíncrono para o mesmo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-543">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="d1c59-544">Por exemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` retorna um proxy síncrono de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-544">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="d1c59-545">Chamar o `async` método nesse bloco e, em seguida, retorna um proxy de objeto remoto assíncrono para o mesmo objeto remoto:</span><span class="sxs-lookup"><span data-stu-id="d1c59-545">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="d1c59-546">em seguida: proxies de objetos remotos assíncronos têm um método Where.</span><span class="sxs-lookup"><span data-stu-id="d1c59-546">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="d1c59-547">Isso permite que eles sejam awaitable.</span><span class="sxs-lookup"><span data-stu-id="d1c59-547">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="d1c59-548">retornará uma promessa que será resolvida com uma representação do objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-548">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="d1c59-549">Se o proxy representar um literal JavaScript, uma cópia dele será retornada localmente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-549">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="d1c59-550">Se o proxy representar uma função, um proxy não awaitable será retornado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-550">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="d1c59-551">Se o proxy representar um objeto JavaScript com uma mistura de propriedades literais e propriedades de função, a cópia do objeto será retornada com algumas propriedades como proxies de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-551">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="d1c59-552">Todas as outras invocações de método e Propriedade (além dos métodos de proxy de objeto remoto acima, lista de forceLocalProperties e propriedades em protótipos de objeto e função) são executadas remotamente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-552">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="d1c59-553">Proxies assíncronos de objetos remotos retornam uma promessa que representa a conclusão assíncrona da invocação remota do método ou a obtenção da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d1c59-553">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="d1c59-554">A promessa é resolvida após a conclusão das operações remotas e as promessas são resolvidas para o valor resultante da operação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-554">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="d1c59-555">Os proxies de objetos remotos síncronos funcionam da mesma forma, mas bloqueiam a execução de JavaScript e aguardam a conclusão da operação remota.</span><span class="sxs-lookup"><span data-stu-id="d1c59-555">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="d1c59-556">A configuração de uma propriedade em um proxy de objeto remoto assíncrono funciona de forma ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-556">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="d1c59-557">O conjunto retorna imediatamente e o valor de retorno é o valor que será definido.</span><span class="sxs-lookup"><span data-stu-id="d1c59-557">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="d1c59-558">Isso é uma exigência do objeto proxy JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1c59-558">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="d1c59-559">Se você precisar esperar assincronamente o conjunto de propriedades para concluir, use o método SetRemote que retorna uma promessa conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="d1c59-559">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="d1c59-560">Propriedade de conjunto de propriedades de objeto síncrono bloqueia sincronamente, até que a propriedade seja definida.</span><span class="sxs-lookup"><span data-stu-id="d1c59-560">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="d1c59-561">Por exemplo, suponha que você tenha um objeto COM com a seguinte interface</span><span class="sxs-lookup"><span data-stu-id="d1c59-561">For example, suppose you have a COM object with the following interface</span></span>

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 <span data-ttu-id="d1c59-562">Poderemos adicionar uma instância dessa interface ao nosso JavaScript com `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="d1c59-562">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="d1c59-563">Nesse caso, podemos nomeá-lo `sample` :</span><span class="sxs-lookup"><span data-stu-id="d1c59-563">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 <span data-ttu-id="d1c59-564">Em seguida, no documento HTML, podemos usar esse objeto COM via `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="d1c59-564">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### <span data-ttu-id="d1c59-565">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d1c59-565">RemoveRemoteObject</span></span> 

<span data-ttu-id="d1c59-566">Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-566">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="d1c59-567">Public HRESULT [RemoveRemoteObject](#removeremoteobject)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d1c59-567">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="d1c59-568">Embora novas tentativas de acesso sejam negadas, se o objeto já for obtido por código JavaScript na WebView, o código JavaScript continuará a ter acesso a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="d1c59-568">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="d1c59-569">Chamar este método para um nome que já foi removido ou nunca adicionado falhará.</span><span class="sxs-lookup"><span data-stu-id="d1c59-569">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="d1c59-570">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="d1c59-570">OpenDevToolsWindow</span></span> 

<span data-ttu-id="d1c59-571">Abre a janela do DevTools para o documento atual no WebView.</span><span class="sxs-lookup"><span data-stu-id="d1c59-571">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="d1c59-572">Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="d1c59-572">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="d1c59-573">Não faz nada se for chamado quando a janela do DevTools já estiver aberta</span><span class="sxs-lookup"><span data-stu-id="d1c59-573">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="d1c59-574">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-574">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="d1c59-575">Notifica quando a propriedade ContainsFullScreenElement muda.</span><span class="sxs-lookup"><span data-stu-id="d1c59-575">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="d1c59-576">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-576">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-577">Isso significa que um elemento HTML dentro do WebView está entrando em tela inteira no tamanho do WebView ou sai do fullscreen.</span><span class="sxs-lookup"><span data-stu-id="d1c59-577">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="d1c59-578">Esse evento é útil quando, por exemplo, um elemento de vídeo solicita a tela inteira.</span><span class="sxs-lookup"><span data-stu-id="d1c59-578">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="d1c59-579">O ouvinte de ContainsFullScreenElementChanged pode então redimensionar a WebView em resposta.</span><span class="sxs-lookup"><span data-stu-id="d1c59-579">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="d1c59-580">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="d1c59-580">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="d1c59-581">Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-581">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="d1c59-582">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-582">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-583">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="d1c59-583">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="d1c59-584">Indica se a WebView contém um elemento HTML de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="d1c59-584">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="d1c59-585">[get_ContainsFullScreenElement](#get_containsfullscreenelement)público HRESULT (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="d1c59-585">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="d1c59-586">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-586">add_WebResourceRequested</span></span> 

<span data-ttu-id="d1c59-587">Adicione um manipulador de eventos para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-587">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="d1c59-588">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-588">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-589">Acionado quando o WebView está executando uma solicitação HTTP para uma URL correspondente e um filtro de contexto de recurso que foi adicionado com o AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="d1c59-589">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="d1c59-590">Pelo menos um filtro deve ser adicionado para que o evento seja acionado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-590">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
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

#### <span data-ttu-id="d1c59-591">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-591">remove_WebResourceRequested</span></span> 

<span data-ttu-id="d1c59-592">Remover um manipulador de eventos adicionado anteriormente com add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-592">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="d1c59-593">[remove_WebResourceRequested](#remove_webresourcerequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-593">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-594">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="d1c59-594">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="d1c59-595">Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-595">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="d1c59-596">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(URI const LPCWSTR,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="d1c59-596">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="d1c59-597">O parâmetro URI pode ser uma cadeia de caracteres curinga (' ': zero ou mais, '? ': exatamente um).</span><span class="sxs-lookup"><span data-stu-id="d1c59-597">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="d1c59-598">nullptr é equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="d1c59-598">nullptr is equivalent to L"".</span></span> <span data-ttu-id="d1c59-599">Consulte CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enumeração para obter a descrição dos filtros de contexto de recurso.</span><span class="sxs-lookup"><span data-stu-id="d1c59-599">See CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="d1c59-600">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="d1c59-600">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="d1c59-601">Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-601">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="d1c59-602">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(URI const LPCWSTR,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="d1c59-602">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="d1c59-603">Se o mesmo filtro tiver sido adicionado várias vezes, será preciso removê-lo quantas vezes forem adicionadas para que a remoção seja efetiva.</span><span class="sxs-lookup"><span data-stu-id="d1c59-603">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="d1c59-604">Retorna E_INVALIDARG para um filtro que nunca foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-604">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="d1c59-605">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-605">add_WindowCloseRequested</span></span> 

<span data-ttu-id="d1c59-606">Adicione um manipulador de eventos para o evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-606">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="d1c59-607">Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d1c59-607">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d1c59-608">Dispara quando o conteúdo dentro do WebView solicitado para fechar a janela, como After Window. Close, é chamado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-608">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="d1c59-609">O aplicativo deve fechar a janela da WebView e do aplicativo relacionado se isso fizer sentido com o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d1c59-609">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="d1c59-610">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="d1c59-610">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="d1c59-611">Remover um manipulador de eventos adicionado anteriormente com add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="d1c59-611">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="d1c59-612">[remove_WindowCloseRequested](#remove_windowcloserequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d1c59-612">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d1c59-613">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="d1c59-613">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="d1c59-614">Formato de imagem usado pelo método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="d1c59-614">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="d1c59-615">Enumeração [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="d1c59-615">enum [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="d1c59-616">Valores</span><span class="sxs-lookup"><span data-stu-id="d1c59-616">Values</span></span>                         | <span data-ttu-id="d1c59-617">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1c59-617">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d1c59-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="d1c59-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="d1c59-619">Formato de imagem PNG.</span><span class="sxs-lookup"><span data-stu-id="d1c59-619">PNG image format.</span></span>
<span data-ttu-id="d1c59-620">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="d1c59-620">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="d1c59-621">Formato de imagem JPEG.</span><span class="sxs-lookup"><span data-stu-id="d1c59-621">JPEG image format.</span></span>

#### <span data-ttu-id="d1c59-622">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="d1c59-622">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="d1c59-623">Tipo de caixa de diálogo JavaScript usada na interface ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d1c59-623">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="d1c59-624">Enumeração [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="d1c59-624">enum [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="d1c59-625">Valores</span><span class="sxs-lookup"><span data-stu-id="d1c59-625">Values</span></span>                         | <span data-ttu-id="d1c59-626">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1c59-626">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d1c59-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="d1c59-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="d1c59-628">Uma caixa de diálogo chamada por meio da função JavaScript Window. Alert.</span><span class="sxs-lookup"><span data-stu-id="d1c59-628">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="d1c59-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="d1c59-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="d1c59-630">Uma caixa de diálogo invocada pela janela. confirmar a função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1c59-630">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="d1c59-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="d1c59-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="d1c59-632">Uma caixa de diálogo chamada por meio da função de JavaScript Window. prompt.</span><span class="sxs-lookup"><span data-stu-id="d1c59-632">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="d1c59-633">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="d1c59-633">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="d1c59-634">Uma caixa de diálogo chamada pelo evento JavaScript beforeunload.</span><span class="sxs-lookup"><span data-stu-id="d1c59-634">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="d1c59-635">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="d1c59-635">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="d1c59-636">Tipo de falha de processo usada na interface ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="d1c59-636">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="d1c59-637">Enumeração [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="d1c59-637">enum [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span></span>

 <span data-ttu-id="d1c59-638">Valores</span><span class="sxs-lookup"><span data-stu-id="d1c59-638">Values</span></span>                         | <span data-ttu-id="d1c59-639">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1c59-639">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d1c59-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="d1c59-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="d1c59-641">Indica que o processo do navegador foi encerrado inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-641">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="d1c59-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="d1c59-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="d1c59-643">Indica que o processo de renderização terminou inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="d1c59-643">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="d1c59-644">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="d1c59-644">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="d1c59-645">Indica que o processo de renderização se torna não responsivo.</span><span class="sxs-lookup"><span data-stu-id="d1c59-645">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="d1c59-646">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="d1c59-646">CORE_WEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="d1c59-647">O tipo de uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="d1c59-647">The type of a permission request.</span></span>

> <span data-ttu-id="d1c59-648">Enumeração [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span><span class="sxs-lookup"><span data-stu-id="d1c59-648">enum [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span></span>

 <span data-ttu-id="d1c59-649">Valores</span><span class="sxs-lookup"><span data-stu-id="d1c59-649">Values</span></span>                         | <span data-ttu-id="d1c59-650">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1c59-650">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d1c59-651">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="d1c59-651">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="d1c59-652">Permissões desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="d1c59-652">Unknown permission.</span></span>
<span data-ttu-id="d1c59-653">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="d1c59-653">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="d1c59-654">Permissão para capturar o áudio.</span><span class="sxs-lookup"><span data-stu-id="d1c59-654">Permission to capture audio.</span></span>
<span data-ttu-id="d1c59-655">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="d1c59-655">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="d1c59-656">Permissão para capturar vídeo.</span><span class="sxs-lookup"><span data-stu-id="d1c59-656">Permission to capture video.</span></span>
<span data-ttu-id="d1c59-657">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="d1c59-657">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="d1c59-658">Permissão para acessar a localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="d1c59-658">Permission to access geolocation.</span></span>
<span data-ttu-id="d1c59-659">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="d1c59-659">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="d1c59-660">Permissão para enviar notificações da Web.</span><span class="sxs-lookup"><span data-stu-id="d1c59-660">Permission to send web notifications.</span></span>
<span data-ttu-id="d1c59-661">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="d1c59-661">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="d1c59-662">Permissão para acessar o sensor genérico.</span><span class="sxs-lookup"><span data-stu-id="d1c59-662">Permission to access generic sensor.</span></span>
<span data-ttu-id="d1c59-663">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="d1c59-663">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="d1c59-664">Permissão para ler a área de transferência do sistema sem um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="d1c59-664">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="d1c59-665">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="d1c59-665">CORE_WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="d1c59-666">Resposta a uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="d1c59-666">Response to a permission request.</span></span>

> <span data-ttu-id="d1c59-667">Enumeração [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="d1c59-667">enum [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span></span>

 <span data-ttu-id="d1c59-668">Valores</span><span class="sxs-lookup"><span data-stu-id="d1c59-668">Values</span></span>                         | <span data-ttu-id="d1c59-669">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1c59-669">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d1c59-670">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d1c59-670">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="d1c59-671">Use o comportamento padrão do navegador, que normalmente solicita aos usuários a decisão.</span><span class="sxs-lookup"><span data-stu-id="d1c59-671">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="d1c59-672">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="d1c59-672">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="d1c59-673">Conceder a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="d1c59-673">Grant the permission request.</span></span>
<span data-ttu-id="d1c59-674">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="d1c59-674">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="d1c59-675">Negue a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="d1c59-675">Deny the permission request.</span></span>

#### <span data-ttu-id="d1c59-676">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="d1c59-676">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="d1c59-677">Valores de status de erro para navegações na Web.</span><span class="sxs-lookup"><span data-stu-id="d1c59-677">Error status values for web navigations.</span></span>

> <span data-ttu-id="d1c59-678">Enumeração [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="d1c59-678">enum [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span></span>

 <span data-ttu-id="d1c59-679">Valores</span><span class="sxs-lookup"><span data-stu-id="d1c59-679">Values</span></span>                         | <span data-ttu-id="d1c59-680">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1c59-680">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d1c59-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="d1c59-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="d1c59-682">Ocorreu um erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d1c59-682">An unknown error occurred.</span></span>
<span data-ttu-id="d1c59-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="d1c59-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="d1c59-684">O nome comum do certificado SSL não corresponde ao endereço Web.</span><span class="sxs-lookup"><span data-stu-id="d1c59-684">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="d1c59-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="d1c59-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="d1c59-686">O certificado SSL venceu.</span><span class="sxs-lookup"><span data-stu-id="d1c59-686">The SSL certificate has expired.</span></span>
<span data-ttu-id="d1c59-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d1c59-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="d1c59-688">O certificado do cliente SSL contém erros.</span><span class="sxs-lookup"><span data-stu-id="d1c59-688">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="d1c59-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="d1c59-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="d1c59-690">A revogação do certificado SSL foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="d1c59-690">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="d1c59-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="d1c59-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="d1c59-692">O certificado SSL é inválido &ndash; isso significa que o certificado não correspondia aos pins da chave pública para o nome do host, o certificado é assinado por uma autoridade não confiável ou por meio de um algoritmo de sinal fraco, o certificado declarado pelos nomes DNS viola restrições de nome, o certificado contém uma chave fraca, o período de validade do certificado é muito longo, falta de informações sobre a revogação ou o mecanismo de revogação, o nome do host não exclusivo, a falta de informações [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)de transparência do certificado</span><span class="sxs-lookup"><span data-stu-id="d1c59-692">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="d1c59-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="d1c59-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="d1c59-694">Não é possível acessar o host.</span><span class="sxs-lookup"><span data-stu-id="d1c59-694">The host is unreachable.</span></span>
<span data-ttu-id="d1c59-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d1c59-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="d1c59-696">A conexão expirou.</span><span class="sxs-lookup"><span data-stu-id="d1c59-696">The connection has timed out.</span></span>
<span data-ttu-id="d1c59-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="d1c59-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="d1c59-698">O servidor retornou uma resposta inválida ou não reconhecida.</span><span class="sxs-lookup"><span data-stu-id="d1c59-698">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="d1c59-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="d1c59-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="d1c59-700">A conexão foi anulada.</span><span class="sxs-lookup"><span data-stu-id="d1c59-700">The connection was aborted.</span></span>
<span data-ttu-id="d1c59-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="d1c59-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="d1c59-702">A conexão foi redefinida.</span><span class="sxs-lookup"><span data-stu-id="d1c59-702">The connection was reset.</span></span>
<span data-ttu-id="d1c59-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="d1c59-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="d1c59-704">A conexão à Internet foi perdida.</span><span class="sxs-lookup"><span data-stu-id="d1c59-704">The Internet connection has been lost.</span></span>
<span data-ttu-id="d1c59-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="d1c59-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="d1c59-706">Não é possível se conectar ao destino.</span><span class="sxs-lookup"><span data-stu-id="d1c59-706">Cannot connect to destination.</span></span>
<span data-ttu-id="d1c59-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="d1c59-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="d1c59-708">Não foi possível resolver o nome de host fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1c59-708">Could not resolve provided host name.</span></span>
<span data-ttu-id="d1c59-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="d1c59-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="d1c59-710">A operação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="d1c59-710">The operation was canceled.</span></span>
<span data-ttu-id="d1c59-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="d1c59-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="d1c59-712">Falha no redirecionamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="d1c59-712">The request redirect failed.</span></span>
<span data-ttu-id="d1c59-713">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="d1c59-713">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="d1c59-714">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="d1c59-714">An unexpected error occurred.</span></span>

#### <span data-ttu-id="d1c59-715">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="d1c59-715">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="d1c59-716">Enumeração para contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="d1c59-716">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="d1c59-717">Enumeração [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="d1c59-717">enum [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span></span>

 <span data-ttu-id="d1c59-718">Valores</span><span class="sxs-lookup"><span data-stu-id="d1c59-718">Values</span></span>                         | <span data-ttu-id="d1c59-719">Descrições</span><span class="sxs-lookup"><span data-stu-id="d1c59-719">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d1c59-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="d1c59-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="d1c59-721">Todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="d1c59-721">All resources.</span></span>
<span data-ttu-id="d1c59-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="d1c59-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="d1c59-723">Recursos de documento.</span><span class="sxs-lookup"><span data-stu-id="d1c59-723">Document resources.</span></span>
<span data-ttu-id="d1c59-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="d1c59-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="d1c59-725">Recursos CSS.</span><span class="sxs-lookup"><span data-stu-id="d1c59-725">CSS resources.</span></span>
<span data-ttu-id="d1c59-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="d1c59-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="d1c59-727">Recursos de imagem.</span><span class="sxs-lookup"><span data-stu-id="d1c59-727">Image resources.</span></span>
<span data-ttu-id="d1c59-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="d1c59-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="d1c59-729">Outros recursos de mídia, como vídeos.</span><span class="sxs-lookup"><span data-stu-id="d1c59-729">Other media resources such as videos.</span></span>
<span data-ttu-id="d1c59-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="d1c59-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="d1c59-731">Recursos de fonte.</span><span class="sxs-lookup"><span data-stu-id="d1c59-731">Font resources.</span></span>
<span data-ttu-id="d1c59-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="d1c59-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="d1c59-733">Recursos de script.</span><span class="sxs-lookup"><span data-stu-id="d1c59-733">Script resources.</span></span>
<span data-ttu-id="d1c59-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="d1c59-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="d1c59-735">Solicitações HTTP XML.</span><span class="sxs-lookup"><span data-stu-id="d1c59-735">XML HTTP requests.</span></span>
<span data-ttu-id="d1c59-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="d1c59-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="d1c59-737">Busque a comunicação da API.</span><span class="sxs-lookup"><span data-stu-id="d1c59-737">Fetch API communication.</span></span>
<span data-ttu-id="d1c59-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="d1c59-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="d1c59-739">Recursos do texttrack.</span><span class="sxs-lookup"><span data-stu-id="d1c59-739">TextTrack resources.</span></span>
<span data-ttu-id="d1c59-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="d1c59-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="d1c59-741">Comunicação de API de EventSource.</span><span class="sxs-lookup"><span data-stu-id="d1c59-741">EventSource API communication.</span></span>
<span data-ttu-id="d1c59-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="d1c59-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="d1c59-743">Comunicação de API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="d1c59-743">WebSocket API communication.</span></span>
<span data-ttu-id="d1c59-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="d1c59-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="d1c59-745">Manifestos do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d1c59-745">Web App Manifests.</span></span>
<span data-ttu-id="d1c59-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="d1c59-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="d1c59-747">Trocas HTTP assinadas.</span><span class="sxs-lookup"><span data-stu-id="d1c59-747">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="d1c59-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="d1c59-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="d1c59-749">Solicitações de ping.</span><span class="sxs-lookup"><span data-stu-id="d1c59-749">Ping requests.</span></span>
<span data-ttu-id="d1c59-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="d1c59-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="d1c59-751">Relatórios de violação de CSP.</span><span class="sxs-lookup"><span data-stu-id="d1c59-751">CSP Violation Reports.</span></span>
<span data-ttu-id="d1c59-752">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="d1c59-752">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="d1c59-753">Outros recursos.</span><span class="sxs-lookup"><span data-stu-id="d1c59-753">Other resources.</span></span>
