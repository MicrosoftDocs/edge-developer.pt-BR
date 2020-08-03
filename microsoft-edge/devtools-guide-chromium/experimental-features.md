---
description: Os recursos experimentais mais recentes do Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/21/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, experimento
ms.openlocfilehash: 6b3e1c06d6b8ed79054c28df483fcca93e5751d6
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902848"
---
# Recursos experimentais  

Você pode usar os recursos experimentais que ainda estão em desenvolvimento no Microsoft Edge DevTools para testar e [fornecer comentários](#providing-feedback-on-experimental-features) antes que cada um seja liberado amplamente.  

Embora os recursos experimentais estejam disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o Microsoft Edge Canárias Channel.  

## Ativar os recursos experimentais  

Use as etapas a seguir para ativar \ (ou desligado \) recursos experimentais no Microsoft Edge.  

1.  [Abra o devtools][DevtoolsOpen].  
     *   Selecione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  
1.  Abra o painel [configurações][DevToolsCustomizeSettings] .  
    *   Selecione `Shift` + `?` .  Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  
1.  No lado esquerdo do painel **configurações** , selecione a seção **experimentos** .  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-devtools.png":::
       Lista de experimentos nas configurações do DevTools  
    :::image-end:::  
    
1.  Na página **experimentos** , percorra a lista de todos os recursos experimentais disponíveis e marque a caixa de seleção ao lado de cada recurso que você deseja testar.  
1.  Feche e abra novamente o Microsoft Edge DevTools.  

> [!NOTE]
> Os recursos experimentais são atualizados constantemente e podem causar problemas de desempenho.  Para desativar um recurso experimental, abra a página **experimentos** e desmarque a caixa de seleção do recurso experimental que você deseja desativar.  

## Recursos experimentais realçados  

As seções a seguir descrevem os novos recursos experimentais que estão disponíveis no Microsoft Edge.  

| Recurso experimental | Microsoft Edge versão |  
|:--- |:--- |  
| [Habilitar a guia Configurações de atalhos de teclado personalizados](#enable-custom-keyboard-shortcuts-settings-tab) | 84 ou posterior |
| [Habilitar novos recursos de depuração de grade CSS](#enable-new-css-grid-debugging-features) | 85 ou posterior |  
| [Habilitar o suporte para mover as guias entre painéis](#enable-support-to-move-tabs-between-panels) | 85 ou posterior |  
| [Habilitar webhint](#enable-webhint) | 85 ou posterior | 
| [Habilitar console de rede](#enable-network-console) | 85 ou posterior |

### Habilitar a guia Configurações de atalhos de teclado personalizados

Fornece uma nova página **atalhos** nas [configurações do devtools][DevToolsCustomizeSettings] que habilita os [atalhos de teclado][DevToolsShortcuts] correspondentes no [código][VisualstudioCode]do devtools para o vs.  

Depois de habilitar o experimento, abra [as configurações do devtools][DevToolsCustomizeSettings] novamente usando selecionar `Shift` + `?` .  Navegue até a página novos **atalhos** .  Selecione **devtools (padrão)** na lista suspensa **coincidir os atalhos de predefinir** e selecione **código do Visual Studio**.  Os atalhos de teclado no DevTools agora correspondem aos atalhos para ações equivalentes no código VS.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Corresponder os atalhos de teclado no DevTools código do VS" lightbox="./media/experiments-keyboard-shortcut.png":::
   Corresponder os atalhos de teclado no DevTools código do VS
:::image-end:::  

Por exemplo, no Windows, o atalho de teclado para pausar ou continuar a execução de um script em um [código vs][VisualstudioCodeShortcutsKeyboardWindows] é `F5` .  Com a predefinição **devtools (padrão)** , o mesmo atalho no devtools é `F8` .  Com a predefinição de **código do Visual Studio** , o atalho também é `F5` .  

### Habilitar novos recursos de depuração de grade CSS  

Aprimora as visualizações na página quando você depura sites que têm layouts de grade CSS.  Você pode personalizar ainda mais as sobreposições nas configurações do DevTools.  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Recurso de depuração de grade CSS" lightbox="./media/experiments-grid.png":::
   Recurso de depuração de grade CSS  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar o suporte para mover as guias entre painéis  

Normalmente, ferramentas como **elementos** e **rede** só podem ser abertas no painel main \ (Top \) do devtools.  Da mesma forma, ferramentas como **modo de exibição 3D** e **problemas** só podem ser abertos no painel gaveta \ (inferior \) do devtools.  Ao escolher o experimento, você pode mover ferramentas entre os painéis superior e inferior passando o mouse sobre a guia, abrindo o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início** ou **mover para o fim**.   Este experimento permite que você personalize o layout do DevTools.  Para mostrar ou ocultar o painel inferior, selecione `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Mover guias entre painéis" lightbox="./media/experiments-move-panels.png":::
   Mover guias entre painéis  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar webhint  

[webhint][WebhintMain] é uma ferramenta de código-fonte aberto que fornece comentários em tempo real sobre a acessibilidade, a compatibilidade entre navegadores, a segurança, o desempenho, a PWAs e outras questões de desenvolvimento da Web comuns dos sites.  O experimento da [webhint][WebhintMain] traz o comentário webhint para devtools no painel [problemas][DevtoolsIssues] .  Você pode selecionar o problema para ver a documentação sobre como corrigir o problema e uma lista dos recursos afetados em seu site.  Selecione um link de recurso para abrir o painel de **rede**, **fontes**ou **elementos** relevantes no devtools.  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Comentários da webhint no painel problemas" lightbox="./media/experiments-webhint.png":::
   Comentários da webhint no painel problemas  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar console de rede

**Console de rede** é o título de trabalho de um experimento para fazer solicitações de rede sintéticas por http.  Você pode usar o experimento do **console de rede** para enviar solicitações de API da Web.  

Depois de habilitar o experimento, certifique-se de reiniciar o DevTools. Para usar o console de rede:
1.  Abra o painel **rede** .
1.  Localize a solicitação de rede que você deseja alterar e envie novamente.
1.  Abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **Editar e reproduzir**. 
1.  Quando o **console de rede** for aberto, edite as informações de solicitação de rede.
1.  Selecione **Enviar**.  

:::image type="complex" source="./media/network-network-console.png" alt-text="Console de rede na gaveta do console" lightbox="./media/network-network-console.png":::
Console de rede na gaveta do console
:::image-end::: 

<!--Available in Microsoft Edge version 85 and later.  --> 

## Recursos experimentais anteriores  

*   o [modo de exibição 3D][Devtools3dViewIndex] agora está disponível e ativado por padrão no Microsoft Edge versão 83 ou posterior.  

## Fornecer comentários sobre os recursos experimentais  

Para fornecer comentários sobre o Microsoft Edge DevTools experimentos ou qualquer outro item relacionado ao DevTools.  

*   Envie seus comentários usando o ícone de comentários no DevTools  
*   Tweet em [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Ícone de comentários no Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   Ícone de comentários no Microsoft Edge DevTools  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Modo de exibição 3D | Documentos da Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge | Documentos da Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsOpen]: ./open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Atalhos de teclado de código do Visual Studio para Windows | Código do Visual Studio"  

[WebhintMain]: https://webhint.io "webhint" 
