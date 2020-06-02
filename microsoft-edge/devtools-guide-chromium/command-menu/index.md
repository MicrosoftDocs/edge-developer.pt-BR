---
title: Executar comandos com o menu de comando do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 748008b347a3498008748b9c3f9ecc1445c47f12
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601744"
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





# <span data-ttu-id="1868b-103">Executar comandos com o menu de comando do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1868b-103">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="1868b-104">O menu de comando fornece uma maneira rápida de navegar na interface do usuário do Microsoft Edge DevTools e realizar tarefas comuns, como [desabilitar o JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="1868b-104">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="1868b-105">Você pode estar familiarizado com um recurso semelhante no código do Visual Studio chamado de [paleta de comandos][VisualStudioCodeUICommandPalette], que era a inspiração original para o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="1868b-105">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

> ##### <span data-ttu-id="1868b-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="1868b-106">Figure 1</span></span>  
> <span data-ttu-id="1868b-107">Usar o menu de comandos para desativar o JavaScript</span><span class="sxs-lookup"><span data-stu-id="1868b-107">Using the Command Menu to disable JavaScript</span></span>  
> ![Usar o menu de comandos para desativar o JavaScript][ImageDisableJS]  

## <span data-ttu-id="1868b-109">Abrir o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="1868b-109">Open the Command Menu</span></span>   

<span data-ttu-id="1868b-110">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="1868b-110">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="1868b-111">Ou clique em **Personalizar e controlar devtools** `...` e, em seguida, selecione **executar comando**.</span><span class="sxs-lookup"><span data-stu-id="1868b-111">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

> ##### <span data-ttu-id="1868b-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="1868b-112">Figure 2</span></span>  
> <span data-ttu-id="1868b-113">Comando executar</span><span class="sxs-lookup"><span data-stu-id="1868b-113">Run Command</span></span>  
> ![Comando executar][ImageRunCommand]  

## <span data-ttu-id="1868b-115">Ver outras ações disponíveis</span><span class="sxs-lookup"><span data-stu-id="1868b-115">See other available actions</span></span>   

<span data-ttu-id="1868b-116">Se você usar o fluxo de trabalho descrito em [abrir o menu de comando](#open-the-command-menu), o menu de comandos será aberto com um `>` caractere colocado na caixa de texto do menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="1868b-116">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character prepended to the Command Menu text box.</span></span>  

> ##### <span data-ttu-id="1868b-117">Figura 3</span><span class="sxs-lookup"><span data-stu-id="1868b-117">Figure 3</span></span>  
> <span data-ttu-id="1868b-118">O caractere de comando</span><span class="sxs-lookup"><span data-stu-id="1868b-118">The command character</span></span>  
> ![O caractere de comando][ImageCommandCharacter]  

<span data-ttu-id="1868b-120">Exclua o `>` caractere e digite `?` para ver outras ações que estão disponíveis no menu de comando.</span><span class="sxs-lookup"><span data-stu-id="1868b-120">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

> ##### <span data-ttu-id="1868b-121">Figura 4</span><span class="sxs-lookup"><span data-stu-id="1868b-121">Figure 4</span></span>  
> <span data-ttu-id="1868b-122">Outras ações disponíveis</span><span class="sxs-lookup"><span data-stu-id="1868b-122">Other available actions</span></span>  
> ![Outras ações disponíveis][ImageActions]  

 



<!-- image links -->  

[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command-java.msft.png "Figura 1: usar o menu de comando para desabilitar o JavaScript"  
[ImageRunCommand]: /microsoft-edge/devtools-guide-chromium/media/command-menu-options-run-command.msft.png "Figura 2: comando executar"  
[ImageCommandCharacter]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command.msft.png "Figura 3: o caractere de comando"  
[ImageActions]: /microsoft-edge/devtools-guide-chromium/media/command-menu-help.msft.png "Figura 4: outras ações disponíveis"  

<!-- links -->  

[JavascriptDisable]: /microsoft-edge/devtools-guide-chromium/javascript/disable "Desabilitar JavaScript com o Microsoft Edge DevTools"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Paleta de comandos-UI de código do Visual Studio"  

> [!NOTE]
> <span data-ttu-id="1868b-130">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="1868b-130">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1868b-131">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1868b-131">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1868b-133">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1868b-133">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  