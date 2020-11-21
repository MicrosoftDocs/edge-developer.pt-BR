---
description: Guia de introdução com o WebView2 para aplicativos do WPF
title: Introdução ao WebView2 para aplicativos do WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos WPF, WPF, Edge, CoreWebView2, controle do navegador, HTML do Edge, introdução, introdução, .NET
ms.openlocfilehash: e928dae0aa63f15ca5fa21860c83fa5529e905df
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182371"
---
# <span data-ttu-id="0b728-104">Introdução ao WebView2 no WPF</span><span class="sxs-lookup"><span data-stu-id="0b728-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="0b728-105">Neste artigo, comece a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2](../index.md).</span><span class="sxs-lookup"><span data-stu-id="0b728-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2](../index.md).</span></span>  <span data-ttu-id="0b728-106">Para obter mais informações sobre APIs individuais, consulte [referência de API](/dotnet/api/microsoft.web.webview2.wpf).</span><span class="sxs-lookup"><span data-stu-id="0b728-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.wpf).</span></span>  

## <span data-ttu-id="0b728-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0b728-107">Prerequisites</span></span>  

<span data-ttu-id="0b728-108">Verifique se você instalou a seguinte lista de pré-requisitos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="0b728-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="0b728-109">[WebView2 Runtime][Webview2Installer] ou qualquer [canal do Canárias Microsoft Edge (Chromium) não estável](https://www.microsoftedgeinsider.com/download) instalado no Windows 10, no Windows 8,1 ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b728-109">[WebView2 Runtime][Webview2Installer] or any [non-stable Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span>  
* <span data-ttu-id="0b728-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0b728-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>  

## <span data-ttu-id="0b728-111">Etapa 1-criar um único aplicativo de janela</span><span class="sxs-lookup"><span data-stu-id="0b728-111">Step 1 - Create a single window application</span></span>  

<span data-ttu-id="0b728-112">Comece com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="0b728-112">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="0b728-113">Abra o **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="0b728-113">Open **Visual Studio**.</span></span>  
1.  <span data-ttu-id="0b728-114">Selecione **aplicativo WPF .NET Core** ou **aplicativo WPF .NET Framework**e, em seguida, selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0b728-114">Select **WPF .NET Core App** or **WPF .NET Framework App**, and then select **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Núcleo do WPF":::
             <span data-ttu-id="0b728-116">Núcleo do WPF</span><span class="sxs-lookup"><span data-stu-id="0b728-116">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Estrutura WPF":::
             <span data-ttu-id="0b728-118">Estrutura WPF</span><span class="sxs-lookup"><span data-stu-id="0b728-118">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="0b728-119">Insira valores para **nome** e **local**do projeto.</span><span class="sxs-lookup"><span data-stu-id="0b728-119">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="0b728-120">Selecione .NET Framework 4.6.2 ou posterior ou .NET Core 3,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0b728-120">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Criar núcleo":::
                 <span data-ttu-id="0b728-122">Criar núcleo</span><span class="sxs-lookup"><span data-stu-id="0b728-122">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Criar estrutura":::
                 <span data-ttu-id="0b728-124">Criar estrutura</span><span class="sxs-lookup"><span data-stu-id="0b728-124">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="0b728-125">Selecione **criar** para criar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0b728-125">Select **Create** to create your project.</span></span>  
    
## <span data-ttu-id="0b728-126">Etapa 2-instalar o SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="0b728-126">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="0b728-127">Em seguida, adicione o SDK WebView2 ao projeto usando o NuGet.</span><span class="sxs-lookup"><span data-stu-id="0b728-127">Next add the WebView2 SDK to the project using NuGet.</span></span>  

1.  <span data-ttu-id="0b728-128">Abra o menu de contexto no projeto \ (clique com o botão direito do mouse \) e selecione **gerenciar pacotes NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="0b728-128">Open the context menu on the project \(right-click\), and select **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="0b728-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="0b728-130">NuGet</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="0b728-131">Digite `Microsoft.Web.WebView2` na barra de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0b728-131">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="0b728-132">Selecione **Microsoft. Web. WebView2** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0b728-132">Select **Microsoft.Web.WebView2** from the search results.</span></span>  
   
     ![NuGet](./media/installnuget.PNG)
    
    <span data-ttu-id="0b728-134">Você está pronto para começar a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="0b728-134">You're all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="0b728-135">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="0b728-135">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="0b728-136">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="0b728-136">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicativo vazio":::
       <span data-ttu-id="0b728-138">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="0b728-138">Empty app</span></span>
    :::image-end:::  
    
## <span data-ttu-id="0b728-139">Etapa 3-criar uma única WebView em MainWindow. XAML</span><span class="sxs-lookup"><span data-stu-id="0b728-139">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="0b728-140">Em seguida, adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b728-140">Next add a WebView to your application.</span></span>  

1.  <span data-ttu-id="0b728-141">Abrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="0b728-141">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="0b728-142">Adicione o namespace WebView2 XAML inserindo a seguinte linha dentro da `<Window/>` marca.</span><span class="sxs-lookup"><span data-stu-id="0b728-142">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="0b728-143">Confirme se o código `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b728-143">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="0b728-144">Adicione o controle WebView2 substituindo as `<Grid>` marcas com o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b728-144">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="0b728-145">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0b728-145">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="0b728-146">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0b728-146">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="0b728-147">Confirme se o controle WebView2 é exibido [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="0b728-147">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="0b728-149">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0b728-149">Microsoft.com</span></span>
    :::image-end:::  
    
## <span data-ttu-id="0b728-150">Etapa 4-navegação</span><span class="sxs-lookup"><span data-stu-id="0b728-150">Step 4 - Navigation</span></span>  

<span data-ttu-id="0b728-151">Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe ao adicionar uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b728-151">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="0b728-152">Em **MainWindow. XAML**, adicione uma barra de endereços copiando e colando o trecho de código a seguir dentro do DockPanel que contém o WebView.</span><span class="sxs-lookup"><span data-stu-id="0b728-152">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="0b728-153">Confirme se a `DockPanel` seção de `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b728-153">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="0b728-154">Abrir `MainWindow.xaml.cs` no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0b728-154">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="0b728-155">Adicione o `CoreWebView2` namespace inserindo o trecho de código a seguir na parte superior de `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="0b728-155">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="0b728-156">No **MainWindow.XAML.cs**, copie o trecho de código a seguir para criar o `ButtonGo_Click` método, que navega pelo WebView para a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="0b728-156">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="0b728-157">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0b728-157">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="0b728-158">Insira uma nova URL na barra de endereços e selecione **Go (ir**).</span><span class="sxs-lookup"><span data-stu-id="0b728-158">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="0b728-159">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="0b728-159">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="0b728-160">Confirme se o controle WebView2 navega para a URL.</span><span class="sxs-lookup"><span data-stu-id="0b728-160">Confirm that the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="0b728-161">Certifique-se de que uma URL completa seja inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="0b728-161">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="0b728-162">Uma `ArgumentException` será lançada se a URL não iniciar com `http://` ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="0b728-162">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="0b728-164">Bing</span><span class="sxs-lookup"><span data-stu-id="0b728-164">Bing</span></span>
    :::image-end:::
    
## <span data-ttu-id="0b728-165">Etapa 5-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="0b728-165">Step 5 - Navigation events</span></span>  

<span data-ttu-id="0b728-166">Durante a navegação na página da Web, o controle WebView2 gera eventos.</span><span class="sxs-lookup"><span data-stu-id="0b728-166">During webpage navigation, the WebView2 control raises events.</span></span> <span data-ttu-id="0b728-167">O aplicativo que hospeda os controles de WebView2 escuta os eventos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b728-167">The application that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="0b728-168">Para obter mais informações, consulte [eventos de navegação](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="0b728-168">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   <span data-ttu-id="0b728-170">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="0b728-170">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="0b728-171">Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="0b728-171">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

<span data-ttu-id="0b728-172">Quando há um redirecionamento HTTP, há vários `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="0b728-172">When there's an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="0b728-173">Para demonstrar como usar esses eventos, comece registrando um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https.</span><span class="sxs-lookup"><span data-stu-id="0b728-173">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="0b728-174">Em `MainWindow.xaml.cs` , modifique o Construtor conforme mostrado abaixo e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="0b728-174">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="0b728-175">No construtor, EnsureHttps é registrado como o manipulador de eventos no `NavigationStarting` evento no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0b728-175">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="0b728-176">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0b728-176">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="0b728-177">Confirme que, ao navegar para um site HTTP, a WebView **permanecerá inalterada**.</span><span class="sxs-lookup"><span data-stu-id="0b728-177">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span>  <span data-ttu-id="0b728-178">No entanto, a WebView navega para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0b728-178">However, the WebView navigates to HTTPS sites.</span></span>  

## <span data-ttu-id="0b728-179">Etapa 6-scripting</span><span class="sxs-lookup"><span data-stu-id="0b728-179">Step 6 - Scripting</span></span>  

<span data-ttu-id="0b728-180">Você pode usar aplicativos de host para injetar código JavaScript em controles WebView2 em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0b728-180">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="0b728-181">O JavaScript injetado aplica-se a todos os novos documentos de nível superior e quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="0b728-181">The injected JavaScript applies to all new top-level documents and any child frames, until the JavaScript is removed.</span></span>  <span data-ttu-id="0b728-182">O JavaScript injetado é executado após a criação do objeto global e antes de qualquer script incluído no documento HTML.</span><span class="sxs-lookup"><span data-stu-id="0b728-182">The injected JavaScript is run after creation of the global object, and before any scripts included in the HTML document.</span></span>  

<span data-ttu-id="0b728-183">Você pode usar o script para alertar o usuário ao navegar para um site que não seja HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0b728-183">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="0b728-184">Modifique a `EnsureHttps` função para que ela Insira o script no conteúdo da Web usando o método [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) .</span><span class="sxs-lookup"><span data-stu-id="0b728-184">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="0b728-185">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0b728-185">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="0b728-186">Confirme se o aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0b728-186">Confirm that the application displays an alert when you navigate to a site that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="0b728-188">HTTPS</span><span class="sxs-lookup"><span data-stu-id="0b728-188">HTTPS</span></span>
:::image-end:::  

## <span data-ttu-id="0b728-189">Etapa 7-comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="0b728-189">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="0b728-190">O conteúdo do host e da Web pode se comunicar uns com os outros usando `postMessage` o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="0b728-190">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

*   <span data-ttu-id="0b728-191">Conteúdo da Web em um controle WebView2 pode postar uma mensagem para o host usando `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="0b728-191">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="0b728-192">O host manipula a mensagem usando qualquer registro registrado `WebMessageReceived` no host.</span><span class="sxs-lookup"><span data-stu-id="0b728-192">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="0b728-193">Hospeda mensagens postadas em conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="0b728-193">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="0b728-194">Essas mensagens são detectadas pelos manipuladores adicionados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="0b728-194">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="0b728-195">Esse mecanismo de comunicação permite que o conteúdo da Web passe mensagens para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="0b728-195">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="0b728-196">Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0b728-196">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="0b728-197">No **MainWindow.XAML.cs**, atualize o construtor e crie uma `InitializeAsync` função conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b728-197">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="0b728-198">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) porque a inicialização `CoreWebView2` é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0b728-198">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="0b728-199">Após a inicialização do **CoreWebView2** , registre um manipulador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="0b728-199">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="0b728-200">No **MainWindow.XAML.cs**, atualize `InitializeAsync` e adicione `UpdateAddressBar` usando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b728-200">In **MainWindow.xaml.cs**, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="0b728-201">Para que o WebView envie e responda à mensagem da Web, após `CoreWebView2` a inicialização, o host:</span><span class="sxs-lookup"><span data-stu-id="0b728-201">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    
    1.  <span data-ttu-id="0b728-202">Injeta um script para o conteúdo da Web que registra um manipulador para imprimir mensagens do host.</span><span class="sxs-lookup"><span data-stu-id="0b728-202">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="0b728-203">Injeta um script para o conteúdo da Web que envia a URL para o host.</span><span class="sxs-lookup"><span data-stu-id="0b728-203">Injects a script to the web content that posts the URL to the host.</span></span>  
    
    <span data-ttu-id="0b728-204">No `MainWindow.xaml.cs` , atualize da `InitializeAsync` seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0b728-204">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="0b728-205">Pressione `F5` para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b728-205">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="0b728-206">Agora, a barra de endereços exibe o URI no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0b728-206">Now, the address bar displays the URI in the WebView2 control.</span></span> <span data-ttu-id="0b728-207">Quando você navega com êxito para um novo URI, o controle WebView2 alerta o usuário do URI que é exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0b728-207">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="0b728-209">addressBar</span><span class="sxs-lookup"><span data-stu-id="0b728-209">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="0b728-210">Parabéns, você criou seu primeiro aplicativo WebView2!</span><span class="sxs-lookup"><span data-stu-id="0b728-210">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="0b728-211">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="0b728-211">Next steps</span></span>  

*   <span data-ttu-id="0b728-212">Para obter um exemplo abrangente de recursos do WebView2, consulte [repositório do WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) no github.</span><span class="sxs-lookup"><span data-stu-id="0b728-212">For a comprehensive example of WebView2 capabilities, see [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) on GitHub.</span></span>  
*   <span data-ttu-id="0b728-213">Para obter informações mais detalhadas sobre APIs do WebView2, consulte [referência de API](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span><span class="sxs-lookup"><span data-stu-id="0b728-213">For more detailed information about WebView2 APIs, see [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="0b728-214">Para obter mais informações sobre o WebView2, consulte [recursos do WebView2](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="0b728-214">For more information about  WebView2, see [WebView2 Resources](../index.md#next-steps).</span></span>  

## <span data-ttu-id="0b728-215">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="0b728-215">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador do WebView2" 
