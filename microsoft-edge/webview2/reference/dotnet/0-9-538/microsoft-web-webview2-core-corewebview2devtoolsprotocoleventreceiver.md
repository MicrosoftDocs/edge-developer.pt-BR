---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: d99349ec763796bd6b1ea242abbe5c2219c221c2
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698249"
---
# <span data-ttu-id="1a84f-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="1a84f-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="1a84f-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1a84f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1a84f-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="1a84f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1a84f-107">Um receptor é criado para um determinado evento de protocolo DevTools e permite que você assine e cancele a assinatura desse evento.</span><span class="sxs-lookup"><span data-stu-id="1a84f-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="1a84f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="1a84f-108">Summary</span></span>

 <span data-ttu-id="1a84f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1a84f-109">Members</span></span>                        | <span data-ttu-id="1a84f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="1a84f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1a84f-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="1a84f-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="1a84f-112">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="1a84f-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="1a84f-113">Obtido do objeto WebView via GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="1a84f-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="1a84f-114">Parte</span><span class="sxs-lookup"><span data-stu-id="1a84f-114">Members</span></span>

#### <span data-ttu-id="1a84f-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="1a84f-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="1a84f-116">Assine um evento DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="1a84f-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="1a84f-117">< do evento público EventHandler [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="1a84f-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="1a84f-118">O método Invoke do manipulador será chamado sempre que o evento DevToolsProtocol correspondente for acionado.</span><span class="sxs-lookup"><span data-stu-id="1a84f-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="1a84f-119">Invoke será chamado com o objeto do evento args que contém o objeto de parâmetro do evento de protocolo DevTools como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="1a84f-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

