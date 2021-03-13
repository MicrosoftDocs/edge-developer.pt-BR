---
description: Corresponder atalhos de teclado no DevTools para Visual Studio Código
title: Personalizar atalhos de teclado no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, personalizado, atalhos, teclado, código do visual studio
ms.openlocfilehash: ec48b075ff6741e0905e963993e7ca4e5dabe714
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408280"
---
# <a name="customize-keyboard-shortcuts-in-the-microsoft-edge-devtools"></a>Personalizar atalhos de teclado no Microsoft Edge DevTools  

A **página Atalhos** em [Configurações][DevToolsCustomizeSettings] fornece uma lista de atalhos de teclado no [DevTools][DevToolsShortcuts] e recursos para personalizar [os atalhos.](#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code)  Para navegar até a página **Atalhos,** conclua as etapas a seguir.  

1.  [Abra DevTools][DevtoolsOpenMain].  
1.  Configurações [abertas][DevToolsCustomizeSettings].
    *   Selecione `Shift` + `?` .  
1.  Navegue até **a página Atalhos.**  
    
    :::image type="complex" source="../media/settings-shortcuts.msft.png" alt-text="A página Atalhos em Configurações" lightbox="../media/settings-shortcuts.msft.png":::
       A **página Atalhos** **em Configurações**  
    :::image-end:::  
    
## <a name="match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code"></a>Corresponder atalhos de teclado no DevTools ao Código Visual Studio Microsoft  

Para corresponder ao atalho do teclado no Microsoft Edge DevTools para uma ação equivalente Visual Studio [Código][VisualStudioCode], conclua as etapas a seguir.  

1.  Navegue até a página da Web [Atalhos.](#customize-keyboard-shortcuts-in-the-microsoft-edge-devtools)  
1.  Escolha Os **atalhos de match no** menu suspenso predefinido e altere **DevTools (Padrão)** para **Visual Studio Código**.  
    
    :::image type="complex" source="../media/match-keyboard-shortcuts-visual-studio-code.msft.png" alt-text="Corresponder atalhos de teclado no DevTools para Visual Studio Código" lightbox="../media/match-keyboard-shortcuts-visual-studio-code.msft.png":::
       Corresponder atalhos de teclado no DevTools para Visual Studio Código  
    :::image-end:::  
    
Por exemplo, para pausar ou continuar executando um script [Visual Studio Código,][VisualStudioCodeShortcutsKeyboardWindows]selecione `F5` .  Com a **predefinição DevTools (Padrão),** para pausar ou continuar executando um script, selecione `F8` .  Quando você altera a predefinição **para Visual Studio Código**, agora você também seleciona , assim como no código Visual Studio `F5` [Código][VisualStudioCodeShortcutsKeyboardWindows].  

## <a name="edit-keyboard-shortcuts-for-any-action-in-the-devtools"></a>Editar atalhos de teclado para qualquer ação no DevTools  

Para personalizar o atalho do teclado para uma ação específica no DevTools, conclua as etapas a seguir.  

1.  Navegue até a página da Web [Atalhos.](#customize-keyboard-shortcuts-in-the-microsoft-edge-devtools)  
1.  Escolha a ação que você deseja personalizar.  Por exemplo, na seção **Depurador,** encontre e selecione a ação **Pausar execução de script.**  
1.  Escolha o **ícone Editar** \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \)  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Escolha a ação a ser personalizar na página Atalhos em Configurações" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Escolha a ação a ser personalizar na página [Atalhos](#customize-keyboard-shortcuts-in-the-microsoft-edge-devtools) [em Configurações][DevToolsCustomizeSettings]  
    :::image-end:::  
    
1.  Para vincular as teclas de atalho à ação, verifique se a caixa de texto ao lado da ação tem foco e use o teclado para selecionar as teclas de atalho.  
1.  Para vincular mais de uma combinação de atalho a uma ação, escolha Adicionar um atalho, verifique se **a**caixa de texto ao lado da ação tem foco e use o teclado para selecionar as teclas de atalho.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Selecione as chaves que você deseja atribuir à ação" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Selecione as chaves que você deseja atribuir à ação  
    :::image-end:::  
    
1.  Para salvar seu novo atalho de teclado, escolha a marca de seleção \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) ícone.
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Escolha o ícone de marca de seleção para salvar seu novo atalho de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Escolha o ícone de marca de seleção para salvar seu novo atalho de teclado  
    :::image-end:::  
    
1.  Selecione seu novo atalho de teclado para disparar a ação no DevTools.  
    
Na página [Atalhos,](#customize-keyboard-shortcuts-in-the-microsoft-edge-devtools) o **ícone Atalho** personalizado do Teclado \( ![ CustomKeyboardShortcut \) exibe atalhos de teclado ](../media/custom-keyboard-shortcut-icon.msft.png) personalizados.  Para redefinir todos os atalhos, escolha **Restaurar atalhos padrão**.  

Enquanto você edita os atalhos de teclado para uma ação, para descartar suas alterações, escolha o ícone X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \)  Para remover atalhos para uma ação específica, escolha o ícone **Excluir atalho** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \)  

> [!NOTE]
> Se um atalho de teclado estiver atribuído a uma ação, você será impedido de salvá-lo em outra ação.  Em vez disso, exclua o atalho do teclado da ação anterior e adicione-o à nova ação.  

<!-- links -->  

[DevToolsCustomizeSettings]: ./index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Atalhos de teclado do Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCode]: https://code.visualstudio.com "Código Visual Studio Microsoft"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio atalhos de Teclado de Código para Windows | Código Visual Studio Microsoft"  
