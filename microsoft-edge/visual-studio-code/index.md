---
description: Microsoft Edge (Chromium) e código do Visual Studio
title: Visual Studio Code
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, depurador, dica da Web
ms.openlocfilehash: 94148864edbd43adbe2dc9f3d0c2fa0c1f7f0b43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562472"
---
# Visual Studio Code

O [código do Visual Studio](https://code.visualstudio.com/Docs) é um editor de código-fonte leve, mas potente, que é executado em sua área de trabalho e está disponível para Windows, MacOS e Linux. Ele vem com suporte interno para JavaScript, TypeScript e node. js, portanto, é uma ótima ferramenta para desenvolvedores da Web imediatamente! Vá até [esta página](https://code.visualstudio.com/) para baixar o código do Visual Studio se você ainda não o estiver usando.

## Extensões

<!-- We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page. I think it's a web page. I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->

Para adquirir qualquer uma das extensões realçadas abaixo, navegue até extensões ( `Ctrl`  +  `Shift`  +  `X` no Windows ou `Command`  +  `Shift`  +  `X` no Mac) no código vs.

Pesquise o Marketplace para obter a extensão específica e selecione **instalar**.

![Instalando o depurador para o Microsoft Edge VS extensão de código](./media/vscode-debugger-install.png)

## Depurador para Microsoft Edge

Depure o código JavaScript front-end linha por linha e exibir `console.log()` instruções diretamente no [código do Visual Studio](https://code.visualstudio.com/) usando a extensão de código do [depurador para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs!

Use o [depurador para o Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código para iniciar ou anexar ao Microsoft Edge (EdgeHTML) e ao Microsoft Edge (Chromium). Confira [esta página](./debugger-for-edge.md) para obter um guia passo a passo de como depurar o Microsoft Edge de código vs e configurações de lançamento de exemplo **. JSON** .

![GIF do depurador para Edge VS extensão de código em Action!](./media/debugger-for-edge.gif)

## Elementos do Microsoft Edge

Ao adicionar os [elementos para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs extensão de código, você pode usar a ferramenta elementos do navegador dentro do código do Visual Studio. Ao iniciar ou anexar, a ferramenta elementos será conectada a uma instância do Microsoft Edge, exibirá a estrutura HTML do tempo de execução e permitirá que você altere o layout ou corrija os problemas de estilo.

Para obter mais informações, confira [esta página](./elements-for-edge.md).

![GIF dos elementos para Edge VS extensão de código em Action!](./media/elements-for-edge.gif)

## webhint

Use [webhint](https://webhint.io), uma ferramenta de redimensionamento personalizável, para melhorar a acessibilidade, o desempenho, a compatibilidade entre navegadores, a compatibilidade do PWA e a segurança do seu site. Ele verifica o código em busca de práticas recomendadas e erros comuns. Este projeto de código aberto, inicialmente desenvolvido pela equipe Microsoft Edge, agora faz parte da [Fundação OpenJS](https://openjsf.org/). A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores da Web na Comunidade.

![Captura de tela da extensão de código do webhint VS](./media/webhint-extension.png)

Identifique e corrija problemas em HTML, CSS, JavaScript, TypeScript e muito mais adicionando a [extensão webhint para o código vs](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint). As dicas aparecem como sublinhados embutidos e são resumidas no painel problemas.

Para obter mais informações, consulte [como usar o webhint no código do Visual Studio](./webhint.md).
