---
description: Automatizar e testar o controle WebView2 usando o Microsoft Edge driver
title: Automatizando e testando o WebView2 com o Microsoft Edge driver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Driver do Microsoft Edge
ms.openlocfilehash: acee8c1f791fdd4a2604b8f3bfa7664548a164d1
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659677"
---
# <span data-ttu-id="40b09-104">Automatizando e testando o WebView2 com o Microsoft Edge driver</span><span class="sxs-lookup"><span data-stu-id="40b09-104">Automating and Testing WebView2 with Microsoft Edge Driver</span></span>

<span data-ttu-id="40b09-105">Como o WebView2 utiliza a plataforma Web Chromium, WebView2 os desenvolvedores podem aproveitar as ferramentas padrão da Web para depuração e automação.</span><span class="sxs-lookup"><span data-stu-id="40b09-105">Because WebView2 utilizes the Chromium web platform, WebView2 developers can take advantage of standard web tooling for debugging and automation.</span></span> <span data-ttu-id="40b09-106">Uma dessas ferramentas é Selenium, que implementa a API do W3C [WebDriver](https://www.w3.org/TR/webdriver2/) , que pode ser usada para criar testes automatizados que simulam interações do usuário.</span><span class="sxs-lookup"><span data-stu-id="40b09-106">One such tool is Selenium, which implements the W3C [WebDriver](https://www.w3.org/TR/webdriver2/) API, which can be used to create automated tests that simulate user interactions.</span></span>

<span data-ttu-id="40b09-107">Veja como começar:</span><span class="sxs-lookup"><span data-stu-id="40b09-107">Here's how to get started:</span></span>

## <span data-ttu-id="40b09-108">Etapa 1: baixar a amostra de WebView2API</span><span class="sxs-lookup"><span data-stu-id="40b09-108">Step 1: Download WebView2API Sample</span></span>

<span data-ttu-id="40b09-109">Se você não tiver um projeto existente do WebView2, baixe o [aplicativo de exemplo do WebView2API](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample), um exemplo abrangente do SDK WebView2 mais recente.</span><span class="sxs-lookup"><span data-stu-id="40b09-109">If you do not have an existing WebView2 project, download our [WebView2API Sample application](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample), a comprehensive sample of the latest WebView2 SDK.</span></span> <span data-ttu-id="40b09-110">Verifique se você já tem satisfeito por estes [pré-requisitos](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="40b09-110">Please double check that you have satisfied these [prerequisites](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites).</span></span>

<span data-ttu-id="40b09-111">Depois de clonar o repositório, compile o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="40b09-111">Once you have cloned the repo, build the project in Visual Studio.</span></span> <span data-ttu-id="40b09-112">Ele deve ter uma aparência semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="40b09-112">It should look like the following:</span></span>

![texto alternativo](../media/webdriver/sample-app.png)

## <span data-ttu-id="40b09-114">Etapa 2: instalar o driver Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40b09-114">Step 2: Install Microsoft Edge Driver</span></span>

<span data-ttu-id="40b09-115">Siga as instruções para instalar o [Driver do Microsoft Edge](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) o driver específico do navegador exigido pelo Selenium para automatizar e testar o WebView2.</span><span class="sxs-lookup"><span data-stu-id="40b09-115">Follow the instructions to install [Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) the browser-specific driver required by Selenium to automate and test WebView2.</span></span>

<span data-ttu-id="40b09-116">É importante verificar se a versão do driver do Microsoft Edge corresponde à versão do Microsoft Edge usada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40b09-116">It is important to make sure that the version of Microsoft Edge Driver matches the version of Microsoft Edge that the application uses.</span></span> <span data-ttu-id="40b09-117">Para que a amostra WebView2API funcione, certifique-se de que sua versão do Microsoft Edge é maior ou igual à versão compatível da versão mais recente do SDK encontrada [nas nossas notas de versão](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes).</span><span class="sxs-lookup"><span data-stu-id="40b09-117">For the WebView2API Sample to work, make sure that your version of Microsoft Edge is greater than or equal to the supported version of our latest SDK release found [in our Release Notes](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes).</span></span> <span data-ttu-id="40b09-118">Para descobrir qual versão do Microsoft Edge você tem atualmente, carregue `edge://settings/help` no navegador.</span><span class="sxs-lookup"><span data-stu-id="40b09-118">To find out what version of Microsoft Edge you currently have, load `edge://settings/help` in the browser.</span></span>

## <span data-ttu-id="40b09-119">Etapa 3: Adicionar Selenium ao exemplo WebView2API</span><span class="sxs-lookup"><span data-stu-id="40b09-119">Step 3: Add Selenium to the WebView2API Sample</span></span>

<span data-ttu-id="40b09-120">Nesse ponto, você deve ter o Microsoft Edge instalado, criar um projeto WebView2 e ter instalado o driver Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40b09-120">At this point you should have Microsoft Edge installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span> <span data-ttu-id="40b09-121">Agora, vamos começar a usar o Selenium.</span><span class="sxs-lookup"><span data-stu-id="40b09-121">Now, let's get started using Selenium.</span></span>

> [!NOTE]
> <span data-ttu-id="40b09-122">O Selenium é compatível com C#, Java, Python, JavaScript e Ruby.</span><span class="sxs-lookup"><span data-stu-id="40b09-122">Selenium supports C#, Java, Python, Javascript, and Ruby.</span></span> <span data-ttu-id="40b09-123">No entanto, esse guia estará em C#.</span><span class="sxs-lookup"><span data-stu-id="40b09-123">However, this guide will be in C#.</span></span>

1. <span data-ttu-id="40b09-124">Comece criando um novo projeto **C# .NET Framework** no **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="40b09-124">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span> <span data-ttu-id="40b09-125">Clique em **Avançar** no canto inferior direito para continuar.</span><span class="sxs-lookup"><span data-stu-id="40b09-125">Click **Next** on the bottom right-hand corner to continue.</span></span>

![texto alternativo](../media/webdriver/new-project.png)

2. <span data-ttu-id="40b09-127">Dê um **nome**ao projeto, salve-o no seu **local**preferido e clique em **criar**.</span><span class="sxs-lookup"><span data-stu-id="40b09-127">Give your project a **name**, save it to your preferred **location**, and click **Create**.</span></span>

![texto alternativo](../media/webdriver/app-create.png)

3. <span data-ttu-id="40b09-129">Um novo projeto será criado.</span><span class="sxs-lookup"><span data-stu-id="40b09-129">A new project will be created.</span></span> <span data-ttu-id="40b09-130">Neste guia, todo o código será escrito no arquivo **Program.cs** .</span><span class="sxs-lookup"><span data-stu-id="40b09-130">In this guide, all code will be written in the **Program.cs** file.</span></span>

![texto alternativo](../media/webdriver/start-app.png)

4. <span data-ttu-id="40b09-132">Agora, vamos adicionar **Selenium** ao projeto.</span><span class="sxs-lookup"><span data-stu-id="40b09-132">Now let's add **Selenium** to the project.</span></span> <span data-ttu-id="40b09-133">Você pode instalar o Selenium pelo **pacote do Selenium. WebDriver NuGet**.</span><span class="sxs-lookup"><span data-stu-id="40b09-133">You can install Selenium via the **Selenium.WebDriver NuGet package**.</span></span>

<span data-ttu-id="40b09-134">Para baixar o **pacote Selenium. WebDriver NuGet**, no **Visual Studio**, passe o mouse sobre o **Project** e selecione **Manage NuGet Package**.</span><span class="sxs-lookup"><span data-stu-id="40b09-134">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover over **Project** and select **Manage NuGet Package**.</span></span> <span data-ttu-id="40b09-135">A seguinte tela deve aparecer:</span><span class="sxs-lookup"><span data-stu-id="40b09-135">The following screen should appear:</span></span>

![texto alternativo](../media/webdriver/download-nuget.png)

5. <span data-ttu-id="40b09-137">Digite **Selenium. WebDriver** na barra de pesquisa, clique em **Selenium. WebDriver** nos resultados e verifique se a caixa está marcando a caixa ao lado de **incluir a versão de pré-lançamento**.</span><span class="sxs-lookup"><span data-stu-id="40b09-137">Enter **Selenium.WebDriver** in the search bar, click **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span> <span data-ttu-id="40b09-138">Na janela do lado direito, verifique se a **versão** está definida como **instalar o 4.0.0-alpha04** ou posterior e clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="40b09-138">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and click **Install**.</span></span> <span data-ttu-id="40b09-139">O NuGet fará o download do Selenium em seu computador.</span><span class="sxs-lookup"><span data-stu-id="40b09-139">Nuget will download Selenium to your machine.</span></span>

[<span data-ttu-id="40b09-140">Saiba mais sobre o pacote NuGet Selenium. WebDriver.</span><span class="sxs-lookup"><span data-stu-id="40b09-140">Learn more about the Selenium.WebDriver NuGet package.</span></span>](https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04)

![texto alternativo](../media/webdriver/nuget.png)

6. <span data-ttu-id="40b09-142">Use **OpenQA. Selenium. Edge** adicionando a seguinte instrução: ```using OpenQA.Selenium.Edge;``` no início de **Program.cs**</span><span class="sxs-lookup"><span data-stu-id="40b09-142">Use **OpenQA.Selenium.Edge** by adding the following statement:```using OpenQA.Selenium.Edge;``` at the beginning of **Program.cs**</span></span>

```csharp
using OpenQA.Selenium.Edge;

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## <span data-ttu-id="40b09-143">Etapa 4: unidade WebView2 com o Selenium e o Microsoft EdgeDriver</span><span class="sxs-lookup"><span data-stu-id="40b09-143">Step 4: Drive WebView2 with Selenium and Microsoft EdgeDriver</span></span>

1. <span data-ttu-id="40b09-144">Primeiro, crie o `EdgeOptions` objeto, copiando o código abaixo:</span><span class="sxs-lookup"><span data-stu-id="40b09-144">First, create the `EdgeOptions` object, by copying the code below:</span></span>

```csharp
static void Main(string[] args)
{
    // EdgeOptions() requires using OpenQA.Selenium.Edge
    // Construct EdgeOptions with is_legacy = false and the string "webview2"
    EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
```

<span data-ttu-id="40b09-145">O `EdgeOptions` objeto tem dois parâmetros:</span><span class="sxs-lookup"><span data-stu-id="40b09-145">The `EdgeOptions` object takes in two parameters:</span></span>
\
    **<span data-ttu-id="40b09-146">Os</span><span class="sxs-lookup"><span data-stu-id="40b09-146">Parameters:</span></span>**
    1. `is_legacy`<span data-ttu-id="40b09-147">: definido como `false` , que informa ao Selenium que você está direcionando o novo navegador Microsoft Edge baseado em Chromium.</span><span class="sxs-lookup"><span data-stu-id="40b09-147">: set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span>
    2. `"webview2"`<span data-ttu-id="40b09-148">: uma cadeia de caracteres que diz ao Selenium que você está dirigindo **WebView2**</span><span class="sxs-lookup"><span data-stu-id="40b09-148">: a string that tell Selenium you are driving **WebView2**</span></span>

2. <span data-ttu-id="40b09-149">Em seguida, defina `edgeOptions.BinaryLocation` como o caminho do arquivo do executável do seu projeto WebView2, crie uma cadeia de caracteres chamada `msedgedriverDir` que forneça o caminho do arquivo para o qual você instalou o [Microsoft Edge driver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads)e crie uma cadeia de caracteres chamada `msedgedriverExe` para armazenar o nome do executável do driver Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40b09-149">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project's executable, create a string called `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads), and create a string called `msedgedriverExe` to store the name of the Microsoft Edge Driver executable.</span></span> <span data-ttu-id="40b09-150">Por padrão, o executável é chamado `"msedgedriver.exe"` .</span><span class="sxs-lookup"><span data-stu-id="40b09-150">By default, the executable is called `"msedgedriver.exe"`.</span></span> <span data-ttu-id="40b09-151">Use essas duas cadeias de caracteres para construir o `EdgeDriverService` objeto conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="40b09-151">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span> <span data-ttu-id="40b09-152">Por fim, crie o `EdgeDriver` objeto usando `EdgeDriverService` e `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="40b09-152">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>

<span data-ttu-id="40b09-153">Você pode copiar e colar o seguinte código abaixo `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="40b09-153">You can copy and paste the following code underneath `edgeOptions`.</span></span> <span data-ttu-id="40b09-154">Certifique-se de especificar os caminhos de arquivo corretos para o executável do seu projeto e o executável do driver do Microsoft Edge em seu computador.</span><span class="sxs-lookup"><span data-stu-id="40b09-154">Make sure to specify the correct file paths to your project's executable and the Microsoft Edge Driver's executable on your machine.</span></span>

```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample's executable
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";

    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";

    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";

    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);

    EdgeDriver e = new EdgeDriver(service, edgeOptions);
```

3. <span data-ttu-id="40b09-155">Agora, o **EdgeDriver** está configurado para direcionar o **WebView2** em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="40b09-155">Now, **EdgeDriver** is configured to drive the **WebView2** in your project.</span></span> <span data-ttu-id="40b09-156">Por exemplo, se você estiver usando o **exemplo WebView2API**, poderá **navegar** para fazer uma <https://microsoft.com> chamada ```e.Url = @"https://www.microsoft.com";``` .</span><span class="sxs-lookup"><span data-stu-id="40b09-156">For example, if you are using the **WebView2API Sample**, you can **Navigate** to <https://microsoft.com> by calling ```e.Url = @"https://www.microsoft.com";```.</span></span> <span data-ttu-id="40b09-157">Você pode assistir **Selenium** Drive **WebView2** definindo um ponto de interrupção nesta linha e executando o projeto.</span><span class="sxs-lookup"><span data-stu-id="40b09-157">You can watch **Selenium** drive **WebView2** by setting a breakpoint on this line and running the project.</span></span>

```csharp
    //The following will Navigate the WebView2API Sample from bing.com to microsoft.com
    e.Url = @"https://www.microsoft.com";

    //This exits the edge driver
    e.Quit();
}
```

![texto alternativo](../media/webdriver/microsoft.png)

<span data-ttu-id="40b09-159">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="40b09-159">Congratulations!</span></span> <span data-ttu-id="40b09-160">Você automatizau com êxito um projeto do WebView2 e conduziu WebView2 usando o Selenium e o Microsoft Edge driver.</span><span class="sxs-lookup"><span data-stu-id="40b09-160">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>

## <span data-ttu-id="40b09-161">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="40b09-161">Next Steps</span></span>

<span data-ttu-id="40b09-162">Para saber mais:</span><span class="sxs-lookup"><span data-stu-id="40b09-162">To learn more:</span></span>

- <span data-ttu-id="40b09-163">Confira a [documentação do Selenium](https://www.selenium.dev/documentation/en/webdriver/) para obter uma visão abrangente do Selenium de APIs que está disponível para direcionar o WebView2 ou o Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="40b09-163">Check out [Selenium's documentation](https://www.selenium.dev/documentation/en/webdriver/) for a comprehensive look at the APIs Selenium has available for driving WebView2 or Microsoft Edge (Chromium)</span></span>
- <span data-ttu-id="40b09-164">Saiba mais sobre o controle [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) e como usá-lo ao inserir conteúdo da Web em seu aplicativo nativo</span><span class="sxs-lookup"><span data-stu-id="40b09-164">Learn more about [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) control and how to use it when embedding web content in your native app</span></span>
- <span data-ttu-id="40b09-165">Confira a [documentação do driver Microsoft Edge](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) para saber mais sobre como automatizar o Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="40b09-165">Check out [documentation for Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) to learn more about automating Microsoft Edge (Chromium)</span></span>

## <span data-ttu-id="40b09-166">Entrar em contato com a equipe do WebView2</span><span class="sxs-lookup"><span data-stu-id="40b09-166">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="40b09-167">Ajude-nos a criar uma experiência WebView2 mais rica compartilhando seus comentários!</span><span class="sxs-lookup"><span data-stu-id="40b09-167">Help us build a richer WebView2 experience by sharing your feedback!</span></span> <span data-ttu-id="40b09-168">Acesse nosso [repositório de comentários](https://github.com/MicrosoftEdge/WebViewFeedback) para enviar solicitações de recursos ou relatórios de erros ou para pesquisar problemas conhecidos.</span><span class="sxs-lookup"><span data-stu-id="40b09-168">Visit our [feedback repo](https://github.com/MicrosoftEdge/WebViewFeedback) to submit feature requests or bug reports or to search for known issues.</span></span>
