---
title: Substituir a cadeia de caracteres do agente do usuário do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 376e1550d0dc31f3b47b6badd6970076a8c13f91
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607304"
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





# <span data-ttu-id="c85eb-103">Substituir a cadeia de caracteres do agente do usuário do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c85eb-103">Override The User Agent String From Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c85eb-104">Para substituir a cadeia de caracteres do [agente do usuário][MDNUserAgent] do Microsoft Edge devtools:</span><span class="sxs-lookup"><span data-stu-id="c85eb-104">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="c85eb-105">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="c85eb-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="c85eb-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="c85eb-106">Figure 1</span></span>  
    > <span data-ttu-id="c85eb-107">O menu de comando</span><span class="sxs-lookup"><span data-stu-id="c85eb-107">The Command Menu</span></span>  
    > ![O menu de comando][ImageCommandMenu]  
    
1.  <span data-ttu-id="c85eb-109">Tipo `network conditions` , selecione **Mostrar condições de rede**e pressione `Enter` para abrir a guia **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="c85eb-109">Type `network conditions`, select **Show Network conditions**, and press `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="c85eb-110">Na seção **agente do usuário** , desabilite a caixa de seleção **selecionar automaticamente** .</span><span class="sxs-lookup"><span data-stu-id="c85eb-110">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="c85eb-111">Figura 2</span><span class="sxs-lookup"><span data-stu-id="c85eb-111">Figure 2</span></span>  
    > <span data-ttu-id="c85eb-112">Desativando **selecionar automaticamente**</span><span class="sxs-lookup"><span data-stu-id="c85eb-112">Disabling **Select automatically**</span></span>  
    > ![Desativando selecionar automaticamente][ImageUserAgentDisableSelectAutomatically]  
    
1.  <span data-ttu-id="c85eb-114">Selecione uma cadeia de caracteres de agente do usuário na lista ou insira sua própria cadeia de caracteres personalizada.</span><span class="sxs-lookup"><span data-stu-id="c85eb-114">Select a user agent string from the list, or enter your own custom string.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Figura 1: menu de comando"  
[ImageUserAgentDisableSelectAutomatically]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png "Figura 2: desativando selecionar automaticamente"  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  

> [!NOTE]
> <span data-ttu-id="c85eb-118">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="c85eb-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c85eb-119">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c85eb-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c85eb-121">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c85eb-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
