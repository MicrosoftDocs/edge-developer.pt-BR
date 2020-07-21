---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 70ccef9e99b3649ceca49b736570ba416cf73ebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883977"
---
# <span data-ttu-id="030e3-104">0.9.430-ICoreWebView2Settings de interface</span><span class="sxs-lookup"><span data-stu-id="030e3-104">0.9.430 - interface ICoreWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="030e3-105">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="030e3-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="030e3-106">Summary</span></span>

 <span data-ttu-id="030e3-107">Parte</span><span class="sxs-lookup"><span data-stu-id="030e3-107">Members</span></span>                        | <span data-ttu-id="030e3-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="030e3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="030e3-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="030e3-110">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="030e3-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="030e3-112">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="030e3-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="030e3-114">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="030e3-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="030e3-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="030e3-116">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="030e3-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="030e3-118">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="030e3-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="030e3-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="030e3-120">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="030e3-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="030e3-122">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="030e3-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="030e3-123">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-123">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="030e3-124">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-124">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="030e3-125">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-125">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="030e3-126">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="030e3-126">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="030e3-127">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-127">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="030e3-128">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-128">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="030e3-129">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-129">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="030e3-130">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-130">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="030e3-131">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-131">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="030e3-132">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-132">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="030e3-133">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="030e3-133">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="030e3-134">A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos remotos podem ser acessados na página do WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-134">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="030e3-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="030e3-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="030e3-136">Defina a propriedade AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="030e3-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="030e3-137">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-137">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="030e3-138">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-138">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="030e3-139">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-139">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="030e3-140">Defina a propriedade IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-140">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="030e3-141">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="030e3-141">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="030e3-142">Parte</span><span class="sxs-lookup"><span data-stu-id="030e3-142">Members</span></span>

#### <span data-ttu-id="030e3-143">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-143">get_IsScriptEnabled</span></span> 

<span data-ttu-id="030e3-144">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-144">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="030e3-145">[get_IsScriptEnabled](#get_isscriptenabled)público HRESULT (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-145">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="030e3-146">Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="030e3-146">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="030e3-147">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="030e3-147">It is true by default.</span></span>

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

#### <span data-ttu-id="030e3-148">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-148">put_IsScriptEnabled</span></span> 

<span data-ttu-id="030e3-149">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-149">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="030e3-150">[put_IsScriptEnabled](#put_isscriptenabled)público HRESULT (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-150">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="030e3-151">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-151">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="030e3-152">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="030e3-152">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="030e3-153">[get_IsWebMessageEnabled](#get_iswebmessageenabled)público HRESULT (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-153">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="030e3-154">Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="030e3-154">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="030e3-155">A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="030e3-155">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="030e3-156">Se definido como false, a comunicação não será permitida.</span><span class="sxs-lookup"><span data-stu-id="030e3-156">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="030e3-157">PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="030e3-157">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="030e3-158">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="030e3-158">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="030e3-159">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-159">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="030e3-160">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-160">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="030e3-161">[put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-161">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="030e3-162">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-162">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="030e3-163">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="030e3-163">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="030e3-164">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-164">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="030e3-165">Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload).</span><span class="sxs-lookup"><span data-stu-id="030e3-165">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="030e3-166">Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="030e3-166">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="030e3-167">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-167">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="030e3-168">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-168">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="030e3-169">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-169">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="030e3-170">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-170">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="030e3-171">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="030e3-171">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="030e3-172">[get_IsStatusBarEnabled](#get_isstatusbarenabled)público HRESULT (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-172">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="030e3-173">A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações.</span><span class="sxs-lookup"><span data-stu-id="030e3-173">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="030e3-174">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="030e3-174">It is true by default.</span></span>

#### <span data-ttu-id="030e3-175">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-175">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="030e3-176">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-176">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="030e3-177">[put_IsStatusBarEnabled](#put_isstatusbarenabled)público HRESULT (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-177">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="030e3-178">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-178">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="030e3-179">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="030e3-179">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="030e3-180">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)público HRESULT (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-180">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="030e3-181">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="030e3-181">It is true by default.</span></span>

#### <span data-ttu-id="030e3-182">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-182">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="030e3-183">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-183">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="030e3-184">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)público HRESULT (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="030e3-184">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="030e3-185">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-185">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="030e3-186">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-186">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="030e3-187">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="030e3-187">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="030e3-188">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="030e3-188">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="030e3-189">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-189">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="030e3-190">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-190">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="030e3-191">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="030e3-191">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="030e3-192">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="030e3-192">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="030e3-193">A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos remotos podem ser acessados na página do WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-193">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="030e3-194">[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)público HRESULT (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="030e3-194">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="030e3-195">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="030e3-195">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="030e3-196">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="030e3-196">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="030e3-197">Defina a propriedade AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="030e3-197">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="030e3-198">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)público HRESULT (bool permitido)</span><span class="sxs-lookup"><span data-stu-id="030e3-198">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="030e3-199">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-199">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="030e3-200">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="030e3-200">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="030e3-201">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="030e3-201">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="030e3-202">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="030e3-202">Defaults to TRUE.</span></span> <span data-ttu-id="030e3-203">Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido via API put_ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="030e3-203">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control is disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control is enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="030e3-204">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="030e3-204">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="030e3-205">Defina a propriedade IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="030e3-205">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="030e3-206">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="030e3-206">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

