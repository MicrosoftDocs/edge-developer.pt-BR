---
description: Abra o Menu de Comando e execute o comando "Desabilitar JavaScript".
title: Desabilitar JavaScript com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2067944fa17c332dd15ffb3ef97afe02d35685ed
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398557"
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

# <a name="disable-javascript-with-microsoft-edge-devtools"></a><span data-ttu-id="48ced-104">Desabilitar JavaScript com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="48ced-104">Disable JavaScript with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="48ced-105">Conclua as seguintes ações para exibir a aparência e o comportamento de uma página da Web quando o JavaScript está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48ced-105">Complete the following actions to display how a webpage looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="48ced-106">[Abra o Microsoft Edge DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="48ced-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="48ced-107">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="48ced-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="O Menu De comando" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="48ced-109">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="48ced-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="48ced-110">Comece a `javascript` digitar, escolha **Desabilitar JavaScript**e, em seguida, selecione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="48ced-110">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="48ced-111">JavaScript agora está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48ced-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Escolha Desabilitar JavaScript no Menu de Comando" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="48ced-113">Escolha **Desabilitar JavaScript** no **Menu de Comando**</span><span class="sxs-lookup"><span data-stu-id="48ced-113">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="48ced-114">O ícone de aviso amarelo ao lado **de Fontes** lembra que JavaScript está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48ced-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="O ícone de aviso ao lado de Fontes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="48ced-116">O ícone de aviso ao lado de **Fontes**</span><span class="sxs-lookup"><span data-stu-id="48ced-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="48ced-117">JavaScript permanece desabilitado na guia enquanto você tiver DevTools aberto.</span><span class="sxs-lookup"><span data-stu-id="48ced-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="48ced-118">Talvez você queira atualizar a página para revisar se e como a página da Web depende do JavaScript durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="48ced-118">You may want to refresh the page to review if and how the webpage depends on JavaScript while loading.</span></span>  

<span data-ttu-id="48ced-119">Para habilitar o JavaScript, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="48ced-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="48ced-120">Abra o **Menu de Comando** novamente e execute o `Enable JavaScript` comando.</span><span class="sxs-lookup"><span data-stu-id="48ced-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="48ced-121">Feche DevTools.</span><span class="sxs-lookup"><span data-stu-id="48ced-121">Close DevTools.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="48ced-122">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="48ced-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="48ced-124">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48ced-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="48ced-125">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="48ced-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="48ced-127">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48ced-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
