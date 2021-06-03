---
description: Automatizar e testar o Controle WebView2 usando Microsoft Edge Driver
title: Automatizando e testando WebView2 com Microsoft Edge Driver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: c23d639582d4ce550406cf955c96171167bde7c8
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536268"
---
# <a name="automating-and-testing-webview2-with-microsoft-edge-driver"></a><span data-ttu-id="db054-104">Automatizando e testando o WebView2 com Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="db054-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="db054-105">Como o WebView2 usa a plataforma web Microsoft Edge \(Chromium\), os desenvolvedores do WebView2 \(you\) podem tirar proveito da ferramenta web padrão para depuração e automação.</span><span class="sxs-lookup"><span data-stu-id="db054-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="db054-106">Selenium é uma dessas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="db054-106">Selenium is one such tool.</span></span>  <span data-ttu-id="db054-107">Ele implementa a API [W3C WebDriver.][W3cWebdriver2]</span><span class="sxs-lookup"><span data-stu-id="db054-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="db054-108">Você pode usar Selenium para criar testes automatizados para simular interações do usuário.</span><span class="sxs-lookup"><span data-stu-id="db054-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="db054-109">Começar com as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="db054-109">Get started with the following steps.</span></span>  

## <a name="step-1--download-webview2api-sample"></a><span data-ttu-id="db054-110">Etapa 1: Baixar Exemplo de WebView2API</span><span class="sxs-lookup"><span data-stu-id="db054-110">Step 1:  Download WebView2API Sample</span></span>  

<span data-ttu-id="db054-111">Se você não tiver um projeto WebView2 existente, baixe o aplicativo De exemplo [WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], um exemplo abrangente do SDK webView2 mais recente.</span><span class="sxs-lookup"><span data-stu-id="db054-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="db054-112">Certifique-se de ter atendido os pré-requisitos do aplicativo de exemplo [WebView2API.][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]</span><span class="sxs-lookup"><span data-stu-id="db054-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span>  

<span data-ttu-id="db054-113">Depois de clonar o repo, crie o projeto Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="db054-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="db054-114">Deve se parecer com a figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="db054-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicativo de exemplo WebView2API" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="db054-116">Aplicativo de exemplo WebView2API</span><span class="sxs-lookup"><span data-stu-id="db054-116">WebView2API Sample app</span></span>  
:::image-end:::  

## <a name="step-2--install-microsoft-edge-driver"></a><span data-ttu-id="db054-117">Etapa 2: Instalar Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="db054-117">Step 2:  Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="db054-118">Siga as instruções para instalar [Microsoft Edge Driver o][WebdriverChromiumDownloadMicrosoftEdgeDriver] driver específico do navegador exigido pela Selenium para automatizar e testar o WebView2.</span><span class="sxs-lookup"><span data-stu-id="db054-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="db054-119">Verifique se a versão do Microsoft Edge Driver corresponde à versão do WebView2 Runtime que o aplicativo usa.</span><span class="sxs-lookup"><span data-stu-id="db054-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="db054-120">Para que o Exemplo de WebView2API funcione, certifique-se de que sua versão do WebView2 Runtime seja maior ou igual que a versão suportada da versão mais recente do SDK WebView2.</span><span class="sxs-lookup"><span data-stu-id="db054-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="db054-121">Para localizar a versão mais recente do SDK webView2, navegue até [WebView2 release notes][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="db054-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="db054-122">Para descobrir qual versão do WebView2 Runtime você tem no momento, navegue até `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="db054-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <a name="step-3--add-selenium-to-the-webview2api-sample"></a><span data-ttu-id="db054-123">Etapa 3: Adicionar Selenium ao exemplo WebView2API</span><span class="sxs-lookup"><span data-stu-id="db054-123">Step 3:  Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="db054-124">Neste ponto, você deve ter WebView2 Runtime instalado, criado um projeto WebView2 e instalado Microsoft Edge Driver.</span><span class="sxs-lookup"><span data-stu-id="db054-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="db054-125">Agora, começar a usar Selenium.</span><span class="sxs-lookup"><span data-stu-id="db054-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="db054-126">Selenium dá suporte a C\#, Java, Python, Javascript e Ruby.</span><span class="sxs-lookup"><span data-stu-id="db054-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="db054-127">No entanto, o guia a seguir é escrito usando C\#.</span><span class="sxs-lookup"><span data-stu-id="db054-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="db054-128">Comece criando um novo projeto **C# .NET Framework** no **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="db054-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="db054-129">Escolha **Next** no canto inferior direito para continuar.</span><span class="sxs-lookup"><span data-stu-id="db054-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Criar um novo projeto" lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="db054-131">Criar um novo projeto</span><span class="sxs-lookup"><span data-stu-id="db054-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="db054-132">Dê um nome ao seu **projeto,** salve-o em seu **local preferencial**e escolha **Criar**.</span><span class="sxs-lookup"><span data-stu-id="db054-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar seu novo projeto" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="db054-134">Configurar seu novo projeto</span><span class="sxs-lookup"><span data-stu-id="db054-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="db054-135">Um novo projeto é criado.</span><span class="sxs-lookup"><span data-stu-id="db054-135">A new project is created.</span></span>  <span data-ttu-id="db054-136">Neste guia, todo o código é gravado no `Program.cs` arquivo.</span><span class="sxs-lookup"><span data-stu-id="db054-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Novo projeto" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="db054-138">Novo projeto</span><span class="sxs-lookup"><span data-stu-id="db054-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="db054-139">Agora adicione **Selenium** ao projeto.</span><span class="sxs-lookup"><span data-stu-id="db054-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="db054-140">Instale Selenium usando o pacote **Selenium.WebDriver NuGet .**</span><span class="sxs-lookup"><span data-stu-id="db054-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="db054-141">Para baixar o pacote **selenium.WebDriver**NuGet , em **Visual Studio,** passe o mouse no Project **e**escolha **Gerenciar NuGet Pacote**.</span><span class="sxs-lookup"><span data-stu-id="db054-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover on **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="db054-142">A tela a seguir deve aparecer.</span><span class="sxs-lookup"><span data-stu-id="db054-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Baixar NuGet pacote" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="db054-144">Baixar NuGet pacote</span><span class="sxs-lookup"><span data-stu-id="db054-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="db054-145">Insira `Selenium.WebDriver` na barra de pesquisa, escolha **Selenium.WebDriver** a partir dos resultados e certifique-se de marcar a caixa ao lado para incluir **a pré-versão**.</span><span class="sxs-lookup"><span data-stu-id="db054-145">Enter `Selenium.WebDriver` in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span>  <span data-ttu-id="db054-146">Na janela do lado direito, verifique se a **versão** está definida para instalar **4.0.0-alfa04** ou posterior e escolha **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="db054-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="db054-147">NuGet baixa Selenium para seu computador.</span><span class="sxs-lookup"><span data-stu-id="db054-147">NuGet downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="db054-148">Para saber mais sobre o pacote selenium.WebDriver NuGet, navegue até [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="db054-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Gerenciar NuGet pacote" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="db054-150">Gerenciar NuGet pacote</span><span class="sxs-lookup"><span data-stu-id="db054-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="db054-151">Use `OpenQA.Selenium.Edge` adicionando a seguinte instrução:  `using OpenQA.Selenium.Edge;` no início do `Program.cs` arquivo.</span><span class="sxs-lookup"><span data-stu-id="db054-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a><span data-ttu-id="db054-152">Etapa 4: Drive WebView2 com Selenium e Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="db054-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="db054-153">Primeiro, crie `EdgeOptions` o objeto, copiando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="db054-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="db054-154">O `EdgeOptions` objeto recebe os dois parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="db054-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="db054-155">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="db054-155">Parameter</span></span> | <span data-ttu-id="db054-156">Detalhes</span><span class="sxs-lookup"><span data-stu-id="db054-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="db054-157">De acordo `false` com , que informa a Selenium que você está conduzindo o novo Chromium de Microsoft Edge navegador.</span><span class="sxs-lookup"><span data-stu-id="db054-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="db054-158">Uma cadeia de caracteres que informa a Selenium que você está conduzindo WebView2.</span><span class="sxs-lookup"><span data-stu-id="db054-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="db054-159">Em seguida, de acordo com o caminho do arquivo do seu tempo de execução do projeto WebView2, crie uma cadeia de caracteres chamada que fornece o caminho do arquivo para onde você instalou o driver do Microsoft Edge e crie uma cadeia de caracteres chamada para armazenar o nome do tempo de execução do `edgeOptions.BinaryLocation` `msedgedriverDir` driver [][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads] `msedgedriverExe` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="db054-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="db054-160">Por padrão, o tempo de execução é chamado `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="db054-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="db054-161">Use essas duas cadeias de caracteres para construir `EdgeDriverService` o objeto conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="db054-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="db054-162">Por fim, crie `EdgeDriver` o objeto usando e `EdgeDriverService` `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="db054-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="db054-163">Você pode copiar e colar o seguinte código abaixo `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="db054-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="db054-164">Certifique-se de especificar os caminhos de arquivo corretos para o tempo de execução do seu projeto e o tempo de execução Microsoft Edge driver em seu computador.</span><span class="sxs-lookup"><span data-stu-id="db054-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
    ```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample runtime
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";
    
    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";
    
    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";
    
    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);
    
    EdgeDriver e = new EdgeDriver(service, edgeOptions);
    ```
    
3.  <span data-ttu-id="db054-165">Agora, `EdgeDriver` está configurado para conduzir o WebView2 em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="db054-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="db054-166">Por exemplo, se você estiver usando o **Exemplo WebView2API,** poderá navegar `https://microsoft.com` para executando o `e.Url = @"https://www.microsoft.com";` comando.</span><span class="sxs-lookup"><span data-stu-id="db054-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="db054-167">Verifique o WebView2 de unidade de selenium definindo um ponto de interrupção na linha e executando o projeto.</span><span class="sxs-lookup"><span data-stu-id="db054-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium executando WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="db054-169">Selenium executando WebView2</span><span class="sxs-lookup"><span data-stu-id="db054-169">Selenium running WebView2</span></span>  
    :::image-end:::

<span data-ttu-id="db054-170">Parabéns.</span><span class="sxs-lookup"><span data-stu-id="db054-170">Congratulations.</span></span>  <span data-ttu-id="db054-171">Você automatiza com êxito um projeto WebView2 e orienta WebView2 usando Selenium e Microsoft Edge Driver.</span><span class="sxs-lookup"><span data-stu-id="db054-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <a name="see-also"></a><span data-ttu-id="db054-172">Consulte também</span><span class="sxs-lookup"><span data-stu-id="db054-172">See also</span></span>  

*   <span data-ttu-id="db054-173">Para uma visão abrangente de como as APIs Selenium conduzEm WebView2 ou Microsoft Edge \(Chromium\), navegue até WebDriver na documentação [selenium][SeleniumWebdriver]</span><span class="sxs-lookup"><span data-stu-id="db054-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="db054-174">Para saber mais sobre o controle WebView2 e como usá-lo ao incorporar conteúdo da Web em seu aplicativo nativo, navegue até Introdução ao Microsoft Edge [WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="db054-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="db054-175">Para saber mais sobre como automatizar Microsoft Edge \(Chromium\), navegue até [Usar o WebDriver (Chromium) para automação de teste][WebdriverChromium]</span><span class="sxs-lookup"><span data-stu-id="db054-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="db054-176">Entrar em contato com a equipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="db054-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Usar o WebDriver (Chromium) para testes de automação | Microsoft Docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Baixar Microsoft Edge Driver - Usar o WebDriver (Chromium) para testes de automação | Microsoft Docs"  
[WebViewIndex]: ../index.md "Introdução ao Microsoft Edge WebView2 - Microsoft Docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de versão do SDK WebView2 | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Baixe o WebDriver | Microsoft Edge Desenvolvedor"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemplo de API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Pré-requisitos - Exemplo de API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium.WebDriver 4.0.0-alpha04 | NuGet Galeria"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
