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
# <a name="override-geolocation-with-microsoft-edge-devtools"></a><span data-ttu-id="a618e-104">Substituir a localização geográfica com Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a618e-104">Override geolocation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="a618e-105">Muitos sites aproveitam a localização do usuário para fornecer uma experiência mais relevante para os usuários.</span><span class="sxs-lookup"><span data-stu-id="a618e-105">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="a618e-106">Por exemplo, um site de previsão do tempo pode mostrar a previsão local na área de um usuário, depois que o usuário concedeu a permissão do site para acessar o local do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="a618e-106">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="a618e-107">Se você estiver criando uma interface do usuário que muda dependendo de onde o usuário está localizado, você provavelmente deseja garantir que o site se comporte corretamente em diferentes lugares ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="a618e-107">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="a618e-108">Para substituir sua localização geográfica Microsoft Edge DevTools, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="a618e-108">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="a618e-109">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="a618e-109">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O Menu De comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="a618e-111">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="a618e-111">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a618e-112">Digite `sensors` , escolha Mostrar **Sensores**e `Enter` selecione .</span><span class="sxs-lookup"><span data-stu-id="a618e-112">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="a618e-113">A **ferramenta Sensors** é aberta na parte inferior da janela DevTools.</span><span class="sxs-lookup"><span data-stu-id="a618e-113">The **Sensors** tool opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="a618e-114">Na lista **Localização** Geográfica, selecione uma das cidades predefinidas, como , ou escolha Local personalizado para inserir coordenadas de longitude e latitude personalizadas ou escolha Local indisponível para exibir como seu site se comporta quando o local do usuário não está `Tokyo` disponível. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a618e-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or choose **Custom location** to enter custom longitude and latitude coordinates, or choose **Location unavailable** to display how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Escolha Tokio na lista De localização geográfica" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="a618e-116">Escolha `Tokyo` na **lista Geolocation**</span><span class="sxs-lookup"><span data-stu-id="a618e-116">Choose `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a618e-117">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a618e-117">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="a618e-118">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a618e-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a618e-119">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="a618e-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a618e-121">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a618e-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
