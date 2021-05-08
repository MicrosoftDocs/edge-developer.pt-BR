---
description: Saiba como vincular estaticamente a biblioteca do carregador WebView2.
title: Como vincular estaticamente a biblioteca do carregador WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 8f48a4fde9e2960de6156fc14db8c84f87a49868
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535743"
---
# <a name="statically-link-the-webview2-loader-library"></a>Vincular estaticamente a biblioteca do carregador WebView2  

Talvez você queira distribuir seu aplicativo com um único arquivo executável, em vez de um pacote de muitos arquivos. Para criar um único arquivo executável ou reduzir o tamanho do pacote, você deve vincular estáticamente os arquivos WebView2Loader. O SDK WebView2 contém um arquivo de header `WebView2Loader.dll` e o `IDL` arquivo. `WebView2Loader.dll` é um pequeno componente que ajuda os aplicativos a localizar o Tempo de Execução do WebView2, ou canais não estáveis do Microsoft Edge, no dispositivo.  

Para aplicativos que não querem enviar `WebView2Loader.dll` um , conclua as etapas a seguir.  

1.  Abra o arquivo de projeto para seu aplicativo em um editor de `.vcxproj` texto, como Visual Studio Código.  
    
    > [!NOTE]
    > O `.vcproj` arquivo do projeto pode ser um arquivo oculto, o que significa que ele não é exibido Visual Studio.  Use a linha de comando para encontrar arquivos ocultos.  
    
1.  Localize a seção no código em que você inclui os arquivos de destino do pacote NuGet WebView2.  O local no código é realçado na figura a seguir.  
    
    :::image type="complex" source="./media/insert-here.png" alt-text="Trecho de código de Arquivos do Projeto" lightbox="./media/insert-here.png":::
       Trecho de código de Arquivos do Projeto   
    :::image-end:::  
    
1.  Copie o trecho de código a seguir e o colar onde o `Microsoft.Web.WebView2.targets` está incluído.  
    
    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```  
    
    :::image type="complex" source="./media/static-lib.png" alt-text="Trecho de código inserido" lightbox="./media/static-lib.png":::
       Trecho de código inserido  
    :::image-end:::  
    
1.  Edite as dependências adicionais da configuração de com build para seu aplicativo.  Para começar, encontre todas as `<AdditionalDependencies>` marcas. Para cada um deles, `version.lib` adicione como uma dependência adicional a cada configuração de com build diferente no `.vcxproj` arquivo.  
    
    :::image type="complex" source="./media/version-lib.png" alt-text="Adicionando version.lib a ItemDefinitionGroups" lightbox="./media/version-lib.png":::
       Adicionando `version.lib` ao `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > A equipe webView2 tem como objetivo automatizar a adição da dependência adicional em versões futuras.  
    
1.  Compile e execute seu aplicativo.  
    
## <a name="getting-in-touch-with-the-webview2-team"></a>Entrar em contato com a equipe webView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

## <a name="see-also"></a>Ver também  

*   Para começar a usar WebView2, navegue até [WebView2 Guias de Início.][Webview2MainGetStarted]  
*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samples] no GitHub.
*   Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][Webview2ApiReference].
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2MainNextSteps].
    
<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Referência da API do Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Novidades? - Depurador JavaScript para código Visual Studio - microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicativos WebView do Microsoft Edge (Chromium) - Visual Studio Código - Depurador para Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
