---
title: Substituir geolocalização com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 307064bedf992e528b6d79eed3a2ade3367830d4
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607437"
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





# <span data-ttu-id="551fd-103">Substituir geolocalização com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="551fd-103">Override Geolocation With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="551fd-104">Muitos websites aproveitam o local do usuário para fornecer uma experiência mais relevante para os usuários.</span><span class="sxs-lookup"><span data-stu-id="551fd-104">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="551fd-105">Por exemplo, um site de clima pode mostrar a previsão local na área de um usuário, após o usuário conceder a permissão de site para acessar a localização do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="551fd-105">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="551fd-106">Se você estiver criando uma interface do usuário que muda de acordo com o local em que o usuário está localizado, provavelmente desejará verificar se o site se comporta corretamente em locais diferentes ao lado do mundo.</span><span class="sxs-lookup"><span data-stu-id="551fd-106">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="551fd-107">Para substituir sua localização geográfica no Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="551fd-107">To override your geolocation in Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="551fd-108">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="551fd-108">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="551fd-109">Figura 1</span><span class="sxs-lookup"><span data-stu-id="551fd-109">Figure 1</span></span>  
    > <span data-ttu-id="551fd-110">O menu de comando</span><span class="sxs-lookup"><span data-stu-id="551fd-110">The Command Menu</span></span>  
    > ![O menu de comando][ImageCommandMenu]  
    
1.  <span data-ttu-id="551fd-112">Tipo `sensors` , selecione **Mostrar sensores**e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="551fd-112">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="551fd-113">A guia **sensores** é aberta na parte inferior da janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="551fd-113">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="551fd-114">Na lista **geolocalização** , selecione uma das cidades predefinidas, como `Tokyo` ou selecione **local personalizado** para inserir coordenadas de longitude e latitude personalizadas, ou selecione **local indisponível** para ver como o seu site se comporta quando o local do usuário não está disponível.</span><span class="sxs-lookup"><span data-stu-id="551fd-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or select **Custom location** to enter custom longitude and latitude coordinates, or select **Location unavailable** to see how your site behaves when the user's location is not available.</span></span>  
    
    > ##### <span data-ttu-id="551fd-115">Figura 2</span><span class="sxs-lookup"><span data-stu-id="551fd-115">Figure 2</span></span>  
    > <span data-ttu-id="551fd-116">Selecionando `Tokyo` na lista de **geolocalização**</span><span class="sxs-lookup"><span data-stu-id="551fd-116">Selecting `Tokyo` from the **Geolocation** list</span></span>  
    > ![Selecionando Tóquio na lista de geolocalização][ImageGeolocationTokyo]  
    
<!--## Feedback   

  -->  

<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Figura 1: menu de comando"  
[ImageGeolocationTokyo]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-geolocation-tokyo.msft.png "Figura 2: selecionando Tokyo na lista de geolocalização"  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="551fd-120">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="551fd-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="551fd-121">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="551fd-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="551fd-123">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="551fd-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
