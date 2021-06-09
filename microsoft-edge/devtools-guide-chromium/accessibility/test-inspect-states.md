---
description: Inspecione a acessibilidade de todos os estados de elementos, como o contraste de texto durante o estado de foco, no painel Estilos usando o estado do elemento Toggle.
title: Verificar a acessibilidade de todos os estados de elementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 129a89f94925de24a4e649bd91f513de031d6b4a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597200"
---
# <a name="verify-accessibility-of-all-states-of-elements"></a><span data-ttu-id="71ff9-104">Verifique a acessibilidade de todos os estados dos elementos</span><span class="sxs-lookup"><span data-stu-id="71ff9-104">Verify accessibility of all states of elements</span></span>

<!-- 5. STYLES: TOGGLE STATE -->

<span data-ttu-id="71ff9-105">Verifique a acessibilidade de todos os estados de elementos, como contraste de cor de texto durante o `hover` estado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-105">Check the accessibility of all states of elements, such as text color contrast during the `hover` state.</span></span>  <span data-ttu-id="71ff9-106">A **ferramenta Inspecionar** relata problemas de acessibilidade para um estado de cada vez.</span><span class="sxs-lookup"><span data-stu-id="71ff9-106">The **Inspect** tool reports accessibility issues for one state at a time.</span></span>  <span data-ttu-id="71ff9-107">Para verificar a acessibilidade dos vários estados de elementos, na guia **Estilos,** selecione **\:hov** ( Estado do Elemento**Toggle**), conforme descrito neste artigo.</span><span class="sxs-lookup"><span data-stu-id="71ff9-107">To check accessibility of the various states of elements, in the **Styles** tab, select **\:hov** (**Toggle Element State**), as described in this article.</span></span> <span data-ttu-id="71ff9-108">Primeiro mostramos por que a simulação de estado é necessária usando a ferramenta **Inspecionar** e, em seguida, mostramos como usar a simulação de estado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-108">We first show why state simulation is necessary using the **Inspect** tool, and then we show how to use state simulation.</span></span>


## <a name="checking-text-color-contrast-in-the-default-state"></a><span data-ttu-id="71ff9-109">Verificando o contraste de cor do texto no estado padrão</span><span class="sxs-lookup"><span data-stu-id="71ff9-109">Checking text color contrast in the default state</span></span>

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

<span data-ttu-id="71ff9-110">Além dos testes automáticos de contraste de cor na ferramenta **Problemas,** você também pode usar a ferramenta **Inspecionar** para verificar se elementos de página individuais têm contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="71ff9-110">In addition to the automatic color-contrast tests in the **Issues** tool, you can also use the **Inspect** tool to check whether individual page elements have enough contrast.</span></span>  <span data-ttu-id="71ff9-111">Se as informações de contraste estão disponíveis, a sobreposição **Inspecionar** mostra a taxa de contraste e um item de caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="71ff9-111">If contrast information is available, the **Inspect** overlay shows the contrast ratio and a checkbox item.</span></span>  <span data-ttu-id="71ff9-112">Um ícone de marca de verificação verde indica que há contraste suficiente e um ícone de alerta amarelo indica que não há contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="71ff9-112">A green check mark icon indicates there's enough contrast, and a yellow alert icon indicates that there's not enough contrast.</span></span>

<span data-ttu-id="71ff9-113">Por exemplo, os links no menu de navegação da barra lateral têm contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="71ff9-113">For example, the links in the sidebar navigation menu have enough contrast.</span></span>  <span data-ttu-id="71ff9-114">Mas o item de lista **de** Cachorros verdes na seção **Status** da Doação não tem contraste suficiente e, portanto, é sinalizado por um aviso na sobreposição **Inspecionar.**</span><span class="sxs-lookup"><span data-stu-id="71ff9-114">But the green **Dogs** list item in the **Donation status** section doesn't have enough contrast, and so is flagged by a warning in the **Inspect** overlay.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Os links no menu de navegação da barra lateral têm contraste suficiente, conforme mostrado na sobreposição Inspecionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            <span data-ttu-id="71ff9-116">Os links no menu de navegação da barra lateral têm contraste suficiente, conforme mostrado na sobreposição **Inspecionar**</span><span class="sxs-lookup"><span data-stu-id="71ff9-116">The links in the sidebar navigation menu have enough contrast, as shown in the **Inspect** overlay</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Um elemento que não tem contraste suficiente é sinalizado por um aviso na sobreposição Inspecionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            <span data-ttu-id="71ff9-118">Um elemento que não tem contraste suficiente é sinalizado por um aviso na sobreposição **Inspecionar**</span><span class="sxs-lookup"><span data-stu-id="71ff9-118">An element that doesn't have enough contrast is flagged by a warning in the **Inspect** overlay</span></span> :::image-end:::
    :::column-end:::
:::row-end:::
        

## <a name="hovering-when-the-inspect-tool-is-active-doesnt-show-the-text-color-contrast-for-the-hover-state"></a><span data-ttu-id="71ff9-119">O foco quando a ferramenta Inspect está ativa não mostra o contraste de cor de texto para o estado de foco</span><span class="sxs-lookup"><span data-stu-id="71ff9-119">Hovering when the Inspect tool is active doesn't show the text-color contrast for the hover state</span></span>

<span data-ttu-id="71ff9-120">A **sobreposição** de informações da ferramenta Inspect representa apenas um único estado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-120">The **Inspect** tool's information overlay only represents a single state.</span></span>  <span data-ttu-id="71ff9-121">Os elementos na página podem ter estados diferentes, todos eles precisam ser testados.</span><span class="sxs-lookup"><span data-stu-id="71ff9-121">Elements on the page can have different states, all of which need to be tested.</span></span>  <span data-ttu-id="71ff9-122">Por exemplo, quando você passar o ponteiro do mouse sobre o menu da página de demonstração de teste de acessibilidade, você obterá uma animação que altera as cores.</span><span class="sxs-lookup"><span data-stu-id="71ff9-122">For example, when you hover the mouse pointer over the menu of the accessibility-testing demo page, you get an animation that changes the colors.</span></span> <span data-ttu-id="71ff9-123">Execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="71ff9-123">Perform the following steps.</span></span>

1.  <span data-ttu-id="71ff9-124">Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="71ff9-124">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.</span></span>

1.  <span data-ttu-id="71ff9-125">Passe o mouse sobre os itens de menu azul no menu de navegação da barra lateral.</span><span class="sxs-lookup"><span data-stu-id="71ff9-125">Hover over the blue menu items in the sidebar navigation menu.</span></span>  <span data-ttu-id="71ff9-126">Observe que cada item tem uma animação.</span><span class="sxs-lookup"><span data-stu-id="71ff9-126">Notice that each item has an animation.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="O item de menu mostrando cores diferentes quando o ponteiro do mouse está sobre ele" lightbox="../media/a11y-testing-hover.msft.png":::
        <span data-ttu-id="71ff9-128">O item de menu mostrando cores diferentes quando o ponteiro do mouse está sobre ele</span><span class="sxs-lookup"><span data-stu-id="71ff9-128">The menu item showing different colors when the mouse pointer is over it</span></span>
    :::image-end:::
    
<span data-ttu-id="71ff9-129">Agora, use a ferramenta Inspecionar.</span><span class="sxs-lookup"><span data-stu-id="71ff9-129">Now, use the Inspect tool.</span></span> <span data-ttu-id="71ff9-130">Quando a ferramenta Inspect é usada, as animações nos itens de menu não são executados quando você passar o mouse sobre eles.</span><span class="sxs-lookup"><span data-stu-id="71ff9-130">When the Inspect tool is used, animations on the menu items won't run when you hover over them.</span></span>  <span data-ttu-id="71ff9-131">Ao usar a ferramenta Inspecionar, você não pode alcançar o estado nos itens de menu para testar a taxa de contraste, pois o estado em seus estilos não `hover` `hover` é disparado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-131">When using the Inspect tool, you can't reach the `hover` state on menu items to test the contrast ratio, because the `hover` state in your styles isn't triggered.</span></span>  
    
<span data-ttu-id="71ff9-132">Para confirmar se suas animações não são executados, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="71ff9-132">To confirm that your animations don't run, perform the following steps.</span></span>
    
1.  <span data-ttu-id="71ff9-133">Selecione o **botão Inspecionar** \( o botão Inspecionar \) no canto superior esquerdo do DevTools para que o ícone seja ![ realçado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="71ff9-133">Select the **Inspect** \(![the Inspect button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="71ff9-134">Passe o mouse sobre os links azuis no menu de navegação da barra lateral.</span><span class="sxs-lookup"><span data-stu-id="71ff9-134">Hover over the blue links on the sidebar navigation menu.</span></span>  <span data-ttu-id="71ff9-135">As animações dos itens de menu não são executados.</span><span class="sxs-lookup"><span data-stu-id="71ff9-135">The animations for the menu items don't run.</span></span> <span data-ttu-id="71ff9-136">Em vez disso, os itens de menu são exibidos usando cores e realçadores para a sobreposição da caixa de flexão.</span><span class="sxs-lookup"><span data-stu-id="71ff9-136">Instead, the menu items are displayed using colors and highlights for the flexbox overlay.</span></span>

<span data-ttu-id="71ff9-137">Verificar o contraste de texto suficiente dessa forma não é suficiente, pois os elementos na página podem ter estados diferentes.</span><span class="sxs-lookup"><span data-stu-id="71ff9-137">Checking for sufficient text contrast this way isn't enough, because the elements on the page could have different states.</span></span>


## <a name="use-state-simulation-to-simulate-the-hover-state-of-an-animated-menu-item"></a><span data-ttu-id="71ff9-138">Usar a simulação de estado para simular o estado de foco de um item de menu animado</span><span class="sxs-lookup"><span data-stu-id="71ff9-138">Use state simulation to simulate the hover state of an animated menu item</span></span> 

<!-- Elements tool: Styles pane: Toggle Element State -->

<span data-ttu-id="71ff9-139">Quando a **ferramenta Inspect** estiver ativa, em vez de passar o mouse sobre um elemento animado, você precisará simular o estado do item de menu.</span><span class="sxs-lookup"><span data-stu-id="71ff9-139">When the **Inspect** tool is active, instead of hovering over an animated element, you need to simulate the state of the menu item.</span></span>  <span data-ttu-id="71ff9-140">Para simular o estado de um item de menu, use a simulação de estado no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="71ff9-140">To simulate the state of a menu item, use the state simulation in the **Styles** pane.</span></span>  <span data-ttu-id="71ff9-141">O **painel Estilos** tem um botão **\:hov** ( Estado do Elemento**Toggle**), que exibe um grupo de caixas de seleção rotuladas estado do elemento **Force**.</span><span class="sxs-lookup"><span data-stu-id="71ff9-141">The **Styles** pane has a **\:hov** (**Toggle Element State**) button, which displays a group of checkboxes labeled **Force element state**.</span></span>

<span data-ttu-id="71ff9-142">Para ativar o estado de foco ao usar a ferramenta Inspecionar:</span><span class="sxs-lookup"><span data-stu-id="71ff9-142">To turn on the hover state while using the Inspect tool:</span></span>

1.  <span data-ttu-id="71ff9-143">Se ainda não estiver aberto, abra a página da [Web][DevToolsA11yErrorsDemopage] de demonstração de teste de acessibilidade em uma nova guia.  Em seguida, **selecione F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="71ff9-143">If it's not open already, open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="71ff9-144">Selecione o **botão Inspecionar** \( Inspecionar botão da ferramenta \) no canto superior esquerdo do DevTools para que o ícone seja ![ realçado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="71ff9-144">Select the **Inspect** \(![Inspect tool button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="71ff9-145">Na página da Web renderizada, selecione o link **azul Gatos** no menu de navegação da barra lateral.</span><span class="sxs-lookup"><span data-stu-id="71ff9-145">In the rendered webpage, select the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="71ff9-146">A **ferramenta Elements** é aberta, com o elemento `<a href="#cats">Cats</a>` selecionado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-146">The **Elements** tool opens, with the element `<a href="#cats">Cats</a>` selected.</span></span>

    :::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspecionar o elemento que tem um estado de foco na ferramenta Elements" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
        <span data-ttu-id="71ff9-148">Inspecionar o elemento que tem um estado de foco na ferramenta Elements</span><span class="sxs-lookup"><span data-stu-id="71ff9-148">Inspecting the element that has a hover state in the Elements tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="71ff9-149">Selecione a **guia Estilos.**  O elemento selecionado tem um estado no CSS que é aplicado a ele, mas que não `a` está visível no painel `hover` **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="71ff9-149">Select the **Styles** tab.  The selected `a` element has a `hover` state in the CSS that is applied to it, but that's not visible in the **Styles** pane.</span></span> 

1.  <span data-ttu-id="71ff9-150">No painel **Estilos,** à direita da regra de `#sidebar nav li a` estilo, selecione o `styles.css` link.</span><span class="sxs-lookup"><span data-stu-id="71ff9-150">In the **Styles** pane, to the right of the style rule `#sidebar nav li a`, select the `styles.css` link.</span></span>  <span data-ttu-id="71ff9-151">A **ferramenta Sources** é aberta.</span><span class="sxs-lookup"><span data-stu-id="71ff9-151">The **Sources** tool opens.</span></span>  <span data-ttu-id="71ff9-152">Em seguida, encontre a regra de pseudo-classe CSS `#sidebar nav li a:hover` .</span><span class="sxs-lookup"><span data-stu-id="71ff9-152">Then find the CSS pseudo-class rule `#sidebar nav li a:hover`.</span></span>  <span data-ttu-id="71ff9-153">Essa regra não é executado quando a **ferramenta Inspect** está ativa.</span><span class="sxs-lookup"><span data-stu-id="71ff9-153">This rule doesn't run when the **Inspect** tool is active.</span></span>  <span data-ttu-id="71ff9-154">Vamos simular a execução dessa regra de estado nas próximas etapas.</span><span class="sxs-lookup"><span data-stu-id="71ff9-154">We'll simulate running this state rule in the next steps.</span></span>

1.  <span data-ttu-id="71ff9-155">Selecione a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="71ff9-155">Select the **Elements** tool.</span></span>  <span data-ttu-id="71ff9-156">Em seguida, no painel **Estilos,** selecione o **botão :hov** (**Estado do Elemento De alternância**).</span><span class="sxs-lookup"><span data-stu-id="71ff9-156">Then in the **Styles** pane, select the **:hov** (**Toggle Element State**) button.</span></span>  <span data-ttu-id="71ff9-157">O **grupo de estado do** elemento Force das caixas de seleção é exibido.</span><span class="sxs-lookup"><span data-stu-id="71ff9-157">The **Force element state** group of checkboxes is displayed.</span></span>

    :::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="A ferramenta de simulação de estado mostrando todas as opções" lightbox="../media/a11y-testing-state-simulation.msft.png":::
        <span data-ttu-id="71ff9-159">A ferramenta de simulação de estado mostrando todas as opções</span><span class="sxs-lookup"><span data-stu-id="71ff9-159">The state simulation tool showing all the options</span></span>
    :::image-end:::

1.  <span data-ttu-id="71ff9-160">Selecione a **caixa de seleção :hover.**</span><span class="sxs-lookup"><span data-stu-id="71ff9-160">Select the **:hover** checkbox.</span></span>  <span data-ttu-id="71ff9-161">No DOM, à esquerda do elemento , aparece um ponto amarelo, indicando que o `<a href="#cats">Cats</a>` elemento tem um estado simulado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-161">In the DOM, to the left of the element `<a href="#cats">Cats</a>`, a yellow dot appears, indicating that the element has a simulated state.</span></span>  <span data-ttu-id="71ff9-162">O \*\*\*\* item de menu Gatos agora aparece na página da Web como se o ponteiro estivesse pairando sobre ele.</span><span class="sxs-lookup"><span data-stu-id="71ff9-162">The **Cats** menu item now appears in the webpage as if the pointer were hovering over it.</span></span>  <span data-ttu-id="71ff9-163">A animação no item de menu pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-163">The animation on the menu item might run.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulando um estado de foco" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
        <span data-ttu-id="71ff9-165">DevTools simulando um estado de foco</span><span class="sxs-lookup"><span data-stu-id="71ff9-165">DevTools simulating a hover state</span></span>
    :::image-end:::

    <span data-ttu-id="71ff9-166">Depois que o estado simulado for aplicado, você poderá usar a ferramenta **Inspecionar** novamente para verificar o contraste do elemento quando o usuário passar o mouse sobre ele, da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="71ff9-166">After the simulated state is applied, you can use the **Inspect** tool again to check the contrast of the element when the user hovers over it, as follows.</span></span>

1.  <span data-ttu-id="71ff9-167">Selecione o **botão Inspecionar** \( Ícone do Inspetor \) no canto superior esquerdo do DevTools para que o ícone seja ![ realçado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="71ff9-167">Select the **Inspect** \(![Inspector icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="71ff9-168">Passe o mouse sobre o link **gatos** azuis no menu de navegação da barra lateral.</span><span class="sxs-lookup"><span data-stu-id="71ff9-168">Hover over the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="71ff9-169">O link agora está azul claro, devido à animação de foco simulado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-169">The link is now light blue, because of the simulated hover animation.</span></span>  <span data-ttu-id="71ff9-170">A **sobreposição** de informações da ferramenta Inspect é exibida, mostrando um ponto de exclamação laranja na linha **Contraste,** indicando que o contraste não é alto o suficiente.</span><span class="sxs-lookup"><span data-stu-id="71ff9-170">The **Inspect** tool's information overlay appears, showing an orange exclamation point in the **Contrast** row, indicating that the contrast isn't high enough.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Testar o contraste de um elemento em um estado de foco simulado" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
        <span data-ttu-id="71ff9-172">Testar o contraste de um elemento em um estado de foco simulado</span><span class="sxs-lookup"><span data-stu-id="71ff9-172">Testing the contrast of an element in a simulated hover state</span></span>
    :::image-end:::

<span data-ttu-id="71ff9-173">A simulação de estado também é uma boa maneira de verificar se você considera diferentes necessidades do usuário, como as necessidades dos usuários de teclado.</span><span class="sxs-lookup"><span data-stu-id="71ff9-173">State simulation is also a good way to check whether you considered different user needs, such as the needs of keyboard users.</span></span>  <span data-ttu-id="71ff9-174">Usando as caixas de seleção estado do elemento **Force,** você pode simular o estado para descobrir que a interface do usuário permanece inalterada `:focus` quando ela tem foco.</span><span class="sxs-lookup"><span data-stu-id="71ff9-174">By using the **Force element state** checkboxes, you can simulate the `:focus` state to discover that the UI remains unchanged when it has focus.</span></span> <span data-ttu-id="71ff9-175">Essa falta de um indicador quando um elemento tem foco é um problema.</span><span class="sxs-lookup"><span data-stu-id="71ff9-175">This lack of an indicator when an element has focus is a problem.</span></span>


## <a name="see-also"></a><span data-ttu-id="71ff9-176">Consulte também</span><span class="sxs-lookup"><span data-stu-id="71ff9-176">See also</span></span>

*  [<span data-ttu-id="71ff9-177">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="71ff9-177">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="71ff9-178">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="71ff9-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
