---
description: Emular deficiências de visão no Microsoft Edge DevTools.
title: Emular deficiências de visão em Microsoft Edge DevTools (color blindness)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0a0ee09c2f739beb366b4c39d113b31fb719ec6a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597121"
---
# <a name="emulate-vision-deficiencies"></a>Emular deficiências visuais  

Para atender melhor às necessidades [][ColorblindawarenessMain] de seus usuários com deficiência de visão de cor \(color blindness\) ou visão desfocado, Microsoft Edge [DevTools permite simular deficiências][DevtoolsIndex] de visão desfocado e visão de cores específicas.  A **ferramenta Emular deficiências de visão** simula as seguintes categorias.  

| Deficiência de visão de cor | Detalhes |  
|:--- |:--- |  
| Visão desfocado | O usuário tem dificuldade para se concentrar em detalhes finos. |  
| Protanopia | O usuário não consegue perceber nenhuma luz vermelha. |  
| Deuteranopia | O usuário não consegue perceber nenhuma luz verde. |  
| Tritanopia | O usuário não consegue perceber nenhuma luz azul. |  
| Achromatopsia | O usuário não consegue perceber qualquer cor, o que reduz toda a cor a um tom de cinza. |  


## <a name="navigate-to-the-rendering-tool"></a>Navegue até a ferramenta Rendering

Para simular uma deficiência de visão que está sendo aplicada ao seu produto Web, abra as [Ferramentas de Renderização.][DevtoolsRenderingToolsIndex]  

1.  Para abrir a ferramenta Rendering, escolha o `...` item de menu na barra de ferramentas  
1.  Escolher **Mais ferramentas**  
1.  Escolha **Renderização**  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir a ferramenta Rendering" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Abrir a **ferramenta Rendering**
    :::image-end:::  
    
O menu **Renderização** aparece na gaveta.  

1.  Role para baixo até o `Emulate vision deficiencies` item de menu e escolha o menu suspenso para exibir as opções.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="O menu Emular Deficiências de Visão na ferramenta Rendering" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       O **menu Emular deficiências de** visão na ferramenta **Rendering**
    :::image-end:::  
    
1.  Escolha uma opção.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="As opções de menu Emular Deficiências de Visão" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       As opções do menu **Emular deficiências de visão**  
    :::image-end:::  
    
1.  As janelas principais exibem a simulação da opção escolhida aplicada à página atual.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Exibição usando simulação de visão desfocado" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Exibir usando **simulação de visão desfocado**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Exibir usando simulação de Achromatopsia" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Exibir usando **simulação de Achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    

## <a name="use-the-command-menu"></a>Usar o Menu de Comando  

Você também pode usar **o Menu de Comando** para acessar as diferentes simulações.  

1.  Selecione `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\) para abrir o **Menu de Comando**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       O **Menu De comando**  
    :::image-end:::  
    
1.  Digite `emulate` , escolha o que você deseja simular e escolha `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="As diferentes opções de simulação disponíveis no Menu de Comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       As diferentes opções de simulação disponíveis no **Menu de Comando**  
    :::image-end:::  
    
> [!IMPORTANT]
> As **ferramentas de deficiências** de visão emular simulam aproximações de como uma pessoa com cada deficiência pode ver seu produto.  Cada pessoa é diferente, portanto, as deficiências de visão variam de pessoa para pessoa.  Para atender melhor às necessidades de seus usuários, evite qualquer combinação de cores que possa ser um problema.  As **ferramentas de deficiências de visão emular** não são uma avaliação de acessibilidade completa do seu produto.  Em vez disso, as **ferramentas de deficiências de visão emular** devem dar uma boa primeira etapa para evitar problemas.  


## <a name="see-also"></a>Consulte também

* [Verifique se a página pode ser usada com visão turva](test-blurred-vision.md)


<!-- links -->  
[DevToolsIndex]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analisar o desempenho do tempo de execução | Microsoft Docs"  

[ColorblindawarenessMain]: https://www.colourblindawareness.org "A organização Color Blind Awareness"  

[AmfcbMain]: https://www.amfcb.org "A American Foundation for the Color Blind (AFCB)"  
