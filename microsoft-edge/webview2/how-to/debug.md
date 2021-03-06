---
description: Saiba como depurar controles WebView2.
title: Começar a depurar aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 01cd67897f7041bca0cedcee2cc3242f3ebcc962
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535748"
---
# <a name="get-started-debugging-webview2-apps"></a>Começar a depurar aplicativos WebView2  

O objetivo do controle Microsoft Edge WebView2 é combinar o melhor dos recursos e ferramentas de desenvolvimento de aplicativos nativos e web.  Ao desenvolver seu aplicativo WebView2, você deve depurar seu aplicativo.  Este artigo descreve as diferentes ferramentas a ser usadas para depurar sua Web e código nativo em seu aplicativo WebView2.  

## [<a name="microsoft-edge-devtools"></a>Microsoft Edge DevTools](#tab/devtools)  

Use [Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] Ferramentas de Desenvolvedor para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que você pode depurar para outra página da Web exibida no Microsoft Edge.  Para abrir o DevTools, de definir o foco no controle WebView e, em seguida, use uma das seguintes ações.  

*   Selecione `F12` .  
*   Selecione `Ctrl` + `Shift` + `I` .  
*   Abra o menu de contexto \(clique com o botão direito do mouse\) e escolha `Inspect` .  
    
Para obter mais informações, navegue até [DevTools overview][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="DevTools depuração" lightbox="./media/f12.png":::
   DevTools depuração  
:::image-end:::    

## [<a name="visual-studio"></a>Visual Studio](#tab/visualstudio)  

Visual Studio fornece várias ferramentas de depuração para web e código nativo em aplicativos WebView2.  Na seção Visual Studio, o foco principal é depurar controles WebView, no entanto, os outros métodos de depuração no Visual Studio estão disponíveis como de costume.  Use o processo a seguir para depurar código nativo e web em aplicativos Win32 ou Office somente complementos.  

> [!IMPORTANT]
> Quando você depura seu aplicativo Visual Studio com o depurador nativo anexado, a seleção pode disparar o depurador nativo em vez `F12` de Ferramentas do Desenvolvedor.  Selecione `Ctrl` + `Shift` + `I` , ou use o menu de contexto \(clique com o botão direito do mouse\) para evitar a situação.  

Antes de começar, certifique-se de que os seguintes requisitos sejam atendidos.  

*   Para depurar scripts, o aplicativo deve ser lançado de dentro Visual Studio.  
*   Não é possível anexar um depurador a um processo WebView2 em execução.  
*   Instale Visual Studio versão 2019 16.4 Preview 2 ou posterior.  
    
Instalar e configurar as ferramentas de depurador de script em Visual Studio.  

1.  Conclua as seguintes ações para instalar o componente de diagnóstico **JavaScript** no **desenvolvimento da área de trabalho com C++**.  
    1.  Na barra Windows Explorer, digite `Visual Studio Installer` .  
    1.  Escolha **Instalador do Visual Studio** abri-lo.  
    1.  Na Instalador do Visual Studio, na versão instalada, escolha o botão **Mais** e escolha **Modificar**.  
    1.  Em Visual Studio, em **Cargas de Trabalho,** escolha a configuração Desenvolvimento da Área de Trabalho **em C++.**  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio Modificando a tela de cargas de trabalho" lightbox="./media/workloads.png":::
            Visual Studio Modificando a tela de cargas de trabalho
        :::image-end:::  
        
    1.  Escolha **Componentes individuais**.  
    1.  Na caixa de pesquisa, digite `JavaScript diagnostics` .  
    1.  Escolha a **configuração de diagnóstico JavaScript.**  
    1.  Escolha **Modificar**. 
        
        :::image type="complex" source="./media/indiv-comp.png" alt-text="Visual Studio Modificando a guia Componentes Individuais" lightbox="./media/indiv-comp.png":::
           Visual Studio Modificando a guia Componentes Individuais  
        :::image-end:::  
        
1.  Habilitar a depuração de script para aplicativos WebView2.  
    1.  Em seu projeto WebView2, abra o menu de contexto \(clique com o botão direito do mouse\) e escolha **Propriedades**.  
    1.  Em Propriedades **de Configuração,** escolha **Depuração**.  
    1.  Em Tipo **de Depurador,** escolha **JavaScript (WebView2)**.  
        
        :::image type="complex" source="./media/enb-js.png" alt-text="Visual Studio Propriedade Depuração de Configuração" lightbox="./media/enb-js.png":::
           Visual Studio Propriedade **de Configuração de Depuração**  
        :::image-end:::  
        
Conclua as seguintes ações para depurar seu aplicativo WebView2.  

1.  Para definir um ponto de interrupção no código-fonte, passe o mouse para a esquerda do número de linha e escolha definir um ponto de interrupção.  O adaptador de depuração JS/TS não executa o mapeamento de caminho de origem.  Você deve abrir exatamente o mesmo caminho associado ao seu WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio adicionar ponto de interrupção" lightbox="./media/breakpoint.png"::: 
       Visual Studio adicionar ponto de interrupção  
    :::image-end:::  
    
1.  Para executar o depurador, escolha o tamanho do bit da plataforma e, em seguida, escolha o botão de reprodução verde ao lado de **Local Windows Depurador**.  O aplicativo é executado e o depurador se conecta ao primeiro processo WebView2 criado.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio Depurador Windows local" lightbox="./media/run.png"::: 
       Visual Studio **Depurador de Windows Local**  
    :::image-end:::  
    
1.  No **Console de Depuração,** encontre a saída do depurador.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio Console de depuração" lightbox="./media/console.png"::: 
       Visual Studio Console **de Depuração**  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a>Visual Studio Code](#tab/visualstudiocode)  

Use Microsoft Visual Studio Código para depurar scripts executados em controles WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

Em Visual Studio Code, conclua as seguintes ações para depurar seu código. 

1.  Seu projeto é necessário para ter um `launch.json` arquivo.  Se seu projeto não tiver um arquivo, copie o trecho de código a seguir `launch.json` e crie um novo `launch.json` arquivo.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > Visual Studio Code mapeamento de caminho de origem agora requer a URL, portanto, seu aplicativo agora recebe um parâmetro de linha de comando quando ele é iniciado.  Você pode ignorar com segurança o `url` parâmetro, se necessário.  
    
1.  Para definir um ponto de interrupção no código-fonte, passe o mouse na linha e selecione `F9`
    
    :::image type="complex" source="./media/breakpoint-vs.png" alt-text="O ponto de interrupção é definido Visual Studio Code" lightbox="./media/breakpoint-vs.png":::
       O ponto de interrupção é definido Visual Studio Code  
    :::image-end:::
    
1.  Execute o código.  
    1.  Na guia **Executar,** escolha a configuração de início no menu suspenso.  
    1.  Para começar a depurar seu aplicativo, escolha Iniciar Depuração, que é o triângulo verde ao lado da configuração de início listada.  
        
        :::image type="complex" source="./media/run-vs.png" alt-text=" Visual Studio Code Guia Executar" lightbox="./media/run-vs.png":::
           Visual Studio Code Guia Executar  
        :::image-end:::  
        
1.  Abra **o Console de Depuração** para exibir a saída e os erros de depuração.  
    
    :::image type="complex" source="./media/results-vs.png" alt-text=" Visual Studio Code Console de depuração" lightbox="./media/results-vs.png":::
       Visual Studio Code Console de depuração  
    :::image-end:::  
    
**Avançado Configurações**:  

*   Depuração de Webview direcionada. 
    
    Em alguns aplicativos WebView2, você pode usar mais de um controle WebView2. Para escolher o controle WebView2 para depurar nessa situação, você pode usar a depuração de webview2 direcionada 
    
    Abra `launch.json` e conclua as seguintes ações para usar a depuração de Webview direcionada.  
    
    1.  Confirme se o `useWebview` parâmetro está definido como `true` .  
    1.  Adicione o `urlFilter` parâmetro.  Quando o controle WebView2 navega para uma URL, o valor do parâmetro é usado para comparar cadeias de caracteres que `urlFilter` aparecem na URL.  
        
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    Ao depurar seu aplicativo, talvez seja necessário passar pelo código desde o início do processo de renderização. Se você estiver renderizando páginas da Web em sites e não tiver acesso ao código-fonte, poderá usar a opção, pois as páginas da Web ignoram parâmetros não `?=value`  reconhecedos.   
    
    > [!IMPORTANT]
    > Depois que a primeira combinação for encontrada na URL, o depurador será interrompido.  Não é possível depurar dois controles WebView2 ao mesmo tempo porque a porta CDP é compartilhada por todos os controles WebView2 e usa um único número de porta.  
    
*   Depurar processos em execução  
    
    Talvez seja necessário anexar o depurador a processos WebView2 em execução. Para fazer isso, em `launch.json` , `request` atualize o parâmetro para `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    Seu controle WebView2 deve abrir a porta CDP para permitir a depuração do controle WebView2.  Seu código deve ser criado para garantir que apenas um controle WebView2 tenha uma porta CDP (Chrome Developer Protocol) aberta, antes de iniciar o depurador.  
    
*   Opções de rastreamento de depuração  
    
    Adicione o `trace` parâmetro launch.jspara habilitar o rastreamento de depuração.  
    
    1.  Adicionar `trace` parâmetro.  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/trace-log.png" alt-text=" Salve a saída de depuração em um arquivo de log." lightbox="./media/trace-log.png":::
                 Salvar a saída de depuração em um arquivo de log  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Saída detalhada" lightbox="./media/verbose.png":::
                 Visual Studio Code Depurar Saída com rastreamento detalhado ligado  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Depurar Office-ins.  
    
    Se você estiver depurando Office de Office, abra o código-fonte do add-in em uma instância separada de Visual Studio Code.  Abra launch.jsem seu aplicativo WebView2 e adicione o seguinte trecho de código para anexar o depurador ao Office de usuário.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Solução de problemas do depurador  
    
    Você pode encontrar os seguintes cenários ao usar o depurador.  
    
    *   O depurador não para no ponto de interrupção e você tem saída de depuração.  Para resolver o problema, confirme se o arquivo com o ponto de interrupção é o mesmo arquivo usado pelo controle WebView2.  O depurador não executa o mapeamento de caminho de origem.  
    *   Você não pode anexar a um processo em execução e obter um erro de tempo de tempo.  Para resolver o problema, confirme se o controle WebView2 abriu a porta CDP.  Verifique se  `additionalBrowserArguments`  o valor no Registro está correto ou se as opções estão corretas.  Para obter mais informações, navegue até [additionalBrowserArguments para dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] e [additionalBrowserArguments para Win32][Webview2ReferenceWin32Webview2IdlParameters].  
        
* * *  

## <a name="see-also"></a>Consulte também  

*   Para começar a usar WebView2, navegue até [WebView2 Introdução Guias][Webview2MainGetStarted].  
*   Para um exemplo abrangente de recursos WebView2, navegue até o repo do [WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.
*   Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][Webview2ApiReference].
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2MainNextSteps].
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propriedade CoreWebView2EnvironmentOptions.AdditionalBrowserArguments (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment - Globals | Microsoft Docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Referência da API WebView2 | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
