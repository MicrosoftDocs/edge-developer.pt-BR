---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: f2c3bcb5334abc907a838971ebc1773b6485194f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652425"
---
# <span data-ttu-id="39b5d-104">Classe Microsoft. Web. WebView2. WPF. WebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="39b5d-105">Namespace: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="39b5d-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="39b5d-106">Assembly: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="39b5d-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="39b5d-107">Um controle para inserir conteúdo da Web em um aplicativo WPF.</span><span class="sxs-lookup"><span data-stu-id="39b5d-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="39b5d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="39b5d-108">Summary</span></span>

 <span data-ttu-id="39b5d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="39b5d-109">Members</span></span>                        | <span data-ttu-id="39b5d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="39b5d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="39b5d-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="39b5d-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="39b5d-112">Um wrapper em torno do evento CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="39b5d-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="39b5d-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="39b5d-114">Esse evento é acionado quando o CoreWebView2 do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="39b5d-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="39b5d-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="39b5d-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="39b5d-116">Um wrapper em torno do evento CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="39b5d-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="39b5d-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="39b5d-118">Um wrapper em torno do evento CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="39b5d-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="39b5d-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="39b5d-120">Um wrapper em torno do evento CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="39b5d-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="39b5d-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="39b5d-122">Um wrapper em torno do evento CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="39b5d-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="39b5d-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="39b5d-124">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="39b5d-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="39b5d-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="39b5d-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="39b5d-126">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="39b5d-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="39b5d-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="39b5d-128">Acesse a funcionalidade completa da API Core. CoreWebView2 COM subjacente.</span><span class="sxs-lookup"><span data-stu-id="39b5d-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="39b5d-129">Creationproperties</span><span class="sxs-lookup"><span data-stu-id="39b5d-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="39b5d-130">Obtém ou define um conjunto de opções que são usadas durante a inicialização do CoreWebView2 do controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="39b5d-131">Origem</span><span class="sxs-lookup"><span data-stu-id="39b5d-131">Source</span></span>](#source) | <span data-ttu-id="39b5d-132">O URI de nível superior que o WebView está exibindo no momento (ou será exibido quando a inicialização de seu CoreWebView2 estiver concluída).</span><span class="sxs-lookup"><span data-stu-id="39b5d-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="39b5d-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="39b5d-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="39b5d-134">Disparar explicitamente a inicialização do CoreWebView2 do controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="39b5d-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="39b5d-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="39b5d-136">Executa o código JavaScript do parâmetro javaScript no documento de nível superior atual renderizado no WebView.</span><span class="sxs-lookup"><span data-stu-id="39b5d-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="39b5d-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="39b5d-137">GoBack</span></span>](#goback) | <span data-ttu-id="39b5d-138">Navega o WebView para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="39b5d-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="39b5d-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="39b5d-139">GoForward</span></span>](#goforward) | <span data-ttu-id="39b5d-140">Navega o WebView para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="39b5d-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="39b5d-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="39b5d-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="39b5d-142">Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.</span><span class="sxs-lookup"><span data-stu-id="39b5d-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="39b5d-143">Recarregar</span><span class="sxs-lookup"><span data-stu-id="39b5d-143">Reload</span></span>](#reload) | <span data-ttu-id="39b5d-144">Recarrega a página atual.</span><span class="sxs-lookup"><span data-stu-id="39b5d-144">Reloads the current page.</span></span>
[<span data-ttu-id="39b5d-145">Parar</span><span class="sxs-lookup"><span data-stu-id="39b5d-145">Stop</span></span>](#stop) | <span data-ttu-id="39b5d-146">Interrompe todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="39b5d-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="39b5d-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-147">WebView2</span></span>](#webview2) | <span data-ttu-id="39b5d-148">Cria uma nova instância de um controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-148">Creates a new instance of a WebView2 control.</span></span>
[<span data-ttu-id="39b5d-149">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="39b5d-149">BuildWindowCore</span></span>](#buildwindowcore) | <span data-ttu-id="39b5d-150">Isso é substituído em HwndHost e é chamado para nos instruir a criar o HWND.</span><span class="sxs-lookup"><span data-stu-id="39b5d-150">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>
[<span data-ttu-id="39b5d-151">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="39b5d-151">DestroyWindowCore</span></span>](#destroywindowcore) | <span data-ttu-id="39b5d-152">Isso é substituído em HwndHost e é chamado para nos instruir a destruir o HWND.</span><span class="sxs-lookup"><span data-stu-id="39b5d-152">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>
[<span data-ttu-id="39b5d-153">Dispose</span><span class="sxs-lookup"><span data-stu-id="39b5d-153">Dispose</span></span>](#dispose) | <span data-ttu-id="39b5d-154">Isso é chamado pela nossa classe base de acordo com a implementação típica do padrão IDispose.</span><span class="sxs-lookup"><span data-stu-id="39b5d-154">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>
[<span data-ttu-id="39b5d-155">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="39b5d-155">HasFocusWithinCore</span></span>](#hasfocuswithincore) | <span data-ttu-id="39b5d-156">Isso é substituído em HwndHost e é chamado quando o WPF precisa saber se o foco está em nosso controle/janela.</span><span class="sxs-lookup"><span data-stu-id="39b5d-156">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>
[<span data-ttu-id="39b5d-157">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="39b5d-157">OnKeyDown</span></span>](#onkeydown) | <span data-ttu-id="39b5d-158">Isso é substituído pelo UIElement e chamado para permitir que manipulemos a entrada de pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="39b5d-158">This is overridden from UIElement and called to allow us to handle key press input.</span></span>
[<span data-ttu-id="39b5d-159">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="39b5d-159">OnKeyUp</span></span>](#onkeyup) | <span data-ttu-id="39b5d-160">Veja OnKeyDown.</span><span class="sxs-lookup"><span data-stu-id="39b5d-160">See OnKeyDown.</span></span>
[<span data-ttu-id="39b5d-161">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="39b5d-161">OnPreviewKeyDown</span></span>](#onpreviewkeydown) | <span data-ttu-id="39b5d-162">Esta é a "visualização" (por exemplo,</span><span class="sxs-lookup"><span data-stu-id="39b5d-162">This is the "Preview" (i.e.</span></span>
[<span data-ttu-id="39b5d-163">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="39b5d-163">OnPreviewKeyUp</span></span>](#onpreviewkeyup) | <span data-ttu-id="39b5d-164">Consulte OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="39b5d-164">See OnPreviewKeyDown.</span></span>
[<span data-ttu-id="39b5d-165">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="39b5d-165">OnWindowPositionChanged</span></span>](#onwindowpositionchanged) | <span data-ttu-id="39b5d-166">Isso é substituído de HwndHost e chamado quando o local de nosso controle é alterado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-166">This is overridden from HwndHost and called when our control's location has changed.</span></span>
[<span data-ttu-id="39b5d-167">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="39b5d-167">TabIntoCore</span></span>](#tabintocore) | <span data-ttu-id="39b5d-168">Isso é substituído em HwndHost e é chamado para informar que a Tabulação fez com que o foco se mova para o nosso controle/janela.</span><span class="sxs-lookup"><span data-stu-id="39b5d-168">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

<span data-ttu-id="39b5d-169">Esse controle é efetivamente um wrapper em torno da API COM WebView2, à qual você pode encontrar a documentação aqui: [https://aka.ms/webview2](https://aka.ms/webview2) você pode acessar diretamente a interface ICoreWebView2 subjacente e todas as suas funcionalidades acessando a propriedade CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-169">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="39b5d-170">Alguns dos recursos COM mais comuns também podem ser acessados diretamente por meio de métodos/Propriedades/eventos de wrapper no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-170">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="39b5d-171">Após a criação, a propriedade CoreWebView2 do controle será nula.</span><span class="sxs-lookup"><span data-stu-id="39b5d-171">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="39b5d-172">Isso ocorre porque a criação do CoreWebView2 é uma operação cara que envolve itens como iniciar processos do navegador Edge.</span><span class="sxs-lookup"><span data-stu-id="39b5d-172">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="39b5d-173">Há duas maneiras de fazer com que o CoreWebView2 seja criado: 1) chame o método EnsureCoreWebView2Async.</span><span class="sxs-lookup"><span data-stu-id="39b5d-173">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="39b5d-174">Isso é conhecido como inicialização explícita.</span><span class="sxs-lookup"><span data-stu-id="39b5d-174">This is referred to as explicit initialization.</span></span> <span data-ttu-id="39b5d-175">2) defina a propriedade Source (que pode ser feita a partir de marcações, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="39b5d-175">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="39b5d-176">Isso é conhecido como inicialização implícita.</span><span class="sxs-lookup"><span data-stu-id="39b5d-176">This is referred to as implicit initialization.</span></span> <span data-ttu-id="39b5d-177">Qualquer uma das opções iniciará a inicialização em segundo plano e retornará para o chamador sem esperar que ele seja concluído.</span><span class="sxs-lookup"><span data-stu-id="39b5d-177">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="39b5d-178">Para especificar as opções em relação ao processo de inicialização, passe seu próprio CoreWebView2Environment para EnsureCoreWebView2Async ou defina a propriedade Creationproperties do controle antes da inicialização.</span><span class="sxs-lookup"><span data-stu-id="39b5d-178">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="39b5d-179">Quando a inicialização terminar (independentemente de como foi disparada), os seguintes itens ocorrerão, nesta ordem: 1) o evento CoreWebView2Ready do controle será invocado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-179">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="39b5d-180">Se você precisar executar operações de configuração únicas no CoreWebView2 antes de seu uso, você deve fazer isso em um manipulador para esse evento.</span><span class="sxs-lookup"><span data-stu-id="39b5d-180">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="39b5d-181">2) se um URI tiver sido definido como a propriedade de origem, o controle começará a navegar para ele em segundo plano (isto é, essas etapas continuarão sem esperar a conclusão da navegação).</span><span class="sxs-lookup"><span data-stu-id="39b5d-181">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="39b5d-182">3) a tarefa retornada de EnsureCoreWebView2Async será concluída.</span><span class="sxs-lookup"><span data-stu-id="39b5d-182">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="39b5d-183">Para obter mais detalhes sobre qualquer um dos métodos/Propriedades/eventos envolvidos no processo de inicialização, consulte a documentação específica.</span><span class="sxs-lookup"><span data-stu-id="39b5d-183">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="39b5d-184">Como o CoreWebView2 do controle é um objeto muito pesado (possivelmente responsável por vários processos em execução e megabytes de espaço em disco), o controle implementa IDisposable para fornecer um meio explícito para liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="39b5d-184">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="39b5d-185">Chamar Dispose vai liberar o CoreWebView2 e seus recursos subjacentes (exceto os que também estão sendo usados por outras exibições) e redefinir CoreWebView2 como NULL.</span><span class="sxs-lookup"><span data-stu-id="39b5d-185">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="39b5d-186">Após Dispose ter sido chamado, o CoreWebView2 não pode ser reinicializado e qualquer tentativa de usar a funcionalidade que o exige será gerar um ObjectDisposedException.</span><span class="sxs-lookup"><span data-stu-id="39b5d-186">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="39b5d-187">Observe que esse controle estende HwndHost para inserir janelas que residem fora do ecossistema do WPF.</span><span class="sxs-lookup"><span data-stu-id="39b5d-187">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="39b5d-188">Isso tem algumas implicações em relação ao comportamento de entrada e saída do controle, bem como a funcionalidade que "herda" de UIElement e FrameworkElement.</span><span class="sxs-lookup"><span data-stu-id="39b5d-188">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="39b5d-189">Consulte a documentação de interoperabilidade do HwndHost e do WPF/Win32 para obter mais informações:</span><span class="sxs-lookup"><span data-stu-id="39b5d-189">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="39b5d-190">Parte</span><span class="sxs-lookup"><span data-stu-id="39b5d-190">Members</span></span>

#### <span data-ttu-id="39b5d-191">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="39b5d-191">ContentLoading</span></span> 

<span data-ttu-id="39b5d-192">Um wrapper em torno do evento CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-192">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="39b5d-193">< do evento público EventHandler CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="39b5d-193">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="39b5d-194">A única diferença entre esse evento e CoreWebView2. ContentLoading é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="39b5d-194">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="39b5d-195">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. ContentLoading receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-195">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="39b5d-196">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="39b5d-196">CoreWebView2Ready</span></span> 

<span data-ttu-id="39b5d-197">Esse evento é acionado quando o CoreWebView2 do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="39b5d-197">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="39b5d-198">evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="39b5d-198">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="39b5d-199">Você deve tratar esse evento se precisar executar operações de configuração únicas no CoreWebView2 que você deseja afetar todos os seus usos (por exemplo, adicionar manipuladores de eventos, definir configurações, instalar scripts de criação de documentos, adicionar objetos host).</span><span class="sxs-lookup"><span data-stu-id="39b5d-199">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="39b5d-200">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="39b5d-200">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="39b5d-201">Esse evento não fornece argumentos, e o remetente será o controle WebView2, cuja propriedade CoreWebView2 agora será válida (ou seja, não nula) pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="39b5d-201">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="39b5d-202">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="39b5d-202">NavigationCompleted</span></span> 

<span data-ttu-id="39b5d-203">Um wrapper em torno do evento CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-203">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="39b5d-204">< do evento público EventHandler CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="39b5d-204">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="39b5d-205">A única diferença entre esse evento e CoreWebView2. NavigationCompleted é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="39b5d-205">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="39b5d-206">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. NavigationCompleted receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-206">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="39b5d-207">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="39b5d-207">NavigationStarting</span></span> 

<span data-ttu-id="39b5d-208">Um wrapper em torno do evento CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-208">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="39b5d-209">< do evento público EventHandler CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="39b5d-209">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="39b5d-210">A única diferença entre esse evento e CoreWebView2. NavigationStarting é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="39b5d-210">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="39b5d-211">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. NavigationStarting receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-211">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="39b5d-212">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="39b5d-212">SourceChanged</span></span> 

<span data-ttu-id="39b5d-213">Um wrapper em torno do evento CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-213">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="39b5d-214">evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="39b5d-214">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="39b5d-215">A única diferença entre esse evento e CoreWebView2. SourceChanged é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="39b5d-215">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="39b5d-216">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. SourceChanged receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-216">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="39b5d-217">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="39b5d-217">WebMessageReceived</span></span> 

<span data-ttu-id="39b5d-218">Um wrapper em torno do evento CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-218">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="39b5d-219">< do evento público EventHandler CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="39b5d-219">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="39b5d-220">A única diferença entre esse evento e CoreWebView2. WebMessageReceived é o primeiro parâmetro que é passado para manipuladores.</span><span class="sxs-lookup"><span data-stu-id="39b5d-220">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="39b5d-221">Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. WebMessageReceived receberão a instância CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-221">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="39b5d-222">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="39b5d-222">CanGoBack</span></span> 

<span data-ttu-id="39b5d-223">Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="39b5d-223">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="39b5d-224">bool público [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="39b5d-224">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="39b5d-225">Wrapper em torno da propriedade CoreWebView2. CanGoBack de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-225">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="39b5d-226">Se CoreWebView2 ainda não for inicializado, retornará false.</span><span class="sxs-lookup"><span data-stu-id="39b5d-226">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="39b5d-227">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="39b5d-227">CanGoForward</span></span> 

<span data-ttu-id="39b5d-228">Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="39b5d-228">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="39b5d-229">Public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="39b5d-229">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="39b5d-230">Wrapper ao meio da propriedade CoreWebView2. CanGoForward de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-230">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="39b5d-231">Se CoreWebView2 ainda não for inicializado, retornará false.</span><span class="sxs-lookup"><span data-stu-id="39b5d-231">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="39b5d-232">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-232">CoreWebView2</span></span> 

<span data-ttu-id="39b5d-233">Acesse a funcionalidade completa da API Core. CoreWebView2 COM subjacente.</span><span class="sxs-lookup"><span data-stu-id="39b5d-233">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="39b5d-234">CoreWebView2 público [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="39b5d-234">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="39b5d-235">Retorna NULL até que a inicialização seja concluída.</span><span class="sxs-lookup"><span data-stu-id="39b5d-235">Returns null until initialization has completed.</span></span> <span data-ttu-id="39b5d-236">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="39b5d-236">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="39b5d-237">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-237">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="39b5d-238">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="39b5d-238">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="39b5d-239">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="39b5d-239">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="39b5d-240">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-240">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-241">Creationproperties</span><span class="sxs-lookup"><span data-stu-id="39b5d-241">CreationProperties</span></span> 

<span data-ttu-id="39b5d-242">Obtém ou define um conjunto de opções que são usadas durante a inicialização do CoreWebView2 do controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-242">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="39b5d-243">[criação](#creationproperties) de CoreWebView2CreationProperties público</span><span class="sxs-lookup"><span data-stu-id="39b5d-243">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="39b5d-244">A configuração dessa propriedade não funcionará depois que a inicialização do CoreWebView2 do controle tiver começado (o valor antigo será mantido).</span><span class="sxs-lookup"><span data-stu-id="39b5d-244">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="39b5d-245">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="39b5d-245">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="39b5d-246">Origem</span><span class="sxs-lookup"><span data-stu-id="39b5d-246">Source</span></span> 

<span data-ttu-id="39b5d-247">O URI de nível superior que o WebView está exibindo no momento (ou será exibido quando a inicialização de seu CoreWebView2 estiver concluída).</span><span class="sxs-lookup"><span data-stu-id="39b5d-247">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="39b5d-248">[fonte](#source) de URI público</span><span class="sxs-lookup"><span data-stu-id="39b5d-248">public Uri [Source](#source)</span></span>

<span data-ttu-id="39b5d-249">Em geral, obter essa propriedade equivale a obter a propriedade CoreWebView2. Source de CoreWebView2 e definir essa propriedade equivale a chamar o método CoreWebView2. Navigate em CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-249">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="39b5d-250">Obter essa propriedade antes da inicialização do CoreWebView2 será recuperar o último URI que estava definido.</span><span class="sxs-lookup"><span data-stu-id="39b5d-250">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="39b5d-251">A configuração dessa propriedade antes da inicialização do CoreWebView2 fará com que a inicialização comece em segundo plano (se ainda não estiver em andamento), após a qual o WebView2 navegará até o URI especificado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-251">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="39b5d-252">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="39b5d-252">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="39b5d-253">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-253">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="39b5d-254">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-255">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="39b5d-255">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="39b5d-256">Disparar explicitamente a inicialização do CoreWebView2 do controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-256">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="39b5d-257">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tarefas públicas (ambiente CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="39b5d-257">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="39b5d-258">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="39b5d-258">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="39b5d-259">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b5d-259">Parameters</span></span>
* `environment` <span data-ttu-id="39b5d-260">Um CoreWebView2Environment pré-criado que deve ser usado para criar o CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-260">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="39b5d-261">Criar seu próprio ambiente permite que você controle várias opções que afetam como a CoreWebView2 é inicializada.</span><span class="sxs-lookup"><span data-stu-id="39b5d-261">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="39b5d-262">Se você passar um ambiente para esse método, ele substituirá as configurações especificadas na propriedade Creationproperties.</span><span class="sxs-lookup"><span data-stu-id="39b5d-262">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="39b5d-263">Se você passar NULL (o valor padrão) e nenhum valor tiver sido definido como Creationproperties, um ambiente padrão será criado e usado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="39b5d-263">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="39b5d-264">Devolver</span><span class="sxs-lookup"><span data-stu-id="39b5d-264">Returns</span></span>
<span data-ttu-id="39b5d-265">Uma tarefa que representa o processo de inicialização em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="39b5d-265">A Task that represents the background initialization process.</span></span> <span data-ttu-id="39b5d-266">Quando a tarefa for concluída, a propriedade CoreWebView2 estará disponível para uso (ou seja, não nulo).</span><span class="sxs-lookup"><span data-stu-id="39b5d-266">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="39b5d-267">Observe que o evento CoreWebView2Ready do controle será invocado antes da conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="39b5d-267">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="39b5d-268">Chamar esse método momentos adicionais não terão efeito (qualquer ambiente especificado será ignorado) e retornará a mesma tarefa que a primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="39b5d-268">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="39b5d-269">Chamar esse método após a inicialização foi disparada implicitamente, definindo a propriedade Source não terá nenhum efeito (qualquer ambiente especificado é ignorado) e simplesmente retornar uma tarefa representando essa inicialização já em andamento.</span><span class="sxs-lookup"><span data-stu-id="39b5d-269">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="39b5d-270">Observe que, embora esse método seja assíncrono e retorne uma tarefa, ele ainda deve ser chamado no thread da interface do usuário, como a maioria das funcionalidades públicas da maioria dos controles da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="39b5d-270">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="39b5d-271">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-271">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="39b5d-272">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="39b5d-272">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="39b5d-273">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="39b5d-273">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="39b5d-274">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-274">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-275">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="39b5d-275">ExecuteScriptAsync</span></span> 

<span data-ttu-id="39b5d-276">Executa o código JavaScript do parâmetro javaScript no documento de nível superior atual renderizado no WebView.</span><span class="sxs-lookup"><span data-stu-id="39b5d-276">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="39b5d-277">Cadeia de caracteres de< de tarefas assíncronas pública > [ExecuteScriptAsync](#executescriptasync)(cadeia de caracteres JavaScript)</span><span class="sxs-lookup"><span data-stu-id="39b5d-277">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="39b5d-278">Equivalente a chamar CoreWebView2. ExecuteScriptAsync no CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-278">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="39b5d-279">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-279">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="39b5d-280">Gerado se CoreWebView2 ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-280">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="39b5d-281">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="39b5d-281">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="39b5d-282">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="39b5d-282">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="39b5d-283">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-283">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-284">GoBack</span><span class="sxs-lookup"><span data-stu-id="39b5d-284">GoBack</span></span> 

<span data-ttu-id="39b5d-285">Navega o WebView para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="39b5d-285">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="39b5d-286">public void [(](#goback)) public void</span><span class="sxs-lookup"><span data-stu-id="39b5d-286">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="39b5d-287">Equivalente a chamar CoreWebView2. GoBack no CoreWebView2 se CoreWebView2 ainda não tiver sido inicializado, não fará nada.</span><span class="sxs-lookup"><span data-stu-id="39b5d-287">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="39b5d-288">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-288">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="39b5d-289">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="39b5d-289">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="39b5d-290">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="39b5d-290">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="39b5d-291">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-291">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-292">GoForward</span><span class="sxs-lookup"><span data-stu-id="39b5d-292">GoForward</span></span> 

<span data-ttu-id="39b5d-293">Navega o WebView para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="39b5d-293">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="39b5d-294">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="39b5d-294">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="39b5d-295">Equivalente a chamar CoreWebView2. GoForward em CoreWebView2 se CoreWebView2 ainda não foi inicializado, não faz nada.</span><span class="sxs-lookup"><span data-stu-id="39b5d-295">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="39b5d-296">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-296">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="39b5d-297">Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="39b5d-297">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="39b5d-298">Consulte DispatcherObject. VerifyAccess para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="39b5d-298">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="39b5d-299">Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-299">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-300">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="39b5d-300">NavigateToString</span></span> 

<span data-ttu-id="39b5d-301">Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.</span><span class="sxs-lookup"><span data-stu-id="39b5d-301">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="39b5d-302">public void [NavigateToString](#navigatetostring)(cadeia de caracteres htmlContent)</span><span class="sxs-lookup"><span data-stu-id="39b5d-302">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="39b5d-303">Equivalente a chamar CoreWebView2. NavigateToString no CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-303">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="39b5d-304">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-304">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="39b5d-305">Gerado se CoreWebView2 ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-305">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="39b5d-306">" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="39b5d-306">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="39b5d-307">Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-307">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-308">Recarregar</span><span class="sxs-lookup"><span data-stu-id="39b5d-308">Reload</span></span> 

<span data-ttu-id="39b5d-309">Recarrega a página atual.</span><span class="sxs-lookup"><span data-stu-id="39b5d-309">Reloads the current page.</span></span>

> <span data-ttu-id="39b5d-310">recarregamento [Reload](#reload)nulo público ()</span><span class="sxs-lookup"><span data-stu-id="39b5d-310">public void [Reload](#reload)()</span></span>

<span data-ttu-id="39b5d-311">Equivalente a chamar CoreWebView2. reload no CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-311">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="39b5d-312">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-312">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="39b5d-313">Gerado se CoreWebView2 ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-313">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="39b5d-314">" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="39b5d-314">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="39b5d-315">Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-315">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-316">Parar</span><span class="sxs-lookup"><span data-stu-id="39b5d-316">Stop</span></span> 

<span data-ttu-id="39b5d-317">Interrompe todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="39b5d-317">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="39b5d-318">[Stop](#stop)void Public ()</span><span class="sxs-lookup"><span data-stu-id="39b5d-318">public void [Stop](#stop)()</span></span>

<span data-ttu-id="39b5d-319">Equivalente a chamar CoreWebView2. Stop no CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-319">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="39b5d-320">Exceções</span><span class="sxs-lookup"><span data-stu-id="39b5d-320">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="39b5d-321">Gerado se CoreWebView2 ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-321">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="39b5d-322">" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="39b5d-322">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="39b5d-323">Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.</span><span class="sxs-lookup"><span data-stu-id="39b5d-323">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="39b5d-324">WebView2</span><span class="sxs-lookup"><span data-stu-id="39b5d-324">WebView2</span></span> 

<span data-ttu-id="39b5d-325">Cria uma nova instância de um controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-325">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="39b5d-326">[WebView2](#webview2)público ()</span><span class="sxs-lookup"><span data-stu-id="39b5d-326">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="39b5d-327">Observe que o CoreWebView2 do controle será nulo até ser inicializado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-327">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="39b5d-328">Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="39b5d-328">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="39b5d-329">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="39b5d-329">BuildWindowCore</span></span> 

<span data-ttu-id="39b5d-330">Isso é substituído em HwndHost e é chamado para nos instruir a criar o HWND.</span><span class="sxs-lookup"><span data-stu-id="39b5d-330">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>

> <span data-ttu-id="39b5d-331">HandleRef de substituição protegido [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span><span class="sxs-lookup"><span data-stu-id="39b5d-331">protected override HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span></span>

##### <span data-ttu-id="39b5d-332">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b5d-332">Parameters</span></span>
* `hwndParent` <span data-ttu-id="39b5d-333">O HWND que devemos usar como pai do que criamos.</span><span class="sxs-lookup"><span data-stu-id="39b5d-333">The HWND that we should use as the parent of the one we create.</span></span>

##### <span data-ttu-id="39b5d-334">Devolver</span><span class="sxs-lookup"><span data-stu-id="39b5d-334">Returns</span></span>
<span data-ttu-id="39b5d-335">O HWND que criamos.</span><span class="sxs-lookup"><span data-stu-id="39b5d-335">The HWND that we created.</span></span>

#### <span data-ttu-id="39b5d-336">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="39b5d-336">DestroyWindowCore</span></span> 

<span data-ttu-id="39b5d-337">Isso é substituído em HwndHost e é chamado para nos instruir a destruir o HWND.</span><span class="sxs-lookup"><span data-stu-id="39b5d-337">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>

> <span data-ttu-id="39b5d-338">substituição protegida de void [DestroyWindowCore](#destroywindowcore)(HandleRef HWND)</span><span class="sxs-lookup"><span data-stu-id="39b5d-338">protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef hwnd)</span></span>

##### <span data-ttu-id="39b5d-339">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b5d-339">Parameters</span></span>
* `hwnd` <span data-ttu-id="39b5d-340">Nosso HWND que precisamos destruir.</span><span class="sxs-lookup"><span data-stu-id="39b5d-340">Our HWND that we need to destroy.</span></span>

#### <span data-ttu-id="39b5d-341">Dispose</span><span class="sxs-lookup"><span data-stu-id="39b5d-341">Dispose</span></span> 

<span data-ttu-id="39b5d-342">Isso é chamado pela nossa classe base de acordo com a implementação típica do padrão IDispose.</span><span class="sxs-lookup"><span data-stu-id="39b5d-342">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>

> <span data-ttu-id="39b5d-343">substituição de substituição de void [descartada (descarte](#dispose)bool) protegida</span><span class="sxs-lookup"><span data-stu-id="39b5d-343">protected override void [Dispose](#dispose)(bool disposing)</span></span>

<span data-ttu-id="39b5d-344">Nós o implementamos ao liberar todos os nossos recursos COM subjacentes, inclusive o nosso CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-344">We implement it by releasing all of our underlying COM resources, including our CoreWebView2.</span></span>

##### <span data-ttu-id="39b5d-345">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b5d-345">Parameters</span></span>
* `disposing` <span data-ttu-id="39b5d-346">Verdadeiro se um chamador estiver chamando explicitamente Dispose, false se estiver sendo finalizado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-346">True if a caller is explicitly calling Dispose, false if we're being finalized.</span></span>

#### <span data-ttu-id="39b5d-347">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="39b5d-347">HasFocusWithinCore</span></span> 

<span data-ttu-id="39b5d-348">Isso é substituído em HwndHost e é chamado quando o WPF precisa saber se o foco está em nosso controle/janela.</span><span class="sxs-lookup"><span data-stu-id="39b5d-348">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>

> <span data-ttu-id="39b5d-349">substituir bool [HasFocusWithinCore](#hasfocuswithincore)() protegido</span><span class="sxs-lookup"><span data-stu-id="39b5d-349">protected override bool [HasFocusWithinCore](#hasfocuswithincore)()</span></span>

<span data-ttu-id="39b5d-350">O WPF não pode saber por conta própria porque estamos hospedando uma janela não-WPF, portanto, em vez disso, ele nos solicitará chamando isso.</span><span class="sxs-lookup"><span data-stu-id="39b5d-350">WPF can't know on its own since we're hosting a non-WPF window, so instead it asks us by calling this.</span></span> <span data-ttu-id="39b5d-351">Para atender, simplesmente rastreamos o estado com base nos eventos do CoreWebView2 que são acionados quando ele ganha ou perde o foco.</span><span class="sxs-lookup"><span data-stu-id="39b5d-351">To answer, we just track state based on CoreWebView2 events that fire when it gains or loses focus.</span></span>

##### <span data-ttu-id="39b5d-352">Devolver</span><span class="sxs-lookup"><span data-stu-id="39b5d-352">Returns</span></span>
<span data-ttu-id="39b5d-353">Verdadeiro se o foco estiver em nosso controle/janela, falso se não estiver.</span><span class="sxs-lookup"><span data-stu-id="39b5d-353">True if the focus is in our control/window, false if it isn't.</span></span>

#### <span data-ttu-id="39b5d-354">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="39b5d-354">OnKeyDown</span></span> 

<span data-ttu-id="39b5d-355">Isso é substituído pelo UIElement e chamado para permitir que manipulemos a entrada de pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="39b5d-355">This is overridden from UIElement and called to allow us to handle key press input.</span></span>

> <span data-ttu-id="39b5d-356">substituição protegida de [AoApertarTecla](#onkeydown)nulo (KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="39b5d-356">protected override void [OnKeyDown](#onkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="39b5d-357">O WPF nunca realmente pode chamar isso em resposta a eventos de teclado porque estamos hospedando uma janela não-WPF.</span><span class="sxs-lookup"><span data-stu-id="39b5d-357">WPF should never actually call this in response to keyboard events because we're hosting a non-WPF window.</span></span> <span data-ttu-id="39b5d-358">Quando a nossa janela tiver foco, o Windows enviará a entrada diretamente para ele, em vez da janela de nível superior e do sistema de entrada do WPF.</span><span class="sxs-lookup"><span data-stu-id="39b5d-358">When our window has focus Windows will send the input directly to it rather than to WPF's top-level window and input system.</span></span> <span data-ttu-id="39b5d-359">Essa substituição só deve ser chamada quando estamos explicitamente encaminhando a entrada da tecla aceleradora do CoreWebView2 para o WPF (em CoreWebView2Controller_AcceleratorKeyPressed).</span><span class="sxs-lookup"><span data-stu-id="39b5d-359">This override should only be called when we're explicitly forwarding accelerator key input from the CoreWebView2 to WPF (in CoreWebView2Controller_AcceleratorKeyPressed).</span></span> <span data-ttu-id="39b5d-360">Mesmo assim, esse KeyDownEvent é disparado porque a implementação do PreviewKeyDownEvent explicitamente o dispara, correspondendo ao sistema usual do WPF.</span><span class="sxs-lookup"><span data-stu-id="39b5d-360">Even then, this KeyDownEvent is only triggered because our PreviewKeyDownEvent implementation explicitly triggers it, matching WPF's usual system.</span></span> <span data-ttu-id="39b5d-361">Portanto, o processo é: CoreWebView2Controller_AcceleratorKeyPressed-> raise PreviewKeyDownEvent-> OnPreviewKeyDown-> disparar KeyDownEvent-> AoApertarTecla</span><span class="sxs-lookup"><span data-stu-id="39b5d-361">So the process is: CoreWebView2Controller_AcceleratorKeyPressed -> raise PreviewKeyDownEvent -> OnPreviewKeyDown -> raise KeyDownEvent -> OnKeyDown</span></span>

#### <span data-ttu-id="39b5d-362">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="39b5d-362">OnKeyUp</span></span> 

<span data-ttu-id="39b5d-363">Veja OnKeyDown.</span><span class="sxs-lookup"><span data-stu-id="39b5d-363">See OnKeyDown.</span></span>

> <span data-ttu-id="39b5d-364">proteção contra substituição nula [onkeyup](#onkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="39b5d-364">protected override void [OnKeyUp](#onkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="39b5d-365">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="39b5d-365">OnPreviewKeyDown</span></span> 

<span data-ttu-id="39b5d-366">Esta é a "visualização" (por exemplo,</span><span class="sxs-lookup"><span data-stu-id="39b5d-366">This is the "Preview" (i.e.</span></span>

> <span data-ttu-id="39b5d-367">substituição protegida de void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="39b5d-367">protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="39b5d-368">tunelamento) da versão de OnKeyDown, portanto, ele realmente acontece primeiro.</span><span class="sxs-lookup"><span data-stu-id="39b5d-368">tunneling) version of OnKeyDown, so it actually happens first.</span></span> <span data-ttu-id="39b5d-369">Como OnKeyDown, isso só será chamado se estivermos encaminhando diretamente os pressionamentos de teclas do CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="39b5d-369">Like OnKeyDown, this will only ever be called if we're explicitly forwarding key presses from the CoreWebView2.</span></span> <span data-ttu-id="39b5d-370">Para imitar a manipulação de entrada padrão do WPF, quando recebermos isso, desativamos e disparamos o KeyDownEvent de bolha padrão.</span><span class="sxs-lookup"><span data-stu-id="39b5d-370">In order to mimic WPF's standard input handling, when we receive this we turn around and fire off the standard bubbling KeyDownEvent.</span></span> <span data-ttu-id="39b5d-371">Dessa forma, outras pessoas na árvore do WPF confiram o mesmo par padrão de eventos de entrada que o próprio WPF teria disparado se estivesse manipulando o pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="39b5d-371">That way others in the WPF tree see the same standard pair of input events that WPF itself would have triggered if it were handling the key press.</span></span>

#### <span data-ttu-id="39b5d-372">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="39b5d-372">OnPreviewKeyUp</span></span> 

<span data-ttu-id="39b5d-373">Consulte OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="39b5d-373">See OnPreviewKeyDown.</span></span>

> <span data-ttu-id="39b5d-374">substituição protegida de void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="39b5d-374">protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="39b5d-375">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="39b5d-375">OnWindowPositionChanged</span></span> 

<span data-ttu-id="39b5d-376">Isso é substituído de HwndHost e chamado quando o local de nosso controle é alterado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-376">This is overridden from HwndHost and called when our control's location has changed.</span></span>

> <span data-ttu-id="39b5d-377">substituição protegida void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span><span class="sxs-lookup"><span data-stu-id="39b5d-377">protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span></span>

<span data-ttu-id="39b5d-378">O HwndHost cuida da atualização do HWND criado.</span><span class="sxs-lookup"><span data-stu-id="39b5d-378">The HwndHost takes care of updating the HWND we created.</span></span> <span data-ttu-id="39b5d-379">O que precisamos fazer é mover nossa CoreWebView2 para corresponder ao novo local.</span><span class="sxs-lookup"><span data-stu-id="39b5d-379">What we need to do is move our CoreWebView2 to match the new location.</span></span>

#### <span data-ttu-id="39b5d-380">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="39b5d-380">TabIntoCore</span></span> 

<span data-ttu-id="39b5d-381">Isso é substituído em HwndHost e é chamado para informar que a Tabulação fez com que o foco se mova para o nosso controle/janela.</span><span class="sxs-lookup"><span data-stu-id="39b5d-381">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

> <span data-ttu-id="39b5d-382">substituição protegida de bool [TabIntoCore](#tabintocore)(solicitação TraversalRequest)</span><span class="sxs-lookup"><span data-stu-id="39b5d-382">protected override bool [TabIntoCore](#tabintocore)(TraversalRequest request)</span></span>

<span data-ttu-id="39b5d-383">Como o WPF não pode gerenciar a transição de foco para um HWND não-WPF, ele delega a transição para nós aqui.</span><span class="sxs-lookup"><span data-stu-id="39b5d-383">Since WPF can't manage the transition of focus to a non-WPF HWND, it delegates the transition to us here.</span></span> <span data-ttu-id="39b5d-384">Portanto, o nosso trabalho é apenas colocar o foco no HWND externo.</span><span class="sxs-lookup"><span data-stu-id="39b5d-384">So our job is just to place the focus in our external HWND.</span></span>

##### <span data-ttu-id="39b5d-385">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b5d-385">Parameters</span></span>
* `request` <span data-ttu-id="39b5d-386">Informações sobre como o foco está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="39b5d-386">Information about how the focus is moving.</span></span>

##### <span data-ttu-id="39b5d-387">Devolver</span><span class="sxs-lookup"><span data-stu-id="39b5d-387">Returns</span></span>
<span data-ttu-id="39b5d-388">True para indicar que manipulamos a navegação ou falso para indicar que não foi.</span><span class="sxs-lookup"><span data-stu-id="39b5d-388">True to indicate that we handled the navigation, or false to indicate that we didn't.</span></span>

