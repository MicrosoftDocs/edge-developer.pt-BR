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

# <span data-ttu-id="a0954-104">Substituir a cadeia de caracteres do agente do usuário do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a0954-104">Override the user agent string from Microsoft Edge DevTools</span></span>  

<span data-ttu-id="a0954-105">Para substituir a cadeia de caracteres do [agente do usuário][MDNUserAgent] do Microsoft Edge devtools:</span><span class="sxs-lookup"><span data-stu-id="a0954-105">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="a0954-106">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.</span><span class="sxs-lookup"><span data-stu-id="a0954-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="a0954-108">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="a0954-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a0954-109">Tipo `network conditions` , escolha **Mostrar condições de rede**e selecione `Enter` para abrir a guia **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="a0954-109">Type `network conditions`, choose **Show Network conditions**, and select `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="a0954-110">Na seção **agente do usuário** , desabilite a caixa de seleção **selecionar automaticamente** .</span><span class="sxs-lookup"><span data-stu-id="a0954-110">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       <span data-ttu-id="a0954-112">Desabilitar **selecionar automaticamente**</span><span class="sxs-lookup"><span data-stu-id="a0954-112">Disable **Select automatically**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a0954-113">Selecione uma cadeia de caracteres de agente do usuário na lista ou insira sua própria cadeia de caracteres personalizada.</span><span class="sxs-lookup"><span data-stu-id="a0954-113">Select a user agent string from the list, or enter your own custom string.</span></span>  
    
## <span data-ttu-id="a0954-114">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a0954-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  

> [!NOTE]
> <span data-ttu-id="a0954-116">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="a0954-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a0954-117">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a0954-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a0954-119">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a0954-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
