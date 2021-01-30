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
# Getting started with WebView2 in Windows Forms

Neste artigo, aprenda a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obter mais informações sobre APIs individuais, navegue até a [referência de API.][DotnetApiMicrosoftWebWebview2Winforms]  

## Pré-requisitos  

Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir.  

*   [WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no sistema operacional suportado \(atualmente Windows 10, Windows 8.1 e Windows 7\).  
    
    > [!NOTE]
    > A equipe WebView recomenda usar o canal Canary e a versão mínima necessária é 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 ou posterior.  
    
> [!NOTE]
> No momento, o WebView2 não dá suporte aos designers do .NET 5 e do .NET Core.

## Etapa 1: criar um aplicativo de janela única

Comece com um projeto de área de trabalho básico que contenha uma única janela principal.  

1.  No Visual Studio, escolha **Windows Forms .NET Framework App**  >  **Next**.
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Novo projeto" lightbox="./media/winforms-newproject.png":::
       Novo projeto  
    :::image-end:::
    
1.  Insira valores para **o nome do projeto** e o **local.**  Escolha **o .NET Framework 4.6.2** ou posterior.  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Iniciar projeto" lightbox="./media/winforms-startproj.png":::
       Iniciar projeto  
    :::image-end:::
    
1.  Para criar seu projeto, escolha **Criar**.
    
## Etapa 2 - Instalar o SDK webView2

Use NuGet para adicionar o SDK WebView2 ao projeto.  

1.  Passe o mouse sobre o projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Gerenciar Pacotes NuGet...**.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gerenciar pacotes NuGet":::
       Gerenciar pacotes NuGet
    :::image-end:::
    
1.  Na barra de pesquisa, digite > `Microsoft.Web.WebView2` escolha **Microsoft.Web.WebView2**.  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Comece a desenvolver aplicativos usando a API WebView2.  Para criar e executar o projeto, selecione `F5` .  O projeto em execução exibe uma janela vazia.  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Aplicativo vazio" lightbox="./media/winforms-emptyapp.png":::
       Aplicativo vazio  
    :::image-end:::
    
## Etapa 3 - Criar um único WebView  

Adicione um WebView ao seu aplicativo.  

1.  Abra o **Designer de Formulários do Windows.**  
1.  Pesquise **WebView2** na **Caixa de Ferramentas.**  
    
    > [!NOTE]
    > Se você estiver usando o Visual Studio 2017, por padrão **WebView2** pode não ser exibido na Caixa **de Ferramentas.**  Para habilitar o comportamento, escolha **Opções**de Ferramentas Gerais > definir a configuração Preencher  >  ****  >  **** **Automaticamente a Caixa de** Ferramentas como `True` .  
    
    Arraste e solte o **controle WebView2** no Aplicativo de Formulários do Windows.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Caixa de ferramentas exibindo WebView2":::
       Caixa de ferramentas exibindo WebView2
    :::image-end:::  

1.  Definir a `(Name)` propriedade como `webView` .
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propriedades do controle WebView2":::
       Propriedades do controle WebView2
    :::image-end:::

1.  A `Source` propriedade define o URI inicial exibido no controle WebView2.  Definir a `Source` propriedade como `https://www.microsoft.com` .  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="A propriedade Source do controle WebView2":::
       A **propriedade Source** do controle WebView2
    :::image-end:::  

Para criar e executar seu projeto, selecione `F5` .  Verifique se o controle WebView2 é [https://www.microsoft.com][|::ref1::|Main] exibido.

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   hello webview  
:::image-end:::  

> [!NOTE]
> Se você estiver trabalhando em um monitor DPI alto, talvez seja necessário configurar seu aplicativo [Windows Forms para suporte a DPI alto.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]  

## Etapa 4 - Manipular eventos de resize da janela

Adicione mais alguns controles ao Windows Forms na caixa de ferramentas e, em seguida, manipular eventos de resize da janela adequadamente.

1.  No **Designer de Formulários do Windows,** abra a **Caixa de Ferramentas**
1.  Arraste e solte um **TextBox no** Aplicativo de Formulários do Windows.  In the **Properties Tab**, name the **TextBox** `addressBar` .
1.  Arraste e solte um **botão no** aplicativo Windows Forms.  Altere o texto no **botão para** e nome `Go!` do **botão** na `goButton` guia **Propriedades**.

    O aplicativo deve se parecer com a imagem a seguir no designer.
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="designer" lightbox="./media/winforms-designer.png":::
       designer  
    :::image-end:::  

1.  No `Form1.cs` arquivo, defina `Form_Resize` para manter os controles no local quando a Janela do Aplicativo for resized.

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

Para criar e executar seu projeto, selecione `F5` .  Certifique-se de que o aplicativo seja exibido de forma semelhante à captura de tela a seguir.

:::image type="complex" source="./media/winforms-app.png" alt-text="aplicativo" lightbox="./media/winforms-app.png":::
   Aplicativo  
:::image-end:::

## Etapa 5 - Navegação

Adicione a capacidade de permitir que os usuários alterem a URL que o controle WebView2 exibe adicionando uma barra de endereços ao aplicativo.

1.  No `Form1.cs` arquivo, para adicionar o namespace, insira o trecho de código a `CoreWebView2` seguir na parte superior.  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  In the **Windows Forms Designer**, double-click on the button to create the method in the `Go!` `goButton_Click` `Form1.cs` file.  Copie e copie e copie o seguinte trecho de código dentro da função.  Agora, a `goButton_Click` função navega pelo WebView até a URL inserida na barra de endereços.

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Para criar e executar seu projeto, selecione `F5` .  Insira uma nova URL na barra de endereços e selecione **Ir.**  Por exemplo, insira `https://www.bing.com` .  Certifique-se de que o controle WebView2 navegue até a URL.  

> [!NOTE]
> Certifique-se de que uma URL completa seja inserida na barra de endereços.  Um `ArgumentException` é lançado se a URL não começa com `http://` ou `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   bing.com  
:::image-end:::

## Etapa 6 - Eventos de navegação  

Durante a navegação na página da Web, o controle WebView2 gera eventos.  O aplicativo que hospeda controles WebView2 escuta os eventos a seguir.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Para obter mais informações, navegue até [Eventos de Navegação.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação":::
   Eventos de navegação
:::image-end:::

Quando ocorre um erro, os eventos a seguir são gerados e podem depender da navegação para uma página da Web de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.  

Para demonstrar como usar esses eventos, comece registrando um manipulador para que cancele quaisquer solicitações que não `NavigationStarting` usem HTTPS.  

No arquivo, atualize o construtor para corresponder ao trecho de código a seguir `Form1.cs` e adicione a `EnsureHttps` função.  

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

No construtor, EnsureHttps é registrado como o manipulador de eventos `NavigationStarting` no evento no controle WebView2.  

Para criar e executar seu projeto, selecione `F5` .  Certifique-se de que, ao navegar para um site HTTP, o WebView permaneça inalterado.  No entanto, o WebView navegará para sites HTTPS.

## Etapa 7 - Scripts  

Você pode usar aplicativos host para inserir código JavaScript em controles WebView2 no tempo de execução.  Você pode tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado com tempo específico.  

*   Execute-o após a criação do objeto global.  
*   Execute-o antes que qualquer outro script incluído no documento HTML seja executado.  

Por exemplo, adicione scripts que enviam um alerta quando um usuário navega para sites não HTTPS.  Modifique `EnsureHttps` a função para inserir um script no conteúdo da Web que usa o método [ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]  

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

Para criar e executar seu projeto, selecione `F5` .  Certifique-se de que o aplicativo exibe um alerta quando você navega para um site que não usa HTTPS.  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   https  
:::image-end:::

## Etapa 8- Comunicação entre o conteúdo do host e da Web  

O conteúdo do host e da Web pode `postMessage` ser usado para se comunicar uns com os outros da seguinte maneira:  

*   O conteúdo da Web em um controle WebView2 pode `window.chrome.webview.postMessage` ser usado para postar uma mensagem no host.  O host lida com a mensagem usando qualquer `WebMessageReceived` registro no host.  
*   Hosts postam mensagens no conteúdo da Web em um controle WebView2 usando `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .  Essas mensagens são capturadas por manipuladores adicionados `window.chrome.webview.addEventListener` a .  

O mecanismo de comunicação passa mensagens do conteúdo da Web para o host usando recursos nativos.  

Em seu projeto, quando o controle WebView2 navega para uma URL, ele exibe a URL na barra de endereços e alerta o usuário da URL exibida no controle WebView2.  

1.  No `Form1.cs` arquivo, atualize o construtor e crie uma `InitializeAsync` função para corresponder ao trecho de código a seguir.  A `InitializeAsync` função aguarda [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] porque a inicialização `CoreWebView2` é assíncrona.  

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

1.  Após `CoreWebView2` a inicialização, registre um manipulador de eventos para `WebMessageReceived` responder.  No `Form1.cs` arquivo, atualize `InitializeAsync` e adicione usando o trecho de código a `UpdateAddressBar` seguir.  

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

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Aplicativo final" lightbox="./media/winforms-finalapp.png":::
   Aplicativo final  
:::image-end:::

Parabéns, você criou seu primeiro aplicativo WebView2.  

## Próximas etapas  

Para continuar a saber mais sobre WebView2, navegue até os seguintes recursos.  

### Ver também  

*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Para obter mais informações sobre WebView2, navegue até [Recursos de WebView2][Webview2IndexNextSteps].  
*   Para obter informações detalhadas sobre a API WebView2, navegue até a [referência de API.][DotnetApiMicrosoftWebWebview2WinformsWebview2]  

## Entrar em contato com a equipe do Microsoft Edge WebView  

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