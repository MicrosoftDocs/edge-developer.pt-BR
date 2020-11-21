---
description: Guia de introdução ao WebView2 para aplicativos do WinUI
title: Introdução ao WebView2 para aplicativos do WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos do WinUI, WinUI, Edge, CoreWebView2, controle do navegador, HTML do Edge, introdução, introdução, .NET
ms.openlocfilehash: a1ccffe332f71ee9d53ff267e8cca6bdbda81703
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182718"
---
# <span data-ttu-id="c67be-104">Introdução ao WebView2 no WinUI 3 (visualização)</span><span class="sxs-lookup"><span data-stu-id="c67be-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="c67be-105">Neste artigo, aprenda a criar seu primeiro aplicativo WebView2 e sobre os principais recursos de [introdução ao Microsoft Edge WebView2 (visualização)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="c67be-105">In this article, learn how to create your first WebView2 app and about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="c67be-106">Seu primeiro aplicativo WebView2 usa o WinUI3.</span><span class="sxs-lookup"><span data-stu-id="c67be-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="c67be-107">Para obter mais informações sobre APIs individuais, navegue até [Referência API][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="c67be-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="c67be-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c67be-108">Prerequisites</span></span>  

<span data-ttu-id="c67be-109">Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir com o artigo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c67be-109">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

1.  <span data-ttu-id="c67be-110">Windows 10 versão 1803 \ (Build 17134 \) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c67be-110">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="c67be-111">Para obter mais informações, navegue até [Windows Update: perguntas frequentes][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="c67be-111">For more information, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
1.  <span data-ttu-id="c67be-112">[Microsoft Edge (Chromium) Canárias Channel][MicrosoftedgeinsiderDownload] no Windows 10, no Windows 8,1 ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c67be-112">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
1.  <span data-ttu-id="c67be-113">Visual Studio 2019, versão 16,9 Preview.</span><span class="sxs-lookup"><span data-stu-id="c67be-113">Visual Studio 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="c67be-114">Para obter mais informações, acesse a [biblioteca de interface do usuário do Windows 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="c67be-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    <span data-ttu-id="c67be-115">Inclua as seguintes cargas de trabalho ao instalar o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c67be-115">Include the following workloads when you install Visual Studio.</span></span>  
    
    *   <span data-ttu-id="c67be-116">Desenvolvimento para área de trabalho .NET \ (o instalador também instala o .NET 5 \)</span><span class="sxs-lookup"><span data-stu-id="c67be-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
    *   <span data-ttu-id="c67be-117">Desenvolvimento da plataforma universal do Windows</span><span class="sxs-lookup"><span data-stu-id="c67be-117">Universal Windows Platform development</span></span>  
        
    <span data-ttu-id="c67be-118">Para criar aplicativos em C++, você também deve incluir as cargas de trabalho a seguir.</span><span class="sxs-lookup"><span data-stu-id="c67be-118">To build C++ apps, you must also include the following workloads.</span></span>  
    
    *   <span data-ttu-id="c67be-119">Desenvolvimento de área de trabalho com C++</span><span class="sxs-lookup"><span data-stu-id="c67be-119">Desktop development with C++</span></span>  
    *   <span data-ttu-id="c67be-120">O componente opcional de ferramentas da plataforma universal do Windows (v142) C++ para a carga de trabalho da plataforma universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="c67be-120">The C++ (v142) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="c67be-121">Para obter mais informações, navegue até detalhes da instalação na seção desenvolvimento da plataforma universal do Windows, no painel direito.</span><span class="sxs-lookup"><span data-stu-id="c67be-121">For more information,  navigate to Installation Details under the Universal Windows Platform development section, on the right pane.</span></span>  
        
1.  <span data-ttu-id="c67be-122">Verifique se o seu sistema tem uma fonte de pacote NuGet habilitada para [NuGet.org][NugetHome].  Para obter mais informações, navegue até [configurações comuns do NuGet][NugetConsumePackagesConfiguringNugetBehavior] e [Kit de ferramentas da Comunidade do Windows][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="c67be-122">Make sure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="c67be-123">Baixe e instale o [pacote VSIX do WinUI 3 Preview 3][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span><span class="sxs-lookup"><span data-stu-id="c67be-123">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="c67be-124">O instalador adiciona os modelos de projeto WinUI 3 e o pacote NuGet que contém as bibliotecas do WinUI 3 ao Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="c67be-124">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="c67be-125">Para obter instruções sobre como adicionar o pacote VSIX ao Visual Studio, navegue para [Localizar e usar extensões do Visual Studio][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span><span class="sxs-lookup"><span data-stu-id="c67be-125">For instructions on how to add the VSIX package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="c67be-126">Habilite o [modo de desenvolvedor][WindowsUwpGetStartedEnableYourDeviceForDevelopment] para garantir que você tenha acesso a todos os recursos do Visual Studio específicos do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="c67be-126">Enable [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all developer-specific Visual Studio features.</span></span>  
    
## <span data-ttu-id="c67be-127">Etapa 1-criar projeto</span><span class="sxs-lookup"><span data-stu-id="c67be-127">Step 1 - Create Project</span></span>  

<span data-ttu-id="c67be-128">Comece com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="c67be-128">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="c67be-129">No Visual Studio, escolha **criar um novo projeto**.</span><span class="sxs-lookup"><span data-stu-id="c67be-129">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="c67be-130">Na lista suspensa projeto, escolha **C#**, **Windows**e **WinUI** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c67be-130">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Criar um novo projeto WinUI usando o Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="c67be-132">Criar um novo projeto WinUI usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c67be-132">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="c67be-133">Escolha **aplicativo em branco, empacotado (WinUI na área de trabalho)** e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c67be-133">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="c67be-134">Insira um nome de projeto, escolha outras opções conforme necessário e, em seguida, escolha **criar**.</span><span class="sxs-lookup"><span data-stu-id="c67be-134">Enter a project name, choose other options as needed, and then choose **Create**.</span></span>  
1.  <span data-ttu-id="c67be-135">Em **novo projeto da plataforma universal do Windows**, escolha os seguintes valores e, em seguida, escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="c67be-135">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="c67be-136">**Versão de destino**:  **Windows 10, versão 1903 (Build 18362)** ou posterior</span><span class="sxs-lookup"><span data-stu-id="c67be-136">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="c67be-137">**Versão mínima**:  **Windows 10, versão 1803 (Build 17134)**</span><span class="sxs-lookup"><span data-stu-id="c67be-137">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="A nova caixa de diálogo do projeto da plataforma universal do Windows com valores escolhidos para a versão de destino e a versão mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="c67be-139">A nova caixa de diálogo do projeto da plataforma universal do Windows com valores escolhidos para a versão de destino e a versão mínima.</span><span class="sxs-lookup"><span data-stu-id="c67be-139">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="c67be-140">No Gerenciador de soluções, são gerados dois projetos.</span><span class="sxs-lookup"><span data-stu-id="c67be-140">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="c67be-141">**O nome do seu projeto (área de trabalho)**.</span><span class="sxs-lookup"><span data-stu-id="c67be-141">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="c67be-142">Este projeto contém o código para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c67be-142">This project contains the code for your app.</span></span>  <span data-ttu-id="c67be-143">**App.XAML.cs** define uma `Application` classe que representa sua instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c67be-143">**App.xaml.cs** defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="c67be-144">**MainWindow.XAML.cs** define uma `MainWindow` classe que representa a janela principal exibida pela instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c67be-144">**MainWindow.xaml.cs** defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="c67be-145">Essas classes derivam de tipos no `Microsoft.UI.Xaml` namespace de WinUI.</span><span class="sxs-lookup"><span data-stu-id="c67be-145">These classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="c67be-146">**O nome do seu projeto (pacote)**.</span><span class="sxs-lookup"><span data-stu-id="c67be-146">**Your project name (Package)**.</span></span>  <span data-ttu-id="c67be-147">Este projeto é um projeto de empacotamento de aplicativos do Windows que está configurado para compilar o aplicativo em um pacote MSIX para implantação.</span><span class="sxs-lookup"><span data-stu-id="c67be-147">This project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="c67be-148">O projeto contém o manifesto do pacote para seu aplicativo, e ele é o projeto de inicialização da solução por padrão.</span><span class="sxs-lookup"><span data-stu-id="c67be-148">The project contains the package manifest for your app, and it is the startup project for your solution by default.</span></span>  <span data-ttu-id="c67be-149">Para obter mais informações, navegue para [configurar seu aplicativo da área de trabalho para o empacotamento do MSIX no Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] e [a referência de esquema do manifesto do pacote para o Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="c67be-149">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="c67be-150">No Gerenciador de soluções, para exibir o código, abra o `MainWindow.xaml` arquivo.</span><span class="sxs-lookup"><span data-stu-id="c67be-150">In the Solution Explorer, to display the code, open `MainWindow.xaml` file.</span></span>  <span data-ttu-id="c67be-151">Selecione `F5` para executar seu projeto e mostrar uma janela com um botão.</span><span class="sxs-lookup"><span data-stu-id="c67be-151">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="c67be-152">Etapa 2-adicionar um controle WebView2 ao seu projeto</span><span class="sxs-lookup"><span data-stu-id="c67be-152">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="c67be-153">Em seguida, adicione um controle WebView2 ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="c67be-153">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="c67be-154">Abrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="c67be-154">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="c67be-155">Adicione o namespace WebView2 XAML inserindo a seguinte linha dentro da `<Window/>` marca.</span><span class="sxs-lookup"><span data-stu-id="c67be-155">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="c67be-156">Confirme se o código em `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="c67be-156">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="c67be-157">Para adicionar o controle WebView2, substitua as `<StackPanel>` marcas pelo trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="c67be-157">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="c67be-158">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="c67be-158">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="c67be-159">Abra `MainWindow.xaml.cs` e comente a seguinte linha.</span><span class="sxs-lookup"><span data-stu-id="c67be-159">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="c67be-160">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="c67be-160">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="c67be-161">Confirme se o controle WebView2 é exibido [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="c67be-161">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Um controle WebView2 exibindo o site do microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="c67be-163">Um controle WebView2 exibindo o site do microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c67be-163">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c67be-164">Etapa 3: adicionar controles de navegação</span><span class="sxs-lookup"><span data-stu-id="c67be-164">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="c67be-165">Permita que os usuários controlem a página da Web que é exibida no seu controle WebView2 adicionando uma barra de endereços ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c67be-165">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span>  

1.  <span data-ttu-id="c67be-166">Em `MainWindow.xaml` , copie e cole o trecho de código a seguir dentro do `Grid` elemento que contém o `WebView2` elemento.</span><span class="sxs-lookup"><span data-stu-id="c67be-166">In `MainWindow.xaml`, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="c67be-167">Confirme se o `Grid` elemento de `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="c67be-167">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="c67be-168">Em `MainWindow.xaml.cs` , copie o trecho de código a seguir para `myButton_Click` , que navega pelo controle WebView2 para a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="c67be-168">In `MainWindow.xaml.cs`, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="c67be-169">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="c67be-169">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="c67be-170">Insira uma nova URL na barra de endereços e, em seguida, escolha **ir**.</span><span class="sxs-lookup"><span data-stu-id="c67be-170">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="c67be-171">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="c67be-171">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c67be-172">Assegure-se de usar URLs completas na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="c67be-172">Ensure you use complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="c67be-173">exceções serão lançadas se a URL não iniciar com `http://` ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="c67be-173">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="c67be-175">Bing.com</span><span class="sxs-lookup"><span data-stu-id="c67be-175">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c67be-176">Etapa 4-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="c67be-176">Step 4 - Navigation events</span></span>  

<span data-ttu-id="c67be-177">Os aplicativos que hospedam controles WebView2 escutam os eventos a seguir que são gerados pelos controles WebView2 durante a navegação na página da Web.</span><span class="sxs-lookup"><span data-stu-id="c67be-177">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="c67be-178">Os redirecionamentos de HTTP geram vários `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="c67be-178">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="c67be-179">Para obter mais informações, navegue até [eventos de navegação][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="c67be-179">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="c67be-180">Quando ocorrem erros, os seguintes eventos são gerados e podem navegar para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="c67be-180">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="c67be-181">Como um exemplo de como usar os eventos, registre um manipulador para `NavigationStarting` que cancele qualquer solicitação que não use HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c67be-181">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any request that does not use HTTPS.</span></span>  <span data-ttu-id="c67be-182">Em `MainWindow.xaml.cs` , modifique o construtor para se registrar `EnsureHttps` e adicione a `EnsureHttps` função para que ele corresponda ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="c67be-182">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="c67be-183">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="c67be-183">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="c67be-184">Confirme se a navegação está bloqueada para sites HTTP e se é permitida para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c67be-184">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="c67be-185">Etapa 5-scripting</span><span class="sxs-lookup"><span data-stu-id="c67be-185">Step 5 - Scripting</span></span>  

<span data-ttu-id="c67be-186">Aplicativos host podem injetar código JavaScript em controles WebView2 em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c67be-186">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="c67be-187">O JavaScript injetado aplica-se a todos os novos documentos de nível superior e quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="c67be-187">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="c67be-188">O JavaScript injetado é executado com temporizador específico.</span><span class="sxs-lookup"><span data-stu-id="c67be-188">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="c67be-189">Execute-o após a criação do objeto global.</span><span class="sxs-lookup"><span data-stu-id="c67be-189">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="c67be-190">Execute-a antes de qualquer outro script incluído no documento HTML ser executado.</span><span class="sxs-lookup"><span data-stu-id="c67be-190">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="c67be-191">Como exemplo, adicione scripts enviar um alerta quando um usuário navegar para sites que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c67be-191">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="c67be-192">Modifique a `EnsureHttps` função para injetar um script no conteúdo da Web que usa o [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="c67be-192">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="c67be-193">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="c67be-193">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="c67be-194">Confirme se o seu aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c67be-194">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Controle WebView2 mostrando uma caixa de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="c67be-196">Controle WebView2 mostrando uma caixa de diálogo de alerta</span><span class="sxs-lookup"><span data-stu-id="c67be-196">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="c67be-197">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="c67be-197">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="c67be-198">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c67be-198">Next Steps</span></span>  

<span data-ttu-id="c67be-199">Atualmente, nossa equipe está desenvolvendo mais APIs do WebView2.</span><span class="sxs-lookup"><span data-stu-id="c67be-199">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="c67be-200">Para obter mais informações sobre o estado atual das APIs do WebView2, navegue até a [espec WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="c67be-200">For more information on the current state of WebView2 APIs, navigate to the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="c67be-201">O objeto WinRT CoreWebView2 pode não estar disponível no momento em que as APIs do WebView2 são entregues.</span><span class="sxs-lookup"><span data-stu-id="c67be-201">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span>  <span data-ttu-id="c67be-202">Para entender quais APIs estão disponíveis para os controles WebView2, navegue até [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] para obter uma lista das APIs que estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c67be-202">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  

<span data-ttu-id="c67be-203">Para obter mais informações sobre os recursos do WebView2, navegue até [WebView2 conceitos e guias de How-To][Webview2IndexNextSteps] e o [repositório de exemplos de WebView2][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="c67be-203">For more information about WebView2 capabilities, navigate to [WebView2 Concepts and How-To guides][Webview2IndexNextSteps] and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="c67be-204">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="c67be-204">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Documentos da Microsoft"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync (String) (Microsoft. Web. WebView2. WPF) | Documentos da Microsoft"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configurações comuns do NuGet | Documentos da Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referência do esquema do manifesto do pacote para Windows 10 | Documentos da Microsoft"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Instalar sem usar a caixa de diálogo Gerenciar extensões-gerenciar extensões do Visual Studio | Documentos da Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar seu ambiente de desenvolvimento-biblioteca de interface do usuário do Windows 3,0 Preview 1 (maio de 2020) | Documentos da Microsoft"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentação do kit de ferramentas da Comunidade do Windows | Documentos da Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar o aplicativo da área de trabalho para empacotamento do MSIX no Visual Studio | Documentos da Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilite seu dispositivo para desenvolvimento | Documentos da Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Especificação do WebView2-Microsoft/Microsoft-UI-XAML-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: perguntas frequentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  

[NugetHome]: https://nuget.org "Página inicial | Galeria do NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Baixar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modelos de projeto do WinUI 3 | Visual Studio Marketplace"  
