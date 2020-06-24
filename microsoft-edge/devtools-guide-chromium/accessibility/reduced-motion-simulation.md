---
title: Forçar o Microsoft Edge DevTools no modo de visualização do esquema de cores (CSS prefere o esquema de cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 94c5369f0eb35059933be7f6202a4f64450629cd
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758045"
---
# <span data-ttu-id="d7f0e-103">Simulação de movimento reduzida</span><span class="sxs-lookup"><span data-stu-id="d7f0e-103">Reduced Motion Simulation</span></span>  

<span data-ttu-id="d7f0e-104">A animação em produtos da Web pode ser um problema de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-104">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="d7f0e-105">Os sistemas operacionais lidam com o problema, incluindo uma opção para desativar as animações para evitar confusão do usuário e possíveis problemas relacionados à integridade, como o disparo de capturas.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-105">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="d7f0e-106">Na Web, você pode usar a consulta de mídia CSS de [preferência de movimento reduzido][MDNPrefersReducedMotion] para detectar se os usuários preferem não ver as animações.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-106">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="d7f0e-107">Em seu produto, você pode encapsular o código de animação em um teste para evitar que as animações sejam exibidas para os usuários afetados.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-107">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
  animation: none;
  }
}
```  

<span data-ttu-id="d7f0e-108">Usando o [Microsoft Edge devtools][DevtoolsGuideChromiumMain], você pode simular essa configuração de movimentação reduzida sem precisar alterar o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-108">Using the [Microsoft Edge DevTools][DevtoolsGuideChromiumMain], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="d7f0e-109">Abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="d7f0e-110">Pressione `Control` + `Shift` + `P` no Windows ou `Command` + `Shift` + `P` no MacOS.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-110">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="d7f0e-112">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="d7f0e-112">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="d7f0e-113">Digite `reduced` para ativar e desativar a simulação.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-113">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="d7f0e-114">Selecione a opção e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d7f0e-114">Select the option and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Ativar ou desativar a configuração de opção escolher movimento reduzido do menu de comandos" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="d7f0e-116">Ativar ou desativar a configuração de opção **escolher movimento reduzido** do **menu de comandos**</span><span class="sxs-lookup"><span data-stu-id="d7f0e-116">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7f0e-117">Atualize a página atual para testar se suas animações estão desativadas ou visíveis.</span><span class="sxs-lookup"><span data-stu-id="d7f0e-117">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Figura 1: menu de comando"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Figura 2: alternar o movimento reduzido da paleta de comandos"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) Microsoft | Documentos da Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "preferência-movimento reduzido | MDN"  