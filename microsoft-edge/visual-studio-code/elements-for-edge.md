---
description: Como usar os elementos do Microsoft Edge (Chromium) a partir do código VS
title: Elementos do Microsoft Edge (Chromium) de código VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, elementos
ms.openlocfilehash: ef516d8364c68b550f889bcad0fe762a73ce5f99
ms.sourcegitcommit: 652009c5cea9e75c22b077f0cbcdc0d96bd337ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2020
ms.locfileid: "10694859"
---
# Elementos da extensão de código do Microsoft Edge VS  

Com os [elementos para Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs extensão de código, use a ferramenta elementos do navegador Microsoft Edge de dentro do [código do Visual Studio][VisualstudioCode].  Ao iniciar ou anexar, a ferramenta elementos se conecta a uma instância do Microsoft Edge, exibe a estrutura HTML do tempo de execução e permite que você altere o layout ou corrija problemas de estilo.  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Elementos para Edge VS extensão de código no trabalho":::
   Elementos para Edge VS extensão de código no trabalho  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## Iniciando o Microsoft Edge da extensão de elementos  

Navegue até elementos na **barra de atividades**.  Ao lado de onde ele diz **elementos para Microsoft Edge: targets,** há um sinal de adição que abre o navegador do seu aplicativo.  Se você tiver selecionado a opção **about: Blank** , você deve navegar para o seu aplicativo Web no navegador para que ele apareça no painel de elementos em vs Code.  

## Iniciando o Microsoft Edge a partir do modo de exibição de depuração  

Se você estiver acostumado a usar o modo de exibição de depuração no código do Visual Studio, acesse elementos dessa ferramenta.  Navegue até o modo de exibição de depuração \ ( `Ctrl` + `Shift` + `D` no Windows ou `Command` + `Shift` + `D` no MacOS \).  

Se você não tiver configurações no código do VS, pressione `F5` no Windows ou no MacOS ou selecione o botão de **reprodução** verde. Selecione **borda** na lista suspensa. Você deve ver um `launch.json` arquivo com a configuração a seguir.  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```  

Agora que você carregou a configuração correta, pressione `F5` no Windows ou no MacOS ou selecione o botão de **reprodução** verde. A ferramenta elementos, que é familiar para você, do navegador Microsoft Edge é iniciada no código VS, permitindo que você acesse o screencast do seu navegador e examine os componentes da página.  

## Anexando ao Microsoft Edge  

Para anexar o código VS a uma instância do Microsoft Edge \ (Chromium \), você deve iniciar o navegador executando o seguinte comando no seu terminal.  

`start msedge --remote-debugging-port=9222`  

Depois que o aplicativo for iniciado, adicione a configuração abaixo ao arquivo **. JSON de inicialização** :  

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```  

Selecione **anexar ao Microsoft Edge e abra a ferramenta elementos** no menu suspenso depurador.  Em seguida, pressione `F5` no Windows ou no MacOS ou selecione o botão de **reprodução** verde.  VS o código inicia a ferramenta elementos, permitindo que você acesse o screencast do seu navegador, inspecione o DOM e o estilo dos componentes na página.  

## Entre em contato com os elementos da equipe de extensão de código do Microsoft Edge versus  

Envie seus comentários por meio do [arquivamento de um problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] no [repositório GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.  

Se você quiser ajudar a melhorar a extensão de código do Microsoft Edge VS, suas contribuições serão bem-vindos!  Encontre tudo o que você precisa para começar a usar o [repositório do GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
Elementos [ImagePngElementsEdge]:./Media/Elements-for-Edge.png "para Edge VS extensão de código em ação"  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Elementos para Microsoft Edge VS extensão de código | Documentos da Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Novo problema-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos do Microsoft Edge (Chromium) | Visual Studio Marketplace"  
