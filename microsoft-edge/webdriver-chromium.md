---
description: Saiba como testar seu site ou aplicativo no Microsoft Edge ou automatizar o navegador com o WebDriver.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento na Web, HTML, CSS, JavaScript, desenvolvedor, WebDriver, Selenium, testes, ferramentas, automação, teste
ms.openlocfilehash: 14537943351db144bb4839d6befbfaa62894cd85
ms.sourcegitcommit: 3f8c8a5643e416b0851254833f9771192883ec45
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699504"
---
# <span data-ttu-id="cd39d-104">Usar o WebDriver (Chromium) para automação de teste</span><span class="sxs-lookup"><span data-stu-id="cd39d-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="cd39d-105">O WebDriver permite que os desenvolvedores criem testes automatizados que simulam a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cd39d-105">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="cd39d-106">Testes e simulações do WebDriver diferem dos testes de unidade JavaScript devido aos seguintes motivos.</span><span class="sxs-lookup"><span data-stu-id="cd39d-106">WebDriver tests and simulations differ from JavaScript unit tests because of the following reasons.</span></span> 
*   <span data-ttu-id="cd39d-107">Acessa funcionalidade e informações que não estão disponíveis para JavaScript em execução nos navegadores.</span><span class="sxs-lookup"><span data-stu-id="cd39d-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="cd39d-108">Simula eventos do usuário ou de nível do sistema operacional com mais precisão.</span><span class="sxs-lookup"><span data-stu-id="cd39d-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="cd39d-109">Gerencia testes em várias janelas, guias e páginas da Web em uma única sessão de teste.</span><span class="sxs-lookup"><span data-stu-id="cd39d-109">Manages testing across multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="cd39d-110">Executa várias sessões do Microsoft Edge em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="cd39d-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  

<span data-ttu-id="cd39d-111">A seção a seguir descreve como começar a usar o WebDriver para Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="cd39d-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="cd39d-112">Instalar o Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="cd39d-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="cd39d-113">Certifique-se [de instalar o Microsoft Edge (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="cd39d-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="cd39d-114">Para confirmar se você tem o Microsoft Edge (Chromium) instalado, vá para `edge://settings/help` no navegador e verifique se a versão do número de versão 75 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cd39d-114">To confirm that you have Microsoft Edge (Chromium) installed, go to `edge://settings/help` in the browser, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="cd39d-115">Baixar o driver Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cd39d-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="cd39d-116">Para começar a automatizar testes, use as etapas a seguir para garantir que a versão do WebDriver que você instalar corresponda à versão do seu navegador.</span><span class="sxs-lookup"><span data-stu-id="cd39d-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="cd39d-117">Vá para `edge://settings/help` para obter a versão do Edge.</span><span class="sxs-lookup"><span data-stu-id="cd39d-117">Go to `edge://settings/help` to get the version of Edge.</span></span>  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="O número do Build para o Microsoft Edge Canárias em 14 de janeiro de 2020":::
       <span data-ttu-id="cd39d-119">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="cd39d-119">Figure 1.</span></span>  <span data-ttu-id="cd39d-120">O número do Build para o Microsoft Edge Canárias em 14 de janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="cd39d-120">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="cd39d-121">Navegue até a página de [downloads do driver Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] e baixe o driver que corresponde ao número de versão da borda.</span><span class="sxs-lookup"><span data-stu-id="cd39d-121">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the Edge version number.</span></span>  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="A seção downloads da página do driver Microsoft Edge":::
       <span data-ttu-id="cd39d-123">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="cd39d-123">Figure 2.</span></span>  <span data-ttu-id="cd39d-124">A seção downloads da página do [driver Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="cd39d-124">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    > [!NOTE] 
    > <span data-ttu-id="cd39d-125">Para obter mais informações sobre a automação de teste usando o Microsoft Edge (EdgeHTML), consulte [Microsoft WebDriver para Microsoft Edge (EdgeHTML)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="cd39d-125">For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].</span></span>  

## <span data-ttu-id="cd39d-126">Escolher uma associação de linguagem do WebDriver</span><span class="sxs-lookup"><span data-stu-id="cd39d-126">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="cd39d-127">O último componente que você deve baixar é um driver de cliente específico do idioma para traduzir seu código \ (Python, Java, C \ #, Ruby, JavaScript \) em comandos que o driver Microsoft Edge funciona no Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="cd39d-127">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="cd39d-128">[Baixe a vinculação de linguagem do WebDriver de sua preferência][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="cd39d-128">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="cd39d-129">A equipe do Microsoft Edge recomenda o [Selenium 4, 0-alpha05][NugetPackagesSeleniumWebdriver400alpha05] ou posterior, pois oferece suporte ao Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="cd39d-129">The Microsoft Edge team recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cd39d-130">No entanto, você pode controlar o Microsoft Edge \ (Chromium \) em todas as versões mais antigas do Selenium, incluindo a versão atual de 3 estável do Selenium.</span><span class="sxs-lookup"><span data-stu-id="cd39d-130">However, you are able to control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="cd39d-131">Se você já estava automatizando ou testando o Microsoft Edge \ (Chromium \) usando `ChromeDriver` e `ChromeOptions` classes, o código do seu WebDriver não é executado no Microsoft edge versão 80 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cd39d-131">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="cd39d-132">Para solucionar esse problema, atualize seus testes para usar a `EdgeOptions` classe e instalar o [Driver do Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="cd39d-132">To solve this problem, update your tests to use the `EdgeOptions` class and install [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="cd39d-133">Usar o Selenium 3</span><span class="sxs-lookup"><span data-stu-id="cd39d-133">Use Selenium 3</span></span>  

<span data-ttu-id="cd39d-134">Se você já usa o [Selenium 3][|::ref1::|], pode ter testes de navegador existentes e deseja adicionar cobertura ao Microsoft Edge \ (Chromium \) sem alterar sua versão do Selenium.</span><span class="sxs-lookup"><span data-stu-id="cd39d-134">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="cd39d-135">Para usar o [Selenium 3][|::ref2::|] para escrever testes automatizados para o Microsoft Edge \ (EdgeHTML \) e o Microsoft Edge \ (Chromium \), instale o pacote de [Ferramentas do Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar o driver atualizado.</span><span class="sxs-lookup"><span data-stu-id="cd39d-135">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="cd39d-136">As `EdgeDriver` classes e as `EdgeDriverService` contidas nas ferramentas são totalmente compatíveis com os equivalentes internos no Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="cd39d-136">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

## <span data-ttu-id="cd39d-137">Usar o Microsoft Edge (Chromium) com o WebDriver</span><span class="sxs-lookup"><span data-stu-id="cd39d-137">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="cd39d-138">Você pode executar os exemplos a seguir usando o Selenium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="cd39d-138">You may run the following examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="cd39d-139">Para usar com o Selenium 3, o pacote de [Ferramentas do Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="cd39d-139">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="cd39d-140">Uso básico</span><span class="sxs-lookup"><span data-stu-id="cd39d-140">Basic Usage</span></span>  

<span data-ttu-id="cd39d-141">Para usar com o Microsoft Edge \ (EdgeHTML \), basta criar uma instância padrão da `EdgeDriver` classe.</span><span class="sxs-lookup"><span data-stu-id="cd39d-141">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="cd39d-142">C#</span><span class="sxs-lookup"><span data-stu-id="cd39d-142">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="cd39d-143">Python</span><span class="sxs-lookup"><span data-stu-id="cd39d-143">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="cd39d-144">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cd39d-144">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="cd39d-145">Dirigir o Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="cd39d-145">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="cd39d-146">Para usar com o Microsoft Edge \ (Chromium \), crie uma nova `EdgeDriver` classe e passe o `EdgeOptions` objeto com a `UseChromium` propriedade definida como `true` .</span><span class="sxs-lookup"><span data-stu-id="cd39d-146">To use with Microsoft Edge \(Chromium\), create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="cd39d-147">C#</span><span class="sxs-lookup"><span data-stu-id="cd39d-147">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="cd39d-148">Python</span><span class="sxs-lookup"><span data-stu-id="cd39d-148">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="cd39d-149">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cd39d-149">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="cd39d-150">Se a política [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] estiver definida como `2` , o [driver Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] não poderá orientar o [Microsoft Edge (Chromium)][MicrosoftEdge] porque o driver usa o [Microsoft Edge devtools][DevToolsMain].</span><span class="sxs-lookup"><span data-stu-id="cd39d-150">If the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy is set to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive [Microsoft Edge (Chromium)][MicrosoftEdge] because the driver uses the [Microsoft Edge DevTools][DevToolsMain].</span></span>  <span data-ttu-id="cd39d-151">Verifique se você definiu a política [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] como `0` ou `1` para automatizar o [Microsoft Edge (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="cd39d-151">Ensure you set the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy to `0` or `1` to automate [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  

### <span data-ttu-id="cd39d-152">Escolher binários específicos do navegador (somente Chromium)</span><span class="sxs-lookup"><span data-stu-id="cd39d-152">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="cd39d-153">Você pode usar a `EdgeOptions` classe com binários específicos do Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="cd39d-153">You may use the `EdgeOptions` class with specific binaries of Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="cd39d-154">Por exemplo, você pode executar testes usando os [canais da visualização do Microsoft Edge][MicrosoftedgeinsiderDownload] , como o Microsoft Edge beta.</span><span class="sxs-lookup"><span data-stu-id="cd39d-154">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="cd39d-155">C#</span><span class="sxs-lookup"><span data-stu-id="cd39d-155">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="cd39d-156">Python</span><span class="sxs-lookup"><span data-stu-id="cd39d-156">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="cd39d-157">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cd39d-157">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="cd39d-158">Personalizando o serviço de driver do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cd39d-158">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="cd39d-159">C#</span><span class="sxs-lookup"><span data-stu-id="cd39d-159">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cd39d-160">Quando uma `EdgeDriver` instância de classe é criada usando `EdgeOptions` classe, ela cria e inicia a `EdgeDriverService` classe apropriada para o Microsoft Edge \ (EdgeHTML \) ou o Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="cd39d-160">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="cd39d-161">Se você quiser criar um `EdgeDriverService` , crie um configurado para o Microsoft Edge \ (Chromium \) usando o `CreateChromiumService()` método.</span><span class="sxs-lookup"><span data-stu-id="cd39d-161">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="cd39d-162">Pode ser útil para personalizações adicionais, como habilitar a saída de log detalhada no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd39d-162">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="cd39d-163">Você não precisa fornecer o `EdgeOptions` objeto ao passar `EdgeDriverService` para a `EdgeDriver` instância.</span><span class="sxs-lookup"><span data-stu-id="cd39d-163">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span> <span data-ttu-id="cd39d-164">A `EdgeDriver` classe usa as opções padrão para o Microsoft Edge \ (EdgeHTML \) ou o Microsoft Edge \ (Chromium \), dependendo do serviço que você fornecer.</span><span class="sxs-lookup"><span data-stu-id="cd39d-164">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on the service you provide.</span></span>  
> <span data-ttu-id="cd39d-165">No entanto, se você quiser fornecer ambas as `EdgeDriverService` classes e as `EdgeOptions` classes, certifique-se de que ambas estejam configuradas para a mesma versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cd39d-165">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="cd39d-166">Por exemplo, não é possível usar uma classe padrão do Microsoft Edge (EdgeHTML) `EdgeDriverService` e as propriedades Chromium na `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="cd39d-166">For example, it is not possible to use a default Microsoft Edge (EdgeHTML) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="cd39d-167">A `EdgeDriver` classe gera um erro para impedir o uso de versões diferentes.</span><span class="sxs-lookup"><span data-stu-id="cd39d-167">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="cd39d-168">Python</span><span class="sxs-lookup"><span data-stu-id="cd39d-168">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cd39d-169">Ao usar Python, o `Edge` objeto cria e gerencia o `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="cd39d-169">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="cd39d-170">Para configurar o `EdgeService` , passe argumentos adicionais para o `Edge` objeto conforme indicado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd39d-170">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="cd39d-171">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cd39d-171">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cd39d-172">Ao usar JavaScript, crie e configure um `Service` com a `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="cd39d-172">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="cd39d-173">Você pode, opcionalmente, passar o `Service` objeto para o `Driver` objeto que inicia e para o serviço para você.</span><span class="sxs-lookup"><span data-stu-id="cd39d-173">You may optionally pass the `Service` object to the `Driver` object which starts and stops the service for you.</span></span>  
<span data-ttu-id="cd39d-174">Para configurar o `Service` , execute métodos adicionais na `ServiceBuilder` classe antes de usar o `build()` método.</span><span class="sxs-lookup"><span data-stu-id="cd39d-174">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="cd39d-175">Em seguida, passe o `service` como um parâmetro no `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="cd39d-175">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * * 

### <span data-ttu-id="cd39d-176">Usar opções específicas do Chromium</span><span class="sxs-lookup"><span data-stu-id="cd39d-176">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="cd39d-177">Se você definir a `UseChromium` propriedade como `true` , poderá usar a `EdgeOptions` classe para acessar as mesmas [Propriedades e métodos específicos do Chromium][SeleniumWebDriverChromeoptionsClass] como quando você automatiza outros navegadores do Chromium.</span><span class="sxs-lookup"><span data-stu-id="cd39d-177">If you set the `UseChromium` property to `true`, you are able to use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] as when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="cd39d-178">C#</span><span class="sxs-lookup"><span data-stu-id="cd39d-178">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="cd39d-179">Python</span><span class="sxs-lookup"><span data-stu-id="cd39d-179">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="cd39d-180">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cd39d-180">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  
> [!NOTE]
> <span data-ttu-id="cd39d-181">Se a `UseChromium` propriedade estiver definida como `true` , você não poderá usar propriedades e métodos para o Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="cd39d-181">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="cd39d-182">Opções de instalação adicionais do WebDriver</span><span class="sxs-lookup"><span data-stu-id="cd39d-182">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="cd39d-183">Chocolate</span><span class="sxs-lookup"><span data-stu-id="cd39d-183">Chocolatey</span></span>  

<span data-ttu-id="cd39d-184">Se você usar uma [chocolate][Chocolatey] como gerente de pacote, instale o driver Microsoft Edge executando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="cd39d-184">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="cd39d-185">Para obter mais informações, consulte [Selenium Chromium Edge driver em leite][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="cd39d-185">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="cd39d-186">Docker</span><span class="sxs-lookup"><span data-stu-id="cd39d-186">Docker</span></span>  

<span data-ttu-id="cd39d-187">Se você usar o [Docker][DockerHub], Baixe uma imagem pré-configurada com o Microsoft Edge \ (Chromium \) e [o Microsoft Edge driver][MicrosoftDeveloperEdgeToolsWebdriver] pré-instalado executando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="cd39d-187">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="cd39d-188">Para obter mais informações, consulte [contêiner no Dock Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="cd39d-188">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="cd39d-189">Entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cd39d-189">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="cd39d-190">A equipe do Microsoft Edge está ansiosos para ouvir seus comentários sobre como usar o WebDriver, o Selenium e o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cd39d-190">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="cd39d-191">Use o ícone de **comentários** no Microsoft Edge devtools ou tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] para que a equipe saiba qual é a sua opinião.</span><span class="sxs-lookup"><span data-stu-id="cd39d-191">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="O ícone de comentários no Microsoft Edge DevTools":::
   <span data-ttu-id="cd39d-193">O ícone de **comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="cd39d-193">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[DevToolsMain]: ./devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"
[Webdriver]: ./webdriver.md "WebDriver (EdgeHTML) | Documentos da Microsoft"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability-Microsoft Edge-Policies | Documentos da Microsoft"  

[Chocolatey]: https://chocolatey.org "Chocolate | Software de chocolate"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selenium Chromium Edge driver | Chocolate"  

[DockerHub]: https://hub.docker.com "Hub do Docker"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub do Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-ferramentas | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selenium | GitHub"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Desenvolvedor da Microsoft"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Downloads-WebDriver | Desenvolvedor da Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Baixar novo navegador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  

[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Galeria do NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium. WebDriver 3.141.0 | Galeria do NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium. WebDriver 4.0.0-alpha05 | Galeria do NuGet"  

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Chromeoptions Class-WebDriver | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um tweet"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem periféricos | Wikipédia"  
