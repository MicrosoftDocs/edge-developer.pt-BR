---
title: Emular deficiências visuais no Microsoft Edge DevTools (cegueira para cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758048"
---
# Emular deficiências de visão

No mundo inteiro, aproximadamente 8% de homens e 0,5% das mulheres têm uma [deficiência de visão de cor][ColorblindawarenessMain] comumente chamada de "cegueira para cores".  O [Microsoft Edge devtools][MicrosoftEdgeDevTools] permite que você eMule várias deficiências conhecidas e forneça uma visualização do seu produto para revisão.  

| Deficiência de cor | Detalhes |  
|:--- |:--- |  
| Visão desfocada |  |   
| Protanopia | A incapacidade de perceber qualquer luz vermelha. |  
| Deuteranopia | A incapacidade de perceber qualquer luz verde. |  
| Tritanopia | A incapacidade de perceber qualquer luz azul. |  
| Achromatopsia | A incapacidade de perceber qualquer cor, com exceção do sombreamento de cinza. |  

## Navegar até as ferramentas de renderização  

Para testar seu produto da Web atual em busca de deficiências de cores, abra as [ferramentas de renderização][RenderingTools].  

1.  Abrir as ferramentas de renderização selecionando o `...` item de menu na barra de ferramentas  
1.  Selecionar `More tools`  
1.  Selecionar `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrindo as ferramentas de renderização" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Abrindo as **ferramentas de renderização**  
    :::image-end:::  

O menu **renderização** é exibido na metade inferior da devtools.  

1.  Role para baixo até o `Emulate Vision deficiencies` item de menu e selecione uma das opções.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="O menu de deficiências da visão de emulação das ferramentas de renderização" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       O menu de **deficiências da visão de emulação** das ferramentas de **renderização**  
    :::image-end:::  
    
1.  Escolha qualquer uma das opções  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Opções do menu de deficiências da visão de emulação" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Opções do menu de **deficiências da visão de emulação**  
    :::image-end:::  
    
1.  A página atual é exibida em uma simulação de como ela pode aparecer para um usuário com a deficiência selecionada.  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Documentação das ferramentas de desenvolvedor do Microsoft Edge na emulação de visão borrada" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Exibido usando a emulação de **visão desfocada**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Documentação das ferramentas de desenvolvedor do Microsoft Edge na emulação do achromatopsia Vision" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Exibir usando a emulação de **visão achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Usar o menu de comandos  

Você também pode alcançar diferentes emulações sem passar pelos vários menus usando o menu de **comandos**.  

1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
1.  Tipo `emulate` , escolha o que você deseja simular e pressione `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="As diferentes opções de emulação disponíveis no menu de comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       As diferentes opções de emulação disponíveis no **menu de comando**  
    :::image-end:::  
    
> [!IMPORTANT]
> As ferramentas de emulação são as aproximações de como uma pessoa com cada deficiência pode ver seu produto.  Cada pessoa é diferente, portanto, as deficiências de visão variam de acordo com a pessoa com a pessoa.  Para atender melhor às necessidades dos seus usuários, evite qualquer combinação de cores que possa ser um problema.  As ferramentas de emulação não são uma avaliação completa da acessibilidade do seu produto, mas você deve ter uma boa primeira etapa em relação a evitar as principais deficiências.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "A organização de conscientização de cores cego"  
[AmfcbMain]: https://www.amfcb.org "A base americana do cego colorido (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Ferramentas de renderização do Microsoft Edge (Chromium)"  
