---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 94c6d6c424d715d3b6b57b366b71cf8e5fb8ec42
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878208"
---
# <span data-ttu-id="0eb02-104">0.8.355-IWebView2Settings de interface</span><span class="sxs-lookup"><span data-stu-id="0eb02-104">0.8.355 - interface IWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="0eb02-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="0eb02-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0eb02-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="0eb02-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="0eb02-107">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="0eb02-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="0eb02-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="0eb02-108">Summary</span></span>

 <span data-ttu-id="0eb02-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0eb02-109">Members</span></span>                        | <span data-ttu-id="0eb02-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="0eb02-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0eb02-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="0eb02-112">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="0eb02-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="0eb02-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="0eb02-114">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="0eb02-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="0eb02-116">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="0eb02-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="0eb02-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="0eb02-118">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="0eb02-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="0eb02-120">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="0eb02-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="0eb02-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="0eb02-122">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="0eb02-123">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="0eb02-123">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="0eb02-124">Essa configuração é preterida e sempre retornará false.</span><span class="sxs-lookup"><span data-stu-id="0eb02-124">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="0eb02-125">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="0eb02-125">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="0eb02-126">Essa configuração é preterida e não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="0eb02-126">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="0eb02-127">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-127">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="0eb02-128">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="0eb02-128">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="0eb02-129">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-129">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="0eb02-130">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-130">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="0eb02-131">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-131">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="0eb02-132">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="0eb02-132">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="0eb02-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="0eb02-134">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-134">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="0eb02-135">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="0eb02-135">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="0eb02-136">Parte</span><span class="sxs-lookup"><span data-stu-id="0eb02-136">Members</span></span>

#### <span data-ttu-id="0eb02-137">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-137">get_IsScriptEnabled</span></span> 

<span data-ttu-id="0eb02-138">Controla se a execução JavaScript está habilitada em todas as navegações futuras no WebView.</span><span class="sxs-lookup"><span data-stu-id="0eb02-138">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="0eb02-139">[get_IsScriptEnabled](#get_isscriptenabled)público HRESULT (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-139">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="0eb02-140">Isso afeta apenas scripts no documento; scripts injetados com ExecuteScript serão executados mesmo se o script estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0eb02-140">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="0eb02-141">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="0eb02-141">It is true by default.</span></span>

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

#### <span data-ttu-id="0eb02-142">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-142">put_IsScriptEnabled</span></span> 

<span data-ttu-id="0eb02-143">Defina a propriedade IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-143">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="0eb02-144">[put_IsScriptEnabled](#put_isscriptenabled)público HRESULT (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-144">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="0eb02-145">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-145">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="0eb02-146">A propriedade IsWebMessageEnabled é usada ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="0eb02-146">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="0eb02-147">[get_IsWebMessageEnabled](#get_iswebmessageenabled)público HRESULT (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-147">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="0eb02-148">Se definido como true, a comunicação do host com o documento HTML de nível superior da WebView é permitida por meio do evento de mensagem do PostWebMessageAsJson, do PostWebMessageAsString e do Window. Chrome. WebView (consulte a documentação do PostWebMessageAsJson para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="0eb02-148">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="0eb02-149">A comunicação do documento HTML de nível superior do WebView para o host é permitida por meio da função de SetWebMessageReceivedEventHandler do Window. Chrome. WebView e do método (consulte a documentação do SetWebMessageReceivedEventHandler para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="0eb02-149">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="0eb02-150">Se definido como false, a comunicação não será permitida.</span><span class="sxs-lookup"><span data-stu-id="0eb02-150">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="0eb02-151">PostWebMessageAsJson e PostWebMessageAsString falharão com E_ACCESSDENIED e Window. Chrome. WebView. CreateMessage irá falhar ao lançar uma instância de um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="0eb02-151">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="0eb02-152">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="0eb02-152">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="0eb02-153">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-153">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="0eb02-154">Defina a propriedade IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-154">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="0eb02-155">[put_IsWebMessageEnabled](#put_iswebmessageenabled)público HRESULT (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-155">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="0eb02-156">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-156">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="0eb02-157">AreDefaultScriptDialogsEnabled é usado ao carregar um novo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="0eb02-157">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="0eb02-158">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)público HRESULT (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-158">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="0eb02-159">Se definido como false, o WebView não renderizará a caixa de diálogo padrão do JavaScript (especificamente as mostradas pelas funções de alerta, confirmação e prompt do JavaScript).</span><span class="sxs-lookup"><span data-stu-id="0eb02-159">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="0eb02-160">Em vez disso, se um manipulador de eventos for definido por SetScriptDialogOpeningEventHandler, o WebView enviará um evento que conterá todas as informações da caixa de diálogo e permitirá que o aplicativo host mostre sua própria interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="0eb02-160">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="0eb02-161">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-161">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="0eb02-162">Defina a propriedade AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-162">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="0eb02-163">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)público HRESULT (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-163">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="0eb02-164">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="0eb02-164">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="0eb02-165">Essa configuração é preterida e sempre retornará false.</span><span class="sxs-lookup"><span data-stu-id="0eb02-165">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="0eb02-166">[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)público HRESULT (bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="0eb02-166">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="0eb02-167">Isso significa que os elementos da WebView só preencherão os limites da WebView.</span><span class="sxs-lookup"><span data-stu-id="0eb02-167">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="0eb02-168">Essa propriedade será completamente removida.</span><span class="sxs-lookup"><span data-stu-id="0eb02-168">This property will then be completely removed.</span></span> <span data-ttu-id="0eb02-169">Em vez disso, ouça o evento ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="0eb02-169">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="0eb02-170">Controla se o fullscreen é permitido para os elementos no WebView.</span><span class="sxs-lookup"><span data-stu-id="0eb02-170">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="0eb02-171">Quando é permitido, o conteúdo da Web, como um elemento de vídeo na WebView, pode ser exibido em tela cheia.</span><span class="sxs-lookup"><span data-stu-id="0eb02-171">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="0eb02-172">Quando não for permitido, o elemento preencherá os limites da WebView quando o elemento exigir a tela inteira.</span><span class="sxs-lookup"><span data-stu-id="0eb02-172">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="0eb02-173">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="0eb02-173">It is true by default.</span></span>

#### <span data-ttu-id="0eb02-174">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="0eb02-174">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="0eb02-175">Essa configuração é preterida e não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="0eb02-175">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="0eb02-176">[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)público HRESULT (bool IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="0eb02-176">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="0eb02-177">Em vez disso, ouça o evento ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="0eb02-177">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="0eb02-178">Defina a propriedade IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="0eb02-178">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="0eb02-179">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-179">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="0eb02-180">IsStatusBarEnabled controla se a barra de status será exibida.</span><span class="sxs-lookup"><span data-stu-id="0eb02-180">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="0eb02-181">[get_IsStatusBarEnabled](#get_isstatusbarenabled)público HRESULT (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-181">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="0eb02-182">A barra de status geralmente é exibida no canto inferior esquerdo da WebView e mostra itens como o URI de um link quando o usuário passa o mouse sobre ele e outras informações.</span><span class="sxs-lookup"><span data-stu-id="0eb02-182">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="0eb02-183">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="0eb02-183">It is true by default.</span></span>

#### <span data-ttu-id="0eb02-184">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-184">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="0eb02-185">Defina a propriedade IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-185">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="0eb02-186">[put_IsStatusBarEnabled](#put_isstatusbarenabled)público HRESULT (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-186">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="0eb02-187">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-187">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="0eb02-188">AreDevToolsEnabled controla se o usuário pode usar o menu de contexto ou os atalhos de teclado para abrir a janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="0eb02-188">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="0eb02-189">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)público HRESULT (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-189">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="0eb02-190">É verdade por padrão.</span><span class="sxs-lookup"><span data-stu-id="0eb02-190">It is true by default.</span></span>

#### <span data-ttu-id="0eb02-191">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb02-191">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="0eb02-192">Defina a propriedade AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="0eb02-192">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="0eb02-193">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)público HRESULT (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="0eb02-193">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

