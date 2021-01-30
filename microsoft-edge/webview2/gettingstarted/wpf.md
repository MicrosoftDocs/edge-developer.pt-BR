---
description: Guia de iniciação com WebView2 para aplicativos WPF
title: Getting started with WebView2 for WPF apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, wpf apps, wpf, edge, CoreWebView2, controle de navegador, html de borda, getting started, Getting Started, .NET
ms.openlocfilehash: de67b8a2da8cda0339b5e8d0b96cf4c3df260ec6
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306142"
---
# Getting started with WebView2 in WPF

Neste artigo, aprenda a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obter mais informações sobre APIs individuais, navegue até a [referência de API.][DotnetApiMicrosoftWebWebview2Wpf]  

## Pré-requisitos  

Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir.  

*   [WebView2 Runtime][Webview2Installer] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no sistema operacional suportado \(atualmente Windows 10, Windows 8.1 e Windows 7\).  
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 ou posterior.  
    
## Etapa 1: criar um aplicativo de janela única  

Comece com um projeto de área de trabalho básico que contenha uma única janela principal.  

1.  No Visual Studio, escolha **WPF .NET Core App** \(ou **WPF .NET Framework App**\) > **Próximo.**  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Núcleo WPF":::
             Núcleo WPF :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Estrutura WPF":::
             Estrutura WPF :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Insira valores para **o nome do projeto** e o **local.**  Escolha **o .NET Framework 4.6.2** ou posterior \(ou **.NET Core 3.0** ou posterior\).  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Criar núcleo":::
                 Criar núcleo :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Criar Estrutura":::
                 Criar Estrutura :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  Para criar seu projeto, escolha **Criar**.  
    
## Etapa 2 - Instalar o SDK webView2  

Use NuGet para adicionar o SDK WebView2 ao projeto.  

1.  Passe o mouse sobre o projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Gerenciar Pacotes **NuGet...**.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gerenciar pacotes NuGet":::
       Gerenciar pacotes NuGet
    :::image-end:::
    
1.  Na barra de pesquisa, digite > `Microsoft.Web.WebView2` escolha **Microsoft.Web.WebView2**.  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Pronto para começar a desenvolver aplicativos usando a API WebView2.  Para criar e executar o projeto, selecione `F5` .  O projeto em execução exibe uma janela vazia.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicativo vazio":::
       Aplicativo vazio
    :::image-end:::  
    
## Etapa 3 : Criar um único WebView em MainWindow.xaml  

Em seguida, adicione um WebView ao seu aplicativo.  

1.  No `MainWindow.xaml` arquivo, para adicionar o namespace XAML WebView2, insira a seguinte linha dentro da `<Window/>` marca.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Certifique-se de que `MainWindow.xaml` o código se parece com o trecho de código a seguir.  
    
    ```xml
    <Window x:Class="WPF_Getting_Started.MainWindow"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
            xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
            xmlns:local="clr-namespace:{YOUR PROJECT NAME}"
            xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
            mc:Ignorable="d"
            Title="MainWindow"
            Height="450"
            Width="800"
    >
        <Grid>
        
        </Grid>
    </Window>
    ```  
    
1.  Para adicionar o controle WebView2, substitua as `<Grid>` marcas pelo trecho de código a seguir.  A `Source` propriedade define o URI inicial exibido no controle WebView2.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Para criar e executar o projeto, selecione `F5`  Garantir que seu controle WebView2 seja [https://www.microsoft.com][|::ref1::|Main] exibido.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## Etapa 4 - Navegação  

Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe adicionando uma barra de endereços ao aplicativo.

1.  No arquivo, adicione uma barra de endereços copiando e copiando o trecho de código a seguir dentro do que `MainWindow.xaml` `<DockPanel>` contém o WebView.  
    
    ```xml
    <DockPanel DockPanel.Dock="Top">
        <Button x:Name="ButtonGo"
                DockPanel.Dock="Right"
                Click="ButtonGo_Click"
                Content="Go"
        />
        <TextBox Name="addressBar"/>
    </DockPanel>
    ```  
    
    Verifique se `<DockPanel>` a seção do arquivo corresponde ao trecho de código a `MainWindow.xaml` seguir.  
    
    ```xml
    <DockPanel>
        <DockPanel DockPanel.Dock="Top">
            <Button x:Name="ButtonGo" DockPanel.Dock="Right" Click="ButtonGo_Click" Content="Go"/>
            <TextBox Name = "addressBar"/>
        </DockPanel>
        <wv2:WebView2 Name = "webView"
                      Source = "https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  No Visual Studio, no `MainWindow.xaml.cs` arquivo, para adicionar o namespace, insira o trecho de código a `CoreWebView2` seguir na parte superior.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  No arquivo, copie o trecho de código a seguir para criar o método, que navega no WebView até a URL inserida na `MainWindow.xaml.cs` `ButtonGo_Click` barra de endereços.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Para criar e executar o projeto, selecione `F5` .  Digite uma nova URL na barra de endereços e escolha **Ir.**  Por exemplo, digite `https://www.bing.com`.  Certifique-se de que o controle WebView2 navegue até a URL.  
    
    > [!NOTE]
    > Certifique-se de que uma URL completa seja inserida na barra de endereços.  Um `ArgumentException` é lançado se a URL não começa com ou `http://` `https://` .  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       bing.com
    :::image-end:::
    
## Etapa 5 - Eventos de navegação  

Durante a navegação na página da Web, o controle WebView2 gera eventos.  O aplicativo que hospeda controles WebView2 escuta os eventos a seguir.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Para obter mais informações, navegue até [Eventos de Navegação.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   Eventos de navegação
:::image-end:::  

Quando ocorre um erro, os eventos a seguir são gerados e podem depender da navegação para uma página da Web de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.  

Para demonstrar como usar os eventos, registre um manipulador para `NavigationStarting` que cancele qualquer solicitação não HTTPS.  

No arquivo, modifique o construtor para corresponder ao trecho de código a seguir `MainWindow.xaml.cs` e adicione a `EnsureHttps` função.  

```csharp
public MainWindow()
{
    InitializeComponent();
    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```  

No construtor, EnsureHttps é registrado como o manipulador de eventos `NavigationStarting` no evento no controle WebView2.  

Para criar e executar o projeto, selecione `F5` .  Certifique-se de que, ao navegar para um site HTTP, o WebView permaneça inalterado.  No entanto, o WebView navega para sites HTTPS.  

## Etapa 6 - Scripts  

Você pode usar aplicativos host para inserir código JavaScript em controles WebView2 no tempo de execução.  Você pode tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado com tempo específico.  

*   Execute-o após a criação do objeto global.  
*   Execute-o antes que qualquer outro script incluído no documento HTML seja executado.  

Por exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites não HTTPS.  Modifique `EnsureHttps` a função para inserir um script no conteúdo da Web que usa o método [ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Para criar e executar o projeto, selecione `F5` .  Certifique-se de que o aplicativo exibe um alerta quando você navega para um site que não usa HTTPS.  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## Etapa 7- Comunicação entre o conteúdo do host e da Web  

O conteúdo do host e da Web pode se comunicar uns com os outros `postMessage` usando o seguinte:  

*   O conteúdo da Web em um controle WebView2 pode postar uma mensagem no host usando `window.chrome.webview.postMessage` .  O host lida com a mensagem usando qualquer `WebMessageReceived` registro no host.  
*   Hosts postam mensagens no conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .  Essas mensagens são capturadas por manipuladores adicionados `window.chrome.webview.addEventListener` a .  

O mecanismo de comunicação passa mensagens do conteúdo da Web para o host usando recursos nativos.  

Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.  

1.  No `MainWindow.xaml.cs` arquivo, atualize o construtor e crie uma `InitializeAsync` função para corresponder ao trecho de código a seguir.  A `InitializeAsync` função aguarda [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) porque a inicialização `CoreWebView2` é assíncrona.  
    
    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }
    
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  
    
1.  Depois **que CoreWebView2** for inicializado, registre um manipulador de eventos para `WebMessageReceived` responder.  Em `MainWindow.xaml.cs` , `InitializeAsync` atualize e adicione usando o trecho de `UpdateAddressBar` código a seguir.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }
    
    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  
    
1.  Para que o WebView envie e responda à mensagem da Web, depois de `CoreWebView2` inicializado, o host:  
    1.  Injeta um script no conteúdo da Web que registra um manipulador para imprimir a mensagem do host.  
    1.  Injeta um script no conteúdo da Web que posta a URL no host.  
        
    No `MainWindow.xaml.cs` arquivo, atualize `InitializeAsync` para corresponder ao trecho de código a seguir.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Para criar e executar o aplicativo, selecione `F5` .  Agora, a barra de endereços exibe o URI no controle WebView2.  Quando você navega com êxito para um novo URI, o controle WebView2 alerta o usuário do URI exibido no controle WebView2.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::

Parabéns, você criou seu primeiro aplicativo WebView2.  

## Próximas etapas  

Para continuar a saber mais sobre WebView2, navegue até os seguintes recursos.  

### Ver também  

*   Para um exemplo abrangente de recursos WebView2, navegue até [o repositório WebView2Samples][GithubMicrosoftedgeWebview2samplesMain] no GitHub.  
*   Para obter informações mais detalhadas sobre a API WebView2, navegue até a [referência de API.](/dotnet/api/microsoft.web.webview2.wpf.webview2)  
*   Para obter mais informações sobre WebView2, navegue até [Recursos de WebView2](../index.md#next-steps).  

## Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desenvolvedor do Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualStudioMain]: https://visualstudio.microsoft.com "Microsoft Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador WebView2" 