---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2Experimental
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2Experimental
ms.openlocfilehash: 01bea6a6f89c61e34fe03af6007bee359770fb54
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011143"
---
# <span data-ttu-id="37859-104">0.9.579-ICoreWebView2Experimental de interface</span><span class="sxs-lookup"><span data-stu-id="37859-104">0.9.579 - interface ICoreWebView2Experimental</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2Experimental
  : public IUnknown
```

## <span data-ttu-id="37859-105">Resumo</span><span class="sxs-lookup"><span data-stu-id="37859-105">Summary</span></span>

 <span data-ttu-id="37859-106">Parte</span><span class="sxs-lookup"><span data-stu-id="37859-106">Members</span></span>                        | <span data-ttu-id="37859-107">Descrições</span><span class="sxs-lookup"><span data-stu-id="37859-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="37859-108">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="37859-108">add_WebResourceResponseReceived</span></span>](#add_webresourceresponsereceived) | <span data-ttu-id="37859-109">Adicione um manipulador de eventos para o evento WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="37859-109">Add an event handler for the WebResourceResponseReceived event.</span></span>
[<span data-ttu-id="37859-110">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="37859-110">remove_WebResourceResponseReceived</span></span>](#remove_webresourceresponsereceived) | <span data-ttu-id="37859-111">Remove o manipulador de eventos WebResourceResponseReceived anteriormente adicionado com add_WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="37859-111">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

## <span data-ttu-id="37859-112">Parte</span><span class="sxs-lookup"><span data-stu-id="37859-112">Members</span></span>

#### <span data-ttu-id="37859-113">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="37859-113">add_WebResourceResponseReceived</span></span> 

<span data-ttu-id="37859-114">Adicione um manipulador de eventos para o evento WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="37859-114">Add an event handler for the WebResourceResponseReceived event.</span></span>

> <span data-ttu-id="37859-115">Public HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="37859-115">public HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="37859-116">O evento WebResourceResponseReceived é acionado depois que a WebView recebeu e processou a resposta de uma solicitação WebResource.</span><span class="sxs-lookup"><span data-stu-id="37859-116">WebResourceResponseReceived event fires after the WebView has received and processed the response for a WebResource request.</span></span> <span data-ttu-id="37859-117">Os args de evento incluem o WebResourceRequest como enviado pelo fio e WebResourceResponse recebidos, incluindo outros cabeçalhos adicionais adicionados pela pilha de rede que não foram incluídos como parte do evento WebResourceRequested associado, como cabeçalhos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="37859-117">The event args include the WebResourceRequest as sent by the wire and WebResourceResponse received, including any additional headers added by the network stack that were not be included as part of the associated WebResourceRequested event, such as Authentication headers.</span></span> 
```cpp
    wil::com_ptr<ICoreWebView2Experimental> webviewExperimental;
    CHECK_FAILURE(m_appWindow->GetWebView()->QueryInterface(IID_PPV_ARGS(&webviewExperimental)));
    CHECK_FAILURE(webviewExperimental->add_WebResourceResponseReceived(
        Callback<ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler>(
            [this](
                ICoreWebView2Experimental* sender,
                ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs* args) {           
                wil::com_ptr<ICoreWebView2WebResourceRequest> request;
                CHECK_FAILURE(args->get_Request(&request));
                wil::unique_cotaskmem_string uri;
                CHECK_FAILURE(request->get_Uri(&uri));
                if (wcscmp(uri.get(), L"https://authenticationtest.com/HTTPAuth/") == 0)
                {
                    wil::com_ptr<ICoreWebView2HttpRequestHeaders> requestHeaders;
                    CHECK_FAILURE(request->get_Headers(&requestHeaders));

                    wil::unique_cotaskmem_string authHeaderValue;
                    if (requestHeaders->GetHeader(L"Authorization", &authHeaderValue) == S_OK)
                    {
                        std::wstring message(L"Authorization: ");
                        message += authHeaderValue.get();
                        MessageBox(nullptr, message.c_str(), nullptr, MB_OK);
                        m_appWindow->DeleteComponent(this);
                    }
                }
                
                return S_OK;
            })
            .Get(),
        &m_webResourceResponseReceivedToken));
```

#### <span data-ttu-id="37859-118">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="37859-118">remove_WebResourceResponseReceived</span></span> 

<span data-ttu-id="37859-119">Remove o manipulador de eventos WebResourceResponseReceived anteriormente adicionado com add_WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="37859-119">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

> <span data-ttu-id="37859-120">[remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="37859-120">public HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(EventRegistrationToken token)</span></span>

