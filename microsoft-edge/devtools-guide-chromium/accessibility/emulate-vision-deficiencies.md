---
description: Emular deficiências visuais no Microsoft Edge DevTools.
title: Emular deficiências visuais no Microsoft Edge DevTools (cegueira para cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230821"
---
# Emular deficiências visuais

Para atender melhor às necessidades dos seus usuários com [deficiências visuais][ColorblindawarenessMain] \ (cegueira para cores \), [o Microsoft Edge devtools][DevtoolsIndex] permite simular deficiências de visão de cor específicas.  A ferramenta de **deficiência de visão de emulação** simula as categorias a seguir.  

| Deficiência de visão colorida | Detalhes |  
|:--- |:--- |  
| Visão desfocada | O usuário tem dificuldades para se concentrar em detalhes. |   
| Protanopia | O usuário não consegue perceber qualquer luz vermelha. |  
| Deuteranopia | O usuário não consegue perceber qualquer luz verde. |  
| Tritanopia | O usuário não consegue perceber qualquer luz azul. |  
| Achromatopsia | O usuário não consegue perceber qualquer cor, o que reduz toda a cor para um tom de cinza. |  

## Navegar até as ferramentas de renderização  

Para simular uma deficiência visual sendo aplicada ao seu produto da Web, abra as [ferramentas de renderização][DevtoolsRenderingToolsIndex].  

1.  Para abrir as ferramentas de renderização, escolha o `...` item de menu na barra de ferramentas  
1.  Escolher `More tools`  
1.  Escolher `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrindo as ferramentas de renderização" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Abrindo as **ferramentas de renderização**  
    :::image-end:::  

O menu **renderização** é exibido na gaveta.  

1.  Role para baixo até o `Emulate vision deficiencies` item de menu e escolha o menu suspenso para exibir as opções.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="O menu de deficiências da visão de emulação na gaveta de renderização" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       O menu de **deficiências da visão de emulação** na gaveta de **renderização**  
    :::image-end:::  
    
1.  Escolha uma opção.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Opções do menu de deficiências da visão de emulação" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Opções do menu de **deficiências da visão de emulação**  
    :::image-end:::  
    
1.  A página principal do Windows exibe a simulação da opção escolhida aplicada à página atual.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Vídeo com a simulação * * desfocada da revisão * *" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Exibição usando simulação de **visão borrada**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Vídeo usando a simulação * * achromatopsia * *" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Exibir usando a simulação **achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Usar o menu de comandos  

Você também pode usar o **menu de comando** para acessar as diferentes simulações.  

1.  Selecione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
1.  Tipo `emulate` , escolha o que você deseja simular e selecionar `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="As diferentes opções de simulação disponíveis no menu de comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       As diferentes opções de simulação disponíveis no **menu de comando**  
    :::image-end:::  
    
> [!IMPORTANT]
> As ferramentas de **deficiência visual de emulação** simulam a forma como uma pessoa com cada deficiência pode ver seu produto.  Cada pessoa é diferente, portanto, as deficiências de visão variam de acordo com a pessoa com a pessoa.  Para atender melhor às necessidades dos seus usuários, evite qualquer combinação de cores que possa ser um problema.  As ferramentas de **deficiências de visão de emulação** não são uma avaliação completa de acessibilidade do seu produto.  Em vez disso, as ferramentas de **deficiência visual de emulação** devem fornecer uma boa primeira etapa para evitar problemas.  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analisar o desempenho do tempo de execução | Documentos da Microsoft"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "A organização de conscientização de cores cego"  

[AmfcbMain]: https://www.amfcb.org "A base americana do cego colorido (AFCB)"  

