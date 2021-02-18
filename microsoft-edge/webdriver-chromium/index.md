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
# Usar o WebDriver (Chromium) para automação de teste  

O WebDriver permite que os desenvolvedores criem testes automatizados que simulam a interação do usuário.  Testes e simulações do WebDriver são diferentes dos testes de unidade JavaScript das seguintes maneiras.  

*   Acessa a funcionalidade e as informações não disponíveis para JavaScript em execução em navegadores.  
*   Simula eventos do usuário ou eventos no nível do sistema operacional com mais precisão.  
*   Gerencia várias janelas, guias e páginas da Web em uma única sessão de teste.  
*   Executa várias sessões do Microsoft Edge em um computador específico.  
    
A seção a seguir descreve como começar a usar o WebDriver para Microsoft Edge \(Chromium\).  

## Instalar o Microsoft Edge (Chromium)  

Certifique-se [de instalar o Microsoft Edge (Chromium).][MicrosoftEdge]  Para confirmar se você tem o Microsoft Edge \(Chromium\) instalado, navegue até e verifique se o número da versão é `edge://settings/help` a versão 75 ou posterior.  

## Baixar o Driver do Microsoft Edge  

Para começar a automatizar testes, use as etapas a seguir para garantir que a versão do WebDriver instalada corresponde à versão do navegador.  

1.  Para exibir a versão do Microsoft Edge, navegue até `edge://settings/help` .  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="O número de build do Microsoft Edge Canary em 10 de fevereiro de 2021" lightbox="./media/microsoft-edge-version.msft.png":::
       O número de build do Microsoft Edge Canary em 10 de fevereiro de 2021  
    :::image-end:::  
    
1.  Navegue [até o Driver do Microsoft Edge,][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]na seção **Downloads,** e baixe o WebDriver que corresponde ao número de versão do Microsoft Edge.  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="A seção Downloads no Driver do Microsoft Edge" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       A **seção Downloads** no [Driver do Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  

## Escolher uma associação de idioma do WebDriver  

O último componente que você deve baixar é um driver de cliente específico da linguagem para traduzir seu código \(Python, Java, C\#, Ruby, JavaScript\) em comandos que o Microsoft Edge Driver executa no Microsoft Edge \(Chromium\).  

[Baixe a associação de idioma do WebDriver de sua escolha.][SeleniumDownloads]  A equipe do Microsoft Edge recomenda [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] ou posterior, porque dá suporte ao Microsoft Edge \(Chromium\).  No entanto, você pode controlar o Microsoft Edge \(Chromium\) em todas as versões mais antigas do Selenium, incluindo a versão estável atual do Selenium 3.  

> [!IMPORTANT]
> Se você tiver automatizado ou testado anteriormente o Microsoft Edge \(Chromium\) usando e classes, o código do WebDriver não será executado no `ChromeDriver` `ChromeOptions` Microsoft Edge Versão 80 ou posterior.  Para resolver o problema, atualize seus testes para usar a `EdgeOptions` classe e baixe o Driver do Microsoft [Edge.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  

### Usar Selenium 3  

Se você já usa [Selenium 3,][|::ref1::|]talvez tenha testes de navegador existentes e queira adicionar cobertura para o Microsoft Edge \(Chromium\) sem alterar sua versão de Selenium.  Para usar [Selenium 3][|::ref2::|] para gravar testes automatizados para o Microsoft Edge \(EdgeHTML\) e o Microsoft Edge \(Chromium\), instale o pacote [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar o driver atualizado.  As classes e as classes incluídas nas ferramentas são totalmente compatíveis com `EdgeDriver` `EdgeDriverService` os equivalentes integrados no Selenium 4.  

Use as etapas a seguir para adicionar as [Ferramentas Selenium do Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] e [Selenium 3][|::ref3::|] ao seu projeto.  

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Adicione os [pacotes Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] e [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] ao seu projeto .NET usando a [CLI do NuGet][NugetCLI] ou [o Visual Studio.][VisualStudio]  

#### [Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Use [pip][PythonPip] para instalar os [pacotes msedge-selenium-tools][PythonSeleniumTools] e [selenium.][PythonSelenium]  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Se seu projeto Java usa Maven, copie e copie e copie a seguinte dependência ao seu arquivo para adicionar `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

O pacote Java também está disponível para download diretamente na página Ferramentas [Selenium para Lançamentos do Microsoft Edge.][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Use [npm][JavaScript|::ref4::|] para instalar os [pacotes edge-selenium-tools][JavaScriptSeleniumTools] e [selenium-webdriver.][JavaScriptSelenium]  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Automatizar o Microsoft Edge (Chromium) com o WebDriver  

Para automatizar um navegador usando o WebDriver, primeiro você deve iniciar uma sessão do WebDriver usando sua associação de idioma preferencial do WebDriver.  Uma sessão é uma única instância em execução de um navegador controlado usando comandos do WebDriver.  Inicie uma sessão do WebDriver para iniciar uma nova instância do navegador.  A instância do navegador lançada permanece aberta até que você feche a sessão do WebDriver.  

O conteúdo a seguir orienta você a usar Selenium para iniciar uma sessão do WebDriver com o Microsoft Edge \(Chromium\).  Você pode executar os exemplos usando Selenium 3 ou 4.  Para usar com Selenium 3, o pacote [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] deve ser instalado.  

### Automatizar o Microsoft Edge (Chromium)  

Selenium usa a `EdgeDriver` classe para gerenciar uma sessão do Microsoft Edge \(Chromium\).  Para iniciar uma sessão e automatizar o Microsoft Edge \(Chromium\), crie um novo objeto e passe um objeto para ele com a propriedade `EdgeDriver` `EdgeOptions` definida como `UseChromium` `true` .  

#### [C#](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

A `EdgeDriver` classe só dá suporte ao Microsoft Edge \(Chromium\) e não dá suporte ao Microsoft Edge \(EdgeHTML\).  Para uso básico, você pode criar um `EdgeDriver` sem fornecer `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [JavaScript](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Se o administrador de IT definiu a política [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] como , o Driver do Microsoft Edge é impedido de conduzir o `2`  [Microsoft][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] Edge \(Chromium\), porque o driver usa o [Microsoft Edge DevTools][DevtoolsIndex].  Verifique se [a política DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] está definida para `0` ou para `1` automatizar o Microsoft Edge (Chromium).  

### Escolher binários específicos do navegador (somente Chromium)  

Você pode iniciar uma sessão do WebDriver com binários específicos do Microsoft Edge \(Chromium\).  Por exemplo, você pode executar testes usando os canais de visualização do [Microsoft Edge,][MicrosoftedgeinsiderDownload] como o Microsoft Edge Beta.  

#### [C#](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Personalizar o Serviço de Driver do Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Quando você usa a classe para criar uma instância de classe, ela cria e inicia a classe apropriada para `EdgeOptions` `EdgeDriver` o Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou o Microsoft Edge \(Chromium\).  

Se você quiser criar um , use o método `EdgeDriverService` para criar um configurado para o Microsoft Edge `CreateChromiumService()` \(Chromium\).  O `CreateChromiumService()` método é útil quando você precisa adicionar personalizações.  Por exemplo, o código a seguir inicia a saída detalhada do log.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Você não precisa fornecer o `EdgeOptions` objeto quando passar para a `EdgeDriverService` `EdgeDriver` instância.  A `EdgeDriver` classe usa as opções padrão para o Microsoft Edge \(EdgeHTML\) ou o Microsoft Edge \(Chromium\) com base no serviço que você fornece.  
> No entanto, se você quiser fornecer as duas classes, verifique se ambas estão `EdgeDriverService` `EdgeOptions` configuradas para a mesma versão do Microsoft Edge.  Por exemplo, você pode usar uma classe padrão do Microsoft Edge \(EdgeHTML\) e propriedades `EdgeDriverService` do Chromium na `EdgeOptions` classe.  A `EdgeDriver` classe lança um erro para impedir o uso de versões diferentes.  

#### [Python](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Quando você usa o Python, `Edge` o objeto cria e gerencia o `EdgeService` .  Para configurar o `EdgeService` , passe argumentos extras para `Edge` o objeto conforme indicado no código a seguir.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [Java](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Use o `createDefaultService()` método para criar um configurado para o Microsoft Edge `EdgeDriverService` \(Chromium\).  Use as propriedades do sistema Java para personalizar serviços de driver em Java.  Por exemplo, o código a seguir usa a `"webdriver.edge.verboseLogging"` propriedade para ativar a saída do log detalhado.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Ao usar JavaScript, crie e configure um `Service` com a `ServiceBuilder` classe.  Opcionalmente, você pode passar o objeto para o objeto, que inicia `Service` `Driver` \(e interrompe\) o serviço para você.  
Para configurar `Service` o método , execute outro método na classe antes de usar o `ServiceBuilder` `build()` método.  Em seguida, `service` passe o parâmetro como um no `Driver.createSession()` método.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Usar Chromium-Specific opções  

Se você definir a propriedade como , você pode usar a classe para acessar as mesmas propriedades e métodos específicos do Chromium que são usados quando você automatizar outros navegadores `UseChromium` `true` `EdgeOptions` Chromium. [][WebdriverCapabilitiesEdgeOptions]  

#### [C#](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Python](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [Java](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [JavaScript](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> Se a propriedade estiver definida como , você não poderá usar propriedades e métodos para `UseChromium` `true` o Microsoft Edge \(EdgeHTML\).  

## Outras opções de instalação do WebDriver  

### Rêo  

Se você usar [Ay como][Chocolatey] seu gerenciador de pacotes, execute o seguinte comando para instalar o Microsoft Edge Driver.  

```console
choco install selenium-chromium-edge-driver
```  

Para obter mais informações, navegue [até Selenium Chromium Edge Driver em Mila .][ChocolateyPackagesSeleniumChromiumEdgeDriver]  

### Docker  

Se você usar [o Docker,][DockerHub]execute o seguinte comando para baixar uma imagem pré-configurada com o Microsoft Edge \(Chromium\) e o Driver do [Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pré-instalados.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Para obter mais informações, navegue até o contêiner [msedgedriver no Hub do Docker.][DockerHubMsedgedriver]  

## Próximas etapas  

Para saber mais sobre o WebDriver e como escrever testes automatizados do WebDriver usando Selenium, navegue até a documentação [Selenium.][SeleniumDocumentation]  

## Entrar em contato com a equipe Microsoft Edge DevTools  

A equipe do Microsoft Edge está ansioso para ouvir seus comentários sobre como usar o WebDriver, Selenium e Microsoft Edge.  Para enviar suas perguntas e comentários à equipe, escolha o ícone Enviar **Comentários** no Microsoft Edge DevTools ou envie um tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Comentários no Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   O **ícone Enviar Comentários** no Microsoft Edge DevTools  
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
