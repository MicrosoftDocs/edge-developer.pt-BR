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
# <a name="reduced-motion-simulation"></a><span data-ttu-id="c8698-104">Simulação de movimento reduzido</span><span class="sxs-lookup"><span data-stu-id="c8698-104">Reduced motion simulation</span></span>  

<span data-ttu-id="c8698-105">A animação em produtos Web pode ser um problema de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="c8698-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="c8698-106">Os Sistemas Operacionais lidam com o problema, incluindo uma opção para desativar animações para evitar confusão do usuário e possíveis problemas relacionados à saúde, como disparar ataques.</span><span class="sxs-lookup"><span data-stu-id="c8698-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="c8698-107">Na Web, você pode usar a Consulta de Mídia CSS [prefers-reduced-motion][MDNPrefersReducedMotion] para detectar se os usuários preferem não executar ou exibir animações.</span><span class="sxs-lookup"><span data-stu-id="c8698-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not run or display any animations.</span></span>  <span data-ttu-id="c8698-108">Em seu produto, você pode quebrar seu código de animação em um teste para evitar animações aparecendo para os usuários afetados.</span><span class="sxs-lookup"><span data-stu-id="c8698-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="c8698-109">Usando o [Microsoft Edge DevTools][DevtoolsIndex], você pode simular essa configuração de movimento reduzida sem precisar alterar seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c8698-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="c8698-110">Abra o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="c8698-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="c8698-111">Selecione `Control` + `Shift` + `P` no Windows/Linux ou `Command` + `Shift` + `P` no macOS.</span><span class="sxs-lookup"><span data-stu-id="c8698-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="c8698-113">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="c8698-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="c8698-114">Digite `reduced` , para ativar e desativar a simulação.</span><span class="sxs-lookup"><span data-stu-id="c8698-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="c8698-115">Escolha a opção e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c8698-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Ativar ou desativar a configuração de movimento reduzido prefers do Menu de Comando" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="c8698-117">Ativar ou desativar a **configuração de** movimento reduzido prefers do **Menu de Comando**</span><span class="sxs-lookup"><span data-stu-id="c8698-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8698-118">Atualize a página atual para testar se suas animações estão desligadas ou visíveis.</span><span class="sxs-lookup"><span data-stu-id="c8698-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
