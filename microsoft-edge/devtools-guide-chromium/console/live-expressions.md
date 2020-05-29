---
title: Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: c388e44ca5507dd88ad9ad7b7ee985e658dfc569
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601737"
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





# <span data-ttu-id="50d74-103">Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas</span><span class="sxs-lookup"><span data-stu-id="50d74-103">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="50d74-104">Se você mesmo digitar a mesma expressão de JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="50d74-104">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="50d74-105">Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.</span><span class="sxs-lookup"><span data-stu-id="50d74-105">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="50d74-106">O valor da expressão é atualizado em tempo real quase em tempo real.</span><span class="sxs-lookup"><span data-stu-id="50d74-106">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="50d74-107">Criar uma expressão ao vivo</span><span class="sxs-lookup"><span data-stu-id="50d74-107">Create a Live Expression</span></span>   

1.  <span data-ttu-id="50d74-108">[Abra o console][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="50d74-108">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="50d74-109">Clique em **criar** expressão ao vivo ![ criar uma expressão ao vivo ][ImageCreateLiveExpressionIcon] .</span><span class="sxs-lookup"><span data-stu-id="50d74-109">Click **Create Live Expression** ![Create Live Expression][ImageCreateLiveExpressionIcon].</span></span>  <span data-ttu-id="50d74-110">A caixa de texto **expressão ao vivo** é exibida.</span><span class="sxs-lookup"><span data-stu-id="50d74-110">The **Live Expression** text box appears.</span></span>  
    
    > ##### <span data-ttu-id="50d74-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="50d74-111">Figure 1</span></span>  
    > <span data-ttu-id="50d74-112">Digitando `document.activeElement` na caixa de texto **expressão dinâmica**</span><span class="sxs-lookup"><span data-stu-id="50d74-112">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    > ![Digitando documento. ActiveElement na caixa de texto expressão dinâmica][ImageLiveExpressionTextbox]  
    
1.  <span data-ttu-id="50d74-114">Digite `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para salvar a expressão ou clique fora da caixa de texto **expressão ao vivo** .</span><span class="sxs-lookup"><span data-stu-id="50d74-114">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/create-live-expression-icon.msft.png  

[ImageLiveExpressionTextbox]: /microsoft-edge/devtools-guide-chromium/media/console-create-live-expression.msft.png "Figura 1: digitando documento. ActiveElement na caixa de texto expressão dinâmica"  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console "Abrir o console-referência do console"  

> [!NOTE]
> <span data-ttu-id="50d74-117">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="50d74-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="50d74-118">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="50d74-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="50d74-120">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50d74-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
