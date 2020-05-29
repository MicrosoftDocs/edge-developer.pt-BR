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





# Simular a orientação do dispositivo com o Microsoft Edge DevTools   



Para simular orientações de dispositivo diferentes do Microsoft Edge DevTools:  

<!--todo: update device orientation section when available -->  

1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    > ##### Figura 1  
    > O menu de comando  
    > ![O menu de comando][ImageCommandMenu]  
    
1.  Tipo `sensors` , selecione **Mostrar sensores**e pressione `Enter` .  A guia **sensores** é aberta na parte inferior da janela do devtools.  
1.  Na lista **orientação** , selecione uma das orientações predefinidas, como `Portrait upside down` ou escolha **orientação personalizada** para fornecer sua orientação exata.  
    
    > ##### Figura 2  
    > Selecionar `Portrait upside down` na lista **orientação**  
    > ![Selecionando retrato de cabeça para baixo na lista orientação][ImageOrientationPortraitUpsideDown]  
    
    Depois de selecionar **orientação personalizada**, `alpha` os `beta` campos, e `gamma` são habilitados.  
    <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how these axes work.  -->  
    <!--todo: update links to alpha, beta, and gamma section when available -->  
    Você também pode definir uma orientação personalizada arrastando o modelo de **orientação**.  Segure `Shift` antes de arrastar para girar ao longo do `alpha` eixo.  
    
    > ##### Figura 3  
    > O **modelo de orientação**  
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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
