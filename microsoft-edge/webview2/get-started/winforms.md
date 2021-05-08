---
description: Guia de início com WebView2 para aplicativos WinForms
title: Começar com WebView2 para aplicativos WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicativos winforms, winforms, edge, CoreWebView2, controle do navegador, html de borda, Introdução, .NET, formulários do windows
ms.openlocfilehash: 704e5732ddcff02e56f49bec37a5d1ad5f11c2b5
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535806"
---
# <a name="get-started-with-webview2-in-windows-forms"></a>Começar com WebView2 em Windows Forms

Neste artigo, você pode começar a criar seu primeiro aplicativo WebView2 e saber mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obter mais informações sobre APIs individuais, navegue até [referência de API][DotnetApiMicrosoftWebWebview2Winforms].  

## <a name="prerequisites"></a>Pré-requisitos  

Certifique-se de instalar a lista de pré-requisitos a seguir antes de prosseguir.  

*   [WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] ou qualquer canal Microsoft Edge [(Chromium)][MicrosoftedgeinsiderDownload] não estável instalado no sistema operacional com suporte \(atualmente Windows 10, Windows 8.1 e Windows 7\).  
    
    > [!NOTE]
    > A equipe webView recomenda o uso do canal Canary e a versão mínima necessária é 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 ou posterior.  
    
> [!NOTE]
> Atualmente, o WebView2 não dá suporte aos designers .NET 5 e .NET Core.  

## <a name="step-1---create-a-single-window-app"></a>Etapa 1 - Criar um aplicativo de janela única

Comece com um projeto de área de trabalho básico que contém uma única janela principal.  

1.  Em Visual Studio, escolha **Windows Formulários .NET Framework App**  >  **Next**.
    
    :::image type="complex" source="./media/winforms-new-project.png" alt-text="Novo projeto" lightbox="./media/winforms-new-project.png":::
       Novo projeto  
    :::image-end:::
    
1.  Insira valores para **Project nome e** **Local.**  Escolha **.NET Framework 4.6.2** ou posterior.  
    
    :::image type="complex" source="./media/winforms-start-proj.png" alt-text="Iniciar projeto" lightbox="./media/winforms-start-proj.png":::
       Iniciar projeto  
    :::image-end:::
    
1.  Para criar seu projeto, escolha **Criar**.
    
## <a name="step-2---install-webview2-sdk"></a>Etapa 2 - Instalar o SDK WebView2

Use NuGet para adicionar o SDK WebView2 ao projeto.  

1.  Passe o mouse no projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Gerenciar NuGet Pacotes...**.  
    
    :::image type="complex" source="./media/wpf-getting-started-mng-nuget.png" alt-text="Gerenciar NuGet pacotes":::
       Gerenciar NuGet pacotes
    :::image-end:::
    
1.  Na barra de pesquisa, digite `Microsoft.Web.WebView2` > escolha **Microsoft.Web.WebView2**.  
    
    :::image type="complex" source="./media/install-nuget.png" alt-text="NuGet" lightbox="./media/install-nuget.png":::
       NuGet  
    :::image-end:::
    
    Comece a desenvolver aplicativos usando a API WebView2.  Para criar e executar o projeto, selecione `F5` .  O projeto em execução exibe uma janela vazia.  
    
    :::image type="complex" source="./media/winforms-empty-app.png" alt-text="Aplicativo vazio" lightbox="./media/winforms-empty-app.png":::
       Aplicativo vazio  
    :::image-end:::
    
## <a name="step-3---create-a-single-webview"></a>Etapa 3 - Criar um único WebView  

Adicione um WebView ao seu aplicativo.  

1.  Abra o **Windows Designer de Formulários.**  
1.  **Pesquise WebView2** na **Caixa de Ferramentas**.  
    
    > [!NOTE]
    > Se você estiver usando Visual Studio 2017, por padrão **WebView2** pode não ser exibido na **Caixa de Ferramentas**.  Para habilitar o comportamento, escolha **Opções**de Ferramentas  >  ****  >  **Gerais** > definir a configuração **Preencher Automaticamente a Caixa** de Ferramentas como `True` .  
    
    Arraste e solte o **controle WebView2** no aplicativo Windows Forms.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Caixa de ferramentas exibindo WebView2":::
       Caixa de ferramentas exibindo WebView2  
    :::image-end:::  
    
1.  De definir `(Name)` a propriedade como `webView` .
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propriedades do controle WebView2":::
       Propriedades do controle WebView2
    :::image-end:::
    
1.  A `Source` propriedade define o URI inicial exibido no controle WebView2.  De definir `Source` a propriedade como `https://www.microsoft.com` .  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="A propriedade Source do controle WebView2":::
       A **propriedade Source** do controle WebView2
    :::image-end:::  

Para criar e executar seu projeto, selecione `F5` .  Certifique-se de que seu controle WebView2 seja [https://www.microsoft.com][|::ref1::|Main] exibido.

:::image type="complex" source="./media/winforms-hello-webview.png" alt-text="Hello webview" lightbox="./media/winforms-hello-webview.png":::
   Hello webview  
:::image-end:::    

> [!NOTE]
> Se você estiver trabalhando em um monitor DPI alto, talvez seja necessário configurar seu aplicativo Windows Forms para alto [suporte a DPI.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]  

## <a name="step-4---handle-window-resize-events"></a>Etapa 4 - Manipular eventos de resize de janela  

Adicione mais alguns controles ao seu Windows Formulários da caixa de ferramentas e, em seguida, manipular eventos de resize da janela adequadamente.  

1.  No Windows **Designer de Formulários,** abra a **Caixa de Ferramentas**.  
1.  Arraste e solte uma **TextBox** no aplicativo Windows Forms.  Nomeia **TextBox** `addressBar` na guia **Propriedades.**  
1.  Arraste e solte um **botão** no aplicativo Windows Formulários.  Altere o texto no **botão** para `Go!` e nomee o **botão** na `goButton` guia **Propriedades.**  
    
    O aplicativo deve ter a aparência da imagem a seguir no designer.  
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="Designer WinForms" lightbox="./media/winforms-designer.png":::
       Designer WinForms  
    :::image-end:::  

1.  No `Form1.cs` arquivo, defina para manter os controles no local quando a Janela do `Form_Resize` Aplicativo for resized.
    
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

Para criar e executar seu projeto, selecione `F5` .  Verifique se o aplicativo é exibido de forma semelhante à captura de tela a seguir.

:::image type="complex" source="./media/winforms-app.png" alt-text="aplicativo" lightbox="./media/winforms-app.png":::
   Aplicativo  
:::image-end:::  

## <a name="step-5---navigation"></a>Etapa 5 - Navegação

Adicione a capacidade de permitir que os usuários alterem a URL exibida pelo controle WebView2 adicionando uma barra de endereços ao aplicativo.  

1.  Selecione `F5` para criar e executar seu projeto.  Confirme se o aplicativo exibe semelhante à captura de tela a seguir.  
    
    :::image type="complex" source="./media/winforms-app.png" alt-text="Aplicativo WinForms" lightbox="./media/winforms-app.png":::
       Aplicativo WinForms  
    :::image-end:::  
    
1.  No `Form1.cs` arquivo, para adicionar o `CoreWebView2` namespace, insira o seguinte trecho de código na parte superior.  
1.  In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs` .  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  No Windows Designer de **Formulários,** clique duas vezes no `Go!` botão para criar o método no `goButton_Click` `Form1.cs` arquivo.  Copie e colar o trecho a seguir dentro da função.  Agora, a `goButton_Click` função navega pelo WebView até a URL inserida na barra de endereços.
    
    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
Para criar e executar seu projeto, selecione `F5` .  Insira uma nova URL na barra de endereços e selecione **Ir**.  Por exemplo, digite `https://www.bing.com` .  Verifique se o controle WebView2 navega até a URL.  

> [!NOTE]
> Verifique se uma URL completa é inserida na barra de endereços.  Um `ArgumentException` é lançado se a URL não começar com `http://` ou `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   bing.com  
:::image-end:::  

## <a name="step-6---navigation-events"></a>Etapa 6 - Eventos de navegação  

Durante a navegação na página da Web, o controle WebView2 gera eventos.  O aplicativo que hospeda controles WebView2 escuta os seguintes eventos.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
    
Para obter mais informações, navegue até [Eventos de Navegação][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   Eventos de navegação
:::image-end:::

Quando ocorre um erro, os seguintes eventos são gerados e podem depender da navegação para uma página da Web de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    
> [!NOTE]
> Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.  

Para demonstrar como usar os eventos, comece registrando um manipulador para que cancele todas as `NavigationStarting` solicitações que não usam HTTPS.  

No `Form1.cs` arquivo, atualize o construtor para corresponder ao trecho de código a seguir e adicione a `EnsureHttps` função.  

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

No construtor, é `EnsureHttps` registrado como o manipulador de eventos no evento no controle `NavigationStarting` WebView2.  

Para criar e executar seu projeto, selecione `F5` .  Verifique se ao navegar para um site HTTP, o WebView permanece inalterado.  No entanto, o WebView navegará até sites HTTPS.

## <a name="step-7---scripting"></a>Etapa 7 - Scripting  

Você pode usar aplicativos host para injetar código JavaScript em controles WebView2 no tempo de execução.  Você pode tarefa webView para executar JavaScript arbitrário ou adicionar scripts de inicialização.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado com tempo específico.  

*   Execute-o após a criação do objeto global.  
*   Execute-o antes que qualquer outro script incluído no documento HTML seja executado.  
    
Como exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites que não são HTTPS.  Modifique `EnsureHttps` a função para injetar um script no conteúdo da Web que usa o método [ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]  

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

Para criar e executar seu projeto, selecione `F5` .  Verifique se o aplicativo exibe um alerta quando você navega até um site que não usa HTTPS.  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   https  
:::image-end:::  

## <a name="step-8---communication-between-host-and-web-content"></a>Etapa 8 - Comunicação entre conteúdo do host e da Web  

O conteúdo do host e da Web pode ser `postMessage` usado para se comunicar uns com os outros da seguinte maneira:  

*   O conteúdo da Web em um controle WebView2 pode ser usado `window.chrome.webview.postMessage` para postar uma mensagem no host.  O host lida com a mensagem usando qualquer `WebMessageReceived` registro no host.  
*   Hosts postam mensagens no conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .  Essas mensagens são capturadas por manipuladores adicionados a `window.chrome.webview.addEventListener` .  
    
O mecanismo de comunicação passa mensagens do conteúdo da Web para o host usando recursos nativos.  

Em seu projeto, quando o controle WebView2 navega até uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.  

1.  No `Form1.cs` arquivo, atualize o construtor e crie uma `InitializeAsync` função para corresponder ao trecho de código a seguir.  A `InitializeAsync` função aguarda [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] porque a inicialização `CoreWebView2` de é assíncrona.  
    
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
    
1.  Depois `CoreWebView2` de inicializado, registre um manipulador de eventos para responder `WebMessageReceived` a .  No `Form1.cs` arquivo, atualize `InitializeAsync` e adicione usando o seguinte trecho de `UpdateAddressBar` código.  
    
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
    
1.  Para que o WebView envie e responda à mensagem da Web, depois de inicializado, o host injeta um script no conteúdo `CoreWebView2` da Web para:  
    1.  Envie a URL para o host usando `postMessage` .
    1.  Registre um manipulador de eventos para imprimir uma mensagem enviada do host.  
        
No `Form1.cs` arquivo, atualize `InitializeAsync` para corresponder ao trecho de código a seguir.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Para criar e executar o aplicativo, selecione `F5` .  Agora, a barra de endereços exibe o URI no controle WebView2.  Além disso, quando você navega com êxito para uma nova URL, o WebView alerta o usuário da URL exibida no WebView.  

:::image type="complex" source="./media/winforms-final-app.png" alt-text="Aplicativo final" lightbox="./media/winforms-final-app.png":::
   Aplicativo final  
:::image-end:::  

Parabéns, você criou seu primeiro aplicativo WebView2.  

## <a name="next-steps"></a>Próximas etapas  

Para continuar a aprender mais sobre WebView2, navegue até os seguintes recursos.  

*   Para saber mais sobre como criar aplicativos WebView2, navegue até Práticas recomendadas de desenvolvimento [webView2.][WV2BestPractices]  
*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].  
*   Para obter informações detalhadas sobre a API WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WinformsWebview2].  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Práticas recomendadas de desenvolvimento do WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "WebView2 Class | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Configurando seu aplicativo do Windows Forms para alto suporte a DPI - Suporte a DPI alto no Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desenvolvedor do Microsoft Edge"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
