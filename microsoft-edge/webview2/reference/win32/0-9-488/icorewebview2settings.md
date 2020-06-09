---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: a3364d8836a44966063002820ef30b14014a503f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698145"
---
# <span data-ttu-id="bce0a-104">interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="bce0a-104">interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="bce0a-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="bce0a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="bce0a-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="bce0a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="bce0a-107">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="bce0a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="bce0a-108">Summary</span></span>

 <span data-ttu-id="bce0a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bce0a-109">Members</span></span>                        | <span data-ttu-id="bce0a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="bce0a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bce0a-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="bce0a-112">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="bce0a-113">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-113">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="bce0a-114">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="bce0a-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="bce0a-115">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-115">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="bce0a-116">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="bce0a-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="bce0a-117">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="bce0a-117">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="bce0a-118">A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-118">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="bce0a-119">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-119">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="bce0a-120">A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="bce0a-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="bce0a-121">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-121">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="bce0a-122">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="bce0a-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="bce0a-124">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="bce0a-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="bce0a-125">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-125">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="bce0a-126">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="bce0a-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="bce0a-127">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-127">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="bce0a-128">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="bce0a-129">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-129">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="bce0a-130">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-130">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="bce0a-131">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-131">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="bce0a-132">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-132">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="bce0a-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="bce0a-134">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-134">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="bce0a-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="bce0a-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="bce0a-136">Defina a propriedade AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="bce0a-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="bce0a-137">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-137">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="bce0a-138">Defina a propriedade IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-138">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="bce0a-139">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-139">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="bce0a-140">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-140">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="bce0a-141">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-141">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="bce0a-142">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-142">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="bce0a-143">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-143">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="bce0a-144">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-144">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="bce0a-145">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-145">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="bce0a-146">Defina a propriedade IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-146">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="bce0a-147">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="bce0a-147">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="bce0a-148">Parte</span><span class="sxs-lookup"><span data-stu-id="bce0a-148">Members</span></span>

#### <span data-ttu-id="bce0a-149">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-149">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="bce0a-150">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-150">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="bce0a-151">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="bce0a-151">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="bce0a-152">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="bce0a-152">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="bce0a-153">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-153">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="bce0a-154">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="bce0a-154">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="bce0a-155">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-155">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="bce0a-156">Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload).</span><span class="sxs-lookup"><span data-stu-id="bce0a-156">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="bce0a-157">Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="bce0a-157">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="bce0a-158">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-158">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="bce0a-159">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="bce0a-159">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="bce0a-160">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)público HRESULT (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-160">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="bce0a-161">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="bce0a-161">It is true by default.</span></span>

#### <span data-ttu-id="bce0a-162">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="bce0a-162">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="bce0a-163">A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-163">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="bce0a-164">[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)público HRESULT (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="bce0a-164">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="bce0a-165">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="bce0a-165">Defaults to TRUE.</span></span>

```cpp
            BOOL allowRemoteObjects;
            CHECK_FAILURE(m_settings->get_AreRemoteObjectsAllowed(&allowRemoteObjects));
            if (allowRemoteObjects)
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to remote objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to remote objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="bce0a-166">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-166">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="bce0a-167">A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="bce0a-167">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="bce0a-168">[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="bce0a-168">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="bce0a-169">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="bce0a-169">Defaults to TRUE.</span></span> <span data-ttu-id="bce0a-170">Quando desativado, a página em branco será mostrada quando ocorrer um erro relacionado.</span><span class="sxs-lookup"><span data-stu-id="bce0a-170">When disabled, blank page will be shown when related error happens.</span></span>

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="bce0a-171">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-171">get_IsScriptEnabled</span></span> 

<span data-ttu-id="bce0a-172">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-172">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="bce0a-173">[get_IsScriptEnabled](#get_isscriptenabled)público HRESULT (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-173">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="bce0a-174">Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="bce0a-174">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="bce0a-175">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="bce0a-175">It is true by default.</span></span>

```cpp
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
```

#### <span data-ttu-id="bce0a-176">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-176">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="bce0a-177">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="bce0a-177">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="bce0a-178">[get_IsStatusBarEnabled](#get_isstatusbarenabled)público HRESULT (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-178">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="bce0a-179">A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações.</span><span class="sxs-lookup"><span data-stu-id="bce0a-179">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="bce0a-180">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="bce0a-180">It is true by default.</span></span>

#### <span data-ttu-id="bce0a-181">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-181">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="bce0a-182">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="bce0a-182">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="bce0a-183">[get_IsWebMessageEnabled](#get_iswebmessageenabled)público HRESULT (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-183">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="bce0a-184">Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="bce0a-184">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="bce0a-185">A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="bce0a-185">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="bce0a-186">Se definido como false, a comunicação não será permitida.</span><span class="sxs-lookup"><span data-stu-id="bce0a-186">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="bce0a-187">PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="bce0a-187">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="bce0a-188">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="bce0a-188">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="bce0a-189">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-189">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="bce0a-190">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="bce0a-190">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="bce0a-191">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="bce0a-191">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="bce0a-192">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="bce0a-192">Defaults to TRUE.</span></span> <span data-ttu-id="bce0a-193">Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido por meio da API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="bce0a-193">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="bce0a-194">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-194">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="bce0a-195">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-195">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="bce0a-196">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="bce0a-196">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="bce0a-197">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-197">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="bce0a-198">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-198">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="bce0a-199">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-199">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="bce0a-200">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-200">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="bce0a-201">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-201">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="bce0a-202">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)público HRESULT (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-202">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="bce0a-203">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="bce0a-203">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="bce0a-204">Defina a propriedade AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="bce0a-204">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="bce0a-205">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)público HRESULT (bool permitido)</span><span class="sxs-lookup"><span data-stu-id="bce0a-205">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="bce0a-206">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-206">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="bce0a-207">Defina a propriedade IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-207">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="bce0a-208">[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="bce0a-208">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="bce0a-209">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-209">put_IsScriptEnabled</span></span> 

<span data-ttu-id="bce0a-210">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-210">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="bce0a-211">[put_IsScriptEnabled](#put_isscriptenabled)público HRESULT (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-211">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="bce0a-212">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-212">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="bce0a-213">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-213">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="bce0a-214">[put_IsStatusBarEnabled](#put_isstatusbarenabled)público HRESULT (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-214">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="bce0a-215">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-215">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="bce0a-216">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-216">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="bce0a-217">[put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="bce0a-217">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="bce0a-218">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="bce0a-218">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="bce0a-219">Defina a propriedade IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="bce0a-219">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="bce0a-220">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="bce0a-220">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

