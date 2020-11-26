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
# Automatizando e testando o WebView2 com o Microsoft Edge driver  

Como o WebView2 usa a plataforma da Web Microsoft Edge \ (Chromium \), os desenvolvedores WebView2 \ (você \) podem aproveitar a ferramenta padrão da Web para depuração e automação.  O Selenium é uma dessas ferramentas.  Ele implementa a API do W3C para [WebDriver][W3cWebdriver2] .  Você pode usar Selenium para criar testes automatizados para simular interações do usuário.  

Comece a usar as etapas a seguir.  

## Etapa 1: baixar a amostra de WebView2API  

Se você não tiver um projeto WebView2 existente, baixe o [aplicativo de exemplo WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], um exemplo abrangente do SDK WebView2 mais recente.  Certifique-se de que você tenha satisfeito com os [pré-requisitos do aplicativo de exemplo WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].  

Depois de clonar o repositório, compile o projeto no Visual Studio.  Ele deve ter a aparência da figura a seguir.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicativo de exemplo WebView2API" lightbox="../media/webdriver/sample-app.png":::
   Aplicativo de exemplo WebView2API  
:::image-end:::  

## Etapa 2: instalar o driver Microsoft Edge  

Siga as instruções para instalar o [Driver do Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] o driver específico do navegador exigido pelo Selenium para automatizar e testar o WebView2.  

Verifique se a versão do driver do Microsoft Edge corresponde à versão do WebView2 Runtime que você usa em seu aplicativo.  Para que a amostra WebView2API funcione, certifique-se de que sua versão do WebView2 do tempo de execução é maior ou igual à versão compatível da versão mais recente do SDK do WebView2.  Para localizar a versão mais recente do SDK do WebView2, acesse [WebView2 notas de versão][Webview2Releasenotes].  Para saber qual é a versão do tempo de execução do WebView2 que você tem no momento, navegue até `edge://settings/help` .  

## Etapa 3: Adicionar Selenium ao exemplo WebView2API  

Nesse ponto, você deve ter o WebView2 Runtime instalado, criar um projeto WebView2 e instalar o Microsoft Edge driver.  Agora, comece a usar o Selenium.  

> [!NOTE]
> O Selenium dá suporte a C \ #, Java, Python, JavaScript e Ruby.  No entanto, o guia a seguir é escrito usando C \ #.  

1.  Comece criando um novo projeto **C# .NET Framework** no **Visual Studio**.  Escolha **Avançar** no canto inferior direito para continuar.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Criar um novo projeto" lightbox="../media/webdriver/new-project.png":::
       Criar um novo projeto  
    :::image-end:::  
    
1.  Dê um **nome**ao projeto, salve-o no seu **local**preferido e escolha **criar**.  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar seu novo projeto" lightbox="../media/webdriver/app-create.png":::
       Configurar seu novo projeto  
    :::image-end:::  
    
1.  Um novo projeto é criado.  Neste guia, todo o código é escrito no `Program.cs` arquivo.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Novo projeto" lightbox="../media/webdriver/start-app.png":::
       Novo projeto  
    :::image-end:::  
    
1.  Agora, adicione **Selenium** ao projeto.  Instale o Selenium usando o **pacote NuGet Selenium. WebDriver**.  
    
    Para baixar o **pacote Selenium. WebDriver NuGet**, no **Visual Studio**, passe o mouse sobre o **Project**e escolha **gerenciar pacote NuGet**.  A tela a seguir deve ser exibida.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Baixar pacote NuGet" lightbox="../media/webdriver/download-nuget.png":::
       Baixar pacote NuGet  
    :::image-end:::  
    
1.  Digite `Selenium.WebDriver` na barra de pesquisa, escolha **Selenium. WebDriver** nos resultados e certifique-se de fazer uma marca de seleção na caixa ao lado de **incluir pré-lançamento**.  Na janela do lado direito, verifique se a **versão** está definida como **instalar o 4.0.0-alpha04** ou posterior e escolha **instalar**.  O NuGet baixa o Selenium em seu computador.  
    
    Para saber mais sobre o pacote NuGet Selenium. WebDriver, navegue até [Selenium. WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Gerenciar pacote NuGet" lightbox="../media/webdriver/nuget.png":::
       Gerenciar pacote NuGet  
    :::image-end:::  
    
1.  Use `OpenQA.Selenium.Edge` ao adicionar a seguinte instrução:  `using OpenQA.Selenium.Edge;` no início do `Program.cs` arquivo.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## Etapa 4: unidade WebView2 com o Selenium e o Microsoft Edge driver  

1.  Primeiro, crie o `EdgeOptions` objeto, copiando o trecho de código a seguir.  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    O `EdgeOptions` objeto assume os dois parâmetros a seguir.  
    
    | Parâmetro | Detalhes |    
    |:--- |:--- |  
    | `is_legacy` | Definido como `false` , que informa ao Selenium que você está direcionando o novo navegador Microsoft Edge baseado em Chromium. |  
    | `"webview2"` | Uma cadeia de caracteres que informa ao Selenium que você está dirigindo WebView2. |  
    
1.  Em seguida, defina o `edgeOptions.BinaryLocation` caminho do arquivo do tempo de execução do projeto do WebView2, crie uma cadeia de caracteres chamada `msedgedriverDir` que forneça o caminho do arquivo para o qual você instalou o [Microsoft Edge driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]e crie uma cadeia de caracteres chamada `msedgedriverExe` para armazenar o nome do tempo de execução do driver do Microsoft Edge.  Por padrão, o tempo de execução é nomeado `msedgedriver.exe` . Use essas duas cadeias de caracteres para construir o `EdgeDriverService` objeto conforme mostrado abaixo.  Por fim, crie o `EdgeDriver` objeto usando `EdgeDriverService` e `EdgeOptions` .  
    
    Você pode copiar e colar o seguinte código abaixo `edgeOptions` .  Certifique-se de especificar os caminhos de arquivo corretos para o tempo de execução do projeto e o tempo de execução do driver do Microsoft Edge em seu computador.  
    
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
    
3.  Agora, `EdgeDriver` está configurado para direcionar o WebView2 em seu projeto.  Por exemplo, se você estiver usando o **exemplo WebView2API**, poderá navegar `https://microsoft.com` executando o `e.Url = @"https://www.microsoft.com";` comando.  Verifique a unidade Selenium WebView2 definindo um ponto de interrupção na linha e executando o projeto.  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium executando o WebView2" lightbox="../media/webdriver/microsoft.png":::
       Selenium executando o WebView2  
    :::image-end:::

Parabéns.  Você automatizau com êxito um projeto do WebView2 e conduziu WebView2 usando o Selenium e o Microsoft Edge driver.  

## Consulte também  

*   Para ter uma visão abrangente de como as APIs Selenium unidades WebView2 ou Microsoft Edge \ (Chromium \), navegue até [WebDriver na documentação do Selenium][SeleniumWebdriver]   
*   Para saber mais sobre o controle WebView2 e como usá-lo ao inserir conteúdo da Web em seu aplicativo nativo, navegue até [introdução ao Microsoft Edge WebView2][WebViewIndex].  
*   Para saber mais sobre como automatizar o Microsoft Edge \ (Chromium \), navegue para [usar o WebDriver (Chromium) para automação de teste][WebdriverChromium]   
    
## Entrar em contato com a equipe do Microsoft Edge WebView  

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
