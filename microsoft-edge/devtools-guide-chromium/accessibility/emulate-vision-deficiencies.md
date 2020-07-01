---
title: Emular deficiências visuais no Microsoft Edge DevTools (cegueira para cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843918"
---
# Emular deficiências de visão

Para atender melhor às necessidades dos seus usuários com [deficiências visuais][ColorblindawarenessMain] \ (cegueira para cores \), [o Microsoft Edge devtools][MicrosoftEdgeDevTools] permite simular deficiências de visão de cor específicas.  A ferramenta de **deficiência de visão de emulação** simula as categorias a seguir.  

| Deficiência de visão colorida | Detalhes |  
|:--- |:--- |  
| Visão desfocada | O usuário tem dificuldades para se concentrar em detalhes. |   
| Protanopia | O usuário não consegue perceber qualquer luz vermelha. |  
| Deuteranopia | O usuário não consegue perceber qualquer luz verde. |  
| Tritanopia | O usuário não consegue perceber qualquer luz azul. |  
| Achromatopsia | O usuário não consegue perceber qualquer cor, o que reduz toda a cor para um tom de cinza. |  

## Navegar até as ferramentas de renderização  

Para simular uma deficiência visual sendo aplicada ao seu produto da Web, abra as [ferramentas de renderização][RenderingTools].  

1.  Abrir as ferramentas de renderização selecionando o `...` item de menu na barra de ferramentas  
1.  Selecionar `More tools`  
1.  Selecionar `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrindo as ferramentas de renderização" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Abrindo as **ferramentas de renderização**  
    :::image-end:::  

O menu **renderização** é exibido na gaveta.  

1.  Role para baixo até o `Emulate vision deficiencies` item de menu e selecione o menu suspenso para exibir as opções.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="O menu de deficiências da visão de emulação na gaveta de renderização" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       O menu de **deficiências da visão de emulação** na gaveta de **renderização**  
    :::image-end:::  
    
1.  Escolha uma opção.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Opções do menu de deficiências da visão de emulação" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Opções do menu de **deficiências da visão de emulação**  
    :::image-end:::  
    
1.  O Windows principal exibe a simulação da opção selecionada aplicada à página atual.  
    
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

1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
1.  Tipo `emulate` , escolha o que você deseja simular e pressione `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="As diferentes opções de simulação disponíveis no menu de comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       As diferentes opções de simulação disponíveis no **menu de comando**  
    :::image-end:::  
    
> [!IMPORTANT]
> As ferramentas de **deficiência visual de emulação** simulam a forma como uma pessoa com cada deficiência pode ver seu produto.  Cada pessoa é diferente, portanto, as deficiências de visão variam de acordo com a pessoa com a pessoa.  Para atender melhor às necessidades dos seus usuários, evite qualquer combinação de cores que possa ser um problema.  As ferramentas de **deficiências de visão de emulação** não são uma avaliação completa de acessibilidade do seu produto.  Em vez disso, as ferramentas de **deficiência visual de emulação** devem fornecer uma boa primeira etapa para evitar problemas.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "A organização de conscientização de cores cego"  
[AmfcbMain]: https://www.amfcb.org "A base americana do cego colorido (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Ferramentas de renderização do Microsoft Edge (Chromium)"  
