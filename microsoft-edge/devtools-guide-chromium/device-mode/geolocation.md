---
title: Substituir geolocalização com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6cc690e7f2f93448c2facb01f0ca2f9b679a473a
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986098"
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

# <span data-ttu-id="c0825-103">Substituir geolocalização com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c0825-103">Override geolocation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c0825-104">Muitos websites aproveitam o local do usuário para fornecer uma experiência mais relevante para os usuários.</span><span class="sxs-lookup"><span data-stu-id="c0825-104">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="c0825-105">Por exemplo, um site de clima pode mostrar a previsão local na área de um usuário, após o usuário conceder a permissão de site para acessar a localização do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c0825-105">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="c0825-106">Se você estiver criando uma interface do usuário que muda de acordo com o local em que o usuário está localizado, provavelmente desejará verificar se o site se comporta corretamente em locais diferentes ao lado do mundo.</span><span class="sxs-lookup"><span data-stu-id="c0825-106">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="c0825-107">Para substituir a localização geográfica no Microsoft Edge DevTools, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0825-107">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="c0825-108">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="c0825-108">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="c0825-110">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="c0825-110">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c0825-111">Tipo `sensors` , selecione **Mostrar sensores**e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c0825-111">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="c0825-112">A guia **sensores** é aberta na parte inferior da janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="c0825-112">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="c0825-113">Na lista **geolocalização** , selecione uma das cidades predefinidas, como `Tokyo` ou selecione **local personalizado** para inserir coordenadas de longitude e latitude personalizadas, ou selecione **local indisponível** para ver como o seu site se comporta quando o local do usuário não está disponível.</span><span class="sxs-lookup"><span data-stu-id="c0825-113">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or select **Custom location** to enter custom longitude and latitude coordinates, or select **Location unavailable** to see how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Selecionar Tóquio na lista de geolocalização" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="c0825-115">Selecionar `Tokyo` na lista de **geolocalização**</span><span class="sxs-lookup"><span data-stu-id="c0825-115">Select `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c0825-116">Entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c0825-116">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="c0825-117">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="c0825-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c0825-118">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c0825-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c0825-120">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c0825-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
