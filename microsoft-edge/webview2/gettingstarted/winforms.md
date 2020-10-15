---
description: Guia de introdução com o WebView2 para aplicativos WinForms
title: Introdução ao WebView2 para aplicativos WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicativos WinForms, WinForms, Edge, CoreWebView2, controle do navegador, HTML Edge, introdução, introdução, .NET, formulários do Windows
ms.openlocfilehash: e9451d4bfafacf78f723be75379e57400d0ba914
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119077"
---
# <span data-ttu-id="d11a1-104">Introdução ao WebView2 no Windows Forms (visualização)</span><span class="sxs-lookup"><span data-stu-id="d11a1-104">Getting started with WebView2 in Windows Forms (Preview)</span></span>  

<span data-ttu-id="d11a1-105">Neste artigo, comece a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2 (visualização)](/microsoft-edge/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="d11a1-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/webview2/index).</span></span>  <span data-ttu-id="d11a1-106">Para obter mais informações sobre APIs individuais, consulte [referência de API](/dotnet/api/microsoft.web.webview2.winforms).</span><span class="sxs-lookup"><span data-stu-id="d11a1-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.winforms).</span></span>  

## <span data-ttu-id="d11a1-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d11a1-107">Prerequisites</span></span>  

<span data-ttu-id="d11a1-108">Verifique se você instalou a seguinte lista de pré-requisitos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="d11a1-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="d11a1-109">[Microsoft Edge (Chromium) Canárias Channel](https://www.microsoftedgeinsider.com/download) instalado no Windows 10, no Windows 8,1 ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d11a1-109">[Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="d11a1-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d11a1-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="d11a1-111">O WebView2 não é compatível no momento com o designer do .NET Core 3.0 [(Preview)](https://visualstudio.microsoft.com/vs/preview).</span><span class="sxs-lookup"><span data-stu-id="d11a1-111">WebView2 does not currently support the .NET Core 3.0's [designer (preview)](https://visualstudio.microsoft.com/vs/preview).</span></span>

## <span data-ttu-id="d11a1-112">Etapa 1-criar um único aplicativo de janela</span><span class="sxs-lookup"><span data-stu-id="d11a1-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="d11a1-113">Comece com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="d11a1-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="d11a1-114">Abra o **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="d11a1-114">Open **Visual Studio.**</span></span>

1. <span data-ttu-id="d11a1-115">Escolha **aplicativo do Windows Forms .NET Framework** e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d11a1-115">Choose **Windows Forms .NET Framework App** and then choose **Next**.</span></span>

    ![newproject](./media/winforms-newproject.png)

1. <span data-ttu-id="d11a1-117">Insira valores para **nome** e **local**do projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="d11a1-118">Selecione **.NET Framework 4.6.2** ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d11a1-118">Select **.NET Framework 4.6.2** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

1. <span data-ttu-id="d11a1-120">Escolha **criar** para criar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="d11a1-121">Etapa 2-instalar o SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="d11a1-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="d11a1-122">Em seguida, adicione o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-122">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="d11a1-123">Para a visualização, instale o SDK do WebView2 usando NuGet.</span><span class="sxs-lookup"><span data-stu-id="d11a1-123">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="d11a1-124">Abra o menu de contexto no projeto \ (clique com o botão direito do mouse \) e escolha **gerenciar pacotes NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="d11a1-124">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gerenciar pacotes NuGet":::
       <span data-ttu-id="d11a1-126">Gerenciar pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="d11a1-126">Manage NuGet Packages</span></span> :::image-end:::

1. <span data-ttu-id="d11a1-127">Digite `Microsoft.Web.WebView2` na barra de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d11a1-127">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="d11a1-128">Escolha **Microsoft. Web. WebView2** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d11a1-128">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="d11a1-129">Verifique se a opção **incluir pré-lançamento**, selecione um pacote de pré-lançamento na **versão**e escolha **instalar**.</span><span class="sxs-lookup"><span data-stu-id="d11a1-129">Ensure you check **Include prerelease**, select a prerelease package in **Version**, and then choose **Install**.</span></span>  

    ![NuGet](./media/installnuget.png)

<span data-ttu-id="d11a1-131">Você está pronto para começar a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="d11a1-131">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="d11a1-132">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-132">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="d11a1-133">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="d11a1-133">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="d11a1-135">Etapa 3-criar uma única WebView</span><span class="sxs-lookup"><span data-stu-id="d11a1-135">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="d11a1-136">Em seguida, adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d11a1-136">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="d11a1-137">Abra o **Windows Forms Designer**.</span><span class="sxs-lookup"><span data-stu-id="d11a1-137">Open the **Windows Forms Designer**.</span></span>  
1. <span data-ttu-id="d11a1-138">Procure por **WebView2** na **caixa de ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="d11a1-138">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="d11a1-139">Arraste e solte o controle **WebView2** no aplicativo formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="d11a1-139">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Gerenciar pacotes NuGet":::
       <span data-ttu-id="d11a1-141">Caixa de ferramentas exibindo WebView2</span><span class="sxs-lookup"><span data-stu-id="d11a1-141">Toolbox displaying WebView2</span></span> :::image-end:::  

1. <span data-ttu-id="d11a1-142">Altere a `Name` propriedade para `webView` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-142">Change the `Name` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Gerenciar pacotes NuGet":::
       <span data-ttu-id="d11a1-144">Propriedades do controle WebView2</span><span class="sxs-lookup"><span data-stu-id="d11a1-144">Properties of the WebView2 control</span></span> :::image-end:::

1. <span data-ttu-id="d11a1-145">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="d11a1-145">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="d11a1-146">Defina a propriedade Source como</span><span class="sxs-lookup"><span data-stu-id="d11a1-146">Set the Source property to</span></span> <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Gerenciar pacotes NuGet":::
       <span data-ttu-id="d11a1-148">A propriedade Source do controle WebView2</span><span class="sxs-lookup"><span data-stu-id="d11a1-148">The Source property of the WebView2 control</span></span> :::image-end:::

<span data-ttu-id="d11a1-149">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-149">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="d11a1-150">Confirme se o controle WebView2 é exibido [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="d11a1-150">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="d11a1-152">Se estiver trabalhando em um monitor de DPI alta, talvez seja necessário [configurar seu aplicativo do Windows Forms para suporte a dpi alta](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="d11a1-152">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="d11a1-153">Etapa 4-manipular eventos de redimensionamento de janela</span><span class="sxs-lookup"><span data-stu-id="d11a1-153">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="d11a1-154">Adicione mais alguns controles aos formulários do Windows a partir da caixa de ferramentas e, em seguida, manipule a janela redimensionar eventos apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="d11a1-154">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="d11a1-155">No **designer do Windows Forms** , abra a **caixa de ferramentas**</span><span class="sxs-lookup"><span data-stu-id="d11a1-155">In the **Windows Forms Designer** open the **Toolbox**</span></span>
1. <span data-ttu-id="d11a1-156">Arraste e solte uma **caixa de texto** no aplicativo formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="d11a1-156">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="d11a1-157">Nomeie a **caixa de texto** `addressBar` na **guia Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="d11a1-157">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
1. <span data-ttu-id="d11a1-158">Arraste e solte um **botão** no aplicativo formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="d11a1-158">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="d11a1-159">Altere o texto no **botão** para `Go!` e nomeie o **botão** `goButton` na **guia Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="d11a1-159">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="d11a1-160">O aplicativo deve ser semelhante ao seguinte no designer:</span><span class="sxs-lookup"><span data-stu-id="d11a1-160">The app should look like the following in the designer:</span></span>
    
    ![desenvolvedor](./media/winforms-designer.png)

1. <span data-ttu-id="d11a1-162">No **Form1.cs** , defina `Form_Resize` para manter os controles in-loco quando a janela do aplicativo for redimensionada.</span><span class="sxs-lookup"><span data-stu-id="d11a1-162">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="d11a1-163">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-163">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="d11a1-164">Confirme se o aplicativo é exibido de forma semelhante à seguinte captura de tela.</span><span class="sxs-lookup"><span data-stu-id="d11a1-164">Confirm that the app displays similar to the following screenshot.</span></span>

![aplicativo](./media/winforms-app.png)

## <span data-ttu-id="d11a1-166">Etapa 5-navegação</span><span class="sxs-lookup"><span data-stu-id="d11a1-166">Step 5 - Navigation</span></span>

<span data-ttu-id="d11a1-167">Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe ao adicionar uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d11a1-167">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="d11a1-168">Em `Form1.cs` Adicionar o `CoreWebView2` namespace, insira o trecho de código a seguir na parte superior de `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-168">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. <span data-ttu-id="d11a1-169">No **Windows Forms Designer**, clique duas vezes no `Go!` botão para criar o `goButton_Click` método `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-169">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="d11a1-170">Copie e cole o seguinte snippet dentro da função.</span><span class="sxs-lookup"><span data-stu-id="d11a1-170">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="d11a1-171">Agora, a `goButton_Click` função navega pelo WebView para a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="d11a1-171">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="d11a1-172">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-172">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="d11a1-173">Insira uma nova URL na barra de endereços e clique em **ir**.</span><span class="sxs-lookup"><span data-stu-id="d11a1-173">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="d11a1-174">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-174">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="d11a1-175">Confirme se o controle WebView2 navega para a URL.</span><span class="sxs-lookup"><span data-stu-id="d11a1-175">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="d11a1-176">Assegure-se de que uma URL completa seja inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="d11a1-176">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="d11a1-177">Uma `ArgumentException` será lançada se a URL não iniciar com `http://` ou</span><span class="sxs-lookup"><span data-stu-id="d11a1-177">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="d11a1-179">Etapa 6-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="d11a1-179">Step 6 - Navigation events</span></span>  

<span data-ttu-id="d11a1-180">O aplicativo que hospeda os controles WebView2 ouve os eventos a seguir que são gerados pelo controle WebView2 durante a navegação em páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="d11a1-180">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="d11a1-181">Para obter mais informações, consulte [eventos de navegação](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="d11a1-181">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Gerenciar pacotes NuGet":::
   <span data-ttu-id="d11a1-183">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="d11a1-183">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="d11a1-184">Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="d11a1-184">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="d11a1-185">Quando há um redirecionamento HTTP, há vários `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="d11a1-185">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="d11a1-186">Para demonstrar como usar esses eventos, comece registrando um manipulador para `NavigationStarting` que cancele todas as solicitações que não usam https.</span><span class="sxs-lookup"><span data-stu-id="d11a1-186">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="d11a1-187">Em `Form1.cs` , modifique o Construtor conforme mostrado abaixo e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="d11a1-187">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="d11a1-188">No construtor, EnsureHttps é registrado como o manipulador de eventos no `NavigationStarting` evento no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="d11a1-188">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="d11a1-189">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-189">Select `F5` to build and run your project.</span></span> <span data-ttu-id="d11a1-190">Confirme que, ao navegar para um site HTTP, a WebView permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="d11a1-190">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="d11a1-191">No entanto, o WebView vai navegar para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d11a1-191">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="d11a1-192">Etapa 7-scripting</span><span class="sxs-lookup"><span data-stu-id="d11a1-192">Step 7 - Scripting</span></span>  

<span data-ttu-id="d11a1-193">Você pode usar aplicativos de host para injetar código JavaScript em controles WebView2 em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d11a1-193">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="d11a1-194">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a quaisquer quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="d11a1-194">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="d11a1-195">O JavaScript injetado é executado após a criação do objeto global e antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="d11a1-195">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="d11a1-196">Você pode usar o script para alertar o usuário ao navegar para um site que não seja HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d11a1-196">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="d11a1-197">Modifique a `EnsureHttps` função para que ela Insira o script no conteúdo da Web usando o método [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="d11a1-197">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="d11a1-198">Selecione `F5` para compilar e executar o projeto.</span><span class="sxs-lookup"><span data-stu-id="d11a1-198">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="d11a1-199">Confirme se o aplicativo exibe um alerta ao navegar para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d11a1-199">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="d11a1-201">Etapa 8 – comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="d11a1-201">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="d11a1-202">O conteúdo do host e da Web pode se comunicar uns com os outros usando `postMessage` o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="d11a1-202">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="d11a1-203">Conteúdo da Web em um controle WebView2 pode postar uma mensagem para o host usando `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-203">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="d11a1-204">O host manipula a mensagem usando qualquer registro registrado `WebMessageReceived` no host.</span><span class="sxs-lookup"><span data-stu-id="d11a1-204">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="d11a1-205">Hospeda mensagens postadas em conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-205">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="d11a1-206">Essas mensagens são detectadas pelos manipuladores adicionados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-206">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="d11a1-207">Esse mecanismo de comunicação permite que o conteúdo da Web passe mensagens para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="d11a1-207">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="d11a1-208">Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="d11a1-208">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="d11a1-209">No **Form1.cs**, atualize o construtor e crie uma `InitializeAsync` função conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d11a1-209">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="d11a1-210">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async]() porque a inicialização `CoreWebView2` é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d11a1-210">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1. <span data-ttu-id="d11a1-211">Após a inicialização do **CoreWebView2** , registre um manipulador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-211">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="d11a1-212">Em `Form1.cs` Atualizar `InitializeAsync` e adicionar `UpdateAddressBar` usando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d11a1-212">In `Form1.cs` update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1. <span data-ttu-id="d11a1-213">Para que o WebView envie e responda à mensagem da Web, após a `CoreWebView2` inicialização, o host injeta um script no conteúdo da Web para:</span><span class="sxs-lookup"><span data-stu-id="d11a1-213">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="d11a1-214">Envie a URL para o host usando `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="d11a1-214">Send the URL to the host using `postMessage`.</span></span>
    1. <span data-ttu-id="d11a1-215">Registre um manipulador de eventos para imprimir uma mensagem enviada do host.</span><span class="sxs-lookup"><span data-stu-id="d11a1-215">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="d11a1-216">Em `Form1.cs` , atualize `InitializeAsync` conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d11a1-216">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="d11a1-217">Selecione `F5` para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d11a1-217">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="d11a1-218">Confirme se a barra de endereços exibe a URL do site exibida no WebView.</span><span class="sxs-lookup"><span data-stu-id="d11a1-218">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="d11a1-219">Além disso, quando você navegar com êxito para uma nova URL, o WebView alertará o usuário da URL exibida na WebView.</span><span class="sxs-lookup"><span data-stu-id="d11a1-219">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="d11a1-221">Parabéns, você criou seu primeiro aplicativo WebView2!</span><span class="sxs-lookup"><span data-stu-id="d11a1-221">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="d11a1-222">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d11a1-222">Next steps</span></span> 

* <span data-ttu-id="d11a1-223">Fazer check-out do [repositório WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) para obter um exemplo abrangente de recursos do WebView2's</span><span class="sxs-lookup"><span data-stu-id="d11a1-223">Checkout the [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) for a comprehensive example of WebView2's capabilities</span></span>
* <span data-ttu-id="d11a1-224">[Referência de API](/dotnet/api/microsoft.web.webview2.winformswebview2) de check-out para obter informações mais detalhadas sobre nossas APIs</span><span class="sxs-lookup"><span data-stu-id="d11a1-224">Checkout [API reference](/dotnet/api/microsoft.web.webview2.winformswebview2) for more detailed information about our APIs</span></span>
* <span data-ttu-id="d11a1-225">Fazer check-out de uma lista de [recursos do WebView2](../index.md#next-steps) para saber mais sobre o WebView2</span><span class="sxs-lookup"><span data-stu-id="d11a1-225">Checkout a list of [WebView2 Resources](../index.md#next-steps) to learn more about WebView2</span></span>


## <span data-ttu-id="d11a1-226">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="d11a1-226">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  
