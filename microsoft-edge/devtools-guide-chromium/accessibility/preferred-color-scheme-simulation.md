---
description: Force Microsoft Edge DevTools no modo de Visualização do Esquema de Cores.
title: Forçar Microsoft Edge DevTools no modo de Visualização de Esquema de Cores (CSS prefere Esquema de Cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: dc2911ce7a7fcbeef7763099541822b5cd6cf053
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597062"
---
# <a name="dark-or-light-color-scheme-simulation"></a>Simulação de esquema de cores escuro ou claro  

Muitos sistemas operacionais têm uma maneira de exibir qualquer aplicativo em cores mais escuras ou mais claras.  Ter um produto Web com um tema claro em um sistema operacional de modo escuro é irritante e pode ser um problema de acessibilidade para alguns usuários.  

Para uma página da Web, você pode usar a Consulta de Mídia CSS de esquema de cores [prefers-color][MDNPrefersColorScheme] para detectar se o usuário prefere exibir seu produto em um esquema de cores mais escuro ou mais claro.  Em seguida, para testar o resultado, use [Microsoft Edge DevTools][DevtoolsIndex] para simular uma alteração do modo escuro para o modo claro, sem precisar alterar a configuração de todo o sistema operacional.  

**Para emular tema escuro ou claro:**

1.  Abra o **Menu de Comando**.  
    1.  Selecione `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\).  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           O **Menu De comando**  
        :::image-end:::  
        
1.  Digite `emulate color` , escolha **Emular CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opção de esquema de cores do Menu de Comando" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Opção de esquema de cores do Menu **de** Comando  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Basta digitar ou não revelar a ferramenta certa, pois também há uma maneira de escolher um `dark` `light` tema para [DevTools][DevtoolsCustomizeDarkTheme].  Se você estiver se perguntando o que escolher, certifique-se de que você está escolhendo um **item** de menu de renderização, não um item de menu **de** aparência.  

1.  Depois de escolher um esquema de cores, atualize o documento atual para exibir o modo simulado.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulado dentro Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Modo de luz simulado dentro Microsoft Edge DevTools  
    :::image-end:::  
    
    Exibir e alterar o CSS como qualquer outra página da Web.  Para obter mais informações, navegue [até Começar a exibir e alterar CSS][DevtoolsCssIndex].  


## <a name="see-also"></a>Consulte também

* [Verifique se há problemas de contraste com o tema escuro e o tema claro](test-dark-mode.md)


<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema escuro no Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Começar a exibir e alterar o CSS | Microsoft Docs"  
<!-- external links -->
[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
