---
description: Abra a guia sensores e vá para a seção orientação.
title: Simular a orientação do dispositivo com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 01e6d3a24513b504665dbe0c03d9e72cc1f97533
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124954"
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

# <span data-ttu-id="d7abb-104">Simular a orientação do dispositivo com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d7abb-104">Simulate device orientation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="d7abb-105">Conclua as seguintes ações para simular orientações de dispositivo diferentes do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="d7abb-105">Complete the following actions to simulate different device orientations from Microsoft Edge DevTools.</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="d7abb-106">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.</span><span class="sxs-lookup"><span data-stu-id="d7abb-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="d7abb-108">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="d7abb-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7abb-109">Digite `sensors` , escolha **Mostrar sensores**e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d7abb-109">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="d7abb-110">A guia **sensores** é aberta na parte inferior da janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="d7abb-110">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="d7abb-111">Na lista **orientação** , selecione uma das orientações predefinidas, por exemplo `Portrait upside down` , ou escolha **orientação personalizada** para fornecer sua orientação exata.</span><span class="sxs-lookup"><span data-stu-id="d7abb-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or choose **Custom orientation** to provide your own exact orientation.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             <span data-ttu-id="d7abb-113">Selecionar `Portrait upside down` na lista **orientação**</span><span class="sxs-lookup"><span data-stu-id="d7abb-113">Select `Portrait upside down` from the **Orientation** list</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="d7abb-114">Depois que você escolhe **orientação personalizada**, `alpha` os `beta` campos, e `gamma` são habilitados.</span><span class="sxs-lookup"><span data-stu-id="d7abb-114">After you choose **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
          <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how each axis works.  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          <span data-ttu-id="d7abb-115">Você também pode definir uma orientação personalizada arrastando o modelo de **orientação**.</span><span class="sxs-lookup"><span data-stu-id="d7abb-115">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="d7abb-116">Segure `Shift` antes de arrastar para girar ao longo do `alpha` eixo.</span><span class="sxs-lookup"><span data-stu-id="d7abb-116">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             <span data-ttu-id="d7abb-118">O **modelo de orientação**</span><span class="sxs-lookup"><span data-stu-id="d7abb-118">The **Orientation Model**</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="d7abb-119">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d7abb-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> <span data-ttu-id="d7abb-120">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="d7abb-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d7abb-121">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d7abb-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d7abb-123">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d7abb-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
