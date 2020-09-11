---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: 8b6076842e6670d425be563687c18d312afd69d7
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010254"
---
# 0.9.579-ICoreWebView2DevToolsProtocolEventReceiver de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

Um receptor é criado para um determinado evento de protocolo DevTools e permite que você assine e cancele a assinatura desse evento.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | Assine um evento DevToolsProtocol.
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Remover um manipulador de eventos adicionado anteriormente com add_DevToolsProtocolEventReceived.

Obtido do objeto WebView via GetDevToolsProtocolEventReceiver.

## Parte

#### add_DevToolsProtocolEventReceived 

Assine um evento DevToolsProtocol.

> [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)público HRESULT (manipulador[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) *, EventRegistrationToken * token)

O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado. Invoke será chamado com um objeto args de evento que contém o objeto de parâmetro do evento de protocolo DevTools como uma cadeia de caracteres JSON.

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

#### remove_DevToolsProtocolEventReceived 

Remover um manipulador de eventos adicionado anteriormente com add_DevToolsProtocolEventReceived.

> [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)público HRESULT (token EventRegistrationToken)

