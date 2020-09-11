---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Referência do c 0.9.579-WebView2 Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 92fad0c93e4942a92f5940834b0057043491b539
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010205"
---
# <span data-ttu-id="8d3bf-104">0.9.579-Reference (WebView2 Win32 C++)</span><span class="sxs-lookup"><span data-stu-id="8d3bf-104">0.9.579 - Reference (WebView2 Win32 C++)</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

<span data-ttu-id="8d3bf-105">O controle WebView2 do Microsoft Edge permite que você hospede conteúdo da Web em seu aplicativo usando o [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) como mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d3bf-105">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="8d3bf-106">Para obter mais informações, consulte [visão geral do Microsoft Edge WebView2](../../index.md)) e [introdução ao WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="8d3bf-106">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="8d3bf-107">[ICoreWebView2](0-9-538/ICoreWebView2.md) é um ótimo lugar para começar a aprender os detalhes da API.</span><span class="sxs-lookup"><span data-stu-id="8d3bf-107">[ICoreWebView2](0-9-538/ICoreWebView2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="8d3bf-108">Globais</span><span class="sxs-lookup"><span data-stu-id="8d3bf-108">Globals</span></span>  

*   [<span data-ttu-id="8d3bf-109">Globais</span><span class="sxs-lookup"><span data-stu-id="8d3bf-109">Globals</span></span>](0-9-538/webview2-idl.md)  

## <span data-ttu-id="8d3bf-110">Classes</span><span class="sxs-lookup"><span data-stu-id="8d3bf-110">Interfaces</span></span>  
*   [<span data-ttu-id="8d3bf-111">ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8d3bf-111">ICoreWebView2</span></span>](0-9-538/icorewebview2.md)
*   [<span data-ttu-id="8d3bf-112">ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="8d3bf-112">ICoreWebView2Controller</span></span>](0-9-538/icorewebview2controller.md)
*   [<span data-ttu-id="8d3bf-113">ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="8d3bf-113">ICoreWebView2Deferral</span></span>](0-9-538/icorewebview2deferral.md)
*   [<span data-ttu-id="8d3bf-114">ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="8d3bf-114">ICoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-538/icorewebview2devtoolsprotocoleventreceiver.md)
*   [<span data-ttu-id="8d3bf-115">ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="8d3bf-115">ICoreWebView2Environment</span></span>](0-9-538/icorewebview2environment.md)
*   [<span data-ttu-id="8d3bf-116">ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="8d3bf-116">ICoreWebView2EnvironmentOptions</span></span>](0-9-538/icorewebview2environmentoptions.md)
*   [<span data-ttu-id="8d3bf-117">ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="8d3bf-117">ICoreWebView2HttpHeadersCollectionIterator</span></span>](0-9-538/icorewebview2httpheaderscollectioniterator.md)
*   [<span data-ttu-id="8d3bf-118">ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="8d3bf-118">ICoreWebView2HttpRequestHeaders</span></span>](0-9-538/icorewebview2httprequestheaders.md)
*   [<span data-ttu-id="8d3bf-119">ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="8d3bf-119">ICoreWebView2HttpResponseHeaders</span></span>](0-9-538/icorewebview2httpresponseheaders.md)
*   [<span data-ttu-id="8d3bf-120">ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="8d3bf-120">ICoreWebView2Settings</span></span>](0-9-538/icorewebview2settings.md)
*   [<span data-ttu-id="8d3bf-121">ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="8d3bf-121">ICoreWebView2WebResourceRequest</span></span>](0-9-538/icorewebview2webresourcerequest.md)
*   [<span data-ttu-id="8d3bf-122">ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="8d3bf-122">ICoreWebView2WebResourceResponse</span></span>](0-9-538/icorewebview2webresourceresponse.md)

### <span data-ttu-id="8d3bf-123">Argumentos de evento</span><span class="sxs-lookup"><span data-stu-id="8d3bf-123">Event arguments</span></span>

*   [<span data-ttu-id="8d3bf-124">ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-124">ICoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-538/icorewebview2acceleratorkeypressedeventargs.md)
*   [<span data-ttu-id="8d3bf-125">ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-125">ICoreWebView2ContentLoadingEventArgs</span></span>](0-9-538/icorewebview2contentloadingeventargs.md)
*   [<span data-ttu-id="8d3bf-126">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-126">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-538/icorewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [<span data-ttu-id="8d3bf-127">ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-127">ICoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-538/icorewebview2movefocusrequestedeventargs.md)
*   [<span data-ttu-id="8d3bf-128">ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-128">ICoreWebView2NavigationCompletedEventArgs</span></span>](0-9-538/icorewebview2navigationcompletedeventargs.md)
*   [<span data-ttu-id="8d3bf-129">ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-129">ICoreWebView2NavigationStartingEventArgs</span></span>](0-9-538/icorewebview2navigationstartingeventargs.md)
*   [<span data-ttu-id="8d3bf-130">ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-130">ICoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-538/icorewebview2newwindowrequestedeventargs.md)
*   [<span data-ttu-id="8d3bf-131">ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-131">ICoreWebView2PermissionRequestedEventArgs</span></span>](0-9-538/icorewebview2permissionrequestedeventargs.md)
*   [<span data-ttu-id="8d3bf-132">ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-132">ICoreWebView2ProcessFailedEventArgs</span></span>](0-9-538/icorewebview2processfailedeventargs.md)
*   [<span data-ttu-id="8d3bf-133">ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-133">ICoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-538/icorewebview2scriptdialogopeningeventargs.md)
*   [<span data-ttu-id="8d3bf-134">ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-134">ICoreWebView2SourceChangedEventArgs</span></span>](0-9-538/icorewebview2sourcechangedeventargs.md)
*   [<span data-ttu-id="8d3bf-135">ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-135">ICoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-538/icorewebview2webmessagereceivedeventargs.md)
*   [<span data-ttu-id="8d3bf-136">ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-136">ICoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-538/icorewebview2webresourcerequestedeventargs.md)

### <span data-ttu-id="8d3bf-137">Delega</span><span class="sxs-lookup"><span data-stu-id="8d3bf-137">Delegates</span></span>

*   [<span data-ttu-id="8d3bf-138">ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-138">ICoreWebView2AcceleratorKeyPressedEventHandler</span></span>](0-9-538/icorewebview2acceleratorkeypressedeventhandler.md)
*   [<span data-ttu-id="8d3bf-139">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-139">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-9-538/icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md)
*   [<span data-ttu-id="8d3bf-140">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-140">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-9-538/icorewebview2calldevtoolsprotocolmethodcompletedhandler.md)
*   [<span data-ttu-id="8d3bf-141">ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-141">ICoreWebView2CapturePreviewCompletedHandler</span></span>](0-9-538/icorewebview2capturepreviewcompletedhandler.md)
*   [<span data-ttu-id="8d3bf-142">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-142">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-9-538/icorewebview2containsfullscreenelementchangedeventhandler.md)
*   [<span data-ttu-id="8d3bf-143">ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-143">ICoreWebView2ContentLoadingEventHandler</span></span>](0-9-538/icorewebview2contentloadingeventhandler.md)
*   [<span data-ttu-id="8d3bf-144">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-144">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span>](0-9-538/icorewebview2createcorewebview2controllercompletedhandler.md)
*   [<span data-ttu-id="8d3bf-145">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-145">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span>](0-9-538/icorewebview2createcorewebview2environmentcompletedhandler.md)
*   [<span data-ttu-id="8d3bf-146">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-146">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-9-538/icorewebview2devtoolsprotocoleventreceivedeventhandler.md)
*   [<span data-ttu-id="8d3bf-147">ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-147">ICoreWebView2DocumentTitleChangedEventHandler</span></span>](0-9-538/icorewebview2documenttitlechangedeventhandler.md)
*   [<span data-ttu-id="8d3bf-148">ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-148">ICoreWebView2ExecuteScriptCompletedHandler</span></span>](0-9-538/icorewebview2executescriptcompletedhandler.md)
*   [<span data-ttu-id="8d3bf-149">ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-149">ICoreWebView2FocusChangedEventHandler</span></span>](0-9-538/icorewebview2focuschangedeventhandler.md)
*   [<span data-ttu-id="8d3bf-150">ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-150">ICoreWebView2HistoryChangedEventHandler</span></span>](0-9-538/icorewebview2historychangedeventhandler.md)
*   [<span data-ttu-id="8d3bf-151">ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-151">ICoreWebView2MoveFocusRequestedEventHandler</span></span>](0-9-538/icorewebview2movefocusrequestedeventhandler.md)
*   [<span data-ttu-id="8d3bf-152">ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-152">ICoreWebView2NavigationCompletedEventHandler</span></span>](0-9-538/icorewebview2navigationcompletedeventhandler.md)
*   [<span data-ttu-id="8d3bf-153">ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-153">ICoreWebView2NavigationStartingEventHandler</span></span>](0-9-538/icorewebview2navigationstartingeventhandler.md)
*   [<span data-ttu-id="8d3bf-154">ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-154">ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span>](0-9-538/icorewebview2newbrowserversionavailableeventhandler.md)
*   [<span data-ttu-id="8d3bf-155">ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-155">ICoreWebView2NewWindowRequestedEventHandler</span></span>](0-9-538/icorewebview2newwindowrequestedeventhandler.md)
*   [<span data-ttu-id="8d3bf-156">ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-156">ICoreWebView2PermissionRequestedEventHandler</span></span>](0-9-538/icorewebview2permissionrequestedeventhandler.md)
*   [<span data-ttu-id="8d3bf-157">ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-157">ICoreWebView2ProcessFailedEventHandler</span></span>](0-9-538/icorewebview2processfailedeventhandler.md)
*   [<span data-ttu-id="8d3bf-158">ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-158">ICoreWebView2ScriptDialogOpeningEventHandler</span></span>](0-9-538/icorewebview2scriptdialogopeningeventhandler.md)
*   [<span data-ttu-id="8d3bf-159">ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-159">ICoreWebView2SourceChangedEventHandler</span></span>](0-9-538/icorewebview2sourcechangedeventhandler.md)
*   [<span data-ttu-id="8d3bf-160">ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-160">ICoreWebView2WebMessageReceivedEventHandler</span></span>](0-9-538/icorewebview2webmessagereceivedeventhandler.md)
*   [<span data-ttu-id="8d3bf-161">ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-161">ICoreWebView2WebResourceRequestedEventHandler</span></span>](0-9-538/icorewebview2webresourcerequestedeventhandler.md)
*   [<span data-ttu-id="8d3bf-162">ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-162">ICoreWebView2WindowCloseRequestedEventHandler</span></span>](0-9-538/icorewebview2windowcloserequestedeventhandler.md)
*   [<span data-ttu-id="8d3bf-163">ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-163">ICoreWebView2ZoomFactorChangedEventHandler</span></span>](0-9-538/icorewebview2zoomfactorchangedeventhandler.md)

### <span data-ttu-id="8d3bf-164">Experimental</span><span class="sxs-lookup"><span data-stu-id="8d3bf-164">Experimental</span></span>

*   [<span data-ttu-id="8d3bf-165">ICoreWebView2Experimental</span><span class="sxs-lookup"><span data-stu-id="8d3bf-165">ICoreWebView2Experimental</span></span>](0-9-538/icorewebview2experimental.md)
*   [<span data-ttu-id="8d3bf-166">ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="8d3bf-166">ICoreWebView2ExperimentalCompositionController</span></span>](0-9-538/icorewebview2experimentalcompositioncontroller.md)
*   [<span data-ttu-id="8d3bf-167">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-167">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span>](0-9-538/icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md)
*   [<span data-ttu-id="8d3bf-168">ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-168">ICoreWebView2ExperimentalCursorChangedEventHandler</span></span>](0-9-538/icorewebview2experimentalcursorchangedeventhandler.md)
*   [<span data-ttu-id="8d3bf-169">ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="8d3bf-169">ICoreWebView2ExperimentalEnvironment</span></span>](0-9-538/icorewebview2experimentalenvironment.md)
*   [<span data-ttu-id="8d3bf-170">ICoreWebView2ExperimentalEnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="8d3bf-170">ICoreWebView2ExperimentalEnvironmentOptions</span></span>](0-9-538/icorewebview2experimentalenvironmentoptions.md)
*   [<span data-ttu-id="8d3bf-171">ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-171">ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span>](0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md)
*   [<span data-ttu-id="8d3bf-172">ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="8d3bf-172">ICoreWebView2ExperimentalPointerInfo</span></span>](0-9-538/icorewebview2experimentalpointerinfo.md)
*   [<span data-ttu-id="8d3bf-173">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d3bf-173">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span>](0-9-538/icorewebview2experimentalwebresourceresponsereceivedeventargs.md)
*   [<span data-ttu-id="8d3bf-174">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-174">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span>](0-9-538/icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md)
*   [<span data-ttu-id="8d3bf-175">ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8d3bf-175">ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span>](0-9-538/icorewebview2experimentalwebresourceresponsereceivedeventhandler.md)
*   [<span data-ttu-id="8d3bf-176">ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="8d3bf-176">ICoreWebView2ExperimentalWindowFeatures</span></span>](0-9-538/icorewebview2experimentalwindowfeatures.md)
