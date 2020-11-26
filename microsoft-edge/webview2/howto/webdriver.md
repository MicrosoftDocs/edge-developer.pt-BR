---
description: Automatizar e testar o controle WebView2 usando o Microsoft Edge driver
title: Automatizando e testando o WebView2 com o Microsoft Edge driver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Driver do Microsoft Edge
ms.openlocfilehash: 2af1ce222abb1dc7a279afc05e87e7e42a45fe9e
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191614"
---
# <span data-ttu-id="22850-104">Automatizando e testando o WebView2 com o Microsoft Edge driver</span><span class="sxs-lookup"><span data-stu-id="22850-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="22850-105">Como o WebView2 usa a plataforma da Web Microsoft Edge \ (Chromium \), os desenvolvedores WebView2 \ (você \) podem aproveitar a ferramenta padrão da Web para depuração e automação.</span><span class="sxs-lookup"><span data-stu-id="22850-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="22850-106">O Selenium é uma dessas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="22850-106">Selenium is one such tool.</span></span>  <span data-ttu-id="22850-107">Ele implementa a API do W3C para [WebDriver][W3cWebdriver2] .</span><span class="sxs-lookup"><span data-stu-id="22850-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="22850-108">Você pode usar Selenium para criar testes automatizados para simular interações do usuário.</span><span class="sxs-lookup"><span data-stu-id="22850-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="22850-109">Comece a usar as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="22850-109">Get started with the following steps.</span></span>  

## <span data-ttu-id="22850-110">Etapa 1: baixar a amostra de WebView2API</span><span class="sxs-lookup"><span data-stu-id="22850-110">Step 1:  Download WebView2API Sample</span></span>  

<span data-ttu-id="22850-111">Se você não tiver um projeto WebView2 existente, baixe o [aplicativo de exemplo WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], um exemplo abrangente do SDK WebView2 mais recente.</span><span class="sxs-lookup"><span data-stu-id="22850-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="22850-112">Certifique-se de que você tenha satisfeito com os [pré-requisitos do aplicativo de exemplo WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span><span class="sxs-lookup"><span data-stu-id="22850-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span>  

<span data-ttu-id="22850-113">Depois de clonar o repositório, compile o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="22850-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="22850-114">Ele deve ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="22850-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicativo de exemplo WebView2API" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="22850-116">Aplicativo de exemplo WebView2API</span><span class="sxs-lookup"><span data-stu-id="22850-116">WebView2API Sample app</span></span>  
:::image-end:::  

## <span data-ttu-id="22850-117">Etapa 2: instalar o driver Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="22850-117">Step 2:  Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="22850-118">Siga as instruções para instalar o [Driver do Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] o driver específico do navegador exigido pelo Selenium para automatizar e testar o WebView2.</span><span class="sxs-lookup"><span data-stu-id="22850-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="22850-119">Verifique se a versão do driver do Microsoft Edge corresponde à versão do WebView2 Runtime que você usa em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22850-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="22850-120">Para que a amostra WebView2API funcione, certifique-se de que sua versão do WebView2 do tempo de execução é maior ou igual à versão compatível da versão mais recente do SDK do WebView2.</span><span class="sxs-lookup"><span data-stu-id="22850-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="22850-121">Para localizar a versão mais recente do SDK do WebView2, acesse [WebView2 notas de versão][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="22850-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="22850-122">Para saber qual é a versão do tempo de execução do WebView2 que você tem no momento, navegue até `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="22850-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <span data-ttu-id="22850-123">Etapa 3: Adicionar Selenium ao exemplo WebView2API</span><span class="sxs-lookup"><span data-stu-id="22850-123">Step 3:  Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="22850-124">Nesse ponto, você deve ter o WebView2 Runtime instalado, criar um projeto WebView2 e instalar o Microsoft Edge driver.</span><span class="sxs-lookup"><span data-stu-id="22850-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="22850-125">Agora, comece a usar o Selenium.</span><span class="sxs-lookup"><span data-stu-id="22850-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="22850-126">O Selenium dá suporte a C \ #, Java, Python, JavaScript e Ruby.</span><span class="sxs-lookup"><span data-stu-id="22850-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="22850-127">No entanto, o guia a seguir é escrito usando C \ #.</span><span class="sxs-lookup"><span data-stu-id="22850-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="22850-128">Comece criando um novo projeto **C# .NET Framework** no **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="22850-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="22850-129">Escolha **Avançar** no canto inferior direito para continuar.</span><span class="sxs-lookup"><span data-stu-id="22850-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Criar um novo projeto" lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="22850-131">Criar um novo projeto</span><span class="sxs-lookup"><span data-stu-id="22850-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="22850-132">Dê um **nome**ao projeto, salve-o no seu **local**preferido e escolha **criar**.</span><span class="sxs-lookup"><span data-stu-id="22850-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar seu novo projeto" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="22850-134">Configurar seu novo projeto</span><span class="sxs-lookup"><span data-stu-id="22850-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="22850-135">Um novo projeto é criado.</span><span class="sxs-lookup"><span data-stu-id="22850-135">A new project is created.</span></span>  <span data-ttu-id="22850-136">Neste guia, todo o código é escrito no `Program.cs` arquivo.</span><span class="sxs-lookup"><span data-stu-id="22850-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Novo projeto" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="22850-138">Novo projeto</span><span class="sxs-lookup"><span data-stu-id="22850-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="22850-139">Agora, adicione **Selenium** ao projeto.</span><span class="sxs-lookup"><span data-stu-id="22850-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="22850-140">Instale o Selenium usando o **pacote NuGet Selenium. WebDriver**.</span><span class="sxs-lookup"><span data-stu-id="22850-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="22850-141">Para baixar o **pacote Selenium. WebDriver NuGet**, no **Visual Studio**, passe o mouse sobre o **Project**e escolha **gerenciar pacote NuGet**.</span><span class="sxs-lookup"><span data-stu-id="22850-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover over **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="22850-142">A tela a seguir deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="22850-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Baixar pacote NuGet" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="22850-144">Baixar pacote NuGet</span><span class="sxs-lookup"><span data-stu-id="22850-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="22850-145">Digite `Selenium.WebDriver` na barra de pesquisa, escolha **Selenium. WebDriver** nos resultados e certifique-se de fazer uma marca de seleção na caixa ao lado de **incluir pré-lançamento**.</span><span class="sxs-lookup"><span data-stu-id="22850-145">Enter `Selenium.WebDriver` in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span>  <span data-ttu-id="22850-146">Na janela do lado direito, verifique se a **versão** está definida como **instalar o 4.0.0-alpha04** ou posterior e escolha **instalar**.</span><span class="sxs-lookup"><span data-stu-id="22850-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="22850-147">O NuGet baixa o Selenium em seu computador.</span><span class="sxs-lookup"><span data-stu-id="22850-147">NuGet downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="22850-148">Para saber mais sobre o pacote NuGet Selenium. WebDriver, navegue até [Selenium. WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="22850-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Gerenciar pacote NuGet" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="22850-150">Gerenciar pacote NuGet</span><span class="sxs-lookup"><span data-stu-id="22850-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="22850-151">Use `OpenQA.Selenium.Edge` ao adicionar a seguinte instrução:  `using OpenQA.Selenium.Edge;` no início do `Program.cs` arquivo.</span><span class="sxs-lookup"><span data-stu-id="22850-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <span data-ttu-id="22850-152">Etapa 4: unidade WebView2 com o Selenium e o Microsoft Edge driver</span><span class="sxs-lookup"><span data-stu-id="22850-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="22850-153">Primeiro, crie o `EdgeOptions` objeto, copiando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="22850-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="22850-154">O `EdgeOptions` objeto assume os dois parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="22850-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="22850-155">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="22850-155">Parameter</span></span> | <span data-ttu-id="22850-156">Detalhes</span><span class="sxs-lookup"><span data-stu-id="22850-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="22850-157">Definido como `false` , que informa ao Selenium que você está direcionando o novo navegador Microsoft Edge baseado em Chromium.</span><span class="sxs-lookup"><span data-stu-id="22850-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="22850-158">Uma cadeia de caracteres que informa ao Selenium que você está dirigindo WebView2.</span><span class="sxs-lookup"><span data-stu-id="22850-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="22850-159">Em seguida, defina o `edgeOptions.BinaryLocation` caminho do arquivo do tempo de execução do projeto do WebView2, crie uma cadeia de caracteres chamada `msedgedriverDir` que forneça o caminho do arquivo para o qual você instalou o [Microsoft Edge driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]e crie uma cadeia de caracteres chamada `msedgedriverExe` para armazenar o nome do tempo de execução do driver do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="22850-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="22850-160">Por padrão, o tempo de execução é nomeado `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="22850-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="22850-161">Use essas duas cadeias de caracteres para construir o `EdgeDriverService` objeto conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="22850-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="22850-162">Por fim, crie o `EdgeDriver` objeto usando `EdgeDriverService` e `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="22850-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="22850-163">Você pode copiar e colar o seguinte código abaixo `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="22850-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="22850-164">Certifique-se de especificar os caminhos de arquivo corretos para o tempo de execução do projeto e o tempo de execução do driver do Microsoft Edge em seu computador.</span><span class="sxs-lookup"><span data-stu-id="22850-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
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
    
3.  <span data-ttu-id="22850-165">Agora, `EdgeDriver` está configurado para direcionar o WebView2 em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="22850-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="22850-166">Por exemplo, se você estiver usando o **exemplo WebView2API**, poderá navegar `https://microsoft.com` executando o `e.Url = @"https://www.microsoft.com";` comando.</span><span class="sxs-lookup"><span data-stu-id="22850-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="22850-167">Verifique a unidade Selenium WebView2 definindo um ponto de interrupção na linha e executando o projeto.</span><span class="sxs-lookup"><span data-stu-id="22850-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium executando o WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="22850-169">Selenium executando o WebView2</span><span class="sxs-lookup"><span data-stu-id="22850-169">Selenium running WebView2</span></span>  
    :::image-end:::

<span data-ttu-id="22850-170">Parabéns.</span><span class="sxs-lookup"><span data-stu-id="22850-170">Congratulations.</span></span>  <span data-ttu-id="22850-171">Você automatizau com êxito um projeto do WebView2 e conduziu WebView2 usando o Selenium e o Microsoft Edge driver.</span><span class="sxs-lookup"><span data-stu-id="22850-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <span data-ttu-id="22850-172">Consulte também</span><span class="sxs-lookup"><span data-stu-id="22850-172">See also</span></span>  

*   <span data-ttu-id="22850-173">Para ter uma visão abrangente de como as APIs Selenium unidades WebView2 ou Microsoft Edge \ (Chromium \), navegue até [WebDriver na documentação do Selenium][SeleniumWebdriver]</span><span class="sxs-lookup"><span data-stu-id="22850-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="22850-174">Para saber mais sobre o controle WebView2 e como usá-lo ao inserir conteúdo da Web em seu aplicativo nativo, navegue até [introdução ao Microsoft Edge WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="22850-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="22850-175">Para saber mais sobre como automatizar o Microsoft Edge \ (Chromium \), navegue para [usar o WebDriver (Chromium) para automação de teste][WebdriverChromium]</span><span class="sxs-lookup"><span data-stu-id="22850-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <span data-ttu-id="22850-176">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="22850-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Use o WebDriver (Chromium) para automação de teste | Documentos da Microsoft"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Baixar o driver do Microsoft Edge-use o WebDriver (Chromium) para automação de teste | Documentos da Microsoft"  
[WebViewIndex]: ../index.md "Introdução ao Microsoft Edge WebView2-documentos da Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Baixar o WebDriver | Desenvolvedor do Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemplo de API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Pré-requisitos-exemplo de API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium. WebDriver 4.0.0-alpha04 | Galeria do NuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
