---
description: Abra a ferramenta Sensores e navegue até a seção Orientação.
title: Simular orientação de dispositivo com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 754df3b271b44f986802c2847862624f6a8b5bd9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398711"
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

# <a name="simulate-device-orientation-with-microsoft-edge-devtools"></a>Simular orientação de dispositivo com o Microsoft Edge DevTools  

Conclua as seguintes ações para simular diferentes orientações de dispositivo do Microsoft Edge DevTools.  

<!--todo: update device orientation section when available -->  

1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O Menu De comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       O **Menu De comando**  
    :::image-end:::  
    
1.  Digite `sensors` , escolha Mostrar **Sensores**e `Enter` selecione .  A **ferramenta Sensors** é aberta na parte inferior da janela DevTools.  
1.  Na lista **Orientação,** selecione uma das orientações predefinidas, como `Portrait upside down` , ou escolha Orientação **personalizada** para fornecer sua própria orientação exata.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Escolha Retrato de cabeça para baixo na lista De orientação" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             Escolha `Portrait upside down` na lista De **orientação**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Depois de escolher **Orientação personalizada,** os campos , e são `alpha` `beta` `gamma` habilitados.  
          <!--To understand how each axis works, navigate to [Alpha][alpha], [Beta][beta], and [Gamma][gamma].  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          Você também pode definir uma orientação personalizada arrastando o **Modelo de Orientação**.  Segure `Shift` antes de arrastar para girar ao longo do `alpha` eixo.  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="O modelo de orientação" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             O **modelo de orientação**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
