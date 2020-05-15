---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 79f6e2712cab6d18025bd49ab0e7ceba01495d65
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652736"
---
# <span data-ttu-id="64abc-104">interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="64abc-104">interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="64abc-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="64abc-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="64abc-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="64abc-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="64abc-107">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="64abc-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="64abc-108">Summary</span></span>

 <span data-ttu-id="64abc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="64abc-109">Members</span></span>                        | <span data-ttu-id="64abc-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="64abc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64abc-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="64abc-112">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="64abc-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="64abc-114">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="64abc-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="64abc-116">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="64abc-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="64abc-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="64abc-118">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="64abc-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="64abc-120">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="64abc-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="64abc-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="64abc-122">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="64abc-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="64abc-124">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="64abc-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="64abc-125">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-125">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="64abc-126">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-126">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="64abc-127">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-127">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="64abc-128">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="64abc-128">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="64abc-129">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-129">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="64abc-130">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-130">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="64abc-131">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-131">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="64abc-132">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="64abc-133">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-133">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="64abc-134">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-134">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="64abc-135">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="64abc-135">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="64abc-136">A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos remotos podem ser acessados na página do WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-136">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="64abc-137">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="64abc-137">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="64abc-138">Defina a propriedade AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="64abc-138">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="64abc-139">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-139">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="64abc-140">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-140">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="64abc-141">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-141">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="64abc-142">Defina a propriedade IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-142">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="64abc-143">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="64abc-143">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="64abc-144">Parte</span><span class="sxs-lookup"><span data-stu-id="64abc-144">Members</span></span>

#### <span data-ttu-id="64abc-145">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-145">get_IsScriptEnabled</span></span> 

<span data-ttu-id="64abc-146">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-146">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="64abc-147">[get_IsScriptEnabled](#get_isscriptenabled)público HRESULT (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-147">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="64abc-148">Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="64abc-148">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="64abc-149">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="64abc-149">It is true by default.</span></span>

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

#### <span data-ttu-id="64abc-150">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-150">put_IsScriptEnabled</span></span> 

<span data-ttu-id="64abc-151">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-151">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="64abc-152">[put_IsScriptEnabled](#put_isscriptenabled)público HRESULT (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-152">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="64abc-153">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-153">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="64abc-154">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="64abc-154">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="64abc-155">[get_IsWebMessageEnabled](#get_iswebmessageenabled)público HRESULT (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-155">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="64abc-156">Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="64abc-156">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="64abc-157">A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="64abc-157">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="64abc-158">Se definido como false, a comunicação não será permitida.</span><span class="sxs-lookup"><span data-stu-id="64abc-158">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="64abc-159">PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="64abc-159">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="64abc-160">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="64abc-160">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="64abc-161">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-161">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="64abc-162">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-162">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="64abc-163">[put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-163">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="64abc-164">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-164">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="64abc-165">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="64abc-165">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="64abc-166">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-166">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="64abc-167">Se definido como false, o WebView não renderizará a caixa de diálogo JavaScript padrão (especificamente as mostradas pelo alerta de JavaScript, confirme, funções de prompt e evento beforeunload).</span><span class="sxs-lookup"><span data-stu-id="64abc-167">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="64abc-168">Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="64abc-168">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="64abc-169">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-169">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="64abc-170">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-170">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="64abc-171">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-171">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="64abc-172">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-172">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="64abc-173">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="64abc-173">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="64abc-174">[get_IsStatusBarEnabled](#get_isstatusbarenabled)público HRESULT (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-174">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="64abc-175">A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações.</span><span class="sxs-lookup"><span data-stu-id="64abc-175">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="64abc-176">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="64abc-176">It is true by default.</span></span>

#### <span data-ttu-id="64abc-177">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-177">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="64abc-178">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-178">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="64abc-179">[put_IsStatusBarEnabled](#put_isstatusbarenabled)público HRESULT (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-179">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="64abc-180">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-180">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="64abc-181">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="64abc-181">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="64abc-182">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)público HRESULT (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-182">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="64abc-183">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="64abc-183">It is true by default.</span></span>

#### <span data-ttu-id="64abc-184">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-184">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="64abc-185">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-185">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="64abc-186">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)público HRESULT (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="64abc-186">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="64abc-187">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-187">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="64abc-188">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-188">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="64abc-189">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="64abc-189">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="64abc-190">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="64abc-190">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="64abc-191">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-191">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="64abc-192">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-192">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="64abc-193">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="64abc-193">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="64abc-194">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="64abc-194">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="64abc-195">A propriedade AreRemoteObjectsAllowed é usada para controlar se os objetos remotos podem ser acessados na página do WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-195">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="64abc-196">[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)público HRESULT (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="64abc-196">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="64abc-197">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="64abc-197">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="64abc-198">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="64abc-198">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="64abc-199">Defina a propriedade AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="64abc-199">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="64abc-200">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)público HRESULT (bool permitido)</span><span class="sxs-lookup"><span data-stu-id="64abc-200">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="64abc-201">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-201">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="64abc-202">A propriedade IsZoomControlEnabled é usada para impedir que o usuário afete o zoom da WebView.</span><span class="sxs-lookup"><span data-stu-id="64abc-202">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="64abc-203">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="64abc-203">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="64abc-204">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="64abc-204">Defaults to TRUE.</span></span> <span data-ttu-id="64abc-205">Quando desabilitado, o usuário não poderá aplicar zoom usando Ctrl +/ou CTRL + mouse wheel, mas o zoom poderá ser definido via API put_ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="64abc-205">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

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

#### <span data-ttu-id="64abc-206">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="64abc-206">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="64abc-207">Defina a propriedade IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="64abc-207">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="64abc-208">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="64abc-208">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

