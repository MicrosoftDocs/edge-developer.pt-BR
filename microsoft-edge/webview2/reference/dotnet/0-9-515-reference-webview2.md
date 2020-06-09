---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: b6131245a550da54545478c9c19e0e9e45d7f7d3
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697242"
---
# <span data-ttu-id="27d0d-104">0-9-515-Reference (WebView2)</span><span class="sxs-lookup"><span data-stu-id="27d0d-104">0-9-515 - Reference (WebView2)</span></span>  

> [!NOTE]
> <span data-ttu-id="27d0d-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="27d0d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="27d0d-106">Consulte a [referência de API WebView2](../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="27d0d-106">Please refer to [WebView2 API reference](../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="27d0d-107">O controle WebView2 do Microsoft Edge permite que você hospede conteúdo da Web em seu aplicativo usando o [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) como mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="27d0d-107">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="27d0d-108">Para obter mais informações, consulte [visão geral do Microsoft Edge WebView2](../../index.md)) e [introdução ao WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="27d0d-108">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="27d0d-109">[Microsoft. Web. WebView2. Core. CoreWebView2](0-9-515/microsoft-web-webview2-core-corewebview2.md) é um ótimo lugar para começar a aprender os detalhes da API.</span><span class="sxs-lookup"><span data-stu-id="27d0d-109">[Microsoft.Web.WebView2.Core.CoreWebView2](0-9-515/microsoft-web-webview2-core-corewebview2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="27d0d-110">Microsoft. Web. WebView2. Core</span><span class="sxs-lookup"><span data-stu-id="27d0d-110">Microsoft.Web.WebView2.Core</span></span>
*   <span data-ttu-id="27d0d-111">Namespace [Microsoft. Web. WebView2. Core](0-9-515/namespace-microsoft-web-webview2-core.md)</span><span class="sxs-lookup"><span data-stu-id="27d0d-111">[Microsoft.Web.WebView2.Core](0-9-515/namespace-microsoft-web-webview2-core.md) namespace</span></span>
*   [<span data-ttu-id="27d0d-112">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="27d0d-112">CoreWebView2</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2.md)
*   [<span data-ttu-id="27d0d-113">CoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="27d0d-113">CoreWebView2Controller</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2controller.md)
*   [<span data-ttu-id="27d0d-114">CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="27d0d-114">CoreWebView2Deferral</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2deferral.md)
*   [<span data-ttu-id="27d0d-115">CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="27d0d-115">CoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceiver.md)
*   [<span data-ttu-id="27d0d-116">CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="27d0d-116">CoreWebView2Environment</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2environment.md)
*   [<span data-ttu-id="27d0d-117">CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="27d0d-117">CoreWebView2EnvironmentOptions</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2environmentoptions.md)
*   [<span data-ttu-id="27d0d-118">CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="27d0d-118">CoreWebView2PhysicalKeyStatus</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2physicalkeystatus.md)
*   [<span data-ttu-id="27d0d-119">CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="27d0d-119">CoreWebView2Settings</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2settings.md)
*   [<span data-ttu-id="27d0d-120">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="27d0d-120">EdgeNotFoundException</span></span>](0-9-515/microsoft-web-webview2-core-edgenotfoundexception.md)

### <span data-ttu-id="27d0d-121">Argumentos de evento</span><span class="sxs-lookup"><span data-stu-id="27d0d-121">Event arguments</span></span>

*   [<span data-ttu-id="27d0d-122">CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-122">CoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2acceleratorkeypressedeventargs.md)
*   [<span data-ttu-id="27d0d-123">CoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-123">CoreWebView2ContentLoadingEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2contentloadingeventargs.md)
*   [<span data-ttu-id="27d0d-124">CoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-124">CoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [<span data-ttu-id="27d0d-125">CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-125">CoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2movefocusrequestedeventargs.md)
*   [<span data-ttu-id="27d0d-126">CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-126">CoreWebView2NavigationCompletedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)
*   [<span data-ttu-id="27d0d-127">CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-127">CoreWebView2NavigationStartingEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)
*   [<span data-ttu-id="27d0d-128">CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-128">CoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2newwindowrequestedeventargs.md)
*   [<span data-ttu-id="27d0d-129">CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-129">CoreWebView2PermissionRequestedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2permissionrequestedeventargs.md)
*   [<span data-ttu-id="27d0d-130">CoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-130">CoreWebView2ProcessFailedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2processfailedeventargs.md)
*   [<span data-ttu-id="27d0d-131">CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-131">CoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2scriptdialogopeningeventargs.md)
*   [<span data-ttu-id="27d0d-132">CoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-132">CoreWebView2SourceChangedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2sourcechangedeventargs.md)
*   [<span data-ttu-id="27d0d-133">CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-133">CoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2webmessagereceivedeventargs.md)
*   [<span data-ttu-id="27d0d-134">CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27d0d-134">CoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2webresourcerequestedeventargs.md)
