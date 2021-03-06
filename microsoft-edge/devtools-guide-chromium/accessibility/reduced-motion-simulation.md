---
description: Simular movimento reduzido usando ferramentas de desenvolvedor.
title: Simular movimento reduzido usando ferramentas de desenvolvedor (CSS prefere Movimento Reduzido)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 29cdbd7492665e819315910b3f743d444470cc12
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397864"
---
# <a name="reduced-motion-simulation"></a>Simulação de movimento reduzido  

A animação em produtos Web pode ser um problema de acessibilidade.  Os Sistemas Operacionais lidam com o problema, incluindo uma opção para desativar animações para evitar confusão do usuário e possíveis problemas relacionados à saúde, como disparar ataques.  Na Web, você pode usar a Consulta de Mídia CSS [prefers-reduced-motion][MDNPrefersReducedMotion] para detectar se os usuários preferem não executar ou exibir animações.  Em seu produto, você pode quebrar seu código de animação em um teste para evitar animações aparecendo para os usuários afetados.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Usando o [Microsoft Edge DevTools][DevtoolsIndex], você pode simular essa configuração de movimento reduzida sem precisar alterar seu sistema operacional.  

1.  Abra o **Menu de Comando**.  
    1.  Selecione `Control` + `Shift` + `P` no Windows/Linux ou `Command` + `Shift` + `P` no macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           O **Menu De comando**  
        :::image-end:::  
        
1.  Digite `reduced` , para ativar e desativar a simulação.  Escolha a opção e selecione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Ativar ou desativar a configuração de movimento reduzido prefers do Menu de Comando" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Ativar ou desativar a **configuração de** movimento reduzido prefers do **Menu de Comando**  
    :::image-end:::  
    
1.  Atualize a página atual para testar se suas animações estão desligadas ou visíveis.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
