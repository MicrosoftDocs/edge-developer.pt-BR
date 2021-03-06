---
description: Abra a ferramenta Condições de Rede, desabilite Selecionar automaticamente e escolha na lista ou insira uma cadeia de caracteres personalizada.
title: Substituir a cadeia de caracteres de agente do usuário do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a0ba10b551b4853cf204656ca7a9fb014323986b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398690"
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

# <a name="override-the-user-agent-string-from-microsoft-edge-devtools"></a><span data-ttu-id="c0667-104">Substituir a cadeia de caracteres de agente do usuário do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c0667-104">Override the user agent string from Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c0667-105">Para substituir a [cadeia de caracteres de][MDNUserAgent] agente do usuário do Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="c0667-105">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="c0667-106">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="c0667-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O Menu De comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="c0667-108">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="c0667-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c0667-109">Digite `network conditions` , escolha Mostrar condições de **rede**e selecione para abrir a ferramenta `Enter` Condições **de** rede.</span><span class="sxs-lookup"><span data-stu-id="c0667-109">Type `network conditions`, choose **Show Network conditions**, and select `Enter` to open the **Network conditions** tool.</span></span>  
1.  <span data-ttu-id="c0667-110">Na seção **Agente do usuário,** desligue a caixa de **seleção Selecionar** automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c0667-110">In the **User agent** section, turn off the **Select automatically** checkbox.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Desativar Selecionar automaticamente" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       <span data-ttu-id="c0667-112">Desativar Selecionar **automaticamente**</span><span class="sxs-lookup"><span data-stu-id="c0667-112">Turn off **Select automatically**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c0667-113">Escolha uma cadeia de caracteres de agente do usuário na lista ou insira sua própria cadeia de caracteres personalizada.</span><span class="sxs-lookup"><span data-stu-id="c0667-113">Choose a user agent string from the list, or enter your own custom string.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c0667-114">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c0667-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  

> [!NOTE]
> <span data-ttu-id="c0667-116">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c0667-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c0667-117">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c0667-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c0667-119">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c0667-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
