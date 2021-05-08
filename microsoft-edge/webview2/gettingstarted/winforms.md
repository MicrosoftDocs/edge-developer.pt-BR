---
description: Guia de início com WebView2 para aplicativos WinForms
title: Iniciando com WebView2 para aplicativos WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicativos winforms, winforms, edge, CoreWebView2, controle do navegador, html de borda, como começar, Como começar, .NET, formulários do Windows
ms.openlocfilehash: 408d225c6c0abe54483226e7004a386d367d65ab
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536263"
---
# <a name="getting-started-with-webview2-in-windows-forms"></a><span data-ttu-id="7cce8-104">Como começar com o WebView2 no Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7cce8-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="7cce8-105">Neste artigo, você pode começar a criar seu primeiro aplicativo WebView2 e saber mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="7cce8-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="7cce8-106">Para obter mais informações sobre APIs individuais, navegue até [referência de API][DotnetApiMicrosoftWebWebview2Winforms].</span><span class="sxs-lookup"><span data-stu-id="7cce8-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Winforms].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="7cce8-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7cce8-107">Prerequisites</span></span>  

<span data-ttu-id="7cce8-108">Certifique-se de instalar a lista de pré-requisitos a seguir antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="7cce8-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="7cce8-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] ou qualquer canal Microsoft Edge [(Chromium)][MicrosoftedgeinsiderDownload] não estável instalado no sistema operacional com suporte \(atualmente Windows 10, Windows 8.1 e Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="7cce8-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7cce8-110">A equipe webView recomenda o uso do canal Canary e a versão mínima necessária é 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="7cce8-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="7cce8-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7cce8-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="7cce8-112">Atualmente, o WebView2 não dá suporte aos designers .NET 5 e .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7cce8-112">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>  

## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="7cce8-113">Etapa 1 - Criar um aplicativo de janela única</span><span class="sxs-lookup"><span data-stu-id="7cce8-113">Step 1 - Create a single-window app</span></span>

<span data-ttu-id="7cce8-114">Comece com um projeto de área de trabalho básico que contém uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="7cce8-114">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="7cce8-115">Em Visual Studio, escolha **Windows Formulários .NET Framework App**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="7cce8-115">In Visual Studio, choose **Windows Forms .NET Framework App** > **Next**.</span></span>
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Novo projeto" lightbox="./media/winforms-newproject.png":::
       <span data-ttu-id="7cce8-117">Novo projeto</span><span class="sxs-lookup"><span data-stu-id="7cce8-117">New project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="7cce8-118">Insira valores para **Project nome e** **Local.**</span><span class="sxs-lookup"><span data-stu-id="7cce8-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="7cce8-119">Escolha **.NET Framework 4.6.2** ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7cce8-119">Choose **.NET Framework 4.6.2** or later.</span></span>  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Iniciar projeto" lightbox="./media/winforms-startproj.png":::
       <span data-ttu-id="7cce8-121">Iniciar projeto</span><span class="sxs-lookup"><span data-stu-id="7cce8-121">Start project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="7cce8-122">Para criar seu projeto, escolha **Criar**.</span><span class="sxs-lookup"><span data-stu-id="7cce8-122">To create your project, choose **Create**.</span></span>
    
## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="7cce8-123">Etapa 2 - Instalar o SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="7cce8-123">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="7cce8-124">Use NuGet para adicionar o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="7cce8-124">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="7cce8-125">Passe o mouse no projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Gerenciar NuGet Pacotes...**.</span><span class="sxs-lookup"><span data-stu-id="7cce8-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gerenciar NuGet pacotes":::
       <span data-ttu-id="7cce8-127">Gerenciar NuGet pacotes</span><span class="sxs-lookup"><span data-stu-id="7cce8-127">Manage NuGet Packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="7cce8-128">Na barra de pesquisa, digite `Microsoft.Web.WebView2` > escolha **Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="7cce8-128">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="7cce8-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="7cce8-130">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="7cce8-131">Comece a desenvolver aplicativos usando a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cce8-131">Start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="7cce8-132">Para criar e executar o projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-132">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="7cce8-133">O projeto em execução exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="7cce8-133">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Aplicativo vazio" lightbox="./media/winforms-emptyapp.png":::
       <span data-ttu-id="7cce8-135">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="7cce8-135">Empty app</span></span>  
    :::image-end:::
    
## <a name="step-3---create-a-single-webview"></a><span data-ttu-id="7cce8-136">Etapa 3 - Criar um único WebView</span><span class="sxs-lookup"><span data-stu-id="7cce8-136">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="7cce8-137">Adicione um WebView ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7cce8-137">Add a WebView to your app.</span></span>  

1.  <span data-ttu-id="7cce8-138">Abra o **Windows Designer de Formulários.**</span><span class="sxs-lookup"><span data-stu-id="7cce8-138">Open the **Windows Forms Designer**.</span></span>  
1.  <span data-ttu-id="7cce8-139">**Pesquise WebView2** na **Caixa de Ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="7cce8-139">Search for **WebView2** in the **Toolbox**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7cce8-140">Se você estiver usando Visual Studio 2017, por padrão **WebView2** pode não ser exibido na **Caixa de Ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="7cce8-140">If you are using Visual Studio 2017, by default **WebView2** may not display in the **Toolbox**.</span></span>  <span data-ttu-id="7cce8-141">Para habilitar o comportamento, escolha **Opções**de Ferramentas  >  \*\*\*\*  >  **Gerais** > definir a configuração **Preencher Automaticamente a Caixa** de Ferramentas como `True` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-141">To enable the behavior, choose **Tools** > **Options** > **General** > set the **Automatically Populate Toolbox** setting to `True`.</span></span>  
    
    <span data-ttu-id="7cce8-142">Arraste e solte o **controle WebView2** no aplicativo Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="7cce8-142">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Caixa de ferramentas exibindo WebView2":::
       <span data-ttu-id="7cce8-144">Caixa de ferramentas exibindo WebView2</span><span class="sxs-lookup"><span data-stu-id="7cce8-144">Toolbox displaying WebView2</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="7cce8-145">De definir `(Name)` a propriedade como `webView` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-145">Set the `(Name)` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propriedades do controle WebView2":::
       <span data-ttu-id="7cce8-147">Propriedades do controle WebView2</span><span class="sxs-lookup"><span data-stu-id="7cce8-147">Properties of the WebView2 control</span></span>
    :::image-end:::

1.  <span data-ttu-id="7cce8-148">A `Source` propriedade define o URI inicial exibido no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cce8-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  <span data-ttu-id="7cce8-149">De definir `Source` a propriedade como `https://www.microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-149">Set the `Source` property to `https://www.microsoft.com`.</span></span>  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="A propriedade Source do controle WebView2":::
       <span data-ttu-id="7cce8-151">A **propriedade Source** do controle WebView2</span><span class="sxs-lookup"><span data-stu-id="7cce8-151">The **Source** property of the WebView2 control</span></span>
    :::image-end:::  

<span data-ttu-id="7cce8-152">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-152">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="7cce8-153">Certifique-se de que seu controle WebView2 seja [https://www.microsoft.com][|::ref1::|Main] exibido.</span><span class="sxs-lookup"><span data-stu-id="7cce8-153">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="Hello webview" lightbox="./media/winforms-hellowebview.png":::
   <span data-ttu-id="7cce8-155">Hello webview</span><span class="sxs-lookup"><span data-stu-id="7cce8-155">hello webview</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7cce8-156">Se você estiver trabalhando em um monitor DPI alto, talvez seja necessário configurar seu aplicativo Windows Forms para alto [suporte a DPI.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]</span><span class="sxs-lookup"><span data-stu-id="7cce8-156">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport].</span></span>  

## <a name="step-4---handle-window-resize-events"></a><span data-ttu-id="7cce8-157">Etapa 4 - Manipular eventos de resize de janela</span><span class="sxs-lookup"><span data-stu-id="7cce8-157">Step 4 - Handle Window Resize Events</span></span>  

<span data-ttu-id="7cce8-158">Adicione mais alguns controles ao seu Windows Formulários da caixa de ferramentas e, em seguida, manipular eventos de resize da janela adequadamente.</span><span class="sxs-lookup"><span data-stu-id="7cce8-158">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>  

1.  <span data-ttu-id="7cce8-159">No Windows **Designer de Formulários,** abra a **Caixa de Ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="7cce8-159">In the **Windows Forms Designer**, open the **Toolbox**.</span></span>  
1.  <span data-ttu-id="7cce8-160">Arraste e solte uma **TextBox** no aplicativo Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="7cce8-160">Drag and Drop a **TextBox** into the Windows Forms App.</span></span>  <span data-ttu-id="7cce8-161">Nomeia **TextBox** `addressBar` na guia **Propriedades.**</span><span class="sxs-lookup"><span data-stu-id="7cce8-161">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>  
1.  <span data-ttu-id="7cce8-162">Arraste e solte um **botão** no aplicativo Windows Formulários.</span><span class="sxs-lookup"><span data-stu-id="7cce8-162">Drag and Drop a **Button** into the Windows Forms App.</span></span>  <span data-ttu-id="7cce8-163">Altere o texto no **botão** para `Go!` e nomee o **botão** na `goButton` guia **Propriedades.**</span><span class="sxs-lookup"><span data-stu-id="7cce8-163">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>  
    
    <span data-ttu-id="7cce8-164">O aplicativo deve ter a aparência da imagem a seguir no designer.</span><span class="sxs-lookup"><span data-stu-id="7cce8-164">The app should look like the following image in the designer.</span></span>  
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="Designer WinForms" lightbox="./media/winforms-designer.png":::
       <span data-ttu-id="7cce8-166">Designer WinForms</span><span class="sxs-lookup"><span data-stu-id="7cce8-166">WinForms designer</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="7cce8-167">No `Form1.cs` arquivo, defina para manter os controles no local quando a Janela do `Form_Resize` Aplicativo for resized.</span><span class="sxs-lookup"><span data-stu-id="7cce8-167">In the `Form1.cs` file, define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="7cce8-168">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-168">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="7cce8-169">Verifique se o aplicativo é exibido de forma semelhante à captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cce8-169">Ensure the app displays similar to the following screenshot.</span></span>

:::image type="complex" source="./media/winforms-app.png" alt-text="aplicativo" lightbox="./media/winforms-app.png":::
   <span data-ttu-id="7cce8-171">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="7cce8-171">App</span></span>  
:::image-end:::

## <a name="step-5---navigation"></a><span data-ttu-id="7cce8-172">Etapa 5 - Navegação</span><span class="sxs-lookup"><span data-stu-id="7cce8-172">Step 5 - Navigation</span></span>

<span data-ttu-id="7cce8-173">Adicione a capacidade de permitir que os usuários alterem a URL exibida pelo controle WebView2 adicionando uma barra de endereços ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7cce8-173">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>  

1.  <span data-ttu-id="7cce8-174">Selecione `F5` para criar e executar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="7cce8-174">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="7cce8-175">Confirme se o aplicativo exibe semelhante à captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cce8-175">Confirm that the app displays similar to the following screenshot.</span></span>  
    
    :::image type="complex" source="./media/winforms-app.png" alt-text="Aplicativo WinForms" lightbox="./media/winforms-app.png":::
       <span data-ttu-id="7cce8-177">Aplicativo WinForms</span><span class="sxs-lookup"><span data-stu-id="7cce8-177">WinForms App</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7cce8-178">No `Form1.cs` arquivo, para adicionar o `CoreWebView2` namespace, insira o seguinte trecho de código na parte superior.</span><span class="sxs-lookup"><span data-stu-id="7cce8-178">In the `Form1.cs`file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  

1.  <span data-ttu-id="7cce8-179">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-179">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  <span data-ttu-id="7cce8-180">No Windows Designer de **Formulários,** clique duas vezes no `Go!` botão para criar o método no `goButton_Click` `Form1.cs` arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cce8-180">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in the `Form1.cs` file.</span></span>  <span data-ttu-id="7cce8-181">Copie e colar o trecho a seguir dentro da função.</span><span class="sxs-lookup"><span data-stu-id="7cce8-181">Copy and paste the following snippet inside the function.</span></span>  <span data-ttu-id="7cce8-182">Agora, a `goButton_Click` função navega pelo WebView até a URL inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="7cce8-182">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="7cce8-183">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-183">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="7cce8-184">Insira uma nova URL na barra de endereços e selecione **Ir**.</span><span class="sxs-lookup"><span data-stu-id="7cce8-184">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="7cce8-185">Por exemplo, digite `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-185">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="7cce8-186">Verifique se o controle WebView2 navega até a URL.</span><span class="sxs-lookup"><span data-stu-id="7cce8-186">Ensure the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="7cce8-187">Verifique se uma URL completa é inserida na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="7cce8-187">Ensure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="7cce8-188">Um `ArgumentException` é lançado se a URL não começar com `http://` ou</span><span class="sxs-lookup"><span data-stu-id="7cce8-188">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   <span data-ttu-id="7cce8-190">bing.com</span><span class="sxs-lookup"><span data-stu-id="7cce8-190">bing.com</span></span>  
:::image-end:::

## <a name="step-6---navigation-events"></a><span data-ttu-id="7cce8-191">Etapa 6 - Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="7cce8-191">Step 6 - Navigation events</span></span>  

<span data-ttu-id="7cce8-192">Durante a navegação na página da Web, o controle WebView2 gera eventos.</span><span class="sxs-lookup"><span data-stu-id="7cce8-192">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="7cce8-193">O aplicativo que hospeda controles WebView2 escuta os seguintes eventos.</span><span class="sxs-lookup"><span data-stu-id="7cce8-193">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="7cce8-194">Para obter mais informações, navegue até [Eventos de Navegação][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="7cce8-194">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   <span data-ttu-id="7cce8-196">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="7cce8-196">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="7cce8-197">Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página da Web de erro.</span><span class="sxs-lookup"><span data-stu-id="7cce8-197">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="7cce8-198">Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="7cce8-198">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="7cce8-199">Para demonstrar como usar os eventos, comece registrando um manipulador para que cancele todas as `NavigationStarting` solicitações que não usam HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7cce8-199">To demonstrate how to use the events, start by registering a handler for `NavigationStarting` that cancels any requests not using HTTPS.</span></span>  

<span data-ttu-id="7cce8-200">No `Form1.cs` arquivo, atualize o construtor para corresponder ao trecho de código a seguir e adicione a `EnsureHttps` função.</span><span class="sxs-lookup"><span data-stu-id="7cce8-200">In the `Form1.cs` file, update the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="7cce8-201">No construtor, é `EnsureHttps` registrado como o manipulador de eventos no evento no controle `NavigationStarting` WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cce8-201">In the constructor, `EnsureHttps` is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="7cce8-202">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-202">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="7cce8-203">Verifique se ao navegar para um site HTTP, o WebView permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="7cce8-203">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="7cce8-204">No entanto, o WebView navegará até sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7cce8-204">However, the WebView will navigate to HTTPS sites.</span></span>

## <a name="step-7---scripting"></a><span data-ttu-id="7cce8-205">Etapa 7 - Scripting</span><span class="sxs-lookup"><span data-stu-id="7cce8-205">Step 7 - Scripting</span></span>  

<span data-ttu-id="7cce8-206">Você pode usar aplicativos host para injetar código JavaScript em controles WebView2 no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7cce8-206">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="7cce8-207">Você pode tarefa webView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="7cce8-207">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="7cce8-208">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="7cce8-208">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="7cce8-209">O JavaScript injetado é executado com tempo específico.</span><span class="sxs-lookup"><span data-stu-id="7cce8-209">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="7cce8-210">Execute-o após a criação do objeto global.</span><span class="sxs-lookup"><span data-stu-id="7cce8-210">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="7cce8-211">Execute-o antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="7cce8-211">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="7cce8-212">Como exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7cce8-212">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="7cce8-213">Modifique `EnsureHttps` a função para injetar um script no conteúdo da Web que usa o método [ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]</span><span class="sxs-lookup"><span data-stu-id="7cce8-213">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] method.</span></span>  

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

<span data-ttu-id="7cce8-214">Para criar e executar seu projeto, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-214">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="7cce8-215">Verifique se o aplicativo exibe um alerta quando você navega até um site que não usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7cce8-215">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   <span data-ttu-id="7cce8-217">https</span><span class="sxs-lookup"><span data-stu-id="7cce8-217">https</span></span>  
:::image-end:::

## <a name="step-8---communication-between-host-and-web-content"></a><span data-ttu-id="7cce8-218">Etapa 8 - Comunicação entre conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="7cce8-218">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="7cce8-219">O conteúdo do host e da Web pode ser `postMessage` usado para se comunicar uns com os outros da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7cce8-219">The host and web content may use `postMessage` to communicate with each other as follows:</span></span>  

*   <span data-ttu-id="7cce8-220">O conteúdo da Web em um controle WebView2 pode ser usado `window.chrome.webview.postMessage` para postar uma mensagem no host.</span><span class="sxs-lookup"><span data-stu-id="7cce8-220">Web content in a WebView2 control may use `window.chrome.webview.postMessage` to post a message to the host.</span></span>  <span data-ttu-id="7cce8-221">O host lida com a mensagem usando qualquer `WebMessageReceived` registro no host.</span><span class="sxs-lookup"><span data-stu-id="7cce8-221">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="7cce8-222">Hosts postam mensagens no conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-222">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="7cce8-223">Essas mensagens são capturadas por manipuladores adicionados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-223">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="7cce8-224">O mecanismo de comunicação passa mensagens do conteúdo da Web para o host usando recursos nativos.</span><span class="sxs-lookup"><span data-stu-id="7cce8-224">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="7cce8-225">Em seu projeto, quando o controle WebView2 navega até uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cce8-225">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="7cce8-226">No `Form1.cs` arquivo, atualize o construtor e crie uma `InitializeAsync` função para corresponder ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cce8-226">In the `Form1.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="7cce8-227">A `InitializeAsync` função aguarda [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] porque a inicialização `CoreWebView2` de é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7cce8-227">The `InitializeAsync` function awaits [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1.  <span data-ttu-id="7cce8-228">Depois `CoreWebView2` de inicializado, registre um manipulador de eventos para responder `WebMessageReceived` a .</span><span class="sxs-lookup"><span data-stu-id="7cce8-228">After `CoreWebView2` is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="7cce8-229">No `Form1.cs` arquivo, atualize `InitializeAsync` e adicione usando o seguinte trecho de `UpdateAddressBar` código.</span><span class="sxs-lookup"><span data-stu-id="7cce8-229">In the `Form1.cs` file, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1.  <span data-ttu-id="7cce8-230">Para que o WebView envie e responda à mensagem da Web, depois de inicializado, o host injeta um script no conteúdo `CoreWebView2` da Web para:</span><span class="sxs-lookup"><span data-stu-id="7cce8-230">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1.  <span data-ttu-id="7cce8-231">Envie a URL para o host usando `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-231">Send the URL to the host using `postMessage`.</span></span>
    1.  <span data-ttu-id="7cce8-232">Registre um manipulador de eventos para imprimir uma mensagem enviada do host.</span><span class="sxs-lookup"><span data-stu-id="7cce8-232">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="7cce8-233">No `Form1.cs` arquivo, atualize `InitializeAsync` para corresponder ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cce8-233">In the `Form1.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="7cce8-234">Para criar e executar o aplicativo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="7cce8-234">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="7cce8-235">Agora, a barra de endereços exibe o URI no controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cce8-235">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="7cce8-236">Além disso, quando você navega com êxito para uma nova URL, o WebView alerta o usuário da URL exibida no WebView.</span><span class="sxs-lookup"><span data-stu-id="7cce8-236">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Aplicativo final" lightbox="./media/winforms-finalapp.png":::
   <span data-ttu-id="7cce8-238">Aplicativo final</span><span class="sxs-lookup"><span data-stu-id="7cce8-238">Final app</span></span>  
:::image-end:::

<span data-ttu-id="7cce8-239">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="7cce8-239">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="7cce8-240">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="7cce8-240">Next steps</span></span>  

<span data-ttu-id="7cce8-241">Para continuar a aprender mais sobre WebView2, navegue até os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="7cce8-241">To continue learning more about WebView2, navigate to the following resources.</span></span>  

*   <span data-ttu-id="7cce8-242">Para saber mais sobre como criar aplicativos WebView2, navegue até Práticas recomendadas de desenvolvimento [webView2.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="7cce8-242">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="7cce8-243">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="7cce8-243">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="7cce8-244">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="7cce8-244">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
*   <span data-ttu-id="7cce8-245">Para obter informações detalhadas sobre a API WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span><span class="sxs-lookup"><span data-stu-id="7cce8-245">For detailed information about the WebView2 API, navigate to [API reference][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="7cce8-246">Entrar em contato com a equipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="7cce8-246">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Práticas recomendadas de desenvolvimento do WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "WebView2 Class | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Configurando seu aplicativo Windows Forms para alto suporte a DPI - Suporte a DPI alto no Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 | Microsoft Edge Desenvolvedor"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
