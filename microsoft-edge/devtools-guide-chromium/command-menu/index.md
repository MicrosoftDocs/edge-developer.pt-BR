---
description: Um guia sobre como abrir o menu de comando, executar comandos, revisar outras ações e muito mais.
title: Executar comandos com o menu de comando do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2f13461fdf04e034b324db63c6ec6d9090f80f50
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125276"
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

# <span data-ttu-id="22561-104">Executar comandos com o menu de comando do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="22561-104">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>  

  

<span data-ttu-id="22561-105">O menu de comando fornece uma maneira rápida de navegar na interface do usuário do Microsoft Edge DevTools e realizar tarefas comuns, como [desabilitar o JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="22561-105">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="22561-106">Você pode estar familiarizado com um recurso semelhante no código do Visual Studio chamado de [paleta de comandos][VisualStudioCodeUICommandPalette], que era a inspiração original para o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="22561-106">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Usar o menu de comandos para desativar o JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="22561-108">Usar o menu de comandos para desativar o JavaScript</span><span class="sxs-lookup"><span data-stu-id="22561-108">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="22561-109">Abrir o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="22561-109">Open the Command Menu</span></span>  

<span data-ttu-id="22561-110">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="22561-110">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="22561-111">Ou escolha **Personalizar e controlar devtools** `...` e, em seguida, escolha **executar comando**.</span><span class="sxs-lookup"><span data-stu-id="22561-111">Or choose **Customize And Control DevTools** `...` and then choose **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Usar o menu de comandos para desativar o JavaScript" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="22561-113">Comando executar</span><span class="sxs-lookup"><span data-stu-id="22561-113">Run Command</span></span>  
:::image-end:::  

## <span data-ttu-id="22561-114">Ver outras ações disponíveis</span><span class="sxs-lookup"><span data-stu-id="22561-114">See other available actions</span></span>  

<span data-ttu-id="22561-115">Se você usar o fluxo de trabalho descrito em [abrir o menu de comando](#open-the-command-menu), o menu de comandos será aberto com um `>` caractere semipendente na caixa de texto do menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="22561-115">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Usar o menu de comandos para desativar o JavaScript" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="22561-117">O caractere de comando</span><span class="sxs-lookup"><span data-stu-id="22561-117">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="22561-118">Exclua o `>` caractere e digite `?` para ver outras ações que estão disponíveis no menu de comando.</span><span class="sxs-lookup"><span data-stu-id="22561-118">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Usar o menu de comandos para desativar o JavaScript" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="22561-120">Outras ações disponíveis</span><span class="sxs-lookup"><span data-stu-id="22561-120">Other available actions</span></span>  
:::image-end:::  

## <span data-ttu-id="22561-121">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="22561-121">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Desabilitar JavaScript com o Microsoft Edge DevTools | Documentos da Microsoft"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Paleta de comandos-UI de código do Visual Studio"  

> [!NOTE]
> <span data-ttu-id="22561-124">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="22561-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="22561-125">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="22561-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="22561-127">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="22561-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
