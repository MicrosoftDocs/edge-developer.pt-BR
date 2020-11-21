---
description: Guia de introdução com o WebView2 para aplicativos WinForms
title: Introdução ao WebView2 para aplicativos WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos WinForms, WinForms, Edge, CoreWebView2, controle do navegador, HTML Edge, introdução, introdução, .NET, formulários do Windows
ms.openlocfilehash: f4768c38f293d1931e625136ea7068a61176541e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182385"
---
# <span data-ttu-id="7f23a-104">Introdução ao WebView2 no Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7f23a-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="7f23a-105">Neste artigo, comece a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2](/microsoft-edge/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="7f23a-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2](/microsoft-edge/webview2/index).</span></span>  <span data-ttu-id="7f23a-106">Para obter mais informações sobre APIs individuais, consulte [referência de API](/dotnet/api/microsoft.web.webview2.winforms).</span><span class="sxs-lookup"><span data-stu-id="7f23a-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.winforms).</span></span>  

## <span data-ttu-id="7f23a-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7f23a-107">Prerequisites</span></span>  

<span data-ttu-id="7f23a-108">Verifique se você instalou a seguinte lista de pré-requisitos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="7f23a-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="7f23a-109">[WebView2 Runtime][Webview2Installer] ou qualquer [canal do Canárias Microsoft Edge (Chromium) não estável](https://www.microsoftedgeinsider.com/download) instalado no Windows 10, no Windows 8,1 ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7f23a-109">[WebView2 Runtime][Webview2Installer] or any [non-stable Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="7f23a-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7f23a-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="7f23a-111">O WebView2 atualmente não é compatível com os designers do .NET 5 e do .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7f23a-111">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>

## <span data-ttu-id="7f23a-112">Etapa 1-criar um único aplicativo de janela</span><span class="sxs-lookup"><span data-stu-id="7f23a-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="7f23a-113">Comece com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="7f23a-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="7f23a-114">Abra o **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="7f23a-114">Open **Visual Studio.**</span></span>

1. <span data-ttu-id="7f23a-115">Escolha **aplicativo do Windows Forms .NET Framework** e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7f23a-115">Choose **Windows Forms .NET Framework App** and then choose **Next**.</span></span>

    ![newproject](./media/winforms-newproject.png)

1. <span data-ttu-id="7f23a-117">Insira valores para **nome** e **local**do projeto.</span><span class="sxs-lookup"><span data-stu-id="7f23a-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="7f23a-118">Selecione **.NET Framework 4.6.2** ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7f23a-118">Select **.NET Framework 4.6.2** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

1. <span data-ttu-id="7f23a-120">Escolha **criar** para criar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="7f23a-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="7f23a-121">Etapa 2-instalar o SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="7f23a-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="7f23a-122">Em seguida, adicione o SDK WebView2 ao projeto usando o NuGet.</span><span class="sxs-lookup"><span data-stu-id="7f23a-122">Next add the WebView2 SDK to the project using NuGet.</span></span>

1. <span data-ttu-id="7f23a-123">Abra o menu de contexto no projeto \ (clique com o botão direito do mouse \) e escolha **gerenciar pacotes NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="7f23a-123">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gerenciar pacotes NuGet":::
       <span data-ttu-id="7f23a-125">Gerenciar pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="7f23a-125">Manage NuGet Packages</span></span> :::image-end:::

1. <span data-ttu-id="7f23a-126">Digite `Microsoft.Web.WebView2` na barra de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7f23a-126">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="7f23a-127">Escolha **Microsoft. Web. WebView2** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7f23a-127">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  

    ![NuGet](./media/installnuget.png)

<span data-ttu-id="7f23a-129">Você está pronto para começar a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="7f23a-129">You're all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="7f23a-130">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="7f23a-130">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="7f23a-131">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="7f23a-131">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="7f23a-133">Etapa 3-criar uma única WebView</span><span class="sxs-lookup"><span data-stu-id="7f23a-133">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="7f23a-134">Em seguida, adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f23a-134">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="7f23a-135">Abra o **Windows Forms Designer**.</span><span class="sxs-lookup"><span data-stu-id="7f23a-135">Open the **Windows Forms Designer**.</span></span>  
1. <span data-ttu-id="7f23a-136">Procure por **WebView2** na **caixa de ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="7f23a-136">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="7f23a-137">Arraste e solte o controle **WebView2** no aplicativo formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f23a-137">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Caixa de ferramentas exibindo WebView2":::
       <span data-ttu-id="7f23a-139">Caixa de ferramentas exibindo WebView2</span><span class="sxs-lookup"><span data-stu-id="7f23a-139">Toolbox displaying WebView2</span></span> :::image-end:::  

1. <span data-ttu-id="7f23a-140">Altere a `Name` propriedade para `webView` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-140">Change the `Name` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propriedades do controle WebView2":::
       <span data-ttu-id="7f23a-142">Propriedades do controle WebView2</span><span class="sxs-lookup"><span data-stu-id="7f23a-142">Properties of the WebView2 control</span></span> :::image-end:::

1. <span data-ttu-id="7f23a-143">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7f23a-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="7f23a-144">Defina a propriedade Source como</span><span class="sxs-lookup"><span data-stu-id="7f23a-144">Set the Source property to</span></span> <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="A propriedade Source do controle WebView2":::
       <span data-ttu-id="7f23a-146">A propriedade Source do controle WebView2</span><span class="sxs-lookup"><span data-stu-id="7f23a-146">The Source property of the WebView2 control</span></span> :::image-end:::

<span data-ttu-id="7f23a-147">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="7f23a-147">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="7f23a-148">Confirme se o controle WebView2 é exibido [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="7f23a-148">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="7f23a-150">Se estiver trabalhando em um monitor de DPI alta, talvez seja necessário [configurar seu aplicativo do Windows Forms para suporte a dpi alta](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="7f23a-150">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="7f23a-151">Etapa 4-manipular eventos de redimensionamento de janela</span><span class="sxs-lookup"><span data-stu-id="7f23a-151">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="7f23a-152">Adicione mais alguns controles aos formulários do Windows a partir da caixa de ferramentas e, em seguida, manipule a janela redimensionar eventos apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="7f23a-152">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="7f23a-153">No **Windows Forms Designer**, abra a **caixa de ferramentas**</span><span class="sxs-lookup"><span data-stu-id="7f23a-153">In the **Windows Forms Designer**, open the **Toolbox**</span></span>
1. <span data-ttu-id="7f23a-154">Arraste e solte uma **caixa de texto** no aplicativo formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f23a-154">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="7f23a-155">Nomeie a **caixa de texto** `addressBar` na **guia Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="7f23a-155">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
1. <span data-ttu-id="7f23a-156">Arraste e solte um **botão** no aplicativo formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f23a-156">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="7f23a-157">Altere o texto no **botão** para `Go!` e nomeie o **botão** `goButton` na **guia Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="7f23a-157">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="7f23a-158">O aplicativo deve se parecer com a imagem a seguir no designer.</span><span class="sxs-lookup"><span data-stu-id="7f23a-158">The app should look like the following image in the designer.</span></span>
    
    ![desenvolvedor](./media/winforms-designer.png)

1. <span data-ttu-id="7f23a-160">No **Form1.cs** , defina `Form_Resize` para manter os controles in-loco quando a janela do aplicativo for redimensionada.</span><span class="sxs-lookup"><span data-stu-id="7f23a-160">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```

<span data-ttu-id="7f23a-161">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="7f23a-161">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="7f23a-162">Confirme se o aplicativo é exibido de forma semelhante à seguinte captura de tela.</span><span class="sxs-lookup"><span data-stu-id="7f23a-162">Confirm that the app displays similar to the following screenshot.</span></span>

![aplicativo](./media/winforms-app.png)

## <span data-ttu-id="7f23a-164">Etapa 5-navegação</span><span class="sxs-lookup"><span data-stu-id="7f23a-164">Step 5 - Navigation</span></span>

<span data-ttu-id="7f23a-165">Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe ao adicionar uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f23a-165">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="7f23a-166">Em `Form1.cs` Adicionar o `CoreWebView2` namespace, insira o trecho de código a seguir na parte superior de `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-166">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. <span data-ttu-id="7f23a-167">No **Windows Forms Designer**, clique duas vezes no `Go!` botão para criar o `goButton_Click` método `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-167">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="7f23a-168">Copie e cole o seguinte snippet dentro da função.</span><span class="sxs-lookup"><span data-stu-id="7f23a-168">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="7f23a-169">Agora, a `goButton_Click` função navega pelo WebView para a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="7f23a-169">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="7f23a-170">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="7f23a-170">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="7f23a-171">Insira uma nova URL na barra de endereços e selecione **Go (ir**).</span><span class="sxs-lookup"><span data-stu-id="7f23a-171">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="7f23a-172">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-172">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="7f23a-173">Confirme se o controle WebView2 navega para a URL.</span><span class="sxs-lookup"><span data-stu-id="7f23a-173">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="7f23a-174">Assegure-se de que uma URL completa seja inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="7f23a-174">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="7f23a-175">Uma `ArgumentException` será lançada se a URL não iniciar com `http://` ou</span><span class="sxs-lookup"><span data-stu-id="7f23a-175">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="7f23a-177">Etapa 6-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="7f23a-177">Step 6 - Navigation events</span></span>  

<span data-ttu-id="7f23a-178">Durante a navegação na página da Web, o controle WebView2 gera eventos.</span><span class="sxs-lookup"><span data-stu-id="7f23a-178">During webpage navigation, the WebView2 control raises events.</span></span> <span data-ttu-id="7f23a-179">O aplicativo que hospeda os controles de WebView2 escuta os eventos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f23a-179">The application that hosts WebView2 controls listens for the following events.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="7f23a-180">Para obter mais informações, consulte [eventos de navegação](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="7f23a-180">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   <span data-ttu-id="7f23a-182">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="7f23a-182">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="7f23a-183">Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="7f23a-183">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="7f23a-184">Quando há um redirecionamento HTTP, há vários `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="7f23a-184">When there's an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="7f23a-185">Para demonstrar como usar esses eventos, comece registrando um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https.</span><span class="sxs-lookup"><span data-stu-id="7f23a-185">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="7f23a-186">Em `Form1.cs` , modifique o Construtor conforme mostrado abaixo e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="7f23a-186">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

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

<span data-ttu-id="7f23a-187">No construtor, EnsureHttps é registrado como o manipulador de eventos no `NavigationStarting` evento no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7f23a-187">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="7f23a-188">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="7f23a-188">Select `F5` to build and run your project.</span></span> <span data-ttu-id="7f23a-189">Confirme que, ao navegar para um site HTTP, a WebView permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="7f23a-189">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="7f23a-190">No entanto, o WebView vai navegar para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7f23a-190">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="7f23a-191">Etapa 7-scripting</span><span class="sxs-lookup"><span data-stu-id="7f23a-191">Step 7 - Scripting</span></span>  

<span data-ttu-id="7f23a-192">Você pode usar aplicativos de host para injetar código JavaScript em controles WebView2 em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7f23a-192">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="7f23a-193">O JavaScript injetado aplica-se a todos os novos documentos de nível superior e quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="7f23a-193">The injected JavaScript applies to all new top-level documents and any child frames, until the JavaScript is removed.</span></span>  <span data-ttu-id="7f23a-194">O JavaScript injetado é executado após a criação do objeto global e antes de qualquer script incluído no documento HTML.</span><span class="sxs-lookup"><span data-stu-id="7f23a-194">The injected JavaScript is run after creation of the global object, and before any scripts included in the HTML document.</span></span>  

<span data-ttu-id="7f23a-195">Você pode usar o script para alertar o usuário ao navegar para um site que não seja HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7f23a-195">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="7f23a-196">Modifique a `EnsureHttps` função para que ela Insira o script no conteúdo da Web usando o método [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="7f23a-196">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="7f23a-197">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="7f23a-197">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="7f23a-198">Confirme se o aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7f23a-198">Confirm that the application displays an alert when you navigate to a site that doesn't use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="7f23a-200">Etapa 8 – comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="7f23a-200">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="7f23a-201">O conteúdo do host e da Web pode se comunicar uns com os outros usando `postMessage` o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="7f23a-201">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="7f23a-202">Conteúdo da Web em um controle WebView2 pode postar uma mensagem para o host usando `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-202">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="7f23a-203">O host manipula a mensagem usando qualquer registro registrado `WebMessageReceived` no host.</span><span class="sxs-lookup"><span data-stu-id="7f23a-203">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="7f23a-204">Hospeda mensagens postadas em conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-204">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="7f23a-205">Essas mensagens são detectadas pelos manipuladores adicionados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-205">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="7f23a-206">Esse mecanismo de comunicação permite que o conteúdo da Web passe mensagens para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="7f23a-206">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="7f23a-207">Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7f23a-207">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="7f23a-208">No **Form1.cs**, atualize o construtor e crie uma `InitializeAsync` função conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f23a-208">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="7f23a-209">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async]() porque a inicialização `CoreWebView2` é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7f23a-209">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

1. <span data-ttu-id="7f23a-210">Após a inicialização do **CoreWebView2** , registre um manipulador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-210">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="7f23a-211">Em `Form1.cs` , atualize `InitializeAsync` e adicione `UpdateAddressBar` usando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f23a-211">In `Form1.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1. <span data-ttu-id="7f23a-212">Para que o WebView envie e responda à mensagem da Web, após a `CoreWebView2` inicialização, o host injeta um script no conteúdo da Web para:</span><span class="sxs-lookup"><span data-stu-id="7f23a-212">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="7f23a-213">Envie a URL para o host usando `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="7f23a-213">Send the URL to the host using `postMessage`.</span></span>
    1. <span data-ttu-id="7f23a-214">Registre um manipulador de eventos para imprimir uma mensagem enviada do host.</span><span class="sxs-lookup"><span data-stu-id="7f23a-214">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="7f23a-215">Em `Form1.cs` , atualize `InitializeAsync` conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f23a-215">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="7f23a-216">Selecione `F5` para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f23a-216">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="7f23a-217">Confirme se a barra de endereços exibe a URL do site exibida no WebView.</span><span class="sxs-lookup"><span data-stu-id="7f23a-217">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="7f23a-218">Além disso, quando você navegar com êxito para uma nova URL, o WebView alertará o usuário da URL exibida na WebView.</span><span class="sxs-lookup"><span data-stu-id="7f23a-218">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="7f23a-220">Parabéns, você criou seu primeiro aplicativo WebView2!</span><span class="sxs-lookup"><span data-stu-id="7f23a-220">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="7f23a-221">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="7f23a-221">Next steps</span></span> 

<span data-ttu-id="7f23a-222">Para continuar aprendendo mais sobre o WebView2, navegue até os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f23a-222">To continue learning more about WebView2, navigate to the following resources.</span></span>

* <span data-ttu-id="7f23a-223">O [repositório WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) tem um exemplo abrangente de recursos do WebView2's.</span><span class="sxs-lookup"><span data-stu-id="7f23a-223">The [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) has a comprehensive example of WebView2's capabilities.</span></span>
* <span data-ttu-id="7f23a-224">A [referência de API](/dotnet/api/microsoft.web.webview2.winforms.webview2) para obter informações mais detalhadas sobre nossas APIs.</span><span class="sxs-lookup"><span data-stu-id="7f23a-224">The [API reference](/dotnet/api/microsoft.web.webview2.winforms.webview2) for more detailed information about our APIs.</span></span>
* <span data-ttu-id="7f23a-225">[Recursos do WebView2](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="7f23a-225">[WebView2 Resources](../index.md#next-steps).</span></span>


## <span data-ttu-id="7f23a-226">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="7f23a-226">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador do WebView2" 
