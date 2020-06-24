---
title: Emular deficiências visuais no Microsoft Edge DevTools (cegueira para cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758048"
---
# <span data-ttu-id="54d1d-103">Emular deficiências de visão</span><span class="sxs-lookup"><span data-stu-id="54d1d-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="54d1d-104">No mundo inteiro, aproximadamente 8% de homens e 0,5% das mulheres têm uma [deficiência de visão de cor][ColorblindawarenessMain] comumente chamada de "cegueira para cores".</span><span class="sxs-lookup"><span data-stu-id="54d1d-104">Worldwide approximately 8% of men and 0.5% of women have a [color vision deficiency][ColorblindawarenessMain] commonly named "Color Blindness".</span></span>  <span data-ttu-id="54d1d-105">O [Microsoft Edge devtools][MicrosoftEdgeDevTools] permite que você eMule várias deficiências conhecidas e forneça uma visualização do seu produto para revisão.</span><span class="sxs-lookup"><span data-stu-id="54d1d-105">[Microsoft Edge DevTools][MicrosoftEdgeDevTools] enables you to emulate various known deficiencies and provide a preview of your product for you to review.</span></span>  

| <span data-ttu-id="54d1d-106">Deficiência de cor</span><span class="sxs-lookup"><span data-stu-id="54d1d-106">Color Deficiency</span></span> | <span data-ttu-id="54d1d-107">Detalhes</span><span class="sxs-lookup"><span data-stu-id="54d1d-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="54d1d-108">Visão desfocada</span><span class="sxs-lookup"><span data-stu-id="54d1d-108">Blurred vision</span></span> |  |   
| <span data-ttu-id="54d1d-109">Protanopia</span><span class="sxs-lookup"><span data-stu-id="54d1d-109">Protanopia</span></span> | <span data-ttu-id="54d1d-110">A incapacidade de perceber qualquer luz vermelha.</span><span class="sxs-lookup"><span data-stu-id="54d1d-110">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="54d1d-111">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="54d1d-111">Deuteranopia</span></span> | <span data-ttu-id="54d1d-112">A incapacidade de perceber qualquer luz verde.</span><span class="sxs-lookup"><span data-stu-id="54d1d-112">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="54d1d-113">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="54d1d-113">Tritanopia</span></span> | <span data-ttu-id="54d1d-114">A incapacidade de perceber qualquer luz azul.</span><span class="sxs-lookup"><span data-stu-id="54d1d-114">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="54d1d-115">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="54d1d-115">Achromatopsia</span></span> | <span data-ttu-id="54d1d-116">A incapacidade de perceber qualquer cor, com exceção do sombreamento de cinza.</span><span class="sxs-lookup"><span data-stu-id="54d1d-116">The inability to perceive any color, except for shades of grey.</span></span> |  

## <span data-ttu-id="54d1d-117">Navegar até as ferramentas de renderização</span><span class="sxs-lookup"><span data-stu-id="54d1d-117">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="54d1d-118">Para testar seu produto da Web atual em busca de deficiências de cores, abra as [ferramentas de renderização][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="54d1d-118">To test your current web product for color deficiencies, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="54d1d-119">Abrir as ferramentas de renderização selecionando o `...` item de menu na barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="54d1d-119">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="54d1d-120">Selecionar</span><span class="sxs-lookup"><span data-stu-id="54d1d-120">Select</span></span> `More tools`  
1.  <span data-ttu-id="54d1d-121">Selecionar</span><span class="sxs-lookup"><span data-stu-id="54d1d-121">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrindo as ferramentas de renderização" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="54d1d-123">Abrindo as **ferramentas de renderização**</span><span class="sxs-lookup"><span data-stu-id="54d1d-123">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="54d1d-124">O menu **renderização** é exibido na metade inferior da devtools.</span><span class="sxs-lookup"><span data-stu-id="54d1d-124">The **Rendering** menu appears in the bottom half of the DevTools.</span></span>  

1.  <span data-ttu-id="54d1d-125">Role para baixo até o `Emulate Vision deficiencies` item de menu e selecione uma das opções.</span><span class="sxs-lookup"><span data-stu-id="54d1d-125">Scroll down to the `Emulate Vision deficiencies` menu item and select from the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="O menu de deficiências da visão de emulação das ferramentas de renderização" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="54d1d-127">O menu de **deficiências da visão de emulação** das ferramentas de **renderização**</span><span class="sxs-lookup"><span data-stu-id="54d1d-127">The **Emulate Vision Deficiencies** menu of the **Rendering** tools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="54d1d-128">Escolha qualquer uma das opções</span><span class="sxs-lookup"><span data-stu-id="54d1d-128">Choose any of the options</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Opções do menu de deficiências da visão de emulação" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="54d1d-130">Opções do menu de **deficiências da visão de emulação**</span><span class="sxs-lookup"><span data-stu-id="54d1d-130">The **Emulate Vision Deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="54d1d-131">A página atual é exibida em uma simulação de como ela pode aparecer para um usuário com a deficiência selecionada.</span><span class="sxs-lookup"><span data-stu-id="54d1d-131">The current page is displayed in a simulation of how it may appear to a user with the chosen deficiency.</span></span>  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Documentação das ferramentas de desenvolvedor do Microsoft Edge na emulação de visão borrada" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="54d1d-133">Exibido usando a emulação de **visão desfocada**</span><span class="sxs-lookup"><span data-stu-id="54d1d-133">Displayed using **Blurred Vision** emulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Documentação das ferramentas de desenvolvedor do Microsoft Edge na emulação do achromatopsia Vision" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="54d1d-135">Exibir usando a emulação de **visão achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="54d1d-135">Display using **Achromatopsia Vision** emulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="54d1d-136">Usar o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="54d1d-136">Using the command menu</span></span>  

<span data-ttu-id="54d1d-137">Você também pode alcançar diferentes emulações sem passar pelos vários menus usando o menu de **comandos**.</span><span class="sxs-lookup"><span data-stu-id="54d1d-137">You may also reach the different emulations without going through the various menus using the **Command Menu**.</span></span>  

1.  <span data-ttu-id="54d1d-138">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="54d1d-138">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="54d1d-140">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="54d1d-140">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="54d1d-141">Tipo `emulate` , escolha o que você deseja simular e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="54d1d-141">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="As diferentes opções de emulação disponíveis no menu de comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="54d1d-143">As diferentes opções de emulação disponíveis no **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="54d1d-143">The different emulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="54d1d-144">As ferramentas de emulação são as aproximações de como uma pessoa com cada deficiência pode ver seu produto.</span><span class="sxs-lookup"><span data-stu-id="54d1d-144">The emulation tools are approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="54d1d-145">Cada pessoa é diferente, portanto, as deficiências de visão variam de acordo com a pessoa com a pessoa.</span><span class="sxs-lookup"><span data-stu-id="54d1d-145">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="54d1d-146">Para atender melhor às necessidades dos seus usuários, evite qualquer combinação de cores que possa ser um problema.</span><span class="sxs-lookup"><span data-stu-id="54d1d-146">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="54d1d-147">As ferramentas de emulação não são uma avaliação completa da acessibilidade do seu produto, mas você deve ter uma boa primeira etapa em relação a evitar as principais deficiências.</span><span class="sxs-lookup"><span data-stu-id="54d1d-147">The emulation tools are not a full assessment of the accessibility of your product, but you should have a good first step towards avoiding the biggest deficiencies.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "A organização de conscientização de cores cego"  
[AmfcbMain]: https://www.amfcb.org "A base americana do cego colorido (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Ferramentas de renderização do Microsoft Edge (Chromium)"  
