---
description: Guia de iniciação com WebView2 para aplicativos WinForms
title: Getting started with WebView2 for WinForms apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicativos winforms, winforms, edge, CoreWebView2, controle de navegador, html de borda, getting started, Getting Started, .NET, windows forms
ms.openlocfilehash: 45a3b59733a57975e373df2e21258198645be2d4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306163"
---
# <span data-ttu-id="9ebbf-104">Getting started with WebView2 in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9ebbf-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="9ebbf-105">Neste artigo, aprenda a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="9ebbf-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="9ebbf-106">Para obter mais informações sobre APIs individuais, navegue até a [referência de API.][DotnetApiMicrosoftWebWebview2Winforms]</span><span class="sxs-lookup"><span data-stu-id="9ebbf-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Winforms].</span></span>  

## <span data-ttu-id="9ebbf-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9ebbf-107">Prerequisites</span></span>  

<span data-ttu-id="9ebbf-108">Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="9ebbf-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no sistema operacional suportado \(atualmente Windows 10, Windows 8.1 e Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="9ebbf-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9ebbf-110">A equipe WebView recomenda usar o canal Canary e a versão mínima necessária é 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="9ebbf-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="9ebbf-112">No momento, o WebView2 não dá suporte aos designers do .NET 5 e do .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-112">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>

## <span data-ttu-id="9ebbf-113">Etapa 1: criar um aplicativo de janela única</span><span class="sxs-lookup"><span data-stu-id="9ebbf-113">Step 1 - Create a single-window app</span></span>

<span data-ttu-id="9ebbf-114">Comece com um projeto de área de trabalho básico que contenha uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-114">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="9ebbf-115">No Visual Studio, escolha **Windows Forms .NET Framework App**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-115">In Visual Studio, choose **Windows Forms .NET Framework App** > **Next**.</span></span>
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Novo projeto" lightbox="./media/winforms-newproject.png":::
       <span data-ttu-id="9ebbf-117">Novo projeto</span><span class="sxs-lookup"><span data-stu-id="9ebbf-117">New project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="9ebbf-118">Insira valores para **o nome do projeto** e o **local.**</span><span class="sxs-lookup"><span data-stu-id="9ebbf-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="9ebbf-119">Escolha **o .NET Framework 4.6.2** ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-119">Choose **.NET Framework 4.6.2** or later.</span></span>  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Iniciar projeto" lightbox="./media/winforms-startproj.png":::
       <span data-ttu-id="9ebbf-121">Iniciar projeto</span><span class="sxs-lookup"><span data-stu-id="9ebbf-121">Start project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="9ebbf-122">Para criar seu projeto, escolha **Criar**.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-122">To create your project, choose **Create**.</span></span>
    
## <span data-ttu-id="9ebbf-123">Etapa 2 - Instalar o SDK webView2</span><span class="sxs-lookup"><span data-stu-id="9ebbf-123">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="9ebbf-124">Use NuGet para adicionar o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-124">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="9ebbf-125">Passe o mouse sobre o projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Gerenciar Pacotes NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gerenciar pacotes NuGet":::
       <span data-ttu-id="9ebbf-127">Gerenciar pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="9ebbf-127">Manage NuGet Packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="9ebbf-128">Na barra de pesquisa, digite > `Microsoft.Web.WebView2` escolha **Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-128">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="9ebbf-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="9ebbf-130">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="9ebbf-131">Comece a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-131">Start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="9ebbf-132">Para criar e executar o projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-132">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="9ebbf-133">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-133">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Aplicativo vazio" lightbox="./media/winforms-emptyapp.png":::
       <span data-ttu-id="9ebbf-135">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="9ebbf-135">Empty app</span></span>  
    :::image-end:::
    
## <span data-ttu-id="9ebbf-136">Etapa 3 - Criar um único WebView</span><span class="sxs-lookup"><span data-stu-id="9ebbf-136">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="9ebbf-137">Adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-137">Add a WebView to your app.</span></span>  

1.  <span data-ttu-id="9ebbf-138">Abra o **Designer de Formulários do Windows.**</span><span class="sxs-lookup"><span data-stu-id="9ebbf-138">Open the **Windows Forms Designer**.</span></span>  
1.  <span data-ttu-id="9ebbf-139">Pesquise **WebView2** na **Caixa de Ferramentas.**</span><span class="sxs-lookup"><span data-stu-id="9ebbf-139">Search for **WebView2** in the **Toolbox**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9ebbf-140">Se você estiver usando o Visual Studio 2017, por padrão **WebView2** pode não ser exibido na Caixa **de Ferramentas.**</span><span class="sxs-lookup"><span data-stu-id="9ebbf-140">If you are using Visual Studio 2017, by default **WebView2** may not display in the **Toolbox**.</span></span>  <span data-ttu-id="9ebbf-141">Para habilitar o comportamento, escolha **Opções**de Ferramentas Gerais > definir a configuração Preencher  >  \*\*\*\*  >  \*\*\*\* **Automaticamente a Caixa de** Ferramentas como `True` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-141">To enable the behavior, choose **Tools** > **Options** > **General** > set the **Automatically Populate Toolbox** setting to `True`.</span></span>  
    
    <span data-ttu-id="9ebbf-142">Arraste e solte o **controle WebView2** no Aplicativo de Formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-142">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Caixa de ferramentas exibindo WebView2":::
       <span data-ttu-id="9ebbf-144">Caixa de ferramentas exibindo WebView2</span><span class="sxs-lookup"><span data-stu-id="9ebbf-144">Toolbox displaying WebView2</span></span>
    :::image-end:::  

1.  <span data-ttu-id="9ebbf-145">Definir a `(Name)` propriedade como `webView` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-145">Set the `(Name)` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propriedades do controle WebView2":::
       <span data-ttu-id="9ebbf-147">Propriedades do controle WebView2</span><span class="sxs-lookup"><span data-stu-id="9ebbf-147">Properties of the WebView2 control</span></span>
    :::image-end:::

1.  <span data-ttu-id="9ebbf-148">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  <span data-ttu-id="9ebbf-149">Definir a `Source` propriedade como `https://www.microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-149">Set the `Source` property to `https://www.microsoft.com`.</span></span>  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="A propriedade Source do controle WebView2":::
       <span data-ttu-id="9ebbf-151">A **propriedade Source** do controle WebView2</span><span class="sxs-lookup"><span data-stu-id="9ebbf-151">The **Source** property of the WebView2 control</span></span>
    :::image-end:::  

<span data-ttu-id="9ebbf-152">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-152">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="9ebbf-153">Verifique se o controle WebView2 é [https://www.microsoft.com][|::ref1::|Main] exibido.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-153">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   <span data-ttu-id="9ebbf-155">hello webview</span><span class="sxs-lookup"><span data-stu-id="9ebbf-155">hello webview</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9ebbf-156">Se você estiver trabalhando em um monitor DPI alto, talvez seja necessário configurar seu aplicativo [Windows Forms para suporte a DPI alto.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]</span><span class="sxs-lookup"><span data-stu-id="9ebbf-156">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport].</span></span>  

## <span data-ttu-id="9ebbf-157">Etapa 4 - Manipular eventos de resize da janela</span><span class="sxs-lookup"><span data-stu-id="9ebbf-157">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="9ebbf-158">Adicione mais alguns controles ao Windows Forms na caixa de ferramentas e, em seguida, manipular eventos de resize da janela adequadamente.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-158">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1.  <span data-ttu-id="9ebbf-159">No **Designer de Formulários do Windows,** abra a **Caixa de Ferramentas**</span><span class="sxs-lookup"><span data-stu-id="9ebbf-159">In the **Windows Forms Designer**, open the **Toolbox**</span></span>
1.  <span data-ttu-id="9ebbf-160">Arraste e solte um **TextBox no** Aplicativo de Formulários do Windows.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-160">Drag and drop a **TextBox** into the Windows Forms App.</span></span>  <span data-ttu-id="9ebbf-161">In the **Properties Tab**, name the **TextBox** `addressBar` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-161">In the **Properties Tab**, name the **TextBox** `addressBar` .</span></span>
1.  <span data-ttu-id="9ebbf-162">Arraste e solte um **botão no** aplicativo Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-162">Drag and drop a **Button** into the Windows Forms App.</span></span>  <span data-ttu-id="9ebbf-163">Altere o texto no **botão para** e nome `Go!` do **botão** na `goButton` guia **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-163">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="9ebbf-164">O aplicativo deve se parecer com a imagem a seguir no designer.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-164">The app should look like the following image in the designer.</span></span>
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="designer" lightbox="./media/winforms-designer.png":::
       <span data-ttu-id="9ebbf-166">designer</span><span class="sxs-lookup"><span data-stu-id="9ebbf-166">designer</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="9ebbf-167">No `Form1.cs` arquivo, defina `Form_Resize` para manter os controles no local quando a Janela do Aplicativo for resized.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-167">In the `Form1.cs` file, define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="9ebbf-168">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-168">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="9ebbf-169">Certifique-se de que o aplicativo seja exibido de forma semelhante à captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-169">Ensure the app displays similar to the following screenshot.</span></span>

:::image type="complex" source="./media/winforms-app.png" alt-text="aplicativo" lightbox="./media/winforms-app.png":::
   <span data-ttu-id="9ebbf-171">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="9ebbf-171">App</span></span>  
:::image-end:::

## <span data-ttu-id="9ebbf-172">Etapa 5 - Navegação</span><span class="sxs-lookup"><span data-stu-id="9ebbf-172">Step 5 - Navigation</span></span>

<span data-ttu-id="9ebbf-173">Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe adicionando uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-173">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="9ebbf-174">No `Form1.cs` arquivo, para adicionar o namespace, insira o trecho de código a `CoreWebView2` seguir na parte superior.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-174">In the `Form1.cs`file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  <span data-ttu-id="9ebbf-175">In the **Windows Forms Designer**, double-click on the button to create the method in the `Go!` `goButton_Click` `Form1.cs` file.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-175">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in the `Form1.cs` file.</span></span>  <span data-ttu-id="9ebbf-176">Copie e copie e copie o seguinte trecho de código dentro da função.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-176">Copy and paste the following snippet inside the function.</span></span>  <span data-ttu-id="9ebbf-177">Agora, a `goButton_Click` função navega pelo WebView até a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-177">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="9ebbf-178">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-178">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="9ebbf-179">Insira uma nova URL na barra de endereços e selecione **Ir.**</span><span class="sxs-lookup"><span data-stu-id="9ebbf-179">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="9ebbf-180">Por exemplo, insira `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-180">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="9ebbf-181">Certifique-se de que o controle WebView2 navegue até a URL.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-181">Ensure the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="9ebbf-182">Certifique-se de que uma URL completa seja inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-182">Ensure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="9ebbf-183">Um `ArgumentException` é lançado se a URL não começa com `http://` ou</span><span class="sxs-lookup"><span data-stu-id="9ebbf-183">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   <span data-ttu-id="9ebbf-185">bing.com</span><span class="sxs-lookup"><span data-stu-id="9ebbf-185">bing.com</span></span>  
:::image-end:::

## <span data-ttu-id="9ebbf-186">Etapa 6 - Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="9ebbf-186">Step 6 - Navigation events</span></span>  

<span data-ttu-id="9ebbf-187">Durante a navegação na página da Web, o controle WebView2 gera eventos.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-187">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="9ebbf-188">O aplicativo que hospeda controles WebView2 escuta os eventos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-188">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="9ebbf-189">Para obter mais informações, navegue até [Eventos de Navegação.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="9ebbf-189">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   <span data-ttu-id="9ebbf-191">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="9ebbf-191">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="9ebbf-192">Quando ocorre um erro, os eventos a seguir são gerados e podem depender da navegação para uma página da Web de erro.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-192">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="9ebbf-193">Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-193">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="9ebbf-194">Para demonstrar como usar esses eventos, comece registrando um manipulador para que cancele quaisquer solicitações que não `NavigationStarting` usem HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-194">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="9ebbf-195">No arquivo, atualize o construtor para corresponder ao trecho de código a seguir `Form1.cs` e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-195">In the `Form1.cs` file, update the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="9ebbf-196">No construtor, EnsureHttps é registrado como o manipulador de eventos `NavigationStarting` no evento no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-196">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="9ebbf-197">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-197">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="9ebbf-198">Certifique-se de que, ao navegar para um site HTTP, o WebView permaneça inalterado.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-198">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="9ebbf-199">No entanto, o WebView navegará para sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-199">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="9ebbf-200">Etapa 7 - Scripts</span><span class="sxs-lookup"><span data-stu-id="9ebbf-200">Step 7 - Scripting</span></span>  

<span data-ttu-id="9ebbf-201">Você pode usar aplicativos host para inserir código JavaScript em controles WebView2 no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-201">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="9ebbf-202">Você pode tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-202">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="9ebbf-203">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-203">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="9ebbf-204">O JavaScript injetado é executado com tempo específico.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-204">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="9ebbf-205">Execute-o após a criação do objeto global.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-205">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="9ebbf-206">Execute-o antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-206">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="9ebbf-207">Por exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-207">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="9ebbf-208">Modifique `EnsureHttps` a função para inserir um script no conteúdo da Web que usa o método [ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]</span><span class="sxs-lookup"><span data-stu-id="9ebbf-208">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] method.</span></span>  

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

<span data-ttu-id="9ebbf-209">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-209">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="9ebbf-210">Certifique-se de que o aplicativo exibe um alerta quando você navega para um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-210">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   <span data-ttu-id="9ebbf-212">https</span><span class="sxs-lookup"><span data-stu-id="9ebbf-212">https</span></span>  
:::image-end:::

## <span data-ttu-id="9ebbf-213">Etapa 8- Comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="9ebbf-213">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="9ebbf-214">O conteúdo do host e da Web pode `postMessage` ser usado para se comunicar uns com os outros da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9ebbf-214">The host and web content may use `postMessage` to communicate with each other as follows:</span></span>  

*   <span data-ttu-id="9ebbf-215">O conteúdo da Web em um controle WebView2 pode `window.chrome.webview.postMessage` ser usado para postar uma mensagem no host.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-215">Web content in a WebView2 control may use `window.chrome.webview.postMessage` to post a message to the host.</span></span>  <span data-ttu-id="9ebbf-216">O host lida com a mensagem usando qualquer `WebMessageReceived` registro no host.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-216">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="9ebbf-217">Hosts postam mensagens no conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-217">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="9ebbf-218">Essas mensagens são capturadas por manipuladores adicionados `window.chrome.webview.addEventListener` a .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-218">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="9ebbf-219">O mecanismo de comunicação passa mensagens do conteúdo da Web para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-219">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="9ebbf-220">Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-220">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="9ebbf-221">No `Form1.cs` arquivo, atualize o construtor e crie uma `InitializeAsync` função para corresponder ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-221">In the `Form1.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="9ebbf-222">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] porque a inicialização `CoreWebView2` é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-222">The `InitializeAsync` function awaits [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1.  <span data-ttu-id="9ebbf-223">Após `CoreWebView2` a inicialização, registre um manipulador de eventos para `WebMessageReceived` responder.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-223">After `CoreWebView2` is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="9ebbf-224">No `Form1.cs` arquivo, atualize `InitializeAsync` e adicione usando o trecho de código a `UpdateAddressBar` seguir.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-224">In the `Form1.cs` file, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1.  <span data-ttu-id="9ebbf-225">Para que o WebView envie e responda à mensagem da Web, depois de inicializado, o host injeta um script no conteúdo `CoreWebView2` da Web para:</span><span class="sxs-lookup"><span data-stu-id="9ebbf-225">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1.  <span data-ttu-id="9ebbf-226">Envie a URL para o host usando `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-226">Send the URL to the host using `postMessage`.</span></span>
    1.  <span data-ttu-id="9ebbf-227">Registre um manipulador de eventos para imprimir uma mensagem enviada do host.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-227">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="9ebbf-228">No `Form1.cs` arquivo, atualize `InitializeAsync` para corresponder ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-228">In the `Form1.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="9ebbf-229">Para criar e executar o aplicativo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="9ebbf-229">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="9ebbf-230">Agora, a barra de endereços exibe o URI no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-230">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="9ebbf-231">Além disso, quando você navega com êxito para uma nova URL, o WebView alerta o usuário da URL exibida no WebView.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-231">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Aplicativo final" lightbox="./media/winforms-finalapp.png":::
   <span data-ttu-id="9ebbf-233">Aplicativo final</span><span class="sxs-lookup"><span data-stu-id="9ebbf-233">Final app</span></span>  
:::image-end:::

<span data-ttu-id="9ebbf-234">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-234">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="9ebbf-235">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9ebbf-235">Next steps</span></span>  

<span data-ttu-id="9ebbf-236">Para continuar a saber mais sobre WebView2, navegue até os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="9ebbf-236">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="9ebbf-237">Ver também</span><span class="sxs-lookup"><span data-stu-id="9ebbf-237">See also</span></span>  

*   <span data-ttu-id="9ebbf-238">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="9ebbf-238">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="9ebbf-239">Para obter mais informações sobre WebView2, navegue até [Recursos de WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="9ebbf-239">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
*   <span data-ttu-id="9ebbf-240">Para obter informações detalhadas sobre a API WebView2, navegue até a [referência de API.][DotnetApiMicrosoftWebWebview2WinformsWebview2]</span><span class="sxs-lookup"><span data-stu-id="9ebbf-240">For detailed information about the WebView2 API, navigate to [API reference][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span></span>  

## <span data-ttu-id="9ebbf-241">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="9ebbf-241">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (visualização) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Classe WebView2 | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Configurando seu aplicativo do Windows Forms para suporte a alto DPI – suporte a DPI alto no Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desenvolvedor do Microsoft Edge"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  