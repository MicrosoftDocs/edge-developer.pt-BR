---
description: Guia de iniciação com WebView2 para aplicativos WinUI
title: Getting started with WebView2 for WinUI apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicativos winui, winui, edge, CoreWebView2, controle de navegador, html de borda, iniciando, Getting Started, .NET
ms.openlocfilehash: 5188a735eaf635c3b3bc0eead6f4ee4f3a83f1c4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306149"
---
# Getting started with WebView2 in WinUI 3 (Preview)  

Neste artigo, aprenda a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Seu primeiro aplicativo WebView2 usa WinUI3.  Para obter mais informações sobre APIs individuais, navegue até a [referência de API.][GithubMicrosoftUiXamlSpecsWebview2]  

## Pré-requisitos  

Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir.  

*   [WebView2 Runtime][Webview2Installer] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no Windows 10 versão 1803 \(build 17134\) ou posterior.  Para obter mais informações sobre o Windows 10, navegue até [o Windows Update: perguntas frequentes.][MicrosoftSupport12373]  
    
    > [!NOTE]
    > A equipe WebView recomenda usar o canal Canary e a versão mínima necessária é 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2019, versão 16.9 Preview.  Para obter mais informações, navegue [até Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].  
    
    *   Inclua as cargas de trabalho a seguir ao instalar o Visual Studio.  
        *   Desenvolvimento de área de trabalho do .NET \(o instalador também instala o .NET 5\)  
        *   Desenvolvimento da Plataforma Universal do Windows  
    *   Para criar aplicativos C++, você também deve incluir as cargas de trabalho a seguir.  
        *   Desenvolvimento da área de trabalho com C++  
        *   O componente opcional de ferramentas da Plataforma Universal do Windows C++ \(v142\) para a carga de trabalho da Plataforma Universal do Windows.  Para obter mais informações, navegue até **Detalhes da** Instalação na seção de desenvolvimento da Plataforma Universal do **Windows,** no painel direito.  
        
## Etapa 0 - Configurações do Visual Studio  

1.  Verifique se o sistema tem uma fonte de pacote NuGet habilitada [para nuget.org][NugetHome].  Para obter mais informações, navegue [até Configurações Comuns do NuGet][NugetConsumePackagesConfiguringNugetBehavior] e Kit [de Ferramentas da Comunidade do Windows.][WindowsCommunitytoolkit]  
1.  Baixe e instale o [pacote WINUI 3 Preview 3 VSIX.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]  O instalador adiciona os modelos de projeto do WinUI 3 e o pacote NuGet que contém as bibliotecas do WinUI 3 ao Visual Studio 2019.  
    
    Para obter instruções sobre como adicionar o `VSIX` pacote ao Visual Studio, navegue até [Localizar e Usar extensões do Visual Studio.][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]
    
1.  Para acessar todos os recursos específicos do Desenvolvedor do Visual Studio, a ligue o [Modo de Desenvolvedor.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]  
    
## Etapa 1 - Criar Projeto  

Comece com um projeto de área de trabalho básico que contenha uma única janela principal.  

1.  No Visual Studio, escolha **Criar um novo projeto.**  
1.  No drop-down do projeto, escolha **C#**, **Windows**e **WinUI,** respectivamente.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Criar um novo projeto WinUI usando o Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Criar um novo projeto WinUI usando o Visual Studio
    :::image-end:::  
    
1.  Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.  
1.  Insira um nome de projeto.
1.  Escolha as opções conforme necessário.  
1.  Escolha **Criar**.  
1.  Em **Novo Projeto da Plataforma Universal do Windows,** escolha os seguintes valores e escolha **OK.**  
    *   **Versão de**destino :  **Windows 10, versão 1903 (build 18362)** ou posterior  
    *   **Versão mínima**:  **Windows 10, versão 1803 (build 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="A caixa de diálogo Novo Projeto da Plataforma Universal do Windows com os valores escolhidos para a versão de destino e a versão mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       A caixa de diálogo Novo Projeto da Plataforma Universal do Windows com os valores escolhidos para a versão de destino e a versão mínima.
    :::image-end:::  
    
1.  No Explorador de Soluções, dois projetos são gerados.  
    *   **O nome do seu projeto (Desktop)**.  O projeto da área de trabalho contém o código do seu aplicativo.  O `App.xaml.cs` arquivo define uma classe que representa a instância do `Application` aplicativo.  O `MainWindow.xaml.cs` arquivo define uma classe que representa a janela principal exibida pela instância do `MainWindow` aplicativo.  As classes derivam de tipos no `Microsoft.UI.Xaml` namespace do WinUI.  
    *   **O nome do seu projeto (Pacote).**  O projeto Package é um projeto de empacotamento de aplicativo do Windows configurado para criar o aplicativo em um pacote MSIX para implantação.  O projeto contém o manifesto do pacote para seu aplicativo e é o projeto de inicialização para sua solução por padrão.  Para obter mais informações, navegue até Configurar seu aplicativo da área de trabalho para empacotamento [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] no Visual Studio e referência de esquema de manifesto do pacote [para Windows 10.][UwpSchemasAppxpackageUapmanifestRoot]  
1.  No Explorador de Soluções, para exibir o código, abra o `MainWindow.xaml` arquivo.  Para executar seu projeto e exibir uma janela com um botão, selecione `F5` .  
    
## Etapa 2: adicionar um controle WebView2 ao seu projeto  

Adicione um controle WebView2 ao seu projeto.  

1.  No `MainWindow.xaml` arquivo, para adicionar o namespace XAML WebView2, insira a seguinte linha dentro da `<Window/>` marca.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Certifique-se de que `MainWindow.xaml` seu código seja semelhante ao trecho de código a seguir.  
    
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
    
1.  No `MainWindow.xaml.cs` arquivo, comente a linha a seguir.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Para criar e executar seu projeto, selecione `F5` .  Verifique se o controle WebView2 é [https://www.microsoft.com][|::ref1::|Main] exibido.  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="O controle WebView2 exibe microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       O controle WebView2 exibe microsoft.com  
    :::image-end:::  
    
## Etapa 3: adicionar controles de navegação  

Para permitir que os usuários controlem a página da Web exibida no controle WebView2, adicione uma barra de endereços ao seu aplicativo.  

1.  No arquivo, copie e copie e copie o trecho de código a `MainWindow.xaml` seguir dentro do elemento que contém o `<Grid>` `WebView2` elemento.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Verifique se `<Grid>` o elemento no arquivo é semelhante ao trecho de código a `MainWindow.xaml` seguir.  
    
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
    
1.  No arquivo, copie o trecho de código a seguir para , que navega no controle WebView2 para a `MainWindow.xaml.cs` URL inserida na barra de `myButton_Click` endereços.  
    
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
    
    Para criar e executar seu projeto, selecione `F5` .  Insira uma nova URL na barra de endereços e escolha **Ir.**  Por exemplo, insira `https://www.bing.com` .  
    
    > [!NOTE]
    > Certifique-se de inserir URLs completas na barra de endereços.  `ArgumentException` exceções são lançadas se a URL não começa com `http://` ou `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       bing.com  
    :::image-end:::  
    
## Etapa 4 - Eventos de navegação  

Os aplicativos que hospedam controles WebView2 escutam os seguintes eventos gerados pelos controles WebView2 durante a navegação da página da Web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.  

Para obter mais informações, navegue até [Eventos de Navegação.][Webviews2ConceptsNavigationEvents]  

Quando ocorrem erros, os eventos a seguir são gerados e podem navegar para uma página da Web de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
Como um exemplo de como usar os eventos, registre um manipulador para que `NavigationStarting` cancele quaisquer solicitações não HTTPS.  Em , modifique o construtor para registrar e adicione a função para que ela `MainWindow.xaml.cs` corresponde ao trecho de código a `EnsureHttps` `EnsureHttps` seguir.  

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

Para criar e executar seu projeto, selecione `F5` .  Verifique se a navegação está bloqueada para sites HTTP e se é permitida para sites HTTPS.  

## Etapa 5 - Scripts  

Você pode usar aplicativos host para inserir código JavaScript em controles WebView2 no tempo de execução.  Você pode tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado com tempo específico.  

*   Execute-o após a criação do objeto global.  
*   Execute-o antes que qualquer outro script incluído no documento HTML seja executado.  

Por exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites não HTTPS.  Modifique `EnsureHttps` a função para injetar um script no conteúdo da Web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

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

Para criar e executar seu projeto, selecione `F5` .  Certifique-se de que seu aplicativo exibe um alerta quando você navega para qualquer site não HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="O controle WebView2 exibe uma caixa de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   O controle WebView2 exibe uma caixa de diálogo de alerta
:::image-end:::  

Parabéns, você criou seu primeiro aplicativo WebView2.  

## Próximas etapas  

Para continuar a saber mais sobre WebView2, navegue até os seguintes recursos.  

### Ver também  

*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Para obter mais informações sobre WebView2, navegue até [Recursos de WebView2][Webview2IndexNextSteps].  
    
    > [!NOTE]
    > O objeto WinRT CoreWebView2 pode não estar disponível com o lançamento da API WebView2.  Para entender quais APIs estão disponíveis para controles WebView2, navegue até [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] para uma lista das APIs disponíveis.  
    
*   Para obter informações detalhadas sobre a API WebView2, navegue até a especificação [WebView2][GithubMicrosoftUiXamlSpecsWebview2].  
    
## Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Introdução ao Microsoft Edge WebView2 (visualização) | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (visualização) | Microsoft Docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configurações Comuns do NuGet | Microsoft Docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referência de esquema de manifesto do pacote para o Windows 10 | Microsoft Docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Instalar sem usar a caixa de diálogo Gerenciar Extensões - Gerenciar extensões para o Visual Studio | Microsoft Docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar seu ambiente dev - Windows UI Library 3.0 Preview 1 (maio de 2020) | Microsoft Docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentação do Kit de Ferramentas da Comunidade do Windows | Microsoft Docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar seu aplicativo da área de trabalho para empacotamento MSIX no Visual Studio | Microsoft Docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar seu dispositivo para desenvolvimento | Microsoft Docs"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Especificação de WebView2 - microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: perguntas frequentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[NugetHome]: https://nuget.org "Home | Galeria NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Baixar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modelos de projeto do WinUI 3 | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador WebView2" 
