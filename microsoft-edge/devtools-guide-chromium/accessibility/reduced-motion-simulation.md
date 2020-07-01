---
title: Simular movimento reduzido usando as ferramentas de desenvolvedor (CSS prefere menor movimento)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f1bf90de4ac1832fff07e9ac963c26f92adeea2c
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843981"
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

Usando o [Microsoft Edge devtools][DevtoolsGuideChromiumMain], você pode simular essa configuração de movimentação reduzida sem precisar alterar o sistema operacional.  

1.  Abrir o **menu de comandos**.  
    1.  Pressione `Control` + `Shift` + `P` no Windows ou `Command` + `Shift` + `P` no MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           O **menu de comando**  
        :::image-end:::   
        
1.  Digite `reduced` para ativar e desativar a simulação.  Selecione a opção e pressione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Ativar ou desativar a configuração de opção escolher movimento reduzido do menu de comandos" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Ativar ou desativar a configuração de opção **escolher movimento reduzido** do **menu de comandos**  
    :::image-end:::  
    
1.  Atualize a página atual para testar se suas animações estão desativadas ou visíveis.  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Figura 1: menu de comando"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Figura 2: alternar o movimento reduzido da paleta de comandos"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) Microsoft | Documentos da Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "preferência-movimento reduzido | MDN"  
