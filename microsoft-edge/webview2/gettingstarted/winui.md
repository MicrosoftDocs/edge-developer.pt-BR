---
description: Guia de introdução ao WebView2 para aplicativos do WinUI
title: Introdução ao WebView2 para aplicativos do WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos do WinUI, WinUI, Edge, CoreWebView2, controle do navegador, HTML do Edge, introdução, introdução, .NET
ms.openlocfilehash: df6ee7a7391337635a63a961f62317e5b8a67334
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119091"
---
# Introdução ao WebView2 no WinUI3 (visualização)  

Neste artigo, comece a criar seu primeiro aplicativo WebView2 com o WinUI3 e saiba mais sobre os principais recursos da [introdução ao Microsoft Edge WebView2 (visualização)][Webview2Index].  Para obter mais informações sobre APIs individuais, consulte [referência de API][GithubMicrosoftUiXamlSpecsWebview2].  

## Pré-requisitos  

Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir com o artigo a seguir.  

*   Windows 10 versão 1803 \ (Build 17134 \) ou posterior.  Para obter mais informações, consulte [Windows Update: perguntas frequentes][MicrosoftSupport12373].  
*   [Microsoft Edge (Chromium) Canárias Channel][MicrosoftedgeinsiderDownload] no Windows 10, no Windows 8,1 ou no Windows 7.  
*   Visual Studio 2019, versão 16,7 Preview 1.  Para obter mais informações, consulte a [biblioteca de interface do usuário do Windows 3 Preview 2 (julho de 2020)][WindowsAppsWinui3ConfigureYourDevEnvironment].  
*   As versões [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] e [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] do .NET 5 Preview 4.  
*   Extensão de [modelos de projetos WinUI 3][VisualstudioMarketplaceWinUiprojecttemplates] para o Visual Studio 2019.  
Assegure-se de [habilitar o modo de desenvolvedor][WindowsUwpGetStartedEnableYourDeviceForDevelopment] para garantir que você tenha acesso a todos os recursos do Visual Studio.  

## Etapa 1-criar projeto  

Comece com um projeto de área de trabalho básico contendo uma única janela principal.  

1.  No Visual Studio, selecione **criar um novo projeto**.  
1.  Na lista suspensa projeto, selecione **C#**, **Windows**e **WinUI** , respectivamente.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Caixa de diálogo criação de projetos do Visual Studio para WinUI" lightbox="./media/winui-gettingstarted-selections.png":::
       Caixa de diálogo criação de projetos do Visual Studio para WinUI  
    :::image-end:::  
    
1.  Escolha **aplicativo em branco, empacotado (WinUI na área de trabalho)** e, em seguida, escolha **Avançar**.  
1.  Insira um nome de projeto, escolha outras opções conforme necessário e, em seguida, selecione **criar**.  
1.  Em **novo projeto da plataforma universal do Windows**, selecione os seguintes valores e, em seguida, escolha **OK**:  
    *   Versão de destino: **Windows 10, versão 1903 (build 18362)** ou posterior.  
    *   Versão mínima: **Windows 10, versão 1803 (build 17134)**.  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Caixa de diálogo criação de projetos do Visual Studio para WinUI" lightbox="./media/winui-gettingstarted-projecttype.png":::
       A nova caixa de diálogo do projeto da plataforma universal do Windows com os valores selecionados para a versão de destino e a versão mínima.
    :::image-end:::  
    
1.  No Gerenciador de soluções, são gerados dois projetos.  
    *   **O nome do seu projeto (área de trabalho)**. Este projeto contém o código para seu aplicativo.  **App.XAML.cs** define uma `Application` classe que representa sua instância do aplicativo. **MainWindow.XAML.cs** define uma `MainWindow` classe que representa a janela principal exibida pela instância do aplicativo.  Essas classes derivam de tipos no `Microsoft.UI.Xaml` namespace de WinUI.  
    
    *   **O nome do seu projeto (pacote)**.  Este projeto é aWindows pacote de aplicativos Projectthat está configurado para construir o aplicativo em um pacote MSIX para implantação.  O projeto contém o pacote manifestfor seu aplicativo e é o projeto de inicialização para a sua solução por padrão. Para obter mais informações, consulte [Configurar o aplicativo da área de trabalho para o empacotamento do MSIX no Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] e [a referência de esquema do manifesto do pacote para o Windows 10][UwpSchemasAppxpackageUapmanifestRoot].
    
1.  No Gerenciador de soluções, abra **MainWindow. XAML** para exibir o código.  Selecione `F5` para executar seu projeto e mostrar uma janela com um botão.  
    
## Etapa 2-adicionar um controle WebView2 ao seu projeto  

Em seguida, adicione um controle WebView2 ao seu projeto.  

1.  Abrir `MainWindow.xaml` .  Adicione o namespace WebView2 XAML inserindo a seguinte linha dentro da `<Window/>` marca.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Confirme se o código em `MainWindow.xaml` é semelhante ao trecho de código a seguir.  
    
    ```xml
    <Window
          x:Class="WinUI_Sample.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:local="using:WinUI_Sample"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          mc:Ignorable="d"
          xmlns:controls="using:Microsoft.UI.Xaml.Controls"
          >
        
          <StackPanel Orientation="Horizontal" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
          </StackPanel>
    
    </Window>
    ```  
    
1.  Para adicionar o controle WebView2, substitua as `<StackPanel>` marcas pelo trecho de código a seguir.  A `Source` propriedade define o URI inicial exibido no controle WebView2.  
    
    ```xml  
    <Grid>

        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
        
        <controls:WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  Abra `MainWindow.xaml.cs` e comente a seguinte linha.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Selecione `F5` para compilar e executar o projeto.  Confirme se o controle WebView2 é exibido [https://www.microsoft.com][|::ref1::|Main] .  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Caixa de diálogo criação de projetos do Visual Studio para WinUI" lightbox="./media/winui-gettingstarted-part3.png":::
       Um controle WebView2 exibindo o site do microsoft.com.  
    :::image-end:::  
    
## Etapa 3: adicionar controles de navegação  

Permita que os usuários controlem a página da Web que é exibida no seu controle WebView2 adicionando uma barra de endereços ao seu aplicativo. 

1.  Em **MainWindow. XAML**, copie e cole o trecho de código a seguir dentro do `Grid` elemento que contém o `WebView2` elemento.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Confirme se o `Grid` elemento de `MainWindow.xaml` é semelhante ao trecho de código a seguir.  
    
    ```xml
    <Grid>
    
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
    
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
        
        <WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  No **MainWindow.XAML.cs**, copie o trecho de código a seguir para `myButton_Click` , que navega pelo controle WEBVIEW2 para a URL inserida na barra de endereços.  
    
    ```csharp
    private void myButton_Click(object sender, RoutedEventArgs e)
    {
        try
        {
            Uri targetUri = new Uri(addressBar.Text);
            MyWebView.Source = targetUri;
        }
        catch (FormatException ex)
        {
            // Incorrect address entered.
        }
    }
    ```  
    
    Selecione `F5` para compilar e executar o projeto.  Insira uma nova URL na barra de endereços e selecione Go ( **ir**).  Por exemplo, digite `https://www.bing.com` . 
    
    > [!NOTE]
    > Assegure-se de usar URLs completas na barra de endereços. `ArgumentException` exceções serão lançadas se a URL não iniciar com `http://` ou `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Caixa de diálogo criação de projetos do Visual Studio para WinUI" lightbox="./media/winui-gettingstarted-bing.png":::
       Bing.com  
    :::image-end:::  
    
## Etapa 4-eventos de navegação  

Os aplicativos que hospedam controles WebView2 escutam os eventos a seguir que são gerados pelos controles WebView2 durante a navegação na página da Web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Os redirecionamentos de HTTP geram vários `NavigationStarting` eventos.  

Para obter mais informações, consulte [eventos de navegação][Webviews2ConceptsNavigationEvents].  

Quando ocorrem erros, os seguintes eventos são gerados e podem navegar para uma página de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
Como um exemplo de como usar os eventos, registre um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https. Em `MainWindow.xaml.cs` , modifique o construtor para se registrar `EnsureHttps` e adicione a `EnsureHttps` função para que ele corresponda ao trecho de código a seguir.  

```csharp
public MainWindow()
{
    InitializeComponent();
    MyWebView.NavigationStarting += EnsureHttps;
}

private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Selecione `F5` para compilar e executar o projeto.  Confirme se a navegação está bloqueada para sites HTTP e se é permitida para sites HTTPS.  

## Etapa 5-scripting  

Aplicativos host podem injetar código JavaScript em controles WebView2 em tempo de execução.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a quaisquer quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado após a criação do objeto global e antes que qualquer outro script incluído no documento HTML seja executado.  

Como exemplo, adicione scripts enviar um alerta quando um usuário navegar para sites que não são HTTPS.  Modifique a `EnsureHttps` função para injetar um script no conteúdo da Web usando o [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

```csharp
private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        MyWebView.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Selecione `F5` para compilar e executar o projeto.  Confirme se o seu aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Caixa de diálogo criação de projetos do Visual Studio para WinUI" lightbox="./media/winui-gettingstarted-script.png":::
   Controle WebView2 mostrando uma caixa de diálogo de alerta
:::image-end:::  

Parabéns, você criou seu primeiro aplicativo WebView2.  

## Próximas etapas  

Atualmente, nossa equipe está desenvolvendo mais APIs do WebView2.  Para obter mais informações sobre o estado atual de APIs do WebView2, consulte a [especificação WebView2][GithubMicrosoftUiXamlSpecsWebview2].  

> [!NOTE]
> O objeto WinRT CoreWebView2 pode não estar disponível no momento em que as APIs do WebView2 são entregues. Para entender quais APIs estão disponíveis para os controles WebView2, consulte [spec WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] para obter uma lista das APIs que estão disponíveis. 

Para obter mais informações sobre os recursos do WebView2, consulte [guias WebView2 conceitos e How-To][Webview2IndexNextSteps]e o [repositório de exemplos WebView2][GithubMicrosoftedgeWebview2samplesMain].  

## Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Documentos da Microsoft"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync (String) (Microsoft. Web. WebView2. WPF) | Documentos da Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referência do esquema do manifesto do pacote para Windows 10 | Documentos da Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar seu ambiente de desenvolvimento-biblioteca de interface do usuário do Windows 3,0 Preview 1 (maio de 2020) | Documentos da Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar o aplicativo da área de trabalho para empacotamento do MSIX no Visual Studio | Documentos da Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilite seu dispositivo para desenvolvimento | Documentos da Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Especificação do WebView2-Microsoft/Microsoft-UI-XAML-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: perguntas frequentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Baixar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceWinUiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modelos de projeto do WinUI 3"  
