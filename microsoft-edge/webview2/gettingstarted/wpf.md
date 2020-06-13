---
description: Hospedar conteúdo da Web em seu aplicativo WPF com o controle Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 para aplicativos do WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos WPF, WPF, Edge, CoreWebView2, controle do navegador, HTML do Edge, introdução, introdução, .NET
ms.openlocfilehash: fad5e7ce7be58ea9992dffee75da0d59aed471e7
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710389"
---
# Introdução ao WebView2 no WPF (visualização)  

Neste artigo, comece a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2 (visualização)](../index.md).  Para obter mais informações sobre APIs individuais, consulte [referência de API](../reference/dotnet/0-9-515-reference-webview2.md).  

## Pré-requisitos  

Verifique se você instalou a seguinte lista de pré-requisitos antes de continuar:  

* [Microsoft Edge (Chromium) Canárias Channel](https://www.microsoftedgeinsider.com/download) instalado no Windows 10, no Windows 8,1 ou no Windows 7.  
* [Visual Studio](https://visualstudio.microsoft.com/) 2017 ou posterior.  

## Etapa 1-criar um único aplicativo de janela  

Comece com um projeto de área de trabalho básico contendo uma única janela principal.  

1.  Abra o **Visual Studio**.  
1.  Selecione **aplicativo WPF .NET Core** ou **aplicativo WPF .NET Framework**e, em seguida, selecione **Avançar**.  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Núcleo do WPF":::
             Núcleo do WPF :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Estrutura WPF":::
             Estrutura WPF :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Insira valores para **nome** e **local**do projeto.  Selecione .NET Framework 4.6.2 ou posterior ou .NET Core 3,0 ou posterior.  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Criar núcleo":::
                 Criar núcleo :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Criar estrutura":::
                 Criar estrutura :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  Selecione **criar** para criar seu projeto.  
    
## Etapa 2-instalar o SDK do WebView2  

Em seguida, adicione o SDK WebView2 ao projeto.  Para a visualização, instale o SDK do WebView2 usando NuGet.  

1.  Abra o menu de contexto no projeto \ (clique com o botão direito do mouse \) e selecione **gerenciar pacotes NuGet..**..  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       NuGet
    :::image-end:::
    
1.  Digite `Microsoft.Web.WebView2` na barra de pesquisa.  Selecione **Microsoft. Web. WebView2** nos resultados da pesquisa.  Defina a versão do pacote como **pré-lançamento**e selecione **instalar**.  
    
     ![NuGet](./media/installnuget.PNG)
    
    Você está pronto para começar a desenvolver aplicativos usando a API WebView2.  Pressione `F5` para compilar e executar o projeto.  O projeto em execução exibe uma janela vazia.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicativo vazio":::
       Aplicativo vazio
    :::image-end:::  
    
## Etapa 3-criar uma única WebView em MainWindow. XAML  

Em seguida, adicione um WebView ao seu aplicativo.  

1.  Abrir `MainWindow.xaml` .  Adicione o namespace WebView2 XAML inserindo a seguinte linha dentro da `<Window/>` marca.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Confirme se o código `MainWindow.xaml` é semelhante ao trecho de código a seguir.  
    
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
    
1.  Adicione o controle WebView2 substituindo as `<Grid>` marcas com o trecho de código a seguir.  A `Source` propriedade define o URI inicial exibido no controle WebView2.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Pressione `F5` para compilar e executar seu projeto.  Confirme se o controle WebView2 é exibido [https://www.microsoft.com](https://www.microsoft.com) .  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## Etapa 4-navegação  

Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe ao adicionar uma barra de endereços ao aplicativo.

1.  Em **MainWindow. XAML**, adicione uma barra de endereços copiando e colando o trecho de código a seguir dentro do DockPanel que contém o WebView.  
    
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
    
    Confirme se a `DockPanel` seção de `MainWindow.xaml` é semelhante ao trecho de código a seguir.  
    
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
    
1.  Abrir `MainWindow.xaml.cs` no Visual Studio.  Adicione o `CoreWebView2` namespace inserindo o trecho de código a seguir na parte superior de `MainWindow.xaml.cs` .  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  No **MainWindow.XAML.cs**, copie o trecho de código a seguir para criar o `ButtonGo_Click` método, que navega pelo WebView para a URL inserida na barra de endereços.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Pressione `F5` para compilar e executar seu projeto.  Insira uma nova URL na barra de endereços e selecione **Go (ir**).  Por exemplo, digite `https://www.bing.com` .  Confirme se o controle WebView2 navega para a URL.  
    
    > [!NOTE]
    > Certifique-se de que uma URL completa seja inserida na barra de endereços.  Uma `ArgumentException` será lançada se a URL não iniciar com `http://` ou `https://` .  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       Bing
    :::image-end:::
    
## Etapa 5-eventos de navegação  

O aplicativo que hospeda os controles WebView2 ouve os eventos a seguir que são gerados pelo controle WebView2 durante a navegação em páginas da Web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Para obter mais informações, consulte [eventos de navegação](../reference/win32/0-9-488/icorewebview2.md#navigation-events).  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   Eventos de navegação
:::image-end:::  

Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

Quando há um redirecionamento HTTP, há vários `NavigationStarting` eventos.  

Para demonstrar como usar esses eventos, comece registrando um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https.  

Em `MainWindow.xaml.cs` , modifique o Construtor conforme mostrado abaixo e adicione a `EnsureHttps` função.  

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

No construtor, EnsureHttps é registrado como o manipulador de eventos no `NavigationStarting` evento no controle WebView2.  

Pressione `F5` para compilar e executar seu projeto.  Confirme que, ao navegar para um site HTTP, a WebView **permanecerá inalterada**.  No entanto, a WebView navega para sites HTTPS.  

## Etapa 6-scripting  

Você pode usar aplicativos de host para injetar código JavaScript em controles WebView2 em tempo de execução.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a quaisquer quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado após a criação do objeto global e antes que qualquer outro script incluído no documento HTML seja executado.  

Você pode usar o script para alertar o usuário ao navegar para um site que não seja HTTPS.  Modifique a `EnsureHttps` função para que ela Insira o script no conteúdo da Web usando o método [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) .  

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

Pressione `F5` para compilar e executar seu projeto.  Confirme se o aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## Etapa 7-comunicação entre o conteúdo do host e da Web  

O conteúdo do host e da Web pode se comunicar uns com os outros usando `postMessage` o seguinte procedimento:  

*   Conteúdo da Web em um controle WebView2 pode postar uma mensagem para o host usando `window.chrome.webview.postMessage` .  O host manipula a mensagem usando qualquer registro registrado `WebMessageReceived` no host.  
*   Hospeda mensagens postadas em conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .  Essas mensagens são detectadas pelos manipuladores adicionados a `window.chrome.webview.addEventListener` .  

Esse mecanismo de comunicação permite que o conteúdo da Web passe mensagens para o host usando recursos nativos.  

Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.  

1.  No **MainWindow.XAML.cs**, atualize o construtor e crie uma `InitializeAsync` função conforme mostrado no trecho de código a seguir.  A `InitializeAsync` função aguarda [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) porque a inicialização `CoreWebView2` é assíncrona.  
    
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
    
1.  Após a inicialização do **CoreWebView2** , registre um manipulador de eventos para responder `WebMessageReceived` .  Na atualização do **MainWindow.XAML.cs** `InitializeAsync` e adicione `UpdateAddressBar` usando o trecho de código a seguir.  
    
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
    
1.  Para que o WebView envie e responda à mensagem da Web, após `CoreWebView2` a inicialização, o host:  
    
    1.  Injeta um script para o conteúdo da Web que registra um manipulador para imprimir mensagens do host.  
    1.  Injeta um script para o conteúdo da Web que envia a URL para o host.  
    
    No `MainWindow.xaml.cs` , atualize da `InitializeAsync` seguinte maneira:  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Pressione `F5` para compilar e executar o aplicativo.  Agora a barra de endereços exibe o URI na WebView e, quando você navega com êxito para um novo URI, o WebView alerta o usuário do URI exibido na WebView.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::

Parabéns, você criou seu primeiro aplicativo WebView2!  

## Próximas etapas  

*   Para obter um exemplo abrangente de recursos do WebView2, consulte [repositório do WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) no github.  
*   Para obter informações mais detalhadas sobre APIs do WebView2, consulte [referência de API](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md).  
*   Para obter mais informações sobre o WebView2, consulte [recursos do WebView2](../index.md#next-steps).  

## Entrar em contato com a equipe do Microsoft Edge WebView  

Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários!  Visite o [repositório de comentários](https://github.com/MicrosoftEdge/WebViewFeedback) da WebView da Microsoft Edge para enviar solicitações de recursos ou relatórios de erros ou Pesquisar problemas conhecidos.  
