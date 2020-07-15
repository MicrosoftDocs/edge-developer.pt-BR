---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 06cff80d1c0dd25ab0753edd521f2c04b49816c3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878005"
---
# <span data-ttu-id="db601-104">0.8.355-IWebView2WebView5 de interface</span><span class="sxs-lookup"><span data-stu-id="db601-104">0.8.355 - interface IWebView2WebView5</span></span> 

> [!NOTE]
> <span data-ttu-id="db601-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="db601-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="db601-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="db601-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="db601-107">Funcionalidades adicionais implementadas pelo objeto WebView primário.</span><span class="sxs-lookup"><span data-stu-id="db601-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="db601-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="db601-108">Summary</span></span>

 <span data-ttu-id="db601-109">Parte</span><span class="sxs-lookup"><span data-stu-id="db601-109">Members</span></span>                        | <span data-ttu-id="db601-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="db601-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="db601-111">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="db601-111">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="db601-112">Notifica quando a propriedade ContainsFullScreenElement muda.</span><span class="sxs-lookup"><span data-stu-id="db601-112">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="db601-113">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="db601-113">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="db601-114">Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.</span><span class="sxs-lookup"><span data-stu-id="db601-114">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="db601-115">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="db601-115">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="db601-116">Indica se a WebView contém um elemento HTML de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="db601-116">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="db601-117">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="db601-117">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="db601-118">Adicione um manipulador de eventos para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="db601-118">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="db601-119">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="db601-119">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="db601-120">Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="db601-120">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="db601-121">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="db601-121">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="db601-122">Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="db601-122">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="db601-123">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="db601-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="db601-124">Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="db601-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="db601-125">Parte</span><span class="sxs-lookup"><span data-stu-id="db601-125">Members</span></span>

#### <span data-ttu-id="db601-126">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="db601-126">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="db601-127">Notifica quando a propriedade ContainsFullScreenElement muda.</span><span class="sxs-lookup"><span data-stu-id="db601-127">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="db601-128">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="db601-128">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="db601-129">Isso significa que um elemento HTML dentro do WebView está entrando em tela inteira no tamanho do WebView ou sai do fullscreen.</span><span class="sxs-lookup"><span data-stu-id="db601-129">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="db601-130">Esse evento é útil quando, por exemplo, um elemento de vídeo solicita a tela inteira.</span><span class="sxs-lookup"><span data-stu-id="db601-130">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="db601-131">O ouvinte de ContainsFullScreenElementChanged pode então redimensionar a WebView em resposta.</span><span class="sxs-lookup"><span data-stu-id="db601-131">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<IWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](IWebView2WebView5* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
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

#### <span data-ttu-id="db601-132">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="db601-132">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="db601-133">Remover um manipulador de eventos adicionado anteriormente com o método de evento add_ correspondente.</span><span class="sxs-lookup"><span data-stu-id="db601-133">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="db601-134">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="db601-134">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="db601-135">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="db601-135">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="db601-136">Indica se a WebView contém um elemento HTML de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="db601-136">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="db601-137">[get_ContainsFullScreenElement](#get_containsfullscreenelement)público HRESULT (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="db601-137">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="db601-138">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="db601-138">add_WebResourceRequested</span></span> 

<span data-ttu-id="db601-139">Adicione um manipulador de eventos para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="db601-139">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="db601-140">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="db601-140">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="db601-141">Acionado quando o WebView está executando uma solicitação HTTP para uma URL correspondente e um filtro de contexto de recurso que foi adicionado com o AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="db601-141">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="db601-142">Pelo menos um filtro deve ser adicionado para que o evento seja acionado.</span><span class="sxs-lookup"><span data-stu-id="db601-142">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
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

#### <span data-ttu-id="db601-143">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="db601-143">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="db601-144">Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="db601-144">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="db601-145">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(URI const LPCWSTR,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="db601-145">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="db601-146">O parâmetro URI pode ser uma cadeia de caracteres curinga (' ': zero ou mais, '? ': exatamente um).</span><span class="sxs-lookup"><span data-stu-id="db601-146">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="db601-147">nullptr é equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="db601-147">nullptr is equivalent to L"".</span></span> <span data-ttu-id="db601-148">Consulte WEBVIEW2_WEB_RESOURCE_CONTEXT enumeração para obter a descrição dos filtros de contexto de recurso.</span><span class="sxs-lookup"><span data-stu-id="db601-148">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="db601-149">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="db601-149">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="db601-150">Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="db601-150">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="db601-151">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(URI const LPCWSTR,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="db601-151">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="db601-152">Se o mesmo filtro tiver sido adicionado várias vezes, será preciso removê-lo quantas vezes forem adicionadas para que a remoção seja efetiva.</span><span class="sxs-lookup"><span data-stu-id="db601-152">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="db601-153">Retorna E_INVALIDARG para um filtro que nunca foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="db601-153">Returns E_INVALIDARG for a filter that was never added.</span></span>

