---
description: Microsoft Edge (Chromium) e Visual Studio Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, vs code, código do visual studio, depurador, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230688"
---
# Visão geral do Visual Studio Code  

[Visual Studio Code][VisualStudioCodeDocs] é um editor de código-fonte leve, mas poderoso.  [Visual Studio Code][VisualStudioCodeDocs] está disponível para Windows, Linux e macOS.  Ele inclui suporte integrado para JavaScript, TypeScript e Node.js, portanto, é uma ótima ferramenta para desenvolvedores da Web antes de personalizá-lo.  Se você ainda não estiver usando, baixe [Visual Studio Code][VisualstudioCode].  

##  <a name="extensions"></a>Extensões  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Para adquirir qualquer uma das extensões realçadas abaixo, navegue até Extensões \(selecione em `Ctrl` + `Shift` + `X` Windows/Linux ou `Command` + `Shift` + `X` no macOS\) no Visual Studio Code.  

Pesquise o Marketplace para a extensão específica e escolha **Instalar**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalar o Depurador para Microsoft Edge Visual Studio Code extensão" lightbox="./media/vscode-debugger-install.png":::
   Instalar o **Depurador para Microsoft Edge** Visual Studio Code extensão  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Depurador para Microsoft Edge Visual Studio Code extensão" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Depurador para Microsoft Edge** Visual Studio Code extensão  
      :::image-end:::  
      [Depurador para Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Ferramentas para Visual Studio Code Visual Studio Code extensão" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Microsoft Edge Ferramentas para Visual Studio Code** Visual Studio Code extensão  
      :::image-end:::  
      [Microsoft Edge Ferramentas para Visual Studio Code](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="webhint Visual Studio Code extensão" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **webhint** Visual Studio Code extensão  
      :::image-end:::  
      [Dica da web](#webhint)  
   :::column-end:::
:::row-end:::  

##  <a name="debugger-for-microsoft-edge"></a>Depurador para Microsoft Edge  

Com o [Depurador][VisualstudioMarketplaceDebuggerMicrosoftEdge] para Microsoft Edge Visual Studio Code, depure seu código javaScript front-end linha por linha e consulte instruções diretamente de `console.log()` [Visual Studio Code][VisualstudioCode].  
      
Usando a ferramenta Depurador, você pode iniciar ou anexar Microsoft Edge \(EdgeHTML\) e Microsoft Edge \(Chromium\).  Para um passo a passo de depuração Microsoft Edge de configurações Visual Studio Code exemplo e de exemplo, navegue até `launch.json` [Depurador para Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].  Escolha a imagem a seguir para ver a extensão em ação.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Depurador para extensão Visual Studio Code de Borda em ação" lightbox="./media/debugger-for-edge.gif":::
   **Depurador para Microsoft Edge** Visual Studio Code extensão em ação  
:::image-end:::  

##  <a name="microsoft-edge-tools-for-visual-studio-code"></a>Microsoft Edge Ferramentas para Visual Studio Code

Com a [Microsoft Edge ferramentas para Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code, use a ferramenta **Elements** do navegador Microsoft Edge no Visual Studio Code.  Use-o para as seguintes ações.  

*   Anexar a uma instância ou iniciar uma instância de Microsoft Edge.  
*   Exibe a estrutura HTML do tempo de execução.  
*   Atualize o layout.  
*   Correção de problemas de estilo.  
    
Para obter mais informações, navegue [até Microsoft Edge Ferramentas para Visual Studio Code Visual Studio Code extensão][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Ferramentas para Visual Studio Code Visual Studio Code extensão em ação" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Microsoft Edge Ferramentas para Visual Studio Code** Visual Studio Code em ação  
:::image-end:::  

##  <a name="webhint"></a>Dica da web  
      
Use [webhint][WebhintMain], uma ferramenta de linting personalizável, para melhorar a funcionalidade a seguir do seu site.  

*   Acessibilidade
*   Desempenho
*   Compatibilidade entre navegadores
*   PWA compatibilidade
*   Segurança

Ele verifica seu código em busca de práticas de codificação e erros comuns. O projeto de código aberto webhint, inicialmente desenvolvido pela equipe Microsoft Edge, agora faz parte do [OpenJS Foundation][OpenjsFoundation].  A Microsoft Edge equipe continua a contribuir para Webhint junto com os desenvolvedores da Web na comunidade.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão Visual Studio Code webhint" lightbox="./media/webhint-extension.png":::
   Captura de tela **da extensão Visual Studio Code webhint**  
:::image-end:::  
      
Identifique e corrige problemas em seu site adicionando a [extensão webhint para Visual Studio Code][VisualstudioMarketplaceWebhint].  As dicas examinam HTML, CSS, JavaScript, TypeScript e muito mais.  As dicas aparecem como sublinhados em linha e são resumidas no painel **Problemas.**  
      
Para obter mais informações, navegue [até Como usar webhint em Visual Studio Code][VisualStudioCodeWebhint].  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Depurador para Microsoft Edge Visual Studio Code extensão | Microsoft Docs"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools para Visual Studio Code extensão | Microsoft Docs"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio Code Extension | Microsoft Docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Visual Studio Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
