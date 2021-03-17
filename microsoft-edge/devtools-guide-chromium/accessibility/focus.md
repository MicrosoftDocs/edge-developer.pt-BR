---
description: Abra o Console, crie uma Expressão Ativa e dejuste a expressão como document.activeElement.
title: Acompanhar qual elemento tem o foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2c2040c690441fb33c802cf454dc7a1e3f33c494
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439167"
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

# <a name="track-which-element-has-focus"></a><span data-ttu-id="aaf5e-104">Acompanhar qual elemento tem o foco</span><span class="sxs-lookup"><span data-stu-id="aaf5e-104">Track which element has focus</span></span>  

<span data-ttu-id="aaf5e-105">Suponha que você está testando a acessibilidade de navegação do teclado de uma página.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-105">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="aaf5e-106">Ao navegar pela página com a chave, o anel de foco às vezes desaparece porque o elemento que `Tab` tem foco está oculto.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-106">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="aaf5e-107">Conclua as seguintes ações para rastrear o elemento focado no DevTools.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-107">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="aaf5e-108">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-108">Open the **Console**.</span></span>  
1.  <span data-ttu-id="aaf5e-109">Escolha **Criar Expressão Ao Vivo** \( Criar Expressão Ao Vivo ![ ](../media/create-live-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="aaf5e-109">Choose **Create Live Expression** \(![Create Live Expression](../media/create-live-expression-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Criar uma expressão ao vivo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="aaf5e-111">Criar uma expressão ao vivo</span><span class="sxs-lookup"><span data-stu-id="aaf5e-111">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aaf5e-112">Digite `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-112">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="aaf5e-113">Escolha fora da **interface do usuário expressão ao** vivo para salvar.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-113">Choose outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="aaf5e-114">O valor exibido abaixo `document.activeElement` é o resultado da expressão.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-114">The value displayed below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="aaf5e-115">Como essa expressão sempre representa o elemento focado, agora você tem uma maneira de sempre acompanhar qual elemento tem foco.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="aaf5e-116">Passe o mouse no resultado para realçar o elemento focado no viewport.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-116">Hover on the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="aaf5e-117">Passe o mouse no resultado, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Revelar** em Elementos painel para mostrar o elemento na Árvore DOM na **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="aaf5e-117">Hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** tool.</span></span>  
*   <span data-ttu-id="aaf5e-118">Passe o mouse no resultado, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Store como **variável global** para criar uma referência variável ao nó que você pode usar no **Console**.</span><span class="sxs-lookup"><span data-stu-id="aaf5e-118">Hover on the result, open the contextual menu \(right-click\), and choose **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="aaf5e-119">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aaf5e-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="aaf5e-120">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aaf5e-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aaf5e-121">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="aaf5e-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="aaf5e-123">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aaf5e-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
