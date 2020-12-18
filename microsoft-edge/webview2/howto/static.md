---
description: Saiba como vincular estaticamente a biblioteca WebView2 Loader.
title: Como vincular estaticamente a biblioteca WebView2 Loader
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230926"
---
# Vincule estaticamente a biblioteca WebView2 Loader  

Você pode querer distribuir seu aplicativo com um único arquivo executável, em vez de um pacote de muitos arquivos. Para criar um único arquivo executável ou reduzir o tamanho do seu pacote, você deve vincular estaticamente os arquivos WebView2Loader. O SDK do WebView2 contém um arquivo de cabeçalho, `WebView2Loader.dll` e o `IDL` arquivo. `WebView2Loader.dll` é um componente pequeno que ajuda os aplicativos a localizar o tempo de execução do WebView2 ou os canais não estáveis do Microsoft Edge, no dispositivo.  

Para os aplicativos que não querem enviar a uma `WebView2Loader.dll` , conclua as etapas a seguir.  

1.  Abra o `.vcxproj` arquivo de projeto para seu aplicativo em um editor de texto, como código do Visual Studio.  
    
    > [!NOTE]
    > O `.vcproj` arquivo de projeto pode ser um arquivo oculto, o que significa que ele não é exibido no Visual Studio.  Use a linha de comando para localizar arquivos ocultos.  
    
1.  Localize a seção no código em que você inclui os arquivos de destino do pacote NuGet do WebView2.  O local no código é realçado na figura a seguir.  

    :::image type="complex" source="./media/inserthere.png" alt-text="Trecho de código de arquivos de projeto" lightbox="./media/inserthere.png":::
       Trecho de código de arquivos de projeto   
    :::image-end:::  
  
1.  Copie o trecho de código a seguir e cole-o onde o `Microsoft.Web.WebView2.targets` está incluído.  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Trecho de código inserido" lightbox="./media/staticlib.png":::
       Trecho de código inserido  
    :::image-end:::  
    
1.  Edite as dependências adicionais da configuração de compilação do seu aplicativo.  Para começar, localize todas as `<AdditionalDependencies>` marcas. Para cada um, adicione `version.lib` como uma dependência adicional a cada configuração de compilação diferente no `.vcxproj` arquivo.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Adicionando Version. lib a ItemDefinitionGroups" lightbox="./media/versionlib.png":::
       Adicionar `version.lib` a `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > A equipe do WebView2 tem o objetivo de automatizar a adição da dependência adicional em lançamentos futuros.  
    
1. Compile e execute o aplicativo.

### Entrar em contato com a equipe do WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### Consulte também  

*   Para começar a usar o WebView2, navegue até [WebView2 guias de introdução][Webview2MainGettingStarted].  
*   Para obter um exemplo abrangente de recursos do WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samples] no github.
*   Para obter informações mais detalhadas sobre APIs do WebView2, navegue até [referência da API][Webview2ApiReference].
*   Para obter mais informações sobre o WebView2, navegue até [recursos do WebView2][Webview2MainNextSteps].

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Referência de API do Microsoft Edge WebView2 | Documentos da Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Ponto de partida-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quais são as novidades? -Depurador JavaScript para código do Visual Studio-Microsoft/vscode-js-depuração | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicativos WebView do Microsoft Edge (Chromium)-depurador de código do Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
