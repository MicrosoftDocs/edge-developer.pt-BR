---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. WinForms. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. WinForms. WebView2
ms.openlocfilehash: 7d707c2a6ecb8127074735f06ba6d4f1f28eea0c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879447"
---
# <span data-ttu-id="ec3ea-104">Classe Microsoft. Web. WebView2. WinForms. WebView2</span><span class="sxs-lookup"><span data-stu-id="ec3ea-104">Microsoft.Web.WebView2.WinForms.WebView2 class</span></span> 

<span data-ttu-id="ec3ea-105">Namespace: Microsoft. Web. WebView2. WinForms </span><span class="sxs-lookup"><span data-stu-id="ec3ea-105">Namespace: Microsoft.Web.WebView2.WinForms</span></span>\
<span data-ttu-id="ec3ea-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span><span class="sxs-lookup"><span data-stu-id="ec3ea-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span></span>

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

<span data-ttu-id="ec3ea-107">Controle para inserir WebView2 em WinForms.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-107">Control to embed WebView2 in WinForms.</span></span>

## <span data-ttu-id="ec3ea-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ec3ea-108">Summary</span></span>

 <span data-ttu-id="ec3ea-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ec3ea-109">Members</span></span>                        | <span data-ttu-id="ec3ea-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ec3ea-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ec3ea-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="ec3ea-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="ec3ea-112">ContentLoading despachos quando uma navegação começa a ser um novo URI e o conteúdo desse URI começa a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-112">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>
[<span data-ttu-id="ec3ea-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="ec3ea-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="ec3ea-114">Esse evento é acionado quando o [CoreWebView2](#corewebview2) do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-114">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="ec3ea-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="ec3ea-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="ec3ea-116">O NavigationCompleted despacha após uma navegação do documento de nível superior executa a renderização com êxito ou não.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-116">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>
[<span data-ttu-id="ec3ea-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="ec3ea-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="ec3ea-118">O NavigationStarting despacha antes de uma nova navegação começar para o documento de nível superior do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-118">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>
[<span data-ttu-id="ec3ea-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="ec3ea-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="ec3ea-120">Os despachos SourceChanged após a alteração da propriedade de origem.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-120">SourceChanged dispatches after the Source property changes.</span></span>
[<span data-ttu-id="ec3ea-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="ec3ea-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="ec3ea-122">WebMessageReceived despachos após conteúdo da Web envia uma mensagem para o host do aplicativo via `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ec3ea-122">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="ec3ea-123">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="ec3ea-123">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="ec3ea-124">O CoreWebView2 subjacente.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-124">The underlying CoreWebView2.</span></span>
[<span data-ttu-id="ec3ea-125">Origem</span><span class="sxs-lookup"><span data-stu-id="ec3ea-125">Source</span></span>](#source) | <span data-ttu-id="ec3ea-126">A propriedade Source é o URI do documento de nível superior do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-126">The Source property is the URI of the top level document of the WebView2.</span></span>
[<span data-ttu-id="ec3ea-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ec3ea-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="ec3ea-128">O fator de zoom para o WebView.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="ec3ea-129">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="ec3ea-129">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="ec3ea-130">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação por meio do método GoBack.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-130">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>
[<span data-ttu-id="ec3ea-131">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="ec3ea-131">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="ec3ea-132">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação por meio do método GoForward.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-132">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>
[<span data-ttu-id="ec3ea-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="ec3ea-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="ec3ea-134">Disparar explicitamente a inicialização do [CoreWebView2](#corewebview2)do controle.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-134">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>
[<span data-ttu-id="ec3ea-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="ec3ea-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="ec3ea-136">Executa o script fornecido no documento de nível superior do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-136">Executes the provided script in the top level document of the WebView2.</span></span>
[<span data-ttu-id="ec3ea-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="ec3ea-137">GoBack</span></span>](#goback) | <span data-ttu-id="ec3ea-138">Navegar para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-138">Navigate to the previous page in navigation history.</span></span>
[<span data-ttu-id="ec3ea-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="ec3ea-139">GoForward</span></span>](#goforward) | <span data-ttu-id="ec3ea-140">Navegar para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-140">Navigate to the next page in navigation history.</span></span>
[<span data-ttu-id="ec3ea-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="ec3ea-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="ec3ea-142">Renderize o HTML fornecido como o documento de nível superior do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-142">Render the provided HTML as the top level document of the WebView2.</span></span>
[<span data-ttu-id="ec3ea-143">Recarregar</span><span class="sxs-lookup"><span data-stu-id="ec3ea-143">Reload</span></span>](#reload) | <span data-ttu-id="ec3ea-144">Recarregue o documento de nível superior da WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-144">Reload the top level document of the WebView2.</span></span>
[<span data-ttu-id="ec3ea-145">Parar</span><span class="sxs-lookup"><span data-stu-id="ec3ea-145">Stop</span></span>](#stop) | <span data-ttu-id="ec3ea-146">Parar a navegação em andamento no WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-146">Stop any in progress navigation in the WebView2.</span></span>
[<span data-ttu-id="ec3ea-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="ec3ea-147">WebView2</span></span>](#webview2) | <span data-ttu-id="ec3ea-148">Crie um novo controle WinForms do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-148">Create a new WebView2 WinForms control.</span></span>

## <span data-ttu-id="ec3ea-149">Parte</span><span class="sxs-lookup"><span data-stu-id="ec3ea-149">Members</span></span>

#### <span data-ttu-id="ec3ea-150">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="ec3ea-150">ContentLoading</span></span> 

<span data-ttu-id="ec3ea-151">ContentLoading despachos quando uma navegação começa a ser um novo URI e o conteúdo desse URI começa a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-151">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>

> <span data-ttu-id="ec3ea-152">< do evento público EventHandler CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-152">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="ec3ea-153">Isso equivale ao evento ContentLoading no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-153">This is equivalent to the ContentLoading event on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-154">Consulte a documentação do CoreWebView2. ContentLoading para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-154">See CoreWebView2.ContentLoading documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-155">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="ec3ea-155">CoreWebView2Ready</span></span> 

<span data-ttu-id="ec3ea-156">Esse evento é acionado quando o [CoreWebView2](#corewebview2) do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-156">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="ec3ea-157">evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-157">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="ec3ea-158">Você deve tratar esse evento se precisar executar operações de configuração únicas no CoreWebView2 que você deseja afetar todos os seus usos (por exemplo, adicionar manipuladores de eventos, definir configurações, instalar scripts de criação de documentos, adicionar objetos host).</span><span class="sxs-lookup"><span data-stu-id="ec3ea-158">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span>

<span data-ttu-id="ec3ea-159">Esse evento não fornece argumentos, e o remetente será o controle WebView2, cuja propriedade CoreWebView2 agora será válida (ou seja, não nula) pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-159">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="ec3ea-160">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="ec3ea-160">NavigationCompleted</span></span> 

<span data-ttu-id="ec3ea-161">O NavigationCompleted despacha após uma navegação do documento de nível superior executa a renderização com êxito ou não.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-161">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>

> <span data-ttu-id="ec3ea-162">< do evento público EventHandler CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-162">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="ec3ea-163">Isso equivale ao evento NavigationCompleted no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-163">This is equivalent to the NavigationCompleted event on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-164">Consulte a documentação do CoreWebView2. NavigationCompleted para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-164">See CoreWebView2.NavigationCompleted documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-165">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="ec3ea-165">NavigationStarting</span></span> 

<span data-ttu-id="ec3ea-166">O NavigationStarting despacha antes de uma nova navegação começar para o documento de nível superior do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-166">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>

> <span data-ttu-id="ec3ea-167">< do evento público EventHandler CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-167">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="ec3ea-168">Isso equivale ao evento NavigationStarting no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-168">This is equivalent to the NavigationStarting event on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-169">Consulte a documentação do CoreWebView2. NavigationStarting para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-169">See CoreWebView2.NavigationStarting documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-170">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="ec3ea-170">SourceChanged</span></span> 

<span data-ttu-id="ec3ea-171">Os despachos SourceChanged após a alteração da propriedade de origem.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-171">SourceChanged dispatches after the Source property changes.</span></span>

> <span data-ttu-id="ec3ea-172">evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-172">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="ec3ea-173">Isso pode ocorrer durante uma navegação ou, caso contrário, o script na página alterará o URI do documento.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-173">This may happen during a navigation or if otherwise the script in the page changes the URI of the document.</span></span> <span data-ttu-id="ec3ea-174">Isso equivale ao evento SourceChanged no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-174">This is equivalent to the SourceChanged event on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-175">Consulte documentação da CoreWebView2. SourceChanged para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-175">See CoreWebView2.SourceChanged documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-176">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="ec3ea-176">WebMessageReceived</span></span> 

<span data-ttu-id="ec3ea-177">WebMessageReceived despachos após conteúdo da Web envia uma mensagem para o host do aplicativo via `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ec3ea-177">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="ec3ea-178">< do evento público EventHandler CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-178">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="ec3ea-179">Isso equivale ao evento WebMessageReceived no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-179">This is equivalent to the WebMessageReceived event on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-180">Consulte a documentação do CoreWebView2. WebMessageReceived para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-180">See CoreWebView2.WebMessageReceived documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-181">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="ec3ea-181">CoreWebView2</span></span> 

<span data-ttu-id="ec3ea-182">O CoreWebView2 subjacente.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-182">The underlying CoreWebView2.</span></span>

> <span data-ttu-id="ec3ea-183">CoreWebView2 público [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-183">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="ec3ea-184">Use essa propriedade para executar mais operações no conteúdo do WebView2 do que é exposto no WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-184">Use this property to perform more operations on the WebView2 content than is exposed on the WebView2.</span></span> <span data-ttu-id="ec3ea-185">Esse valor é nulo até ser inicializado.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-185">This value is null until it is initialized.</span></span> <span data-ttu-id="ec3ea-186">Você pode forçar o CoreWebView2 subjacente a inicializar por meio do método InitializeAsync.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-186">You can force the underlying CoreWebView2 to initialize via the InitializeAsync method.</span></span>

#### <span data-ttu-id="ec3ea-187">Origem</span><span class="sxs-lookup"><span data-stu-id="ec3ea-187">Source</span></span> 

<span data-ttu-id="ec3ea-188">A propriedade Source é o URI do documento de nível superior do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-188">The Source property is the URI of the top level document of the WebView2.</span></span>

> <span data-ttu-id="ec3ea-189">[fonte](#source) de URI público</span><span class="sxs-lookup"><span data-stu-id="ec3ea-189">public Uri [Source](#source)</span></span>

<span data-ttu-id="ec3ea-190">A configuração da fonte equivale a chamar CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-190">Setting the Source is equivalent to calling CoreWebView2.Navigate.</span></span> <span data-ttu-id="ec3ea-191">Se a CoreWebView2 subjacente ainda não tiver sido inicializada, essa propriedade será "About: blank".</span><span class="sxs-lookup"><span data-stu-id="ec3ea-191">If the underlying CoreWebView2 is not yet initialized, this property is "about:blank".</span></span> <span data-ttu-id="ec3ea-192">Se a propriedade estiver definida como um URI não absoluto ou nulo, a propriedade permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-192">If the property is set to a non-absolute URI or null, the property remains unchanged.</span></span> <span data-ttu-id="ec3ea-193">Consulte CoreWebView2. Navegue na documentação para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-193">See CoreWebView2.Navigate documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-194">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ec3ea-194">ZoomFactor</span></span> 

<span data-ttu-id="ec3ea-195">O fator de zoom para o WebView.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-195">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="ec3ea-196">[ZoomFactors](#zoomfactor) duplos públicos</span><span class="sxs-lookup"><span data-stu-id="ec3ea-196">public double [ZoomFactor](#zoomfactor)</span></span>

#### <span data-ttu-id="ec3ea-197">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="ec3ea-197">CanGoBack</span></span> 

<span data-ttu-id="ec3ea-198">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação por meio do método GoBack.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-198">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>

> <span data-ttu-id="ec3ea-199">bool público [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-199">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="ec3ea-200">Isso equivale à propriedade CanGoBack no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-200">This is equivalent to the CanGoBack property on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-201">Se a CoreWebView2 subjacente ainda não tiver sido inicializada, essa propriedade será falsa.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-201">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="ec3ea-202">Consulte a documentação do CoreWebView2. CanGoBack para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-202">See CoreWebView2.CanGoBack documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-203">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="ec3ea-203">CanGoForward</span></span> 

<span data-ttu-id="ec3ea-204">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação por meio do método GoForward.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-204">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>

> <span data-ttu-id="ec3ea-205">Public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-205">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="ec3ea-206">Isso equivale à propriedade CanGoForward no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-206">This is equivalent to the CanGoForward property on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-207">Se a CoreWebView2 subjacente ainda não tiver sido inicializada, essa propriedade será falsa.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-207">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="ec3ea-208">Consulte a documentação do CoreWebView2. CanGoForward para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-208">See CoreWebView2.CanGoForward documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-209">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="ec3ea-209">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="ec3ea-210">Disparar explicitamente a inicialização do [CoreWebView2](#corewebview2)do controle.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-210">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>

> <span data-ttu-id="ec3ea-211">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tarefas públicas (ambiente CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-211">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

##### <span data-ttu-id="ec3ea-212">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec3ea-212">Parameters</span></span>
* `environment` <span data-ttu-id="ec3ea-213">Um CoreWebView2Environment pré-criado que deve ser usado para criar o CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-213">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-214">Criar seu próprio ambiente permite que você controle várias opções que afetam como a CoreWebView2 é inicializada.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-214">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="ec3ea-215">Se você passar NULL (o valor padrão), um ambiente padrão será criado e usado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-215">If you pass null (the default value) then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="ec3ea-216">Devolver</span><span class="sxs-lookup"><span data-stu-id="ec3ea-216">Returns</span></span>
<span data-ttu-id="ec3ea-217">Uma tarefa que representa o processo de inicialização em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-217">A Task that represents the background initialization process.</span></span> <span data-ttu-id="ec3ea-218">Quando a tarefa for concluída, a propriedade CoreWebView2 estará disponível para uso (ou seja, não nulo).</span><span class="sxs-lookup"><span data-stu-id="ec3ea-218">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="ec3ea-219">Observe que o evento [CoreWebView2Ready](#corewebview2ready) do controle será invocado antes da conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-219">Note that the control's [CoreWebView2Ready](#corewebview2ready) event will be invoked before the task completes.</span></span> 

<span data-ttu-id="ec3ea-220">Chamar esse método momentos adicionais não terão efeito (qualquer ambiente especificado será ignorado) e retornará a mesma tarefa que a primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-220">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="ec3ea-221">Chamar esse método após a inicialização foi disparada implicitamente, definindo a propriedade [Source](#source) não terá nenhum efeito (qualquer ambiente especificado é ignorado) e simplesmente retornar uma tarefa representando essa inicialização já em andamento.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-221">Calling this method after initialization has been implicitly triggered by setting the [Source](#source) property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> 

##### <span data-ttu-id="ec3ea-222">Exceções</span><span class="sxs-lookup"><span data-stu-id="ec3ea-222">Exceptions</span></span>
* `System.InvalidOperationException` <span data-ttu-id="ec3ea-223">Lançada quando invocada do thread que não é da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-223">Thrown when invoked from non-UI thread.</span></span>

#### <span data-ttu-id="ec3ea-224">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="ec3ea-224">ExecuteScriptAsync</span></span> 

<span data-ttu-id="ec3ea-225">Executa o script fornecido no documento de nível superior do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-225">Executes the provided script in the top level document of the WebView2.</span></span>

> <span data-ttu-id="ec3ea-226">Cadeia de caracteres de< de tarefa assíncrona pública > [ExecuteScriptAsync](#executescriptasync)(script de cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-226">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string script)</span></span>

<span data-ttu-id="ec3ea-227">Isso equivale ao método ExecuteScriptAsync no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-227">This is equivalent to the ExecuteScriptAsync method on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-228">Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método lançará um InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-228">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="ec3ea-229">Consulte CoreWebView2.Exedocumentação do cuteScriptAsync para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-229">See CoreWebView2.ExecuteScriptAsync documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-230">GoBack</span><span class="sxs-lookup"><span data-stu-id="ec3ea-230">GoBack</span></span> 

<span data-ttu-id="ec3ea-231">Navegar para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-231">Navigate to the previous page in navigation history.</span></span>

> <span data-ttu-id="ec3ea-232">public void [(](#goback)) public void</span><span class="sxs-lookup"><span data-stu-id="ec3ea-232">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="ec3ea-233">Isso equivale ao método GoBack no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-233">This is equivalent to the GoBack method on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-234">Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método não fará nada.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-234">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="ec3ea-235">Consulte a documentação do CoreWebView2. GoBack para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-235">See CoreWebView2.GoBack documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-236">GoForward</span><span class="sxs-lookup"><span data-stu-id="ec3ea-236">GoForward</span></span> 

<span data-ttu-id="ec3ea-237">Navegar para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-237">Navigate to the next page in navigation history.</span></span>

> <span data-ttu-id="ec3ea-238">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="ec3ea-238">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="ec3ea-239">Isso equivale ao método GoForward no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-239">This is equivalent to the GoForward method on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-240">Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método não fará nada.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-240">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="ec3ea-241">Consulte a documentação do CoreWebView2. GoForward para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-241">See CoreWebView2.GoForward documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-242">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="ec3ea-242">NavigateToString</span></span> 

<span data-ttu-id="ec3ea-243">Renderize o HTML fornecido como o documento de nível superior do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-243">Render the provided HTML as the top level document of the WebView2.</span></span>

> <span data-ttu-id="ec3ea-244">public void [NavigateToString](#navigatetostring)(cadeia de caracteres htmlContent)</span><span class="sxs-lookup"><span data-stu-id="ec3ea-244">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="ec3ea-245">Isso equivale ao método NavigateToString no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-245">This is equivalent to the NavigateToString method on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-246">Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método lançará um InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-246">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="ec3ea-247">Consulte a documentação do CoreWebView2. NavigateToString para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-247">See CoreWebView2.NavigateToString documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-248">Recarregar</span><span class="sxs-lookup"><span data-stu-id="ec3ea-248">Reload</span></span> 

<span data-ttu-id="ec3ea-249">Recarregue o documento de nível superior da WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-249">Reload the top level document of the WebView2.</span></span>

> <span data-ttu-id="ec3ea-250">recarregamento [Reload](#reload)nulo público ()</span><span class="sxs-lookup"><span data-stu-id="ec3ea-250">public void [Reload](#reload)()</span></span>

<span data-ttu-id="ec3ea-251">Isso equivale ao método reload no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-251">This is equivalent to the Reload method on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-252">Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método lançará um InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-252">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="ec3ea-253">Consulte CoreWebView2. recarregue a documentação para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-253">See CoreWebView2.Reload documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-254">Parar</span><span class="sxs-lookup"><span data-stu-id="ec3ea-254">Stop</span></span> 

<span data-ttu-id="ec3ea-255">Parar a navegação em andamento no WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-255">Stop any in progress navigation in the WebView2.</span></span>

> <span data-ttu-id="ec3ea-256">[Stop](#stop)void Public ()</span><span class="sxs-lookup"><span data-stu-id="ec3ea-256">public void [Stop](#stop)()</span></span>

<span data-ttu-id="ec3ea-257">Isso equivale ao método Stop no CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-257">This is equivalent to the Stop method on the CoreWebView2.</span></span> <span data-ttu-id="ec3ea-258">Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método não fará nada.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-258">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="ec3ea-259">Consulte CoreWebView2. pare a documentação para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-259">See CoreWebView2.Stop documentation for more information.</span></span>

#### <span data-ttu-id="ec3ea-260">WebView2</span><span class="sxs-lookup"><span data-stu-id="ec3ea-260">WebView2</span></span> 

<span data-ttu-id="ec3ea-261">Crie um novo controle WinForms do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-261">Create a new WebView2 WinForms control.</span></span>

> <span data-ttu-id="ec3ea-262">[WebView2](#webview2)público ()</span><span class="sxs-lookup"><span data-stu-id="ec3ea-262">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="ec3ea-263">Após a construção, a propriedade CoreWebView2 é NULL.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-263">After construction the CoreWebView2 property is null.</span></span> <span data-ttu-id="ec3ea-264">Chame [EnsureCoreWebView2Async](#ensurecorewebview2async) para inicializar o CoreWebView2 subjacente.</span><span class="sxs-lookup"><span data-stu-id="ec3ea-264">Call [EnsureCoreWebView2Async](#ensurecorewebview2async) to initialize the underlying CoreWebView2.</span></span>

