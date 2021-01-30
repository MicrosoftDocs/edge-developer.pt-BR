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
# <span data-ttu-id="d3265-104">Getting started with WebView2 in WPF</span><span class="sxs-lookup"><span data-stu-id="d3265-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="d3265-105">Neste artigo, aprenda a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="d3265-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="d3265-106">Para obter mais informações sobre APIs individuais, navegue até a [referência de API.][DotnetApiMicrosoftWebWebview2Wpf]</span><span class="sxs-lookup"><span data-stu-id="d3265-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Wpf].</span></span>  

## <span data-ttu-id="d3265-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d3265-107">Prerequisites</span></span>  

<span data-ttu-id="d3265-108">Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="d3265-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="d3265-109">[WebView2 Runtime][Webview2Installer] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no sistema operacional suportado \(atualmente Windows 10, Windows 8.1 e Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="d3265-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
*   <span data-ttu-id="d3265-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d3265-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
## <span data-ttu-id="d3265-111">Etapa 1: criar um aplicativo de janela única</span><span class="sxs-lookup"><span data-stu-id="d3265-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="d3265-112">Comece com um projeto de área de trabalho básico que contenha uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="d3265-112">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="d3265-113">No Visual Studio, escolha **WPF .NET Core App** \(ou **WPF .NET Framework App**\) > **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="d3265-113">In Visual Studio, choose **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Núcleo WPF":::
             <span data-ttu-id="d3265-115">Núcleo WPF</span><span class="sxs-lookup"><span data-stu-id="d3265-115">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Estrutura WPF":::
             <span data-ttu-id="d3265-117">Estrutura WPF</span><span class="sxs-lookup"><span data-stu-id="d3265-117">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="d3265-118">Insira valores para **o nome do projeto** e o **local.**</span><span class="sxs-lookup"><span data-stu-id="d3265-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="d3265-119">Escolha **o .NET Framework 4.6.2** ou posterior \(ou **.NET Core 3.0** ou posterior\).</span><span class="sxs-lookup"><span data-stu-id="d3265-119">Choose **.NET Framework 4.6.2** or later \(or **.NET Core 3.0** or later\).</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Criar núcleo":::
                 <span data-ttu-id="d3265-121">Criar núcleo</span><span class="sxs-lookup"><span data-stu-id="d3265-121">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Criar Estrutura":::
                 <span data-ttu-id="d3265-123">Criar Estrutura</span><span class="sxs-lookup"><span data-stu-id="d3265-123">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="d3265-124">Para criar seu projeto, escolha **Criar**.</span><span class="sxs-lookup"><span data-stu-id="d3265-124">To create your project, choose **Create**.</span></span>  
    
## <span data-ttu-id="d3265-125">Etapa 2 - Instalar o SDK webView2</span><span class="sxs-lookup"><span data-stu-id="d3265-125">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="d3265-126">Use NuGet para adicionar o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="d3265-126">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="d3265-127">Passe o mouse sobre o projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Gerenciar Pacotes **NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="d3265-127">Hover on the projecty, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gerenciar pacotes NuGet":::
       <span data-ttu-id="d3265-129">Gerenciar pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="d3265-129">Manage NuGet packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="d3265-130">Na barra de pesquisa, digite > `Microsoft.Web.WebView2` escolha **Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="d3265-130">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="d3265-132">NuGet</span><span class="sxs-lookup"><span data-stu-id="d3265-132">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="d3265-133">Pronto para começar a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="d3265-133">Ready to start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="d3265-134">Para criar e executar o projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="d3265-134">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="d3265-135">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="d3265-135">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicativo vazio":::
       <span data-ttu-id="d3265-137">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="d3265-137">Empty app</span></span>
    :::image-end:::  
    
## <span data-ttu-id="d3265-138">Etapa 3 : Criar um único WebView em MainWindow.xaml</span><span class="sxs-lookup"><span data-stu-id="d3265-138">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="d3265-139">Em seguida, adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3265-139">Next add a WebView to your app.</span></span>  

1.  <span data-ttu-id="d3265-140">No `MainWindow.xaml` arquivo, para adicionar o namespace XAML WebView2, insira a seguinte linha dentro da `<Window/>` marca.</span><span class="sxs-lookup"><span data-stu-id="d3265-140">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="d3265-141">Certifique-se de que `MainWindow.xaml` o código se parece com o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3265-141">Ensure the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="d3265-142">Para adicionar o controle WebView2, substitua as `<Grid>` marcas pelo trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3265-142">To add the WebView2 control, replace the `<Grid>` tags with the following code snippet.</span></span>  <span data-ttu-id="d3265-143">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="d3265-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="d3265-144">Para criar e executar o projeto, selecione `F5`  Garantir que seu controle WebView2 seja [https://www.microsoft.com][|::ref1::|Main] exibido.</span><span class="sxs-lookup"><span data-stu-id="d3265-144">To build and run the project, select `F5`  Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="d3265-146">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d3265-146">Microsoft.com</span></span>
    :::image-end:::  
    
## <span data-ttu-id="d3265-147">Etapa 4 - Navegação</span><span class="sxs-lookup"><span data-stu-id="d3265-147">Step 4 - Navigation</span></span>  

<span data-ttu-id="d3265-148">Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe adicionando uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3265-148">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="d3265-149">No arquivo, adicione uma barra de endereços copiando e copiando o trecho de código a seguir dentro do que `MainWindow.xaml` `<DockPanel>` contém o WebView.</span><span class="sxs-lookup"><span data-stu-id="d3265-149">In the `MainWindow.xaml` file, add an address bar by copying and pasting the following code snippet inside the `<DockPanel>` that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="d3265-150">Verifique se `<DockPanel>` a seção do arquivo corresponde ao trecho de código a `MainWindow.xaml` seguir.</span><span class="sxs-lookup"><span data-stu-id="d3265-150">Ensure the `<DockPanel>` section of the `MainWindow.xaml` file matches the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="d3265-151">No Visual Studio, no `MainWindow.xaml.cs` arquivo, para adicionar o namespace, insira o trecho de código a `CoreWebView2` seguir na parte superior.</span><span class="sxs-lookup"><span data-stu-id="d3265-151">In Visual Studio, in the `MainWindow.xaml.cs` file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="d3265-152">No arquivo, copie o trecho de código a seguir para criar o método, que navega no WebView até a URL inserida na `MainWindow.xaml.cs` `ButtonGo_Click` barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="d3265-152">In the `MainWindow.xaml.cs`file, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="d3265-153">Para criar e executar o projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="d3265-153">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="d3265-154">Digite uma nova URL na barra de endereços e escolha **Ir.**</span><span class="sxs-lookup"><span data-stu-id="d3265-154">Type a new URL in the address bar and choose **Go**.</span></span>  <span data-ttu-id="d3265-155">Por exemplo, digite `https://www.bing.com`.</span><span class="sxs-lookup"><span data-stu-id="d3265-155">For example, type `https://www.bing.com`.</span></span>  <span data-ttu-id="d3265-156">Certifique-se de que o controle WebView2 navegue até a URL.</span><span class="sxs-lookup"><span data-stu-id="d3265-156">Ensure the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d3265-157">Certifique-se de que uma URL completa seja inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="d3265-157">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="d3265-158">Um `ArgumentException` é lançado se a URL não começa com ou `http://` `https://` .</span><span class="sxs-lookup"><span data-stu-id="d3265-158">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="d3265-160">bing.com</span><span class="sxs-lookup"><span data-stu-id="d3265-160">bing.com</span></span>
    :::image-end:::
    
## <span data-ttu-id="d3265-161">Etapa 5 - Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="d3265-161">Step 5 - Navigation events</span></span>  

<span data-ttu-id="d3265-162">Durante a navegação na página da Web, o controle WebView2 gera eventos.</span><span class="sxs-lookup"><span data-stu-id="d3265-162">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="d3265-163">O aplicativo que hospeda controles WebView2 escuta os eventos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3265-163">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="d3265-164">Para obter mais informações, navegue até [Eventos de Navegação.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="d3265-164">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   <span data-ttu-id="d3265-166">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="d3265-166">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="d3265-167">Quando ocorre um erro, os eventos a seguir são gerados e podem depender da navegação para uma página da Web de erro.</span><span class="sxs-lookup"><span data-stu-id="d3265-167">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="d3265-168">Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="d3265-168">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="d3265-169">Para demonstrar como usar os eventos, registre um manipulador para `NavigationStarting` que cancele qualquer solicitação não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d3265-169">To demonstrate how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  

<span data-ttu-id="d3265-170">No arquivo, modifique o construtor para corresponder ao trecho de código a seguir `MainWindow.xaml.cs` e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="d3265-170">In the `MainWindow.xaml.cs` file, modify the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="d3265-171">No construtor, EnsureHttps é registrado como o manipulador de eventos `NavigationStarting` no evento no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="d3265-171">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="d3265-172">Para criar e executar o projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="d3265-172">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="d3265-173">Certifique-se de que, ao navegar para um site HTTP, o WebView permaneça inalterado.</span><span class="sxs-lookup"><span data-stu-id="d3265-173">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="d3265-174">No entanto, o WebView navega para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d3265-174">However, the WebView navigates to HTTPS sites.</span></span>  

## <span data-ttu-id="d3265-175">Etapa 6 - Scripts</span><span class="sxs-lookup"><span data-stu-id="d3265-175">Step 6 - Scripting</span></span>  

<span data-ttu-id="d3265-176">Você pode usar aplicativos host para inserir código JavaScript em controles WebView2 no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d3265-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="d3265-177">Você pode tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="d3265-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="d3265-178">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="d3265-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="d3265-179">O JavaScript injetado é executado com tempo específico.</span><span class="sxs-lookup"><span data-stu-id="d3265-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="d3265-180">Execute-o após a criação do objeto global.</span><span class="sxs-lookup"><span data-stu-id="d3265-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="d3265-181">Execute-o antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="d3265-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="d3265-182">Por exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d3265-182">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="d3265-183">Modifique `EnsureHttps` a função para inserir um script no conteúdo da Web que usa o método [ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)</span><span class="sxs-lookup"><span data-stu-id="d3265-183">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="d3265-184">Para criar e executar o projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="d3265-184">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="d3265-185">Certifique-se de que o aplicativo exibe um alerta quando você navega para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d3265-185">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="d3265-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="d3265-187">HTTPS</span></span>
:::image-end:::  

## <span data-ttu-id="d3265-188">Etapa 7- Comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="d3265-188">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="d3265-189">O conteúdo do host e da Web pode se comunicar uns com os outros `postMessage` usando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d3265-189">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

*   <span data-ttu-id="d3265-190">O conteúdo da Web em um controle WebView2 pode postar uma mensagem no host usando `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="d3265-190">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="d3265-191">O host lida com a mensagem usando qualquer `WebMessageReceived` registro no host.</span><span class="sxs-lookup"><span data-stu-id="d3265-191">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="d3265-192">Hosts postam mensagens no conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="d3265-192">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="d3265-193">Essas mensagens são capturadas por manipuladores adicionados `window.chrome.webview.addEventListener` a .</span><span class="sxs-lookup"><span data-stu-id="d3265-193">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="d3265-194">O mecanismo de comunicação passa mensagens do conteúdo da Web para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="d3265-194">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="d3265-195">Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="d3265-195">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="d3265-196">No `MainWindow.xaml.cs` arquivo, atualize o construtor e crie uma `InitializeAsync` função para corresponder ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3265-196">In the `MainWindow.xaml.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="d3265-197">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) porque a inicialização `CoreWebView2` é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d3265-197">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="d3265-198">Depois **que CoreWebView2** for inicializado, registre um manipulador de eventos para `WebMessageReceived` responder.</span><span class="sxs-lookup"><span data-stu-id="d3265-198">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="d3265-199">Em `MainWindow.xaml.cs` , `InitializeAsync` atualize e adicione usando o trecho de `UpdateAddressBar` código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3265-199">In `MainWindow.xaml.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="d3265-200">Para que o WebView envie e responda à mensagem da Web, depois de `CoreWebView2` inicializado, o host:</span><span class="sxs-lookup"><span data-stu-id="d3265-200">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    1.  <span data-ttu-id="d3265-201">Injeta um script no conteúdo da Web que registra um manipulador para imprimir a mensagem do host.</span><span class="sxs-lookup"><span data-stu-id="d3265-201">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="d3265-202">Injeta um script no conteúdo da Web que posta a URL no host.</span><span class="sxs-lookup"><span data-stu-id="d3265-202">Injects a script to the web content that posts the URL to the host.</span></span>  
        
    <span data-ttu-id="d3265-203">No `MainWindow.xaml.cs` arquivo, atualize `InitializeAsync` para corresponder ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3265-203">In the `MainWindow.xaml.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="d3265-204">Para criar e executar o aplicativo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="d3265-204">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="d3265-205">Agora, a barra de endereços exibe o URI no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="d3265-205">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="d3265-206">Quando você navega com êxito para um novo URI, o controle WebView2 alerta o usuário do URI exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="d3265-206">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="d3265-208">addressBar</span><span class="sxs-lookup"><span data-stu-id="d3265-208">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="d3265-209">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="d3265-209">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="d3265-210">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d3265-210">Next steps</span></span>  

<span data-ttu-id="d3265-211">Para continuar a saber mais sobre WebView2, navegue até os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="d3265-211">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="d3265-212">Ver também</span><span class="sxs-lookup"><span data-stu-id="d3265-212">See also</span></span>  

*   <span data-ttu-id="d3265-213">Para um exemplo abrangente de recursos WebView2, navegue até [o repositório WebView2Samples][GithubMicrosoftedgeWebview2samplesMain] no GitHub.</span><span class="sxs-lookup"><span data-stu-id="d3265-213">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samplesMain] on GitHub.</span></span>  
*   <span data-ttu-id="d3265-214">Para obter informações mais detalhadas sobre a API WebView2, navegue até a [referência de API.](/dotnet/api/microsoft.web.webview2.wpf.webview2)</span><span class="sxs-lookup"><span data-stu-id="d3265-214">For more detailed information about WebView2 API, navigate to [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="d3265-215">Para obter mais informações sobre WebView2, navegue até [Recursos de WebView2](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="d3265-215">For more information about  WebView2, navigate to [WebView2 Resources](../index.md#next-steps).</span></span>  

## <span data-ttu-id="d3265-216">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="d3265-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

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