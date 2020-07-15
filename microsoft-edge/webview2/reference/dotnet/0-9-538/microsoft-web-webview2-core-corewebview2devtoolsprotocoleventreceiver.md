---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: 155b0ae414d03d7a062b1e3426331307457687ae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878908"
---
# <span data-ttu-id="3786b-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="3786b-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="3786b-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3786b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3786b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="3786b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3786b-107">Um receptor é criado para um determinado evento de protocolo DevTools e permite que você assine e cancele a assinatura desse evento.</span><span class="sxs-lookup"><span data-stu-id="3786b-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="3786b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="3786b-108">Summary</span></span>

 <span data-ttu-id="3786b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3786b-109">Members</span></span>                        | <span data-ttu-id="3786b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="3786b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3786b-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="3786b-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="3786b-112">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="3786b-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="3786b-113">Obtido do objeto WebView via GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="3786b-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="3786b-114">Parte</span><span class="sxs-lookup"><span data-stu-id="3786b-114">Members</span></span>

#### <span data-ttu-id="3786b-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="3786b-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="3786b-116">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="3786b-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="3786b-117">< do evento público EventHandler [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="3786b-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="3786b-118">O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado.</span><span class="sxs-lookup"><span data-stu-id="3786b-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="3786b-119">Invoke será chamado com o objeto do evento args que contém o objeto de parâmetro do evento de protocolo DevTools como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="3786b-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

