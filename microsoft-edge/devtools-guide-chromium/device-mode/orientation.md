---
title: Simular a orientação do dispositivo com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 9e8115819fa6c3209a6c82940e033113783ece0c
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607318"
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





# <span data-ttu-id="2191c-103">Simular a orientação do dispositivo com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2191c-103">Simulate Device Orientation With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="2191c-104">Para simular orientações de dispositivo diferentes do Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="2191c-104">To simulate different device orientations from Microsoft Edge DevTools:</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="2191c-105">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="2191c-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="2191c-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="2191c-106">Figure 1</span></span>  
    > <span data-ttu-id="2191c-107">O menu de comando</span><span class="sxs-lookup"><span data-stu-id="2191c-107">The Command Menu</span></span>  
    > ![O menu de comando][ImageCommandMenu]  
    
1.  <span data-ttu-id="2191c-109">Tipo `sensors` , selecione **Mostrar sensores**e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2191c-109">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="2191c-110">A guia **sensores** é aberta na parte inferior da janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="2191c-110">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="2191c-111">Na lista **orientação** , selecione uma das orientações predefinidas, como `Portrait upside down` ou escolha **orientação personalizada** para fornecer sua orientação exata.</span><span class="sxs-lookup"><span data-stu-id="2191c-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or select **Custom orientation** to provide your own exact orientation.</span></span>  
    
    > ##### <span data-ttu-id="2191c-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="2191c-112">Figure 2</span></span>  
    > <span data-ttu-id="2191c-113">Selecionar `Portrait upside down` na lista **orientação**</span><span class="sxs-lookup"><span data-stu-id="2191c-113">Selecting `Portrait upside down` from the **Orientation** list</span></span>  
    > ![Selecionando retrato de cabeça para baixo na lista orientação][ImageOrientationPortraitUpsideDown]  
    
    <span data-ttu-id="2191c-115">Depois de selecionar **orientação personalizada**, `alpha` os `beta` campos, e `gamma` são habilitados.</span><span class="sxs-lookup"><span data-stu-id="2191c-115">After selecting **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
    <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how these axes work.  -->  
    <!--todo: update links to alpha, beta, and gamma section when available -->  
    <span data-ttu-id="2191c-116">Você também pode definir uma orientação personalizada arrastando o modelo de **orientação**.</span><span class="sxs-lookup"><span data-stu-id="2191c-116">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="2191c-117">Segure `Shift` antes de arrastar para girar ao longo do `alpha` eixo.</span><span class="sxs-lookup"><span data-stu-id="2191c-117">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
    
    > ##### <span data-ttu-id="2191c-118">Figura 3</span><span class="sxs-lookup"><span data-stu-id="2191c-118">Figure 3</span></span>  
    > <span data-ttu-id="2191c-119">O **modelo de orientação**</span><span class="sxs-lookup"><span data-stu-id="2191c-119">The **Orientation Model**</span></span>  
    > ![O modelo de orientação][ImageOrientationModel]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Figura 1: menu de comando"  
[ImageOrientationPortraitUpsideDown]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png "Figura 2: selecionando retrato de cabeça para baixo na lista orientação"  
[ImageOrientationModel]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-custom.msft.png "Figura 3: o modelo de orientação"  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation \& Motion"  -->  

> [!NOTE]
> <span data-ttu-id="2191c-124">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="2191c-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2191c-125">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="2191c-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2191c-127">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2191c-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
