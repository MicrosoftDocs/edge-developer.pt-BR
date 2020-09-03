---
description: Abra a guia sensores e selecione coordenadas na lista geolocalização.
title: Substituir geolocalização com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 269e7ca4bf259aa168c06ac0fd915604731463c4
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992985"
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

# Substituir geolocalização com o Microsoft Edge DevTools  

Muitos websites aproveitam o local do usuário para fornecer uma experiência mais relevante para os usuários.  Por exemplo, um site de clima pode mostrar a previsão local na área de um usuário, após o usuário conceder a permissão de site para acessar a localização do usuário atual.  

<!--todo: add link to user location section when available -->  

Se você estiver criando uma interface do usuário que muda de acordo com o local em que o usuário está localizado, provavelmente desejará verificar se o site se comporta corretamente em locais diferentes ao lado do mundo.  Para substituir a localização geográfica no Microsoft Edge DevTools, conclua as ações a seguir.  

1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
1.  Tipo `sensors` , selecione **Mostrar sensores**e pressione `Enter` .  A guia **sensores** é aberta na parte inferior da janela do devtools.  
1.  Na lista **geolocalização** , selecione uma das cidades predefinidas, como `Tokyo` ou selecione **local personalizado** para inserir coordenadas de longitude e latitude personalizadas, ou selecione **local indisponível** para ver como o seu site se comporta quando o local do usuário não está disponível.  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Selecionar Tóquio na lista de geolocalização" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Selecionar `Tokyo` na lista de **geolocalização**  
    :::image-end:::  
    
## Entrar em contato com a equipe do Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
