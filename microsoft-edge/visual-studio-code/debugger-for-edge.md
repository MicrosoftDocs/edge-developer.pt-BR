---
description: Como depurar Microsoft Edge (Chromium) e Microsoft Edge (EdgeHTML) Visual Studio Code
title: Depurar Microsoft Edge (Chromium) de Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, vs code, código do visual studio, depurador
ms.openlocfilehash: e36348fc1ef5e30a511e6eda73c7646a85d8717e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399292"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a>Depurador para Microsoft Edge Visual Studio Code Extension  

Com o [Depurador][VisualstudioMarketplaceDebuggerMicrosoftEdge] para Microsoft Edge Visual Studio Code, depure sua linha de código JavaScript front-end por linha e consulte instruções diretamente do `console.log()` [Visual Studio Code][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador de borda Visual Studio Code extensão no trabalho" lightbox="./media/debugger-for-edge.gif":::
   Depurador de borda Visual Studio Code extensão no trabalho  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a>Iniciando Microsoft Edge  

Navegue até o exibição de depuração \( `Ctrl` + `Shift` + `D` no Windows ou `Command` + `Shift` + `D` no macOS\) na Barra **de Atividades.**  Se você não tiver nenhuma configuração no Visual Studio Code, selecione no Windows ou macOS ou `F5` selecione o botão verde **Reproduzir.**  Selecione **Borda** no menu suspenso.  Você deve ver um `launch.json` arquivo com a configuração a seguir.  

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

Se você selecionar no Windows ou macOS ou selecionar o botão verde Reproduzir novamente, o Visual Studio Code iniciará o `F5` Microsoft Edge \(EdgeHTML\) e poderá **** depurar qualquer projeto web executado na porta diretamente do `8080` Visual Studio Code!  

### <a name="microsoft-edge-chromium"></a>Microsoft Edge (Chromium)  

Se você quiser iniciar o Microsoft Edge \(Chromium\), o novo Microsoft Edge, em vez de Microsoft Edge \(EdgeHTML\), basta adicionar um atributo à configuração existente com a versão do Microsoft Edge \(Chromium\) que deseja iniciar `version` \( `dev` , ou `beta` `canary` \).  A configuração a seguir inicia a versão canária do Microsoft Edge \(Chromium\).  

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

## <a name="attaching-to-microsoft-edge"></a>Anexando a Microsoft Edge  

Anexe Visual Studio Code Microsoft Edge \(Chromium\).  No terminal, execute o seguinte comando.  

```shell
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

Se você executar essa configuração agora, Visual Studio Code anexa a Microsoft Edge \(Chromium\) e iniciar a depuração.  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a>Entrar em contato com a equipe de Microsoft Edge Visual Studio Code de extensão    

Envie seus comentários [arquivando um problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] no GitHub [da][GithubMicrosoftVscodeEdgeDebug2] extensão.  Inclua o arquivo de log do adaptador de depuração, que é criado para cada executar no `%temp%` diretório com o nome `vscode-edge-debug2.txt` .  Arraste esse arquivo para um comentário de problema para enviá-lo para GitHub.  

Para ajudar a melhorar a extensão Elements for Microsoft Edge Visual Studio Code, suas contribuições são bem-vindas!  Encontre tudo o que você precisa para começar [GitHub o repo][GithubMicrosoftVscodeEdgeDebug2] da extensão.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Depurador para Visual Studio Code de Borda em ação"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Novo problema - microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador do Microsoft Edge | Visual Studio Marketplace"  
