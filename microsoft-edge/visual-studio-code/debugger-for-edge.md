---
description: Como depurar o Microsoft Edge (Chromium) e o Microsoft Edge (EdgeHTML) a partir de código VS
title: Depurar o Microsoft Edge (Chromium) a partir de código VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, depurador
ms.openlocfilehash: d9f33a17db7083a6a7cbb013dbf9886755f92c5e
ms.sourcegitcommit: 56cb5821d1b8e96f55bfa14a4ce87a3845b009c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182298"
---
# Depurador para extensão de código do Microsoft Edge VS  

Com o [depurador do Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] versus extensão de código, depure o código JavaScript front-end linha por linha e veja `console.log()` instruções diretamente do [código do Visual Studio][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para Edge VS extensão de código no trabalho":::
   Depurador para Edge VS extensão de código no trabalho  
:::image-end:::

<!--![Debugger for Edge VS Code extension at work][ImageGifDebuggerEdge]  -->  

## Iniciando o Microsoft Edge  

Navegue até o modo de exibição de depuração \ ( `Ctrl` + `Shift` + `D` no Windows ou `Command` + `Shift` + `D` no MacOS \) na **barra de atividades**.  Se você não tiver configurações no código do VS, pressione `F5` no Windows ou no MacOS ou selecione o botão de **reprodução** verde.  Selecione **borda** na lista suspensa.  Você deve ver um `launch.json` arquivo com a configuração a seguir.  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```  

Se você pressionar `F5` o Windows ou o MacOS ou selecionar o botão de **reprodução** verde novamente, o código do vs Inicializa o Microsoft Edge \ (EdgeHTML \) e você poderá depurar qualquer projeto da Web que esteja executando na porta `8080` diretamente do vs Code!  

### Microsoft Edge (Chromium)  

Se você quiser iniciar o Microsoft Edge \ (Chromium \), a próxima versão do Microsoft Edge, em vez do Microsoft Edge \ (EdgeHTML \), basta adicionar um `version` atributo à sua configuração existente com a versão do Microsoft Edge \ (Chromium \) que você deseja iniciar \ ( `stable` ,,, `dev` `beta` ou `canary` \). A seguinte configuração a seguir inicia a versão Canárias do Microsoft Edge \ (Chromium \).  

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```  

## Anexando ao Microsoft Edge  

Anexe o código VS ao Microsoft Edge \ (Chromium \).  Em seu terminal, execute o seguinte comando.  

```console
start msedge --remote-debugging-port=9222
```  

Adicione a configuração abaixo ao seu `launch.json` arquivo.   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

Se agora você executa essa configuração, o código VS é anexado ao Microsoft Edge \ (Chromium \) e inicia a depuração!  

## Entre em contato com os elementos da equipe de extensão de código do Microsoft Edge versus    

Envie seus comentários por meio do [arquivamento de um problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] no [repositório do GitHub][GithubMicrosoftVscodeEdgeDebug2] da extensão.  Inclua o arquivo de log do adaptador de depuração, que é criado para cada execução no `%temp%` diretório com o nome `vscode-edge-debug2.txt` .  Arraste este arquivo para um comentário de problema para carregá-lo no GitHub.  

Para ajudar a melhorar a extensão de código do Microsoft Edge versus o Microsoft Edge, suas contribuições são bem-vindos!  Encontre tudo o que você precisa para começar a usar o [repositório do GitHub][GithubMicrosoftVscodeEdgeDebug2] da extensão.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge VS Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "depurador para borda VS extensão de código em ação"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Novo problema-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
