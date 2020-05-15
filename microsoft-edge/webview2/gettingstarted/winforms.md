---
description: Hospedar conteúdo da Web em seu aplicativo do Windows Forms com o controle do Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 para aplicativos do Windows Forms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos WinForms, WinForms, Edge, CoreWebView2, controle do navegador, HTML Edge, introdução, introdução, .NET, formulários do Windows
ms.openlocfilehash: b2616eeed2a8e896889e2cc1a395c401a8aad435
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652486"
---
# <span data-ttu-id="6d0a1-104">Introdução ao WebView2 em aplicativos do Windows Forms (visualização)</span><span class="sxs-lookup"><span data-stu-id="6d0a1-104">Getting Started with WebView2 in Windows Forms apps (Preview)</span></span>  

<span data-ttu-id="6d0a1-105">Neste artigo, comece a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2 (visualização)](/microsoft-edge/hosting/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="6d0a1-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="6d0a1-106">Para obter mais informações sobre APIs individuais, consulte [referência de API](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="6d0a1-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="6d0a1-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="6d0a1-107">Prerequisites</span></span>  

<span data-ttu-id="6d0a1-108">Verifique se você instalou a seguinte lista de pré-requisitos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="6d0a1-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="6d0a1-109">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) instalado no Windows 10, no Windows 8,1 ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-109">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span>  <span data-ttu-id="6d0a1-110">A equipe do Microsoft Edge WebView recomenda usar o canal Canárias.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-110">The Microsoft Edge WebView team recommends using the Canary channel.</span></span>  
* <span data-ttu-id="6d0a1-111">[Visual Studio](https://visualstudio.microsoft.com/) 2015 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-111">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="6d0a1-112">Se estiver desenvolvendo com o **Windows Forms .NET Core 3,0 ou o .NET 5**, baixe o [Visual Studio (Preview)](https://visualstudio.microsoft.com/vs/preview/)</span><span class="sxs-lookup"><span data-stu-id="6d0a1-112">If developing with **Windows Forms .NET Core 3.0 or .NET 5**, download [Visual Studio (Preview)](https://visualstudio.microsoft.com/vs/preview/)</span></span>

## <span data-ttu-id="6d0a1-113">Etapa 1-criar um único aplicativo de janela</span><span class="sxs-lookup"><span data-stu-id="6d0a1-113">Step 1 - Create a single window application</span></span>

<span data-ttu-id="6d0a1-114">Comece com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-114">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="6d0a1-115">Abra o **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="6d0a1-115">Open **Visual Studio.**</span></span>

2. <span data-ttu-id="6d0a1-116">Escolha **aplicativo do Windows Forms .NET Framework** ou **aplicativo do Windows Forms .NET Core**e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-116">Choose **Windows Forms .NET Framework App** or **Windows Forms .NET Core App**, and then choose **Next**.</span></span>

    ![newproject](./media/winforms-newproject.png)

3. <span data-ttu-id="6d0a1-118">Insira valores para **nome** e **local**do projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="6d0a1-119">Selecione **.NET Framework 4.6.2** ou posterior ou **.NET Core 3,0** ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-119">Select **.NET Framework 4.6.2** or later, or **.NET Core 3.0** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

4. <span data-ttu-id="6d0a1-121">Escolha **criar** para criar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-121">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="6d0a1-122">Etapa 2-instalar o SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="6d0a1-122">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="6d0a1-123">Em seguida, adicione o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-123">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="6d0a1-124">Para a visualização, instale o SDK do WebView2 usando NuGet.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-124">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="6d0a1-125">Abra o menu de contexto no projeto \ (clique com o botão direito do mouse \) e escolha **gerenciar pacotes NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="6d0a1-125">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="6d0a1-127">NuGet</span><span class="sxs-lookup"><span data-stu-id="6d0a1-127">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="6d0a1-128">Digite `Microsoft.Web.WebView2` na barra de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-128">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="6d0a1-129">Escolha **Microsoft. Web. WebView2** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-129">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="6d0a1-130">Defina a versão do pacote como **pré-lançamento**e escolha **instalar**.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-130">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

    ![NuGet](./media/installnuget.png)

<span data-ttu-id="6d0a1-132">Você está pronto para começar a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-132">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="6d0a1-133">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-133">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="6d0a1-134">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-134">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="6d0a1-136">Etapa 3-criar uma única WebView</span><span class="sxs-lookup"><span data-stu-id="6d0a1-136">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="6d0a1-137">Em seguida, adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-137">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="6d0a1-138">Abra o **Windows Forms Designer**.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-138">Open the **Windows Forms Designer**.</span></span>  
2. <span data-ttu-id="6d0a1-139">Procure por **WebView2** na **caixa de ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-139">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="6d0a1-140">Arraste e solte o controle **WebView2** no aplicativo formulários do Windows</span><span class="sxs-lookup"><span data-stu-id="6d0a1-140">Drag and drop the **WebView2** control into the Windows Forms App</span></span>

    ![ferramentas](./media/winforms-toolbox.png)

3. <span data-ttu-id="6d0a1-142">Altere a `Name` propriedade para `webView` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-142">Change the `Name` property to `webView`.</span></span>

    ![ferramentas](./media/winforms-properties.png)

4. <span data-ttu-id="6d0a1-144">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-144">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="6d0a1-145">Defina a propriedade Source como</span><span class="sxs-lookup"><span data-stu-id="6d0a1-145">Set the Source property to</span></span> <https://www.microsoft.com>

    ![ferramentas](./media/winforms-source.png)

<span data-ttu-id="6d0a1-147">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-147">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="6d0a1-148">Confirme se o controle WebView2 é exibido [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-148">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="6d0a1-150">Se estiver trabalhando em um monitor de DPI alta, talvez seja necessário [configurar seu aplicativo do Windows Forms para suporte a dpi alta](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="6d0a1-150">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="6d0a1-151">Etapa 4-manipular eventos de redimensionamento de janela</span><span class="sxs-lookup"><span data-stu-id="6d0a1-151">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="6d0a1-152">Adicione mais alguns controles aos formulários do Windows a partir da caixa de ferramentas e, em seguida, manipule a janela redimensionar eventos apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-152">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="6d0a1-153">No **designer do Windows Forms** , abra a **caixa de ferramentas**</span><span class="sxs-lookup"><span data-stu-id="6d0a1-153">In the **Windows Forms Designer** open the **Toolbox**</span></span>
2. <span data-ttu-id="6d0a1-154">Arraste e solte uma **caixa de texto** no aplicativo formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-154">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="6d0a1-155">Nomeie a **caixa de texto** `addressBar` na **guia Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-155">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
3. <span data-ttu-id="6d0a1-156">Arraste e solte um **botão** no aplicativo formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-156">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="6d0a1-157">Altere o texto no **botão** para `Go!` e nomeie o **botão** `goButton` na **guia Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-157">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

<span data-ttu-id="6d0a1-158">O aplicativo deve ser semelhante ao seguinte no designer:</span><span class="sxs-lookup"><span data-stu-id="6d0a1-158">The app should look like the following in the designer:</span></span>

![desenvolvedor](./media/winforms-designer.png)

4. <span data-ttu-id="6d0a1-160">No **Form1.cs** , defina `Form_Resize` para manter os controles in-loco quando a janela do aplicativo for redimensionada.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-160">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="6d0a1-161">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-161">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="6d0a1-162">Confirme se o aplicativo é exibido de forma semelhante à seguinte captura de tela.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-162">Confirm that the app displays similar to the following screenshot.</span></span>

![app](./media/winforms-app.png)

## <span data-ttu-id="6d0a1-164">Etapa 5-navegação</span><span class="sxs-lookup"><span data-stu-id="6d0a1-164">Step 5 - Navigation</span></span>

<span data-ttu-id="6d0a1-165">Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe ao adicionar uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-165">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="6d0a1-166">Em `Form1.cs` Adicionar o `CoreWebView2` namespace, insira o trecho de código a seguir na parte superior de `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-166">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

2. <span data-ttu-id="6d0a1-167">No **Windows Forms Designer**, clique duas vezes no `Go!` botão para criar o `goButton_Click` método `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-167">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="6d0a1-168">Copie e cole o seguinte snippet dentro da função.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-168">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="6d0a1-169">Agora, a `goButton_Click` função navega pelo WebView para a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-169">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="6d0a1-170">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-170">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="6d0a1-171">Insira uma nova URL na barra de endereços e clique em **ir**.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-171">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="6d0a1-172">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-172">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="6d0a1-173">Confirme se o controle WebView2 navega para a URL.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-173">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="6d0a1-174">Assegure-se de que uma URL completa seja inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-174">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="6d0a1-175">Uma `ArgumentException` será lançada se a URL não iniciar com `http://` ou</span><span class="sxs-lookup"><span data-stu-id="6d0a1-175">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="6d0a1-177">Etapa 6-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="6d0a1-177">Step 6 - Navigation events</span></span>  

<span data-ttu-id="6d0a1-178">O aplicativo que hospeda os controles WebView2 ouve os eventos a seguir que são gerados pelo controle WebView2 durante a navegação em páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-178">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="6d0a1-179">Para obter mais informações, consulte [eventos de navegação](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="6d0a1-179">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   <span data-ttu-id="6d0a1-181">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="6d0a1-181">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="6d0a1-182">Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-182">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="6d0a1-183">Quando há um redirecionamento HTTP, há vários `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-183">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="6d0a1-184">Para demonstrar como usar esses eventos, comece registrando um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-184">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="6d0a1-185">Em `Form1.cs` , modifique o Construtor conforme mostrado abaixo e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-185">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="6d0a1-186">No construtor, EnsureHttps é registrado como o manipulador de eventos no `NavigationStarting` evento no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-186">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="6d0a1-187">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-187">Select `F5` to build and run your project.</span></span> <span data-ttu-id="6d0a1-188">Confirme que, ao navegar para um site HTTP, a WebView permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-188">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="6d0a1-189">No entanto, o WebView vai navegar para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-189">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="6d0a1-190">Etapa 7-scripting</span><span class="sxs-lookup"><span data-stu-id="6d0a1-190">Step 7 - Scripting</span></span>  

<span data-ttu-id="6d0a1-191">Você pode usar aplicativos de host para injetar código JavaScript em controles WebView2 em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-191">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="6d0a1-192">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a quaisquer quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-192">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="6d0a1-193">O JavaScript injetado é executado após a criação do objeto global e antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-193">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="6d0a1-194">Você pode usar o script para alertar o usuário ao navegar para um site que não seja HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-194">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="6d0a1-195">Modifique a `EnsureHttps` função para que ela Insira o script no conteúdo da Web usando o método [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-195">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="6d0a1-196">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-196">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="6d0a1-197">Confirme se o aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-197">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="6d0a1-199">Etapa 8 – comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="6d0a1-199">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="6d0a1-200">O conteúdo do host e da Web pode se comunicar uns com os outros usando `postMessage` o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="6d0a1-200">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="6d0a1-201">Conteúdo da Web em um controle WebView2 pode postar uma mensagem para o host usando `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-201">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="6d0a1-202">O host manipula a mensagem usando qualquer registro registrado `WebMessageReceived` no host.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-202">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="6d0a1-203">Hospeda mensagens postadas em conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-203">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="6d0a1-204">Essas mensagens são detectadas pelos manipuladores adicionados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-204">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="6d0a1-205">Esse mecanismo de comunicação permite que o conteúdo da Web passe mensagens para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-205">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="6d0a1-206">Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-206">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="6d0a1-207">No **Form1.cs**, atualize o construtor e crie uma `InitializeAsync` função conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-207">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="6d0a1-208">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async]() porque a inicialização `CoreWebView2` é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-208">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

2. <span data-ttu-id="6d0a1-209">Após a inicialização do **CoreWebView2** , registre um manipulador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-209">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="6d0a1-210">Em `Form1.cs` Atualizar `InitializeAsync` e adicionar `UpdateAddressBar` usando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-210">In `Form1.cs` update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

3. <span data-ttu-id="6d0a1-211">Para que o WebView envie e responda à mensagem da Web, após a `CoreWebView2` inicialização, o host injeta um script no conteúdo da Web para:</span><span class="sxs-lookup"><span data-stu-id="6d0a1-211">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="6d0a1-212">Envie a URL para o host usando `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="6d0a1-212">Send the URL to the host using `postMessage`.</span></span>
    2. <span data-ttu-id="6d0a1-213">Registre um manipulador de eventos para imprimir uma mensagem enviada do host.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-213">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="6d0a1-214">Em `Form1.cs` , atualize `InitializeAsync` conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-214">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="6d0a1-215">Selecione `F5` para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-215">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="6d0a1-216">Confirme se a barra de endereços exibe a URL do site exibida no WebView.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-216">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="6d0a1-217">Além disso, quando você navegar com êxito para uma nova URL, o WebView alertará o usuário da URL exibida na WebView.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-217">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="6d0a1-219">Parabéns, você criou seu primeiro aplicativo WebView2!</span><span class="sxs-lookup"><span data-stu-id="6d0a1-219">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="6d0a1-220">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="6d0a1-220">Next Steps</span></span>  

<span data-ttu-id="6d0a1-221">Para obter mais informações sobre os recursos do WebView2 não incluídos neste guia passo a passo, consulte a [referência de API](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="6d0a1-221">For more information on WebView2 features not covered in this walkthrough, see the [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>

## <span data-ttu-id="6d0a1-222">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="6d0a1-222">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="6d0a1-223">Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários!</span><span class="sxs-lookup"><span data-stu-id="6d0a1-223">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="6d0a1-224">Visite o [repositório de comentários](https://aka.ms/webviewfeedback) da WebView da Microsoft Edge para enviar solicitações de recursos ou relatórios de erros ou Pesquisar problemas conhecidos.</span><span class="sxs-lookup"><span data-stu-id="6d0a1-224">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  
