---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2Settings
ms.openlocfilehash: 24a1e06be83fbb5c510c455e80c52b7165dabcde
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879587"
---
# <span data-ttu-id="5dafc-104">interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="5dafc-104">interface ICoreWebView2Settings</span></span> 

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="5dafc-105">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="5dafc-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5dafc-106">Summary</span></span>

 <span data-ttu-id="5dafc-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5dafc-107">Members</span></span>                        | <span data-ttu-id="5dafc-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5dafc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5dafc-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="5dafc-110">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="5dafc-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="5dafc-112">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="5dafc-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="5dafc-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="5dafc-114">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="5dafc-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="5dafc-115">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="5dafc-115">get_AreHostObjectsAllowed</span></span>](#get_arehostobjectsallowed) | <span data-ttu-id="5dafc-116">A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-116">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="5dafc-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="5dafc-118">A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="5dafc-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="5dafc-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="5dafc-120">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="5dafc-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="5dafc-122">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="5dafc-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="5dafc-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="5dafc-124">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="5dafc-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="5dafc-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="5dafc-126">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="5dafc-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="5dafc-128">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="5dafc-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="5dafc-130">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="5dafc-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="5dafc-132">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="5dafc-133">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="5dafc-133">put_AreHostObjectsAllowed</span></span>](#put_arehostobjectsallowed) | <span data-ttu-id="5dafc-134">Defina a propriedade AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="5dafc-134">Set the AreHostObjectsAllowed property.</span></span>
[<span data-ttu-id="5dafc-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="5dafc-136">Defina a propriedade IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="5dafc-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="5dafc-138">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="5dafc-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="5dafc-140">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="5dafc-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="5dafc-142">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="5dafc-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="5dafc-144">Defina a propriedade IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="5dafc-145">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="5dafc-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="5dafc-146">Parte</span><span class="sxs-lookup"><span data-stu-id="5dafc-146">Members</span></span>

#### <span data-ttu-id="5dafc-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="5dafc-148">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="5dafc-149">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="5dafc-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="5dafc-150">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="5dafc-150">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="5dafc-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="5dafc-152">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="5dafc-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="5dafc-153">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="5dafc-154">Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload).</span><span class="sxs-lookup"><span data-stu-id="5dafc-154">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="5dafc-155">Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="5dafc-155">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="5dafc-156">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-156">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="5dafc-157">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="5dafc-157">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="5dafc-158">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)público HRESULT (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-158">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="5dafc-159">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="5dafc-159">It is true by default.</span></span>

#### <span data-ttu-id="5dafc-160">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="5dafc-160">get_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="5dafc-161">A propriedade AreHostObjectsAllowed é usada para controlar se os objetos de host são acessíveis a partir da página em WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-161">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="5dafc-162">[get_AreHostObjectsAllowed](#get_arehostobjectsallowed)público HRESULT (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="5dafc-162">public HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="5dafc-163">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="5dafc-163">Defaults to TRUE.</span></span>

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="5dafc-164">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-164">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="5dafc-165">A propriedade IsBuiltInErrorPageEnabled é usada para desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="5dafc-165">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="5dafc-166">[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="5dafc-166">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="5dafc-167">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="5dafc-167">Defaults to TRUE.</span></span> <span data-ttu-id="5dafc-168">Quando desativado, a página em branco será mostrada quando ocorrer um erro relacionado.</span><span class="sxs-lookup"><span data-stu-id="5dafc-168">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="5dafc-169">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-169">get_IsScriptEnabled</span></span> 

<span data-ttu-id="5dafc-170">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-170">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="5dafc-171">[get_IsScriptEnabled](#get_isscriptenabled)público HRESULT (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-171">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="5dafc-172">Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5dafc-172">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="5dafc-173">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="5dafc-173">It is true by default.</span></span>

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

#### <span data-ttu-id="5dafc-174">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-174">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="5dafc-175">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="5dafc-175">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="5dafc-176">[get_IsStatusBarEnabled](#get_isstatusbarenabled)público HRESULT (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-176">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="5dafc-177">A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações.</span><span class="sxs-lookup"><span data-stu-id="5dafc-177">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="5dafc-178">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="5dafc-178">It is true by default.</span></span>

#### <span data-ttu-id="5dafc-179">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-179">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="5dafc-180">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="5dafc-180">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="5dafc-181">[get_IsWebMessageEnabled](#get_iswebmessageenabled)público HRESULT (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-181">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="5dafc-182">Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="5dafc-182">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="5dafc-183">A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="5dafc-183">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="5dafc-184">Se definido como false, a comunicação não será permitida.</span><span class="sxs-lookup"><span data-stu-id="5dafc-184">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="5dafc-185">PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="5dafc-185">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="5dafc-186">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="5dafc-186">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="5dafc-187">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-187">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="5dafc-188">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="5dafc-188">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="5dafc-189">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="5dafc-189">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="5dafc-190">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="5dafc-190">Defaults to TRUE.</span></span> <span data-ttu-id="5dafc-191">Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido por meio da API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="5dafc-191">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="5dafc-192">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-192">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="5dafc-193">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-193">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="5dafc-194">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="5dafc-194">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="5dafc-195">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-195">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="5dafc-196">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-196">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="5dafc-197">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-197">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="5dafc-198">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-198">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="5dafc-199">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-199">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="5dafc-200">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)público HRESULT (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-200">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="5dafc-201">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="5dafc-201">put_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="5dafc-202">Defina a propriedade AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="5dafc-202">Set the AreHostObjectsAllowed property.</span></span>

> <span data-ttu-id="5dafc-203">[put_AreHostObjectsAllowed](#put_arehostobjectsallowed)público HRESULT (bool permitido)</span><span class="sxs-lookup"><span data-stu-id="5dafc-203">public HRESULT [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="5dafc-204">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-204">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="5dafc-205">Defina a propriedade IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-205">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="5dafc-206">[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="5dafc-206">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="5dafc-207">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-207">put_IsScriptEnabled</span></span> 

<span data-ttu-id="5dafc-208">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-208">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="5dafc-209">[put_IsScriptEnabled](#put_isscriptenabled)público HRESULT (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-209">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="5dafc-210">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-210">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="5dafc-211">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-211">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="5dafc-212">[put_IsStatusBarEnabled](#put_isstatusbarenabled)público HRESULT (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-212">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="5dafc-213">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-213">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="5dafc-214">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-214">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="5dafc-215">[put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="5dafc-215">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="5dafc-216">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="5dafc-216">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="5dafc-217">Defina a propriedade IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="5dafc-217">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="5dafc-218">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="5dafc-218">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

