---
description: Microsoft Edge (Chromium) e código do Visual Studio
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, depurador, dica da Web
ms.openlocfilehash: 0d13c6eb9411f89e3a681176ade0caf8d59d46d8
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182725"
---
# Visual Studio Code  

O [código do Visual Studio][VisualStudioCodeDocs] é um editor de código-fonte leve, mas potente.  O [código do Visual Studio][VisualStudioCodeDocs] está disponível para Windows, Linux e MacOS.  Ele inclui suporte interno para JavaScript, TypeScript e Node.js, portanto é uma ótima ferramenta para desenvolvedores da Web antes de você personalizá-lo.  Se você ainda não o estiver usando, baixe o [código do Visual Studio][VisualstudioCode].  

## Extensões  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Para adquirir qualquer uma das extensões realçadas abaixo, navegue até Extensões \ (selecione `Ctrl` + `Shift` + `X` no Windows/Linux ou `Command` + `Shift` + `X` no MacOS \) no código do Visual Studio.  

Pesquise o Marketplace para obter a extensão específica e escolha **instalar**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalar o depurador para extensão de código do Microsoft Edge Visual Studio" lightbox="./media/vscode-debugger-install.png":::
   Instalar o **depurador para extensão de código do Microsoft Edge** Visual Studio  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Depurador para extensão de código do Microsoft Edge Visual Studio" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Depurador para Microsoft Edge** Extensão de código do Visual Studio  
      :::image-end:::  
      [Depurador para Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Extensão de código do Visual Studio de ferramentas do Microsoft Edge para Visual Studio" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Ferramentas do Microsoft Edge para o código do Visual Studio** Extensão de código do Visual Studio  
      :::image-end:::  
      [Ferramentas do Microsoft Edge para o código do Visual Studio](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extensão de código do webdica Visual Studio" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **webhint** Extensão de código do Visual Studio  
      :::image-end:::  
      [Dica da web](#webhint)  
   :::column-end:::
:::row-end:::  

## Depurador para Microsoft Edge  

Com o [depurador para extensão de código do Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio, depure o código JavaScript front-end linha por linha e veja as `console.log()` instruções diretamente do [código do Visual Studio][VisualstudioCode].  
      
Usando a ferramenta depurador, você pode iniciar ou anexar tanto ao Microsoft Edge \ (EdgeHTML \) quanto ao Microsoft Edge \ (Chromium \).  Para obter instruções passo a passo para depurar o Microsoft Edge do Visual Studio e configurações de exemplo `launch.json` , navegue até [depurador para extensão de código do Visual Studio do Microsoft Edge][VisualStudioCodeDebuggerEdge].  Escolha a imagem a seguir para ver a extensão em ação.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Depurador para extensão de código do Edge Visual Studio em ação" lightbox="./media/debugger-for-edge.gif":::
   **Depurador para Microsoft Edge** Extensão de código do Visual Studio em ação  
:::image-end:::  

## Ferramentas do Microsoft Edge para o código do Visual Studio

Com a extensão de código do Visual Studio de código do Visual Studio [Tools do Microsoft Edge][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] , use a ferramenta **elementos** do navegador Microsoft Edge dentro do código do Visual Studio.  Use-o para as seguintes ações.  

*   Anexar a uma instância ou iniciar uma instância do Microsoft Edge.  
*   Exiba a estrutura HTML do tempo de execução.  
*   Atualize o layout.  
*   Corrigir problemas de estilo.  
    
Para obter mais informações, acesse a [extensão de código do Visual Studio de código do Visual Studio para ferramentas do Microsoft Edge][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Extensão de código do Visual Studio de ferramentas do Microsoft Edge para Visual Studio em ação" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Ferramentas do Microsoft Edge para o código do Visual Studio** Extensão de código do Visual Studio em ação  
:::image-end:::  

## Dica da web  
      
Use [webhint][WebhintMain], uma ferramenta de refiapoção personalizável, para melhorar a funcionalidade do seu site a seguir.  

*   Acessibilidade
*   Desempenho
*   Compatibilidade entre navegadores
*   Compatibilidade com o PWA
*   Segurança

Ele verifica o código em busca de práticas de codificação e erros comuns. O projeto de código-fonte aberto da webdica, inicialmente desenvolvido pela equipe do Microsoft Edge, agora faz parte da [Fundação do OpenJS][OpenjsFoundation].  A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores da Web na Comunidade.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão de código do webdica Visual Studio" lightbox="./media/webhint-extension.png":::
   Captura de tela da extensão de código do **webdica** Visual Studio  
:::image-end:::  
      
Identifique e corrija os problemas no seu site adicionando a [extensão webhint para o código do Visual Studio][VisualstudioMarketplaceWebhint].  Dicas examine HTML, CSS, JavaScript, TypeScript e muito mais.  As dicas aparecem como sublinhados embutidos e são resumidas no painel **problemas** .  
      
Para obter mais informações, navegue até [como usar o webhint no código do Visual Studio][VisualStudioCodeWebhint].  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Depurador para extensão de código do Microsoft Edge Visual Studio | Documentos da Microsoft"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Extensão de código do Microsoft Edge DevTools para Visual Studio | Documentos da Microsoft"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio extensão de código | Documentos da Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o código do Visual Studio | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "Base do OpenJS"  
