---
title: Acompanhar Qual Elemento Tem o Foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 04091ddf7986b8554e4f615a92e0303446048eaa
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981741"
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





# <span data-ttu-id="4c63d-103">Acompanhar Qual Elemento Tem o Foco</span><span class="sxs-lookup"><span data-stu-id="4c63d-103">Track Which Element Has Focus</span></span>   



<span data-ttu-id="4c63d-104">Suponha que você esteja testando o acesso à navegação pelo teclado de uma página.</span><span class="sxs-lookup"><span data-stu-id="4c63d-104">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="4c63d-105">Ao navegar a página com a `Tab` chave, o anel de foco às vezes desaparece porque o elemento que tem o foco está oculto.</span><span class="sxs-lookup"><span data-stu-id="4c63d-105">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  <span data-ttu-id="4c63d-106">Para acompanhar o elemento focalizado no DevTools:</span><span class="sxs-lookup"><span data-stu-id="4c63d-106">To track the focused element in DevTools:</span></span>  

1.  <span data-ttu-id="4c63d-107">Abra o **console**.</span><span class="sxs-lookup"><span data-stu-id="4c63d-107">Open the **Console**.</span></span>  
1.  <span data-ttu-id="4c63d-108">Clique em **criar expressão ao vivo** \ ( ![ criar expressão ao vivo ][ImageCreateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4c63d-108">Click **Create Live Expression** \(![Create Live Expression][ImageCreateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Criar uma expressão ao vivo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="4c63d-110">Criar uma expressão ao vivo</span><span class="sxs-lookup"><span data-stu-id="4c63d-110">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4c63d-111">Digite `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="4c63d-111">Type `document.activeElement`.</span></span>
1.  <span data-ttu-id="4c63d-112">Clique fora da interface de usuário do **Live Expression** para salvar.</span><span class="sxs-lookup"><span data-stu-id="4c63d-112">Click outside of the **Live Expression** UI to save.</span></span>
    
<span data-ttu-id="4c63d-113">O valor que você vê abaixo `document.activeElement` é o resultado da expressão.</span><span class="sxs-lookup"><span data-stu-id="4c63d-113">The value that you see below `document.activeElement` is the result of the expression.</span></span>  
<span data-ttu-id="4c63d-114">Como essa expressão sempre representa o elemento destaques, agora você tem uma maneira de sempre manter o controle de qual elemento está focalizado.</span><span class="sxs-lookup"><span data-stu-id="4c63d-114">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="4c63d-115">Passe o mouse sobre o resultado para realçar o elemento focalizado no visor.</span><span class="sxs-lookup"><span data-stu-id="4c63d-115">Hover over the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="4c63d-116">Clique com o botão direito do mouse no resultado e selecione **revelar no painel de elementos** para mostrar o elemento na árvore DOM do painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="4c63d-116">Right-click the result and select **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** panel.</span></span>  
*   <span data-ttu-id="4c63d-117">Clique com o botão direito do mouse no resultado e selecione **armazenar como variável global** para criar uma referência de variável para o nó que você pode usar no **console**.</span><span class="sxs-lookup"><span data-stu-id="4c63d-117">Right-click the result and select **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  
    
<!--## Feedback   -->  



<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="4c63d-118">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="4c63d-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4c63d-119">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4c63d-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4c63d-121">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4c63d-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
