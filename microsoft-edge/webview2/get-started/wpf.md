---
description: Guia de início com WebView2 para aplicativos WPF
title: Começar com WebView2 para aplicativos WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicativos wpf, wpf, borda, CoreWebView2, controle do navegador, html de borda, get started, Get Started, .NET
ms.openlocfilehash: e7ddb3977d34e8150a10354e638226bcf96d610d
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535782"
---
# <a name="get-started-with-webview2-in-wpf"></a>Começar com WebView2 no WPF

Neste artigo, você pode começar a criar seu primeiro aplicativo WebView2 e saber mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obter mais informações sobre APIs individuais, navegue até [referência de API][DotnetApiMicrosoftWebWebview2Wpf].  

## <a name="prerequisites"></a>Pré-requisitos  

Certifique-se de instalar a lista de pré-requisitos a seguir antes de prosseguir.  

*   [WebView2 Runtime][Webview2Installer] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no sistema operacional com suporte \(atualmente Windows 10, Windows 8.1 e Windows 7\).  
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 ou posterior.  
    
## <a name="step-1---create-a-single-window-app"></a>Etapa 1 - Criar um aplicativo de janela única  

Comece com um projeto de área de trabalho básico que contém uma única janela principal.  

1.  Em Visual Studio, escolha **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-wpf-core.png" alt-text="Núcleo WPF":::
             Núcleo WPF :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-wpf-fw.png" alt-text="Estrutura WPF":::
             Estrutura WPF :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Insira valores para **Nome do Projeto e** **Local.**  Escolha **.NET Framework 4.6.2** ou posterior \(ou **.NET Core 3.0** ou posterior\).  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-create-core.png" alt-text="Criar núcleo":::
             Criar núcleo :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-create-fw.png" alt-text="Criar Estrutura":::
             Criar Estrutura :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Para criar seu projeto, escolha **Criar**.  
    
## <a name="step-2---install-webview2-sdk"></a>Etapa 2 - Instalar o SDK WebView2  

Use NuGet para adicionar o SDK WebView2 ao projeto.  

1.  Passe o mouse no projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Gerenciar Pacotes NuGet...**.  
    
    :::image type="complex" source="./media/wpf-getting-started-mng-nuget.png" alt-text="Gerenciar pacotes NuGet" lightbox="./media/wpf-getting-started-mng-nuget.png":::
       Gerenciar pacotes NuGet
    :::image-end:::
    
1.  Na barra de pesquisa, digite `Microsoft.Web.WebView2` > escolha **Microsoft.Web.WebView2**.  
    
    :::image type="complex" source="./media/install-nuget.png" alt-text="NuGet" lightbox="./media/install-nuget.png":::
       NuGet  
    :::image-end:::
    
    Pronto para começar a desenvolver aplicativos usando a API WebView2.  Para criar e executar o projeto, selecione `F5` .  O projeto em execução exibe uma janela vazia.  
    
    :::image type="complex" source="./media/winforms-empty-app.png" alt-text="Aplicativo vazio" lightbox="./media/winforms-empty-app.png":::
       Aplicativo vazio  
    :::image-end:::  
    
## <a name="step-3---create-a-single-webview"></a>Etapa 3 - Criar um único WebView 

Em seguida, adicione um WebView ao seu aplicativo.  

1.  No `MainWindow.xaml` arquivo, para adicionar o namespace XAML WebView2, insira a seguinte linha dentro da `<Window/>` marca.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Verifique se o código em `MainWindow.xaml` se parece com o trecho de código a seguir.  
    
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
    
    :::image type="complex" source="./media/wpf-getting-started-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## <a name="step-4---navigation"></a>Etapa 4 - Navegação  

Adicione a capacidade de permitir que os usuários alterem a URL exibida pelo controle WebView2 adicionando uma barra de endereços ao aplicativo.

1.  No arquivo, adicione uma barra de endereços copiando e colar o seguinte trecho de código dentro do que `MainWindow.xaml` `<DockPanel>` contém o WebView.  
    
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
    
1.  Em Visual Studio, no arquivo, para adicionar o namespace, insira o seguinte trecho de `MainWindow.xaml.cs` `CoreWebView2` código na parte superior.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  No arquivo, copie o seguinte trecho de código para criar o método, que navega pelo WebView para a URL inserida `MainWindow.xaml.cs` `ButtonGo_Click` na barra de endereços.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Para criar e executar o projeto, selecione `F5` .  Digite uma nova URL na barra de endereços e escolha **Ir**.  Por exemplo, digite `https://www.bing.com`.  Verifique se o controle WebView2 navega até a URL.  
    
    > [!NOTE]
    > Certifique-se de que uma URL completa seja inserida na barra de endereços.  Um `ArgumentException` é lançado se a URL não começar com ou `http://` `https://` .  
    
    :::image type="complex" source="./media/wpf-getting-started-bing.png" alt-text="Bing":::
       bing.com
    :::image-end:::
    
## <a name="step-5---navigation-events"></a>Etapa 5 - Eventos de navegação  

Durante a navegação na página da Web, o controle WebView2 gera eventos.  O aplicativo que hospeda controles WebView2 escuta os seguintes eventos.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
    
Para obter mais informações, navegue até [Eventos de Navegação][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   Eventos de navegação
:::image-end:::  

Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página da Web de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    
> [!NOTE]
> Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.  

Para demonstrar como usar os eventos, registre um manipulador para que cancele qualquer solicitação `NavigationStarting` que não seja HTTPS.  

No `MainWindow.xaml.cs` arquivo, modifique o construtor para corresponder ao trecho de código a seguir e adicione a `EnsureHttps` função.  

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

No construtor, é `EnsureHttps` registrado como o manipulador de eventos no evento no controle `NavigationStarting` WebView2.  

Para criar e executar o projeto, selecione `F5` .  Verifique se ao navegar para um site HTTP, o WebView permanece inalterado.  No entanto, o WebView navega para sites HTTPS.  

## <a name="step-6---scripting"></a>Etapa 6 - Scripting  

Você pode usar aplicativos host para injetar código JavaScript em controles WebView2 no tempo de execução.  Você pode tarefa webView para executar JavaScript arbitrário ou adicionar scripts de inicialização.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado com tempo específico.  

*   Execute-o após a criação do objeto global.  
*   Execute-o antes que qualquer outro script incluído no documento HTML seja executado.  
    
Como exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites que não são HTTPS.  Modifique `EnsureHttps` a função para injetar um script no conteúdo da Web que usa o método [ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)  

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

Para criar e executar o projeto, selecione `F5` .  Verifique se o aplicativo exibe um alerta quando você navega até um site que não usa HTTPS.  

:::image type="complex" source="./media/wpf-getting-started-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## <a name="step-7---communication-between-host-and-web-content"></a>Etapa 7 - Comunicação entre conteúdo do host e da Web  

O conteúdo do host e da Web pode se comunicar das seguintes maneiras usando `postMessage` .  

*   O conteúdo da Web em um controle WebView2 pode postar uma mensagem no host usando `window.chrome.webview.postMessage` .  O host lida com a mensagem usando qualquer `WebMessageReceived` registro no host.  
*   Hosts postam mensagens no conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .  As mensagens são capturadas por manipuladores adicionados a `window.chrome.webview.addEventListener` .  
    
O mecanismo de comunicação passa mensagens do conteúdo da Web para o host usando recursos nativos.  

Em seu projeto, quando o controle WebView2 navega até uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.  

1.  No `MainWindow.xaml.cs` arquivo, atualize o construtor e crie uma `InitializeAsync` função para corresponder ao trecho de código a seguir.  A `InitializeAsync` função aguarda [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) porque a inicialização `CoreWebView2` de é assíncrona.  
    
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
    
1.  Depois **que CoreWebView2** for inicializado, registre um manipulador de eventos para responder `WebMessageReceived` a .  In `MainWindow.xaml.cs` , update and add using the following code `InitializeAsync` `UpdateAddressBar` snippet.  
    
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
    1.  Injeta um script no conteúdo da Web que registra um manipulador para imprimir mensagem do host.  
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
    
    :::image type="complex" source="./media/wpf-getting-started-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::
    
Parabéns, você criou seu primeiro aplicativo WebView2.  

## <a name="next-steps"></a>Próximas etapas  

Para continuar a aprender mais sobre WebView2, navegue até os seguintes recursos.  

*   Para saber mais sobre como criar aplicativos WebView2, navegue até Práticas recomendadas de desenvolvimento [webView2.][WV2BestPractices]  
*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples repo][GithubMicrosoftedgeWebview2samplesMain] em GitHub.  
*   Para obter informações mais detalhadas sobre a API WebView2, navegue até [referência de API](/dotnet/api/microsoft.web.webview2.wpf.webview2).  
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2](../index.md#next-steps).  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
[WV2BestPractices]: ../concepts/developer-guide.md "Práticas recomendadas de desenvolvimento do WebView2 | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 | Microsoft Edge Desenvolvedor"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualStudioMain]: https://visualstudio.microsoft.com "Microsoft Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador WebView2" 
