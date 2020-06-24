---
title: Forçar o Microsoft Edge DevTools no modo de visualização do esquema de cores (CSS prefere o esquema de cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: a83284b676ad388114a4a0ddb7ebdf2203ebcb90
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758047"
---
# Simulação de esquema de cores escuras ou leves  

Os sistemas operacionais têm uma maneira de exibir qualquer aplicativo em cores mais escuras ou mais claras.  Ter um produto da Web com um tema claro em um sistema operacional em modo escuro está de meio funcionamento e pode ser um problema de acessibilidade para alguns usuários.  Na Web, você pode usar a consulta de mídia CSS de [preferência esquema de cores][MDNPrefersColorScheme] para detectar se os usuários preferem ver o produto em um esquema de cores mais escuro ou mais claro.  Use o [Microsoft Edge devtools][DevtoolsGuideChromiumMain] para simular uma alteração do modo escuro para Light sem ter que alterar todo o sistema operacional.  

1.  Abrir o **menu de comandos**.  
    1.  Pressione `Control` + `Shift` + `P` no Windows ou `Command` + `Shift` + `P` no MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           O **menu de comando**  
        :::image-end:::   
        
1.  Tipo `emulate color` , selecione **emular CSS prefere opções-esquema de cores: escuro** ou **emular CSS prefere-Color-esquema: Light** e pressione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Seleção do esquema de cores no menu de comandos" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Seleção do esquema de cores no menu de **comandos**  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Basta digitar `dark` ou `light` não revelar a ferramenta certa, pois também há uma maneira de [escolher um tema para devtools][DevtoolsGuideChromiumCustomizeDarkTheme].  Se você estiver imaginando o que escolher, verifique se está selecionando um item de menu de **renderização** , não um item de menu de **aparência** .  

1.  Depois de selecionar um esquema de cores, recarregue o documento atual para ver o modo simulado.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulado dentro do Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Modo de luz simulado dentro do Microsoft Edge DevTools  
    :::image-end:::  
    
    Exiba e altere sua CSS como qualquer outra página da Web.  Para obter mais informações, consulte [introdução à visualização e à alteração de CSS][DevtoolsGuideChromiumCssIndex].  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) Microsoft | Documentos da Microsoft"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema escuro no Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "preferência – esquema de cores | MDN"  
