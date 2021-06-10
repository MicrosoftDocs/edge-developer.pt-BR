---
description: Saiba como testar seu site ou aplicativo Microsoft Edge automatizar o navegador com o WebDriver
title: Usar o WebDriver (Chromium) para automação de teste
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento da Web, html, css, javascript, desenvolvedor, webdriver, selenium, teste, ferramentas, automação, teste
ms.openlocfilehash: 3865162b8227db2f0cfa051801a5de28ecf4b9d1
ms.sourcegitcommit: 3094c972532bc89dcb429d26880c873809fd1ab8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "11599454"
---
# <a name="use-webdriver-chromium-for-test-automation"></a><span data-ttu-id="795d4-104">Usar o WebDriver (Chromium) para automação de teste</span><span class="sxs-lookup"><span data-stu-id="795d4-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="795d4-105">O WebDriver permite que os desenvolvedores criem testes automatizados que simulam a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="795d4-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="795d4-106">Testes e simulações do WebDriver diferem dos testes de unidade JavaScript das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="795d4-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="795d4-107">Acessa a funcionalidade e as informações não disponíveis para JavaScript em execução em navegadores.</span><span class="sxs-lookup"><span data-stu-id="795d4-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="795d4-108">Simula eventos do usuário ou eventos no nível do sistema operacional com mais precisão.</span><span class="sxs-lookup"><span data-stu-id="795d4-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="795d4-109">Gerencia várias janelas, guias e páginas da Web em uma única sessão de teste.</span><span class="sxs-lookup"><span data-stu-id="795d4-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="795d4-110">Executa várias sessões de Microsoft Edge em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="795d4-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  

## <a name="relationship-between-webdriver-and-other-software"></a><span data-ttu-id="795d4-111">Relação entre WebDriver e outros softwares</span><span class="sxs-lookup"><span data-stu-id="795d4-111">Relationship between WebDriver and other software</span></span>

<span data-ttu-id="795d4-112">Para automatizar Microsoft Edge com o WebDriver para simular a interação do usuário, você precisa de três componentes:</span><span class="sxs-lookup"><span data-stu-id="795d4-112">To automate Microsoft Edge with WebDriver to simulate user interaction, you need 3 components:</span></span>

*  <span data-ttu-id="795d4-113">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="795d4-113">Microsoft Edge</span></span>
*  <span data-ttu-id="795d4-114">Driver do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="795d4-114">Microsoft Edge Driver</span></span>
*  <span data-ttu-id="795d4-115">Uma estrutura de teste do WebDriver, como Selenium</span><span class="sxs-lookup"><span data-stu-id="795d4-115">A WebDriver testing framework, such as Selenium</span></span>

<span data-ttu-id="795d4-116">A relação funcional entre WebDriver, Microsoft Edge Driver, Selenium e Internet Explorer Driver é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="795d4-116">The functional relationship between WebDriver, Microsoft Edge Driver, Selenium, and Internet Explorer Driver is as follows.</span></span>

| <span data-ttu-id="795d4-117">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="795d4-117">Technology</span></span> | <span data-ttu-id="795d4-118">Função</span><span class="sxs-lookup"><span data-stu-id="795d4-118">Role</span></span> |
|---|---|
| <span data-ttu-id="795d4-119">WebDriver</span><span class="sxs-lookup"><span data-stu-id="795d4-119">WebDriver</span></span> | <span data-ttu-id="795d4-120">Um padrão W3C para um protocolo de fio de plataforma e idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="795d4-120">A W3C standard for a platform- and language-neutral wire protocol.</span></span>  <span data-ttu-id="795d4-121">Esse protocolo permite que programas fora do processo instruam remotamente o comportamento dos navegadores da Web.</span><span class="sxs-lookup"><span data-stu-id="795d4-121">This protocol allows out-of-process programs to remotely instruct the behavior of web browsers.</span></span> |
| <span data-ttu-id="795d4-122">Driver do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="795d4-122">Microsoft Edge Driver</span></span> | <span data-ttu-id="795d4-123">Implementação da Microsoft do protocolo WebDriver especificamente para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="795d4-123">Microsoft's implementation of the WebDriver protocol specifically for Microsoft Edge.</span></span> <span data-ttu-id="795d4-124">Os autores de teste escrevem testes que usam comandos WebDriver que Microsoft Edge Driver recebe.</span><span class="sxs-lookup"><span data-stu-id="795d4-124">Test authors write tests that use WebDriver commands that Microsoft Edge Driver receives.</span></span> <span data-ttu-id="795d4-125">Microsoft Edge O driver é responsável por comunicar esse comando ao navegador.</span><span class="sxs-lookup"><span data-stu-id="795d4-125">Microsoft Edge Driver is then responsible for communicating that command to the browser.</span></span> |
| <span data-ttu-id="795d4-126">Selenium</span><span class="sxs-lookup"><span data-stu-id="795d4-126">Selenium</span></span> | <span data-ttu-id="795d4-127">Uma estrutura de teste popular do WebDriver que os autores de teste usam para gravar testes de ponta a ponta e automatizar navegadores.</span><span class="sxs-lookup"><span data-stu-id="795d4-127">A popular WebDriver testing framework that test authors use to write end-to-end tests and automate browsers.</span></span> <span data-ttu-id="795d4-128">Selenium pode ser usado em qualquer plataforma e está disponível em Java, Python, C#, Ruby e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="795d4-128">Selenium can be used on any platform, and is available in Java, Python, C#, Ruby, and JavaScript.</span></span> |
| <span data-ttu-id="795d4-129">Internet Explorer Driver</span><span class="sxs-lookup"><span data-stu-id="795d4-129">Internet Explorer Driver</span></span> | <span data-ttu-id="795d4-130">Uma implementação do protocolo WebDriver especificamente para o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="795d4-130">An implementation of the WebDriver protocol specifically for Internet Explorer.</span></span> <span data-ttu-id="795d4-131">Esse produto é mantido pelo projeto Selenium.</span><span class="sxs-lookup"><span data-stu-id="795d4-131">This product is maintained by the Selenium project.</span></span> <span data-ttu-id="795d4-132">Para executar testes de ponta a ponta herdou para o Internet Explorer, recomendamos usar o Internet Explorer Driver.</span><span class="sxs-lookup"><span data-stu-id="795d4-132">To run legacy end-to-end tests for Internet Explorer, we recommend using Internet Explorer Driver.</span></span> |

<span data-ttu-id="795d4-133">As seções a seguir descrevem como começar a usar o WebDriver para Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-133">The following sections describe how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <a name="install-microsoft-edge-chromium"></a><span data-ttu-id="795d4-134">Instalar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="795d4-134">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="795d4-135">Certifique-se de [instalar Microsoft Edge (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="795d4-135">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="795d4-136">Para confirmar se você Microsoft Edge \(Chromium\) instalado, navegue até e verifique se o número da versão é a versão `edge://settings/help` 75 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="795d4-136">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is version 75 or later.</span></span>  

## <a name="download-microsoft-edge-driver"></a><span data-ttu-id="795d4-137">Baixar o Driver do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="795d4-137">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="795d4-138">Para começar a automatizar testes, use as etapas a seguir para garantir que a versão do WebDriver instalada corresponde à versão do navegador.</span><span class="sxs-lookup"><span data-stu-id="795d4-138">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="795d4-139">Encontre sua versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="795d4-139">Find your version of Microsoft Edge.</span></span>  
    1.  <span data-ttu-id="795d4-140">Navegue até `edge://settings/help`.</span><span class="sxs-lookup"><span data-stu-id="795d4-140">Navigate to `edge://settings/help`.</span></span>  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="O número de com build para Microsoft Edge em 15 de abril de 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           <span data-ttu-id="795d4-142">O número de com build para Microsoft Edge em 15 de abril de 2021</span><span class="sxs-lookup"><span data-stu-id="795d4-142">The build number for Microsoft Edge on April 15, 2021</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="795d4-143">Navegue [até Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="795d4-143">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  
1.  <span data-ttu-id="795d4-144">Navegue **até Obter a versão mais recente**.</span><span class="sxs-lookup"><span data-stu-id="795d4-144">Navigate to **Get the latest version**.</span></span>  
1.  <span data-ttu-id="795d4-145">Escolha a com build do canal que corresponde ao número de versão Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="795d4-145">Choose the build of channel that matches your version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="A seção Obter a versão mais recente na página Microsoft Edge Driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="795d4-147">A **seção Obter a versão mais** recente na página Microsoft Edge [Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="795d4-147">The **Get the latest version** section on the [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] webpage</span></span>  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a><span data-ttu-id="795d4-148">Escolha uma associação de idioma do WebDriver</span><span class="sxs-lookup"><span data-stu-id="795d4-148">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="795d4-149">O último componente que você deve baixar é um driver de cliente específico do idioma para traduzir seu código \(Python, Java, C\#, Ruby, JavaScript\) em comandos que o driver do Microsoft Edge executa em Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-149">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="795d4-150">[Baixe a associação de idioma WebDriver de sua escolha][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="795d4-150">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="795d4-151">A equipe Microsoft Edge recomenda [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] ou posterior, porque suporta Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-151">The Microsoft Edge team recommends [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="795d4-152">No entanto, você pode controlar Microsoft Edge \(Chromium\) em todas as versões mais antigas do Selenium, incluindo a versão selenium 3 estável atual.</span><span class="sxs-lookup"><span data-stu-id="795d4-152">However, you can control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="795d4-153">Se você tiver automatizado ou testado anteriormente Microsoft Edge \(Chromium\) usando e classes, seu código WebDriver não será executado no Microsoft Edge `ChromeDriver` `ChromeOptions` Versão 80 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="795d4-153">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="795d4-154">Para resolver o problema, atualize seus testes para usar a `EdgeOptions` classe e baixe Microsoft Edge [Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="795d4-154">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <a name="using-selenium-4"></a><span data-ttu-id="795d4-155">Usando Selenium 4</span><span class="sxs-lookup"><span data-stu-id="795d4-155">Using Selenium 4</span></span>

<span data-ttu-id="795d4-156">Selenium 4 tem suporte integrado para Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="795d4-156">Selenium 4 has built-in support for Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="795d4-157">Para instalar o Selenium 4, navegue até [Installing Selenium libraries][SeleniumInstallingLibraries].</span><span class="sxs-lookup"><span data-stu-id="795d4-157">To install Selenium 4, navigate to [Installing Selenium libraries][SeleniumInstallingLibraries].</span></span>

<span data-ttu-id="795d4-158">Quando você usa Selenium 4, não precisa usar As Ferramentas de Selenium para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="795d4-158">When you use Selenium 4, you don't need to use Selenium Tools for Microsoft Edge.</span></span>  <span data-ttu-id="795d4-159">Selenium Tools for Microsoft Edge são somente para Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="795d4-159">Selenium Tools for Microsoft Edge are for Selenium 3 only.</span></span>  <span data-ttu-id="795d4-160">Se você tentar usar Selenium 4 com Ferramentas selenium para Microsoft Edge e tentar criar uma nova instância, você obterá `EdgeDriver` o seguinte erro: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'` .</span><span class="sxs-lookup"><span data-stu-id="795d4-160">If you try to use Selenium 4 with Selenium Tools for Microsoft Edge and try to create a new `EdgeDriver` instance, you get the following error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'`.</span></span>  

<span data-ttu-id="795d4-161">Se você estiver usando o Selenium 4 e receber esse erro, remova do seu projeto e certifique-se de estar usando o oficial e as classes do `Microsoft.Edge.SeleniumTools` `EdgeOptions` `EdgeDriver` `OpenQA.Selenium.Edge` namespace.</span><span class="sxs-lookup"><span data-stu-id="795d4-161">If you're using Selenium 4 and get this error, remove `Microsoft.Edge.SeleniumTools` from your project, and make sure you're using the official `EdgeOptions` and `EdgeDriver` classes from the `OpenQA.Selenium.Edge` namespace.</span></span>

### <a name="using-selenium-3"></a><span data-ttu-id="795d4-162">Usando Selenium 3</span><span class="sxs-lookup"><span data-stu-id="795d4-162">Using Selenium 3</span></span>  

<span data-ttu-id="795d4-163">Se você já usa [Selenium 3][|::ref1::|], pode ter testes de navegador existentes e deseja adicionar cobertura para Microsoft Edge \(Chromium\) sem alterar sua versão do Selenium.</span><span class="sxs-lookup"><span data-stu-id="795d4-163">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="795d4-164">Para usar [o Selenium 3][|::ref2::|] para gravar testes automatizados para o Microsoft Edge \(EdgeHTML\) e o Microsoft Edge \(Chromium\), instale o pacote [Ferramentas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar o driver atualizado.</span><span class="sxs-lookup"><span data-stu-id="795d4-164">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="795d4-165">As `EdgeDriver` classes `EdgeDriverService` e incluídas nas ferramentas são totalmente compatíveis com os equivalentes integrados no Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="795d4-165">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="795d4-166">Use as etapas a seguir para adicionar as [Ferramentas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] e [Selenium 3][|::ref3::|] ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="795d4-166">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<a name="c"></a><span data-ttu-id="795d4-167">C#</span><span class="sxs-lookup"><span data-stu-id="795d4-167">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="795d4-168">Adicione os [pacotes Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] e [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] ao seu projeto .NET usando o [NuGet CLI][NugetCLI] ou [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="795d4-168">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<a name="python"></a><span data-ttu-id="795d4-169">Python</span><span class="sxs-lookup"><span data-stu-id="795d4-169">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="795d4-170">Use [pip][PythonPip] para instalar os [pacotes msedge-selenium-tools][PythonSeleniumTools] e [selenium.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="795d4-170">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a><span data-ttu-id="795d4-171">Java</span><span class="sxs-lookup"><span data-stu-id="795d4-171">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="795d4-172">Se seu projeto Java usar Maven, copie e colar a seguinte dependência ao seu arquivo para adicionar `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span><span class="sxs-lookup"><span data-stu-id="795d4-172">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="795d4-173">O Java também está disponível para download diretamente na página [Ferramentas de Selenium para Microsoft Edge Versões.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="795d4-173">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<a name="javascript"></a><span data-ttu-id="795d4-174">JavaScript</span><span class="sxs-lookup"><span data-stu-id="795d4-174">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="795d4-175">Use [npm][JavaScript|::ref4::|] para instalar [os pacotes edge-selenium-tools][JavaScriptSeleniumTools] e [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="795d4-175">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a><span data-ttu-id="795d4-176">Automatizar Microsoft Edge (Chromium) com o WebDriver</span><span class="sxs-lookup"><span data-stu-id="795d4-176">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="795d4-177">Para automatizar um navegador usando o WebDriver, primeiro você deve iniciar uma sessão do WebDriver usando sua associação de idioma WebDriver preferida.</span><span class="sxs-lookup"><span data-stu-id="795d4-177">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="795d4-178">Uma sessão é uma única instância em execução de um navegador controlado usando comandos WebDriver.</span><span class="sxs-lookup"><span data-stu-id="795d4-178">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="795d4-179">Inicie uma sessão do WebDriver para iniciar uma nova instância do navegador.</span><span class="sxs-lookup"><span data-stu-id="795d4-179">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="795d4-180">A instância do navegador lançada permanece aberta até que você feche a sessão do WebDriver.</span><span class="sxs-lookup"><span data-stu-id="795d4-180">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="795d4-181">O conteúdo a seguir orienta você a usar Selenium para iniciar uma sessão do WebDriver com Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-181">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="795d4-182">Você pode executar os exemplos usando Selenium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="795d4-182">You can run the examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="795d4-183">Para usar com Selenium 3, o pacote [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="795d4-183">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <a name="automate-microsoft-edge-chromium"></a><span data-ttu-id="795d4-184">Automatizar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="795d4-184">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="795d4-185">Selenium usa a `EdgeDriver` classe para gerenciar uma sessão Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-185">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="795d4-186">Para iniciar uma sessão e automatizar Microsoft Edge \(Chromium\), crie um novo objeto e passe um objeto com a propriedade `EdgeDriver` `EdgeOptions` definida como `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="795d4-186">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<a name="c"></a><span data-ttu-id="795d4-187">C#</span><span class="sxs-lookup"><span data-stu-id="795d4-187">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="795d4-188">Python</span><span class="sxs-lookup"><span data-stu-id="795d4-188">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="795d4-189">Java</span><span class="sxs-lookup"><span data-stu-id="795d4-189">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="795d4-190">A classe dá suporte Microsoft Edge \(Chromium\) e não dá suporte `EdgeDriver` Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="795d4-190">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="795d4-191">Para uso básico, você pode criar um `EdgeDriver` sem fornecer `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="795d4-191">For basic usage, you can create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a><span data-ttu-id="795d4-192">JavaScript</span><span class="sxs-lookup"><span data-stu-id="795d4-192">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="795d4-193">Se o administrador de IT tiver definido a política [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] como , o driver do Microsoft Edge será impedido de conduzir o Microsoft Edge \(Chromium\), porque o driver usa o `2` Microsoft Edge [DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="795d4-193">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="795d4-194">Verifique se [a política DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] está definida como ou para automatizar Microsoft Edge `0` `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="795d4-194">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <a name="choose-specific-browser-binaries-chromium-only"></a><span data-ttu-id="795d4-195">Escolha Binários específicos do navegador (somente Chromium))</span><span class="sxs-lookup"><span data-stu-id="795d4-195">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="795d4-196">Você pode iniciar uma sessão do WebDriver com binários Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-196">You can start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="795d4-197">Por exemplo, você pode executar testes usando os canais [Microsoft Edge de visualização,][MicrosoftedgeinsiderDownload] como Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="795d4-197">For example, you can run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<a name="c"></a><span data-ttu-id="795d4-198">C#</span><span class="sxs-lookup"><span data-stu-id="795d4-198">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="795d4-199">Python</span><span class="sxs-lookup"><span data-stu-id="795d4-199">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="795d4-200">Java</span><span class="sxs-lookup"><span data-stu-id="795d4-200">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a><span data-ttu-id="795d4-201">JavaScript</span><span class="sxs-lookup"><span data-stu-id="795d4-201">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a><span data-ttu-id="795d4-202">Personalizar o serviço Microsoft Edge driver</span><span class="sxs-lookup"><span data-stu-id="795d4-202">Customize the Microsoft Edge Driver Service</span></span>  

#### [<a name="c"></a><span data-ttu-id="795d4-203">C#</span><span class="sxs-lookup"><span data-stu-id="795d4-203">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="795d4-204">Quando você usa a classe para criar uma instância de classe, ela cria e inicia a classe apropriada para `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-204">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="795d4-205">Se você quiser criar um , use o método para criar um configurado para `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-205">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="795d4-206">O `CreateChromiumService()` método é útil quando você precisa adicionar personalizações.</span><span class="sxs-lookup"><span data-stu-id="795d4-206">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="795d4-207">Por exemplo, o código a seguir inicia a saída de log detalhado.</span><span class="sxs-lookup"><span data-stu-id="795d4-207">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="795d4-208">Você não precisa fornecer o `EdgeOptions` objeto quando passar para a `EdgeDriverService` `EdgeDriver` instância.</span><span class="sxs-lookup"><span data-stu-id="795d4-208">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="795d4-209">A classe usa as opções padrão `EdgeDriver` para Microsoft Edge \(EdgeHTML\) ou Microsoft Edge \(Chromium\) com base no serviço que você fornece.</span><span class="sxs-lookup"><span data-stu-id="795d4-209">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="795d4-210">No entanto, se você quiser fornecer ambas as classes, verifique se ambas estão configuradas para `EdgeDriverService` a mesma versão do `EdgeOptions` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="795d4-210">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="795d4-211">Por exemplo, você pode usar uma classe padrão Microsoft Edge \(EdgeHTML\) e Chromium `EdgeDriverService` propriedades na `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="795d4-211">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="795d4-212">A `EdgeDriver` classe lança um erro para impedir o uso de versões diferentes.</span><span class="sxs-lookup"><span data-stu-id="795d4-212">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<a name="python"></a><span data-ttu-id="795d4-213">Python</span><span class="sxs-lookup"><span data-stu-id="795d4-213">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="795d4-214">Quando você usa Python, `Edge` o objeto cria e gerencia o `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="795d4-214">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="795d4-215">Para configurar `EdgeService` o , passe argumentos extras para o objeto conforme indicado no código a `Edge` seguir.</span><span class="sxs-lookup"><span data-stu-id="795d4-215">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a><span data-ttu-id="795d4-216">Java</span><span class="sxs-lookup"><span data-stu-id="795d4-216">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="795d4-217">Use o método para criar um configurado para Microsoft Edge `createDefaultService()` `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="795d4-217">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="795d4-218">Use Java do sistema para personalizar os serviços de driver no Java.</span><span class="sxs-lookup"><span data-stu-id="795d4-218">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="795d4-219">Por exemplo, o código a seguir usa a `"webdriver.edge.verboseLogging"` propriedade para ativar a saída de log detalhado.</span><span class="sxs-lookup"><span data-stu-id="795d4-219">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a><span data-ttu-id="795d4-220">JavaScript</span><span class="sxs-lookup"><span data-stu-id="795d4-220">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="795d4-221">Ao usar JavaScript, crie e configure um `Service` com a `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="795d4-221">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="795d4-222">Opcionalmente, você pode passar o objeto para `Service` o `Driver` objeto, que inicia \(e para\) o serviço para você.</span><span class="sxs-lookup"><span data-stu-id="795d4-222">Optionally, you can pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="795d4-223">Para configurar `Service` o , execute outro método na classe antes de usar o `ServiceBuilder` `build()` método.</span><span class="sxs-lookup"><span data-stu-id="795d4-223">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="795d4-224">Em seguida, `service` passe o parâmetro como um no `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="795d4-224">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a><span data-ttu-id="795d4-225">Usar Chromium-Specific opções</span><span class="sxs-lookup"><span data-stu-id="795d4-225">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="795d4-226">Se você definir a propriedade como , você poderá usar a classe para acessar as mesmas propriedades e métodos específicos do Chromium que são usados quando você automatiza outros navegadores `UseChromium` `true` `EdgeOptions` Chromium. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="795d4-226">If you set the `UseChromium` property to `true`, you can use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<a name="c"></a><span data-ttu-id="795d4-227">C#</span><span class="sxs-lookup"><span data-stu-id="795d4-227">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a><span data-ttu-id="795d4-228">Python</span><span class="sxs-lookup"><span data-stu-id="795d4-228">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a><span data-ttu-id="795d4-229">Java</span><span class="sxs-lookup"><span data-stu-id="795d4-229">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a><span data-ttu-id="795d4-230">JavaScript</span><span class="sxs-lookup"><span data-stu-id="795d4-230">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="795d4-231">Se a propriedade estiver definida como , você não poderá usar propriedades e métodos para Microsoft Edge `UseChromium` `true` \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="795d4-231">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <a name="other-webdriver-installation-options"></a><span data-ttu-id="795d4-232">Outras opções de instalação do WebDriver</span><span class="sxs-lookup"><span data-stu-id="795d4-232">Other WebDriver installation options</span></span>  

### <a name="docker"></a><span data-ttu-id="795d4-233">Docker</span><span class="sxs-lookup"><span data-stu-id="795d4-233">Docker</span></span>  

<span data-ttu-id="795d4-234">Se você usar [o Docker,][DockerHub]execute o seguinte comando para baixar uma imagem pré-configurada com Microsoft Edge \(Chromium\) e [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pré-instalado.</span><span class="sxs-lookup"><span data-stu-id="795d4-234">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="795d4-235">Para obter mais informações, navegue até o [contêiner msedgedriver no Hub do Docker.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="795d4-235">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <a name="testing-internet-explorer"></a><span data-ttu-id="795d4-236">Testando o Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="795d4-236">Testing Internet Explorer</span></span>

<span data-ttu-id="795d4-237">Mesmo que Microsoft Edge suporte ao modo IE, você não pode usar o driver Microsoft Edge com Microsoft Edge para testar sites no modo IE.</span><span class="sxs-lookup"><span data-stu-id="795d4-237">Even though Microsoft Edge supports IE Mode, you can't use Microsoft Edge Driver with Microsoft Edge to test sites in IE Mode.</span></span>  <span data-ttu-id="795d4-238">Para testar sites que exigem o Internet Explorer, use [o Internet Explorer Driver][GithubSeleniumHqWikiIEDriver] com o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="795d4-238">To test sites that require Internet Explorer, use [Internet Explorer Driver][GithubSeleniumHqWikiIEDriver] with Internet Explorer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="795d4-239">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="795d4-239">Next steps</span></span>  

<span data-ttu-id="795d4-240">Para obter mais informações sobre o WebDriver e como gravar testes automatizados do WebDriver usando Selenium, navegue até a documentação [de Selenium][SeleniumDocumentation].</span><span class="sxs-lookup"><span data-stu-id="795d4-240">For more information about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="795d4-241">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="795d4-241">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="795d4-242">A Microsoft Edge equipe está ávida para ouvir seus comentários sobre como usar o WebDriver, Selenium e Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="795d4-242">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="795d4-243">Para enviar à equipe suas perguntas e comentários, escolha o ícone **Enviar Comentários** no Microsoft Edge DevTools ou envie um tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="795d4-243">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Feedback no Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="795d4-245">O **ícone Enviar Comentários** no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="795d4-245">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Recursos e edgeOptions | Microsoft Docs"  

<!--[Webdriver]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge - Políticas | Microsoft Docs"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub do Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  
[GithubSeleniumHqWikiIEDriver]: https://github.com/SeleniumHQ/selenium/wiki/InternetExplorerDriver "Driver do Internet Explorer - Selenium | GitHub"

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Microsoft Edge Driver | Microsoft Edge Desenvolvedor"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Baixar Novo Microsoft Edge Navegador"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | NuGet Galeria"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Galeria"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Galeria"  
[NugetPackagesSeleniumWebdriver400beta02]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-beta2 "Selenium.WebDriver 4.0.0-beta2 | NuGet Galeria"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "A versão de Automação do Navegador selenium Project | Documentação para Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selenium"  
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Instalar bibliotecas Selenium | Selenium"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem | Wikipédia"  
