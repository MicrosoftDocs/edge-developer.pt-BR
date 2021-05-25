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
ms.openlocfilehash: 5d30fe14051ac8857c6ea4d64b8c8f1f8e8049ac
ms.sourcegitcommit: a7609b75a94755ed983111af7083a0d3bf64eeac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583584"
---
# <a name="use-webdriver-chromium-for-test-automation"></a>Usar o WebDriver (Chromium) para automação de teste  

O WebDriver permite que os desenvolvedores criem testes automatizados que simulam a interação do usuário.  Testes e simulações do WebDriver diferem dos testes de unidade JavaScript das seguintes maneiras.  

*   Acessa a funcionalidade e as informações não disponíveis para JavaScript em execução em navegadores.  
*   Simula eventos do usuário ou eventos no nível do sistema operacional com mais precisão.  
*   Gerencia várias janelas, guias e páginas da Web em uma única sessão de teste.  
*   Executa várias sessões de Microsoft Edge em um computador específico.  
    
A seção a seguir descreve como começar a usar o WebDriver para Microsoft Edge \(Chromium\).  

## <a name="install-microsoft-edge-chromium"></a>Instalar Microsoft Edge (Chromium)  

Certifique-se de [instalar Microsoft Edge (Chromium)][MicrosoftEdge].  Para confirmar se você Microsoft Edge \(Chromium\) instalado, navegue até e verifique se o número da versão é a versão `edge://settings/help` 75 ou posterior.  

## <a name="download-microsoft-edge-driver"></a>Baixar o Driver do Microsoft Edge  

Para começar a automatizar testes, use as etapas a seguir para garantir que a versão do WebDriver instalada corresponde à versão do navegador.  

1.  Encontre sua versão do Microsoft Edge.  
    1.  Navegue até `edge://settings/help`.  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="O número de com build para Microsoft Edge em 15 de abril de 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           O número de com build para Microsoft Edge em 15 de abril de 2021  
        :::image-end:::  
        
1.  Navegue [até Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].  
1.  Navegue **até Obter a versão mais recente**.  
1.  Escolha a com build do canal que corresponde ao número de versão Microsoft Edge.  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="A seção Obter a versão mais recente na página Microsoft Edge Driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       A **seção Obter a versão mais** recente na página Microsoft Edge [Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a>Escolha uma associação de idioma do WebDriver  

O último componente que você deve baixar é um driver de cliente específico do idioma para traduzir seu código \(Python, Java, C\#, Ruby, JavaScript\) em comandos que o driver do Microsoft Edge executa em Microsoft Edge \(Chromium\).  

[Baixe a associação de idioma WebDriver de sua escolha][SeleniumDownloads].  A equipe Microsoft Edge recomenda [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] ou posterior, porque suporta Microsoft Edge \(Chromium\).  No entanto, você pode controlar Microsoft Edge \(Chromium\) em todas as versões mais antigas do Selenium, incluindo a versão selenium 3 estável atual.  

> [!IMPORTANT]
> Se você tiver automatizado ou testado anteriormente Microsoft Edge \(Chromium\) usando e classes, seu código WebDriver não será executado no Microsoft Edge `ChromeDriver` `ChromeOptions` Versão 80 ou posterior.  Para resolver o problema, atualize seus testes para usar a `EdgeOptions` classe e baixe Microsoft Edge [Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].  

### <a name="using-selenium-4"></a>Usando Selenium 4

Selenium 4 tem suporte integrado para Microsoft Edge (Chromium).  Para instalar o Selenium 4, navegue até [Installing Selenium libraries][SeleniumInstallingLibraries].

Quando você usa Selenium 4, não precisa usar As Ferramentas de Selenium para Microsoft Edge.  Selenium Tools for Microsoft Edge for Selenium 3 only.  Se você tentar usar Selenium 4 com Selenium Tools para Microsoft Edge e tentar criar uma nova instância, você obterá `EdgeDriver` o seguinte erro: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'` .  

Se você estiver usando o Selenium 4 e receber esse erro, remova do seu projeto e certifique-se de estar usando o oficial e as classes do `Microsoft.Edge.SeleniumTools` `EdgeOptions` `EdgeDriver` `OpenQA.Selenium.Edge` namespace.

### <a name="using-selenium-3"></a>Usando Selenium 3  

Se você já usa [Selenium 3][|::ref1::|], pode ter testes de navegador existentes e deseja adicionar cobertura para Microsoft Edge \(Chromium\) sem alterar sua versão do Selenium.  Para usar [o Selenium 3][|::ref2::|] para gravar testes automatizados para o Microsoft Edge \(EdgeHTML\) e o Microsoft Edge \(Chromium\), instale o pacote [Ferramentas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar o driver atualizado.  As `EdgeDriver` classes `EdgeDriverService` e incluídas nas ferramentas são totalmente compatíveis com os equivalentes integrados no Selenium 4.  

Use as etapas a seguir para adicionar as [Ferramentas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] e [Selenium 3][|::ref3::|] ao seu projeto.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Adicione os [pacotes Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] e [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] ao seu projeto .NET usando o [NuGet CLI][NugetCLI] ou [Visual Studio][VisualStudio].  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Use [pip][PythonPip] para instalar os [pacotes msedge-selenium-tools][PythonSeleniumTools] e [selenium.][PythonSelenium]  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Se seu projeto Java usar Maven, copie e colar a seguinte dependência ao seu arquivo para adicionar `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

O Java também está disponível para download diretamente na página [Ferramentas de Selenium para Microsoft Edge Versões.][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Use [npm][JavaScript|::ref4::|] para instalar [os pacotes edge-selenium-tools][JavaScriptSeleniumTools] e [selenium-webdriver.][JavaScriptSelenium]  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a>Automatizar Microsoft Edge (Chromium) com o WebDriver  

Para automatizar um navegador usando o WebDriver, primeiro você deve iniciar uma sessão do WebDriver usando sua associação de idioma WebDriver preferida.  Uma sessão é uma única instância em execução de um navegador controlado usando comandos WebDriver.  Inicie uma sessão do WebDriver para iniciar uma nova instância do navegador.  A instância do navegador lançada permanece aberta até que você feche a sessão do WebDriver.  

O conteúdo a seguir orienta você a usar Selenium para iniciar uma sessão do WebDriver com Microsoft Edge \(Chromium\).  Você pode executar os exemplos usando Selenium 3 ou 4.  Para usar com Selenium 3, o pacote [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] deve ser instalado.  

### <a name="automate-microsoft-edge-chromium"></a>Automatizar Microsoft Edge (Chromium)  

Selenium usa a `EdgeDriver` classe para gerenciar uma sessão Microsoft Edge \(Chromium\).  Para iniciar uma sessão e automatizar Microsoft Edge \(Chromium\), crie um novo objeto e passe um objeto com a propriedade `EdgeDriver` `EdgeOptions` definida como `UseChromium` `true` .  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

A classe dá suporte Microsoft Edge \(Chromium\) e não dá suporte `EdgeDriver` Microsoft Edge \(EdgeHTML\).  Para uso básico, você pode criar um `EdgeDriver` sem fornecer `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Se o administrador de IT tiver definido a política [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] como , o driver do Microsoft Edge será impedido de conduzir o Microsoft Edge \(Chromium\), porque o driver usa o `2` Microsoft Edge [DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  Verifique se [a política DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] está definida como ou para automatizar Microsoft Edge `0` `1` (Chromium).  

### <a name="choose-specific-browser-binaries-chromium-only"></a>Escolha Binários específicos do navegador (somente Chromium))  

Você pode iniciar uma sessão do WebDriver com binários Microsoft Edge \(Chromium\).  Por exemplo, você pode executar testes usando os canais [Microsoft Edge de visualização,][MicrosoftedgeinsiderDownload] como Microsoft Edge Beta.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a>Personalizar o serviço Microsoft Edge driver  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Quando você usa a classe para criar uma instância de classe, ela cria e inicia a classe apropriada para `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou Microsoft Edge \(Chromium\).  

Se você quiser criar um , use o método para criar um configurado para `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\).  O `CreateChromiumService()` método é útil quando você precisa adicionar personalizações.  Por exemplo, o código a seguir inicia a saída de log detalhado.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Você não precisa fornecer o `EdgeOptions` objeto quando passar para a `EdgeDriverService` `EdgeDriver` instância.  A classe usa as opções padrão `EdgeDriver` para Microsoft Edge \(EdgeHTML\) ou Microsoft Edge \(Chromium\) com base no serviço que você fornece.  
> No entanto, se você quiser fornecer ambas as classes, verifique se ambas estão configuradas para `EdgeDriverService` a mesma versão do `EdgeOptions` Microsoft Edge.  Por exemplo, você pode usar uma classe padrão Microsoft Edge \(EdgeHTML\) e Chromium `EdgeDriverService` propriedades na `EdgeOptions` classe.  A `EdgeDriver` classe lança um erro para impedir o uso de versões diferentes.  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Quando você usa Python, `Edge` o objeto cria e gerencia o `EdgeService` .  Para configurar `EdgeService` o , passe argumentos extras para o objeto conforme indicado no código a `Edge` seguir.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Use o método para criar um configurado para Microsoft Edge `createDefaultService()` `EdgeDriverService` \(Chromium\).  Use Java do sistema para personalizar os serviços de driver no Java.  Por exemplo, o código a seguir usa a `"webdriver.edge.verboseLogging"` propriedade para ativar a saída de log detalhado.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Ao usar JavaScript, crie e configure um `Service` com a `ServiceBuilder` classe.  Opcionalmente, você pode passar o objeto para `Service` o `Driver` objeto, que inicia \(e para\) o serviço para você.  
Para configurar `Service` o , execute outro método na classe antes de usar o `ServiceBuilder` `build()` método.  Em seguida, `service` passe o parâmetro como um no `Driver.createSession()` método.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a>Usar Chromium-Specific opções  

Se você definir a propriedade como , você poderá usar a classe para acessar as mesmas propriedades e métodos específicos do Chromium que são usados quando você automatiza outros navegadores `UseChromium` `true` `EdgeOptions` Chromium. [][WebdriverCapabilitiesEdgeOptions]  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> Se a propriedade estiver definida como , você não poderá usar propriedades e métodos para Microsoft Edge `UseChromium` `true` \(EdgeHTML\).  

## <a name="other-webdriver-installation-options"></a>Outras opções de instalação do WebDriver  

### <a name="docker"></a>Docker  

Se você usar [o Docker,][DockerHub]execute o seguinte comando para baixar uma imagem pré-configurada com Microsoft Edge \(Chromium\) e [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pré-instalado.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Para obter mais informações, navegue até o [contêiner msedgedriver no Hub do Docker.][DockerHubMsedgedriver]  

## <a name="next-steps"></a>Próximas etapas  

Para obter mais informações sobre o WebDriver e como gravar testes automatizados do WebDriver usando Selenium, navegue até a documentação [de Selenium][SeleniumDocumentation].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

A Microsoft Edge equipe está ávida para ouvir seus comentários sobre como usar o WebDriver, Selenium e Microsoft Edge.  Para enviar à equipe suas perguntas e comentários, escolha o ícone **Enviar Comentários** no Microsoft Edge DevTools ou envie um tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Feedback no Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   O **ícone Enviar Comentários** no Microsoft Edge DevTools  
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
