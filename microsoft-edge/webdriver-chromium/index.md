---
description: Saiba como testar seu site ou aplicativo no Microsoft Edge ou automatizar o navegador com o WebDriver
title: Usar o WebDriver (Chromium) para automação de teste
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento na Web, html, css, javascript, desenvolvedor, webdriver, selenium, teste, ferramentas, automação, teste
ms.openlocfilehash: b3b8a4ef2174c7f313fe9ee71bedbdf5e2f9b771
ms.sourcegitcommit: f95812c4e1b7277f67c6c4891be2779cc1b5bdf1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/18/2021
ms.locfileid: "11343783"
---
# <span data-ttu-id="275eb-104">Usar o WebDriver (Chromium) para automação de teste</span><span class="sxs-lookup"><span data-stu-id="275eb-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="275eb-105">O WebDriver permite que os desenvolvedores criem testes automatizados que simulam a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="275eb-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="275eb-106">Testes e simulações do WebDriver são diferentes dos testes de unidade JavaScript das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="275eb-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="275eb-107">Acessa a funcionalidade e as informações não disponíveis para JavaScript em execução em navegadores.</span><span class="sxs-lookup"><span data-stu-id="275eb-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="275eb-108">Simula eventos do usuário ou eventos no nível do sistema operacional com mais precisão.</span><span class="sxs-lookup"><span data-stu-id="275eb-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="275eb-109">Gerencia várias janelas, guias e páginas da Web em uma única sessão de teste.</span><span class="sxs-lookup"><span data-stu-id="275eb-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="275eb-110">Executa várias sessões do Microsoft Edge em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="275eb-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="275eb-111">A seção a seguir descreve como começar a usar o WebDriver para Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="275eb-112">Instalar o Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="275eb-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="275eb-113">Certifique-se [de instalar o Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="275eb-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="275eb-114">Para confirmar se você tem o Microsoft Edge \(Chromium\) instalado, navegue até e verifique se o número da versão é `edge://settings/help` a versão 75 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="275eb-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is version 75 or later.</span></span>  

## <span data-ttu-id="275eb-115">Baixar o Driver do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="275eb-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="275eb-116">Para começar a automatizar testes, use as etapas a seguir para garantir que a versão do WebDriver instalada corresponde à versão do navegador.</span><span class="sxs-lookup"><span data-stu-id="275eb-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="275eb-117">Para exibir a versão do Microsoft Edge, navegue até `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="275eb-117">To display the version of Microsoft Edge, navigate to `edge://settings/help`.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="O número de build do Microsoft Edge Canary em 10 de fevereiro de 2021" lightbox="./media/microsoft-edge-version.msft.png":::
       <span data-ttu-id="275eb-119">O número de build do Microsoft Edge Canary em 10 de fevereiro de 2021</span><span class="sxs-lookup"><span data-stu-id="275eb-119">The build number for Microsoft Edge Canary on February 10, 2021</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="275eb-120">Navegue [até o Driver do Microsoft Edge,][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]na seção **Downloads,** e baixe o WebDriver que corresponde ao número de versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="275eb-120">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver], under the **Downloads** section, and download the WebDriver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="A seção Downloads no Driver do Microsoft Edge" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="275eb-122">A **seção Downloads** no [Driver do Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="275eb-122">The **Downloads** section on [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span></span>  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  

## <span data-ttu-id="275eb-123">Escolher uma associação de idioma do WebDriver</span><span class="sxs-lookup"><span data-stu-id="275eb-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="275eb-124">O último componente que você deve baixar é um driver de cliente específico da linguagem para traduzir seu código \(Python, Java, C\#, Ruby, JavaScript\) em comandos que o Microsoft Edge Driver executa no Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="275eb-125">[Baixe a associação de idioma do WebDriver de sua escolha.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="275eb-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="275eb-126">A equipe do Microsoft Edge recomenda [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] ou posterior, porque dá suporte ao Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-126">The Microsoft Edge team recommends [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="275eb-127">No entanto, você pode controlar o Microsoft Edge \(Chromium\) em todas as versões mais antigas do Selenium, incluindo a versão estável atual do Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="275eb-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="275eb-128">Se você tiver automatizado ou testado anteriormente o Microsoft Edge \(Chromium\) usando e classes, o código do WebDriver não será executado no `ChromeDriver` `ChromeOptions` Microsoft Edge Versão 80 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="275eb-128">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="275eb-129">Para resolver o problema, atualize seus testes para usar a `EdgeOptions` classe e baixe o Driver do Microsoft [Edge.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="275eb-129">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="275eb-130">Usar Selenium 3</span><span class="sxs-lookup"><span data-stu-id="275eb-130">Use Selenium 3</span></span>  

<span data-ttu-id="275eb-131">Se você já usa [Selenium 3,][|::ref1::|]talvez tenha testes de navegador existentes e queira adicionar cobertura para o Microsoft Edge \(Chromium\) sem alterar sua versão de Selenium.</span><span class="sxs-lookup"><span data-stu-id="275eb-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="275eb-132">Para usar [Selenium 3][|::ref2::|] para gravar testes automatizados para o Microsoft Edge \(EdgeHTML\) e o Microsoft Edge \(Chromium\), instale o pacote [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar o driver atualizado.</span><span class="sxs-lookup"><span data-stu-id="275eb-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="275eb-133">As classes e as classes incluídas nas ferramentas são totalmente compatíveis com `EdgeDriver` `EdgeDriverService` os equivalentes integrados no Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="275eb-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="275eb-134">Use as etapas a seguir para adicionar as [Ferramentas Selenium do Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] e [Selenium 3][|::ref3::|] ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="275eb-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<span data-ttu-id="275eb-135">C#</span><span class="sxs-lookup"><span data-stu-id="275eb-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="275eb-136">Adicione os [pacotes Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] e [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] ao seu projeto .NET usando a [CLI do NuGet][NugetCLI] ou [o Visual Studio.][VisualStudio]</span><span class="sxs-lookup"><span data-stu-id="275eb-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="275eb-137">Python</span><span class="sxs-lookup"><span data-stu-id="275eb-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="275eb-138">Use [pip][PythonPip] para instalar os [pacotes msedge-selenium-tools][PythonSeleniumTools] e [selenium.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="275eb-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="275eb-139">Java</span><span class="sxs-lookup"><span data-stu-id="275eb-139">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="275eb-140">Se seu projeto Java usa Maven, copie e copie e copie a seguinte dependência ao seu arquivo para adicionar `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span><span class="sxs-lookup"><span data-stu-id="275eb-140">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="275eb-141">O pacote Java também está disponível para download diretamente na página Ferramentas [Selenium para Lançamentos do Microsoft Edge.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="275eb-141">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<span data-ttu-id="275eb-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="275eb-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="275eb-143">Use [npm][JavaScript|::ref4::|] para instalar os [pacotes edge-selenium-tools][JavaScriptSeleniumTools] e [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="275eb-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="275eb-144">Automatizar o Microsoft Edge (Chromium) com o WebDriver</span><span class="sxs-lookup"><span data-stu-id="275eb-144">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="275eb-145">Para automatizar um navegador usando o WebDriver, primeiro você deve iniciar uma sessão do WebDriver usando sua associação de idioma preferencial do WebDriver.</span><span class="sxs-lookup"><span data-stu-id="275eb-145">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="275eb-146">Uma sessão é uma única instância em execução de um navegador controlado usando comandos do WebDriver.</span><span class="sxs-lookup"><span data-stu-id="275eb-146">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="275eb-147">Inicie uma sessão do WebDriver para iniciar uma nova instância do navegador.</span><span class="sxs-lookup"><span data-stu-id="275eb-147">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="275eb-148">A instância do navegador lançada permanece aberta até que você feche a sessão do WebDriver.</span><span class="sxs-lookup"><span data-stu-id="275eb-148">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="275eb-149">O conteúdo a seguir orienta você a usar Selenium para iniciar uma sessão do WebDriver com o Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-149">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="275eb-150">Você pode executar os exemplos usando Selenium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="275eb-150">You may run the examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="275eb-151">Para usar com Selenium 3, o pacote [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="275eb-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="275eb-152">Automatizar o Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="275eb-152">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="275eb-153">Selenium usa a `EdgeDriver` classe para gerenciar uma sessão do Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-153">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="275eb-154">Para iniciar uma sessão e automatizar o Microsoft Edge \(Chromium\), crie um novo objeto e passe um objeto para ele com a propriedade `EdgeDriver` `EdgeOptions` definida como `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="275eb-154">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="275eb-155">C#</span><span class="sxs-lookup"><span data-stu-id="275eb-155">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="275eb-156">Python</span><span class="sxs-lookup"><span data-stu-id="275eb-156">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="275eb-157">Java</span><span class="sxs-lookup"><span data-stu-id="275eb-157">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="275eb-158">A `EdgeDriver` classe só dá suporte ao Microsoft Edge \(Chromium\) e não dá suporte ao Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="275eb-158">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="275eb-159">Para uso básico, você pode criar um `EdgeDriver` sem fornecer `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="275eb-159">For basic usage, you may create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<span data-ttu-id="275eb-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="275eb-160">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="275eb-161">Se o administrador de IT definiu a política [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] como , o Driver do Microsoft Edge é impedido de conduzir o `2`  [Microsoft][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] Edge \(Chromium\), porque o driver usa o [Microsoft Edge DevTools][DevtoolsIndex].</span><span class="sxs-lookup"><span data-stu-id="275eb-161">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="275eb-162">Verifique se [a política DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] está definida para `0` ou para `1` automatizar o Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="275eb-162">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <span data-ttu-id="275eb-163">Escolher binários específicos do navegador (somente Chromium)</span><span class="sxs-lookup"><span data-stu-id="275eb-163">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="275eb-164">Você pode iniciar uma sessão do WebDriver com binários específicos do Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-164">You may start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="275eb-165">Por exemplo, você pode executar testes usando os canais de visualização do [Microsoft Edge,][MicrosoftedgeinsiderDownload] como o Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="275eb-165">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="275eb-166">C#</span><span class="sxs-lookup"><span data-stu-id="275eb-166">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="275eb-167">Python</span><span class="sxs-lookup"><span data-stu-id="275eb-167">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="275eb-168">Java</span><span class="sxs-lookup"><span data-stu-id="275eb-168">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="275eb-169">JavaScript</span><span class="sxs-lookup"><span data-stu-id="275eb-169">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="275eb-170">Personalizar o Serviço de Driver do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="275eb-170">Customize the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="275eb-171">C#</span><span class="sxs-lookup"><span data-stu-id="275eb-171">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="275eb-172">Quando você usa a classe para criar uma instância de classe, ela cria e inicia a classe apropriada para `EdgeOptions` `EdgeDriver` o Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou o Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-172">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="275eb-173">Se você quiser criar um , use o método `EdgeDriverService` para criar um configurado para o Microsoft Edge `CreateChromiumService()` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-173">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="275eb-174">O `CreateChromiumService()` método é útil quando você precisa adicionar personalizações.</span><span class="sxs-lookup"><span data-stu-id="275eb-174">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="275eb-175">Por exemplo, o código a seguir inicia a saída detalhada do log.</span><span class="sxs-lookup"><span data-stu-id="275eb-175">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="275eb-176">Você não precisa fornecer o `EdgeOptions` objeto quando passar para a `EdgeDriverService` `EdgeDriver` instância.</span><span class="sxs-lookup"><span data-stu-id="275eb-176">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="275eb-177">A `EdgeDriver` classe usa as opções padrão para o Microsoft Edge \(EdgeHTML\) ou o Microsoft Edge \(Chromium\) com base no serviço que você fornece.</span><span class="sxs-lookup"><span data-stu-id="275eb-177">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="275eb-178">No entanto, se você quiser fornecer as duas classes, verifique se ambas estão `EdgeDriverService` `EdgeOptions` configuradas para a mesma versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="275eb-178">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="275eb-179">Por exemplo, você pode usar uma classe padrão do Microsoft Edge \(EdgeHTML\) e propriedades `EdgeDriverService` do Chromium na `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="275eb-179">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="275eb-180">A `EdgeDriver` classe lança um erro para impedir o uso de versões diferentes.</span><span class="sxs-lookup"><span data-stu-id="275eb-180">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="275eb-181">Python</span><span class="sxs-lookup"><span data-stu-id="275eb-181">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="275eb-182">Quando você usa o Python, `Edge` o objeto cria e gerencia o `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="275eb-182">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="275eb-183">Para configurar o `EdgeService` , passe argumentos extras para `Edge` o objeto conforme indicado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="275eb-183">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="275eb-184">Java</span><span class="sxs-lookup"><span data-stu-id="275eb-184">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="275eb-185">Use o `createDefaultService()` método para criar um configurado para o Microsoft Edge `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="275eb-185">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="275eb-186">Use as propriedades do sistema Java para personalizar serviços de driver em Java.</span><span class="sxs-lookup"><span data-stu-id="275eb-186">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="275eb-187">Por exemplo, o código a seguir usa a `"webdriver.edge.verboseLogging"` propriedade para ativar a saída do log detalhado.</span><span class="sxs-lookup"><span data-stu-id="275eb-187">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<span data-ttu-id="275eb-188">JavaScript</span><span class="sxs-lookup"><span data-stu-id="275eb-188">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="275eb-189">Ao usar JavaScript, crie e configure um `Service` com a `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="275eb-189">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="275eb-190">Opcionalmente, você pode passar o objeto para o objeto, que inicia `Service` `Driver` \(e interrompe\) o serviço para você.</span><span class="sxs-lookup"><span data-stu-id="275eb-190">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="275eb-191">Para configurar `Service` o método , execute outro método na classe antes de usar o `ServiceBuilder` `build()` método.</span><span class="sxs-lookup"><span data-stu-id="275eb-191">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="275eb-192">Em seguida, `service` passe o parâmetro como um no `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="275eb-192">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="275eb-193">Usar Chromium-Specific opções</span><span class="sxs-lookup"><span data-stu-id="275eb-193">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="275eb-194">Se você definir a propriedade como , você pode usar a classe para acessar as mesmas propriedades e métodos específicos do Chromium que são usados quando você automatizar outros navegadores `UseChromium` `true` `EdgeOptions` Chromium. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="275eb-194">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="275eb-195">C#</span><span class="sxs-lookup"><span data-stu-id="275eb-195">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="275eb-196">Python</span><span class="sxs-lookup"><span data-stu-id="275eb-196">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="275eb-197">Java</span><span class="sxs-lookup"><span data-stu-id="275eb-197">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<span data-ttu-id="275eb-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="275eb-198">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="275eb-199">Se a propriedade estiver definida como , você não poderá usar propriedades e métodos para `UseChromium` `true` o Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="275eb-199">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="275eb-200">Outras opções de instalação do WebDriver</span><span class="sxs-lookup"><span data-stu-id="275eb-200">Other WebDriver installation options</span></span>  

### <span data-ttu-id="275eb-201">Rêo</span><span class="sxs-lookup"><span data-stu-id="275eb-201">Chocolatey</span></span>  

<span data-ttu-id="275eb-202">Se você usar [Ay como][Chocolatey] seu gerenciador de pacotes, execute o seguinte comando para instalar o Microsoft Edge Driver.</span><span class="sxs-lookup"><span data-stu-id="275eb-202">If you use [Chocolatey][Chocolatey] as your package manager, run the following command to install the Microsoft Edge Driver.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="275eb-203">Para obter mais informações, navegue [até Selenium Chromium Edge Driver em Mila .][ChocolateyPackagesSeleniumChromiumEdgeDriver]</span><span class="sxs-lookup"><span data-stu-id="275eb-203">For more information, navigate to [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="275eb-204">Docker</span><span class="sxs-lookup"><span data-stu-id="275eb-204">Docker</span></span>  

<span data-ttu-id="275eb-205">Se você usar [o Docker,][DockerHub]execute o seguinte comando para baixar uma imagem pré-configurada com o Microsoft Edge \(Chromium\) e o Driver do [Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pré-instalados.</span><span class="sxs-lookup"><span data-stu-id="275eb-205">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="275eb-206">Para obter mais informações, navegue até o contêiner [msedgedriver no Hub do Docker.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="275eb-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="275eb-207">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="275eb-207">Next steps</span></span>  

<span data-ttu-id="275eb-208">Para saber mais sobre o WebDriver e como escrever testes automatizados do WebDriver usando Selenium, navegue até a documentação [Selenium.][SeleniumDocumentation]</span><span class="sxs-lookup"><span data-stu-id="275eb-208">To learn more about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <span data-ttu-id="275eb-209">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="275eb-209">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="275eb-210">A equipe do Microsoft Edge está ansioso para ouvir seus comentários sobre como usar o WebDriver, Selenium e Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="275eb-210">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="275eb-211">Para enviar suas perguntas e comentários à equipe, escolha o ícone Enviar **Comentários** no Microsoft Edge DevTools ou envie um tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="275eb-211">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Comentários no Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="275eb-213">O **ícone Enviar Comentários** no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="275eb-213">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Recursos e edgeOptions | Microsoft Docs"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge - Políticas | Microsoft Docs"  

[Chocolatey]: https://chocolatey.org "| Software Quey"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Driver de borda Selenium Chromium | Rêo"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub do Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Desenvolvedor da Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Baixar Novo Navegador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | Galeria NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | Galeria NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | Galeria NuGet"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Selenium.WebDriver 4.0.0-alpha07 | Galeria NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "O Projeto de Automação do Navegador Selenium | Documentação para Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selenium"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem | Wikipédia"  
