---
description: O botão Mais Ferramentas, documentação no contexto para começar a usar a extensão DevTools, maior suporte para leitores de tela no Console e muito mais.
title: Novidades no DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ebd512800b8e55b5e9c0001c314a7c08fd242d5d
ms.sourcegitcommit: 30817cd9ae187a716d14d06962eb23b32dd54548
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "11590837"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a>Novidades no DevTools (Microsoft Edge 92)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

> [!TIP]
> A **conferência do Microsoft Build 2021** foi de 25 a 27 de maio.  Veja um vídeo do Build sobre as atualizações para o DevTools: [Microsoft Edge | Estado da plataforma][YoutubeEdgeStateOfThePlatform] - Microsoft Edge uma plataforma atraente e consistente com ferramentas para desenvolvedores.  À medida que nossos navegadores herdados estão sem suporte, o Edge em breve será o único navegador com suporte da Microsoft no Windows 10.  Junte-se a nós para saber mais sobre o mais recente na plataforma de Borda, ferramentas e aplicativos Web.


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a>O botão Fechar não fica mais oculto quando o DevTools é estreito

<!-- Title: DevTools is now easier to close -->  
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->  

Na Microsoft Edge versão 91 ou anterior, o botão Fechar para fechar DevTools não é exibido quando o visor DevTools é estreito. ****  Na Microsoft Edge versão 92, o botão **Fechar** no DevTools está sempre presente, independentemente da largura do viewport DevTools.

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="O botão Fechar DevTools agora está presente mesmo quando o viewport é estreito" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   O **botão Fechar** DevTools agora está presente mesmo quando o viewport é estreito  
:::image-end:::  


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a>Adicionar ferramentas rapidamente com o novo botão Mais Ferramentas

<!-- Title: Add tools quickly with the new More Tools button -->  
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->  

Há uma nova maneira de abrir mais ferramentas no Microsoft Edge DevTools: o menu **Mais Ferramentas** ( `+` ) . O **menu Mais Ferramentas** aparece na barra de ferramentas no painel principal e na barra de ferramentas da gaveta. Selecionar uma ferramenta no menu **Mais Ferramentas** adiciona a ferramenta à barra de ferramentas.

Para reordenar as guias em qualquer barra de ferramentas, selecione e arraste as guias.  

O **menu Mais Ferramentas** estava disponível como um experimento na Microsoft Edge versão 89 e agora está sempre presente.

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="O botão Mais Ferramentas na barra de ferramentas superior e na barra de ferramentas da gaveta" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   O **botão Mais Ferramentas** na barra de ferramentas superior e na barra de ferramentas da gaveta
:::image-end:::  

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="O menu Mais Ferramentas" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   O menu **Mais Ferramentas**
:::image-end:::  


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a>Melhorias para ferramentas de foco, seleção e fechamento

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

Guias para cada ferramenta foram reformatados para reduzir a chance de fechar acidentalmente uma ferramenta.  Em cada guia na barra de ferramentas principal e na barra de ferramentas da gaveta, adicionamos:
*  Espaçamento ao redor da guia.
*  Espaçamento ao redor do botão fechar ( `x` ) na guia.
*  Uma cor de plano de fundo ao passar o mouse sobre a guia.
*  Uma dica de ferramenta para o botão fechar ( `x` ) da guia.
*  Contraste mais alto para o botão fechar ( `x` ) da guia.

Por exemplo, quando você estiver na ferramenta **** **Desempenho** e passar o mouse sobre a guia da ferramenta Rede, essas melhorias ajudam a impedir o fechamento acidental **da ferramenta Rede.**

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Guias antes da reformatação" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           Guias antes da reformatação :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Guias após a reformatação" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           Guias após a reformatação :::image-end:::
    :::column-end:::
:::row-end:::

Essas melhorias são especialmente relevantes para os usuários do DevTools localizado, no qual as guias podem ser mais estreitas e mais fáceis de fechar acidentalmente.

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="DevTools localizado com guias estreitas" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   DevTools localizado com guias estreitas
:::image-end:::

Também facilitamos a nova adição de uma ferramenta que você fechou adicionando um [menu](#add-tools-quickly-with-the-new-more-tools-button) Mais Ferramentas à barra de ferramentas principal e à barra de ferramentas da gaveta.


## <a name="better-support-for-screen-readers-in-the-console"></a>Melhor suporte para leitores de tela no Console

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

Antes da Microsoft Edge versão 92, no **Console,** as tecnologias assistivas, como leitores de tela, não anunciam sugestões de preenchimento automático ou os resultados das expressões avaliadas. Isso foi corrigido agora.

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="No Console, os leitores de tela agora anunciam a sugestão de preenchimento automático selecionado no momento" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           No **Console ,** os leitores de tela agora anunciam a sugestão de preenchimento automático selecionado no momento :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="No Console, os leitores de tela agora anunciam o resultado de uma expressão avaliada" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           No **Console ,** os leitores de tela agora anunciam o resultado de uma expressão avaliada :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a>Microsoft Edge Ferramentas de desenvolvedor Visual Studio Code versão 1.1.8

O [Microsoft Edge ferramentas][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de desenvolvedor para Visual Studio Code versão 1.1.8 do Microsoft Visual Studio Code tem as seguintes alterações desde a versão anterior.  O Microsoft Visual Studio Code atualiza as extensões automaticamente.  Para atualizar manualmente para a versão 1.1.8, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

Você pode registrar problemas e contribuir para a extensão no [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].  

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a>Documentação no contexto e interface do usuário para facilitar o uso da extensão DevTools

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->  
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->  

A versão 1.1.8 do Microsoft Edge [Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension agora apresenta uma maneira mais simples de iniciar uma nova instância do Microsoft Edge, apresentando instruções, botões, links e uma página de documentação para orientá-lo.

*  Quando você seleciona o botão **ferramentas** **** Microsoft Edge na Barra de Atividades do Visual Studio Code, o painel Ferramentas **Microsoft Edge: Destinos** agora apresenta texto explicativo, botões e links para orientá-lo, em vez de um painel em branco.

*  Quando você abre uma nova instância de Microsoft Edge de dentro do Visual Studio Code, o Microsoft Edge agora mostra uma página inicial que explica como usar a extensão Ferramentas do Desenvolvedor, em vez de uma página em branco.

*  O **Microsoft Edge Ferramentas: Destinos** agora tem um botão **Gerar** launch.jsno botão e instruções, para ajudar a iniciar seu projeto para depuração em Microsoft Edge.

Para obter mais informações, navegue [até Usando as ferramentas][GithubIoDevToolsUsing].


## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Usando as ferramentas | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Marketplace de Extensões | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Ferramentas de desenvolvedor para Visual Studio Code | Visual Studio Marketplace"  

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: estado da plataforma | YouTube"

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
