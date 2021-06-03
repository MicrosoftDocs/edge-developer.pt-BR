---
description: Saiba como usar JavaScript em cenários complexos em aplicativos WebView2
title: Usar JavaScript em aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 8db5c4a5b3709c144240fe88e6f8480445c1659f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535750"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a>Usar JavaScript no WebView para cenários estendidos  

Usar o JavaScript em controles WebView2 permite personalizar aplicativos nativos para atender aos seus requisitos.  Este artigo explora como usar o JavaScript no WebView2 e analisa como desenvolver usando recursos e funcionalidade avançados do WebView2.  

## <a name="before-you-begin"></a>Antes de começar  

Este artigo supõe que você já tenha um projeto funcionando.  Se você não tiver um projeto e quiser acompanhar, navegue até o Guia de Introdução [WebView2.][Webview2GetStartedWpf]  

## <a name="basic-webview2-functions"></a>Funções Básicas do WebView2  

Use as seguintes funções para começar a incorporar JavaScript em seu aplicativo WebView.  

| API  | Descrição  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | Execute JavaScript em um controle WebView. Para obter mais informações, navegue até a Introdução tutorial. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | É executado quando o Modelo de Objeto de Documento \(DOM\) é criado. |
      
## <a name="scenario--running-a-dedicated-script-file"></a>Cenário: executando um arquivo de script dedicado  

Nesta seção, acesse um arquivo JavaScript dedicado do controle WebView2.  

> [!NOTE]
> Embora escrever JavaScript em linha possa ser eficiente para comandos JavaScript rápidos, você perde temas de cores javaScript e formatação de linha que dificulta a gravação de grandes seções de código em Visual Studio.  

Para resolver o problema, crie um arquivo JavaScript separado com seu código e, em seguida, passe uma referência para esse arquivo usando `ExecuteScriptAsync` os parâmetros.  

1.  Crie um `.js` arquivo em seu projeto e adicione o código JavaScript que você deseja executar.  Por exemplo, crie um arquivo chamado `script.js` .  
1.  Converta o arquivo JavaScript em uma cadeia de caracteres que é passada para `ExecuteScriptAsync` .  
    1.  Para converter seu arquivo JavaScript em uma cadeia de caracteres, copie o seguinte trecho de código.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Colar o código em `MainWindow.xaml.cs` .  
1.  Passe a variável de texto usando `ExecuteScriptAsync` .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  
    
## <a name="scenario--remove-drag-and-drop-functionality"></a>Cenário: remover a funcionalidade de arrastar e soltar  

Nesta seção, use JavaScript para remover a funcionalidade de arrastar e soltar do controle WebView2.  

Para começar, explore a funcionalidade atual de arrastar e soltar.  

1.  Crie um `.txt` arquivo para arrastar e soltar.  Por exemplo, crie um arquivo nomeado `contoso.txt` e adicione texto a ele.  
1.  Execute seu projeto.  
1.  Arraste e solte o arquivo `contoso.txt` no controle WebView.  Uma nova janela é aberta, que é o resultado do código em seu projeto de exemplo.  
    
    :::image type="complex" source="./media/drag-text.png" alt-text="Resultado de arrastar e soltar contoso.txt" lightbox="./media/drag-text.png":::
       Resultado de arrastar e soltar contoso.txt  
    :::image-end:::  
    
Agora, adicione código para remover a funcionalidade de arrastar e soltar do controle WebView2.  

1.  Copie e colar o seguinte trecho de código `InitializeAsync()` em `MainWindow.xaml.cs` .   
    
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
    
1.  Execute seu projeto.  
1.  Tente arrastar e `contoso.txt` soltar.  Confirme se você não é capaz de arrastar e soltar.  
    
## <a name="scenario--removing-the-context-menu"></a>Cenário: Removendo o Menu de Contexto  

Nesta seção, remova o menu de contexto padrão do controle WebView2.  

Para começar, explore a funcionalidade atual do menu contextual.  

1.  Execute seu projeto.  
1.  Passe o mouse em qualquer lugar no controle WebView2 e abra o menu de contexto \(clique com o botão direito do mouse\).  O menu de contexto exibe as opções padrão.  
    
    :::image type="complex" source="./media/context-menu.png" alt-text="O menu de contexto mostrando as opções padrão" lightbox="./media/context-menu.png":::
       O menu de contexto mostrando as opções padrão  
    :::image-end:::  
    
Agora adicione código para remover a funcionalidade de menu contextual do controle WebView2.  

1.  Copie e colar o seguinte trecho de código `InitializeAsync()` em `MainWindow.xaml.cs` .    
    
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  
    
1.  Execute o código novamente.  Confirme se não é possível abrir um menu de contexto \(clique com o botão direito do mouse\).  
    
## <a name="see-also"></a>Consulte também  

*   Para começar a usar WebView2, navegue até [WebView2 Introdução Guias][Webview2MainGetStarted].  
*   Para um exemplo abrangente de recursos WebView2, navegue até o repo do [WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.  
*   Para obter informações detalhadas sobre APIs WebView2, navegue até [referência de API][Webview2ApiReference].  
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2MainNextSteps].  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Referência da API WebView2 | Microsoft Docs"  
[Webview2GetStartedWpf]: ../get-started/wpf.md "Começar com WebView2 no WPF (Visualização) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0,9.579 - interface ICoreWebView2 | Microsoft Docs"  

[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
