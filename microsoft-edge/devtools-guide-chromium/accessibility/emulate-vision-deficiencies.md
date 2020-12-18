---
description: Emular deficiências visuais no Microsoft Edge DevTools.
title: Emular deficiências visuais no Microsoft Edge DevTools (cegueira para cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230821"
---
# <span data-ttu-id="8bfbb-104">Emular deficiências visuais</span><span class="sxs-lookup"><span data-stu-id="8bfbb-104">Emulate vision deficiencies</span></span>

<span data-ttu-id="8bfbb-105">Para atender melhor às necessidades dos seus usuários com [deficiências visuais][ColorblindawarenessMain] \ (cegueira para cores \), [o Microsoft Edge devtools][DevtoolsIndex] permite simular deficiências de visão de cor específicas.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="8bfbb-106">A ferramenta de **deficiência de visão de emulação** simula as categorias a seguir.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="8bfbb-107">Deficiência de visão colorida</span><span class="sxs-lookup"><span data-stu-id="8bfbb-107">Color vision deficiency</span></span> | <span data-ttu-id="8bfbb-108">Detalhes</span><span class="sxs-lookup"><span data-stu-id="8bfbb-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8bfbb-109">Visão desfocada</span><span class="sxs-lookup"><span data-stu-id="8bfbb-109">Blurred vision</span></span> | <span data-ttu-id="8bfbb-110">O usuário tem dificuldades para se concentrar em detalhes.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-110">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="8bfbb-111">Protanopia</span><span class="sxs-lookup"><span data-stu-id="8bfbb-111">Protanopia</span></span> | <span data-ttu-id="8bfbb-112">O usuário não consegue perceber qualquer luz vermelha.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="8bfbb-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="8bfbb-113">Deuteranopia</span></span> | <span data-ttu-id="8bfbb-114">O usuário não consegue perceber qualquer luz verde.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="8bfbb-115">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="8bfbb-115">Tritanopia</span></span> | <span data-ttu-id="8bfbb-116">O usuário não consegue perceber qualquer luz azul.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="8bfbb-117">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="8bfbb-117">Achromatopsia</span></span> | <span data-ttu-id="8bfbb-118">O usuário não consegue perceber qualquer cor, o que reduz toda a cor para um tom de cinza.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="8bfbb-119">Navegar até as ferramentas de renderização</span><span class="sxs-lookup"><span data-stu-id="8bfbb-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="8bfbb-120">Para simular uma deficiência visual sendo aplicada ao seu produto da Web, abra as [ferramentas de renderização][DevtoolsRenderingToolsIndex].</span><span class="sxs-lookup"><span data-stu-id="8bfbb-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="8bfbb-121">Para abrir as ferramentas de renderização, escolha o `...` item de menu na barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="8bfbb-121">To open the Rendering Tools, by choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="8bfbb-122">Escolher</span><span class="sxs-lookup"><span data-stu-id="8bfbb-122">Choose</span></span> `More tools`  
1.  <span data-ttu-id="8bfbb-123">Escolher</span><span class="sxs-lookup"><span data-stu-id="8bfbb-123">Choose</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrindo as ferramentas de renderização" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="8bfbb-125">Abrindo as **ferramentas de renderização**</span><span class="sxs-lookup"><span data-stu-id="8bfbb-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="8bfbb-126">O menu **renderização** é exibido na gaveta.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="8bfbb-127">Role para baixo até o `Emulate vision deficiencies` item de menu e escolha o menu suspenso para exibir as opções.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="O menu de deficiências da visão de emulação na gaveta de renderização" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="8bfbb-129">O menu de **deficiências da visão de emulação** na gaveta de **renderização**</span><span class="sxs-lookup"><span data-stu-id="8bfbb-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8bfbb-130">Escolha uma opção.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Opções do menu de deficiências da visão de emulação" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="8bfbb-132">Opções do menu de **deficiências da visão de emulação**</span><span class="sxs-lookup"><span data-stu-id="8bfbb-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8bfbb-133">A página principal do Windows exibe a simulação da opção escolhida aplicada à página atual.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Vídeo com a simulação \* \* desfocada da revisão \* \*" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="8bfbb-135">Exibição usando simulação de **visão borrada**</span><span class="sxs-lookup"><span data-stu-id="8bfbb-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Vídeo usando a simulação \* \* achromatopsia \* \*" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="8bfbb-137">Exibir usando a simulação **achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="8bfbb-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="8bfbb-138">Usar o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="8bfbb-138">Use the Command Menu</span></span>  

<span data-ttu-id="8bfbb-139">Você também pode usar o **menu de comando** para acessar as diferentes simulações.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="8bfbb-140">Selecione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-140">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="8bfbb-142">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="8bfbb-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8bfbb-143">Tipo `emulate` , escolha o que você deseja simular e selecionar `Enter` .</span><span class="sxs-lookup"><span data-stu-id="8bfbb-143">Type `emulate`, choose what you want to simulate and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="As diferentes opções de simulação disponíveis no menu de comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="8bfbb-145">As diferentes opções de simulação disponíveis no **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="8bfbb-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="8bfbb-146">As ferramentas de **deficiência visual de emulação** simulam a forma como uma pessoa com cada deficiência pode ver seu produto.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="8bfbb-147">Cada pessoa é diferente, portanto, as deficiências de visão variam de acordo com a pessoa com a pessoa.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="8bfbb-148">Para atender melhor às necessidades dos seus usuários, evite qualquer combinação de cores que possa ser um problema.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="8bfbb-149">As ferramentas de **deficiências de visão de emulação** não são uma avaliação completa de acessibilidade do seu produto.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="8bfbb-150">Em vez disso, as ferramentas de **deficiência visual de emulação** devem fornecer uma boa primeira etapa para evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="8bfbb-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analisar o desempenho do tempo de execução | Documentos da Microsoft"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "A organização de conscientização de cores cego"  

[AmfcbMain]: https://www.amfcb.org "A base americana do cego colorido (AFCB)"  

