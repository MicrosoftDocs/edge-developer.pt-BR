---
description: Automatizar e testar o controle WebView2 usando o Microsoft Edge driver
title: Automatizando e testando o WebView2 com o Microsoft Edge driver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Driver do Microsoft Edge
ms.openlocfilehash: a91c01d1ad765dae45061e382daedc2295d70bb8
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926440"
---
# Automatizando e testando o WebView2 com o Microsoft Edge driver

Como o WebView2 utiliza a plataforma Web Chromium, WebView2 os desenvolvedores podem aproveitar as ferramentas padrão da Web para depuração e automação. Uma dessas ferramentas é Selenium, que implementa a API do W3C [WebDriver](https://www.w3.org/TR/webdriver2/) , que pode ser usada para criar testes automatizados que simulam interações do usuário.

Veja como começar:

## Etapa 1: baixar a amostra de WebView2API

Se você não tiver um projeto existente do WebView2, baixe o [aplicativo de exemplo do WebView2API](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample), um exemplo abrangente do SDK WebView2 mais recente. Verifique se você já tem satisfeito por estes [pré-requisitos](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites).

Depois de clonar o repositório, compile o projeto no Visual Studio. Ele deve ter uma aparência semelhante a esta:

![texto alternativo](../media/webdriver/sample-app.png)

## Etapa 2: instalar o driver Microsoft Edge

Siga as instruções para instalar o [Driver do Microsoft Edge](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) o driver específico do navegador exigido pelo Selenium para automatizar e testar o WebView2.

É importante verificar se a versão do driver do Microsoft Edge corresponde à versão do Microsoft Edge usada pelo aplicativo. Para que a amostra WebView2API funcione, certifique-se de que sua versão do Microsoft Edge é maior ou igual à versão compatível da versão mais recente do SDK encontrada [nas nossas notas de versão](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes). Para descobrir qual versão do Microsoft Edge você tem atualmente, carregue `edge://settings/help` no navegador.

## Etapa 3: Adicionar Selenium ao exemplo WebView2API

Nesse ponto, você deve ter o Microsoft Edge instalado, criar um projeto WebView2 e ter instalado o driver Microsoft Edge. Agora, vamos começar a usar o Selenium.

> [!NOTE]
> O Selenium é compatível com C#, Java, Python, JavaScript e Ruby. No entanto, esse guia estará em C#.

1. Comece criando um novo projeto **C# .NET Framework** no **Visual Studio**. Clique em **Avançar** no canto inferior direito para continuar.

![texto alternativo](../media/webdriver/new-project.png)

2. Dê um **nome**ao projeto, salve-o no seu **local**preferido e clique em **criar**.

![texto alternativo](../media/webdriver/app-create.png)

3. Um novo projeto será criado. Neste guia, todo o código será escrito no arquivo **Program.cs** .

![texto alternativo](../media/webdriver/start-app.png)

4. Agora, vamos adicionar **Selenium** ao projeto. Você pode instalar o Selenium pelo **pacote do Selenium. WebDriver NuGet**.

Para baixar o **pacote Selenium. WebDriver NuGet**, no **Visual Studio**, passe o mouse sobre o **Project** e selecione **Manage NuGet Package**. A seguinte tela deve aparecer:

![texto alternativo](../media/webdriver/download-nuget.png)

5. Digite **Selenium. WebDriver** na barra de pesquisa, clique em **Selenium. WebDriver** nos resultados e verifique se a caixa está marcando a caixa ao lado de **incluir a versão de pré-lançamento**. Na janela do lado direito, verifique se a **versão** está definida como **instalar o 4.0.0-alpha04** ou posterior e clique em **instalar**. O NuGet fará o download do Selenium em seu computador.

[Saiba mais sobre o pacote NuGet Selenium. WebDriver.](https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04)

![texto alternativo](../media/webdriver/nuget.png)

6. Use **OpenQA. Selenium. Edge** adicionando a seguinte instrução: ```using OpenQA.Selenium.Edge;``` no início de **Program.cs**

```csharp
using OpenQA.Selenium.Edge;

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Etapa 4: unidade WebView2 com o Selenium e o Microsoft EdgeDriver

1. Primeiro, crie o `EdgeOptions` objeto, copiando o código abaixo:

```csharp
static void Main(string[] args)
{
    // EdgeOptions() requires using OpenQA.Selenium.Edge
    // Construct EdgeOptions with is_legacy = false and the string "webview2"
    EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
```

O `EdgeOptions` objeto tem dois parâmetros:
\
    **Os**
    1. `is_legacy`: definido como `false` , que informa ao Selenium que você está direcionando o novo navegador Microsoft Edge baseado em Chromium.
    2. `"webview2"`: uma cadeia de caracteres que diz ao Selenium que você está dirigindo **WebView2**

2. Em seguida, defina `edgeOptions.BinaryLocation` como o caminho do arquivo do executável do seu projeto WebView2, crie uma cadeia de caracteres chamada `msedgedriverDir` que forneça o caminho do arquivo para o qual você instalou o [Microsoft Edge driver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads)e crie uma cadeia de caracteres chamada `msedgedriverExe` para armazenar o nome do executável do driver Microsoft Edge. Por padrão, o executável é chamado `"msedgedriver.exe"` . Use essas duas cadeias de caracteres para construir o `EdgeDriverService` objeto conforme mostrado abaixo. Por fim, crie o `EdgeDriver` objeto usando `EdgeDriverService` e `EdgeOptions` .

Você pode copiar e colar o seguinte código abaixo `edgeOptions` . Certifique-se de especificar os caminhos de arquivo corretos para o executável do seu projeto e o executável do driver do Microsoft Edge em seu computador.

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

3. Agora, o **EdgeDriver** está configurado para direcionar o **WebView2** em seu projeto. Por exemplo, se você estiver usando o **exemplo WebView2API**, poderá **navegar** para fazer uma <https://microsoft.com> chamada ```e.Url = @"https://www.microsoft.com";``` . Você pode assistir **Selenium** Drive **WebView2** definindo um ponto de interrupção nesta linha e executando o projeto.

```csharp
    //The following will Navigate the WebView2API Sample from bing.com to microsoft.com
    e.Url = @"https://www.microsoft.com";

    //This exits the edge driver
    e.Quit();
}
```

![texto alternativo](../media/webdriver/microsoft.png)

Parabéns! Você automatizau com êxito um projeto do WebView2 e conduziu WebView2 usando o Selenium e o Microsoft Edge driver.

## Próximas etapas

Para saber mais:

- Confira a [documentação do Selenium](https://www.selenium.dev/documentation/en/webdriver/) para obter uma visão abrangente do Selenium de APIs que está disponível para direcionar o WebView2 ou o Microsoft Edge (Chromium)
- Saiba mais sobre o controle [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) e como usá-lo ao inserir conteúdo da Web em seu aplicativo nativo
- Confira a [documentação do driver Microsoft Edge](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) para saber mais sobre como automatizar o Microsoft Edge (Chromium)

## Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  
