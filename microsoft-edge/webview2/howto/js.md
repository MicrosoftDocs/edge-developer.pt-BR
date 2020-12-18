---
description: Saiba como usar JavaScript em cenários complexos em aplicativos do WebView2
title: Usar JavaScript em aplicativos do WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: da04d1e24b95dfa7ea477bbd228fd46b64727ec3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230933"
---
# Usar JavaScript em WebView para cenários estendidos  

Usar JavaScript nos controles WebView2 permite que você personalize aplicativos nativos para atender às suas necessidades.  Este artigo explica como usar JavaScript no WebView2 e analisa como desenvolver usando recursos e funcionalidades avançados do WebView2.  

## Antes de começar  

Este artigo pressupõe que você já tem um projeto em funcionamento.  Se você não tiver um projeto e quiser acompanhar, navegue até o [Guia de introdução ao WebView2][Webview2GettingstartedWpf].  

## Funções básicas de WebView2  

Use as funções a seguir para começar a inserir JavaScript em seu aplicativo WebView.  

| API  | Descrição  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | Executar JavaScript em um controle WebView. Para obter mais informações, navegue até o tutorial de introdução. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | É executado quando o modelo de objeto do documento (DOM \) é criado. |
      
## Cenário: executando um arquivo de script dedicado  

Nesta seção, acesse um arquivo JavaScript dedicado a partir de seu controle WebView2.  

> [!NOTE]
> Embora escrever JavaScript inline possa ser eficiente para comandos JavaScript rápidos, você perde os temas de cor JavaScript e a formatação de linha que tornam difícil escrever seções grandes de código no Visual Studio.  

Para solucionar o problema, crie um arquivo JavaScript separado com seu código e, em seguida, passe uma referência para esse arquivo usando os `ExecuteScriptAsync` parâmetros.  

1.  Crie um `.js` arquivo em seu projeto e adicione o código JavaScript que você deseja executar.  Por exemplo, crie um arquivo chamado `script.js` .  
1.  Converter o arquivo JavaScript em uma cadeia de caracteres que é passada para `ExecuteScriptAsync` .  
    1.  Para converter o arquivo JavaScript em uma cadeia de caracteres, copie o trecho de código a seguir.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Cole o código em `MainWindow.xaml.cs` .  
1.  Passe a variável de texto usando `ExecuteScriptAsync` .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## Cenário: remover a funcionalidade de arrastar e soltar  

Nesta seção, use JavaScript para remover a funcionalidade de arrastar e soltar do controle WebView2.  

Para começar, explore a funcionalidade de arrastar e soltar atual.  

1.  Crie um `.txt` arquivo para arrastar e soltar.  Por exemplo, crie um arquivo denominado `contoso.txt` e adicione texto a ele.  
1.  Execute o projeto.  
1.  Arraste e solte o arquivo no `contoso.txt` controle WebView.  Uma nova janela será aberta, que é o resultado do código em seu projeto de amostra.  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Resultado de arrastar e soltar contoso.txt" lightbox="./media/dragtext.png":::
       Resultado de arrastar e soltar contoso.txt  
    :::image-end:::  

Agora, adicione código para remover a funcionalidade de arrastar e soltar do controle WebView2.  

1.  Copie e cole o trecho de código a seguir em `InitializeAsync()` `MainWindow.xaml.cs` .   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  Execute o projeto.  
1.  Tente arrastar e soltar `contoso.txt` .  Confirme que você não pode arrastar e soltar.  

## Cenário: removendo o menu de contexto  

Nesta seção, remova o menu de contexto padrão do seu controle WebView2.  

Para começar, explore a funcionalidade do menu contextual atual.  

1.  Execute o projeto.  
1.  Passe o mouse em qualquer lugar do controle WebView2 e abra o menu de contexto \ (clique com o botão direito do mouse \).  O menu de contexto exibe as opções padrão.  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="O menu de contexto mostrando as opções padrão" lightbox="./media/contextmenu.png":::
       O menu de contexto mostrando as opções padrão  
    :::image-end:::  
    
Agora, adicione código para remover a funcionalidade do menu contextual do controle WebView2.  

1.  Copie e cole o trecho de código a seguir em `InitializeAsync()` `MainWindow.xaml.cs` .    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  Execute o código novamente.  Confirme que você não pode abrir um menu de contexto \ (clique com o botão direito do mouse \).  
   
## Consulte também  

*   Para obter mais informações sobre como começar a usar o WebView2, navegue até [WebView2 guias de introdução][Webview2MainGettingStarted].  
*   Para obter um exemplo abrangente de recursos do WebView2, navegue até o repositório do [WebView2Samples][GithubMicrosoftedgeWebview2samples] no github.  
*   Para obter informações detalhadas sobre APIs do WebView2, navegue até [referência da API][Webview2ApiReference].  
*   Para obter mais informações sobre o WebView2, navegue até [recursos do WebView2][Webview2MainNextSteps].  

## Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  


[Webview2ApiReference]: ../webview2-api-reference.md "Referência de API do Microsoft Edge WebView2 | Documentos da Microsoft"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Introdução ao WebView2 no WPF (visualização) | Documentos da Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Ponto de partida-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-interface ICoreWebView2 | Documentos da Microsoft"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync (String) (Microsoft. Web. WebView2. WPF) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
