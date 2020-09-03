---
description: Abra a guia "renderização" e selecione "emular mídia CSS" > "imprimir".
title: Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1b71135c5ed2d86903b76e659434ee2125985a24
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993048"
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





# <span data-ttu-id="95f71-104">Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS)</span><span class="sxs-lookup"><span data-stu-id="95f71-104">Force Microsoft Edge DevTools into Print Preview mode (CSS Print Media Type)</span></span>   



<span data-ttu-id="95f71-105">A [consulta imprimir mídia][MDNUsingMediaQueries] controla a aparência da sua página quando impressa.</span><span class="sxs-lookup"><span data-stu-id="95f71-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="95f71-106">Para forçar sua página no modo de visualização de impressão:</span><span class="sxs-lookup"><span data-stu-id="95f71-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="95f71-107">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="95f71-107">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="95f71-109">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="95f71-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="95f71-110">Tipo `rendering` , selecione **Mostrar renderização**e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="95f71-110">Type `rendering`, select **Show Rendering**, and then press `Enter`.</span></span>  
1.  <span data-ttu-id="95f71-111">Em **emular mídia CSS** , selecione **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="95f71-111">Under **Emulate CSS media** select **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Modo de visualização de impressão" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="95f71-113">Modo de visualização de impressão</span><span class="sxs-lookup"><span data-stu-id="95f71-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="95f71-114">Aqui, você pode exibir e alterar seu CSS, como qualquer outra página da Web.</span><span class="sxs-lookup"><span data-stu-id="95f71-114">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="95f71-115">Confira [introdução à exibição e à alteração da CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="95f71-115">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevToolsCSSGetStarted]: ./index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usando consultas de mídia | MDN"  

> [!NOTE]
> <span data-ttu-id="95f71-119">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="95f71-119">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="95f71-120">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="95f71-120">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="95f71-122">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="95f71-122">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
