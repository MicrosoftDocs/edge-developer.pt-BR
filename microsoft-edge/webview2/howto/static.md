---
description: Saiba como vincular estaticamente a biblioteca WebView2 Loader.
title: Como vincular estaticamente a biblioteca WebView2 Loader
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: b7e0ec70cb00f318d4eb67254f37fcec79a5fcf6
ms.sourcegitcommit: 903524ab85321ade278facd741d6487e8cabe33f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100292"
---
# Como vincular estaticamente a biblioteca WebView2 Loader  

## Contexto  

O que é o WebView2Loader.dll?  

*   O SDK do WebView2 contém um arquivo de cabeçalho, `WebView2Loader.dll.` e o `IDL` arquivo. `WebView2Loader.dll` é um componente pequeno que ajuda os aplicativos a localizar o tempo de execução do WebView2 (ou canais do Microsoft Edge não estáveis) no dispositivo.  

Para aplicativos que têm um tempo de execução único e não querem enviar a `WebView2Loader.dll` , conclua as etapas do **procedimento** a seguir.  

## Procedimento  

1.  Abra o `.vcxproj` arquivo de projeto para seu aplicativo em um editor de texto, como código do Visual Studio.  
    
    > [!NOTE]
    > O `.vcproj` arquivo de projeto pode ser um arquivo oculto, o que significa que ele não é exibido no Visual Studio.  Use a linha de comando para localizar um arquivo oculto.  
    
1.  Localize a seção no código em que você inclui os arquivos de destino do pacote NuGet do WebView2.  O local no código é realçado na figura a seguir.  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Trecho de código de arquivos de projeto" lightbox="./media/inserthere.png"::: 
       Trecho de código de arquivos de projeto  
    :::image-end:::  
    
1.  Copie o trecho de código a seguir e cole-o em qualquer lugar no qual o `Microsoft.Web.WebView2.targets` está incluído.  

    > [!NOTE]
    > Por exemplo, inclua-o após o seguinte bloco de código.  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Trecho de código de arquivos de projeto" lightbox="./media/staticlib.png"::: 
       Trecho de código inserido  
    :::image-end:::  
    
1.  Edite as dependências adicionais da configuração de compilação do seu aplicativo.  Para começar, localize todas as `<AdditionalDependencies>` marcas.  
1.  Adicione `version.lib` como uma dependência adicional a cada configuração de compilação diferente no `.vcxproj` arquivo do seu aplicativo.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Trecho de código de arquivos de projeto" lightbox="./media/versionlib.png"::: 
       Adicionar `version.lib` a `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > A equipe WebView2 tem o objetivo de automatizar a etapa de dependência adicional em lançamentos futuros.  
    
Compile e implante seu aplicativo.  Cessões.  

## Consulte também  

*   Para começar a usar o WebView2, navegue até [WebView2 guias de introdução][Webview2MainGettingStarted].  
*   Para obter um exemplo abrangente de recursos do WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samples] no github.
*   Para obter informações mais detalhadas sobre APIs do WebView2, navegue até [referência da API][Webview2ApiReference].
*   Para obter mais informações sobre o WebView2, navegue até [recursos do WebView2][Webview2MainNextSteps].

## Entrar em contato com a equipe do WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-a classe Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions | Documentos da Microsoft"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-globais | Documentos da Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referência de API do Microsoft Edge WebView2 | Documentos da Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Ponto de partida-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quais são as novidades? -Depurador JavaScript para código do Visual Studio-Microsoft/vscode-js-depuração | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicativos WebView do Microsoft Edge (Chromium)-depurador de código do Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
