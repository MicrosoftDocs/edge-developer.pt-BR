---
description: Os recursos experimentais mais recentes no Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, experimento
ms.openlocfilehash: 612b3b83aee1ee9035982e58e008395ec3645b2b
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408301"
---
# <a name="experimental-features"></a>Recursos experimentais  

O Microsoft Edge DevTools fornece acesso a recursos experimentais que ainda estão em desenvolvimento.  Você pode testar e [fornecer comentários antes](#providing-feedback-on-experimental-features) de cada recurso ser lançado.  

Embora os recursos experimentais estão disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o canal Canary do Microsoft Edge.  

## <a name="turn-on-experimental-features"></a>Ativar recursos experimentais  

Para ativar \(ou desativar\) recursos experimentais no Microsoft Edge, conclua as etapas a seguir.  

1.  [Abra DevTools][DevtoolsOpenIndex].  
    *   Selecione `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` ou \(macOS\).  Para obter mais informações, navegue até Atalhos de teclado [do Microsoft Edge DevTools.][DevtoolsShortcutsIndex]  
1.  Abra o [painel Configurações.][DevToolsCustomizeIndexSettings]  
    *   Selecione `Shift` + `?` .  Para obter mais informações, navegue até Atalhos de teclado [do Microsoft Edge DevTools.][DevtoolsShortcutsIndex]  
1.  No lado esquerdo do painel **Configurações,** escolha a **seção Experimentos.**  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="A página Experimentos em Configurações" lightbox="../media/experiments-devtools.msft.png":::
       A **página Experimentos** **em Configurações**  
    :::image-end:::  
    
1.  Na página **Experimentos,** role a lista de todos os recursos experimentais disponíveis e escolha a caixa de seleção ao lado de cada recurso que você deseja testar.  
1.  Feche e reabra o Microsoft Edge DevTools.  
    
> [!NOTE]
> Os recursos experimentais estão sendo atualizados constantemente e podem causar problemas de desempenho.  Para desativar um recurso experimental, abra a página **Experimentos** e limpe a caixa de seleção do recurso experimental que você deseja desativar.  

## <a name="highlighted-experimental-features"></a>Recursos experimentais realçados  

As seções a seguir descrevem os novos recursos experimentais disponíveis no Microsoft Edge.  

| Recurso experimental | Versão do Microsoft Edge |  
|:--- |:--- |  
| [Habilitar webhint](#enable-webhint) | 85 ou posterior |  
| [Habilitar o Console de Rede](#enable-network-console) | 85 ou posterior |  
| [Visualizador de Ordem de Origem](#source-order-viewer) | 86 ou posterior |  
| [Habilitar camadas compostas no modo de exibição 3D](#enable-composited-layers-in-3d-view) | 87 ou posterior |  
| [Habilitar a nova ferramenta Editor de Fontes no painel Estilos](#enable-new-font-editor-tool-within-the-styles-pane) | 89 ou posterior |  
| [Habilitar novos recursos de depuração do CSS Flexbox](#enable-new-css-flexbox-debugging-features) | 89 ou posterior |  
| [Habilitar + menus de guia de botão para abrir mais ferramentas](#enable--button-tab-menus-to-open-more-tools) | 89 ou posterior |  
| [Habilitar a guia Bem-vindo](#enable-welcome-tool) | 89 ou posterior |  

### <a name="enable-webhint"></a>Habilitar webhint  

[webhint][WebhintMain] é uma ferramenta de código aberto que fornece comentários em tempo real para sites e páginas da Web locais.  O tipo de comentários fornecido pela [webhint][WebhintMain].  

*   acessibilidade  
*   Compatibilidade entre navegadores  
*   segurança  
*   performance  
*   Aplicativos Web Progressivos (PWAs)  
*   outros problemas comuns de desenvolvimento da Web  
    
O [experimento webhint][WebhintMain] exibe os comentários webhint no painel [Problemas.][DevtoolsIssuesIndex]  Escolha um problema para exibir a documentação da solução e uma lista dos recursos afetados em seu site.  Escolha um link de recurso para abrir o painel **Rede,** **Fontes**ou **Elementos** relevantes no DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentários webhint no painel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   comentários webhint no painel **Problemas**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a>Habilitar o Console de Rede  

**Console de** Rede é o título de trabalho de um experimento para fazer solicitações de rede sintéticas por HTTP.  Você pode usar o experimento **de Console de Rede** para enviar solicitações de API da Web.  

Depois de ativar o experimento, reinicie o DevTools.  Para usar o **Console de Rede,** conclua as etapas a seguir.  

1.  Abra o **painel** Rede.  
1.  Encontre a solicitação de rede que você deseja alterar e reendá-la.  
1.  Abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Editar e Repetir**.  
1.  Quando o **Console de Rede** for aberto, edite as informações de solicitação de rede.  
1.  Escolha **Enviar**.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console de rede na gaveta console" lightbox="../media/network-network-console.msft.png":::
   **Console de rede** na gaveta **console**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a>Visualizador de Ordem de Origem  

**O Visualizador de Ordem de** Origem é um experimento que exibe a ordem dos elementos na origem da página da Web.  A ordem de exibição na tela pode ser diferente da ordem da origem, o que confundiu usuários de leitor de tela e teclado.  Use o **experimento Visualizador de Ordem** de Origem para encontrar as diferenças entre a ordem de exibição na tela e a ordem da fonte.  

Depois de ativar o experimento, reinicie o DevTools.  Para usar **o Visualizador de Ordem de**Origem, conclua as etapas a seguir.  

1.  Abra a **ferramenta Elements.**  
1.  Abra o **painel Acessibilidade** no painel de gaveta \(bottom\)  
1.  Na seção **Visualizador de Ordem de** Origem, escolha a caixa de seleção **Mostrar Ordem** de Origem.  
1.  Realça qualquer elemento HTML para exibir uma sobreposição que a ordem na origem da página da Web.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visualizador de Ordem de Origem no painel Acessibilidade" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Visualizador de Ordem de** Origem no painel **Acessibilidade**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a>Habilitar camadas compostas no modo de exibição 3D  

Agora você pode visualizar Layers juntamente com índices z e o Modelo de Objeto de Documento \(DOM\).  Esse recurso ajuda você a depurar sem alternar contextos com a mesma frequência.  Você identificou que a redução da alternção de contexto era um grande ponto de dor.  Nem sempre é claro como o código que você escreve afeta seu aplicativo Web.  Para uma experiência de depuração visual abrangente, o Modo de exibição 3D e as camadas compostas agora são combinados.  

Depois de ativar o experimento, reinicie o DevTools.  Para usar **Camadas Compostas,** conclua as etapas a seguir.  

1.  Na gaveta, escolha a ferramenta De exibição **3D.**  
1.  Abra o **painel Camadas Compostas.**  
1.  Todas as camadas pintadas do aplicativo são exibidas.  Experimente esse recurso com seus próprios aplicativos Web.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Painel de Camadas compostas" lightbox="../media/experiments-layers.msft.png":::
   Painel de **Camadas Compostas**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a>Habilitar a nova ferramenta Editor de Fontes no painel Estilos  

Agora você pode usar o novo Editor de [Fonte visual][DevtoolsInspectStylesEditFonts] para editar fontes.  Use-o para definir fontes e características de fonte.  O Editor **de Fonte visual** ajuda você a concluir as seguintes ações.  

*   Alternar entre unidades para propriedades de fonte diferentes  
*   Alternar entre palavras-chave para propriedades de fonte diferentes  
*   Converter unidades  
*   Gerar código CSS preciso  
    
Depois de ativar o experimento, reinicie o DevTools.  Para usar o novo Editor de **Fonte visual,** conclua as etapas a seguir.  

1.  Abra a **ferramenta Elements.**  
1.  Abra o **painel Estilos.**  
1.  Escolha o **ícone editor de** fontes.  
    
Para obter mais informações sobre o novo Editor de **Fontes visuais,** navegue até Editar estilos de fonte CSS e configurações no [painel Estilos em DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="O painel editor de fontes visual é realçado" lightbox="../media/font-editor-open.msft.png":::
   O painel **editor de fontes** visual é realçado  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a>Habilitar novos recursos de depuração do CSS Flexbox  

Esse recurso experimental fornece muitas novas visualizações para ajudá-lo a depurar layouts do CSS Flexbox.  Para visualizar os recursos experimentais mais recentes, [a ligue este experimento](#turn-on-experimental-features) e recarregue o DevTools.  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a>Exibir sobreposições persistentes em layouts do Flexbox com a ferramenta Inspecionar  

A **ferramenta Inspect** fornece uma maneira rápida de identificar e visualizar layouts do CSS Flexbox em um site, pairando sobre eles com o mouse.  Escolha o **ícone Inspecionar** \( ![ Inspecionar ](../media/inspect-icon.msft.png) \) no canto superior esquerdo do DevTools.  Em seguida, durante a depuração do site, passe o mouse em um contêiner flexível para exibir contornos ao redor do contêiner flexível.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Exibir contêineres do Flexbox com a ferramenta Inspecionar" lightbox="../media/flexbox-hover.msft.png":::
   Exibir contêineres do Flexbox com a **ferramenta Inspecionar**  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a>Exibir sobreposições persistentes em layouts do Flexbox  

No Microsoft Edge versão 89 ou posterior, o recurso experimental CSS Flexbox também oferece a opção de ativar sobreposições persistentes em layouts do Flexbox.  Sobreposições persistentes fornecem os seguintes benefícios.  

*   As sobreposições persistentes permanecem visíveis na página da Web à medida que você rola, move o mouse e usa outros recursos do DevTools.
*   Várias sobreposições persistentes podem ser usadas ao mesmo tempo, para permitir que você revise vários layouts do Flexbox ao mesmo tempo.  
*   Sobreposições persistentes oferecem opções de configuração de cores.  
    
Para alternar sobreposições persistentes no layout do Flexbox, use uma das seguintes ações.  

*   Escolha o ícone de oval **Flexbox** ao lado de qualquer contêiner Flexbox exibido na árvore DOM da **ferramenta Elements.**  
*   Abra o novo **painel layout** localizado na ferramenta **Elementos** e escolha a caixa de seleção ao lado de cada contêiner do Flexbox que você deseja realçar.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Ícones flexíveis e painel layout no DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Ícones flexíveis **e painel layout** no DevTools  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a>Configurar sobreposições persistentes  

Para configurar opções para sobreposições persistentes para grades CSS ou layouts do Flexbox, use o **painel Layout.**  O **painel Layout** está localizado na ferramenta **Elements** ao lado dos painéis **Estilos** **e** Calculados.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Painel de layout" lightbox="../media/flexbox-layout.msft.png":::
   Painel de layout  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a>Habilitar + menus de guia de botão para abrir mais ferramentas  

Agora você pode abrir mais ferramentas usando o novo ícone **Mais Ferramentas** \( `+` \)  Depois de ativar os **menus** de guia Habilitar + botão para abrir mais ferramentas experimento e recarregar DevTools, um sinal de a mais \( \) é exibido à direita do grupo de guias na parte superior `+` do DevTools.  Para exibir uma lista de outras ferramentas que você pode adicionar à barra de guias, escolha o novo ícone **Mais Ferramentas** \( `+` \).  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Mais Ferramentas no painel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Mais Ferramentas** no painel superior
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a>Habilitar a ferramenta Bem-vindo

Este experimento substitui a **ferramenta Novidades** pela nova ferramenta **de Boas-vindas.**  Ele exibe um design atualizado para o conteúdo a seguir.  

*   Links para documentos de desenvolvedor  
*   os recursos mais recentes  
*   notas de versão  
*   Opção para entrar em contato com a equipe do Microsoft Edge DevTools  
    
A **ferramenta Bem-vindo** é aberta automaticamente após cada atualização para o Microsoft Edge.  Para impedir a exibição da ferramenta **De** boas-vindas após cada atualização, deslocar a caixa de seleção ao lado da guia **Abrir** após cada atualização sob o **título** da ferramenta de boas-vindas.  

Se você preferir a ferramenta **Original Novidades,** navegue até [Configurações Experimentos][DevtoolsCustomizeIndexSettings]e remova a caixa de seleção ao lado da guia  >  **** Habilitar **Boas-vindas.**  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Ferramenta de boas-vindas" lightbox="../media/experiments-welcome.msft.png":::
   **Ferramenta de boas-vindas**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Recursos experimentais anteriores  

*   [O Modo de Exibição 3D][Devtools3dViewIndex] agora está disponível e ligado por padrão no Microsoft Edge versão 83 ou posterior.  
*   [Ativar o suporte para mover guias][DevtoolsCustomizeIndex] entre painéis agora está disponível e ligado por padrão no Microsoft Edge versão 85 ou posterior.  
*   [Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.  
*   Editar atalhos de teclado para qualquer ação no [DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] agora está disponível e ativado por padrão no Microsoft Edge versão 89 ou posterior.  
*   [Ativar novos recursos de depuração][DevtoolsCssGrid] de grade CSS agora está disponível e ligado por padrão no Microsoft Edge versão 89 ou posterior.  
*   [Emulação: o modo de tela dupla][DevtoolsDeviceModeDualScreenAndFoldables] de suporte agora está disponível e ligado por padrão no Microsoft Edge versão 90 ou posterior.  

    
## <a name="providing-feedback-on-experimental-features"></a>Fornecendo comentários sobre recursos experimentais  

Para fornecer comentários sobre experimentos do Microsoft Edge DevTools ou qualquer outra coisa relacionada ao DevTools.  

*   Enviar seus comentários usando o **ícone Enviar Comentários** no DevTools  
*   Tweet no [@EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Comentários no Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   O **ícone Enviar Comentários** no Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Modo de exibição 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspecionar Grade CSS no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Editar atalhos de teclado para qualquer ação no devTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos de fonte CSS e configurações no painel Estilos no DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevtoolsOpenIndex]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Atalhos de teclado do Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de tela dupla e dobráveis no Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
