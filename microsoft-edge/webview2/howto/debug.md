---
description: Saiba como depurar controles WebView2.
title: Introdução à depuração de aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 15171147b847b1d41cd603efed1b8ee42185dc29
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010695"
---
# Introdução à depuração de aplicativos WebView2  

O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos e ferramentas de desenvolvimento de aplicativo Web e nativo.  Ao desenvolver seu aplicativo WebView2, você deve depurar seu aplicativo.  Este artigo descreve as diferentes ferramentas a serem usadas para depurar o código nativo e Web em seu aplicativo do WebView2.  

## [Microsoft Edge DevTools](#tab/devtools)  

Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que você pode depurar para outra página da Web exibida no Microsoft Edge.  Para abrir o DevTools, defina o foco no controle WebView e use uma das ações a seguir.  

*   Selecione `F12` .  
*   Selecione `Ctrl` + `Shift` + `I` .  
*   Abra o menu de contexto \ (clique com o botão direito do mouse \) e escolha `Inspect` .  

Para obter mais informações, consulte [visão geral de devtools][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="Depuração DevTools" lightbox="./media/f12.png":::
   Depuração DevTools  
:::image-end:::  

## [Visual Studio](#tab/visualstudio)  

O Visual Studio fornece várias ferramentas de depuração para o código nativo e Web em aplicativos do WebView2.  Na seção do Visual Studio, o foco principalmente é a depuração de controles WebView, mas os outros métodos de depuração no Visual Studio estão disponíveis normalmente.  Use o processo a seguir para depurar o código nativo e Web somente em aplicativos Win32 ou em suplementos do Office.  

> [!IMPORTANT]
> Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, a seleção `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.  Selecione `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar a situação.  

Antes de começar, certifique-se de que os seguintes requisitos sejam atendidos.  

*   Para depurar scripts, o aplicativo deve ser iniciado no Visual Studio.  
*   Não é possível anexar um depurador a um processo de WebView2 em execução.  
*   Instale o Visual Studio 2019 versão 16,4 Preview 2 ou posterior.  

Instale e configure as ferramentas do depurador de scripts no Visual Studio.  

1.  Conclua as seguintes ações para instalar o componente de **diagnóstico JavaScript** no **desenvolvimento de área de trabalho com C++**.  

    1. Na barra do Windows Explorer, digite `Visual Studio Installer` .  
    1. Escolha **instalador do Visual Studio** para abri-lo.  
    1. No instalador do Visual Studio, na versão instalada, escolha o botão **mais** e, em seguida, escolha **Modificar**.  
    1. No Visual Studio, em **cargas**de trabalho, escolha a configuração **desenvolvimento de área de trabalho em C++** .  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Tela modificando cargas de trabalho do Visual Studio" lightbox="./media/workloads.png":::
            Tela modificando cargas de trabalho do Visual Studio :::image-end:::  
        
    1.  Escolha **componentes individuais**.  
    1.  Na caixa de pesquisa, digite `JavaScript diagnostics` .  
    1.  Escolha a configuração **diagnóstico de JavaScript** .  
    1.  Escolha **Modificar**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio modificando a guia componentes individuais" lightbox="./media/indivcomp.png":::
           Visual Studio modificando a guia componentes individuais  
        :::image-end:::  
        
1.  Habilite a depuração de script para aplicativos do WebView2.  
    1.  No projeto do WebView2, abra o menu de contexto \ (clique com o botão direito do mouse \) e escolha **Propriedades**.  
    1.  Em **Propriedades de configuração**, escolha **depuração**.  
    1.  Em **tipo de depurador**, escolha **JavaScript (WebView2)**.  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Propriedade de configuração de depuração do Visual Studio" lightbox="./media/enbjs.png":::
           Propriedade de configuração de **depuração** do Visual Studio  
        :::image-end:::  
        
Conclua as seguintes ações para depurar seu aplicativo WebView2.  

1.  Para definir um ponto de interrupção no código-fonte, passe o mouse à esquerda do número da linha e escolha definir um ponto de interrupção.  O adaptador de depuração JS/TS não executa o mapeamento de caminho de origem.  Você deve abrir exatamente o mesmo caminho associado à sua WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Adicionar ponto de interrupção do Visual Studio" lightbox="./media/breakpoint.png"::: 
       Adicionar ponto de interrupção do Visual Studio  
    :::image-end:::  
    
1.  Para executar o depurador, escolha o tamanho do bit da plataforma e escolha o botão de reprodução verde ao lado de **depurador local do Windows**.  O aplicativo é executado e o depurador se conecta ao primeiro processo WebView2 criado.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Depurador local do Windows do Visual Studio" lightbox="./media/run.png"::: 
       **Depurador local do Windows** do Visual Studio  
    :::image-end:::  
    
1.  No **console de depuração**, localize a saída do depurador.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Console de depuração do Visual Studio" lightbox="./media/console.png"::: 
       Console de **depuração** do Visual Studio  
    :::image-end:::  
    
* * *  

## Consulte também  

*   Para começar a usar o WebView2, confira [WebView2 guias de introdução][Webview2MainGettingStarted].  
*   Para obter um exemplo abrangente de recursos do WebView2, consulte o repositório do [WebView2Samples][GithubMicrosoftedgeWebview2samples] no github.
*   Para obter informações mais detalhadas sobre APIs do WebView2, consulte [referência de API][Webview2ApiReference].
*   Para obter mais informações sobre o WebView2, consulte [recursos do WebView2][Webview2MainNextSteps].

## Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-a classe Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions | Documentos da Microsoft"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-globais | Documentos da Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referência de API do Microsoft Edge WebView2 | Documentos da Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Ponto de partida-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quais são as novidades? -Depurador JavaScript para código do Visual Studio-Microsoft/vscode-js-depuração | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicativos WebView do Microsoft Edge (Chromium)-depurador de código do Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
