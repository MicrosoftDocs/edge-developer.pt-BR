---
description: Verificando a Árvore de Acessibilidade para suporte a teclado e leitor de tela.
title: Verifique o suporte ao leitor de tela e ao teclado na Árvore de Acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0ab5e5609485505d1ad5fa6e2fffced9af25edcb
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597219"
---
# <a name="check-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a><span data-ttu-id="417b3-104">Verifique o suporte ao leitor de tela e ao teclado na Árvore de Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="417b3-104">Check the Accessibility Tree for keyboard and screen reader support</span></span>

<!-- Accessibility tab: Accessibility Tree -->

<span data-ttu-id="417b3-105">Vários recursos do DevTools verificam se há suporte para teclado e leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="417b3-105">Several DevTools features check for keyboard and screen reader support.</span></span>  <span data-ttu-id="417b3-106">Usar a **ferramenta Inspecionar** para verificar a acessibilidade de cada elemento de página individualmente pode se tornar muito demorado.</span><span class="sxs-lookup"><span data-stu-id="417b3-106">Using the **Inspect** tool to check the accessibility of each page element individually can become pretty time-consuming.</span></span>  <span data-ttu-id="417b3-107">Uma maneira alternativa de verificar uma página da Web é usar a **Árvore de Acessibilidade**.</span><span class="sxs-lookup"><span data-stu-id="417b3-107">An alternative way to check a webpage is to use the **Accessibility Tree**.</span></span>  <span data-ttu-id="417b3-108">A **Árvore de Acessibilidade** indica quais informações a página fornece para tecnologias assistivas, como leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="417b3-108">The **Accessibility Tree** indicates what information the page provides to assistive technology such as screen readers.</span></span>

<span data-ttu-id="417b3-109">A **Árvore de** Acessibilidade é um subconjunto da árvore DOM, que contém elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página em um leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="417b3-109">The **Accessibility Tree** is a subset of the DOM tree, which contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  <span data-ttu-id="417b3-110">A **Árvore de Acessibilidade** está na guia **Acessibilidade** da ferramenta **Elements** (perto da **guia Estilos).**</span><span class="sxs-lookup"><span data-stu-id="417b3-110">The **Accessibility Tree** is in the **Accessibility** tab of the **Elements** tool (near the **Styles** tab).</span></span>


<span data-ttu-id="417b3-111">Para explorar usando a Árvore de Acessibilidade com a página de demonstração:</span><span class="sxs-lookup"><span data-stu-id="417b3-111">To explore using the Accessibility Tree with the demo page:</span></span>

1.  <span data-ttu-id="417b3-112">Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia.  Em seguida, **selecione F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="417b3-112">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="417b3-113">Selecione o **botão Inspecionar** \( o botão Inspecionar ícone \) no canto superior esquerdo do DevTools para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).</span><span class="sxs-lookup"><span data-stu-id="417b3-113">Select the **Inspect** \(![the Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="417b3-114">Na página da Web renderizada, na seção **Doação,** passe o mouse sobre o botão **100.**</span><span class="sxs-lookup"><span data-stu-id="417b3-114">In the rendered webpage, in the **Donation** section, hover over the **100** button.</span></span>  <span data-ttu-id="417b3-115">A **sobreposição da** ferramenta Inspect é exibida.</span><span class="sxs-lookup"><span data-stu-id="417b3-115">The **Inspect** tool overlay appears.</span></span>

1.  <span data-ttu-id="417b3-116">Na página da Web renderizada, selecione o botão **100.**</span><span class="sxs-lookup"><span data-stu-id="417b3-116">In the rendered webpage, select the **100** button.</span></span>  <span data-ttu-id="417b3-117">No DevTools, a **ferramenta Elements** é exibida.</span><span class="sxs-lookup"><span data-stu-id="417b3-117">In DevTools, the **Elements** tool is displayed.</span></span>  <span data-ttu-id="417b3-118">A árvore DOM mostra `div` o elemento do botão **100.**</span><span class="sxs-lookup"><span data-stu-id="417b3-118">The DOM tree shows the `div` element for the **100** button.</span></span>  <span data-ttu-id="417b3-119">O **painel Estilos** mostra as configurações CSS do elemento.</span><span class="sxs-lookup"><span data-stu-id="417b3-119">The **Styles** pane shows the CSS settings for the element.</span></span>

1.  <span data-ttu-id="417b3-120">À direita da guia **Estilos,** selecione **a** guia Acessibilidade.  A **Árvore de** Acessibilidade do elemento é exibida e expandida.</span><span class="sxs-lookup"><span data-stu-id="417b3-120">To the right of the **Styles** tab, select the **Accessibility** tab.  The **Accessibility Tree** for the element is displayed, and is expanded.</span></span>

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Botão Formulário de doação na ferramenta Árvore de Acessibilidade" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    <span data-ttu-id="417b3-122">Botão Formulário de doação na ferramenta Árvore de Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="417b3-122">Donation form button in the Accessibility Tree tool</span></span>
:::image-end:::

<span data-ttu-id="417b3-123">Qualquer elemento na árvore que não tenha um nome ou que tenha uma função (como o elemento) é um problema, porque esse elemento não estará disponível para usuários de teclado ou para usuários que estão usando a tecnologia `generic` `div` assistida.</span><span class="sxs-lookup"><span data-stu-id="417b3-123">Any element in the tree that doesn't have a name, or has a role of `generic` (such as the `div` element) is a problem, because that element won't be available to keyboard users, or to users who are using assistive technology.</span></span>


## <a name="see-also"></a><span data-ttu-id="417b3-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="417b3-124">See also</span></span>

*  [<span data-ttu-id="417b3-125">Exibir a posição de um elemento na Árvore de Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="417b3-125">View the position of an element in the Accessibility Tree</span></span>][DevtoolsAccessibilityAccessibilityTabViewTree]
*  [<span data-ttu-id="417b3-126">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="417b3-126">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="417b3-127">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="417b3-127">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityAccessibilityTabViewTree]: accessibility-tab.md#view-the-position-of-an-element-in-the-accessibility-tree "Exibir a posição de um elemento na Árvore de Acessibilidade - Testar acessibilidade usando a guia Acessibilidade | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
