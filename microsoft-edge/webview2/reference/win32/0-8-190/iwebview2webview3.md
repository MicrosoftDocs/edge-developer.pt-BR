---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: a095b1ed085cd49a597195e01da21cde53b9095d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884740"
---
# <span data-ttu-id="4ffc4-104">0.8.355-IWebView2WebView3 de interface</span><span class="sxs-lookup"><span data-stu-id="4ffc4-104">0.8.355 - interface IWebView2WebView3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="4ffc4-105">Funcionalidades adicionais implementadas pelo objeto WebView primário.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="4ffc4-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4ffc4-106">Summary</span></span>

 <span data-ttu-id="4ffc4-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4ffc4-107">Members</span></span>                        | <span data-ttu-id="4ffc4-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4ffc4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4ffc4-109">Parar</span><span class="sxs-lookup"><span data-stu-id="4ffc4-109">Stop</span></span>](#stop) | <span data-ttu-id="4ffc4-110">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-110">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="4ffc4-111">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="4ffc4-111">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="4ffc4-112">Adicione um manipulador de eventos para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-112">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="4ffc4-113">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="4ffc4-113">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="4ffc4-114">Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-114">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="4ffc4-115">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="4ffc4-115">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="4ffc4-116">Adicione um manipulador de eventos para o evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-116">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="4ffc4-117">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="4ffc4-117">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="4ffc4-118">Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-118">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="4ffc4-119">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="4ffc4-119">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="4ffc4-120">O título do documento atual de nível superior.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-120">The title for the current top level document.</span></span>

<span data-ttu-id="4ffc4-121">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="4ffc4-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="4ffc4-122">Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="4ffc4-123">Parte</span><span class="sxs-lookup"><span data-stu-id="4ffc4-123">Members</span></span>

#### <span data-ttu-id="4ffc4-124">Parar</span><span class="sxs-lookup"><span data-stu-id="4ffc4-124">Stop</span></span> 

<span data-ttu-id="4ffc4-125">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-125">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="4ffc4-126">público- [limite](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="4ffc4-126">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="4ffc4-127">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="4ffc4-127">add_NewWindowRequested</span></span> 

<span data-ttu-id="4ffc4-128">Adicione um manipulador de eventos para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-128">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="4ffc4-129">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="4ffc4-129">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4ffc4-130">Acionado quando o conteúdo dentro do WebView solicitado para abrir uma nova janela, por exemplo, por meio de Window. Open.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-130">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="4ffc4-131">O aplicativo pode passar um WebView de destino que será considerado a janela aberta.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-131">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="4ffc4-132">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="4ffc4-132">remove_NewWindowRequested</span></span> 

<span data-ttu-id="4ffc4-133">Remover um manipulador de eventos adicionado anteriormente com add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-133">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="4ffc4-134">[remove_NewWindowRequested](#remove_newwindowrequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="4ffc4-134">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4ffc4-135">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="4ffc4-135">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="4ffc4-136">Adicione um manipulador de eventos para o evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-136">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="4ffc4-137">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="4ffc4-137">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4ffc4-138">O evento é acionado quando a propriedade DocumentTitle da WebView muda e pode ser acionada antes ou depois do evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-138">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="4ffc4-139">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="4ffc4-139">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="4ffc4-140">Remover um manipulador de eventos adicionado anteriormente com add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-140">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="4ffc4-141">[remove_DocumentTitleChanged](#remove_documenttitlechanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="4ffc4-141">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4ffc4-142">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="4ffc4-142">get_DocumentTitle</span></span> 

<span data-ttu-id="4ffc4-143">O título do documento atual de nível superior.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-143">The title for the current top level document.</span></span>

> <span data-ttu-id="4ffc4-144">público HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span><span class="sxs-lookup"><span data-stu-id="4ffc4-144">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="4ffc4-145">Se o documento não tiver um título explícito ou estiver vazio, um padrão que pode ou não corresponder ao URI do documento será usado.</span><span class="sxs-lookup"><span data-stu-id="4ffc4-145">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

