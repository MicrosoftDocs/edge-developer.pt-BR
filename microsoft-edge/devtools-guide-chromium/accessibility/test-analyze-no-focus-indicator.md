---
description: Analisando a falta de indicação do foco do teclado em um menu de barra lateral, devido à falta de uma regra de pseudo-classe CSS para o estado de foco em um link, combinado com o link sem configuração de estrutura.
title: Analise a falta de indicação do foco do teclado em um menu de barra lateral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3626de9bdc2cce266efafe4b1b2e8fff501a74f7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597218"
---
# <a name="analyze-the-lack-of-indication-of-keyboard-focus-in-a-sidebar-menu"></a><span data-ttu-id="9e107-104">Analise a falta de indicação do foco do teclado em um menu de barra lateral</span><span class="sxs-lookup"><span data-stu-id="9e107-104">Analyze the lack of indication of keyboard focus in a sidebar menu</span></span>

<!-- Inspect tool, and CSS rules: pseudo-classes for states -->

<span data-ttu-id="9e107-105">Na página de demonstração de teste de acessibilidade, o menu de navegação da barra lateral com links azuis não indica visualmente qual link tem foco ao usar um teclado.</span><span class="sxs-lookup"><span data-stu-id="9e107-105">In the accessibility-testing demo page, the sidebar navigation menu with blue links doesn't visually indicate which link has focus, when using a keyboard.</span></span>  <span data-ttu-id="9e107-106">Para descobrir por que o menu de barra lateral é confuso para os usuários de teclado, procuraremos regras de pseudo-classe CSS para os estados e, juntamente com a propriedade CSS para estruturas de `hover` `focus` links.</span><span class="sxs-lookup"><span data-stu-id="9e107-106">To find out why the sidebar menu is confusing to keyboard users, we'll look for CSS pseudo-class rules for the `hover` and `focus` states, along with the CSS property for link outlines.</span></span>  

<span data-ttu-id="9e107-107">Esta análise descobre que a falta de indicação do foco do teclado nos links do menu de navegação da barra lateral é porque:</span><span class="sxs-lookup"><span data-stu-id="9e107-107">This analysis finds that the lack of indication of keyboard focus in the links of the sidebar navigation menu is because:</span></span>
*  <span data-ttu-id="9e107-108">Os `a` links têm uma configuração de propriedade CSS de `outline: none` .</span><span class="sxs-lookup"><span data-stu-id="9e107-108">The `a` links have a CSS property setting of `outline: none`.</span></span>
*  <span data-ttu-id="9e107-109">Os `a` links não têm uma regra de pseudo-classe CSS para o `:focus` estado.</span><span class="sxs-lookup"><span data-stu-id="9e107-109">The `a` links lack a CSS pseudo-class rule for the `:focus` state.</span></span>

<span data-ttu-id="9e107-110">Para navegar até o CSS, vamos usar a ferramenta **Inspecionar** para realçar um link azul no menu de navegação da barra lateral e, em seguida, exibir a árvore DOM e CSS para o elemento `a` que define esse link.</span><span class="sxs-lookup"><span data-stu-id="9e107-110">To navigate to the CSS, we'll use the **Inspect** tool to highlight a blue link on the sidebar navigation menu, and then view the DOM tree and CSS for the `a` element that defines that link.</span></span>

1.  <span data-ttu-id="9e107-111">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9e107-111">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="9e107-112">Selecione o **botão Inspecionar** \( Inspecionar ícone \) no canto superior esquerdo do DevTools para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).</span><span class="sxs-lookup"><span data-stu-id="9e107-112">Select the **Inspect** \(![Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="9e107-113">Passe o mouse sobre o link **gatos** azuis no menu de navegação da barra lateral.</span><span class="sxs-lookup"><span data-stu-id="9e107-113">Hover over the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="9e107-114">A sobreposição Inspecionar é exibida, mostrando que o elemento é focalizado `a` no teclado.</span><span class="sxs-lookup"><span data-stu-id="9e107-114">The Inspect overlay appears, showing that the `a` element is keyboard-focusable.</span></span>  <span data-ttu-id="9e107-115">Mas a sobreposição não mostra que não há nenhuma indicação visual quando o link tem foco.</span><span class="sxs-lookup"><span data-stu-id="9e107-115">But the overlay doesn't show that there's no visual indication when the link has focus.</span></span>

    <span data-ttu-id="9e107-116">Em seguida, inspecionaremos o estilo CSS deste link.</span><span class="sxs-lookup"><span data-stu-id="9e107-116">Next, we'll inspect the CSS styling of this link.</span></span>
 
1.  <span data-ttu-id="9e107-117">Selecione o link **Gatos** no menu de navegação da barra lateral.</span><span class="sxs-lookup"><span data-stu-id="9e107-117">Select the **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="9e107-118">A **ferramenta Inspecionar** é desligada e a ferramenta **Elements** é aberta, realçando o nó na `a` árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="9e107-118">The **Inspect** tool turns off, and the **Elements** tool opens, highlighting the `a` node in the DOM tree.</span></span>

1.  <span data-ttu-id="9e107-119">Selecione a **guia Estilos.**  A regra CSS `#sidebar nav li a` é exibida, juntamente com um link para um número de linha em `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="9e107-119">Select the **Styles** tab.  The CSS rule `#sidebar nav li a` appears, along with a link to a line number in `styles.css`.</span></span>

    :::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspecionar o código-fonte e os estilos aplicados de um link no menu" lightbox="../media/a11y-testing-menu-link.msft.png":::
        <span data-ttu-id="9e107-121">Inspecionar o código-fonte e os estilos aplicados de um link no menu</span><span class="sxs-lookup"><span data-stu-id="9e107-121">Inspecting the source code and the applied styles of a link in the menu</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="9e107-122">Selecione o link para o arquivo CSS.</span><span class="sxs-lookup"><span data-stu-id="9e107-122">Select the link to the CSS file.</span></span>  <span data-ttu-id="9e107-123">O arquivo CSS é aberto na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="9e107-123">The CSS file opens within the **Sources** tool.</span></span>

    :::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Os estilos aplicados ao link na ferramenta Sources" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
        <span data-ttu-id="9e107-125">Os estilos aplicados ao link na ferramenta Sources</span><span class="sxs-lookup"><span data-stu-id="9e107-125">The styles applied to the link in the Sources tool</span></span>
    :::image-end:::
    
<span data-ttu-id="9e107-126">Os estilos da página têm uma regra de pseudo-classe CSS para o estado que indica qual item de menu você está `hover` ao usar um mouse: `#sidebar nav li a:hover` .</span><span class="sxs-lookup"><span data-stu-id="9e107-126">The styles of the page have a CSS pseudo-class rule for the `hover` state that indicates which menu item you are on when you use a mouse: `#sidebar nav li a:hover`.</span></span>  <span data-ttu-id="9e107-127">No entanto, não há nenhuma regra de pseudo-classe CSS para o estado indicar visualmente qual item de menu você está usando ao usar `focus` um teclado, como `#sidebar nav li a:focus` .</span><span class="sxs-lookup"><span data-stu-id="9e107-127">However, there is no CSS pseudo-class rule for the `focus` state to visually indicate which menu item you are on when you use a keyboard, such as `#sidebar nav li a:focus`.</span></span>

<span data-ttu-id="9e107-128">Além disso, observe que os links têm uma configuração de propriedade CSS de `outline: none` .</span><span class="sxs-lookup"><span data-stu-id="9e107-128">Also, notice that the links have a CSS property setting of `outline: none`.</span></span>  <span data-ttu-id="9e107-129">Essa é uma prática comum, para remover o contorno que os navegadores adicionam automaticamente aos elementos quando você se concentra neles usando um teclado.</span><span class="sxs-lookup"><span data-stu-id="9e107-129">This is a common practice, to remove the outline which browsers automatically add to elements when you focus on them using a keyboard.</span></span>  <span data-ttu-id="9e107-130">Não usar `focus` o estilo causa confusão para os usuários.</span><span class="sxs-lookup"><span data-stu-id="9e107-130">Not using `focus` styling causes confusion for your users.</span></span>


## <a name="see-also"></a><span data-ttu-id="9e107-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9e107-131">See also</span></span> 

*  [<span data-ttu-id="9e107-132">Acompanhar qual elemento tem o foco</span><span class="sxs-lookup"><span data-stu-id="9e107-132">Track which element has focus</span></span>](focus.md)
*  [<span data-ttu-id="9e107-133">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="9e107-133">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9e107-134">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9e107-134">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
