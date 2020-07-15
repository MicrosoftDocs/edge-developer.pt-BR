---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 5e6e2d955dd0d52a093eea116a01961e1ee58c76
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877767"
---
# <span data-ttu-id="b07d0-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="b07d0-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

> [!NOTE]
> <span data-ttu-id="b07d0-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b07d0-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b07d0-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="b07d0-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="b07d0-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b07d0-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b07d0-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b07d0-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b07d0-109">Um receptor é criado para um determinado evento de protocolo DevTools e permite que você assine e cancele a assinatura desse evento.</span><span class="sxs-lookup"><span data-stu-id="b07d0-109">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="b07d0-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="b07d0-110">Summary</span></span>

 <span data-ttu-id="b07d0-111">Parte</span><span class="sxs-lookup"><span data-stu-id="b07d0-111">Members</span></span>                        | <span data-ttu-id="b07d0-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="b07d0-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b07d0-113">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="b07d0-113">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="b07d0-114">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="b07d0-114">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="b07d0-115">Obtido do objeto WebView via GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="b07d0-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="b07d0-116">Parte</span><span class="sxs-lookup"><span data-stu-id="b07d0-116">Members</span></span>

#### <span data-ttu-id="b07d0-117">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="b07d0-117">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="b07d0-118">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="b07d0-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="b07d0-119">< do evento público EventHandler [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="b07d0-119">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="b07d0-120">O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado.</span><span class="sxs-lookup"><span data-stu-id="b07d0-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="b07d0-121">Invoke será chamado com o objeto do evento args que contém o objeto de parâmetro do evento de protocolo DevTools como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="b07d0-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

