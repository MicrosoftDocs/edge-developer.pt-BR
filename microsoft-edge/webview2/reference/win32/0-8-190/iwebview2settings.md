---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 649506b28e0ecdbff33b44bbd8010ddb3d2a66b0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885797"
---
# <span data-ttu-id="48c0d-104">0.8.355-IWebView2Settings de interface</span><span class="sxs-lookup"><span data-stu-id="48c0d-104">0.8.355 - interface IWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="48c0d-105">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="48c0d-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="48c0d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="48c0d-106">Summary</span></span>

 <span data-ttu-id="48c0d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="48c0d-107">Members</span></span>                        | <span data-ttu-id="48c0d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="48c0d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="48c0d-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="48c0d-110">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="48c0d-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="48c0d-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="48c0d-112">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="48c0d-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="48c0d-114">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="48c0d-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="48c0d-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="48c0d-116">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="48c0d-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="48c0d-118">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="48c0d-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="48c0d-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="48c0d-120">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="48c0d-121">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="48c0d-121">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="48c0d-122">Essa configuração é preterida e sempre retornará false.</span><span class="sxs-lookup"><span data-stu-id="48c0d-122">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="48c0d-123">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="48c0d-123">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="48c0d-124">Essa configuração é preterida e não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="48c0d-124">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="48c0d-125">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-125">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="48c0d-126">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="48c0d-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="48c0d-127">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-127">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="48c0d-128">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-128">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="48c0d-129">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-129">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="48c0d-130">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="48c0d-130">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="48c0d-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="48c0d-132">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-132">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="48c0d-133">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="48c0d-133">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="48c0d-134">Parte</span><span class="sxs-lookup"><span data-stu-id="48c0d-134">Members</span></span>

#### <span data-ttu-id="48c0d-135">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-135">get_IsScriptEnabled</span></span> 

<span data-ttu-id="48c0d-136">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="48c0d-136">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="48c0d-137">[get_IsScriptEnabled](#get_isscriptenabled)público HRESULT (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-137">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="48c0d-138">Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48c0d-138">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="48c0d-139">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="48c0d-139">It is true by default.</span></span>

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

#### <span data-ttu-id="48c0d-140">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-140">put_IsScriptEnabled</span></span> 

<span data-ttu-id="48c0d-141">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-141">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="48c0d-142">[put_IsScriptEnabled](#put_isscriptenabled)público HRESULT (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-142">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="48c0d-143">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-143">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="48c0d-144">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="48c0d-144">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="48c0d-145">[get_IsWebMessageEnabled](#get_iswebmessageenabled)público HRESULT (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-145">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="48c0d-146">Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="48c0d-146">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="48c0d-147">A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="48c0d-147">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="48c0d-148">Se definido como false, a comunicação não será permitida.</span><span class="sxs-lookup"><span data-stu-id="48c0d-148">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="48c0d-149">PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="48c0d-149">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="48c0d-150">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="48c0d-150">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="48c0d-151">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-151">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="48c0d-152">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-152">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="48c0d-153">[put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-153">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="48c0d-154">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-154">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="48c0d-155">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="48c0d-155">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="48c0d-156">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-156">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="48c0d-157">Se definido como false, o WebView não renderizará a caixa de diálogo padrão do JavaScript (especificamente as mostradas pelas funções de alerta, confirmação e prompt do JavaScript).</span><span class="sxs-lookup"><span data-stu-id="48c0d-157">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="48c0d-158">Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="48c0d-158">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="48c0d-159">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-159">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="48c0d-160">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-160">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="48c0d-161">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-161">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="48c0d-162">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="48c0d-162">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="48c0d-163">Essa configuração é preterida e sempre retornará false.</span><span class="sxs-lookup"><span data-stu-id="48c0d-163">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="48c0d-164">[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)público HRESULT (bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="48c0d-164">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="48c0d-165">Isso significa que os elementos da WebView só preencherão os limites da WebView.</span><span class="sxs-lookup"><span data-stu-id="48c0d-165">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="48c0d-166">Essa propriedade será completamente removida.</span><span class="sxs-lookup"><span data-stu-id="48c0d-166">This property will then be completely removed.</span></span> <span data-ttu-id="48c0d-167">Em vez disso, ouça o evento ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="48c0d-167">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="48c0d-168">Controla se o fullscreen é permitido para os elementos no WebView.</span><span class="sxs-lookup"><span data-stu-id="48c0d-168">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="48c0d-169">Quando é permitido, o conteúdo da Web, como um elemento de vídeo na WebView, pode ser exibido em tela cheia.</span><span class="sxs-lookup"><span data-stu-id="48c0d-169">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="48c0d-170">Quando não for permitido, o elemento preencherá os limites da WebView quando o elemento exigir a tela inteira.</span><span class="sxs-lookup"><span data-stu-id="48c0d-170">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="48c0d-171">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="48c0d-171">It is true by default.</span></span>

#### <span data-ttu-id="48c0d-172">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="48c0d-172">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="48c0d-173">Essa configuração é preterida e não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="48c0d-173">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="48c0d-174">[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)público HRESULT (bool IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="48c0d-174">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="48c0d-175">Em vez disso, ouça o evento ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="48c0d-175">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="48c0d-176">Defina a propriedade IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="48c0d-176">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="48c0d-177">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-177">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="48c0d-178">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="48c0d-178">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="48c0d-179">[get_IsStatusBarEnabled](#get_isstatusbarenabled)público HRESULT (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-179">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="48c0d-180">A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações.</span><span class="sxs-lookup"><span data-stu-id="48c0d-180">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="48c0d-181">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="48c0d-181">It is true by default.</span></span>

#### <span data-ttu-id="48c0d-182">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-182">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="48c0d-183">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-183">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="48c0d-184">[put_IsStatusBarEnabled](#put_isstatusbarenabled)público HRESULT (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-184">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="48c0d-185">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-185">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="48c0d-186">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="48c0d-186">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="48c0d-187">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)público HRESULT (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-187">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="48c0d-188">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="48c0d-188">It is true by default.</span></span>

#### <span data-ttu-id="48c0d-189">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="48c0d-189">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="48c0d-190">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="48c0d-190">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="48c0d-191">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)público HRESULT (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="48c0d-191">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

