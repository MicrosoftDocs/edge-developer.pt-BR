---
title: Desabilitar JavaScript com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f3838b4e8eccf83aaa71be35ff477ec56cbe7455
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581807"
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





# <span data-ttu-id="17b93-103">Desabilitar JavaScript com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="17b93-103">Disable JavaScript With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="17b93-104">Para ver como uma página da Web tem a aparência e se comporta quando o JavaScript está desabilitado:</span><span class="sxs-lookup"><span data-stu-id="17b93-104">To see how a web page looks and behaves when JavaScript is disabled:</span></span>  

1.  <span data-ttu-id="17b93-105">[Abra o Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="17b93-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="17b93-106">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="17b93-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="17b93-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="17b93-107">Figure 1</span></span>  
    > <span data-ttu-id="17b93-108">O menu de comando</span><span class="sxs-lookup"><span data-stu-id="17b93-108">The Command Menu</span></span>  
    > ![O menu de comando][ImageCommandMenu]  
    
1.  <span data-ttu-id="17b93-110">Comece a digitar `javascript` , selecione **desativar JavaScript**e pressione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="17b93-110">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="17b93-111">JavaScript agora está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="17b93-111">JavaScript is now disabled.</span></span>  
    
    > ##### <span data-ttu-id="17b93-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="17b93-112">Figure 2</span></span>  
    > <span data-ttu-id="17b93-113">Selecionar **desativar JavaScript** no menu de comando</span><span class="sxs-lookup"><span data-stu-id="17b93-113">Selecting **Disable JavaScript** in the Command Menu</span></span>  
    > ![Selecionar desativar JavaScript no menu de comando][ImageDisableJS]  
    
    <span data-ttu-id="17b93-115">O ícone de aviso amarelo ao lado de **fontes** lembra que o JavaScript está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="17b93-115">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    > ##### <span data-ttu-id="17b93-116">Figura 3</span><span class="sxs-lookup"><span data-stu-id="17b93-116">Figure 3</span></span>  
    > <span data-ttu-id="17b93-117">O ícone de aviso ao lado de **fontes**</span><span class="sxs-lookup"><span data-stu-id="17b93-117">The warning icon next to **Sources**</span></span>  
    > ![O ícone de aviso ao lado de fontes][ImageDisableJSWarning]  

<span data-ttu-id="17b93-119">O JavaScript permanece desabilitado nessa guia por quanto tempo você tiver o DevTools aberto.</span><span class="sxs-lookup"><span data-stu-id="17b93-119">JavaScript remains disabled in this tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="17b93-120">Você pode querer recarregar a página para ver se e como a página depende de JavaScript durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="17b93-120">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="17b93-121">Para habilitar novamente o JavaScript:</span><span class="sxs-lookup"><span data-stu-id="17b93-121">To re-enable JavaScript:</span></span>  

*   <span data-ttu-id="17b93-122">Abra o **menu de comandos** novamente e execute o `Enable JavaScript` comando.</span><span class="sxs-lookup"><span data-stu-id="17b93-122">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="17b93-123">Feche o DevTools.</span><span class="sxs-lookup"><span data-stu-id="17b93-123">Close DevTools.</span></span>  

## <span data-ttu-id="17b93-124">Privacidade Jurídica</span><span class="sxs-lookup"><span data-stu-id="17b93-124">Feedback</span></span>   



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command.msft.png "Figura 1: menu de comando"  
[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command-javascript.msft.png "Figura 2: selecionando desabilitar JavaScript no menu de comando"  
[ImageDisableJSWarning]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-javascript-disabled-warning.msft.png "Figura 3: o ícone de aviso ao lado de fontes"  

<!-- links -->  

[DevToolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="17b93-129">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="17b93-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="17b93-130">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="17b93-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="17b93-132">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="17b93-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
