---
description: Automatizar e testar o Controle WebView2 usando Microsoft Edge Driver
title: Automatizando e testando WebView2 com Microsoft Edge Driver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: 37c0e41e11693c8a21b7240bf9370fd658834cff
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535741"
---
# <a name="automate-and-test-webview2-with-microsoft-edge-driver"></a>Automatizar e testar WebView2 com Microsoft Edge Driver  

Como o WebView2 usa a plataforma web Microsoft Edge \(Chromium\), os desenvolvedores do WebView2 \(you\) podem tirar proveito da ferramenta web padrão para depuração e automação.  Selenium é uma dessas ferramentas.  Ele implementa a API [W3C WebDriver.][W3cWebdriver2]  Você pode usar Selenium para criar testes automatizados para simular interações do usuário.  

Começar com as etapas a seguir.  

## <a name="step-1--download-webview2api-sample"></a>Etapa 1: Baixar Exemplo de WebView2API  

Se você não tiver um projeto WebView2 existente, baixe o aplicativo De exemplo [WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], um exemplo abrangente do SDK webView2 mais recente.  Certifique-se de ter atendido os pré-requisitos do aplicativo de exemplo [WebView2API.][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]  

Depois de clonar o repo, crie o projeto Visual Studio.  Deve se parecer com a figura a seguir.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicativo de exemplo WebView2API" lightbox="../media/webdriver/sample-app.png":::
   Aplicativo de exemplo WebView2API  
:::image-end:::    

## <a name="step-2--install-microsoft-edge-driver"></a>Etapa 2: Instalar Microsoft Edge Driver  

Siga as instruções para instalar [Microsoft Edge Driver o][WebdriverChromiumDownloadMicrosoftEdgeDriver] driver específico do navegador exigido pela Selenium para automatizar e testar o WebView2.  

Verifique se a versão do Microsoft Edge Driver corresponde à versão do WebView2 Runtime que o aplicativo usa.  Para que o Exemplo de WebView2API funcione, certifique-se de que sua versão do WebView2 Runtime seja maior ou igual que a versão suportada da versão mais recente do SDK WebView2.  Para localizar a versão mais recente do SDK webView2, navegue até [WebView2 release notes][Webview2ReleaseNotes].  Para descobrir qual versão do WebView2 Runtime você tem no momento, navegue até `edge://settings/help` .  

## <a name="step-3--add-selenium-to-the-webview2api-sample"></a>Etapa 3: Adicionar Selenium ao exemplo WebView2API  

Neste ponto, você deve ter WebView2 Runtime instalado, criado um projeto WebView2 e instalado Microsoft Edge Driver.  Agora, começar a usar Selenium.  

> [!NOTE]
> Selenium dá suporte a C\#, Java, Python, Javascript e Ruby.  No entanto, o guia a seguir é escrito usando C\#.  

1.  Comece criando um novo projeto **C# .NET Framework** no **Visual Studio**.  Escolha **Next** no canto inferior direito para continuar.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Criar um novo projeto" lightbox="../media/webdriver/new-project.png":::
       Criar um novo projeto  
    :::image-end:::  
    
1.  Dê um nome ao seu **projeto,** salve-o em seu **local preferencial**e escolha **Criar**.  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar seu novo projeto" lightbox="../media/webdriver/app-create.png":::
       Configurar seu novo projeto  
    :::image-end:::  
    
1.  Um novo projeto é criado.  Neste guia, todo o código é gravado no `Program.cs` arquivo.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Novo projeto" lightbox="../media/webdriver/start-app.png":::
       Novo projeto  
    :::image-end:::  
    
1.  Agora adicione **Selenium** ao projeto.  Instale Selenium usando o pacote **Selenium.WebDriver NuGet .**  
    
    Para baixar o pacote **selenium.WebDriver**NuGet , em **Visual Studio,** passe o mouse no Project **e**escolha **Gerenciar NuGet Pacote**.  A tela a seguir deve aparecer.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Baixar NuGet pacote" lightbox="../media/webdriver/download-nuget.png":::
       Baixar NuGet pacote  
    :::image-end:::  
    
1.  Digite `Selenium.WebDriver` na barra de pesquisa, escolha **Selenium.WebDriver** a partir dos resultados e certifique-se de marcar a caixa ao lado para incluir **a pré-versão**.  Na janela do lado direito, verifique se a **versão** está definida para instalar **4.0.0-alfa04** ou posterior e escolha **Instalar**.  NuGet baixa Selenium para seu computador.  
    
    Para saber mais sobre o pacote selenium.WebDriver NuGet, navegue até [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Gerenciar NuGet pacote" lightbox="../media/webdriver/nuget.png":::
       Gerenciar NuGet pacote  
    :::image-end:::  
    
1.  Use `OpenQA.Selenium.Edge` adicionando a seguinte instrução:  `using OpenQA.Selenium.Edge;` no início do `Program.cs` arquivo.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a>Etapa 4: Drive WebView2 com Selenium e Microsoft Edge Driver  

1.  Primeiro, crie `EdgeOptions` o objeto, copiando o trecho de código a seguir.  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    O `EdgeOptions` objeto recebe os dois parâmetros a seguir.  
    
    | Parâmetro | Detalhes |    
    |:--- |:--- |  
    | `is_legacy` | De acordo `false` com , que informa a Selenium que você está conduzindo o novo Chromium de Microsoft Edge navegador. |  
    | `"webview2"` | Uma cadeia de caracteres que informa a Selenium que você está conduzindo WebView2. |  
    
1.  Em seguida, de acordo com o caminho do arquivo do seu tempo de execução do projeto WebView2, crie uma cadeia de caracteres chamada que fornece o caminho do arquivo para onde você instalou o driver do Microsoft Edge e crie uma cadeia de caracteres chamada para armazenar o nome do tempo de execução do `edgeOptions.BinaryLocation` `msedgedriverDir` driver [][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads] `msedgedriverExe` Microsoft Edge.  Por padrão, o tempo de execução é chamado `msedgedriver.exe` . Use essas duas cadeias de caracteres para construir `EdgeDriverService` o objeto conforme mostrado abaixo.  Por fim, crie `EdgeDriver` o objeto usando e `EdgeDriverService` `EdgeOptions` .  
    
    Você pode copiar e colar o seguinte código abaixo `edgeOptions` .  Certifique-se de especificar os caminhos de arquivo corretos para o tempo de execução do seu projeto e o tempo de execução Microsoft Edge driver em seu computador.  
    
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
    
3.  Agora, `EdgeDriver` está configurado para conduzir o WebView2 em seu projeto.  Por exemplo, se você estiver usando o **Exemplo WebView2API,** poderá navegar `https://microsoft.com` para executando o `e.Url = @"https://www.microsoft.com";` comando.  Verifique o WebView2 de unidade de selenium definindo um ponto de interrupção na linha e executando o projeto.  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium executando WebView2" lightbox="../media/webdriver/microsoft.png":::
       Selenium executando WebView2  
    :::image-end:::
    
Parabéns.  Você automatiza com êxito um projeto WebView2 e orienta WebView2 usando Selenium e Microsoft Edge Driver.  

## <a name="see-also"></a>Ver também  

*   Para uma visão abrangente de como as APIs Selenium conduzEm WebView2 ou Microsoft Edge \(Chromium\), navegue até WebDriver na documentação [selenium][SeleniumWebdriver]   
*   Para saber mais sobre o controle WebView2 e como usá-lo ao incorporar conteúdo da Web em seu aplicativo nativo, navegue até Introdução ao Microsoft Edge [WebView2][WebViewIndex].  
*   Para saber mais sobre como automatizar Microsoft Edge \(Chromium\), navegue até [Usar o WebDriver (Chromium) para automação de teste][WebdriverChromium]   
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Usar o WebDriver (Chromium) para testes de automação | Microsoft Docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Baixar Microsoft Edge Driver - Usar o WebDriver (Chromium) para testes de automação | Microsoft Docs"  
[WebViewIndex]: ../index.md "Introdução ao Microsoft Edge WebView2 - Microsoft Docs"  
[Webview2ReleaseNotes]: ../release-notes.md "Notas de versão do SDK WebView2 | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Baixe o WebDriver | Microsoft Edge Desenvolvedor"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemplo de API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Pré-requisitos - Exemplo de API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium.WebDriver 4.0.0-alpha04 | NuGet Galeria"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
