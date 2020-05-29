---
title: Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601343"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="ab4bb-103">Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)</span><span class="sxs-lookup"><span data-stu-id="ab4bb-103">Change Microsoft Edge DevTools Placement (Undock, Dock To Bottom, Dock To Left)</span></span>   



<span data-ttu-id="ab4bb-104">Por padrão, o DevTools está encaixado à direita do seu visor.</span><span class="sxs-lookup"><span data-stu-id="ab4bb-104">By default DevTools is docked to the right of your viewport.</span></span>  <span data-ttu-id="ab4bb-105">Você também pode encaixar na parte inferior, encaixar à esquerda ou desencaixar o DevTools em uma janela separada.</span><span class="sxs-lookup"><span data-stu-id="ab4bb-105">You may also dock to bottom, dock to left, or undock the DevTools to a separate window.</span></span>  

> ##### <span data-ttu-id="ab4bb-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="ab4bb-106">Figure 1</span></span>  
> <span data-ttu-id="ab4bb-107">Encaixar à esquerda</span><span class="sxs-lookup"><span data-stu-id="ab4bb-107">Dock To Left</span></span>  
> ![Encaixar à esquerda][ImageDockLeft]  

> ##### <span data-ttu-id="ab4bb-109">Figura 2</span><span class="sxs-lookup"><span data-stu-id="ab4bb-109">Figure 2</span></span>  
> <span data-ttu-id="ab4bb-110">Encaixar na parte inferior</span><span class="sxs-lookup"><span data-stu-id="ab4bb-110">Dock To Bottom</span></span>  
> ![Encaixar na parte inferior][ImageDockBottom]  

> ##### <span data-ttu-id="ab4bb-112">Figura 3</span><span class="sxs-lookup"><span data-stu-id="ab4bb-112">Figure 3</span></span>  
> <span data-ttu-id="ab4bb-113">Navegador em janela separada</span><span class="sxs-lookup"><span data-stu-id="ab4bb-113">Browser in separate window</span></span>  
> ![Navegador em janela separada][ImageUndockBrowser]  

> ##### <span data-ttu-id="ab4bb-115">Figura 4</span><span class="sxs-lookup"><span data-stu-id="ab4bb-115">Figure 4</span></span>  
> <span data-ttu-id="ab4bb-116">DevTools desencaixada em janela separada</span><span class="sxs-lookup"><span data-stu-id="ab4bb-116">Undocked DevTools in separate window</span></span>  
> ![DevTools desencaixada em janela separada][ImageUndockDevTools]  

## <span data-ttu-id="ab4bb-118">Alterar o posicionamento a partir do menu principal</span><span class="sxs-lookup"><span data-stu-id="ab4bb-118">Change placement from the main menu</span></span>   

1.  <span data-ttu-id="ab4bb-119">Clique em **Personalizar e controle devtools** `...` e selecione desencaixar em desencaixar de **janela separado** ![ ][ImageUndockIcon] , **encaixar na barra inferior** ![ para baixo ][ImageBottomIcon] ou **encaixar à esquerda** para a ![ esquerda ][ImageLeftIcon] .</span><span class="sxs-lookup"><span data-stu-id="ab4bb-119">Click **Customize And Control DevTools** `...` and select **Undock Into Separate Window** ![Undock][ImageUndockIcon], **Dock To Bottom** ![Dock To Bottom][ImageBottomIcon], or **Dock To Left** ![Dock To Left][ImageLeftIcon].</span></span>  
    
    > ##### <span data-ttu-id="ab4bb-120">Figura 5</span><span class="sxs-lookup"><span data-stu-id="ab4bb-120">Figure 5</span></span>  
    > <span data-ttu-id="ab4bb-121">Selecionar **desencaixar em uma janela separada**</span><span class="sxs-lookup"><span data-stu-id="ab4bb-121">Selecting **Undock Into Separate Window**</span></span>  
    > ![Selecionar desencaixar em uma janela separada][ImageUndockSettings]  
    
## <span data-ttu-id="ab4bb-123">Alterar o posicionamento no menu de comando</span><span class="sxs-lookup"><span data-stu-id="ab4bb-123">Change placement from the Command Menu</span></span>   

1.  <span data-ttu-id="ab4bb-124">[Abrir o menu de comandos][DevtoolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="ab4bb-124">[Open the Command Menu][DevtoolsCommandMenu].</span></span>  
1.  <span data-ttu-id="ab4bb-125">Execute um dos seguintes comandos: `Dock To Bottom` , `Undock Into Separate Window` .</span><span class="sxs-lookup"><span data-stu-id="ab4bb-125">Run one of the following commands: `Dock To Bottom`, `Undock Into Separate Window`.</span></span>  <span data-ttu-id="ab4bb-126">No momento, não há um comando para encaixar à esquerda, mas você pode acessá-lo no [menu principal](#change-placement-from-the-main-menu).</span><span class="sxs-lookup"><span data-stu-id="ab4bb-126">Currently there is no command for docking to left, but you may access it from the [main menu](#change-placement-from-the-main-menu).</span></span>  
    
    > ##### <span data-ttu-id="ab4bb-127">Figura 6</span><span class="sxs-lookup"><span data-stu-id="ab4bb-127">Figure 6</span></span>  
    > <span data-ttu-id="ab4bb-128">O comando desencaixar</span><span class="sxs-lookup"><span data-stu-id="ab4bb-128">The undock command</span></span>  
    > ![O comando desencaixar][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Figura 1: encaixar à esquerda"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Figura 2: encaixar na parte inferior"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Figura 3: navegador em uma janela separada"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Figura 4: DevTools desencaixada em janela separada"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Figura 5: selecionando desencaixar em uma janela separada"  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Figura 6: o comando desencaixar"  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="ab4bb-137">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="ab4bb-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ab4bb-138">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/customize/placement) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ab4bb-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/customize/placement) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ab4bb-140">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ab4bb-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
