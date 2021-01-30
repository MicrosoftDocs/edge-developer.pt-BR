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
# <span data-ttu-id="6ed47-104">Getting started with WebView2 in WinUI 3 (Preview)</span><span class="sxs-lookup"><span data-stu-id="6ed47-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="6ed47-105">Neste artigo, aprenda a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="6ed47-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="6ed47-106">Seu primeiro aplicativo WebView2 usa WinUI3.</span><span class="sxs-lookup"><span data-stu-id="6ed47-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="6ed47-107">Para obter mais informações sobre APIs individuais, navegue até a [referência de API.][GithubMicrosoftUiXamlSpecsWebview2]</span><span class="sxs-lookup"><span data-stu-id="6ed47-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="6ed47-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="6ed47-108">Prerequisites</span></span>  

<span data-ttu-id="6ed47-109">Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="6ed47-109">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="6ed47-110">[WebView2 Runtime][Webview2Installer] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no Windows 10 versão 1803 \(build 17134\) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6ed47-110">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="6ed47-111">Para obter mais informações sobre o Windows 10, navegue até [o Windows Update: perguntas frequentes.][MicrosoftSupport12373]</span><span class="sxs-lookup"><span data-stu-id="6ed47-111">For more information about Windows 10, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6ed47-112">A equipe WebView recomenda usar o canal Canary e a versão mínima necessária é 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="6ed47-112">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="6ed47-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, versão 16.9 Preview.</span><span class="sxs-lookup"><span data-stu-id="6ed47-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="6ed47-114">Para obter mais informações, navegue [até Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="6ed47-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    *   <span data-ttu-id="6ed47-115">Inclua as cargas de trabalho a seguir ao instalar o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6ed47-115">Include the following workloads when you install Visual Studio.</span></span>  
        *   <span data-ttu-id="6ed47-116">Desenvolvimento de área de trabalho do .NET \(o instalador também instala o .NET 5\)</span><span class="sxs-lookup"><span data-stu-id="6ed47-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
        *   <span data-ttu-id="6ed47-117">Desenvolvimento da Plataforma Universal do Windows</span><span class="sxs-lookup"><span data-stu-id="6ed47-117">Universal Windows Platform development</span></span>  
    *   <span data-ttu-id="6ed47-118">Para criar aplicativos C++, você também deve incluir as cargas de trabalho a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ed47-118">To build C++ apps, you must also include the following workloads.</span></span>  
        *   <span data-ttu-id="6ed47-119">Desenvolvimento da área de trabalho com C++</span><span class="sxs-lookup"><span data-stu-id="6ed47-119">Desktop development with C++</span></span>  
        *   <span data-ttu-id="6ed47-120">O componente opcional de ferramentas da Plataforma Universal do Windows C++ \(v142\) para a carga de trabalho da Plataforma Universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="6ed47-120">The C++ \(v142\) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="6ed47-121">Para obter mais informações, navegue até **Detalhes da** Instalação na seção de desenvolvimento da Plataforma Universal do **Windows,** no painel direito.</span><span class="sxs-lookup"><span data-stu-id="6ed47-121">For more information,  navigate to **Installation Details** under the **Universal Windows Platform development** section, on the right pane.</span></span>  
        
## <span data-ttu-id="6ed47-122">Etapa 0 - Configurações do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6ed47-122">Step 0 - Visual Studio settings</span></span>  

1.  <span data-ttu-id="6ed47-123">Verifique se o sistema tem uma fonte de pacote NuGet habilitada [para nuget.org][NugetHome].  Para obter mais informações, navegue [até Configurações Comuns do NuGet][NugetConsumePackagesConfiguringNugetBehavior] e Kit [de Ferramentas da Comunidade do Windows.][WindowsCommunitytoolkit]</span><span class="sxs-lookup"><span data-stu-id="6ed47-123">Ensure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="6ed47-124">Baixe e instale o [pacote WINUI 3 Preview 3 VSIX.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]</span><span class="sxs-lookup"><span data-stu-id="6ed47-124">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="6ed47-125">O instalador adiciona os modelos de projeto do WinUI 3 e o pacote NuGet que contém as bibliotecas do WinUI 3 ao Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="6ed47-125">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="6ed47-126">Para obter instruções sobre como adicionar o `VSIX` pacote ao Visual Studio, navegue até [Localizar e Usar extensões do Visual Studio.][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]</span><span class="sxs-lookup"><span data-stu-id="6ed47-126">For instructions on how to add the `VSIX` package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="6ed47-127">Para acessar todos os recursos específicos do Desenvolvedor do Visual Studio, a ligue o [Modo de Desenvolvedor.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]</span><span class="sxs-lookup"><span data-stu-id="6ed47-127">To access all developer-specific Visual Studio features, turn on [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment].</span></span>  
    
## <span data-ttu-id="6ed47-128">Etapa 1 - Criar Projeto</span><span class="sxs-lookup"><span data-stu-id="6ed47-128">Step 1 - Create Project</span></span>  

<span data-ttu-id="6ed47-129">Comece com um projeto de área de trabalho básico que contenha uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="6ed47-129">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="6ed47-130">No Visual Studio, escolha **Criar um novo projeto.**</span><span class="sxs-lookup"><span data-stu-id="6ed47-130">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="6ed47-131">No drop-down do projeto, escolha **C#**, **Windows**e **WinUI,** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6ed47-131">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Criar um novo projeto WinUI usando o Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="6ed47-133">Criar um novo projeto WinUI usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6ed47-133">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="6ed47-134">Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="6ed47-134">Choose **Blank App, Packaged (WinUI in Desktop)** > **Next**.</span></span>  
1.  <span data-ttu-id="6ed47-135">Insira um nome de projeto.</span><span class="sxs-lookup"><span data-stu-id="6ed47-135">Enter a project name.</span></span>
1.  <span data-ttu-id="6ed47-136">Escolha as opções conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="6ed47-136">Choose options as needed.</span></span>  
1.  <span data-ttu-id="6ed47-137">Escolha **Criar**.</span><span class="sxs-lookup"><span data-stu-id="6ed47-137">Choose **Create**.</span></span>  
1.  <span data-ttu-id="6ed47-138">Em **Novo Projeto da Plataforma Universal do Windows,** escolha os seguintes valores e escolha **OK.**</span><span class="sxs-lookup"><span data-stu-id="6ed47-138">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="6ed47-139">**Versão de**destino :  **Windows 10, versão 1903 (build 18362)** ou posterior</span><span class="sxs-lookup"><span data-stu-id="6ed47-139">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="6ed47-140">**Versão mínima**:  **Windows 10, versão 1803 (build 17134)**</span><span class="sxs-lookup"><span data-stu-id="6ed47-140">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="A caixa de diálogo Novo Projeto da Plataforma Universal do Windows com os valores escolhidos para a versão de destino e a versão mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="6ed47-142">A caixa de diálogo Novo Projeto da Plataforma Universal do Windows com os valores escolhidos para a versão de destino e a versão mínima.</span><span class="sxs-lookup"><span data-stu-id="6ed47-142">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="6ed47-143">No Explorador de Soluções, dois projetos são gerados.</span><span class="sxs-lookup"><span data-stu-id="6ed47-143">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="6ed47-144">**O nome do seu projeto (Desktop)**.</span><span class="sxs-lookup"><span data-stu-id="6ed47-144">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="6ed47-145">O projeto da área de trabalho contém o código do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed47-145">The Desktop project contains the code for your app.</span></span>  <span data-ttu-id="6ed47-146">O `App.xaml.cs` arquivo define uma classe que representa a instância do `Application` aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed47-146">The `App.xaml.cs` file defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="6ed47-147">O `MainWindow.xaml.cs` arquivo define uma classe que representa a janela principal exibida pela instância do `MainWindow` aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed47-147">The `MainWindow.xaml.cs` file defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="6ed47-148">As classes derivam de tipos no `Microsoft.UI.Xaml` namespace do WinUI.</span><span class="sxs-lookup"><span data-stu-id="6ed47-148">The classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    *   <span data-ttu-id="6ed47-149">**O nome do seu projeto (Pacote).**</span><span class="sxs-lookup"><span data-stu-id="6ed47-149">**Your project name (Package)**.</span></span>  <span data-ttu-id="6ed47-150">O projeto Package é um projeto de empacotamento de aplicativo do Windows configurado para criar o aplicativo em um pacote MSIX para implantação.</span><span class="sxs-lookup"><span data-stu-id="6ed47-150">The Package project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="6ed47-151">O projeto contém o manifesto do pacote para seu aplicativo e é o projeto de inicialização para sua solução por padrão.</span><span class="sxs-lookup"><span data-stu-id="6ed47-151">The project contains the package manifest for your app, and is the startup project for your solution by default.</span></span>  <span data-ttu-id="6ed47-152">Para obter mais informações, navegue até Configurar seu aplicativo da área de trabalho para empacotamento [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] no Visual Studio e referência de esquema de manifesto do pacote [para Windows 10.][UwpSchemasAppxpackageUapmanifestRoot]</span><span class="sxs-lookup"><span data-stu-id="6ed47-152">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>  
1.  <span data-ttu-id="6ed47-153">No Explorador de Soluções, para exibir o código, abra o `MainWindow.xaml` arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ed47-153">In the Solution Explorer, to display the code, open the `MainWindow.xaml` file.</span></span>  <span data-ttu-id="6ed47-154">Para executar seu projeto e exibir uma janela com um botão, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="6ed47-154">To run your project and display a window with a button, select `F5`.</span></span>  
    
## <span data-ttu-id="6ed47-155">Etapa 2: adicionar um controle WebView2 ao seu projeto</span><span class="sxs-lookup"><span data-stu-id="6ed47-155">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="6ed47-156">Adicione um controle WebView2 ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="6ed47-156">Add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="6ed47-157">No `MainWindow.xaml` arquivo, para adicionar o namespace XAML WebView2, insira a seguinte linha dentro da `<Window/>` marca.</span><span class="sxs-lookup"><span data-stu-id="6ed47-157">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="6ed47-158">Certifique-se de que `MainWindow.xaml` seu código seja semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ed47-158">Ensure your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="6ed47-159">Para adicionar o controle WebView2, substitua as `<StackPanel>` marcas pelo trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ed47-159">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="6ed47-160">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="6ed47-160">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="6ed47-161">No `MainWindow.xaml.cs` arquivo, comente a linha a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ed47-161">In the `MainWindow.xaml.cs` file, comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="6ed47-162">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="6ed47-162">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="6ed47-163">Verifique se o controle WebView2 é [https://www.microsoft.com][|::ref1::|Main] exibido.</span><span class="sxs-lookup"><span data-stu-id="6ed47-163">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="O controle WebView2 exibe microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="6ed47-165">O controle WebView2 exibe microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6ed47-165">WebView2 control displays microsoft.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6ed47-166">Etapa 3: adicionar controles de navegação</span><span class="sxs-lookup"><span data-stu-id="6ed47-166">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="6ed47-167">Para permitir que os usuários controlem a página da Web exibida no controle WebView2, adicione uma barra de endereços ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed47-167">To allow users to control the webpage that is displayed in your WebView2 control, add an address bar to your app.</span></span>  

1.  <span data-ttu-id="6ed47-168">No arquivo, copie e copie e copie o trecho de código a `MainWindow.xaml` seguir dentro do elemento que contém o `<Grid>` `WebView2` elemento.</span><span class="sxs-lookup"><span data-stu-id="6ed47-168">In the `MainWindow.xaml` file, copy and paste the following code snippet inside the `<Grid>` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="6ed47-169">Verifique se `<Grid>` o elemento no arquivo é semelhante ao trecho de código a `MainWindow.xaml` seguir.</span><span class="sxs-lookup"><span data-stu-id="6ed47-169">Ensure your `<Grid>` element in the `MainWindow.xaml` file is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="6ed47-170">No arquivo, copie o trecho de código a seguir para , que navega no controle WebView2 para a `MainWindow.xaml.cs` URL inserida na barra de `myButton_Click` endereços.</span><span class="sxs-lookup"><span data-stu-id="6ed47-170">In the `MainWindow.xaml.cs` file, copy the following code snippet into `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="6ed47-171">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="6ed47-171">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="6ed47-172">Insira uma nova URL na barra de endereços e escolha **Ir.**</span><span class="sxs-lookup"><span data-stu-id="6ed47-172">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="6ed47-173">Por exemplo, insira `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="6ed47-173">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6ed47-174">Certifique-se de inserir URLs completas na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="6ed47-174">Ensure you enter complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="6ed47-175">exceções são lançadas se a URL não começa com `http://` ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="6ed47-175">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="6ed47-177">bing.com</span><span class="sxs-lookup"><span data-stu-id="6ed47-177">bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6ed47-178">Etapa 4 - Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="6ed47-178">Step 4 - Navigation events</span></span>  

<span data-ttu-id="6ed47-179">Os aplicativos que hospedam controles WebView2 escutam os seguintes eventos gerados pelos controles WebView2 durante a navegação da página da Web.</span><span class="sxs-lookup"><span data-stu-id="6ed47-179">Apps that host WebView2 controls listen for the following events that are raised by WebView2 controls during webpage navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="6ed47-180">Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="6ed47-180">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="6ed47-181">Para obter mais informações, navegue até [Eventos de Navegação.][Webviews2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="6ed47-181">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="6ed47-182">Quando ocorrem erros, os eventos a seguir são gerados e podem navegar para uma página da Web de erro.</span><span class="sxs-lookup"><span data-stu-id="6ed47-182">When errors occur, the following events are raised and may navigate to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="6ed47-183">Como um exemplo de como usar os eventos, registre um manipulador para que `NavigationStarting` cancele quaisquer solicitações não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6ed47-183">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  <span data-ttu-id="6ed47-184">Em , modifique o construtor para registrar e adicione a função para que ela `MainWindow.xaml.cs` corresponde ao trecho de código a `EnsureHttps` `EnsureHttps` seguir.</span><span class="sxs-lookup"><span data-stu-id="6ed47-184">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="6ed47-185">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="6ed47-185">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="6ed47-186">Verifique se a navegação está bloqueada para sites HTTP e se é permitida para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6ed47-186">Ensure navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="6ed47-187">Etapa 5 - Scripts</span><span class="sxs-lookup"><span data-stu-id="6ed47-187">Step 5 - Scripting</span></span>  

<span data-ttu-id="6ed47-188">Você pode usar aplicativos host para inserir código JavaScript em controles WebView2 no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6ed47-188">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="6ed47-189">Você pode tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="6ed47-189">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="6ed47-190">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="6ed47-190">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="6ed47-191">O JavaScript injetado é executado com tempo específico.</span><span class="sxs-lookup"><span data-stu-id="6ed47-191">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="6ed47-192">Execute-o após a criação do objeto global.</span><span class="sxs-lookup"><span data-stu-id="6ed47-192">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="6ed47-193">Execute-o antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="6ed47-193">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="6ed47-194">Por exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6ed47-194">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="6ed47-195">Modifique `EnsureHttps` a função para injetar um script no conteúdo da Web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="6ed47-195">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="6ed47-196">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="6ed47-196">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="6ed47-197">Certifique-se de que seu aplicativo exibe um alerta quando você navega para qualquer site não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6ed47-197">Ensure your app displays an alert when you navigate to any non-HTTPS websites.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="O controle WebView2 exibe uma caixa de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="6ed47-199">O controle WebView2 exibe uma caixa de diálogo de alerta</span><span class="sxs-lookup"><span data-stu-id="6ed47-199">WebView2 control displays an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="6ed47-200">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="6ed47-200">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="6ed47-201">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="6ed47-201">Next steps</span></span>  

<span data-ttu-id="6ed47-202">Para continuar a saber mais sobre WebView2, navegue até os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="6ed47-202">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="6ed47-203">Ver também</span><span class="sxs-lookup"><span data-stu-id="6ed47-203">See also</span></span>  

*   <span data-ttu-id="6ed47-204">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="6ed47-204">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="6ed47-205">Para obter mais informações sobre WebView2, navegue até [Recursos de WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="6ed47-205">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6ed47-206">O objeto WinRT CoreWebView2 pode não estar disponível com o lançamento da API WebView2.</span><span class="sxs-lookup"><span data-stu-id="6ed47-206">The WinRT CoreWebView2 object may not be available with the release of the WebView2 API.</span></span>  <span data-ttu-id="6ed47-207">Para entender quais APIs estão disponíveis para controles WebView2, navegue até [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] para uma lista das APIs disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6ed47-207">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  
    
*   <span data-ttu-id="6ed47-208">Para obter informações detalhadas sobre a API WebView2, navegue até a especificação [WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="6ed47-208">For detailed information about the WebView2 API, navigate to [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  
    
## <span data-ttu-id="6ed47-209">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="6ed47-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
