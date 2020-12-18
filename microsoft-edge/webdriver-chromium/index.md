---
description: Saiba como testar seu site ou aplicativo no Microsoft Edge ou automatizar o navegador com o WebDriver.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento na Web, HTML, CSS, JavaScript, desenvolvedor, WebDriver, Selenium, testes, ferramentas, automação, teste
ms.openlocfilehash: 5e881eec59c966fd4fa6d35118032a3a51e7b9e5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231122"
---
# Usar o WebDriver (Chromium) para visão geral da automação de teste  

O WebDriver permite que você \ (desenvolvedores \) crie testes automatizados que simulam a interação do usuário.  Testes e simulações do WebDriver diferem dos testes de unidade JavaScript devido aos seguintes motivos.  

*   Acessa funcionalidade e informações que não estão disponíveis para JavaScript em execução nos navegadores.  
*   Simula eventos do usuário ou de nível do sistema operacional com mais precisão.  
*   Gerencia várias janelas, guias e páginas da Web em uma única sessão de teste.  
*   Executa várias sessões do Microsoft Edge em um computador específico.  
    
A seção a seguir descreve como começar a usar o WebDriver para Microsoft Edge \ (Chromium \).  

## Instalar o Microsoft Edge (Chromium)  

Certifique-se [de instalar o Microsoft Edge (Chromium)][MicrosoftEdge].  Para confirmar que você tem o Microsoft Edge \ (Chromium \) instalado, navegue até `edge://settings/help` e verifique se o número da versão é versão 75 ou posterior.  

## Baixar o driver Microsoft Edge  

Para começar a automatizar testes, use as etapas a seguir para garantir que a versão do WebDriver que você instalar corresponda à versão do seu navegador.  

1.  Navegue até `edge://settings/help` para obter a versão do Microsoft Edge.  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="O número do Build para o Microsoft Edge Canárias em 14 de janeiro de 2020":::
       O número do Build para o Microsoft Edge Canárias em 14 de janeiro de 2020
    :::image-end:::  
    
1.  Navegue até a página de [downloads do driver Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] e baixe o driver que corresponde ao número de versão do Microsoft Edge.  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="A seção downloads da página do driver Microsoft Edge":::
       A seção downloads da página do [driver Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## Escolher uma associação de linguagem do WebDriver  

O último componente que você deve baixar é um driver de cliente específico do idioma para traduzir seu código \ (Python, Java, C \ #, Ruby, JavaScript \) em comandos que o driver Microsoft Edge funciona no Microsoft Edge \ (Chromium \).  

[Baixe a vinculação de linguagem do WebDriver de sua preferência][SeleniumDownloads].  A equipe do Microsoft Edge recomenda o [Selenium 4, 0-alpha05][NugetPackagesSeleniumWebdriver400alpha05] ou posterior, pois oferece suporte ao Microsoft Edge \ (Chromium \).  No entanto, você pode controlar o Microsoft Edge \ (Chromium \) em todas as versões mais antigas do Selenium, incluindo a versão atual de 3 estável do Selenium.  

> [!IMPORTANT]
> Se você já estava automatizando ou testando o Microsoft Edge \ (Chromium \) usando `ChromeDriver` e `ChromeOptions` classes, o código do seu WebDriver não é executado no Microsoft edge versão 80 ou posterior.  Para solucionar esse problema, atualize seus testes para usar a `EdgeOptions` classe e instalar o [Driver do Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].  

### Usar o Selenium 3  

Se você já usa o [Selenium 3][|::ref1::|], pode ter testes de navegador existentes e deseja adicionar cobertura ao Microsoft Edge \ (Chromium \) sem alterar sua versão do Selenium.  Para usar o [Selenium 3][|::ref2::|] para escrever testes automatizados para o Microsoft Edge \ (EdgeHTML \) e o Microsoft Edge \ (Chromium \), instale o pacote de [Ferramentas do Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar o driver atualizado.  As `EdgeDriver` classes e as `EdgeDriverService` contidas nas ferramentas são totalmente compatíveis com os equivalentes internos no Selenium 4.  

Use as etapas a seguir para adicionar as [ferramentas Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] e [Selenium 3][|::ref3::|] ao seu projeto.

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Adicione os pacotes [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] e [Selenium. WebDriver][NugetPackagesSeleniumWebdriver31410] ao seu projeto .NET usando a [CLI do NuGet][NugetCLI] ou o [Visual Studio][VisualStudio].  

#### [Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Use [Pip][PythonPip] para instalar os pacotes [msedge-Selenium-Tools][PythonSeleniumTools] e [Selenium][PythonSelenium] .  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Use o [NPM][JavaScript|::ref4::|] para instalar os pacotes [Edge-Selenium-Tools][JavaScriptSeleniumTools] e [Selenium-WebDriver][JavaScriptSelenium] .  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Usar o Microsoft Edge (Chromium) com o WebDriver

Você pode executar os exemplos a seguir usando o Selenium 3 ou 4.  Para usar com o Selenium 3, o pacote de [Ferramentas do Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] deve ser instalado.  

### Uso básico  

Para usar com o Microsoft Edge \ (EdgeHTML \), crie uma instância padrão da `EdgeDriver` classe.  

#### [C#](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [Python](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [JavaScript](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### Dirigir o Microsoft Edge (Chromium)  

Para usar com o Microsoft Edge \ (Chromium \), crie uma nova `EdgeDriver` classe e passe o `EdgeOptions` objeto com a `UseChromium` propriedade definida como `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Se o administrador de TI tiver definido a política [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] como `2` , o [driver Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] não poderá orientar o [Microsoft Edge (Chromium)][MicrosoftEdge] porque o driver usa o [Microsoft Edge devtools][DevToolsMain].  Verifique se a política [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] está definida como `0` ou `1` para automatizar o [Microsoft Edge (Chromium)][MicrosoftEdge].  

### Escolher binários específicos do navegador (somente Chromium)  

Você pode usar a `EdgeOptions` classe com binários específicos do Microsoft Edge \ (Chromium \).  Por exemplo, você pode executar testes usando os [canais da visualização do Microsoft Edge][MicrosoftedgeinsiderDownload] , como o Microsoft Edge beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Personalizando o serviço de driver do Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Quando uma `EdgeDriver` instância de classe é criada usando `EdgeOptions` classe, ela cria e inicia a `EdgeDriverService` classe apropriada para o Microsoft Edge \ (EdgeHTML \) ou o Microsoft Edge \ (Chromium \).  

Se você quiser criar um `EdgeDriverService` , crie um configurado para o Microsoft Edge \ (Chromium \) usando o `CreateChromiumService()` método.  Pode ser útil para personalizações adicionais, como habilitar a saída de log detalhada no código a seguir.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Você não precisa fornecer o `EdgeOptions` objeto ao passar `EdgeDriverService` para a `EdgeDriver` instância. A `EdgeDriver` classe usa as opções padrão para o Microsoft Edge \ (EdgeHTML \) ou o Microsoft Edge \ (Chromium \), dependendo do serviço que você fornecer.  
> No entanto, se você quiser fornecer ambas as `EdgeDriverService` classes e as `EdgeOptions` classes, certifique-se de que ambas estejam configuradas para a mesma versão do Microsoft Edge.  Por exemplo, não é possível usar uma classe padrão do Microsoft Edge \ (EdgeHTML \) `EdgeDriverService` e as propriedades Chromium na `EdgeOptions` classe.  A `EdgeDriver` classe gera um erro para impedir o uso de versões diferentes.  

#### [Python](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Ao usar Python, o `Edge` objeto cria e gerencia o `EdgeService` .  Para configurar o `EdgeService` , passe argumentos adicionais para o `Edge` objeto conforme indicado no código a seguir.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Ao usar JavaScript, crie e configure um `Service` com a `ServiceBuilder` classe.  Opcionalmente, você pode passar o `Service` objeto para o `Driver` objeto, que inicia \ (e interrompe \) o serviço para você.  
Para configurar o `Service` , execute métodos adicionais na `ServiceBuilder` classe antes de usar o `build()` método.  Em seguida, passe o `service` como um parâmetro no `Driver.createSession()` método.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Usar opções de Chromium-Specific  

Se você definir a `UseChromium` propriedade como `true` , poderá usar a `EdgeOptions` classe para acessar as mesmas [Propriedades e métodos específicos do Chromium][SeleniumWebDriverChromeoptionsClass] como quando você automatiza outros navegadores do Chromium.  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Python](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [JavaScript](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  

> [!NOTE]
> Se a `UseChromium` propriedade estiver definida como `true` , você não poderá usar propriedades e métodos para o Microsoft Edge \ (EdgeHTML \).  

## Opções de instalação adicionais do WebDriver  

### Chocolate  

Se você usar uma [chocolate][Chocolatey] como gerente de pacote, instale o driver Microsoft Edge executando o seguinte comando.  

```console
choco install selenium-chromium-edge-driver
```  

Para obter mais informações, consulte [Selenium Chromium Edge driver em leite][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Se você usar o [Docker][DockerHub], Baixe uma imagem pré-configurada com o Microsoft Edge \ (Chromium \) e [o Microsoft Edge driver][MicrosoftDeveloperEdgeToolsWebdriver] pré-instalado executando o seguinte comando.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Para obter mais informações, consulte [contêiner no Dock Hub][DockerHubMsedgedriver].  

## Entrar em contato com a equipe Microsoft Edge DevTools  

A equipe do Microsoft Edge está ansiosos para ouvir seus comentários sobre como usar o WebDriver, o Selenium e o Microsoft Edge.  Para permitir que a equipe saiba o que você acha, escolha o ícone **enviar comentários** no Microsoft Edge devtools ou envie um tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone enviar comentários no Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   O ícone **enviar comentários** no Microsoft Edge devtools  
:::image-end:::  

<!-- links -->  

[DevToolsMain]: ../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"
[Webdriver]: ../webdriver/index.md "WebDriver (EdgeHTML) | Documentos da Microsoft"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability-Microsoft Edge-Policies | Documentos da Microsoft"  

[Chocolatey]: https://chocolatey.org "Chocolate | Software de chocolate"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selenium Chromium Edge driver | Chocolate"  

[DockerHub]: https://hub.docker.com "Hub do Docker"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub do Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-ferramentas | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "NPM"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/Edge-Selenium-Tools | NPM"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "Selenium-WebDriver | NPM"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Desenvolvedor da Microsoft"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Downloads-WebDriver | Desenvolvedor da Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Baixar novo navegador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | Galeria do NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Galeria do NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium. WebDriver 3.141.0 | Galeria do NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium. WebDriver 4.0.0-alpha05 | Galeria do NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "Pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-Selenium-ferramentas | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "Selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Chromeoptions Class-WebDriver | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem periféricos | Wikipédia"  
