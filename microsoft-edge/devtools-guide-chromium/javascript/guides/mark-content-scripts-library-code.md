---
title: Marcar scripts de conteúdo como código de biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: fe34d8f2fb656283b1821441162b93d47d51d24e
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581786"
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





# <span data-ttu-id="deda2-103">Marcar scripts de conteúdo como código de biblioteca</span><span class="sxs-lookup"><span data-stu-id="deda2-103">Mark Content Scripts as Library Code</span></span>   



<span data-ttu-id="deda2-104">Ao usar o painel **fontes** do Microsoft Edge devtools para percorrer o [código][DevToolsJavascriptStepThroughCode], às vezes, você pode pausar o código que não reconhece.</span><span class="sxs-lookup"><span data-stu-id="deda2-104">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="deda2-105">Você provavelmente pausou no código de uma das extensões do Microsoft Edge instaladas.</span><span class="sxs-lookup"><span data-stu-id="deda2-105">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="deda2-106">Conclua as etapas a seguir para não pausar no código de extensão.</span><span class="sxs-lookup"><span data-stu-id="deda2-106">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="deda2-107">Abra o DevTools, selecione **Personalizar e controle devtools** `...` e clique em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="deda2-107">Open DevTools, select **Customize and control DevTools** `...` and click **Settings**.</span></span>  <span data-ttu-id="deda2-108">Você também pode abrir **as configurações** pressionando `F1` .</span><span class="sxs-lookup"><span data-stu-id="deda2-108">You may also open **Settings** by pressing `F1`.</span></span>  

1.  <span data-ttu-id="deda2-109">Selecione a guia **código de biblioteca** que abre a seção de código da biblioteca de **estrutura** de **configurações**.</span><span class="sxs-lookup"><span data-stu-id="deda2-109">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="deda2-110">Habilite a caixa de seleção **Marcar scripts de conteúdo como código de biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="deda2-110">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="deda2-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="deda2-111">Figure 1</span></span>  
    > <span data-ttu-id="deda2-112">Habilitar a caixa de seleção **Marcar scripts de conteúdo como código de biblioteca**</span><span class="sxs-lookup"><span data-stu-id="deda2-112">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    > ![Habilitar a caixa de seleção Marcar scripts de conteúdo como código de biblioteca][ImageMarkContentScriptsLibraryCode]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMarkContentScriptsLibraryCode]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png "Figura 1: habilitar a caixa de seleção Marcar scripts de conteúdo como código de biblioteca"  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Etapa 4: percorrer o código-introdução à depuração JavaScript no Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="deda2-116">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="deda2-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="deda2-117">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="deda2-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="deda2-119">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="deda2-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
