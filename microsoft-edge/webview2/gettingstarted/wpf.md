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
ms.openlocfilehash: 01d92322a85e38dab3c502e8dd76729fef8400b1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652458"
---
# <span data-ttu-id="23426-104">Introdução ao WebView2 no WPF (visualização)</span><span class="sxs-lookup"><span data-stu-id="23426-104">Getting Started with WebView2 in WPF (Preview)</span></span>  

<span data-ttu-id="23426-105">Neste artigo, comece a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2 (visualização)](/microsoft-edge/hosting/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="23426-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="23426-106">Para obter mais informações sobre APIs individuais, consulte [referência de API](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="23426-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="23426-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="23426-107">Prerequisites</span></span>  

<span data-ttu-id="23426-108">Verifique se você instalou a seguinte lista de pré-requisitos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="23426-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="23426-109">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) instalado no Windows 10, no Windows 8,1 ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23426-109">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span>  <span data-ttu-id="23426-110">A equipe do Microsoft Edge WebView recomenda usar o canal Canárias.</span><span class="sxs-lookup"><span data-stu-id="23426-110">The Microsoft Edge WebView team recommends using the Canary channel.</span></span>  
* <span data-ttu-id="23426-111">[Visual Studio](https://visualstudio.microsoft.com/) 2015 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="23426-111">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later.</span></span>  

## <span data-ttu-id="23426-112">Etapa 1-criar um único aplicativo de janela</span><span class="sxs-lookup"><span data-stu-id="23426-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="23426-113">Comece com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="23426-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="23426-114">Abra o **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="23426-114">Open **Visual Studio.**</span></span>
2. <span data-ttu-id="23426-115">Escolha **aplicativo WPF .NET Core** ou **aplicativo WPF .NET Framework**e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="23426-115">Choose **WPF .NET Core App** or **WPF .NET Framework App**, and then choose **Next**.</span></span>  

    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Núcleo do WPF":::
             <span data-ttu-id="23426-117">Núcleo do WPF</span><span class="sxs-lookup"><span data-stu-id="23426-117">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Estrutura WPF":::
             <span data-ttu-id="23426-119">Estrutura WPF</span><span class="sxs-lookup"><span data-stu-id="23426-119">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

3. <span data-ttu-id="23426-120">Insira valores para **nome** e **local**do projeto.</span><span class="sxs-lookup"><span data-stu-id="23426-120">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="23426-121">Selecione .NET Framework 4.6.2 ou posterior ou .NET Core 3,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="23426-121">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  

:::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Criar núcleo":::
             <span data-ttu-id="23426-123">Criar núcleo</span><span class="sxs-lookup"><span data-stu-id="23426-123">Create core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Criar estrutura":::
             <span data-ttu-id="23426-125">Criar estrutura</span><span class="sxs-lookup"><span data-stu-id="23426-125">Create Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

4. <span data-ttu-id="23426-126">Escolha **criar** para criar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="23426-126">Choose **Create** to create your project.</span></span>  

## <span data-ttu-id="23426-127">Etapa 2-instalar o SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="23426-127">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="23426-128">Em seguida, adicione o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="23426-128">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="23426-129">Para a visualização, instale o SDK do WebView2 usando NuGet.</span><span class="sxs-lookup"><span data-stu-id="23426-129">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="23426-130">Abra o menu de contexto no projeto \ (clique com o botão direito do mouse \) e escolha **gerenciar pacotes NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="23426-130">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="23426-132">NuGet</span><span class="sxs-lookup"><span data-stu-id="23426-132">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="23426-133">Digite `Microsoft.Web.WebView2` na barra de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="23426-133">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="23426-134">Escolha **Microsoft. Web. WebView2** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="23426-134">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="23426-135">Defina a versão do pacote como **pré-lançamento**e escolha **instalar**.</span><span class="sxs-lookup"><span data-stu-id="23426-135">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

     ![NuGet](./media/installnuget.PNG)

<span data-ttu-id="23426-137">Você está pronto para começar a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="23426-137">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="23426-138">Pressione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="23426-138">Press `F5` to build and run the project.</span></span>  <span data-ttu-id="23426-139">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="23426-139">The running project displays an empty window.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicativo vazio":::
   <span data-ttu-id="23426-141">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="23426-141">Empty app</span></span>
:::image-end:::

## <span data-ttu-id="23426-142">Etapa 3-criar uma única WebView em MainWindow. XAML</span><span class="sxs-lookup"><span data-stu-id="23426-142">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="23426-143">Em seguida, adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23426-143">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="23426-144">Abrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="23426-144">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="23426-145">Adicione o namespace WebView2 XAML inserindo a seguinte linha dentro da `<Window/>` marca.</span><span class="sxs-lookup"><span data-stu-id="23426-145">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  

    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  

    <span data-ttu-id="23426-146">Confirme se o código `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="23426-146">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  

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

2. <span data-ttu-id="23426-147">Adicione o controle WebView2 substituindo as `<Grid>` marcas com o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="23426-147">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="23426-148">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="23426-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  

    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  

3. <span data-ttu-id="23426-149">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="23426-149">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="23426-150">Confirme se o controle WebView2 é exibido [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="23426-150">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="23426-152">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="23426-152">Microsoft.com</span></span> :::image-end:::

## <span data-ttu-id="23426-153">Etapa 4-navegação</span><span class="sxs-lookup"><span data-stu-id="23426-153">Step 4 - Navigation</span></span>  

<span data-ttu-id="23426-154">Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe ao adicionar uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23426-154">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="23426-155">Em **MainWindow. XAML**, adicione uma barra de endereços copiando e colando o trecho de código a seguir dentro do DockPanel que contém o WebView.</span><span class="sxs-lookup"><span data-stu-id="23426-155">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  

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

<span data-ttu-id="23426-156">Confirme se a `DockPanel` seção de `MainWindow.xaml` é semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="23426-156">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  

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

2. <span data-ttu-id="23426-157">Abrir `MainWindow.xaml.cs` no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="23426-157">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="23426-158">Adicione o `CoreWebView2` namespace inserindo o trecho de código a seguir na parte superior de `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="23426-158">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

3. <span data-ttu-id="23426-159">No **MainWindow.XAML.cs**, copie o trecho de código a seguir para criar o `ButtonGo_Click` método, que navega pelo WebView para a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="23426-159">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  

    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="23426-160">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="23426-160">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="23426-161">Insira uma nova URL na barra de endereços e clique em **ir**.</span><span class="sxs-lookup"><span data-stu-id="23426-161">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="23426-162">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="23426-162">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="23426-163">Confirme se o controle WebView2 navega para a URL.</span><span class="sxs-lookup"><span data-stu-id="23426-163">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="23426-164">Certifique-se de que uma URL completa seja inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="23426-164">Make sure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="23426-165">Uma `ArgumentException` será lançada se a URL não iniciar com `http://` ou</span><span class="sxs-lookup"><span data-stu-id="23426-165">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
   <span data-ttu-id="23426-167">Bing</span><span class="sxs-lookup"><span data-stu-id="23426-167">Bing</span></span>
:::image-end:::

## <span data-ttu-id="23426-168">Etapa 5-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="23426-168">Step 5 - Navigation events</span></span>  

<span data-ttu-id="23426-169">O aplicativo que hospeda os controles WebView2 ouve os eventos a seguir que são gerados pelo controle WebView2 durante a navegação em páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="23426-169">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="23426-170">Para obter mais informações, consulte [eventos de navegação](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="23426-170">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   <span data-ttu-id="23426-172">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="23426-172">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="23426-173">Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="23426-173">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="23426-174">Quando há um redirecionamento HTTP, há vários `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="23426-174">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="23426-175">Para demonstrar como usar esses eventos, comece registrando um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https.</span><span class="sxs-lookup"><span data-stu-id="23426-175">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="23426-176">Em `MainWindow.xaml.cs` , modifique o Construtor conforme mostrado abaixo e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="23426-176">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="23426-177">No construtor, EnsureHttps é registrado como o manipulador de eventos no `NavigationStarting` evento no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="23426-177">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="23426-178">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="23426-178">Press `F5` to build and run your project.</span></span> <span data-ttu-id="23426-179">Confirme que, ao navegar para um site HTTP, a WebView **permanecerá inalterada**.</span><span class="sxs-lookup"><span data-stu-id="23426-179">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span> <span data-ttu-id="23426-180">No entanto, o WebView vai navegar para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="23426-180">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="23426-181">Etapa 6-scripting</span><span class="sxs-lookup"><span data-stu-id="23426-181">Step 6 - Scripting</span></span>  

<span data-ttu-id="23426-182">Você pode usar aplicativos de host para injetar código JavaScript em controles WebView2 em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="23426-182">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="23426-183">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a quaisquer quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="23426-183">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="23426-184">O JavaScript injetado é executado após a criação do objeto global e antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="23426-184">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="23426-185">Você pode usar o script para alertar o usuário ao navegar para um site que não seja HTTPS.</span><span class="sxs-lookup"><span data-stu-id="23426-185">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="23426-186">Modifique a `EnsureHttps` função para que ela Insira o script no conteúdo da Web usando o método [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) .</span><span class="sxs-lookup"><span data-stu-id="23426-186">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) method.</span></span>  

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

<span data-ttu-id="23426-187">Pressione `F5` para compilar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="23426-187">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="23426-188">Confirme se o aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="23426-188">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="23426-190">HTTPS</span><span class="sxs-lookup"><span data-stu-id="23426-190">HTTPS</span></span>
:::image-end:::

## <span data-ttu-id="23426-191">Etapa 7-comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="23426-191">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="23426-192">O conteúdo do host e da Web pode se comunicar uns com os outros usando `postMessage` o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="23426-192">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="23426-193">Conteúdo da Web em um controle WebView2 pode postar uma mensagem para o host usando `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="23426-193">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="23426-194">O host manipula a mensagem usando qualquer registro registrado `WebMessageReceived` no host.</span><span class="sxs-lookup"><span data-stu-id="23426-194">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="23426-195">Hospeda mensagens postadas em conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="23426-195">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="23426-196">Essas mensagens são detectadas pelos manipuladores adicionados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="23426-196">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="23426-197">Esse mecanismo de comunicação permite que o conteúdo da Web passe mensagens para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="23426-197">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="23426-198">Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="23426-198">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="23426-199">No **MainWindow.XAML.cs**, atualize o construtor e crie uma `InitializeAsync` função conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="23426-199">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="23426-200">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) porque a inicialização `CoreWebView2` é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="23426-200">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

2. <span data-ttu-id="23426-201">Após a inicialização do **CoreWebView2** , registre um manipulador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="23426-201">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="23426-202">Na atualização do **MainWindow.XAML.cs** `InitializeAsync` e adicione `UpdateAddressBar` usando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="23426-202">In **MainWindow.xaml.cs** update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

3. <span data-ttu-id="23426-203">Para que o WebView envie e responda à mensagem da Web, após `CoreWebView2` a inicialização, o host:</span><span class="sxs-lookup"><span data-stu-id="23426-203">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  

    1. <span data-ttu-id="23426-204">Injeta um script para o conteúdo da Web que registra um manipulador para imprimir mensagens do host.</span><span class="sxs-lookup"><span data-stu-id="23426-204">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    2. <span data-ttu-id="23426-205">Injeta um script para o conteúdo da Web que envia a URL para o host.</span><span class="sxs-lookup"><span data-stu-id="23426-205">Injects a script to the web content that posts the URL to the host.</span></span>  

<span data-ttu-id="23426-206">No `MainWindow.xaml.cs` , atualize da `InitializeAsync` seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="23426-206">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="23426-207">Pressione `F5` para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23426-207">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="23426-208">Agora a barra de endereços exibe o URI na WebView e, quando você navega com êxito para um novo URI, o WebView alerta o usuário do URI exibido na WebView.</span><span class="sxs-lookup"><span data-stu-id="23426-208">Now the address bar displays the URI in the WebView and when you successfully navigate to a new URI, the WebView alerts the user of the URI displayed in the WebView.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
   <span data-ttu-id="23426-210">addressBar</span><span class="sxs-lookup"><span data-stu-id="23426-210">addressBar</span></span>
:::image-end:::

<span data-ttu-id="23426-211">Parabéns, você criou seu primeiro aplicativo WebView2!</span><span class="sxs-lookup"><span data-stu-id="23426-211">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="23426-212">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="23426-212">Next Steps</span></span>  

<span data-ttu-id="23426-213">Há muitas funcionalidades WebView2s que não são abordadas neste guia passo a passo.</span><span class="sxs-lookup"><span data-stu-id="23426-213">There are plenty of WebView2 functionalities that are not covered in this walkthrough.</span></span>  

<span data-ttu-id="23426-214">Para saber mais:</span><span class="sxs-lookup"><span data-stu-id="23426-214">To learn more:</span></span>  

* <span data-ttu-id="23426-215">Explore a [referência de API](../reference/dotnet/0-9-515-reference-webview2.md) para obter informações detalhadas sobre cada API.</span><span class="sxs-lookup"><span data-stu-id="23426-215">Please explore [API reference](../reference/dotnet/0-9-515-reference-webview2.md) for detailed information about each API.</span></span>  

## <span data-ttu-id="23426-216">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="23426-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="23426-217">Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários!</span><span class="sxs-lookup"><span data-stu-id="23426-217">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="23426-218">Visite o [repositório de comentários](https://aka.ms/webviewfeedback) da WebView da Microsoft Edge para enviar solicitações de recursos ou relatórios de erros ou Pesquisar problemas conhecidos.</span><span class="sxs-lookup"><span data-stu-id="23426-218">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  
