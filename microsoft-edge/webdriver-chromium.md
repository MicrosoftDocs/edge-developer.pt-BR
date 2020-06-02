---
description: Saiba como testar seu site ou aplicativo no Microsoft Edge ou automatizar o navegador com o WebDriver.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento na Web, HTML, CSS, JavaScript, desenvolvedor, WebDriver, Selenium, testes, ferramentas, automação, teste
ms.openlocfilehash: 52d1a92df1a0faa21a1f8caa780fe203ad27856e
ms.sourcegitcommit: d39c64e0d439eb0643950248cdf2282383779225
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "10689672"
---
# <span data-ttu-id="40c87-104">WebDriver (Chromium)</span><span class="sxs-lookup"><span data-stu-id="40c87-104">WebDriver (Chromium)</span></span>  

<span data-ttu-id="40c87-105">A API do W3C [WebDriver][W3CWebdriver] é uma plataforma e uma interface neutra em linguagem e um protocolo de conexão, permitindo que programas ou scripts controlem o comportamento de um navegador da Web, como o Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="40c87-105">The W3C [WebDriver][W3CWebdriver] API is a platform and language-neutral interface and wire protocol allowing programs or scripts to control the behavior of a web browser, like Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="40c87-106">O WebDriver permite que os desenvolvedores criem testes automatizados que simulam a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="40c87-106">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="40c87-107">Testes e simulações do WebDriver diferem dos testes de unidade JavaScript porque o WebDriver tem acesso à funcionalidade e às informações que o JavaScript em execução no navegador não, e o WebDrive pode simular mais precisamente os eventos do usuário ou dos eventos no nível do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="40c87-107">WebDriver tests and simulations differ from JavaScript unit tests because WebDriver has access to functionality and information that JavaScript running in the browser does not, and WebDrive is able to more accurately simulate user events or OS-level events.</span></span>  <span data-ttu-id="40c87-108">O WebDriver é capaz de gerenciar testes em várias janelas, guias e páginas da Web em uma única sessão de teste.</span><span class="sxs-lookup"><span data-stu-id="40c87-108">WebDriver is able to manage testing across multiple windows, tabs and webpages in a single test session.</span></span>  

<span data-ttu-id="40c87-109">Veja como começar a usar o WebDriver para Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="40c87-109">Here is how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="40c87-110">Instalar o Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="40c87-110">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="40c87-111">Se você ainda não tiver feito isso, [Instale o Microsoft Edge (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="40c87-111">If you have not already, [install Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="40c87-112">Se você estiver usando uma versão pré-instalada do Microsoft Edge em seu computador, verifique se você tem o Microsoft Edge \ (Chromium \) e não o Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="40c87-112">If you are using a pre-installed version of Microsoft Edge on your machine, verify that you have Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="40c87-113">Uma maneira rápida de verificar é carregar `edge://settings/help` no navegador e confirmar se o número da versão é v75 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="40c87-113">A quick way to check is to load `edge://settings/help` in the browser and confirm that the version number is v75 or later.</span></span>  

## <span data-ttu-id="40c87-114">Baixar o driver Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40c87-114">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="40c87-115">O WebDriver requer um driver específico do navegador para automatizar cada navegador.</span><span class="sxs-lookup"><span data-stu-id="40c87-115">WebDriver requires a browser-specific driver to automate each browser.</span></span>  <span data-ttu-id="40c87-116">Para o Microsoft Edge \ (Chromium \), o WebDriver requer o [Driver da Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] apropriado para a compilação do Microsoft Edge que você deseja testar ou automatizar.</span><span class="sxs-lookup"><span data-stu-id="40c87-116">For Microsoft Edge \(Chromium\), WebDriver requires the appropriate [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] for the build of Microsoft Edge you want to test or automate.</span></span>  

<span data-ttu-id="40c87-117">Para encontrar o seu número de versão correto, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="40c87-117">To find your correct build number, use the following steps.</span></span>  

1.  <span data-ttu-id="40c87-118">Iniciar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40c87-118">Launch Microsoft Edge</span></span> 
1.  <span data-ttu-id="40c87-119">Exiba a versão \ (Chromium \) do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40c87-119">View the Microsoft Edge \(Chromium\) version.</span></span>  
    *   <span data-ttu-id="40c87-120">Navegue até</span><span class="sxs-lookup"><span data-stu-id="40c87-120">Navigate to</span></span> `edge://settings/help`  
    *   <span data-ttu-id="40c87-121">Selecionar `...`  >  **configurações**  >   **sobre o Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="40c87-121">Select `...` > **Settings** >  **About Microsoft Edge**</span></span>  
1.  <span data-ttu-id="40c87-122">Verifique se a versão correta do WebDriver para a sua compilação garante, para que ele seja executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="40c87-122">Verify the correct version of WebDriver for your build ensures, so it runs correctly.</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="O número do Build para o Microsoft Edge Canárias em 14 de janeiro de 2020":::
   <span data-ttu-id="40c87-124">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="40c87-124">Figure 1.</span></span>  <span data-ttu-id="40c87-125">O número do Build para o Microsoft Edge Canárias em 14 de janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="40c87-125">The build number for Microsoft Edge Canary on January 14, 2020</span></span>  
:::image-end:::  

<span data-ttu-id="40c87-126">Agora, [Baixe a versão correspondente do driver Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="40c87-126">Now, [download the matching version of Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="A seção downloads da página do driver Microsoft Edge":::
   <span data-ttu-id="40c87-128">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="40c87-128">Figure 2.</span></span>  <span data-ttu-id="40c87-129">A seção downloads da página do [driver Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads]</span><span class="sxs-lookup"><span data-stu-id="40c87-129">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="40c87-130">O Microsoft Edge \ (EdgeHTML \) não funciona com [o Microsoft Edge driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="40c87-130">Microsoft Edge \(EdgeHTML\) does not work with [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="40c87-131">Para automatizar o Microsoft Edge \ (EdgeHTML \), você deve baixar [o Microsoft WebDriver para Microsoft Edge \ (EdgeHTML \)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="40c87-131">To automate Microsoft Edge \(EdgeHTML\), you must download [Microsoft WebDriver for Microsoft Edge \(EdgeHTML\)][Webdriver].</span></span>  

## <span data-ttu-id="40c87-132">Escolher uma associação de linguagem do WebDriver</span><span class="sxs-lookup"><span data-stu-id="40c87-132">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="40c87-133">O último componente que você deve baixar é um driver de cliente específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="40c87-133">The last component you must download is a language-specific client driver.</span></span>  <span data-ttu-id="40c87-134">A associação de linguagem traduz o código que você escreve em Python, Java, C \ #, Ruby e JavaScript em comandos que o driver Microsoft Edge que você [baixou na seção anterior](#download-microsoft-edge-driver) pode executar no Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="40c87-134">The language binding translates the code you write in Python, Java, C\#, Ruby, and JavaScript into commands that the Microsoft Edge Driver you [downloaded in the previous section](#download-microsoft-edge-driver) is able to run in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="40c87-135">[Baixe a vinculação de linguagem do WebDriver de sua preferência][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="40c87-135">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="40c87-136">A equipe do Microsoft Edge é altamente recomendável [Selenium 4, 0-alpha05][NugetPackagesSeleniumWebdriver400alpha05] ou posterior, pois ele tem suporte interno para o Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="40c87-136">The Microsoft Edge team highly recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, since it has built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="40c87-137">No entanto, você pode orientar o Microsoft Edge \ (Chromium \) em todas as versões mais antigas do Selenium, incluindo a versão atual de 3 estável do Selenium.</span><span class="sxs-lookup"><span data-stu-id="40c87-137">However, you are able to drive Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="40c87-138">Se você já estava automatizando ou testando o Microsoft Edge \ (Chromium \) usando `ChromeDriver` e `ChromeOptions` , o código do seu WebDriver não é executado com êxito no Microsoft Edge V80 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="40c87-138">If you were previously automating or testing Microsoft Edge \(Chromium\) by using `ChromeDriver` and `ChromeOptions`, your WebDriver code does not run successfully against Microsoft Edge v80 or later.</span></span>  <span data-ttu-id="40c87-139">Esta é uma alteração significativa, e o Microsoft Edge \ (Chromium \) não aceita mais os comandos.</span><span class="sxs-lookup"><span data-stu-id="40c87-139">This is a breaking change and Microsoft Edge \(Chromium\) no longer accepts the commands.</span></span>  <span data-ttu-id="40c87-140">Você deve alterar seus testes para usar o `EdgeOptions` Driver de classe e [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="40c87-140">You must change your tests to use the `EdgeOptions` class and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="40c87-141">Usando o Selenium 3</span><span class="sxs-lookup"><span data-stu-id="40c87-141">Using Selenium 3</span></span>  

<span data-ttu-id="40c87-142">O [Selenium 3][|::ref1::|] é a versão mais recente do Selenium estável.</span><span class="sxs-lookup"><span data-stu-id="40c87-142">[Selenium 3][|::ref1::|] is the latest stable Selenium release.</span></span>  <span data-ttu-id="40c87-143">Por padrão, o Selenium 3 impulsiona o antigo Microsoft Edge \ (EdgeHTML \) e não tem suporte interno para o Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="40c87-143">By default, Selenium 3 drives the old Microsoft Edge \(EdgeHTML\), and does not have built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="40c87-144">Para usar o Selenium 3 com o Microsoft Edge \ (Chromium \), instale o pacote do [Selenium Tools para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .</span><span class="sxs-lookup"><span data-stu-id="40c87-144">To use Selenium 3 with Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package.</span></span>  <span data-ttu-id="40c87-145">As ferramentas Selenium para Microsoft Edge Extend Selenium 3 com um driver atualizado para ajudá-lo a escrever testes automatizados para os navegadores Microsoft Edge \ (EdgeHTML \) e New Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="40c87-145">The Selenium Tools for Microsoft Edge extend Selenium 3 with an updated driver to help you write automated tests for both the Microsoft Edge \(EdgeHTML\) and new Microsoft Edge \(Chromium\) browsers.</span></span>  

<span data-ttu-id="40c87-146">O Selenium Tools para Microsoft Edge é uma solução para os desenvolvedores que preferem permanecer no Selenium 3 e nos desenvolvedores que têm testes de navegador existentes e querem adicionar cobertura para o novo navegador Microsoft Edge \ (Chromium \) sem alterar as versões do Selenium.</span><span class="sxs-lookup"><span data-stu-id="40c87-146">Selenium Tools for Microsoft Edge is a solution for developers who prefer to remain on Selenium 3 and developers who have existing browser tests and want to add coverage for the new Microsoft Edge \(Chromium\) browser without changing Selenium versions.</span></span>  <span data-ttu-id="40c87-147">As `EdgeDriver` classes e as `EdgeDriverService` contidas nas ferramentas são totalmente compatíveis com os equivalentes internos no Selenium e executam o Microsoft Edge \ (EdgeHTML \) por padrão para que as ferramentas possam ser usadas como uma substituição automática para as classes de borda existentes no Selenium.</span><span class="sxs-lookup"><span data-stu-id="40c87-147">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium, and run Microsoft Edge \(EdgeHTML\) by default so the tools may be used as a seamless drop-in replacement for the existing Edge classes in Selenium.</span></span>  

<span data-ttu-id="40c87-148">[Instale o Selenium Tools para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para começar a usar o Microsoft Edge \ (Chromium \) com seu projeto do Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="40c87-148">[Install Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] to begin using Microsoft Edge \(Chromium\) with your Selenium 3 project.</span></span>  

## <span data-ttu-id="40c87-149">Usar o Microsoft Edge (Chromium) com o WebDriver</span><span class="sxs-lookup"><span data-stu-id="40c87-149">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="40c87-150">Os exemplos a seguir são executáveis usando o Selenium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="40c87-150">The following examples are runnable using either Selenium 3 or 4.</span></span>  <span data-ttu-id="40c87-151">Para usar com o Selenium 3, as [Ferramentas do Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] devem estar instaladas.</span><span class="sxs-lookup"><span data-stu-id="40c87-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] must be installed.</span></span>  

### <span data-ttu-id="40c87-152">Uso básico</span><span class="sxs-lookup"><span data-stu-id="40c87-152">Basic Usage</span></span>  

<span data-ttu-id="40c87-153">Para usar com o Microsoft Edge \ (EdgeHTML \), basta criar uma instância padrão da `EdgeDriver` classe.</span><span class="sxs-lookup"><span data-stu-id="40c87-153">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="40c87-154">C#</span><span class="sxs-lookup"><span data-stu-id="40c87-154">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="40c87-155">Python</span><span class="sxs-lookup"><span data-stu-id="40c87-155">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="40c87-156">JavaScript</span><span class="sxs-lookup"><span data-stu-id="40c87-156">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="40c87-157">Dirigir o Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="40c87-157">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="40c87-158">Para usar com o Microsoft Edge \ (Chromium \) em vez disso, crie uma nova `EdgeDriver` classe e passe a ela o `EdgeOptions` objeto com a `UseChromium` propriedade definida como `true` .</span><span class="sxs-lookup"><span data-stu-id="40c87-158">To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="40c87-159">C#</span><span class="sxs-lookup"><span data-stu-id="40c87-159">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="40c87-160">Python</span><span class="sxs-lookup"><span data-stu-id="40c87-160">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="40c87-161">JavaScript</span><span class="sxs-lookup"><span data-stu-id="40c87-161">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="40c87-162">Escolher binários específicos do navegador (somente Chromium)</span><span class="sxs-lookup"><span data-stu-id="40c87-162">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="40c87-163">Use a `EdgeOptions` classe para escolher um binário específico.</span><span class="sxs-lookup"><span data-stu-id="40c87-163">Use the `EdgeOptions` class to choose a specific binary.</span></span>  <span data-ttu-id="40c87-164">Isso é útil para testar os [canais da visualização do Microsoft Edge][MicrosoftedgeinsiderDownload] , como o Microsoft Edge beta.</span><span class="sxs-lookup"><span data-stu-id="40c87-164">It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="40c87-165">C#</span><span class="sxs-lookup"><span data-stu-id="40c87-165">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="40c87-166">Python</span><span class="sxs-lookup"><span data-stu-id="40c87-166">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="40c87-167">JavaScript</span><span class="sxs-lookup"><span data-stu-id="40c87-167">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="40c87-168">Personalizando o serviço de driver do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40c87-168">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="40c87-169">C#</span><span class="sxs-lookup"><span data-stu-id="40c87-169">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="40c87-170">Quando uma `EdgeDriver` instância de classe é criada usando `EdgeOptions` classe, ela cria e abre automaticamente a `EdgeDriverService` classe apropriada para o Microsoft Edge \ (EdgeHTML \) ou o Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="40c87-170">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="40c87-171">Se você quiser criar um `EdgeDriverService` , crie um configurado para o Microsoft Edge \ (Chromium \) usando o `CreateChromiumService()` método.</span><span class="sxs-lookup"><span data-stu-id="40c87-171">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="40c87-172">Pode ser útil para personalizações adicionais, como habilitar a saída de log detalhada no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="40c87-172">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> <span data-ttu-id="40c87-173">Você não precisa fornecer o `EdgeOptions` objeto ao passar a `EdgeDriver` instância da classe a `EdgeDriverService` .</span><span class="sxs-lookup"><span data-stu-id="40c87-173">You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.</span></span>  <span data-ttu-id="40c87-174">A `EdgeDriver` classe usa as opções padrão para o Microsoft Edge \ (EdgeHTML \) ou o Microsoft Edge \ (Chromium \), dependendo do tipo de serviço que você fornecer.</span><span class="sxs-lookup"><span data-stu-id="40c87-174">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.</span></span>  
> 
> <span data-ttu-id="40c87-175">No entanto, se você quiser fornecer uma `EdgeDriverService` classe and e `EdgeOptions` , você deve garantir que ambos estejam configurados para a mesma versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40c87-175">However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="40c87-176">Por exemplo, não é possível usar uma classe padrão do Microsoft Edge \ (EdgeHTML \) `EdgeDriverService` e as propriedades Chromium na `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="40c87-176">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="40c87-177">A `EdgeDriver` classe gera um erro para impedir o uso de versões diferentes.</span><span class="sxs-lookup"><span data-stu-id="40c87-177">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="40c87-178">Python</span><span class="sxs-lookup"><span data-stu-id="40c87-178">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="40c87-179">Ao usar Python, o `Edge` objeto cria e gerencia o `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="40c87-179">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="40c87-180">Para configurar o `EdgeService` , passe argumentos adicionais para o `Edge` objeto:</span><span class="sxs-lookup"><span data-stu-id="40c87-180">To configure the `EdgeService`, pass additional arguments to the `Edge` object:</span></span>

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="40c87-181">JavaScript</span><span class="sxs-lookup"><span data-stu-id="40c87-181">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="40c87-182">Ao usar JavaScript, crie e configure um `Service` com a `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="40c87-182">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="40c87-183">Você pode, opcionalmente, passar o `Service` objeto para o `Driver` objeto que inicia e para o serviço para você.</span><span class="sxs-lookup"><span data-stu-id="40c87-183">You may optionally pass the `Service` object to the `Driver` object which starts and stops the service for you.</span></span>  

<span data-ttu-id="40c87-184">Para configurar o `Service` , execute métodos adicionais na `ServiceBuilder` classe antes de usar o `build()` método e, em seguida, passe o `service` como um parâmetro no `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="40c87-184">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method and  then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="40c87-185">Usando opções específicas do Chromium</span><span class="sxs-lookup"><span data-stu-id="40c87-185">Using Chromium-Specific Options</span></span>  

<span data-ttu-id="40c87-186">Usar a `EdgeOptions` classe com a `UseChromium` propriedade definida como `true` fornece acesso a todos os mesmos métodos e propriedades que estão disponíveis na classe [chromeoptions][SeleniumWebDriverChromeoptionsClass] em Selenium.</span><span class="sxs-lookup"><span data-stu-id="40c87-186">Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.</span></span>  <span data-ttu-id="40c87-187">Por exemplo, assim como outros navegadores do Chromium, use o `EdgeOptions.AddArguments()` método para executar o Microsoft Edge \ (Chromium \) no [modo sem periféricos][WikiHeadlessBrowser] no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="40c87-187">For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.</span></span>  

#### [<span data-ttu-id="40c87-188">C#</span><span class="sxs-lookup"><span data-stu-id="40c87-188">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="40c87-189">Python</span><span class="sxs-lookup"><span data-stu-id="40c87-189">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="40c87-190">JavaScript</span><span class="sxs-lookup"><span data-stu-id="40c87-190">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```
* * *  

> [!NOTE]
> <span data-ttu-id="40c87-191">As [Propriedades e métodos específicos do Chromium][SeleniumWebDriverChromeoptionsClass] estão sempre disponíveis, mas não têm efeito se a `UseChromium` propriedade não estiver definida como `true` .</span><span class="sxs-lookup"><span data-stu-id="40c87-191">The [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.</span></span>  <span data-ttu-id="40c87-192">Da mesma forma, propriedades e métodos existentes para Microsoft Edge \ (EdgeHTML \) não têm efeito se `UseChromium` a propriedade for definida como `true` .</span><span class="sxs-lookup"><span data-stu-id="40c87-192">Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.</span></span>  

## <span data-ttu-id="40c87-193">Outras maneiras de configurar o WebDriver</span><span class="sxs-lookup"><span data-stu-id="40c87-193">Other ways to set up WebDriver</span></span>  

### <span data-ttu-id="40c87-194">Chocolate</span><span class="sxs-lookup"><span data-stu-id="40c87-194">Chocolatey</span></span>  

<span data-ttu-id="40c87-195">Se você estiver usando uma [chocolate][Chocolatey] como gerente de pacote, instale o driver Microsoft Edge executando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="40c87-195">If you are using [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="40c87-196">Para obter mais informações, consulte [Selenium Chromium Edge driver em leite][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="40c87-196">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="40c87-197">Docker</span><span class="sxs-lookup"><span data-stu-id="40c87-197">Docker</span></span>  

<span data-ttu-id="40c87-198">Se você estiver usando o [Docker][DockerHub], Baixe uma imagem pré-configurada com o Microsoft Edge \ (Chromium \) e [o Microsoft Edge driver][MicrosoftDeveloperEdgeToolsWebdriver] já instalado executando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="40c87-198">If you are using [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] already installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="40c87-199">Para obter mais informações, consulte [contêiner no Dock Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="40c87-199">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="40c87-200">Entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="40c87-200">Getting in touch with the Microsoft Edge DevTools team</span></span>    

<span data-ttu-id="40c87-201">A equipe do Microsoft Edge está ansiosos para ouvir seus comentários sobre como usar o WebDriver, o Selenium e o Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="40c87-201">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge!</span></span>  <span data-ttu-id="40c87-202">Use o ícone de **comentários** no Microsoft Edge devtools ou tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] para que a equipe saiba qual é a sua opinião.</span><span class="sxs-lookup"><span data-stu-id="40c87-202">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="O ícone de comentários no Microsoft Edge DevTools":::
   <span data-ttu-id="40c87-204">O ícone de **comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="40c87-204">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[Webdriver]: ./webdriver.md "WebDriver (EdgeHTML) | Documentos da Microsoft"  

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
