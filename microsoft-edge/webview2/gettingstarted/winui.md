---
description: Guia de início com WebView2 para aplicativos WinUI
title: Como começar com WebView2 para aplicativos WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicativos winui, winui, edge, CoreWebView2, controle do navegador, html de borda, como começar, Como começar, .NET
ms.openlocfilehash: 8ecc40a1940bfb656e2dfdc7ab6f57effa90717d
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536265"
---
# <a name="getting-started-with-webview2-in-winui-3-preview"></a>Como começar com WebView2 no WinUI 3 (Visualização)  

Neste artigo, você pode começar a criar seu primeiro aplicativo WebView2 e saber mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Seu primeiro aplicativo WebView2 usa WinUI3.  Para obter mais informações sobre APIs individuais, navegue até [referência de API][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].  

## <a name="prerequisites"></a>Pré-requisitos  

Certifique-se de instalar a lista de pré-requisitos a seguir antes de prosseguir.  

*   [WebView2 Runtime][Webview2Installer] ou qualquer canal Microsoft Edge [(Chromium)][MicrosoftedgeinsiderDownload] não estável instalado no Windows 10 versão 1803 \(build 17134\) ou posterior.  Para obter mais informações sobre Windows 10, navegue [até Windows Atualização: Perguntas frequentes][MicrosoftSupport12373].  
    
    > [!NOTE]
    > A equipe webView recomenda o uso do canal Canary e a versão mínima necessária é 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2019, versão 16.9 Preview.  Para obter mais informações, navegue [até Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].  
    *   Inclua as seguintes cargas de trabalho ao instalar Visual Studio.  
        *   Desenvolvimento da área de trabalho do .NET \(o instalador também instala o .NET 5\)  
        *   Desenvolvimento Windows Plataforma Universal  
    *   Para criar aplicativos C++, você também deve incluir as cargas de trabalho a seguir.  
        *   Desenvolvimento de área de trabalho com C++  
        *   O componente opcional C++ \(v142\) Universal Windows Plataforma para a carga de trabalho da Plataforma Universal Windows.  Para obter mais informações, navegue até **Detalhes de** Instalação na seção Desenvolvimento da **Plataforma Universal** Windows, no painel direito.  
        
## <a name="step-0---visual-studio-settings"></a>Etapa 0 - Visual Studio configurações  

1.  Verifique se o sistema tem uma NuGet de pacote habilitada para [nuget.org][NugetHome].  Para obter mais informações, navegue [até Common NuGet configurações][NugetConsumePackagesConfiguringNugetBehavior] e [Windows Community Toolkit][WindowsCommunitytoolkit].  
1.  Baixe e instale o [pacote VSIX do WinUI 3 Preview 3.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]  O instalador adiciona os modelos de projeto winui 3 e o pacote NuGet que contém as bibliotecas winui 3 para Visual Studio 2019.  
    
    Para obter instruções sobre como adicionar o pacote Visual Studio, navegue até Localizar e `VSIX` [Usar Visual Studio Extensões][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].
    
1.  Para acessar todos os recursos de Visual Studio específicos do desenvolvedor, a opção Ativar o [Modo de Desenvolvedor.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]  
    
## <a name="step-1---create-project"></a>Etapa 1 - Criar Project  

Comece com um projeto de área de trabalho básico que contém uma única janela principal.  

1.  Em Visual Studio, escolha **Criar um novo projeto**.  
1.  No drop-down do projeto, escolha **C#,** **Windows**e **WinUI,** respectivamente.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Criar um novo projeto WinUI usando Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Criar um novo projeto WinUI usando Visual Studio
    :::image-end:::  
    
1.  Escolha **Aplicativo em Branco, Empacotado (WinUI na Área de Trabalho)**  >  **Next**.  
1.  Insira um nome de projeto.
1.  Escolha opções conforme necessário.  
1.  Escolha **Criar**.  
1.  Em **New Universal Windows Platform Project**, escolha os seguintes valores e escolha **OK**.  
    *   **Versão de**destino : **Windows 10, versão 1903 (build 18362)** ou posterior  
    *   **Versão mínima**: **Windows 10, versão 1803 (build 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="A caixa de diálogo Nova Plataforma Windows Project Universal com valores escolhidos para a versão De destino e a versão Mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       A caixa de diálogo Nova Plataforma Windows Project Universal com valores escolhidos para a versão De destino e a versão Mínima.
    :::image-end:::  
    
1.  No Explorador de Soluções, dois projetos são gerados.  
    *   **Seu nome do projeto (Área de Trabalho)**.  O projeto desktop contém o código do seu aplicativo.  O `App.xaml.cs` arquivo define uma classe que representa a instância do `Application` aplicativo.  O `MainWindow.xaml.cs` arquivo define uma classe que representa a janela principal exibida pela instância do `MainWindow` aplicativo.  As classes derivam de tipos no `Microsoft.UI.Xaml` namespace do WinUI.  
    *   **Seu nome do projeto (Pacote)**.  O projeto Package é um Windows de empacotamento de aplicativos Project configurado para criar o aplicativo em um pacote MSIX para implantação.  O projeto contém o manifesto do pacote para seu aplicativo e é o projeto de inicialização da solução por padrão.  Para obter mais informações, navegue até Configurar seu aplicativo de área de trabalho para empacotamento [MSIX no Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] e referência do esquema de manifesto do [pacote para Windows 10][UwpSchemasAppxpackageUapmanifestRoot].  
1.  No Explorador de Soluções, para exibir o código, abra o `MainWindow.xaml` arquivo.  Para executar seu projeto e exibir uma janela com um botão, selecione `F5` .  
    
## <a name="step-2---add-a-webview2-control-to-your-project"></a>Etapa 2 - Adicionar um controle WebView2 ao seu projeto  

Adicione um controle WebView2 ao seu projeto.  

1.  No `MainWindow.xaml` arquivo, para adicionar o namespace XAML WebView2, insira a seguinte linha dentro da `<Window/>` marca.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Verifique se seu código `MainWindow.xaml` é semelhante ao trecho de código a seguir.  
    
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
    
1.  No `MainWindow.xaml.cs` arquivo, comente a seguinte linha.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Para criar e executar seu projeto, selecione `F5` .  Certifique-se de que seu controle WebView2 seja [https://www.microsoft.com][|::ref1::|Main] exibido.  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="O controle WebView2 exibe microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       O controle WebView2 exibe microsoft.com  
    :::image-end:::  
    
## <a name="step-3---add-navigation-controls"></a>Etapa 3 - Adicionar controles de navegação  

Para permitir que os usuários controlem a página da Web exibida no controle WebView2, adicione uma barra de endereços ao seu aplicativo.  

1.  No `MainWindow.xaml` arquivo, copie e copie o seguinte trecho de código dentro do `<Grid>` elemento que contém o `WebView2` elemento.  
    
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
    
1.  No arquivo, copie o seguinte trecho de código para , que navega o controle WebView2 para a URL inserida `MainWindow.xaml.cs` `myButton_Click` na barra de endereços.  
    
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
    
    Para criar e executar seu projeto, selecione `F5` .  Insira uma nova URL na barra de endereços e escolha **Ir**.  Por exemplo, digite `https://www.bing.com` .  
    
    > [!NOTE]
    > Certifique-se de inserir URLs completas na barra de endereços.  `ArgumentException` exceções são lançadas se a URL não começar `http://` com ou `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       bing.com  
    :::image-end:::  
    
## <a name="step-4---navigation-events"></a>Etapa 4 - Eventos de navegação  

Os aplicativos que hospedam controles WebView2 ouvem os seguintes eventos gerados pelos controles WebView2 durante a navegação na página da Web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.  

Para obter mais informações, navegue até [Eventos de Navegação][Webviews2ConceptsNavigationEvents].  

Quando ocorrem erros, os seguintes eventos são gerados e podem navegar até uma página da Web de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
Como exemplo de como usar os eventos, registre um manipulador para que `NavigationStarting` cancele solicitações que não são HTTPS.  In `MainWindow.xaml.cs` , modify the constructor to register , and add the function so that it matches the following code `EnsureHttps` `EnsureHttps` snippet.  

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

Para criar e executar seu projeto, selecione `F5` .  Verifique se a navegação está bloqueada em sites HTTP e permitida para sites HTTPS.  

## <a name="step-5---scripting"></a>Etapa 5 - Scripting  

Você pode usar aplicativos host para injetar código JavaScript em controles WebView2 no tempo de execução.  Você pode tarefa webView para executar JavaScript arbitrário ou adicionar scripts de inicialização.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado com tempo específico.  

*   Execute-o após a criação do objeto global.  
*   Execute-o antes que qualquer outro script incluído no documento HTML seja executado.  

Como exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites que não são HTTPS.  Modifique `EnsureHttps` a função para injetar um script no conteúdo da Web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

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

Para criar e executar seu projeto, selecione `F5` .  Certifique-se de que seu aplicativo exibe um alerta quando você navega para qualquer site que não seja HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="O controle WebView2 exibe uma caixa de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   O controle WebView2 exibe uma caixa de diálogo de alerta
:::image-end:::  

Parabéns, você criou seu primeiro aplicativo WebView2.  

## <a name="next-steps"></a>Próximas etapas  

Para continuar a aprender mais sobre WebView2, navegue até os seguintes recursos.  

*   Para saber mais sobre como criar aplicativos WebView2, navegue até Práticas recomendadas de desenvolvimento [webView2.][WV2BestPractices]  
*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].  
    
    > [!NOTE]
    > O objeto WinRT CoreWebView2 pode não estar disponível com o lançamento da API WebView2.  Para entender quais APIs estão disponíveis para controles WebView2, navegue até [WebView2 Spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] para uma lista das APIs disponíveis.  
    
*   Para obter informações detalhadas sobre a API WebView2, navegue até [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

Para enviar suas solicitações ou bugs de recursos específicos do WinUI, navegue até [Problemas - microsoft/microsoft-ui-xaml][GithubMicrosoftMicrosoftUiXamlIssues] e escolha **Novo problema**.  

<!-- links -->  
[WV2BestPractices]: ../concepts/developer-guide.md "Práticas recomendadas de desenvolvimento do WebView2 | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configurações NuGet comuns | Microsoft Docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referência do esquema de manifesto do pacote para Windows 10 | Microsoft Docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Instalar sem usar a caixa de diálogo Gerenciar Extensões - Gerenciar extensões para Visual Studio | Microsoft Docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar seu ambiente de dev - Windows biblioteca de interface do usuário 3.0 Versão 1 (maio de 2020) | Microsoft Docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Windows Community Toolkit documentação | Microsoft Docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar seu aplicativo de área de trabalho para empacotamento MSIX Visual Studio | Microsoft Docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar seu dispositivo para desenvolvimento | Microsoft Docs"  

[GithubMicrosoftMicrosoftUiXamlIssues]: https://github.com/microsoft/microsoft-ui-xaml/issues "Problemas - microsoft/microsoft-ui-xaml | GitHub"  
[GithubMicrosoftMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec - microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Atualização: perguntas frequentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[NugetHome]: https://nuget.org "Home | NuGet Galeria"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Baixar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modelos do WinUI 3 Project | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador WebView2" 
