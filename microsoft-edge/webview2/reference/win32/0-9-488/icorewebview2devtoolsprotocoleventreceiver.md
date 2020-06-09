---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 760919ba215f725cac10ad03d278d0a3e994286e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698054"
---
# <span data-ttu-id="a4f45-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="a4f45-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

> [!NOTE]
> <span data-ttu-id="a4f45-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a4f45-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a4f45-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a4f45-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="a4f45-107">Um receptor é criado para um determinado evento de protocolo DevTools e permite que você assine e cancele a assinatura desse evento.</span><span class="sxs-lookup"><span data-stu-id="a4f45-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="a4f45-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a4f45-108">Summary</span></span>

 <span data-ttu-id="a4f45-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a4f45-109">Members</span></span>                        | <span data-ttu-id="a4f45-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a4f45-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a4f45-111">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="a4f45-111">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="a4f45-112">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="a4f45-112">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="a4f45-113">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="a4f45-113">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="a4f45-114">Remover um manipulador de eventos adicionado anteriormente com add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="a4f45-114">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="a4f45-115">Obtido do objeto WebView via GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="a4f45-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="a4f45-116">Parte</span><span class="sxs-lookup"><span data-stu-id="a4f45-116">Members</span></span>

#### <span data-ttu-id="a4f45-117">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="a4f45-117">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="a4f45-118">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="a4f45-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="a4f45-119">[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)público HRESULT (manipulador[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="a4f45-119">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="a4f45-120">O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado.</span><span class="sxs-lookup"><span data-stu-id="a4f45-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="a4f45-121">Invoke será chamado com o objeto do evento args que contém o objeto de parâmetro do evento de protocolo DevTools como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="a4f45-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="a4f45-122">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="a4f45-122">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="a4f45-123">Remover um manipulador de eventos adicionado anteriormente com add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="a4f45-123">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="a4f45-124">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="a4f45-124">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

