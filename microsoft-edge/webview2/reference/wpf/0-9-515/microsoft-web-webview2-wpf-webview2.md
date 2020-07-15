---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. WPF. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. WPF. WebView2
ms.openlocfilehash: 2dd7bf1035cf5254f4668070d56d2bd2405f1276
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880259"
---
# <span data-ttu-id="b4cf9-104">Classe Microsoft. Web. WebView2. WPF. WebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="b4cf9-105">Namespace: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="b4cf9-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="b4cf9-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="b4cf9-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="b4cf9-107">Um controle para inserir conteúdo da Web em um aplicativo WPF.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="b4cf9-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b4cf9-108">Summary</span></span>

 <span data-ttu-id="b4cf9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b4cf9-109">Members</span></span>                        | <span data-ttu-id="b4cf9-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="b4cf9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b4cf9-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="b4cf9-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="b4cf9-112">Um wrapper em torno do evento CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="b4cf9-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="b4cf9-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="b4cf9-114">Esse evento é acionado quando o CoreWebView2 do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="b4cf9-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="b4cf9-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="b4cf9-116">Um wrapper em torno do evento CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="b4cf9-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b4cf9-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="b4cf9-118">Um wrapper em torno do evento CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="b4cf9-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="b4cf9-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="b4cf9-120">Um wrapper em torno do evento CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="b4cf9-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="b4cf9-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="b4cf9-122">Um wrapper em torno do evento CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="b4cf9-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="b4cf9-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="b4cf9-124">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="b4cf9-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="b4cf9-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="b4cf9-126">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="b4cf9-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="b4cf9-128">Acesse a funcionalidade completa da API Core. CoreWebView2 COM subjacente.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="b4cf9-129">Creationproperties</span><span class="sxs-lookup"><span data-stu-id="b4cf9-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="b4cf9-130">Obtém ou define um conjunto de opções que são usadas durante a inicialização do CoreWebView2 do controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="b4cf9-131">Origem</span><span class="sxs-lookup"><span data-stu-id="b4cf9-131">Source</span></span>](#source) | <span data-ttu-id="b4cf9-132">O URI de nível superior que o WebView está exibindo no momento (ou será exibido quando a inicialização de seu CoreWebView2 estiver concluída).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="b4cf9-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="b4cf9-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="b4cf9-134">Disparar explicitamente a inicialização do CoreWebView2 do controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="b4cf9-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="b4cf9-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="b4cf9-136">Executa o código JavaScript do parâmetro javaScript no documento de nível superior atual renderizado no WebView.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="b4cf9-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="b4cf9-137">GoBack</span></span>](#goback) | <span data-ttu-id="b4cf9-138">Navega o WebView para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="b4cf9-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="b4cf9-139">GoForward</span></span>](#goforward) | <span data-ttu-id="b4cf9-140">Navega o WebView para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="b4cf9-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="b4cf9-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="b4cf9-142">Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="b4cf9-143">Recarregar</span><span class="sxs-lookup"><span data-stu-id="b4cf9-143">Reload</span></span>](#reload) | <span data-ttu-id="b4cf9-144">Recarrega a página atual.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-144">Reloads the current page.</span></span>
[<span data-ttu-id="b4cf9-145">Parar</span><span class="sxs-lookup"><span data-stu-id="b4cf9-145">Stop</span></span>](#stop) | <span data-ttu-id="b4cf9-146">Interrompe todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="b4cf9-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-147">WebView2</span></span>](#webview2) | <span data-ttu-id="b4cf9-148">Cria uma nova instância de um controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-148">Creates a new instance of a WebView2 control.</span></span>

<span data-ttu-id="b4cf9-149">Esse controle é efetivamente um wrapper em torno da API COM WebView2, à qual você pode encontrar a documentação aqui: [https://aka.ms/webview2](https://aka.ms/webview2) você pode acessar diretamente a interface ICoreWebView2 subjacente e todas as suas funcionalidades acessando a propriedade CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-149">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="b4cf9-150">Alguns dos recursos COM mais comuns também podem ser acessados diretamente por meio de métodos/Propriedades/eventos de wrapper no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-150">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="b4cf9-151">Após a criação, a propriedade CoreWebView2 do controle será nula.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-151">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="b4cf9-152">Isso ocorre porque a criação do CoreWebView2 é uma operação cara que envolve itens como iniciar processos do navegador Edge.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-152">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="b4cf9-153">Há duas maneiras de fazer com que o CoreWebView2 seja criado: 1) chame o método EnsureCoreWebView2Async.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-153">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="b4cf9-154">Isso é conhecido como inicialização explícita.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-154">This is referred to as explicit initialization.</span></span> <span data-ttu-id="b4cf9-155">2) defina a propriedade Source (que pode ser feita a partir de marcações, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-155">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="b4cf9-156">Isso é conhecido como inicialização implícita.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-156">This is referred to as implicit initialization.</span></span> <span data-ttu-id="b4cf9-157">Qualquer uma das opções iniciará a inicialização em segundo plano e retornará para o chamador sem esperar que ele seja concluído.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-157">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="b4cf9-158">Para especificar as opções em relação ao processo de inicialização, passe seu próprio CoreWebView2Environment para EnsureCoreWebView2Async ou defina a propriedade Creationproperties do controle antes da inicialização.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-158">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="b4cf9-159">Quando a inicialização terminar (independentemente de como foi disparada), os seguintes itens ocorrerão, nesta ordem: 1) o evento CoreWebView2Ready do controle será invocado.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-159">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="b4cf9-160">Se você precisar executar operações de configuração únicas no CoreWebView2 antes de seu uso, você deve fazer isso em um manipulador para esse evento.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-160">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="b4cf9-161">2) se um URI tiver sido definido como a propriedade de origem, o controle começará a navegar para ele em segundo plano (isto é, essas etapas continuarão sem esperar a conclusão da navegação).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-161">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="b4cf9-162">3) a tarefa retornada de EnsureCoreWebView2Async será concluída.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-162">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="b4cf9-163">Para obter mais detalhes sobre qualquer um dos métodos/Propriedades/eventos envolvidos no processo de inicialização, consulte a documentação específica.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-163">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="b4cf9-164">Como o CoreWebView2 do controle é um objeto muito pesado (possivelmente responsável por vários processos em execução e megabytes de espaço em disco), o controle implementa IDisposable para fornecer um meio explícito para liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-164">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="b4cf9-165">Chamar Dispose vai liberar o CoreWebView2 e seus recursos subjacentes (exceto os que também estão sendo usados por outras exibições) e redefinir CoreWebView2 como NULL.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-165">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="b4cf9-166">Após Dispose ter sido chamado, o CoreWebView2 não pode ser reinicializado e qualquer tentativa de usar a funcionalidade que o exige será gerar um ObjectDisposedException.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-166">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="b4cf9-167">Observe que esse controle estende HwndHost para inserir janelas que residem fora do ecossistema do WPF.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-167">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="b4cf9-168">Isso tem algumas implicações em relação ao comportamento de entrada e saída do controle, bem como a funcionalidade que "herda" de UIElement e FrameworkElement.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-168">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="b4cf9-169">Consulte a documentação de interoperabilidade do HwndHost e do WPF/Win32 para obter mais informações:</span><span class="sxs-lookup"><span data-stu-id="b4cf9-169">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="b4cf9-170">Parte</span><span class="sxs-lookup"><span data-stu-id="b4cf9-170">Members</span></span>

#### <span data-ttu-id="b4cf9-171">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="b4cf9-171">ContentLoading</span></span> 

<span data-ttu-id="b4cf9-172">Um wrapper em torno do evento CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-172">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="b4cf9-173">< do evento público EventHandler CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-173">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="b4cf9-174">A única diferença entre esse evento e CoreWebView2. ContentLoading é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-174">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="b4cf9-175">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. ContentLoading receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-175">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="b4cf9-176">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="b4cf9-176">CoreWebView2Ready</span></span> 

<span data-ttu-id="b4cf9-177">Esse evento é acionado quando o CoreWebView2 do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-177">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="b4cf9-178">evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-178">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="b4cf9-179">Você deve tratar esse evento se precisar executar operações de configuração únicas no CoreWebView2 que você deseja afetar todos os seus usos (por exemplo, adicionar manipuladores de eventos, definir configurações, instalar scripts de criação de documentos, adicionar objetos host).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-179">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="b4cf9-180">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-180">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="b4cf9-181">Esse evento não fornece argumentos, e o remetente será o controle WebView2, cuja propriedade CoreWebView2 agora será válida (ou seja, não nula) pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-181">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="b4cf9-182">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="b4cf9-182">NavigationCompleted</span></span> 

<span data-ttu-id="b4cf9-183">Um wrapper em torno do evento CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-183">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="b4cf9-184">< do evento público EventHandler CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-184">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="b4cf9-185">A única diferença entre esse evento e CoreWebView2. NavigationCompleted é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-185">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="b4cf9-186">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. NavigationCompleted receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-186">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="b4cf9-187">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b4cf9-187">NavigationStarting</span></span> 

<span data-ttu-id="b4cf9-188">Um wrapper em torno do evento CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-188">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="b4cf9-189">< do evento público EventHandler CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-189">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="b4cf9-190">A única diferença entre esse evento e CoreWebView2. NavigationStarting é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-190">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="b4cf9-191">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. NavigationStarting receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-191">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="b4cf9-192">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="b4cf9-192">SourceChanged</span></span> 

<span data-ttu-id="b4cf9-193">Um wrapper em torno do evento CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-193">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="b4cf9-194">evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-194">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="b4cf9-195">A única diferença entre esse evento e CoreWebView2. SourceChanged é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-195">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="b4cf9-196">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. SourceChanged receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-196">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="b4cf9-197">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="b4cf9-197">WebMessageReceived</span></span> 

<span data-ttu-id="b4cf9-198">Um wrapper em torno do evento CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-198">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="b4cf9-199">< do evento público EventHandler CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-199">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="b4cf9-200">A única diferença entre esse evento e CoreWebView2. WebMessageReceived é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-200">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="b4cf9-201">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. WebMessageReceived receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-201">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="b4cf9-202">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="b4cf9-202">CanGoBack</span></span> 

<span data-ttu-id="b4cf9-203">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-203">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="b4cf9-204">bool público [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-204">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="b4cf9-205">Wrapper em torno da propriedade CoreWebView2. CanGoBack de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-205">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="b4cf9-206">Se CoreWebView2 ainda não for inicializado, retornará false.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-206">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="b4cf9-207">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="b4cf9-207">CanGoForward</span></span> 

<span data-ttu-id="b4cf9-208">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-208">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="b4cf9-209">Public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-209">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="b4cf9-210">Wrapper ao meio da propriedade CoreWebView2. CanGoForward de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-210">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="b4cf9-211">Se CoreWebView2 ainda não for inicializado, retornará false.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-211">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="b4cf9-212">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-212">CoreWebView2</span></span> 

<span data-ttu-id="b4cf9-213">Acesse a funcionalidade completa da API Core. CoreWebView2 COM subjacente.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-213">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="b4cf9-214">CoreWebView2 público [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-214">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="b4cf9-215">Retorna NULL até que a inicialização seja concluída.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-215">Returns null until initialization has completed.</span></span> <span data-ttu-id="b4cf9-216">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-216">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="b4cf9-217">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-217">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="b4cf9-218">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-218">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="b4cf9-219">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-219">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="b4cf9-220">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-220">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-221">Creationproperties</span><span class="sxs-lookup"><span data-stu-id="b4cf9-221">CreationProperties</span></span> 

<span data-ttu-id="b4cf9-222">Obtém ou define um conjunto de opções que são usadas durante a inicialização do CoreWebView2 do controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-222">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="b4cf9-223">[criação](#creationproperties) de CoreWebView2CreationProperties público</span><span class="sxs-lookup"><span data-stu-id="b4cf9-223">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="b4cf9-224">A configuração dessa propriedade não funcionará depois que a inicialização do CoreWebView2 do controle tiver começado (o valor antigo será mantido).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-224">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="b4cf9-225">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-225">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="b4cf9-226">Origem</span><span class="sxs-lookup"><span data-stu-id="b4cf9-226">Source</span></span> 

<span data-ttu-id="b4cf9-227">O URI de nível superior que o WebView está exibindo no momento (ou será exibido quando a inicialização de seu CoreWebView2 estiver concluída).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-227">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="b4cf9-228">[fonte](#source) de URI público</span><span class="sxs-lookup"><span data-stu-id="b4cf9-228">public Uri [Source](#source)</span></span>

<span data-ttu-id="b4cf9-229">Em geral, obter essa propriedade equivale a obter a propriedade CoreWebView2. Source de CoreWebView2 e definir essa propriedade equivale a chamar o método CoreWebView2. Navigate em CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-229">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="b4cf9-230">Obter essa propriedade antes da inicialização do CoreWebView2 será recuperar o último URI que estava definido.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-230">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="b4cf9-231">A configuração dessa propriedade antes da inicialização do CoreWebView2 fará com que a inicialização comece em segundo plano (se ainda não estiver em andamento), após a qual o WebView2 navegará até o URI especificado.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-231">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="b4cf9-232">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-232">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="b4cf9-233">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-233">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="b4cf9-234">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-234">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-235">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="b4cf9-235">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="b4cf9-236">Disparar explicitamente a inicialização do CoreWebView2 do controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-236">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="b4cf9-237">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tarefas públicas (ambiente CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-237">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="b4cf9-238">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-238">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="b4cf9-239">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4cf9-239">Parameters</span></span>
* `environment` <span data-ttu-id="b4cf9-240">Um CoreWebView2Environment pré-criado que deve ser usado para criar o CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-240">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="b4cf9-241">Criar seu próprio ambiente permite que você controle várias opções que afetam como a CoreWebView2 é inicializada.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-241">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="b4cf9-242">Se você passar um ambiente para esse método, ele substituirá as configurações especificadas na propriedade Creationproperties.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-242">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="b4cf9-243">Se você passar NULL (o valor padrão) e nenhum valor tiver sido definido como Creationproperties, um ambiente padrão será criado e usado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-243">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="b4cf9-244">Devolver</span><span class="sxs-lookup"><span data-stu-id="b4cf9-244">Returns</span></span>
<span data-ttu-id="b4cf9-245">Uma tarefa que representa o processo de inicialização em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-245">A Task that represents the background initialization process.</span></span> <span data-ttu-id="b4cf9-246">Quando a tarefa for concluída, a propriedade CoreWebView2 estará disponível para uso (ou seja, não nulo).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-246">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="b4cf9-247">Observe que o evento CoreWebView2Ready do controle será invocado antes da conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-247">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="b4cf9-248">Chamar esse método momentos adicionais não terão efeito (qualquer ambiente especificado será ignorado) e retornará a mesma tarefa que a primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-248">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="b4cf9-249">Chamar esse método após a inicialização foi disparada implicitamente, definindo a propriedade Source não terá nenhum efeito (qualquer ambiente especificado é ignorado) e simplesmente retornar uma tarefa representando essa inicialização já em andamento.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-249">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="b4cf9-250">Observe que, embora esse método seja assíncrono e retorne uma tarefa, ele ainda deve ser chamado no thread da interface do usuário, como a maioria das funcionalidades públicas da maioria dos controles da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-250">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="b4cf9-251">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-251">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="b4cf9-252">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-252">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="b4cf9-253">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-253">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="b4cf9-254">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-255">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="b4cf9-255">ExecuteScriptAsync</span></span> 

<span data-ttu-id="b4cf9-256">Executa o código JavaScript do parâmetro javaScript no documento de nível superior atual renderizado no WebView.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-256">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="b4cf9-257">Cadeia de caracteres de< de tarefas assíncronas pública > [ExecuteScriptAsync](#executescriptasync)(cadeia de caracteres JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-257">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="b4cf9-258">Equivalente a chamadas CoreWebView2.ExecuteScriptAsync no CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-258">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="b4cf9-259">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-259">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="b4cf9-260">Gerado se CoreWebView2 ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-260">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="b4cf9-261">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-261">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="b4cf9-262">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-262">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="b4cf9-263">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-263">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-264">GoBack</span><span class="sxs-lookup"><span data-stu-id="b4cf9-264">GoBack</span></span> 

<span data-ttu-id="b4cf9-265">Navega o WebView para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-265">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="b4cf9-266">public void [(](#goback)) public void</span><span class="sxs-lookup"><span data-stu-id="b4cf9-266">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="b4cf9-267">Equivalente a chamar CoreWebView2. GoBack no CoreWebView2 se CoreWebView2 ainda não tiver sido inicializado, não fará nada.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-267">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="b4cf9-268">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-268">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="b4cf9-269">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-269">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="b4cf9-270">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-270">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="b4cf9-271">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-271">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-272">GoForward</span><span class="sxs-lookup"><span data-stu-id="b4cf9-272">GoForward</span></span> 

<span data-ttu-id="b4cf9-273">Navega o WebView para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-273">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="b4cf9-274">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="b4cf9-274">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="b4cf9-275">Equivalente a chamar CoreWebView2. GoForward em CoreWebView2 se CoreWebView2 ainda não foi inicializado, não faz nada.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-275">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="b4cf9-276">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-276">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="b4cf9-277">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-277">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="b4cf9-278">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-278">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="b4cf9-279">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-279">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-280">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="b4cf9-280">NavigateToString</span></span> 

<span data-ttu-id="b4cf9-281">Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-281">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="b4cf9-282">public void [NavigateToString](#navigatetostring)(cadeia de caracteres htmlContent)</span><span class="sxs-lookup"><span data-stu-id="b4cf9-282">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="b4cf9-283">Equivalente a chamar CoreWebView2. NavigateToString no CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-283">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="b4cf9-284">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-284">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="b4cf9-285">Gerado se CoreWebView2 ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-285">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="b4cf9-286">" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-286">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="b4cf9-287">Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-287">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-288">Recarregar</span><span class="sxs-lookup"><span data-stu-id="b4cf9-288">Reload</span></span> 

<span data-ttu-id="b4cf9-289">Recarrega a página atual.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-289">Reloads the current page.</span></span>

> <span data-ttu-id="b4cf9-290">recarregamento [Reload](#reload)nulo público ()</span><span class="sxs-lookup"><span data-stu-id="b4cf9-290">public void [Reload](#reload)()</span></span>

<span data-ttu-id="b4cf9-291">Equivalente a chamar CoreWebView2. reload no CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-291">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="b4cf9-292">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-292">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="b4cf9-293">Gerado se CoreWebView2 ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-293">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="b4cf9-294">" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-294">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="b4cf9-295">Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-295">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-296">Parar</span><span class="sxs-lookup"><span data-stu-id="b4cf9-296">Stop</span></span> 

<span data-ttu-id="b4cf9-297">Interrompe todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-297">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="b4cf9-298">[Stop](#stop)void Public ()</span><span class="sxs-lookup"><span data-stu-id="b4cf9-298">public void [Stop](#stop)()</span></span>

<span data-ttu-id="b4cf9-299">Equivalente a chamar CoreWebView2. Stop no CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-299">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="b4cf9-300">Exceções</span><span class="sxs-lookup"><span data-stu-id="b4cf9-300">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="b4cf9-301">Gerado se CoreWebView2 ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-301">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="b4cf9-302">" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="b4cf9-302">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="b4cf9-303">Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-303">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="b4cf9-304">WebView2</span><span class="sxs-lookup"><span data-stu-id="b4cf9-304">WebView2</span></span> 

<span data-ttu-id="b4cf9-305">Cria uma nova instância de um controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-305">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="b4cf9-306">[WebView2](#webview2)público ()</span><span class="sxs-lookup"><span data-stu-id="b4cf9-306">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="b4cf9-307">Observe que o CoreWebView2 do controle será nulo até ser inicializado.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-307">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="b4cf9-308">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b4cf9-308">See the WebView2 class documentation for an initialization overview.</span></span>

