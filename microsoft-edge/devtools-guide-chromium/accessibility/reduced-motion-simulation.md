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
# <a name="reduced-motion-simulation"></a><span data-ttu-id="f1e47-104">Simulação de movimento reduzido</span><span class="sxs-lookup"><span data-stu-id="f1e47-104">Reduced motion simulation</span></span>  

<span data-ttu-id="f1e47-105">A animação em produtos Web pode ser um problema de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="f1e47-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="f1e47-106">Os sistemas operacionais lidam com esse problema, incluindo uma opção para desativar animações para evitar confusão do usuário e possíveis problemas relacionados à saúde, como disparar ataques.</span><span class="sxs-lookup"><span data-stu-id="f1e47-106">Operating systems deal with this problem by including an option to turn off animations to avoid user confusion and potential health-related problems, such as triggering seizures.</span></span>  

<span data-ttu-id="f1e47-107">Em uma página da Web, você pode usar a consulta de mídia CSS [prefers-reduced-motion][MDNPrefersReducedMotion] para detectar se o usuário prefere exibir quaisquer animações.</span><span class="sxs-lookup"><span data-stu-id="f1e47-107">On a webpage, you can use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS media query to detect whether the user prefers to display any animations.</span></span>  <span data-ttu-id="f1e47-108">Em seguida, envolva seu código de animação em um teste para executar animações condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="f1e47-108">Then wrap your animation code in a test, to conditionally run animations.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="f1e47-109">Em seguida, teste seu código, da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="f1e47-109">Then test your code, as follows.</span></span>

<span data-ttu-id="f1e47-110">Para simular a configuração de movimento reduzida do sistema operacional, sem precisar alterar a configuração do sistema operacional:</span><span class="sxs-lookup"><span data-stu-id="f1e47-110">To simulate the operating system's reduced motion setting, without having to change your operating system setting:</span></span>

1.  <span data-ttu-id="f1e47-111">Abra o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="f1e47-111">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="f1e47-112">Selecione `Control` + `Shift` + `P` em Windows/Linux ou `Command` + `Shift` + `P` no macOS.</span><span class="sxs-lookup"><span data-stu-id="f1e47-112">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="f1e47-114">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="f1e47-114">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="f1e47-115">Digite `reduced` , para ativar e desativar a simulação.</span><span class="sxs-lookup"><span data-stu-id="f1e47-115">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="f1e47-116">Escolha a opção e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f1e47-116">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Ativar ou desativar a configuração de movimento reduzido prefers do Menu de Comando" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="f1e47-118">Ativar ou desativar a **configuração de** movimento reduzido prefers do **Menu de Comando**</span><span class="sxs-lookup"><span data-stu-id="f1e47-118">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f1e47-119">Atualize a página da Web e verifique se suas animações são executados.</span><span class="sxs-lookup"><span data-stu-id="f1e47-119">Refresh the webpage and check whether your animations run.</span></span>


## <a name="see-also"></a><span data-ttu-id="f1e47-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f1e47-120">See also</span></span>

* <span data-ttu-id="f1e47-121">[Verifique se a página é usável](test-reduced-ui-motion.md) com a animação da interface do usuário desligada - Um passo a passo usando uma página de demonstração, com explicações.</span><span class="sxs-lookup"><span data-stu-id="f1e47-121">[Verify that the page is usable with UI animation turned off](test-reduced-ui-motion.md) - A walkthrough using a demo page, with explanations.</span></span>

    
<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
