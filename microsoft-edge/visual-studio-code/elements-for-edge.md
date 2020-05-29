---
description: Como usar os elementos do Microsoft Edge (Chromium) a partir do código VS
title: Elementos do Microsoft Edge (Chromium) de código VS
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, elementos
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562473"
---
# Elementos da extensão de código do Microsoft Edge VS

Ao adicionar os [elementos para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs extensão de código, você pode usar a ferramenta elementos do navegador dentro do [código do Visual Studio](https://code.visualstudio.com/). Ao iniciar ou anexar, a ferramenta elementos será conectada a uma instância do Microsoft Edge, exibirá a estrutura HTML do tempo de execução e permitirá que você altere o layout ou corrija os problemas de estilo.

![GIF dos elementos para Edge VS extensão de código no trabalho](./media/elements-for-edge.gif)

## Iniciando o Microsoft Edge da extensão de elementos 

Navegue até elementos na **barra de atividades**. Ao lado do local em que diz "elementos para Microsoft Edge: targets", há um sinal de adição que abrirá o navegador do seu aplicativo. Se você tiver selecionado a opção *about: Blank* , será preciso navegar até seu aplicativo Web no navegador para que ele seja exibido no painel de elementos em vs Code.

## Iniciando o Microsoft Edge a partir do modo de exibição de depuração

Se você estiver acostumado a usar o modo de exibição de depuração no código do Visual Studio, poderá acessar os elementos dessa ferramenta. Navegue até o modo de exibição de depuração ( `Ctrl`  +  `Shift`  +  `D` no Windows ou `Command`  +  `Shift`  +  `D` no Mac). 

Se você não tiver nenhuma configuração no código do VS, pressione `F5` no Windows ou Mac ou clique no botão de **reprodução** verde. Selecione "borda" na lista suspensa. Agora, você verá um arquivo **inicialização. JSON** com a seguinte configuração:

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

Agora que você carregou a configuração correta, pressione `F5` no Windows ou no Mac ou clique no botão verde **Play** . A ferramenta de elementos com a qual você está familiarizado com o navegador Microsoft Edge agora será iniciada no código VS, permitindo que você acesse o screencast do seu navegador e examine os componentes da página.

## Anexando ao Microsoft Edge
Se quiser anexar o código VS a uma instância do Microsoft Edge (Chromium), você deve iniciar o navegador executando o seguinte comando em seu teminal:

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

Selecione "anexar ao Microsoft Edge e abra a ferramenta elementos" no menu suspenso depurador. Em seguida, pressione `F5` no Windows ou Mac ou clique no botão de **reprodução** verde. O código VS iniciará a ferramenta elementos, permitindo que você acesse o screencast do seu navegador, inspecione o DOM e o estilo dos componentes na página.

## Privacidade Jurídica
Envie-nos seus comentários [arquivando um problema](https://github.com/microsoft/vscode-edge-devtools/issues/new) em relação ao [repositório GitHub](https://github.com/microsoft/vscode-edge-devtools)da extensão. 

Se você quiser nos ajudar a aprimorar essa extensão, Agradecemos suas contribuições! Você pode encontrar tudo o que precisa para começar a usar o [repositório do GitHub](https://github.com/microsoft/vscode-edge-devtools).