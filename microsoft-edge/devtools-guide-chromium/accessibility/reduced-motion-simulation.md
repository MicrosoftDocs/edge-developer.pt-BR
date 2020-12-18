---
description: Simule o Motion reduzido usando as ferramentas de desenvolvedor.
title: Simular movimento reduzido usando as ferramentas de desenvolvedor (CSS prefere menor movimento)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0e5243e01ca6c9344dceffb0bf004dadccc3d4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230786"
---
# Simulação de movimento reduzida  

A animação em produtos da Web pode ser um problema de acessibilidade.  Os sistemas operacionais lidam com o problema, incluindo uma opção para desativar as animações para evitar confusão do usuário e possíveis problemas relacionados à integridade, como o disparo de capturas.  Na Web, você pode usar a consulta de mídia CSS de [preferência de movimento reduzido][MDNPrefersReducedMotion] para detectar se os usuários preferem não ver as animações.  Em seu produto, você pode encapsular o código de animação em um teste para evitar que as animações sejam exibidas para os usuários afetados.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Usando o [Microsoft Edge devtools][DevtoolsIndex], você pode simular essa configuração de movimentação reduzida sem precisar alterar o sistema operacional.  

1.  Abrir o **menu de comandos**.  
    1.  Selecione `Control` + `Shift` + `P` no Windows/Linux ou `Command` + `Shift` + `P` no MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           O **menu de comando**  
        :::image-end:::  
        
1.  Digite `reduced` para ativar e desativar a simulação.  Escolha a opção e selecione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Ativar ou desativar a configuração de opção escolher movimento reduzido do menu de comandos" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Ativar ou desativar a configuração de opção **escolher movimento reduzido** do **menu de comandos**  
    :::image-end:::  
    
1.  Atualize a página atual para testar se suas animações estão desativadas ou visíveis.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "preferência-movimento reduzido | MDN"  
