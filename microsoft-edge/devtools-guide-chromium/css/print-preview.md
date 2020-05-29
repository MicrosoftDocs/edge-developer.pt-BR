---
title: Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 659120414597273b15657377c33c800e0c83b7cb
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601835"
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





# <span data-ttu-id="9dd9f-103">Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS)</span><span class="sxs-lookup"><span data-stu-id="9dd9f-103">Force Microsoft Edge DevTools Into Print Preview Mode (CSS Print Media Type)</span></span>   



<span data-ttu-id="9dd9f-104">A [consulta imprimir mídia][MDNUsingMediaQueries] controla a aparência da sua página quando impressa.</span><span class="sxs-lookup"><span data-stu-id="9dd9f-104">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="9dd9f-105">Para forçar sua página no modo de visualização de impressão:</span><span class="sxs-lookup"><span data-stu-id="9dd9f-105">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="9dd9f-106">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="9dd9f-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="9dd9f-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="9dd9f-107">Figure 1</span></span>  
    > <span data-ttu-id="9dd9f-108">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="9dd9f-108">The **Command Menu**</span></span>  
    > ![O menu de comando][ImageCommandMenu]  
    
1.  <span data-ttu-id="9dd9f-110">Tipo `rendering` , selecione **Mostrar renderização**e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9dd9f-110">Type `rendering`, select **Show Rendering**, and then press `Enter`.</span></span>  
1.  <span data-ttu-id="9dd9f-111">Em **emular mídia CSS** , selecione **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="9dd9f-111">Under **Emulate CSS media** select **print**.</span></span>  
    
    > ##### <span data-ttu-id="9dd9f-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="9dd9f-112">Figure 2</span></span>  
    > <span data-ttu-id="9dd9f-113">Modo de visualização de impressão</span><span class="sxs-lookup"><span data-stu-id="9dd9f-113">Print preview mode</span></span>  
    > ![Modo de visualização de impressão][ImagePrintMode]  
    
<span data-ttu-id="9dd9f-115">Aqui, você pode exibir e alterar seu CSS, como qualquer outra página da Web.</span><span class="sxs-lookup"><span data-stu-id="9dd9f-115">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="9dd9f-116">Confira [introdução à exibição e à alteração da CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="9dd9f-116">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

 



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Figura 1: menu de comando"  
[ImagePrintMode]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png "Figura 2: modo de visualização de impressão"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução à exibição e alteração de CSS"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usando consultas de mídia | MDN"  

> [!NOTE]
> <span data-ttu-id="9dd9f-122">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="9dd9f-122">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9dd9f-123">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="9dd9f-123">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9dd9f-125">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9dd9f-125">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
