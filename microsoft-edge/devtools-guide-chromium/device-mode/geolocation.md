---
description: Abra a guia sensores e selecione coordenadas na lista geolocalização.
title: Substituir geolocalização com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f2bc395993ff59d88360a363b2c4bc12b570f1ab
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125010"
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

# <span data-ttu-id="08cda-104">Substituir geolocalização com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="08cda-104">Override geolocation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="08cda-105">Muitos websites aproveitam o local do usuário para fornecer uma experiência mais relevante para os usuários.</span><span class="sxs-lookup"><span data-stu-id="08cda-105">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="08cda-106">Por exemplo, um site de clima pode mostrar a previsão local na área de um usuário, após o usuário conceder a permissão de site para acessar a localização do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="08cda-106">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="08cda-107">Se você estiver criando uma interface do usuário que muda de acordo com o local em que o usuário está localizado, provavelmente desejará verificar se o site se comporta corretamente em locais diferentes ao lado do mundo.</span><span class="sxs-lookup"><span data-stu-id="08cda-107">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="08cda-108">Para substituir a localização geográfica no Microsoft Edge DevTools, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="08cda-108">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="08cda-109">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.</span><span class="sxs-lookup"><span data-stu-id="08cda-109">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="08cda-111">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="08cda-111">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="08cda-112">Digite `sensors` , escolha **Mostrar sensores**e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="08cda-112">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="08cda-113">A guia **sensores** é aberta na parte inferior da janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="08cda-113">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="08cda-114">Na lista **geolocalização** , selecione uma das cidades predefinidas, como `Tokyo` ou escolha o **local personalizado** para inserir coordenadas de longitude e latitude personalizadas ou escolha **local indisponível** para ver como o seu site se comporta quando o local do usuário não está disponível.</span><span class="sxs-lookup"><span data-stu-id="08cda-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or choose **Custom location** to enter custom longitude and latitude coordinates, or choose **Location unavailable** to see how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="08cda-116">Selecionar `Tokyo` na lista de **geolocalização**</span><span class="sxs-lookup"><span data-stu-id="08cda-116">Select `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="08cda-117">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="08cda-117">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="08cda-118">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="08cda-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="08cda-119">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="08cda-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="08cda-121">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="08cda-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
