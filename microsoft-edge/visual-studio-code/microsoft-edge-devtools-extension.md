---
description: Como usar os elementos do Microsoft Edge (Chromium) a partir do código do Visual Studio
title: Elementos para Microsoft Edge (Chromium) do código do Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, elementos
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135472"
---
# Extensão de código do Microsoft Edge DevTools para Visual Studio  

Usar <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->Esta extensão para acessar o Microsoft Edge DevTools dentro do [código do Visual Studio][VisualstudioCode].  Você tem acesso aos **elementos** e às ferramentas de **rede** no Microsoft Edge devtools.  Você pode iniciar ou anexar uma instância do Microsoft Edge.  Depois de se conectar, você pode exibir a estrutura HTML do tempo de execução, alterar o layout, corrigir os problemas de estilo e inspecionar o tráfego de rede.  

## Ferramenta elementos  

Por padrão, a extensão inicia uma instância de navegador em uma janela exclusiva e oferece a funcionalidade de **elementos** do Microsoft Edge devtools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools para o código do Visual Studio em execução com uma janela de navegador completa" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge DevTools para o código do Visual Studio em execução com uma janela de navegador completa  
:::image-end:::  

Nas configurações de extensão, você pode habilitar mais funcionalidade, como **modo sem periféricos** e **rede**.  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Microsoft Edge DevTools para o código do Visual Studio em execução com uma janela de navegador completa" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Habilitando \ (ou desativando \) o modo sem periféricos e a inspeção de rede nas configurações de extensão  
:::image-end:::  

## Modo sem periféricos  

No modo sem periféricos, essa extensão não inicia uma instância completa do navegador para depurar.  Ele executa uma instância em segundo plano.  Talvez você precise ficar dentro do editor e interagir com o navegador integrado.  Um ícone adicional do navegador não é exibido na barra de tarefas.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools para o código do Visual Studio em execução com uma janela de navegador completa" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge DevTools para o código do Visual Studio em execução com um navegador sem periféricos  
:::image-end:::  

> [!NOTE]
> No macOS, você deve ativar o modo sem periféricos como modo preferencial.  Usar o modo sem periféricos deve resolver um problema em que, se a janela não estiver visível, a janela do navegador informa que é `Not Active` .  

## Ferramenta de rede  

Se você também quiser inspecionar o tráfego de rede do seu aplicativo, abra as configurações e ative a guia **rede** .  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Microsoft Edge DevTools para o código do Visual Studio em execução com uma janela de navegador completa" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Inspeção de rede no Microsoft Edge DevTools para código do Visual Studio  
:::image-end:::  

## Iniciando o Microsoft Edge da extensão  

Navegue até ferramentas do Microsoft Edge na **barra de atividades**.  Ao lado de onde diz as **Ferramentas do Microsoft Edge: destinos,** há um sinal de adição que abre o navegador do seu aplicativo.  Se você escolher a opção **about: Blank** , navegue até o seu aplicativo Web no navegador para que ele apareça no painel **elementos** do código do Visual Studio.  

## Iniciando o Microsoft Edge a partir do modo de exibição de depuração  

Se você estiver acostumado a usar o modo de exibição de depuração no código do Visual Studio, acesse o Microsoft Edge DevTools dele.  

1.  No código do Visual Studio, navegue até o modo de exibição de depuração 
    *   Selecione `Ctrl` + `Shift` + `D` no Windows/Linux \ ( `Command` + `Shift` + `D` no MacOS \).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Se você não tiver nenhuma configuração no código do Visual Studio, execute uma das seguintes ações.  
>     *   Selecione `F5` .  
>     *   Escolha o botão **reproduzir** \ (verde \).  
> 1.  Na lista suspensa, escolha **borda** na lista suspensa.  
> 1.  `launch.json`Deve ser exibido um arquivo que contenha a configuração a seguir.  
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

1.  Para iniciar a ferramenta **elementos** a partir do código do Visual Studio, conclua uma das ações a seguir. 
    *   Selecione `F5` .  
    *   Escolha o botão **reproduzir** \ (verde \).  
         
Agora, você pode executar as seguintes ações.  

*   Acesse o screencast do seu navegador.  
*   Inspecione o DOM e o estilo dos componentes na página.  

## Anexando ao Microsoft Edge  

Para abrir um navegador e anexar a instância ao código do Visual Studio, conclua as etapas a seguir. 

1.  Para abrir uma instância do Microsoft Edge \ (Chromium \), copie e execute o seguinte comando.  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  Depois que a instância iniciar, copie e cole o trecho de código a seguir no seu `launch.json` arquivo.  
    
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
    
1.  No código do Visual Studio, abra o menu suspenso **depurador** e escolha **anexar ao Microsoft Edge e abra as ferramentas de desenvolvedor**.  
1.  Para iniciar a ferramenta **elementos** a partir do código do Visual Studio, conclua uma das ações a seguir. 
    *   Selecione `F5` .  
    *   Escolha o botão **reproduzir** \ (verde \).  
         
Agora, você pode executar as seguintes ações.  

*   Acesse o screencast do seu navegador.  
*   Inspecione o DOM e o estilo dos componentes na página.  
    
## Entrar em contato com o Microsoft Edge DevTools para a equipe de extensão de código do Visual Studio  

Envie seus comentários por meio do [arquivamento de um problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] no [repositório GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.  

Se você quiser ajudar a fazer <!--the Microsoft Edge DevTools for Visual Studio Code -->Esta extensão melhor, suas contribuições são bem-vindos.  Encontre tudo o que você precisa para começar a usar o [repositório do GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Novo problema-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para código VS"  
