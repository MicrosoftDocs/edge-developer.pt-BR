---
description: Saiba como usar JavaScript em cenários complexos em aplicativos WebView2
title: Usar JavaScript em aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 8db5c4a5b3709c144240fe88e6f8480445c1659f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535750"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a><span data-ttu-id="33360-104">Usar JavaScript no WebView para cenários estendidos</span><span class="sxs-lookup"><span data-stu-id="33360-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="33360-105">Usar o JavaScript em controles WebView2 permite personalizar aplicativos nativos para atender aos seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="33360-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="33360-106">Este artigo explora como usar o JavaScript no WebView2 e analisa como desenvolver usando recursos e funcionalidade avançados do WebView2.</span><span class="sxs-lookup"><span data-stu-id="33360-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="33360-107">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="33360-107">Before you begin</span></span>  

<span data-ttu-id="33360-108">Este artigo supõe que você já tenha um projeto funcionando.</span><span class="sxs-lookup"><span data-stu-id="33360-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="33360-109">Se você não tiver um projeto e quiser acompanhar, navegue até o Guia de Introdução [WebView2.][Webview2GetStartedWpf]</span><span class="sxs-lookup"><span data-stu-id="33360-109">If you do not have a project and want to follow along, navigate to the [WebView2 Get Started Guide][Webview2GetStartedWpf].</span></span>  

## <a name="basic-webview2-functions"></a><span data-ttu-id="33360-110">Funções Básicas do WebView2</span><span class="sxs-lookup"><span data-stu-id="33360-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="33360-111">Use as seguintes funções para começar a incorporar JavaScript em seu aplicativo WebView.</span><span class="sxs-lookup"><span data-stu-id="33360-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="33360-112">API</span><span class="sxs-lookup"><span data-stu-id="33360-112">API</span></span>  | <span data-ttu-id="33360-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="33360-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="33360-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="33360-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | <span data-ttu-id="33360-115">Execute JavaScript em um controle WebView.</span><span class="sxs-lookup"><span data-stu-id="33360-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="33360-116">Para obter mais informações, navegue até a Introdução tutorial.</span><span class="sxs-lookup"><span data-stu-id="33360-116">For more information, navigate to the Get Started tutorial.</span></span> |
| [<span data-ttu-id="33360-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="33360-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="33360-118">É executado quando o Modelo de Objeto de Documento \(DOM\) é criado.</span><span class="sxs-lookup"><span data-stu-id="33360-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <a name="scenario--running-a-dedicated-script-file"></a><span data-ttu-id="33360-119">Cenário: executando um arquivo de script dedicado</span><span class="sxs-lookup"><span data-stu-id="33360-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="33360-120">Nesta seção, acesse um arquivo JavaScript dedicado do controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="33360-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="33360-121">Embora escrever JavaScript em linha possa ser eficiente para comandos JavaScript rápidos, você perde temas de cores javaScript e formatação de linha que dificulta a gravação de grandes seções de código em Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="33360-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="33360-122">Para resolver o problema, crie um arquivo JavaScript separado com seu código e, em seguida, passe uma referência para esse arquivo usando `ExecuteScriptAsync` os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="33360-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="33360-123">Crie um `.js` arquivo em seu projeto e adicione o código JavaScript que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="33360-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="33360-124">Por exemplo, crie um arquivo chamado `script.js` .</span><span class="sxs-lookup"><span data-stu-id="33360-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="33360-125">Converta o arquivo JavaScript em uma cadeia de caracteres que é passada para `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="33360-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="33360-126">Para converter seu arquivo JavaScript em uma cadeia de caracteres, copie o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="33360-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="33360-127">Colar o código em `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="33360-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="33360-128">Passe a variável de texto usando `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="33360-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  
    
## <a name="scenario--remove-drag-and-drop-functionality"></a><span data-ttu-id="33360-129">Cenário: remover a funcionalidade de arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="33360-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="33360-130">Nesta seção, use JavaScript para remover a funcionalidade de arrastar e soltar do controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="33360-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="33360-131">Para começar, explore a funcionalidade atual de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="33360-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="33360-132">Crie um `.txt` arquivo para arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="33360-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="33360-133">Por exemplo, crie um arquivo nomeado `contoso.txt` e adicione texto a ele.</span><span class="sxs-lookup"><span data-stu-id="33360-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="33360-134">Execute seu projeto.</span><span class="sxs-lookup"><span data-stu-id="33360-134">Run your project.</span></span>  
1.  <span data-ttu-id="33360-135">Arraste e solte o arquivo `contoso.txt` no controle WebView.</span><span class="sxs-lookup"><span data-stu-id="33360-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="33360-136">Uma nova janela é aberta, que é o resultado do código em seu projeto de exemplo.</span><span class="sxs-lookup"><span data-stu-id="33360-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/drag-text.png" alt-text="Resultado de arrastar e soltar contoso.txt" lightbox="./media/drag-text.png":::
       <span data-ttu-id="33360-138">Resultado de arrastar e soltar contoso.txt</span><span class="sxs-lookup"><span data-stu-id="33360-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  
    
<span data-ttu-id="33360-139">Agora, adicione código para remover a funcionalidade de arrastar e soltar do controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="33360-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="33360-140">Copie e colar o seguinte trecho de código `InitializeAsync()` em `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="33360-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
    
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
    
1.  <span data-ttu-id="33360-141">Execute seu projeto.</span><span class="sxs-lookup"><span data-stu-id="33360-141">Run your project.</span></span>  
1.  <span data-ttu-id="33360-142">Tente arrastar e `contoso.txt` soltar.</span><span class="sxs-lookup"><span data-stu-id="33360-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="33360-143">Confirme se você não é capaz de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="33360-143">Confirm that you are not able to drag-and-drop.</span></span>  
    
## <a name="scenario--removing-the-context-menu"></a><span data-ttu-id="33360-144">Cenário: Removendo o Menu de Contexto</span><span class="sxs-lookup"><span data-stu-id="33360-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="33360-145">Nesta seção, remova o menu de contexto padrão do controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="33360-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="33360-146">Para começar, explore a funcionalidade atual do menu contextual.</span><span class="sxs-lookup"><span data-stu-id="33360-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="33360-147">Execute seu projeto.</span><span class="sxs-lookup"><span data-stu-id="33360-147">Run your project.</span></span>  
1.  <span data-ttu-id="33360-148">Passe o mouse em qualquer lugar no controle WebView2 e abra o menu de contexto \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="33360-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="33360-149">O menu de contexto exibe as opções padrão.</span><span class="sxs-lookup"><span data-stu-id="33360-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/context-menu.png" alt-text="O menu de contexto mostrando as opções padrão" lightbox="./media/context-menu.png":::
       <span data-ttu-id="33360-151">O menu de contexto mostrando as opções padrão</span><span class="sxs-lookup"><span data-stu-id="33360-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="33360-152">Agora adicione código para remover a funcionalidade de menu contextual do controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="33360-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="33360-153">Copie e colar o seguinte trecho de código `InitializeAsync()` em `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="33360-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
    
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  
    
1.  <span data-ttu-id="33360-154">Execute o código novamente.</span><span class="sxs-lookup"><span data-stu-id="33360-154">Run the code again.</span></span>  <span data-ttu-id="33360-155">Confirme se não é possível abrir um menu de contexto \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="33360-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="33360-156">Consulte também</span><span class="sxs-lookup"><span data-stu-id="33360-156">See also</span></span>  

*   <span data-ttu-id="33360-157">Para começar a usar WebView2, navegue até [WebView2 Introdução Guias][Webview2MainGetStarted].</span><span class="sxs-lookup"><span data-stu-id="33360-157">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].</span></span>  
*   <span data-ttu-id="33360-158">Para um exemplo abrangente de recursos WebView2, navegue até o repo do [WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="33360-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="33360-159">Para obter informações detalhadas sobre APIs WebView2, navegue até [referência de API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="33360-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="33360-160">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="33360-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="33360-161">Entrar em contato com a equipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="33360-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Referência da API WebView2 | Microsoft Docs"  
[Webview2GetStartedWpf]: ../get-started/wpf.md "Começar com WebView2 no WPF (Visualização) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0,9.579 - interface ICoreWebView2 | Microsoft Docs"  

[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
