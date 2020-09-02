---
title: Acompanhar Qual Elemento Tem o Foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5261824b725384240453f216071255494e88e98d
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991173"
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

# <span data-ttu-id="02952-103">Acompanhar Qual Elemento Tem o Foco</span><span class="sxs-lookup"><span data-stu-id="02952-103">Track Which Element Has Focus</span></span>  

<span data-ttu-id="02952-104">Suponha que você esteja testando o acesso à navegação pelo teclado de uma página.</span><span class="sxs-lookup"><span data-stu-id="02952-104">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="02952-105">Ao navegar a página com a `Tab` chave, o anel de foco às vezes desaparece porque o elemento que tem o foco está oculto.</span><span class="sxs-lookup"><span data-stu-id="02952-105">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="02952-106">Conclua as ações a seguir para acompanhar o elemento focalizado no DevTools.</span><span class="sxs-lookup"><span data-stu-id="02952-106">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="02952-107">Abra o **console**.</span><span class="sxs-lookup"><span data-stu-id="02952-107">Open the **Console**.</span></span>  
1.  <span data-ttu-id="02952-108">Clique em **criar expressão ao vivo** \ ( ![ criar expressão ao vivo ][ImageCreateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="02952-108">Click **Create Live Expression** \(![Create Live Expression][ImageCreateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Criar uma expressão ao vivo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="02952-110">Criar uma expressão ao vivo</span><span class="sxs-lookup"><span data-stu-id="02952-110">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="02952-111">Digite `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="02952-111">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="02952-112">Clique fora da interface de usuário do **Live Expression** para salvar.</span><span class="sxs-lookup"><span data-stu-id="02952-112">Click outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="02952-113">O valor que você vê abaixo `document.activeElement` é o resultado da expressão.</span><span class="sxs-lookup"><span data-stu-id="02952-113">The value that you see below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="02952-114">Como essa expressão sempre representa o elemento destaques, agora você tem uma maneira de sempre manter o controle de qual elemento está focalizado.</span><span class="sxs-lookup"><span data-stu-id="02952-114">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="02952-115">Passe o mouse sobre o resultado para realçar o elemento focalizado no visor.</span><span class="sxs-lookup"><span data-stu-id="02952-115">Hover over the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="02952-116">Clique com o botão direito do mouse no resultado e selecione **revelar no painel de elementos** para mostrar o elemento na árvore DOM do painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="02952-116">Right-click the result and select **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** panel.</span></span>  
*   <span data-ttu-id="02952-117">Clique com o botão direito do mouse no resultado e selecione **armazenar como variável global** para criar uma referência de variável para o nó que você pode usar no **console**.</span><span class="sxs-lookup"><span data-stu-id="02952-117">Right-click the result and select **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <span data-ttu-id="02952-118">Entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="02952-118">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="02952-119">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="02952-119">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="02952-120">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="02952-120">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="02952-122">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="02952-122">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
