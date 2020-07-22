---
description: Saiba como depurar controles WebView2.
title: Depurando WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888574"
---
# Como depurar com WebView2  

O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos de desenvolvimento de aplicativos Web e nativo e ferramentas de desenvolvedor.  A página a seguir descreve as diferentes ferramentas a serem usadas ao desenvolver com controles WebView2.  

## Microsoft Edge DevTools  

Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsMain] para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que faria se estivesse usando o Microsoft Edge.  Para abrir o DevTools, defina o foco na janela do WebView e use qualquer uma das ações a seguir.  

*   Selecione `F12` .  
*   Selecione `Ctrl` + `Shift` + `I` .  
*   Abra o menu de contexto \ (clique com o botão direito do mouse \) e selecione `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!IMPORTANT]
> Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, a seleção `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.  Use `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar a situação.  

## Visual Studio  

Você pode usar o Visual Studio para desenvolver o código do aplicativo e depurar scripts ao mesmo tempo.  

Tenha o seguinte em mente.  

*   O Visual Studio só oferece suporte a scripts de depuração quando o aplicativo é iniciado no Visual Studio.  \ (Não há suporte para anexar um processo em execução para depuração. \)  
*   Não há suporte para o cenário de depuração de webviews direcionado.  

Use o depurador de script do Visual Studio 2019 versão 16,4 Preview 2 ou posterior para depurar seu script no Visual Studio.  

Configurar o depurador.  

*   Verifique se o componente de **diagnóstico JavaScript** em **desenvolvimento de área de trabalho com carga de trabalho C++** está instalado.  
    
    1.  Navegue até **aplicativos &** configurações de recursos no Windows.  Pesquise por ele usando a barra de tarefas do Windows.  
    1.  Escolha **Modificar**.  
    1.  Verifique se as caixas de seleção **diagnóstico** e **desenvolvimento da área de trabalho do JavaScript em C++** estão marcadas.  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Aplicativos e recursos" lightbox="../media/appsandfeatures.png":::
           Aplicativos e recursos  
        :::image-end:::  
        
*   Habilite a depuração de script WebView2.  
    1.  Passe o mouse no seu projeto, abra o menu de contexto \ (clique com o botão direito do mouse \) e selecione **Propriedades**.  
    1.  Em **Propriedades de configuração**, selecione **depuração**.  
    1.  Na propriedade **tipo de depurador** , procure a lista de opções e selecione **JavaScript (WebView2)**.  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Depurador do JavaScript do Visual Studio" lightbox="../media/enbjs.png":::
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

Você pode usar o código do Visual Studio para depurar scripts executados em controles WebView2.  Para obter mais informações, consulte [aplicativos do Microsoft Edge (Chromium) WebView][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Entrar em contato com a equipe do Microsoft Edge WebView  

Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários.  Acesse o [repositório de comentários][GithubMicrosoftedgeWebviewfeedback] para enviar solicitações de recursos ou relatórios de erros.  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chromium) aplicativos WebView-VS-depurador de código-depurador para Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
