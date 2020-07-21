---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 1982c6926d2ed8805433efc4d46ff6f3cac691ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885050"
---
# <span data-ttu-id="84b4a-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="84b4a-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="84b4a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="84b4a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="84b4a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="84b4a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="84b4a-107">Um receptor é criado para um determinado evento de protocolo DevTools e permite que você assine e cancele a assinatura desse evento.</span><span class="sxs-lookup"><span data-stu-id="84b4a-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="84b4a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="84b4a-108">Summary</span></span>

 <span data-ttu-id="84b4a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="84b4a-109">Members</span></span>                        | <span data-ttu-id="84b4a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="84b4a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="84b4a-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="84b4a-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="84b4a-112">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="84b4a-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="84b4a-113">Obtido do objeto WebView via GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="84b4a-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="84b4a-114">Parte</span><span class="sxs-lookup"><span data-stu-id="84b4a-114">Members</span></span>

#### <span data-ttu-id="84b4a-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="84b4a-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="84b4a-116">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="84b4a-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="84b4a-117">< do evento público EventHandler [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="84b4a-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="84b4a-118">O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado.</span><span class="sxs-lookup"><span data-stu-id="84b4a-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="84b4a-119">Invoke será chamado com o objeto do evento args que contém o objeto de parâmetro do evento de protocolo DevTools como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="84b4a-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

