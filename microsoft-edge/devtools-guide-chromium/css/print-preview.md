---
description: Abra a ferramenta "Renderização" e selecione Emular mídia CSS > impressão.
title: Forçar Microsoft Edge DevTools no modo Visualização de Impressão (Tipo de Mídia de Impressão CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6c49d956a9a7185b162ca8e2996e7b3e715b40ab
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564424"
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
# <a name="force-microsoft-edge-devtools-into-print-preview-mode"></a><span data-ttu-id="2998d-104">Forçar Microsoft Edge DevTools no modo visualização de impressão</span><span class="sxs-lookup"><span data-stu-id="2998d-104">Force Microsoft Edge DevTools into Print Preview mode</span></span>  

<span data-ttu-id="2998d-105">A [consulta de mídia de][MDNUsingMediaQueries] impressão controla a aparência da sua página quando impressa.</span><span class="sxs-lookup"><span data-stu-id="2998d-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="2998d-106">Para forçar sua página no modo de visualização de impressão:</span><span class="sxs-lookup"><span data-stu-id="2998d-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="2998d-107">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="2998d-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="2998d-109">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="2998d-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2998d-110">Digite `rendering` , escolha Mostrar **Renderização**e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2998d-110">Type `rendering`, choose **Show Rendering**, and then select `Enter`.</span></span>  
1.  <span data-ttu-id="2998d-111">Em **Emular mídia CSS,** escolha **imprimir**.</span><span class="sxs-lookup"><span data-stu-id="2998d-111">Under **Emulate CSS media**, choose **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Modo de visualização de impressão" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="2998d-113">Modo de visualização de impressão</span><span class="sxs-lookup"><span data-stu-id="2998d-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2998d-114">A partir daqui, você pode exibir e alterar seu CSS, como qualquer outra página da Web.</span><span class="sxs-lookup"><span data-stu-id="2998d-114">From here, you may display and change your CSS, like any other web page.</span></span>  <span data-ttu-id="2998d-115">Navegue [até Introdução exibindo e alterando CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="2998d-115">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2998d-116">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2998d-116">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Ferramentas de desenvolvedor | Microsoft Docs"  
[DevToolsCSSGetStarted]: ./index.md "Começar a exibir e alterar o CSS | Microsoft Docs"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usando consultas de mídia | MDN"  

> [!NOTE]
> <span data-ttu-id="2998d-120">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2998d-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2998d-121">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="2998d-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2998d-123">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2998d-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
