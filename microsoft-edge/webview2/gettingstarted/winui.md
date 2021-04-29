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
ms.sourcegitcommit: b51df5036642060525e03cd744b7d35726326abe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526056"
---
# <a name="getting-started-with-webview2-in-winui-3-preview"></a><span data-ttu-id="cff84-104">Como começar com WebView2 no WinUI 3 (Visualização)</span><span class="sxs-lookup"><span data-stu-id="cff84-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="cff84-105">Neste artigo, você pode começar a criar seu primeiro aplicativo WebView2 e saber mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="cff84-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="cff84-106">Seu primeiro aplicativo WebView2 usa WinUI3.</span><span class="sxs-lookup"><span data-stu-id="cff84-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="cff84-107">Para obter mais informações sobre APIs individuais, navegue até [referência de API][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="cff84-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="cff84-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="cff84-108">Prerequisites</span></span>  

<span data-ttu-id="cff84-109">Certifique-se de instalar a lista de pré-requisitos a seguir antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="cff84-109">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="cff84-110">[WebView2 Runtime][Webview2Installer] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no Windows 10 versão 1803 \(build 17134\) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cff84-110">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="cff84-111">Para obter mais informações sobre o Windows 10, navegue até [Windows Update: Perguntas frequentes][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="cff84-111">For more information about Windows 10, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cff84-112">A equipe webView recomenda o uso do canal Canary e a versão mínima necessária é 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="cff84-112">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="cff84-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, versão 16.9 Preview.</span><span class="sxs-lookup"><span data-stu-id="cff84-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="cff84-114">Para obter mais informações, navegue [até Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="cff84-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    *   <span data-ttu-id="cff84-115">Inclua as seguintes cargas de trabalho ao instalar Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cff84-115">Include the following workloads when you install Visual Studio.</span></span>  
        *   <span data-ttu-id="cff84-116">Desenvolvimento da área de trabalho do .NET \(o instalador também instala o .NET 5\)</span><span class="sxs-lookup"><span data-stu-id="cff84-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
        *   <span data-ttu-id="cff84-117">Desenvolvimento da Plataforma Universal do Windows</span><span class="sxs-lookup"><span data-stu-id="cff84-117">Universal Windows Platform development</span></span>  
    *   <span data-ttu-id="cff84-118">Para criar aplicativos C++, você também deve incluir as cargas de trabalho a seguir.</span><span class="sxs-lookup"><span data-stu-id="cff84-118">To build C++ apps, you must also include the following workloads.</span></span>  
        *   <span data-ttu-id="cff84-119">Desenvolvimento de área de trabalho com C++</span><span class="sxs-lookup"><span data-stu-id="cff84-119">Desktop development with C++</span></span>  
        *   <span data-ttu-id="cff84-120">O componente opcional C++ \(v142\) Ferramentas da Plataforma Universal do Windows para a carga de trabalho da Plataforma Universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="cff84-120">The C++ \(v142\) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="cff84-121">Para obter mais informações, navegue até **Detalhes de** Instalação na seção desenvolvimento da Plataforma Universal do **Windows,** no painel direito.</span><span class="sxs-lookup"><span data-stu-id="cff84-121">For more information,  navigate to **Installation Details** under the **Universal Windows Platform development** section, on the right pane.</span></span>  
        
## <a name="step-0---visual-studio-settings"></a><span data-ttu-id="cff84-122">Etapa 0 - Visual Studio configurações</span><span class="sxs-lookup"><span data-stu-id="cff84-122">Step 0 - Visual Studio settings</span></span>  

1.  <span data-ttu-id="cff84-123">Verifique se o sistema tem uma fonte de pacote NuGet habilitada para [nuget.org][NugetHome].  Para obter mais informações, navegue [até Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="cff84-123">Ensure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="cff84-124">Baixe e instale o [pacote VSIX do WinUI 3 Preview 3.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]</span><span class="sxs-lookup"><span data-stu-id="cff84-124">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="cff84-125">O instalador adiciona os modelos de projeto do WinUI 3 e o pacote NuGet que contém as bibliotecas do WinUI 3 para Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="cff84-125">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="cff84-126">Para obter instruções sobre como adicionar o pacote ao Visual Studio, navegue até Localizar e `VSIX` [Usar Visual Studio Extensões][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span><span class="sxs-lookup"><span data-stu-id="cff84-126">For instructions on how to add the `VSIX` package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="cff84-127">Para acessar todos os recursos de Visual Studio específicos do desenvolvedor, a opção Modo [de Desenvolvedor.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]</span><span class="sxs-lookup"><span data-stu-id="cff84-127">To access all developer-specific Visual Studio features, turn on [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment].</span></span>  
    
## <a name="step-1---create-project"></a><span data-ttu-id="cff84-128">Etapa 1 - Criar Projeto</span><span class="sxs-lookup"><span data-stu-id="cff84-128">Step 1 - Create Project</span></span>  

<span data-ttu-id="cff84-129">Comece com um projeto de área de trabalho básico que contém uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="cff84-129">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="cff84-130">Em Visual Studio, escolha **Criar um novo projeto**.</span><span class="sxs-lookup"><span data-stu-id="cff84-130">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="cff84-131">No drop-down do projeto, escolha **C#,** **Windows**e **WinUI,** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cff84-131">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Criar um novo projeto WinUI usando Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="cff84-133">Criar um novo projeto WinUI usando Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cff84-133">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="cff84-134">Escolha **Aplicativo em Branco, Empacotado (WinUI na Área de Trabalho)**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="cff84-134">Choose **Blank App, Packaged (WinUI in Desktop)** > **Next**.</span></span>  
1.  <span data-ttu-id="cff84-135">Insira um nome de projeto.</span><span class="sxs-lookup"><span data-stu-id="cff84-135">Enter a project name.</span></span>
1.  <span data-ttu-id="cff84-136">Escolha opções conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="cff84-136">Choose options as needed.</span></span>  
1.  <span data-ttu-id="cff84-137">Escolha **Criar**.</span><span class="sxs-lookup"><span data-stu-id="cff84-137">Choose **Create**.</span></span>  
1.  <span data-ttu-id="cff84-138">No **Novo Projeto da Plataforma Universal do Windows,** escolha os seguintes valores e escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="cff84-138">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="cff84-139">**Versão de**destino :  **Windows 10, versão 1903 (build 18362)** ou posterior</span><span class="sxs-lookup"><span data-stu-id="cff84-139">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="cff84-140">**Versão mínima**:  **Windows 10, versão 1803 (build 17134)**</span><span class="sxs-lookup"><span data-stu-id="cff84-140">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="A caixa de diálogo Novo Projeto da Plataforma Universal do Windows com valores escolhidos para a versão De destino e a versão Mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="cff84-142">A caixa de diálogo Novo Projeto da Plataforma Universal do Windows com valores escolhidos para a versão De destino e a versão Mínima.</span><span class="sxs-lookup"><span data-stu-id="cff84-142">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="cff84-143">No Explorador de Soluções, dois projetos são gerados.</span><span class="sxs-lookup"><span data-stu-id="cff84-143">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="cff84-144">**Seu nome do projeto (Área de Trabalho)**.</span><span class="sxs-lookup"><span data-stu-id="cff84-144">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="cff84-145">O projeto desktop contém o código do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cff84-145">The Desktop project contains the code for your app.</span></span>  <span data-ttu-id="cff84-146">O `App.xaml.cs` arquivo define uma classe que representa a instância do `Application` aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cff84-146">The `App.xaml.cs` file defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="cff84-147">O `MainWindow.xaml.cs` arquivo define uma classe que representa a janela principal exibida pela instância do `MainWindow` aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cff84-147">The `MainWindow.xaml.cs` file defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="cff84-148">As classes derivam de tipos no `Microsoft.UI.Xaml` namespace do WinUI.</span><span class="sxs-lookup"><span data-stu-id="cff84-148">The classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    *   <span data-ttu-id="cff84-149">**Seu nome do projeto (Pacote)**.</span><span class="sxs-lookup"><span data-stu-id="cff84-149">**Your project name (Package)**.</span></span>  <span data-ttu-id="cff84-150">O projeto Pacote é um Projeto de Empacotamento de Aplicativos do Windows configurado para criar o aplicativo em um pacote MSIX para implantação.</span><span class="sxs-lookup"><span data-stu-id="cff84-150">The Package project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="cff84-151">O projeto contém o manifesto do pacote para seu aplicativo e é o projeto de inicialização da solução por padrão.</span><span class="sxs-lookup"><span data-stu-id="cff84-151">The project contains the package manifest for your app, and is the startup project for your solution by default.</span></span>  <span data-ttu-id="cff84-152">Para obter mais informações, navegue até Configurar seu aplicativo de área de trabalho para empacotamento [MSIX Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] referência de esquema de manifesto de pacote [para Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="cff84-152">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>  
1.  <span data-ttu-id="cff84-153">No Explorador de Soluções, para exibir o código, abra o `MainWindow.xaml` arquivo.</span><span class="sxs-lookup"><span data-stu-id="cff84-153">In the Solution Explorer, to display the code, open the `MainWindow.xaml` file.</span></span>  <span data-ttu-id="cff84-154">Para executar seu projeto e exibir uma janela com um botão, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="cff84-154">To run your project and display a window with a button, select `F5`.</span></span>  
    
## <a name="step-2---add-a-webview2-control-to-your-project"></a><span data-ttu-id="cff84-155">Etapa 2 - Adicionar um controle WebView2 ao seu projeto</span><span class="sxs-lookup"><span data-stu-id="cff84-155">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="cff84-156">Adicione um controle WebView2 ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="cff84-156">Add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="cff84-157">No `MainWindow.xaml` arquivo, para adicionar o namespace XAML WebView2, insira a seguinte linha dentro da `<Window/>` marca.</span><span class="sxs-lookup"><span data-stu-id="cff84-157">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="cff84-158">Verifique se seu código `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="cff84-158">Ensure your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="cff84-159">Para adicionar o controle WebView2, substitua as `<StackPanel>` marcas pelo trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="cff84-159">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="cff84-160">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="cff84-160">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="cff84-161">No `MainWindow.xaml.cs` arquivo, comente a seguinte linha.</span><span class="sxs-lookup"><span data-stu-id="cff84-161">In the `MainWindow.xaml.cs` file, comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="cff84-162">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="cff84-162">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="cff84-163">Certifique-se de que seu controle WebView2 seja [https://www.microsoft.com][|::ref1::|Main] exibido.</span><span class="sxs-lookup"><span data-stu-id="cff84-163">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="O controle WebView2 exibe microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="cff84-165">O controle WebView2 exibe microsoft.com</span><span class="sxs-lookup"><span data-stu-id="cff84-165">WebView2 control displays microsoft.com</span></span>  
    :::image-end:::  
    
## <a name="step-3---add-navigation-controls"></a><span data-ttu-id="cff84-166">Etapa 3 - Adicionar controles de navegação</span><span class="sxs-lookup"><span data-stu-id="cff84-166">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="cff84-167">Para permitir que os usuários controlem a página da Web exibida no controle WebView2, adicione uma barra de endereços ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cff84-167">To allow users to control the webpage that is displayed in your WebView2 control, add an address bar to your app.</span></span>  

1.  <span data-ttu-id="cff84-168">No `MainWindow.xaml` arquivo, copie e copie o seguinte trecho de código dentro do `<Grid>` elemento que contém o `WebView2` elemento.</span><span class="sxs-lookup"><span data-stu-id="cff84-168">In the `MainWindow.xaml` file, copy and paste the following code snippet inside the `<Grid>` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="cff84-169">Verifique se `<Grid>` o elemento no arquivo é semelhante ao trecho de código a `MainWindow.xaml` seguir.</span><span class="sxs-lookup"><span data-stu-id="cff84-169">Ensure your `<Grid>` element in the `MainWindow.xaml` file is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="cff84-170">No arquivo, copie o seguinte trecho de código para , que navega o controle WebView2 para a URL inserida `MainWindow.xaml.cs` `myButton_Click` na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="cff84-170">In the `MainWindow.xaml.cs` file, copy the following code snippet into `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="cff84-171">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="cff84-171">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="cff84-172">Insira uma nova URL na barra de endereços e escolha **Ir**.</span><span class="sxs-lookup"><span data-stu-id="cff84-172">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="cff84-173">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="cff84-173">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cff84-174">Certifique-se de inserir URLs completas na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="cff84-174">Ensure you enter complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="cff84-175">exceções são lançadas se a URL não começar `http://` com ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="cff84-175">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="cff84-177">bing.com</span><span class="sxs-lookup"><span data-stu-id="cff84-177">bing.com</span></span>  
    :::image-end:::  
    
## <a name="step-4---navigation-events"></a><span data-ttu-id="cff84-178">Etapa 4 - Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="cff84-178">Step 4 - Navigation events</span></span>  

<span data-ttu-id="cff84-179">Os aplicativos que hospedam controles WebView2 ouvem os seguintes eventos gerados pelos controles WebView2 durante a navegação na página da Web.</span><span class="sxs-lookup"><span data-stu-id="cff84-179">Apps that host WebView2 controls listen for the following events that are raised by WebView2 controls during webpage navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="cff84-180">Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="cff84-180">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="cff84-181">Para obter mais informações, navegue até [Eventos de Navegação][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="cff84-181">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="cff84-182">Quando ocorrem erros, os seguintes eventos são gerados e podem navegar até uma página da Web de erro.</span><span class="sxs-lookup"><span data-stu-id="cff84-182">When errors occur, the following events are raised and may navigate to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="cff84-183">Como exemplo de como usar os eventos, registre um manipulador para que `NavigationStarting` cancele solicitações que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cff84-183">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  <span data-ttu-id="cff84-184">In `MainWindow.xaml.cs` , modify the constructor to register , and add the function so that it matches the following code `EnsureHttps` `EnsureHttps` snippet.</span><span class="sxs-lookup"><span data-stu-id="cff84-184">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="cff84-185">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="cff84-185">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="cff84-186">Verifique se a navegação está bloqueada em sites HTTP e permitida para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cff84-186">Ensure navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <a name="step-5---scripting"></a><span data-ttu-id="cff84-187">Etapa 5 - Scripting</span><span class="sxs-lookup"><span data-stu-id="cff84-187">Step 5 - Scripting</span></span>  

<span data-ttu-id="cff84-188">Você pode usar aplicativos host para injetar código JavaScript em controles WebView2 no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="cff84-188">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="cff84-189">Você pode tarefa webView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="cff84-189">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="cff84-190">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="cff84-190">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="cff84-191">O JavaScript injetado é executado com tempo específico.</span><span class="sxs-lookup"><span data-stu-id="cff84-191">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="cff84-192">Execute-o após a criação do objeto global.</span><span class="sxs-lookup"><span data-stu-id="cff84-192">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="cff84-193">Execute-o antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="cff84-193">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="cff84-194">Como exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cff84-194">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="cff84-195">Modifique `EnsureHttps` a função para injetar um script no conteúdo da Web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="cff84-195">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="cff84-196">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="cff84-196">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="cff84-197">Certifique-se de que seu aplicativo exibe um alerta quando você navega para qualquer site que não seja HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cff84-197">Ensure your app displays an alert when you navigate to any non-HTTPS websites.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="O controle WebView2 exibe uma caixa de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="cff84-199">O controle WebView2 exibe uma caixa de diálogo de alerta</span><span class="sxs-lookup"><span data-stu-id="cff84-199">WebView2 control displays an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="cff84-200">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="cff84-200">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="cff84-201">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="cff84-201">Next steps</span></span>  

<span data-ttu-id="cff84-202">Para continuar a aprender mais sobre WebView2, navegue até os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="cff84-202">To continue learning more about WebView2, navigate to the following resources.</span></span>  

*   <span data-ttu-id="cff84-203">Para saber mais sobre como criar aplicativos WebView2, navegue até Práticas recomendadas de desenvolvimento [webView2.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="cff84-203">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="cff84-204">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="cff84-204">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="cff84-205">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="cff84-205">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cff84-206">O objeto WinRT CoreWebView2 pode não estar disponível com o lançamento da API WebView2.</span><span class="sxs-lookup"><span data-stu-id="cff84-206">The WinRT CoreWebView2 object may not be available with the release of the WebView2 API.</span></span>  <span data-ttu-id="cff84-207">Para entender quais APIs estão disponíveis para controles WebView2, navegue até [WebView2 Spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] para uma lista das APIs disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cff84-207">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  
    
*   <span data-ttu-id="cff84-208">Para obter informações detalhadas sobre a API WebView2, navegue até [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="cff84-208">For detailed information about the WebView2 API, navigate to [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="cff84-209">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="cff84-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<span data-ttu-id="cff84-210">Para enviar suas solicitações ou bugs de recursos específicos do WinUI, navegue até [Problemas - microsoft/microsoft-ui-xaml][GithubMicrosoftMicrosoftUiXamlIssues] e escolha **Novo problema**.</span><span class="sxs-lookup"><span data-stu-id="cff84-210">To send your WinUI-specific feature requests or bugs, navigate to [Issues - microsoft/microsoft-ui-xaml][GithubMicrosoftMicrosoftUiXamlIssues] and choose **New issue**.</span></span>  

<!-- links -->  
[WV2BestPractices]: ../concepts/developer-guide.md "Práticas recomendadas de desenvolvimento do WebView2 | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configurações Comuns do NuGet | Microsoft Docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referência do esquema de manifesto do pacote para o Windows 10 | Microsoft Docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Instalar sem usar a caixa de diálogo Gerenciar Extensões - Gerenciar extensões para Visual Studio | Microsoft Docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar seu ambiente de dev - Windows UI Library 3.0 Preview 1 (maio de 2020) | Microsoft Docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentação Toolkit do Windows Community | Microsoft Docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar seu aplicativo de área de trabalho para empacotamento MSIX no Visual Studio | Microsoft Docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar seu dispositivo para desenvolvimento | Microsoft Docs"  

[GithubMicrosoftMicrosoftUiXamlIssues]: https://github.com/microsoft/microsoft-ui-xaml/issues "Problemas - microsoft/microsoft-ui-xaml | GitHub"  
[GithubMicrosoftMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec - microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: Perguntas frequentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[NugetHome]: https://nuget.org "Home | Galeria NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Baixar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modelos de projeto do WinUI 3 | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador WebView2" 
