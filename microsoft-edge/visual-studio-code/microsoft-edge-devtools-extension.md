---
description: Como usar Elementos para Microsoft Edge (Chromium) de Visual Studio Code
title: Elementos para Microsoft Edge (Chromium) de Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, vs code, visual studio code, elements
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398452"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a>Microsoft Edge DevTools para Visual Studio Code extensão  

Usar <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->esta extensão para acessar no Microsoft Edge DevTools [dentro Microsoft Visual Studio Código][VisualstudioCode].  Você tem acesso às ferramentas **Elementos** e **Rede** no Microsoft Edge DevTools.  Você pode iniciar ou anexar a uma instância de Microsoft Edge.  Depois de se conectar, você pode exibir a estrutura HTML do tempo de execução, alterar o layout, corrigir problemas de estilo e inspecionar o tráfego de rede.  

## <a name="elements-tool"></a>Ferramenta Elements  

Por padrão, a extensão inicia uma instância do navegador em uma janela exclusiva e fornece a funcionalidade **Elements** do Microsoft Edge DevTools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools para Visual Studio Code em execução com uma janela completa do navegador" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge DevTools para Visual Studio Code em execução com uma janela completa do navegador  
:::image-end:::  

Nas configurações de extensão, você pode habilitar mais funcionalidades como **Modo Sem Cabeça** e **Rede.**  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Habilitando (ou desabilitando) o modo sem cabeça e a inspeção de rede nas configurações de extensão" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Habilitando \(ou desabilitando\) modo sem cabeça e inspeção de rede nas configurações de extensão  
:::image-end:::  

## <a name="headless-mode"></a>Modo Sem Cabeça  

No modo sem cabeça, essa extensão não inicia uma instância completa do navegador para depurar.  Ele executa uma instância em segundo plano.  Talvez seja preciso ficar dentro do editor e interagir com o navegador incorporado.  Um ícone extra do navegador não será exibido na barra de tarefas.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools para Visual Studio Code executando com um sem cabeça" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge DevTools para Visual Studio Code em execução com um navegador sem cabeça  
:::image-end:::  

> [!NOTE]
> No macOS, você deve ativar o modo sem cabeça como seu modo preferencial.  O uso do modo sem cabeça deve resolver um problema em que, se a janela não estiver visível, a janela do navegador relata que ela é `Not Active` .  

## <a name="network-tool"></a>Ferramenta Rede  

Se você também quiser inspecionar o tráfego de rede do seu aplicativo, abra as configurações e acione a **guia** Rede.  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspeção de rede Microsoft Edge DevTools para Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Inspeção de rede Microsoft Edge DevTools para Visual Studio Code  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a>Iniciando Microsoft Edge da extensão  

Navegue até Microsoft Edge Ferramentas na Barra **de Atividades**.  Ao lado de onde ele **Microsoft Edge Ferramentas: Destinos,** há um sinal de aplicação que abre o navegador para seu aplicativo.  Se você escolher a **opção about:blank,** deverá navegar até seu aplicativo Web no navegador para que ele apareça no painel **Elementos** no Visual Studio Code.  

## <a name="launching-microsoft-edge-from-the-debug-view"></a>Iniciando Microsoft Edge do exibição Depurar  

Se você estiver acostumado a usar o exibição Depurar no Visual Studio Code, acesse Microsoft Edge DevTools a partir dele.  

1.  Em Visual Studio Code, navegue até o exibição Depurar 
    *   Selecione `Ctrl` + `Shift` + `D` em Windows/Linux \( `Command` + `Shift` + `D` no macOS\).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Se você não tiver configurações no Visual Studio Code, conclua uma das seguintes ações.  
>     *   Selecione `F5` .  
>     *   Escolha o **botão Reproduzir** \(verde\).  
> 1.  No menu suspenso, escolha **Borda** no menu suspenso.  
> 1.  Um `launch.json` arquivo deve ser exibido que contém a seguinte configuração.  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> Depois de carregar a configuração correta, conclua a ação a seguir.  

1.  Para iniciar a **ferramenta Elements** Visual Studio Code, conclua uma das seguintes ações. 
    *   Selecione `F5` .  
    *   Escolha o **botão Reproduzir** \(verde\).  
         
Agora, você pode fazer as seguintes ações.  

*   Acesse uma screencast do navegador.  
*   Inspecione o DOM e o estilo dos componentes em sua página.  

## <a name="attaching-to-microsoft-edge"></a>Anexando a Microsoft Edge  

Para abrir um navegador e anexar a instância Visual Studio Code, conclua as etapas a seguir. 

1.  Para abrir uma instância de Microsoft Edge \(Chromium\), copie e execute o seguinte comando.  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  Depois que a instância é lançada, copie e colar o seguinte trecho de código em seu `launch.json` arquivo.  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  Em Visual Studio Code, abra o menu suspenso **Depurador** e escolha Anexar ao Microsoft Edge **e abra as ferramentas de desenvolvedor.**  
1.  Para iniciar a **ferramenta Elements** Visual Studio Code, conclua uma das seguintes ações. 
    *   Selecione `F5` .  
    *   Escolha o **botão Reproduzir** \(verde\).  
         
Agora, você pode fazer as seguintes ações.  

*   Acesse uma screencast do navegador.  
*   Inspecione o DOM e o estilo dos componentes em sua página.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a>Entrar em contato com o Microsoft Edge DevTools para Visual Studio Code de extensão  

Envie seus comentários [arquivando um problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] GitHub [o repo][GithubMicrosoftVscodeEdgeDevtools] da extensão.  

Se você quiser ajudar a fazer <!--the Microsoft Edge DevTools for Visual Studio Code -->essa extensão é melhor, suas contribuições são bem-vindas.  Encontre tudo o que você precisa para começar no GitHub [do repo][GithubMicrosoftVscodeEdgeDevtools] da extensão.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Novo Problema - microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Ferramentas para Visual Studio Code"  
