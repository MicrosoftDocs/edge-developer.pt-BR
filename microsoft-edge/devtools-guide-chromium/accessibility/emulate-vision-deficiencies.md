---
title: Emular deficiências visuais no Microsoft Edge DevTools (cegueira para cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843918"
---
# <span data-ttu-id="eea62-103">Emular deficiências de visão</span><span class="sxs-lookup"><span data-stu-id="eea62-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="eea62-104">Para atender melhor às necessidades dos seus usuários com [deficiências visuais][ColorblindawarenessMain] \ (cegueira para cores \), [o Microsoft Edge devtools][MicrosoftEdgeDevTools] permite simular deficiências de visão de cor específicas.</span><span class="sxs-lookup"><span data-stu-id="eea62-104">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="eea62-105">A ferramenta de **deficiência de visão de emulação** simula as categorias a seguir.</span><span class="sxs-lookup"><span data-stu-id="eea62-105">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="eea62-106">Deficiência de visão colorida</span><span class="sxs-lookup"><span data-stu-id="eea62-106">Color vision deficiency</span></span> | <span data-ttu-id="eea62-107">Detalhes</span><span class="sxs-lookup"><span data-stu-id="eea62-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="eea62-108">Visão desfocada</span><span class="sxs-lookup"><span data-stu-id="eea62-108">Blurred vision</span></span> | <span data-ttu-id="eea62-109">O usuário tem dificuldades para se concentrar em detalhes.</span><span class="sxs-lookup"><span data-stu-id="eea62-109">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="eea62-110">Protanopia</span><span class="sxs-lookup"><span data-stu-id="eea62-110">Protanopia</span></span> | <span data-ttu-id="eea62-111">O usuário não consegue perceber qualquer luz vermelha.</span><span class="sxs-lookup"><span data-stu-id="eea62-111">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="eea62-112">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="eea62-112">Deuteranopia</span></span> | <span data-ttu-id="eea62-113">O usuário não consegue perceber qualquer luz verde.</span><span class="sxs-lookup"><span data-stu-id="eea62-113">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="eea62-114">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="eea62-114">Tritanopia</span></span> | <span data-ttu-id="eea62-115">O usuário não consegue perceber qualquer luz azul.</span><span class="sxs-lookup"><span data-stu-id="eea62-115">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="eea62-116">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="eea62-116">Achromatopsia</span></span> | <span data-ttu-id="eea62-117">O usuário não consegue perceber qualquer cor, o que reduz toda a cor para um tom de cinza.</span><span class="sxs-lookup"><span data-stu-id="eea62-117">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="eea62-118">Navegar até as ferramentas de renderização</span><span class="sxs-lookup"><span data-stu-id="eea62-118">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="eea62-119">Para simular uma deficiência visual sendo aplicada ao seu produto da Web, abra as [ferramentas de renderização][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="eea62-119">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="eea62-120">Abrir as ferramentas de renderização selecionando o `...` item de menu na barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="eea62-120">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="eea62-121">Selecionar</span><span class="sxs-lookup"><span data-stu-id="eea62-121">Select</span></span> `More tools`  
1.  <span data-ttu-id="eea62-122">Selecionar</span><span class="sxs-lookup"><span data-stu-id="eea62-122">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrindo as ferramentas de renderização" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="eea62-124">Abrindo as **ferramentas de renderização**</span><span class="sxs-lookup"><span data-stu-id="eea62-124">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="eea62-125">O menu **renderização** é exibido na gaveta.</span><span class="sxs-lookup"><span data-stu-id="eea62-125">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="eea62-126">Role para baixo até o `Emulate vision deficiencies` item de menu e selecione o menu suspenso para exibir as opções.</span><span class="sxs-lookup"><span data-stu-id="eea62-126">Scroll down to the `Emulate vision deficiencies` menu item and select the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="O menu de deficiências da visão de emulação na gaveta de renderização" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="eea62-128">O menu de **deficiências da visão de emulação** na gaveta de **renderização**</span><span class="sxs-lookup"><span data-stu-id="eea62-128">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="eea62-129">Escolha uma opção.</span><span class="sxs-lookup"><span data-stu-id="eea62-129">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Opções do menu de deficiências da visão de emulação" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="eea62-131">Opções do menu de **deficiências da visão de emulação**</span><span class="sxs-lookup"><span data-stu-id="eea62-131">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="eea62-132">O Windows principal exibe a simulação da opção selecionada aplicada à página atual.</span><span class="sxs-lookup"><span data-stu-id="eea62-132">The main windows displays the simulation of your selected option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Vídeo com a simulação \* \* desfocada da revisão \* \*" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="eea62-134">Exibição usando simulação de **visão borrada**</span><span class="sxs-lookup"><span data-stu-id="eea62-134">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Vídeo usando a simulação \* \* achromatopsia \* \*" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="eea62-136">Exibir usando a simulação **achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="eea62-136">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="eea62-137">Usar o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="eea62-137">Use the Command Menu</span></span>  

<span data-ttu-id="eea62-138">Você também pode usar o **menu de comando** para acessar as diferentes simulações.</span><span class="sxs-lookup"><span data-stu-id="eea62-138">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="eea62-139">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="eea62-139">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="eea62-141">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="eea62-141">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="eea62-142">Tipo `emulate` , escolha o que você deseja simular e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="eea62-142">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="As diferentes opções de simulação disponíveis no menu de comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="eea62-144">As diferentes opções de simulação disponíveis no **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="eea62-144">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="eea62-145">As ferramentas de **deficiência visual de emulação** simulam a forma como uma pessoa com cada deficiência pode ver seu produto.</span><span class="sxs-lookup"><span data-stu-id="eea62-145">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="eea62-146">Cada pessoa é diferente, portanto, as deficiências de visão variam de acordo com a pessoa com a pessoa.</span><span class="sxs-lookup"><span data-stu-id="eea62-146">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="eea62-147">Para atender melhor às necessidades dos seus usuários, evite qualquer combinação de cores que possa ser um problema.</span><span class="sxs-lookup"><span data-stu-id="eea62-147">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="eea62-148">As ferramentas de **deficiências de visão de emulação** não são uma avaliação completa de acessibilidade do seu produto.</span><span class="sxs-lookup"><span data-stu-id="eea62-148">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="eea62-149">Em vez disso, as ferramentas de **deficiência visual de emulação** devem fornecer uma boa primeira etapa para evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="eea62-149">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "A organização de conscientização de cores cego"  
[AmfcbMain]: https://www.amfcb.org "A base americana do cego colorido (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Ferramentas de renderização do Microsoft Edge (Chromium)"  
