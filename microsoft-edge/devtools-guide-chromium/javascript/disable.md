---
title: Desabilitar JavaScript com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 587f4780432b1b2b964462d2d7f5779f447f1313
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982904"
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





# <span data-ttu-id="32b28-103">Desabilitar JavaScript com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="32b28-103">Disable JavaScript with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="32b28-104">Para ver como uma página da Web tem uma aparência e se comporta quando o JavaScript está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="32b28-104">To see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="32b28-105">[Abra o Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="32b28-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="32b28-106">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="32b28-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="O menu de comando" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="32b28-108">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="32b28-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32b28-109">Comece a digitar `javascript` , selecione **desativar JavaScript**e pressione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="32b28-109">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="32b28-110">JavaScript agora está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="32b28-110">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Selecionar desativar JavaScript no menu de comando" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="32b28-112">Selecionar **desativar JavaScript** no **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="32b28-112">Select **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="32b28-113">O ícone de aviso amarelo ao lado de **fontes** lembra que o JavaScript está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="32b28-113">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="O ícone de aviso ao lado de fontes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="32b28-115">O ícone de aviso ao lado de **fontes**</span><span class="sxs-lookup"><span data-stu-id="32b28-115">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="32b28-116">O JavaScript permanece desabilitado nessa guia por quanto tempo você tiver o DevTools aberto.</span><span class="sxs-lookup"><span data-stu-id="32b28-116">JavaScript remains disabled in this tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="32b28-117">Você pode querer recarregar a página para ver se e como a página depende de JavaScript durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="32b28-117">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="32b28-118">Para habilitar novamente o JavaScript, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="32b28-118">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="32b28-119">Abra o **menu de comandos** novamente e execute o `Enable JavaScript` comando.</span><span class="sxs-lookup"><span data-stu-id="32b28-119">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="32b28-120">Feche o DevTools.</span><span class="sxs-lookup"><span data-stu-id="32b28-120">Close DevTools.</span></span>  

<!--  
## Feedback   


-->  

<!-- links -->  

[DevToolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

> [!NOTE]
> <span data-ttu-id="32b28-122">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="32b28-122">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="32b28-123">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="32b28-123">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="32b28-125">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="32b28-125">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
