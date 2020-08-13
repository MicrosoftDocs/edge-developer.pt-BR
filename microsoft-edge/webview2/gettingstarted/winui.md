---
description: Hospedar o conteúdo da Web em seu aplicativo do WinUI com o controle Microsoft Edge WebView 2
title: Microsoft Edge WebView2 para aplicativos do WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos do WinUI, WinUI, Edge, CoreWebView2, controle do navegador, HTML do Edge, introdução, introdução, .NET
ms.openlocfilehash: 5b9bbb4578fc580ddc77680a57b481501e48cda7
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926488"
---
# <span data-ttu-id="f4471-104">Introdução ao WebView2 no WinUI3 (visualização)</span><span class="sxs-lookup"><span data-stu-id="f4471-104">Getting started with WebView2 in WinUI3 (Preview)</span></span>  

<span data-ttu-id="f4471-105">Neste artigo, comece a criar seu primeiro aplicativo WebView2 com o WinUI3 e saiba mais sobre os principais recursos da [introdução ao Microsoft Edge WebView2 (visualização)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="f4471-105">In this article, get started creating your first WebView2 app with WinUI3 and learn about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="f4471-106">Para obter mais informações sobre APIs individuais, consulte [referência de API][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="f4471-106">For more information on individual APIs, see [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="f4471-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f4471-107">Prerequisites</span></span>  

<span data-ttu-id="f4471-108">Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir com o artigo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4471-108">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

*   <span data-ttu-id="f4471-109">Windows 10 versão 1803 \ (Build 17134 \) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f4471-109">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="f4471-110">Para obter mais informações, consulte [Windows Update: perguntas frequentes][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="f4471-110">For more information, see [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
*   <span data-ttu-id="f4471-111">[Microsoft Edge (Chromium) Canárias Channel][MicrosoftedgeinsiderDownload] no Windows 10, no Windows 8,1 ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f4471-111">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
*   <span data-ttu-id="f4471-112">Visual Studio 2019, versão 16,7 Preview 1.</span><span class="sxs-lookup"><span data-stu-id="f4471-112">Visual Studio 2019, version 16.7 Preview 1.</span></span>  <span data-ttu-id="f4471-113">Para obter mais informações, consulte a [biblioteca de interface do usuário do Windows 3 Preview 2 (julho de 2020)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="f4471-113">For more information, see [Windows UI Library 3 Preview 2 (July 2020)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
*   <span data-ttu-id="f4471-114">As versões [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] e [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] do .NET 5 Preview 4.</span><span class="sxs-lookup"><span data-stu-id="f4471-114">Both the [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] and [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] versions of .NET 5 Preview 4.</span></span>  
*   <span data-ttu-id="f4471-115">Extensão de [modelos de projetos WinUI 3][VisualstudioMarketplaceWinUiprojecttemplates] para o Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="f4471-115">[WinUI 3 Project Templates][VisualstudioMarketplaceWinUiprojecttemplates] extension for Visual Studio 2019.</span></span>  
<span data-ttu-id="f4471-116">Assegure-se de [habilitar o modo de desenvolvedor][WindowsUwpGetStartedEnableYourDeviceForDevelopment] para garantir que você tenha acesso a todos os recursos do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f4471-116">Ensure you [Enable Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all Visual Studio features.</span></span>  

## <span data-ttu-id="f4471-117">Etapa 1-criar projeto</span><span class="sxs-lookup"><span data-stu-id="f4471-117">Step 1 - Create Project</span></span>  

<span data-ttu-id="f4471-118">Comece com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="f4471-118">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="f4471-119">No Visual Studio, selecione **criar um novo projeto**.</span><span class="sxs-lookup"><span data-stu-id="f4471-119">In Visual Studio, select **Create a new project**.</span></span>  
1.  <span data-ttu-id="f4471-120">Na lista suspensa projeto, selecione **C#**, **Windows**e **WinUI** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f4471-120">In the project drop-down, select **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Caixa de diálogo criação de projetos do Visual Studio para WinUI" lightbox="./media/winui-gettingstarted-selections.png":::
       <span data-ttu-id="f4471-122">Caixa de diálogo criação de projetos do Visual Studio para WinUI</span><span class="sxs-lookup"><span data-stu-id="f4471-122">Visual studio project creation dialog for WinUI</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f4471-123">Escolha **aplicativo em branco, empacotado (WinUI na área de trabalho)** e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f4471-123">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="f4471-124">Insira um nome de projeto, escolha outras opções conforme necessário e, em seguida, selecione **criar**.</span><span class="sxs-lookup"><span data-stu-id="f4471-124">Enter a project name, choose other options as needed, and then select **Create**.</span></span>  
1.  <span data-ttu-id="f4471-125">Em **novo projeto da plataforma universal do Windows**, selecione os seguintes valores e, em seguida, escolha **OK**:</span><span class="sxs-lookup"><span data-stu-id="f4471-125">In **New Universal Windows Platform Project**, select the following values, and then choose **OK**:</span></span>  
    *   <span data-ttu-id="f4471-126">Versão de destino: **Windows 10, versão 1903 (build 18362)** ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f4471-126">Target version: **Windows 10, version 1903 (build 18362)** or later.</span></span>  
    *   <span data-ttu-id="f4471-127">Versão mínima: **Windows 10, versão 1803 (build 17134)**.</span><span class="sxs-lookup"><span data-stu-id="f4471-127">Minimum version: **Windows 10, version 1803 (build 17134)**.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="A nova caixa de diálogo do projeto da plataforma universal do Windows com os valores selecionados para a versão de destino e a versão mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="f4471-129">A nova caixa de diálogo do projeto da plataforma universal do Windows com os valores selecionados para a versão de destino e a versão mínima.</span><span class="sxs-lookup"><span data-stu-id="f4471-129">The New Universal Windows Platform Project dialog with selected values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="f4471-130">No Gerenciador de soluções, são gerados dois projetos.</span><span class="sxs-lookup"><span data-stu-id="f4471-130">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="f4471-131">**O nome do seu projeto (área de trabalho)**.</span><span class="sxs-lookup"><span data-stu-id="f4471-131">**Your project name(Desktop)**.</span></span> <span data-ttu-id="f4471-132">Este projeto contém o código para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4471-132">This project contains the code for your app.</span></span>  <span data-ttu-id="f4471-133">**App.XAML.cs** define uma `Application` classe que representa sua instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4471-133">**App.xaml.cs** defines an`Application`class that represents your app instance.</span></span> <span data-ttu-id="f4471-134">**MainWindow.XAML.cs** define uma `MainWindow` classe que representa a janela principal exibida pela instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4471-134">**MainWindow.xaml.cs** defines a`MainWindow`class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="f4471-135">Essas classes derivam de tipos no `Microsoft.UI.Xaml` namespace de WinUI.</span><span class="sxs-lookup"><span data-stu-id="f4471-135">These classes derive from types in the`Microsoft.UI.Xaml`namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="f4471-136">**O nome do seu projeto (pacote)**.</span><span class="sxs-lookup"><span data-stu-id="f4471-136">**Your project name(Package)**.</span></span>  <span data-ttu-id="f4471-137">Este projeto é aWindows pacote de aplicativos Projectthat está configurado para construir o aplicativo em um pacote MSIX para implantação.</span><span class="sxs-lookup"><span data-stu-id="f4471-137">This project is aWindows Application Packaging Projectthat is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="f4471-138">O projeto contém o pacote manifestfor seu aplicativo e é o projeto de inicialização para a sua solução por padrão.</span><span class="sxs-lookup"><span data-stu-id="f4471-138">The project contains thepackage manifestfor your app, and it is the startup project for your solution by default.</span></span> <span data-ttu-id="f4471-139">Para obter mais informações, consulte [Configurar o aplicativo da área de trabalho para o empacotamento do MSIX no Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] e [a referência de esquema do manifesto do pacote para o Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="f4471-139">For more information, see [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="f4471-140">No Gerenciador de soluções, abra **MainWindow. XAML** para exibir o código.</span><span class="sxs-lookup"><span data-stu-id="f4471-140">In the Solution Explorer, open **MainWindow.xaml** to display the code.</span></span>  <span data-ttu-id="f4471-141">Selecione `F5` para executar seu projeto e mostrar uma janela com um botão.</span><span class="sxs-lookup"><span data-stu-id="f4471-141">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="f4471-142">Etapa 2-adicionar um controle WebView2 ao seu projeto</span><span class="sxs-lookup"><span data-stu-id="f4471-142">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="f4471-143">Em seguida, adicione um controle WebView2 ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="f4471-143">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="f4471-144">Abrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="f4471-144">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="f4471-145">Adicione o namespace WebView2 XAML inserindo a seguinte linha dentro da `<Window/>` marca.</span><span class="sxs-lookup"><span data-stu-id="f4471-145">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="f4471-146">Confirme se o código em `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4471-146">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="f4471-147">Para adicionar o controle WebView2, substitua as `<StackPanel>` marcas pelo trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4471-147">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="f4471-148">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="f4471-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="f4471-149">Abra `MainWindow.xaml.cs` e comente a seguinte linha.</span><span class="sxs-lookup"><span data-stu-id="f4471-149">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="f4471-150">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="f4471-150">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="f4471-151">Confirme se o controle WebView2 é exibido [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="f4471-151">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Um controle WebView2 exibindo o site do microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="f4471-153">Um controle WebView2 exibindo o site do microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f4471-153">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f4471-154">Etapa 3: adicionar controles de navegação</span><span class="sxs-lookup"><span data-stu-id="f4471-154">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="f4471-155">Permita que os usuários controlem a página da Web que é exibida no seu controle WebView2 adicionando uma barra de endereços ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4471-155">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span> 

1.  <span data-ttu-id="f4471-156">Em **MainWindow. XAML**, copie e cole o trecho de código a seguir dentro do `Grid` elemento que contém o `WebView2` elemento.</span><span class="sxs-lookup"><span data-stu-id="f4471-156">In **MainWindow.xaml**, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="f4471-157">Confirme se o `Grid` elemento de `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4471-157">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="f4471-158">No **MainWindow.XAML.cs**, copie o trecho de código a seguir para `myButton_Click` , que navega pelo controle WEBVIEW2 para a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="f4471-158">In **MainWindow.xaml.cs**, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="f4471-159">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="f4471-159">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="f4471-160">Insira uma nova URL na barra de endereços e selecione Go ( **ir**).</span><span class="sxs-lookup"><span data-stu-id="f4471-160">Enter a new URL in the address bar, and then select **Go**.</span></span>  <span data-ttu-id="f4471-161">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="f4471-161">For example, enter `https://www.bing.com`.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f4471-162">Assegure-se de usar URLs completas na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="f4471-162">Ensure you use complete URLs in the address bar.</span></span> `ArgumentException` <span data-ttu-id="f4471-163">exceções serão lançadas se a URL não iniciar com `http://` ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="f4471-163">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="f4471-165">Bing.com</span><span class="sxs-lookup"><span data-stu-id="f4471-165">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f4471-166">Etapa 4-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="f4471-166">Step 4 - Navigation events</span></span>  

<span data-ttu-id="f4471-167">Os aplicativos que hospedam controles WebView2 escutam os eventos a seguir que são gerados pelos controles WebView2 durante a navegação na página da Web.</span><span class="sxs-lookup"><span data-stu-id="f4471-167">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
> [!NOTE]
> <span data-ttu-id="f4471-168">Os redirecionamentos de HTTP geram vários `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="f4471-168">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  
<span data-ttu-id="f4471-169">Para obter mais informações, consulte [eventos de navegação][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="f4471-169">For more information, see [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="f4471-170">Quando ocorrem erros, os seguintes eventos são gerados e podem navegar para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="f4471-170">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    

<span data-ttu-id="f4471-171">Como um exemplo de como usar os eventos, registre um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https.</span><span class="sxs-lookup"><span data-stu-id="f4471-171">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span> <span data-ttu-id="f4471-172">Em `MainWindow.xaml.cs` , modifique o construtor para se registrar `EnsureHttps` e adicione a `EnsureHttps` função para que ele corresponda ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4471-172">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  


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

<span data-ttu-id="f4471-173">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="f4471-173">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="f4471-174">Confirme se a navegação está bloqueada para sites HTTP e se é permitida para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f4471-174">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="f4471-175">Etapa 5-scripting</span><span class="sxs-lookup"><span data-stu-id="f4471-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="f4471-176">Aplicativos host podem injetar código JavaScript em controles WebView2 em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f4471-176">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="f4471-177">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a quaisquer quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="f4471-177">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="f4471-178">O JavaScript injetado é executado após a criação do objeto global e antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="f4471-178">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="f4471-179">Como exemplo, adicione scripts enviar um alerta quando um usuário navegar para sites que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f4471-179">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="f4471-180">Modifique a `EnsureHttps` função para injetar um script no conteúdo da Web usando o [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="f4471-180">Modify the `EnsureHttps` function to inject a script into the web content using [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="f4471-181">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="f4471-181">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="f4471-182">Confirme se o seu aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f4471-182">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Controle WebView2 mostrando uma caixa de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="f4471-184">Controle WebView2 mostrando uma caixa de diálogo de alerta</span><span class="sxs-lookup"><span data-stu-id="f4471-184">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="f4471-185">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="f4471-185">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="f4471-186">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="f4471-186">Next Steps</span></span>  

<span data-ttu-id="f4471-187">Atualmente, nossa equipe está desenvolvendo mais APIs do WebView2.</span><span class="sxs-lookup"><span data-stu-id="f4471-187">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="f4471-188">Para obter mais informações sobre o estado atual de APIs do WebView2, consulte a [especificação WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="f4471-188">For more information on the current state of WebView2 APIs, see the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="f4471-189">O objeto WinRT CoreWebView2 pode não estar disponível no momento em que as APIs do WebView2 são entregues.</span><span class="sxs-lookup"><span data-stu-id="f4471-189">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span> <span data-ttu-id="f4471-190">Para entender quais APIs estão disponíveis para os controles WebView2, consulte [spec WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] para obter uma lista das APIs que estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f4471-190">To understand which APIs are available to WebView2 controls, see [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span> 

<span data-ttu-id="f4471-191">Para obter mais informações sobre os recursos do WebView2, consulte os [guias conceitos e instruções do WebView2][Webview2IndexNextSteps]e o [repositório de exemplos WebView2][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="f4471-191">For more information about WebView2 capabilities, see [WebView2 Concepts and How-To guides][Webview2IndexNextSteps], and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="f4471-192">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="f4471-192">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Documentos da Microsoft"  
[Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "ExecuteScriptAsync-classe Microsoft. Web. WebView2. WPF. WebView2 | Documentos da Microsoft"  

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

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe "dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceWinUiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modelos de projeto do WinUI 3"  
