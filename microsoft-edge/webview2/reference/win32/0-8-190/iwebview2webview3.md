---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 436e0e33180c65afcce0487fffeff5f168dceab7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652348"
---
# <span data-ttu-id="e76b5-104">interface IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="e76b5-104">interface IWebView2WebView3</span></span> 

> [!NOTE]
> <span data-ttu-id="e76b5-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e76b5-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e76b5-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="e76b5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="e76b5-107">Funcionalidades adicionais implementadas pelo objeto WebView primário.</span><span class="sxs-lookup"><span data-stu-id="e76b5-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="e76b5-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e76b5-108">Summary</span></span>

 <span data-ttu-id="e76b5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e76b5-109">Members</span></span>                        | <span data-ttu-id="e76b5-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e76b5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e76b5-111">Parar</span><span class="sxs-lookup"><span data-stu-id="e76b5-111">Stop</span></span>](#stop) | <span data-ttu-id="e76b5-112">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="e76b5-112">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="e76b5-113">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="e76b5-113">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="e76b5-114">Adicione um manipulador de eventos para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="e76b5-114">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="e76b5-115">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="e76b5-115">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="e76b5-116">Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="e76b5-116">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="e76b5-117">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="e76b5-117">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="e76b5-118">Adicione um manipulador de eventos para o evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="e76b5-118">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="e76b5-119">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="e76b5-119">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="e76b5-120">Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="e76b5-120">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="e76b5-121">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="e76b5-121">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="e76b5-122">O título do documento atual de nível superior.</span><span class="sxs-lookup"><span data-stu-id="e76b5-122">The title for the current top level document.</span></span>

<span data-ttu-id="e76b5-123">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="e76b5-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="e76b5-124">Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e76b5-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="e76b5-125">Parte</span><span class="sxs-lookup"><span data-stu-id="e76b5-125">Members</span></span>

#### <span data-ttu-id="e76b5-126">Parar</span><span class="sxs-lookup"><span data-stu-id="e76b5-126">Stop</span></span> 

<span data-ttu-id="e76b5-127">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="e76b5-127">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="e76b5-128">público- [limite](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="e76b5-128">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="e76b5-129">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="e76b5-129">add_NewWindowRequested</span></span> 

<span data-ttu-id="e76b5-130">Adicione um manipulador de eventos para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="e76b5-130">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="e76b5-131">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="e76b5-131">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e76b5-132">Acionado quando o conteúdo dentro do WebView solicitado para abrir uma nova janela, por exemplo, por meio de Window. Open.</span><span class="sxs-lookup"><span data-stu-id="e76b5-132">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="e76b5-133">O aplicativo pode passar um WebView de destino que será considerado a janela aberta.</span><span class="sxs-lookup"><span data-stu-id="e76b5-133">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<IWebView2NewWindowRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<IWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
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

#### <span data-ttu-id="e76b5-134">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="e76b5-134">remove_NewWindowRequested</span></span> 

<span data-ttu-id="e76b5-135">Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="e76b5-135">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="e76b5-136">[remove_NewWindowRequested](#remove_newwindowrequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="e76b5-136">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="e76b5-137">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="e76b5-137">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="e76b5-138">Adicione um manipulador de eventos para o evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="e76b5-138">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="e76b5-139">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="e76b5-139">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e76b5-140">O evento é acionado quando a propriedade DocumentTitle da WebView muda e pode ser acionada antes ou depois do evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="e76b5-140">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<IWebView2DocumentTitleChangedEventHandler>(
            [this](IWebView2WebView3* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="e76b5-141">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="e76b5-141">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="e76b5-142">Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="e76b5-142">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="e76b5-143">[remove_DocumentTitleChanged](#remove_documenttitlechanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="e76b5-143">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="e76b5-144">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="e76b5-144">get_DocumentTitle</span></span> 

<span data-ttu-id="e76b5-145">O título do documento atual de nível superior.</span><span class="sxs-lookup"><span data-stu-id="e76b5-145">The title for the current top level document.</span></span>

> <span data-ttu-id="e76b5-146">público HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span><span class="sxs-lookup"><span data-stu-id="e76b5-146">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="e76b5-147">Se o documento não tiver um título explícito ou estiver vazio, um padrão que pode ou não corresponder ao URI do documento será usado.</span><span class="sxs-lookup"><span data-stu-id="e76b5-147">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

