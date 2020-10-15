---
description: Saiba como depurar controles WebView2.
title: Introdução à depuração de aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 25a710796b499a78a43045266058029caa890b78
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119105"
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

O Visual Studio fornece várias ferramentas de depuração para o código nativo e Web em aplicativos do WebView2.  Na seção do Visual Studio, o foco principal é a depuração de controles WebView, mas os outros métodos de depuração no Visual Studio estão disponíveis normalmente.  Use o processo a seguir para depurar o código nativo e Web somente em aplicativos Win32 ou em suplementos do Office.  

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
        
        :::image type="complex" source="./media/workloads.png" alt-text="Depuração DevTools" lightbox="./media/workloads.png":::
            Tela modificando cargas de trabalho do Visual Studio :::image-end:::  
        
    1.  Escolha **componentes individuais**.  
    1.  Na caixa de pesquisa, digite `JavaScript diagnostics` .  
    1.  Escolha a configuração **diagnóstico de JavaScript** .  
    1.  Escolha **Modificar**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Depuração DevTools" lightbox="./media/indivcomp.png":::
           Visual Studio modificando a guia componentes individuais  
        :::image-end:::  
        
1.  Habilite a depuração de script para aplicativos do WebView2.  
    1.  No projeto do WebView2, abra o menu de contexto \ (clique com o botão direito do mouse \) e escolha **Propriedades**.  
    1.  Em **Propriedades de configuração**, escolha **depuração**.  
    1.  Em **tipo de depurador**, escolha **JavaScript (WebView2)**.  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Depuração DevTools" lightbox="./media/enbjs.png":::
           Propriedade de configuração de **depuração** do Visual Studio  
        :::image-end:::  
        
Conclua as seguintes ações para depurar seu aplicativo WebView2.  

1.  Para definir um ponto de interrupção no código-fonte, passe o mouse à esquerda do número da linha e escolha definir um ponto de interrupção.  O adaptador de depuração JS/TS não executa o mapeamento de caminho de origem.  Você deve abrir exatamente o mesmo caminho associado à sua WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Depuração DevTools" lightbox="./media/breakpoint.png"::: 
       Adicionar ponto de interrupção do Visual Studio  
    :::image-end:::  
    
1.  Para executar o depurador, escolha o tamanho do bit da plataforma e escolha o botão de reprodução verde ao lado de **depurador local do Windows**.  O aplicativo é executado e o depurador se conecta ao primeiro processo WebView2 criado.  
    
    :::image type="complex" source="./media/run.png" alt-text="Depuração DevTools" lightbox="./media/run.png"::: 
       **Depurador local do Windows** do Visual Studio  
    :::image-end:::  
    
1.  No **console de depuração**, localize a saída do depurador.  
    
    :::image type="complex" source="./media/console.png" alt-text="Depuração DevTools" lightbox="./media/console.png"::: 
       Console de **depuração** do Visual Studio  
    :::image-end:::  
    
## [Visual Studio Code](#tab/visualstudiocode)  

Use o código do Microsoft Visual Studio para depurar scripts executados em controles WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

No código do Visual Studio, conclua as seguintes ações para depurar seu código. 

1.  Seu projeto precisa ter um `launch.json` arquivo.  Se o seu projeto não tiver um `launch.json` arquivo, copie o trecho de código a seguir e crie um novo `launch.json` arquivo.  
        
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
        
1.  Para definir um ponto de interrupção no código-fonte, passe o mouse sobre a linha e selecione `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Depuração DevTools" lightbox="./media/breakpointvs.png":::
       O ponto de interrupção é definido no código do Visual Studio  
    :::image-end:::
    
    > [!NOTE]
    > Como o código do Visual Studio não executa o mapeamento de origem, certifique-se de definir pontos de interrupção no mesmo arquivo que o WebView2 usa.  Se os caminhos não corresponderem, o código do Visual Studio não pausará o código em execução no ponto de interrupção.  
    
1.  Executar o código.  
    1.  Na guia **executar** , escolha a configuração iniciar no menu suspenso.  
    1.  Para iniciar a depuração do aplicativo, escolha Iniciar Depuração, que é o triângulo verde ao lado do menu suspenso configuração de inicialização.  
        
        :::image type="complex" source="./media/runvs.png" alt-text="Depuração DevTools" lightbox="./media/runvs.png":::
           Guia executar código do Visual Studio  
        :::image-end:::  
        
1.  Abra o **console de depuração** para exibir a saída de depuração e os erros.  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text="Depuração DevTools" lightbox="./media/resultsvs.png":::
       Console de depuração de código do Visual Studio  
    :::image-end:::  
    
**Configurações avançadas**:  

*   Depuração WebView direcionada. 

    Em alguns aplicativos do WebView2, você pode usar mais de um controle WebView2. Para escolher o controle WebView2 para depurar nesta situação, você pode usar a depuração de WebView2 direcionada 
    
    Abra `launch.json` e conclua as seguintes ações para usar a depuração WebView direcionada.  
    
    1.  Confirme se o `useWebview` parâmetro está definido como `true` .  
    1.  Adicione o `urlFilter` parâmetro.  Quando o controle WebView2 navega para uma URL, o `urlFilter` valor do parâmetro é usado para comparar cadeias de caracteres que aparecem na URL.  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    Ao depurar seu aplicativo, talvez você precise percorrer o código do início do processo de renderização. Se você estiver renderizando páginas da Web em sites e não tiver acesso ao código-fonte, poderá usar a `?=value`  opção porque as páginas da Web ignoram parâmetros não reconhecidos.   
    
    > [!IMPORTANT]
    > Depois que a primeira correspondência for encontrada na URL, o depurador será interrompido.  Você não pode depurar dois controles WebView2 ao mesmo tempo porque a porta CDP é compartilhada por todos os controles WebView2 e usa um número de porta único.  
    
*   Depurar processos em execução  
    
    Talvez seja necessário anexar o depurador para executar os processos do WebView2. Para fazer isso, `launch.json` atualize o `request` parâmetro para `attach` .
        
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
        
    O controle WebView2 deve abrir a porta CDP para permitir a depuração do controle WebView2.  Seu código deve ser criado para garantir que apenas um controle WebView2 tenha uma porta CDP (protocolo de desenvolvedor Chrome) aberta antes de iniciar o depurador.  
    
*   Opções de rastreamento de depuração  
    
    Adicione o `trace` parâmetro a launch.jspara habilitar o rastreamento de depuração.  
    
    1.  Adicionar `trace` parâmetro.  
        
 
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text="Depuração DevTools" lightbox="./media/tracelog.png":::
                 Salvar a saída de depuração em um arquivo de log  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text="Depuração DevTools" lightbox="./media/verbose.png":::
                 Saída de depuração de código do Visual Studio com o rastreamento detalhado ativado  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Depurar suplementos do Office.
    
    Se você estiver Depurando suplementos do Office, abra o código-fonte do suplemento em uma instância separada do código do Visual Studio.  Abra o launch.jsem seu aplicativo do WebView2 e adicione o trecho de código a seguir para anexar o depurador ao suplemento do Office.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Solucionando problemas com o depurador  
    
    Você pode encontrar os seguintes cenários ao usar o depurador.  

    *   O depurador não pára no ponto de interrupção, e você tem saída de depuração.  Para resolver o problema, confirme se o arquivo com o ponto de interrupção é o mesmo arquivo que é usado pelo controle WebView2.  O depurador não executa o mapeamento de caminho de origem.  
    *   Você não pode anexar a um processo em execução e Obtém um erro de tempo limite.  Para solucionar o problema, confirme se o controle WebView2 abriu a porta CDP.  Verifique se o  `additionalBrowserArguments`  valor no registro está correto ou as opções estão corretas.  Para obter mais informações, consulte [additionalBrowserArguments para dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] e [additionalBrowserArguments para Win32][Webview2ReferenceWin32Webview2IdlParameters].  
    
* * *  


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

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propriedade CoreWebView2EnvironmentOptions. AdditionalBrowserArguments (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment-globais | Documentos da Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referência de API do Microsoft Edge WebView2 | Documentos da Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Ponto de partida-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quais são as novidades? -Depurador JavaScript para código do Visual Studio-Microsoft/vscode-js-depuração | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicativos WebView do Microsoft Edge (Chromium)-depurador de código do Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
