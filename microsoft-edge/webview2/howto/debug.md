---
description: Saiba como depurar controles WebView2.
title: Depurando WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 6b2cc65e5cb368c29efec2eb3638f0c1772000d9
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926474"
---
# Como depurar com WebView2  

O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos de desenvolvimento de aplicativos Web e nativo e ferramentas de desenvolvedor.  A página a seguir descreve as diferentes ferramentas a serem usadas ao desenvolver com controles WebView2.  

## Microsoft Edge DevTools  

Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que você usa o Microsoft Edge.  Para abrir o DevTools, defina o foco na janela do WebView e use qualquer uma das ações a seguir.  
*   Selecione `F12` .  
*   Selecione `Ctrl` + `Shift` + `I` .  
*   Abra o menu de contexto \ (clique com o botão direito do mouse \) > selecionar `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!NOTE]
> Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, o pressionamento `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.  Pressione `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar a situação.  

> [!NOTE]
> Você pode usar o `--auto-open-devtools-for-tabs` argumento da linha de comando para abrir uma nova janela do devtools ao criar pela primeira vez um WebView.  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## Visual Studio  

Use o depurador de script do Visual Studio 2019 versão 16,4 Preview 2 ou posterior para depurar seu script no Visual Studio.  Verifique se o componente de **diagnóstico JavaScript** em **desenvolvimento de área de trabalho com carga de trabalho C++** está instalado.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnóstico do JavaScript do Visual Studio":::
   Diagnóstico do JavaScript do Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Para habilitar a depuração de script do WebView2, abra o menu de contexto \ (clique com o botão direito do mouse \) em seu projeto > selecione **Propriedades**.  

*   Em **Propriedades de configuração**, selecione **depuração**.  
*   Na propriedade **tipo de depurador** , selecione **JavaScript (WebView2)** na lista de opções. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Depurador do JavaScript do Visual Studio":::
   Depurador do JavaScript do Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Você está configurado e pronto para depurar.  

Para depurar, conclua as ações a seguir.  

1.  Definir pontos de interrupção  
    *   Abra o arquivo de script e defina o ponto de interrupção onde você deseja.  
        
        > [!NOTE]
        > O adaptador de depuração JS/TS não faz o mapeamento de caminho de origem.Você deve abrir exatamente o mesmo caminho associado à sua WebView2.  
        
1.  Executar código  
    *   Selecione seu tipo de compilação e ambiente de tempo de execução apropriados e inicie o depurador local do Windows.  
1.  Exibir console de depuração  
    *   Seu aplicativo é executado e o depurador se conecta após a criação do primeiro webview2.Qualquer saída de depuração pendente será exibida.  
        
        > [!NOTE]
        > Esse método de depuração está atualmente restrito a aplicativos Win32 e suplementos do Office.  
        
## Visual Studio Code  

Você pode usar o código do Visual Studio para depurar scripts executados em controles WebView2.  Para obter mais informações, consulte [aplicativos do Microsoft Edge (Chromium) WebView][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chromium) aplicativos WebView-VS Code-Debugger para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
