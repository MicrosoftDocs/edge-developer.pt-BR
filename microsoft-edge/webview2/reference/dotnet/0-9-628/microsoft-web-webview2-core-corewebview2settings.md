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
# <span data-ttu-id="cef2b-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="cef2b-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="cef2b-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cef2b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cef2b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="cef2b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cef2b-107">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="cef2b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="cef2b-108">Summary</span></span>

 <span data-ttu-id="cef2b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="cef2b-109">Members</span></span>                        | <span data-ttu-id="cef2b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="cef2b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cef2b-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="cef2b-112">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>
[<span data-ttu-id="cef2b-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="cef2b-114">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="cef2b-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="cef2b-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="cef2b-116">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="cef2b-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="cef2b-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="cef2b-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="cef2b-118">A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>
[<span data-ttu-id="cef2b-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="cef2b-120">A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="cef2b-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="cef2b-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="cef2b-122">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="cef2b-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="cef2b-124">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="cef2b-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="cef2b-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="cef2b-126">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="cef2b-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="cef2b-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="cef2b-128">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="cef2b-129">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="cef2b-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="cef2b-130">Parte</span><span class="sxs-lookup"><span data-stu-id="cef2b-130">Members</span></span>

#### <span data-ttu-id="cef2b-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="cef2b-132">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>

> <span data-ttu-id="cef2b-133">Public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="cef2b-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="cef2b-134">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-134">It is true by default.</span></span>

#### <span data-ttu-id="cef2b-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="cef2b-136">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="cef2b-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="cef2b-137">Public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="cef2b-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="cef2b-138">Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload).</span><span class="sxs-lookup"><span data-stu-id="cef2b-138">If set to false, then WebView won't render the default JavaScript dialog box (Specifically those shown by the JavaScript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="cef2b-139">Se definido como true, um também poderá se inscrever para o evento ScriptDialogOpening que conterá todas as informações da caixa de diálogo e permitir que o aplicativo host mostre sua própria interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="cef2b-139">If set to true, one can also subscribe to ScriptDialogOpening event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span> <span data-ttu-id="cef2b-140">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-140">It is true by default.</span></span>

#### <span data-ttu-id="cef2b-141">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-141">AreDevToolsEnabled</span></span> 

<span data-ttu-id="cef2b-142">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="cef2b-142">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="cef2b-143">Public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="cef2b-143">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="cef2b-144">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-144">It is true by default.</span></span>

#### <span data-ttu-id="cef2b-145">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="cef2b-145">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="cef2b-146">A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-146">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>

> <span data-ttu-id="cef2b-147">Public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="cef2b-147">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="cef2b-148">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-148">It is true by default.</span></span>

#### <span data-ttu-id="cef2b-149">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-149">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="cef2b-150">A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="cef2b-150">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="cef2b-151">Public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="cef2b-151">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="cef2b-152">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-152">It is true by default.</span></span> <span data-ttu-id="cef2b-153">Quando desativado, a página em branco será mostrada quando ocorrer um erro relacionado.</span><span class="sxs-lookup"><span data-stu-id="cef2b-153">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="cef2b-154">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-154">IsScriptEnabled</span></span> 

<span data-ttu-id="cef2b-155">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-155">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="cef2b-156">Public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="cef2b-156">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="cef2b-157">Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="cef2b-157">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="cef2b-158">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-158">It is true by default.</span></span>

#### <span data-ttu-id="cef2b-159">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-159">IsStatusBarEnabled</span></span> 

<span data-ttu-id="cef2b-160">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="cef2b-160">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="cef2b-161">Public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="cef2b-161">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="cef2b-162">A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações.</span><span class="sxs-lookup"><span data-stu-id="cef2b-162">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="cef2b-163">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-163">It is true by default.</span></span>

#### <span data-ttu-id="cef2b-164">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-164">IsWebMessageEnabled</span></span> 

<span data-ttu-id="cef2b-165">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="cef2b-165">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="cef2b-166">Public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="cef2b-166">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="cef2b-167">Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="cef2b-167">If set to true, communication from the host to the WebView's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="cef2b-168">A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de mensagem de automensagem do Window. Chrome. WebView e do evento WebMessageReceived (consulte a documentação do WebMessageReceived para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="cef2b-168">Communication from the WebView's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the WebMessageReceived event (see WebMessageReceived documentation for details).</span></span> <span data-ttu-id="cef2b-169">Se definido como false, a comunicação não será permitida.</span><span class="sxs-lookup"><span data-stu-id="cef2b-169">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="cef2b-170">PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="cef2b-170">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="cef2b-171">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-171">It is true by default.</span></span>

#### <span data-ttu-id="cef2b-172">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="cef2b-172">IsZoomControlEnabled</span></span> 

<span data-ttu-id="cef2b-173">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="cef2b-173">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="cef2b-174">Public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="cef2b-174">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="cef2b-175">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="cef2b-175">It is true by default.</span></span> <span data-ttu-id="cef2b-176">Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido por meio da API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="cef2b-176">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

