---
title: Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 39a7967a7dd1d0b34eb802d2879e04a64afd0dd0
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982230"
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





# <span data-ttu-id="43595-103">Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas</span><span class="sxs-lookup"><span data-stu-id="43595-103">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="43595-104">Se você mesmo digitar a mesma expressão de JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="43595-104">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="43595-105">Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.</span><span class="sxs-lookup"><span data-stu-id="43595-105">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="43595-106">O valor da expressão é atualizado em tempo real quase em tempo real.</span><span class="sxs-lookup"><span data-stu-id="43595-106">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="43595-107">Criar uma expressão ao vivo</span><span class="sxs-lookup"><span data-stu-id="43595-107">Create a Live Expression</span></span>   

1.  <span data-ttu-id="43595-108">[Abra o console][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="43595-108">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="43595-109">Clique em **criar expressão ao vivo** \ ( ![ criar expressão ao vivo ][ImageCreateLiveExpressionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="43595-109">Click **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="43595-110">A caixa de texto **expressão ao vivo** é exibida.</span><span class="sxs-lookup"><span data-stu-id="43595-110">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Digitando documento. ActiveElement na caixa de texto expressão dinâmica" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="43595-112">Digitando `document.activeElement` na caixa de texto **expressão dinâmica**</span><span class="sxs-lookup"><span data-stu-id="43595-112">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="43595-113">Digite `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para salvar a expressão ou clique fora da caixa de texto **expressão ao vivo** .</span><span class="sxs-lookup"><span data-stu-id="43595-113">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Abrir o console-referência do console | Documentos da Microsoft"  

> [!NOTE]
> <span data-ttu-id="43595-115">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="43595-115">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="43595-116">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="43595-116">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="43595-118">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="43595-118">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
