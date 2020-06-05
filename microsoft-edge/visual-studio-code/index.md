---
description: Microsoft Edge (Chromium) e código do Visual Studio
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, depurador, dica da Web
ms.openlocfilehash: e178612d9db8ce3223bb5158c4557675d3314e15
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695872"
---
# Visual Studio Code  

O [código do Visual Studio][VisualStudioCodeDocs] é um editor de código-fonte leve e leve, que é executado em sua área de trabalho e está disponível para Windows, MacOS e Linux.  Ele vem com suporte interno para JavaScript, TypeScript e node. js, portanto, é uma ótima ferramenta para desenvolvedores da Web imediatamente!  Se você ainda não o estiver usando, baixe o [código do Visual Studio][VisualstudioCode].  

## Extensões  

<!--Todo: We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Para adquirir qualquer uma das extensões realçadas abaixo, navegue até Extensões \ ( `Ctrl` + `Shift` + `X` no Windows ou `Command` + `Shift` + `X` no MacOS \) em código vs.  

Pesquise o Marketplace para obter a extensão específica e selecione **instalar**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalando o depurador para o Microsoft Edge VS extensão de código":::
   Instalando o depurador para o Microsoft Edge VS extensão de código  
:::image-end:::  

:::row:::
   :::column span="1":::
      ### Depurador para Microsoft Edge  

      Com o [depurador do Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] versus extensão de código, depure o código JavaScript de front-end linha por linha e veja as `console.log()` instruções diretamente do [código do Visual Studio][VisualstudioCode]!  
      
      Usando a ferramenta depurador, você pode iniciar ou anexar tanto ao Microsoft Edge \ (EdgeHTML \) quanto ao Microsoft Edge \ (Chromium \).  Para obter instruções passo a passo para depurar o Microsoft Edge a partir de código e exemplos de configurações do VS `launch.json` , consulte [depurador para extensão de código do Microsoft Edge vs][VscodeDebuggerEdge].  Selecione a imagem a seguir para ver a extensão em ação.  

      :::image type="content" source="./media/debugger-for-edge.png" alt-text="Depurador para borda VS extensão de código em ação" lightbox="./media/debugger-for-edge.gif":::  
   :::column-end:::
   :::column span="1":::
      ### Elementos do Microsoft Edge  
      
      Com os [elementos para Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs extensão de código, use a ferramenta elementos do navegador Microsoft Edge de dentro do código do Visual Studio.  Ao iniciar ou anexar, a ferramenta elementos se conecta a uma instância do Microsoft Edge, exibe a estrutura HTML do tempo de execução e permite que você altere o layout ou corrija problemas de estilo.  
      
      Para obter mais informações, consulte [elementos para Microsoft Edge vs extensão de código][VscodeElementsEdge].  Selecione a imagem a seguir para ver a extensão em ação.  
      
      :::image type="content" source="./media/elements-for-edge.png" alt-text="Elementos para Edge VS extensão de código em ação" lightbox="./media/elements-for-edge.gif":::  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      ### Dica da web
      
      Use [webhint][WebhintMain], uma ferramenta de redimensionamento personalizável, para melhorar a acessibilidade, o desempenho, a compatibilidade entre navegadores, a compatibilidade do PWA e a segurança do seu site.  Ele verifica o código em busca de práticas recomendadas e erros comuns. O projeto de código-fonte aberto da webdica, inicialmente desenvolvido pela equipe do Microsoft Edge, agora faz parte da [Fundação do OpenJS][OpenjsFoundation].  A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores da Web na Comunidade.  <!--Select the following image to see the extension in action.  -->  
      
      :::image type="content" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão de código do webhint VS" lightbox="./media/webhint-extension.png":::  
      
      Identifique e corrija problemas em HTML, CSS, JavaScript, TypeScript e muito mais adicionando a [extensão webhint para o código vs][VisualstudioMarketplaceWebhint].  As dicas aparecem como sublinhados embutidos e são resumidas no painel **problemas** .  
      
      Para obter mais informações, consulte [como usar o webhint no código do Visual Studio][VscodeWebhint].  
   :::column-end:::
   :::column span="1":::
      <!--Empty to retain grid  -->  
   :::column-end:::
:::row-end:::

<!-- image links -->  

<!--links -->  

[VscodeDebuggerEdge]: ./debugger-for-edge.md "Depurador para Microsoft Edge VS extensão de código | Documentos da Microsoft"  
[VscodeElementsEdge]: ./elements-for-edge.md "Elementos para Microsoft Edge VS extensão de código | Documentos da Microsoft"  
[VscodeWebhint]: ./webhint.md "Webhint VS extensão de código | Documentos da Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos do Microsoft Edge (Chromium) | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "Base do OpenJS"  
