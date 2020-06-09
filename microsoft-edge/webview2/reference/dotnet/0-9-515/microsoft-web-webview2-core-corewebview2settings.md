---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: f0ac0bf7ae3b237bca45b22ed97ec16513666922
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697550"
---
# <span data-ttu-id="fbe4d-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="fbe4d-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

> [!NOTE]
> <span data-ttu-id="fbe4d-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="fbe4d-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="fbe4d-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fbe4d-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fbe4d-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="fbe4d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fbe4d-109">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-109">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="fbe4d-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="fbe4d-110">Summary</span></span>

 <span data-ttu-id="fbe4d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="fbe4d-111">Members</span></span>                        | <span data-ttu-id="fbe4d-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="fbe4d-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fbe4d-113">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-113">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="fbe4d-114">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-114">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="fbe4d-115">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-115">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="fbe4d-116">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-116">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="fbe4d-117">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-117">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="fbe4d-118">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-118">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="fbe4d-119">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="fbe4d-119">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="fbe4d-120">A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-120">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="fbe4d-121">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-121">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="fbe4d-122">A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-122">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="fbe4d-123">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-123">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="fbe4d-124">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-124">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="fbe4d-125">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-125">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="fbe4d-126">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="fbe4d-127">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-127">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="fbe4d-128">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-128">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="fbe4d-129">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-129">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="fbe4d-130">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-130">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="fbe4d-131">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-131">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="fbe4d-132">Parte</span><span class="sxs-lookup"><span data-stu-id="fbe4d-132">Members</span></span>

#### <span data-ttu-id="fbe4d-133">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-133">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="fbe4d-134">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-134">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="fbe4d-135">Public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-135">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="fbe4d-136">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-136">Defaults to TRUE.</span></span>

#### <span data-ttu-id="fbe4d-137">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-137">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="fbe4d-138">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-138">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="fbe4d-139">Public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-139">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="fbe4d-140">Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload).</span><span class="sxs-lookup"><span data-stu-id="fbe4d-140">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="fbe4d-141">Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-141">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="fbe4d-142">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-142">AreDevToolsEnabled</span></span> 

<span data-ttu-id="fbe4d-143">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-143">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="fbe4d-144">Public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-144">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="fbe4d-145">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-145">It is true by default.</span></span>

#### <span data-ttu-id="fbe4d-146">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="fbe4d-146">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="fbe4d-147">A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-147">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="fbe4d-148">Public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-148">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="fbe4d-149">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-149">Defaults to TRUE.</span></span>

#### <span data-ttu-id="fbe4d-150">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-150">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="fbe4d-151">A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-151">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="fbe4d-152">Public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-152">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="fbe4d-153">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-153">Defaults to TRUE.</span></span> <span data-ttu-id="fbe4d-154">Quando desativado, a página em branco será mostrada quando ocorrer um erro relacionado.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-154">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="fbe4d-155">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-155">IsScriptEnabled</span></span> 

<span data-ttu-id="fbe4d-156">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-156">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="fbe4d-157">Public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-157">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="fbe4d-158">Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-158">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="fbe4d-159">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-159">It is true by default.</span></span>

#### <span data-ttu-id="fbe4d-160">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-160">IsStatusBarEnabled</span></span> 

<span data-ttu-id="fbe4d-161">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-161">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="fbe4d-162">Public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-162">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="fbe4d-163">A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-163">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="fbe4d-164">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-164">It is true by default.</span></span>

#### <span data-ttu-id="fbe4d-165">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-165">IsWebMessageEnabled</span></span> 

<span data-ttu-id="fbe4d-166">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-166">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="fbe4d-167">Public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-167">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="fbe4d-168">Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="fbe4d-168">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="fbe4d-169">A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="fbe4d-169">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="fbe4d-170">Se definido como false, a comunicação não será permitida.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-170">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="fbe4d-171">PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-171">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="fbe4d-172">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-172">It is true by default.</span></span>

#### <span data-ttu-id="fbe4d-173">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="fbe4d-173">IsZoomControlEnabled</span></span> 

<span data-ttu-id="fbe4d-174">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-174">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="fbe4d-175">Public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="fbe4d-175">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="fbe4d-176">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-176">Defaults to TRUE.</span></span> <span data-ttu-id="fbe4d-177">Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido por meio da API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-177">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

