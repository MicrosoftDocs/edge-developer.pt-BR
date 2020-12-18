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
# <span data-ttu-id="bc005-104">Simulação de movimento reduzida</span><span class="sxs-lookup"><span data-stu-id="bc005-104">Reduced Motion Simulation</span></span>  

<span data-ttu-id="bc005-105">A animação em produtos da Web pode ser um problema de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="bc005-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="bc005-106">Os sistemas operacionais lidam com o problema, incluindo uma opção para desativar as animações para evitar confusão do usuário e possíveis problemas relacionados à integridade, como o disparo de capturas.</span><span class="sxs-lookup"><span data-stu-id="bc005-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="bc005-107">Na Web, você pode usar a consulta de mídia CSS de [preferência de movimento reduzido][MDNPrefersReducedMotion] para detectar se os usuários preferem não ver as animações.</span><span class="sxs-lookup"><span data-stu-id="bc005-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="bc005-108">Em seu produto, você pode encapsular o código de animação em um teste para evitar que as animações sejam exibidas para os usuários afetados.</span><span class="sxs-lookup"><span data-stu-id="bc005-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="bc005-109">Usando o [Microsoft Edge devtools][DevtoolsIndex], você pode simular essa configuração de movimentação reduzida sem precisar alterar o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bc005-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="bc005-110">Abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="bc005-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="bc005-111">Selecione `Control` + `Shift` + `P` no Windows/Linux ou `Command` + `Shift` + `P` no MacOS.</span><span class="sxs-lookup"><span data-stu-id="bc005-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="bc005-113">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="bc005-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="bc005-114">Digite `reduced` para ativar e desativar a simulação.</span><span class="sxs-lookup"><span data-stu-id="bc005-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="bc005-115">Escolha a opção e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="bc005-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Ativar ou desativar a configuração de opção escolher movimento reduzido do menu de comandos" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="bc005-117">Ativar ou desativar a configuração de opção **escolher movimento reduzido** do **menu de comandos**</span><span class="sxs-lookup"><span data-stu-id="bc005-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bc005-118">Atualize a página atual para testar se suas animações estão desativadas ou visíveis.</span><span class="sxs-lookup"><span data-stu-id="bc005-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "preferência-movimento reduzido | MDN"  
