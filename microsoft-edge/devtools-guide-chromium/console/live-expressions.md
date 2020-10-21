---
description: Se você estiver digitando as mesmas expressões JavaScript no console repetidamente, experimente expressões dinâmicas em vez disso.
title: Assista aos valores de expressão JavaScript no Real-Time com expressões ao vivo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f6787455863f738d0fa4e014ca8fc318ad83a9cb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125227"
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

# <span data-ttu-id="6c8a6-104">Assista aos valores de expressão JavaScript no Real-Time com expressões ao vivo</span><span class="sxs-lookup"><span data-stu-id="6c8a6-104">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>  

<span data-ttu-id="6c8a6-105">Se você mesmo digitar a mesma expressão de JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="6c8a6-106">Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="6c8a6-107">O valor da expressão é atualizado em tempo real quase em tempo real.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-107">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="6c8a6-108">Criar uma expressão ao vivo</span><span class="sxs-lookup"><span data-stu-id="6c8a6-108">Create a Live Expression</span></span>  

1.  <span data-ttu-id="6c8a6-109">[Abra o console][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="6c8a6-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="6c8a6-110">Escolha **criar expressão ao vivo** \ ( ![ criar expressão ao vivo ][ImageCreateLiveExpressionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6c8a6-110">Choose **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="6c8a6-111">A caixa de texto **expressão ao vivo** é exibida.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-111">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Digitando documento. ActiveElement na caixa de texto expressão dinâmica" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="6c8a6-113">Digitando `document.activeElement` na caixa de texto **expressão dinâmica**</span><span class="sxs-lookup"><span data-stu-id="6c8a6-113">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6c8a6-114">Selecione `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \) para salvar a expressão ou escolha fora da caixa de texto de **expressão ao vivo** .</span><span class="sxs-lookup"><span data-stu-id="6c8a6-114">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save the expression, or choose outside of the **Live Expression** textbox.</span></span>  

## <span data-ttu-id="6c8a6-115">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6c8a6-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Abrir o console-referência do console | Documentos da Microsoft"  

> [!NOTE]
> <span data-ttu-id="6c8a6-117">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6c8a6-118">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="6c8a6-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6c8a6-120">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6c8a6-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
