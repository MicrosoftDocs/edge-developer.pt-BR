---
description: Simular movimento reduzido usando ferramentas de desenvolvedor.
title: Simular movimento reduzido usando ferramentas de desenvolvedor (CSS prefere Movimento Reduzido)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7244c2e80bbf9070214b6abd02583792c785953c
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597056"
---
# <a name="reduced-motion-simulation"></a>Simulação de movimento reduzido  

A animação em produtos Web pode ser um problema de acessibilidade.  Os sistemas operacionais lidam com esse problema, incluindo uma opção para desativar animações para evitar confusão do usuário e possíveis problemas relacionados à saúde, como disparar ataques.  

Em uma página da Web, você pode usar a consulta de mídia CSS [prefers-reduced-motion][MDNPrefersReducedMotion] para detectar se o usuário prefere exibir quaisquer animações.  Em seguida, envolva seu código de animação em um teste para executar animações condicionalmente.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Em seguida, teste seu código, da seguinte forma.

Para simular a configuração de movimento reduzida do sistema operacional, sem precisar alterar a configuração do sistema operacional:

1.  Abra o **Menu de Comando**.  
    1.  Selecione `Control` + `Shift` + `P` em Windows/Linux ou `Command` + `Shift` + `P` no macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           O **Menu De comando**  
        :::image-end:::  
        
1.  Digite `reduced` , para ativar e desativar a simulação.  Escolha a opção e selecione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Ativar ou desativar a configuração de movimento reduzido prefers do Menu de Comando" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Ativar ou desativar a **configuração de** movimento reduzido prefers do **Menu de Comando**  
    :::image-end:::  
    
1.  Atualize a página da Web e verifique se suas animações são executados.


## <a name="see-also"></a>Consulte também

* [Verifique se a página é usável](test-reduced-ui-motion.md) com a animação da interface do usuário desligada - Um passo a passo usando uma página de demonstração, com explicações.

    
<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
