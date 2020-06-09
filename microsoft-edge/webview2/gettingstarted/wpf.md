---
description: Hospedar conteúdo da Web em seu aplicativo WPF com o controle Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 para aplicativos do WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos WPF, WPF, Edge, CoreWebView2, controle do navegador, HTML do Edge, introdução, introdução, .NET
ms.openlocfilehash: a38af67e4ac9f7d70c698231882a6b479994fbfd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697970"
---
# <span data-ttu-id="73927-104">Introdução ao WebView2 no WPF (visualização)</span><span class="sxs-lookup"><span data-stu-id="73927-104">Getting started with WebView2 in WPF (Preview)</span></span>  

<span data-ttu-id="73927-105">Neste artigo, comece a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2 (visualização)](/microsoft-edge/hosting/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="73927-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="73927-106">Para obter mais informações sobre APIs individuais, consulte [referência de API](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="73927-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="73927-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="73927-107">Prerequisites</span></span>  

<span data-ttu-id="73927-108">Verifique se você instalou a seguinte lista de pré-requisitos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="73927-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="73927-109">[Microsoft Edge (Chromium) Canárias Channel](https://www.microsoftedgeinsider.com/download/) instalado no Windows 10, no Windows 8,1 ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="73927-109">[Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="73927-110">[Visual Studio](https://visualstudio.microsoft.com/) 2017 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="73927-110">[Visual Studio](https://visualstudio.microsoft.com/) 2017 or later.</span></span>  

## <span data-ttu-id="73927-111">Etapa 1-criar um único aplicativo de janela</span><span class="sxs-lookup"><span data-stu-id="73927-111">Step 1 - Create a single window application</span></span>

<span data-ttu-id="73927-112">Comece com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="73927-112">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="73927-113">Abra o **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="73927-113">Open **Visual Studio.**</span></span>
2. <span data-ttu-id="73927-114">Escolha **aplicativo WPF .NET Core** ou **aplicativo WPF .NET Framework**e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="73927-114">Choose **WPF .NET Core App** or **WPF .NET Framework App**, and then choose **Next**.</span></span>  

    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Núcleo do WPF":::
             <span data-ttu-id="73927-116">Núcleo do WPF</span><span class="sxs-lookup"><span data-stu-id="73927-116">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Estrutura WPF":::
             <span data-ttu-id="73927-118">Estrutura WPF</span><span class="sxs-lookup"><span data-stu-id="73927-118">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

3. <span data-ttu-id="73927-119">Insira valores para **nome** e **local**do projeto.</span><span class="sxs-lookup"><span data-stu-id="73927-119">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="73927-120">Selecione .NET Framework 4.6.2 ou posterior ou .NET Core 3,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="73927-120">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  

:::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Criar núcleo":::
             <span data-ttu-id="73927-122">Criar núcleo</span><span class="sxs-lookup"><span data-stu-id="73927-122">Create core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Criar estrutura":::
             <span data-ttu-id="73927-124">Criar estrutura</span><span class="sxs-lookup"><span data-stu-id="73927-124">Create Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

4. <span data-ttu-id="73927-125">Escolha **criar** para criar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="73927-125">Choose **Create** to create your project.</span></span>  

## <span data-ttu-id="73927-126">Etapa 2-instalar o SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="73927-126">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="73927-127">Em seguida, adicione o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="73927-127">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="73927-128">Para a visualização, instale o SDK do WebView2 usando NuGet.</span><span class="sxs-lookup"><span data-stu-id="73927-128">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="73927-129">Abra o menu de contexto no projeto \ (clique com o botão direito do mouse \) e escolha **gerenciar pacotes NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="73927-129">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="73927-131">NuGet</span><span class="sxs-lookup"><span data-stu-id="73927-131">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="73927-132">Digite `Microsoft.Web.WebView2` na barra de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="73927-132">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="73927-133">Escolha **Microsoft. Web. WebView2** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="73927-133">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="73927-134">Defina a versão do pacote como **pré-lançamento**e escolha **instalar**.</span><span class="sxs-lookup"><span data-stu-id="73927-134">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

     ![NuGet](./media/installnuget.PNG)

<span data-ttu-id="73927-136">Você está pronto para começar a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="73927-136">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="73927-137">Pressione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="73927-137">Press `F5` to build and run the project.</span></span>  <span data-ttu-id="73927-138">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="73927-138">The running project displays an empty window.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicativo vazio":::
   <span data-ttu-id="73927-140">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="73927-140">Empty app</span></span>
:::image-end:::

## <span data-ttu-id="73927-141">Etapa 3-criar uma única WebView em MainWindow. XAML</span><span class="sxs-lookup"><span data-stu-id="73927-141">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="73927-142">Em seguida, adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73927-142">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="73927-143">Abrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="73927-143">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="73927-144">Adicione o namespace WebView2 XAML inserindo a seguinte linha dentro da `<Window/>` marca.</span><span class="sxs-lookup"><span data-stu-id="73927-144">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  

    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  

    <span data-ttu-id="73927-145">Confirme se o código `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="73927-145">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  

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
        />
        <Grid>

                </Grid>
    </Window>
    ```  

2. <span data-ttu-id="73927-146">Adicione o controle WebView2 substituindo as `<Grid>` marcas com o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="73927-146">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="73927-147">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="73927-147">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  

    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  

3. <span data-ttu-id="73927-148">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="73927-148">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="73927-149">Confirme se o controle WebView2 é exibido [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="73927-149">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="73927-151">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="73927-151">Microsoft.com</span></span> :::image-end:::

## <span data-ttu-id="73927-152">Etapa 4-navegação</span><span class="sxs-lookup"><span data-stu-id="73927-152">Step 4 - Navigation</span></span>  

<span data-ttu-id="73927-153">Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe ao adicionar uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73927-153">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="73927-154">Em **MainWindow. XAML**, adicione uma barra de endereços copiando e colando o trecho de código a seguir dentro do DockPanel que contém o WebView.</span><span class="sxs-lookup"><span data-stu-id="73927-154">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  

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

<span data-ttu-id="73927-155">Confirme se a `DockPanel` seção de `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="73927-155">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  

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

2. <span data-ttu-id="73927-156">Abrir `MainWindow.xaml.cs` no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="73927-156">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="73927-157">Adicione o `CoreWebView2` namespace inserindo o trecho de código a seguir na parte superior de `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="73927-157">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

3. <span data-ttu-id="73927-158">No **MainWindow.XAML.cs**, copie o trecho de código a seguir para criar o `ButtonGo_Click` método, que navega pelo WebView para a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="73927-158">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  

    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="73927-159">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="73927-159">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="73927-160">Insira uma nova URL na barra de endereços e clique em **ir**.</span><span class="sxs-lookup"><span data-stu-id="73927-160">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="73927-161">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="73927-161">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="73927-162">Confirme se o controle WebView2 navega para a URL.</span><span class="sxs-lookup"><span data-stu-id="73927-162">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="73927-163">Certifique-se de que uma URL completa seja inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="73927-163">Make sure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="73927-164">Uma `ArgumentException` será lançada se a URL não iniciar com `http://` ou</span><span class="sxs-lookup"><span data-stu-id="73927-164">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
   <span data-ttu-id="73927-166">Bing</span><span class="sxs-lookup"><span data-stu-id="73927-166">Bing</span></span>
:::image-end:::

## <span data-ttu-id="73927-167">Etapa 5-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="73927-167">Step 5 - Navigation events</span></span>  

<span data-ttu-id="73927-168">O aplicativo que hospeda os controles WebView2 ouve os eventos a seguir que são gerados pelo controle WebView2 durante a navegação em páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="73927-168">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="73927-169">Para obter mais informações, consulte [eventos de navegação](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="73927-169">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   <span data-ttu-id="73927-171">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="73927-171">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="73927-172">Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="73927-172">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="73927-173">Quando há um redirecionamento HTTP, há vários `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="73927-173">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="73927-174">Para demonstrar como usar esses eventos, comece registrando um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https.</span><span class="sxs-lookup"><span data-stu-id="73927-174">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="73927-175">Em `MainWindow.xaml.cs` , modifique o Construtor conforme mostrado abaixo e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="73927-175">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="73927-176">No construtor, EnsureHttps é registrado como o manipulador de eventos no `NavigationStarting` evento no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="73927-176">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="73927-177">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="73927-177">Press `F5` to build and run your project.</span></span> <span data-ttu-id="73927-178">Confirme que, ao navegar para um site HTTP, a WebView **permanecerá inalterada**.</span><span class="sxs-lookup"><span data-stu-id="73927-178">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span> <span data-ttu-id="73927-179">No entanto, o WebView vai navegar para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="73927-179">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="73927-180">Etapa 6-scripting</span><span class="sxs-lookup"><span data-stu-id="73927-180">Step 6 - Scripting</span></span>  

<span data-ttu-id="73927-181">Você pode usar aplicativos de host para injetar código JavaScript em controles WebView2 em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="73927-181">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="73927-182">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a quaisquer quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="73927-182">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="73927-183">O JavaScript injetado é executado após a criação do objeto global e antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="73927-183">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="73927-184">Você pode usar o script para alertar o usuário ao navegar para um site que não seja HTTPS.</span><span class="sxs-lookup"><span data-stu-id="73927-184">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="73927-185">Modifique a `EnsureHttps` função para que ela Insira o script no conteúdo da Web usando o método [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) .</span><span class="sxs-lookup"><span data-stu-id="73927-185">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) method.</span></span>  

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

<span data-ttu-id="73927-186">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="73927-186">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="73927-187">Confirme se o aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="73927-187">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="73927-189">HTTPS</span><span class="sxs-lookup"><span data-stu-id="73927-189">HTTPS</span></span>
:::image-end:::

## <span data-ttu-id="73927-190">Etapa 7-comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="73927-190">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="73927-191">O conteúdo do host e da Web pode se comunicar uns com os outros usando `postMessage` o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="73927-191">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="73927-192">Conteúdo da Web em um controle WebView2 pode postar uma mensagem para o host usando `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="73927-192">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="73927-193">O host manipula a mensagem usando qualquer registro registrado `WebMessageReceived` no host.</span><span class="sxs-lookup"><span data-stu-id="73927-193">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="73927-194">Hospeda mensagens postadas em conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="73927-194">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="73927-195">Essas mensagens são detectadas pelos manipuladores adicionados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="73927-195">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="73927-196">Esse mecanismo de comunicação permite que o conteúdo da Web passe mensagens para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="73927-196">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="73927-197">Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="73927-197">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="73927-198">No **MainWindow.XAML.cs**, atualize o construtor e crie uma `InitializeAsync` função conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="73927-198">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="73927-199">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) porque a inicialização `CoreWebView2` é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="73927-199">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

2. <span data-ttu-id="73927-200">Após a inicialização do **CoreWebView2** , registre um manipulador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="73927-200">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="73927-201">Na atualização do **MainWindow.XAML.cs** `InitializeAsync` e adicione `UpdateAddressBar` usando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="73927-201">In **MainWindow.xaml.cs** update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

3. <span data-ttu-id="73927-202">Para que o WebView envie e responda à mensagem da Web, após `CoreWebView2` a inicialização, o host:</span><span class="sxs-lookup"><span data-stu-id="73927-202">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  

    1. <span data-ttu-id="73927-203">Injeta um script para o conteúdo da Web que registra um manipulador para imprimir mensagens do host.</span><span class="sxs-lookup"><span data-stu-id="73927-203">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    2. <span data-ttu-id="73927-204">Injeta um script para o conteúdo da Web que envia a URL para o host.</span><span class="sxs-lookup"><span data-stu-id="73927-204">Injects a script to the web content that posts the URL to the host.</span></span>  

<span data-ttu-id="73927-205">No `MainWindow.xaml.cs` , atualize da `InitializeAsync` seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="73927-205">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="73927-206">Pressione `F5` para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73927-206">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="73927-207">Agora a barra de endereços exibe o URI na WebView e, quando você navega com êxito para um novo URI, o WebView alerta o usuário do URI exibido na WebView.</span><span class="sxs-lookup"><span data-stu-id="73927-207">Now the address bar displays the URI in the WebView and when you successfully navigate to a new URI, the WebView alerts the user of the URI displayed in the WebView.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
   <span data-ttu-id="73927-209">addressBar</span><span class="sxs-lookup"><span data-stu-id="73927-209">addressBar</span></span>
:::image-end:::

<span data-ttu-id="73927-210">Parabéns, você criou seu primeiro aplicativo WebView2!</span><span class="sxs-lookup"><span data-stu-id="73927-210">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="73927-211">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="73927-211">Next steps</span></span>  

* <span data-ttu-id="73927-212">Fazer check-out do [repositório WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) para obter um exemplo abrangente de recursos do WebView2's</span><span class="sxs-lookup"><span data-stu-id="73927-212">Checkout the [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) for a comprehensive example of WebView2's capabilities</span></span>
* <span data-ttu-id="73927-213">[Referência de API](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md) de check-out para obter informações mais detalhadas sobre nossas APIs</span><span class="sxs-lookup"><span data-stu-id="73927-213">Checkout [API reference](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md) for more detailed information about our APIs</span></span>
* <span data-ttu-id="73927-214">Fazer check-out de uma lista de [recursos do WebView2](../index.md#next-steps) para saber mais sobre o WebView2</span><span class="sxs-lookup"><span data-stu-id="73927-214">Checkout a list of [WebView2 Resources](../index.md#next-steps) to learn more about WebView2</span></span>

## <span data-ttu-id="73927-215">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="73927-215">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="73927-216">Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários!</span><span class="sxs-lookup"><span data-stu-id="73927-216">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="73927-217">Visite o [repositório de comentários](https://aka.ms/webviewfeedback) da WebView da Microsoft Edge para enviar solicitações de recursos ou relatórios de erros ou Pesquisar problemas conhecidos.</span><span class="sxs-lookup"><span data-stu-id="73927-217">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  
