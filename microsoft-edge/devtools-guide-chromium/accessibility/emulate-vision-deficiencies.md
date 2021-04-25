---
description: Emular deficiências de visão no Microsoft Edge DevTools.
title: Emular deficiências de visão no Microsoft Edge DevTools (color blindness)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 8c3f3a34c441692117906f51c3d8430e79fd72b1
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519167"
---
# <a name="emulate-vision-deficiencies"></a><span data-ttu-id="b436f-104">Emular deficiências visuais</span><span class="sxs-lookup"><span data-stu-id="b436f-104">Emulate vision deficiencies</span></span>

<span data-ttu-id="b436f-105">Para atender melhor às necessidades [][ColorblindawarenessMain] de seus usuários com deficiência de visão de cor \(color blindness\), o [Microsoft Edge DevTools][DevtoolsIndex] permite simular deficiências de visão de cores específicas.</span><span class="sxs-lookup"><span data-stu-id="b436f-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] allow you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="b436f-106">A **ferramenta Emular deficiências de visão** simula as seguintes categorias.</span><span class="sxs-lookup"><span data-stu-id="b436f-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="b436f-107">Deficiência de visão de cor</span><span class="sxs-lookup"><span data-stu-id="b436f-107">Color vision deficiency</span></span> | <span data-ttu-id="b436f-108">Detalhes</span><span class="sxs-lookup"><span data-stu-id="b436f-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b436f-109">Visão desfocado</span><span class="sxs-lookup"><span data-stu-id="b436f-109">Blurred vision</span></span> | <span data-ttu-id="b436f-110">O usuário tem dificuldade para se concentrar em detalhes finos.</span><span class="sxs-lookup"><span data-stu-id="b436f-110">The user has difficulty focusing on fine details.</span></span> |  
| <span data-ttu-id="b436f-111">Protanopia</span><span class="sxs-lookup"><span data-stu-id="b436f-111">Protanopia</span></span> | <span data-ttu-id="b436f-112">O usuário não consegue perceber nenhuma luz vermelha.</span><span class="sxs-lookup"><span data-stu-id="b436f-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="b436f-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="b436f-113">Deuteranopia</span></span> | <span data-ttu-id="b436f-114">O usuário não consegue perceber nenhuma luz verde.</span><span class="sxs-lookup"><span data-stu-id="b436f-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="b436f-115">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="b436f-115">Tritanopia</span></span> | <span data-ttu-id="b436f-116">O usuário não consegue perceber nenhuma luz azul.</span><span class="sxs-lookup"><span data-stu-id="b436f-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="b436f-117">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="b436f-117">Achromatopsia</span></span> | <span data-ttu-id="b436f-118">O usuário não consegue perceber qualquer cor, o que reduz toda a cor a um tom de cinza.</span><span class="sxs-lookup"><span data-stu-id="b436f-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <a name="navigate-to-the-rendering-tools"></a><span data-ttu-id="b436f-119">Navegue até as Ferramentas de Renderização</span><span class="sxs-lookup"><span data-stu-id="b436f-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="b436f-120">Para simular uma deficiência de visão que está sendo aplicada ao seu produto Web, abra as [Ferramentas de Renderização.][DevtoolsRenderingToolsIndex]</span><span class="sxs-lookup"><span data-stu-id="b436f-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="b436f-121">Para abrir as Ferramentas de Renderização, escolha `...` o item de menu na barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="b436f-121">To open the Rendering Tools, choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="b436f-122">Escolher **Mais ferramentas**</span><span class="sxs-lookup"><span data-stu-id="b436f-122">Choose **More tools**</span></span>  
1.  <span data-ttu-id="b436f-123">Escolha **Renderização**</span><span class="sxs-lookup"><span data-stu-id="b436f-123">Choose **Rendering**</span></span>  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir as Ferramentas de Renderização" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="b436f-125">Abrir as Ferramentas **de Renderização**</span><span class="sxs-lookup"><span data-stu-id="b436f-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="b436f-126">O menu **Renderização** aparece na gaveta.</span><span class="sxs-lookup"><span data-stu-id="b436f-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="b436f-127">Role para baixo até o `Emulate vision deficiencies` item de menu e escolha o menu suspenso para exibir as opções.</span><span class="sxs-lookup"><span data-stu-id="b436f-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="O menu Emular deficiências de visão na gaveta renderização" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="b436f-129">O **menu Emular deficiências de visão** na gaveta **renderização**</span><span class="sxs-lookup"><span data-stu-id="b436f-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b436f-130">Escolha uma opção.</span><span class="sxs-lookup"><span data-stu-id="b436f-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="As opções de menu Emular Deficiências de Visão" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="b436f-132">As opções do menu **Emular deficiências de visão**</span><span class="sxs-lookup"><span data-stu-id="b436f-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b436f-133">As janelas principais exibem a simulação da opção escolhida aplicada à página atual.</span><span class="sxs-lookup"><span data-stu-id="b436f-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Exibir usando a simulação **Visão Desfocado**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="b436f-135">Exibição usando **simulação de visão desfocado**</span><span class="sxs-lookup"><span data-stu-id="b436f-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Exibir usando **Achromatopsia** simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="b436f-137">Exibir usando **simulação de Achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="b436f-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="use-the-command-menu"></a><span data-ttu-id="b436f-138">Usar o Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="b436f-138">Use the Command Menu</span></span>  

<span data-ttu-id="b436f-139">Você também pode usar **o Menu de Comando** para acessar as diferentes simulações.</span><span class="sxs-lookup"><span data-stu-id="b436f-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="b436f-140">Selecione `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\) para abrir o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="b436f-140">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="b436f-142">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="b436f-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b436f-143">Digite `emulate` , escolha o que você deseja simular e escolha `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b436f-143">Type `emulate`, choose what you want to simulate and choose `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="As diferentes opções de simulação disponíveis no Menu de Comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="b436f-145">As diferentes opções de simulação disponíveis no **Menu de Comando**</span><span class="sxs-lookup"><span data-stu-id="b436f-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="b436f-146">As **ferramentas de deficiências** de visão emular simulam aproximações de como uma pessoa com cada deficiência pode ver seu produto.</span><span class="sxs-lookup"><span data-stu-id="b436f-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="b436f-147">Cada pessoa é diferente, portanto, as deficiências de visão variam de pessoa para pessoa.</span><span class="sxs-lookup"><span data-stu-id="b436f-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="b436f-148">Para atender melhor às necessidades de seus usuários, evite qualquer combinação de cores que possa ser um problema.</span><span class="sxs-lookup"><span data-stu-id="b436f-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="b436f-149">As **ferramentas de deficiências de visão emular** não são uma avaliação de acessibilidade completa do seu produto.</span><span class="sxs-lookup"><span data-stu-id="b436f-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="b436f-150">Em vez disso, as **ferramentas de deficiências de visão emular** devem dar uma boa primeira etapa para evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="b436f-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevToolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analisar o desempenho do tempo de execução | Microsoft Docs"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "A organização Color Blind Awareness"  

[AmfcbMain]: https://www.amfcb.org "A American Foundation for the Color Blind (AFCB)"  
