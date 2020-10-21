---
description: Abra a guia condições de rede, desabilite selecionar automaticamente e escolha na lista ou insira uma cadeia de caracteres personalizada.
title: Substituir a cadeia de caracteres do agente do usuário do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: befbe186a5992c651f877a18f1c3232bf212394a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124947"
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

# Substituir a cadeia de caracteres do agente do usuário do Microsoft Edge DevTools  

Para substituir a cadeia de caracteres do [agente do usuário][MDNUserAgent] do Microsoft Edge devtools:  

1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
1.  Tipo `network conditions` , escolha **Mostrar condições de rede**e selecione `Enter` para abrir a guia **condições de rede** .  
1.  Na seção **agente do usuário** , desabilite a caixa de seleção **selecionar automaticamente** .  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       Desabilitar **selecionar automaticamente**  
    :::image-end:::  
    
1.  Selecione uma cadeia de caracteres de agente do usuário na lista ou insira sua própria cadeia de caracteres personalizada.  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
