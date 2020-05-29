---
description: Como depurar o Microsoft Edge (Chromium) e o Microsoft Edge (EdgeHTML) a partir de código VS
title: Depurar o Microsoft Edge (Chromium) a partir de código VS
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, depurador
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562469"
---
# Depurador para extensão de código do Microsoft Edge VS

Com o [depurador para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código, você pode depurar o código JavaScript front-end linha por linha e ver `console.log()` instruções diretamente do [código do Visual Studio](https://code.visualstudio.com/)!

![GIF do depurador para Edge VS extensão de código no trabalho](./media/debugger-for-edge.gif)

## Iniciando o Microsoft Edge

Navegue até o modo de exibição de depuração ( `Ctrl`  +  `Shift`  +  `D` no Windows ou `Command`  +  `Shift`  +  `D` no Mac) na **barra de atividades**. Se você não tiver nenhuma configuração no código do VS, pressione `F5` no Windows ou Mac ou clique no botão de **reprodução** verde. Selecione "borda" na lista suspensa. Agora, você verá um arquivo **inicialização. JSON** com a seguinte configuração:

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

Se você agora pressionar `F5` no Windows ou Mac ou clicar no botão verde de **reprodução** novamente, o código do vs iniciará o Microsoft Edge (EdgeHTML) e você poderá depurar qualquer projeto Web que você esteja executando na porta **8080** diretamente de um código vs!

### Microsoft Edge (Chromium)

Se você quiser iniciar o Microsoft Edge (Chromium), a próxima versão do Microsoft Edge, em vez do Microsoft Edge (EdgeHTML), basta adicionar um `version` atributo à sua configuração existente com a versão do Microsoft Edge (Chromium) que você deseja iniciar ( `dev` , `beta` ou ou `canary` ). A configuração a seguir inicializará a versão Canárias do Microsoft Edge (Chromium):

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

Você também pode anexar o código VS ao Microsoft Edge (Chromium). Em seu terminal, execute o seguinte comando:

`start msedge --remote-debugging-port=9222`

Adicione a configuração abaixo ao arquivo **. JSON de inicialização** :

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

Se agora você executar essa configuração, o código do VS será anexado ao Microsoft Edge (Chromium) e você poderá iniciar a depuração!

## Privacidade Jurídica

Envie-nos seus comentários [arquivando um problema](https://github.com/Microsoft/vscode-edge-debug2/issues/new) em relação ao [repositório GitHub](https://github.com/Microsoft/vscode-edge-debug2)da extensão. Inclua o arquivo de log do adaptador de depuração, que é criado para cada execução no diretório% Temp% com o nome `vscode-edge-debug2.txt` . Você pode arrastar esse arquivo para um comentário de questão para carregá-lo no GitHub.

Se você quiser nos ajudar a aprimorar essa extensão, Agradecemos suas contribuições! Você pode encontrar tudo o que precisa para começar a usar o [repositório do GitHub](https://github.com/Microsoft/vscode-edge-debug2).