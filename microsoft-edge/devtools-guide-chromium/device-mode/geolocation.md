---
description: Abra a ferramenta Sensores e selecione coordenadas na lista Geolocalização.
title: Substituir a localização geográfica com Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5e162d5591dec4013a899a16b0c56fd09d58610f
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564326"
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
# <a name="override-geolocation-with-microsoft-edge-devtools"></a>Substituir a localização geográfica com Microsoft Edge DevTools  

Muitos sites aproveitam a localização do usuário para fornecer uma experiência mais relevante para os usuários.  Por exemplo, um site de previsão do tempo pode mostrar a previsão local na área de um usuário, depois que o usuário concedeu a permissão do site para acessar o local do usuário atual.  

<!--todo: add link to user location section when available -->  

Se você estiver criando uma interface do usuário que muda dependendo de onde o usuário está localizado, você provavelmente deseja garantir que o site se comporte corretamente em diferentes lugares ao redor do mundo.  Para substituir sua localização geográfica Microsoft Edge DevTools, conclua as seguintes ações.  

1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O Menu De comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       O **Menu De comando**  
    :::image-end:::  
    
1.  Digite `sensors` , escolha Mostrar **Sensores**e `Enter` selecione .  A **ferramenta Sensors** é aberta na parte inferior da janela DevTools.  
1.  Na lista **Localização** Geográfica, selecione uma das cidades predefinidas, como , ou escolha Local personalizado para inserir coordenadas de longitude e latitude personalizadas ou escolha Local indisponível para exibir como seu site se comporta quando o local do usuário não está `Tokyo` disponível. **** ****  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Escolha Tokio na lista De localização geográfica" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Escolha `Tokyo` na **lista Geolocation**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
