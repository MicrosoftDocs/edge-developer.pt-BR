---
description: Abrir o menu de comando e executar o comando "desabilitar JavaScript".
title: Desabilitar JavaScript com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f7aafee4b05f843319a4a744e6cba148d4642667
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230667"
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

# <span data-ttu-id="fae68-104">Desabilitar JavaScript com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fae68-104">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="fae68-105">Conclua as seguintes ações para ver como uma página da Web tem a aparência e se comporta quando o JavaScript está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fae68-105">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="fae68-106">[Abra o Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="fae68-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="fae68-107">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.</span><span class="sxs-lookup"><span data-stu-id="fae68-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="O menu de comando" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="fae68-109">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="fae68-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fae68-110">Comece a digitar `javascript` , escolha **desabilitar JavaScript**e, em seguida, selecione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="fae68-110">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="fae68-111">JavaScript agora está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fae68-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Selecionar desativar JavaScript no menu de comando" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="fae68-113">Escolha **desativar JavaScript** no **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="fae68-113">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="fae68-114">O ícone de aviso amarelo ao lado de **fontes** lembra que o JavaScript está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fae68-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="O ícone de aviso ao lado de fontes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="fae68-116">O ícone de aviso ao lado de **fontes**</span><span class="sxs-lookup"><span data-stu-id="fae68-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="fae68-117">O JavaScript permanece desabilitado na guia pelo tempo em que você tiver o DevTools aberto.</span><span class="sxs-lookup"><span data-stu-id="fae68-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="fae68-118">Você pode querer recarregar a página para ver se e como a página depende de JavaScript durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="fae68-118">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="fae68-119">Para habilitar novamente o JavaScript, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="fae68-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="fae68-120">Abra o **menu de comandos** novamente e execute o `Enable JavaScript` comando.</span><span class="sxs-lookup"><span data-stu-id="fae68-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="fae68-121">Feche o DevTools.</span><span class="sxs-lookup"><span data-stu-id="fae68-121">Close DevTools.</span></span>  

## <span data-ttu-id="fae68-122">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fae68-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

> [!NOTE]
> <span data-ttu-id="fae68-124">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fae68-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fae68-125">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="fae68-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fae68-127">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fae68-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
