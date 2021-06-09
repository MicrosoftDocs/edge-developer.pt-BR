---
description: Teste automaticamente uma página da Web para problemas de acessibilidade usando a seção Acessibilidade da ferramenta Problemas.
title: Teste automaticamente uma página da Web em busca de problemas de acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 986a021d2fd390cd45bd53dcfc37a83d58ed2338
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597172"
---
# <a name="automatically-test-a-webpage-for-accessibility-issues"></a><span data-ttu-id="7e91b-104">Teste automaticamente uma página da Web em busca de problemas de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="7e91b-104">Automatically test a webpage for accessibility issues</span></span>

<span data-ttu-id="7e91b-105">A **ferramenta Issues** inclui uma seção **Acessibilidade** que relata automaticamente problemas como falta de texto alternativo em imagens, rótulos ausentes em campos de formulário e contraste insuficiente de cores de texto.</span><span class="sxs-lookup"><span data-stu-id="7e91b-105">The **Issues** tool includes an **Accessibility** section that automatically reports issues such as missing alternative text on images, missing labels on form fields, and insufficient contrast of text colors.</span></span>  <span data-ttu-id="7e91b-106">A **ferramenta Issues** está dentro da **Gaveta** na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-106">The **Issues** tool is within the **Drawer** at the bottom of DevTools.</span></span>  <span data-ttu-id="7e91b-107">Este artigo usa a página da Web de demonstração de teste de acessibilidade para passar por meio do uso da seção **Acessibilidade** da **ferramenta Issues.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-107">This article uses the accessibility-testing demo webpage to step through using the **Accessibility** section of the **Issues** tool.</span></span>

<span data-ttu-id="7e91b-108">Há várias maneiras de abrir a **ferramenta Problemas,** como:</span><span class="sxs-lookup"><span data-stu-id="7e91b-108">There are several ways to open the **Issues** tool, such as:</span></span>
*  <span data-ttu-id="7e91b-109">Selecione o **contador Problemas** \( Contador de problemas ![ ](../media/issues-counter-icon.msft.png) \) no canto superior direito do DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-109">Select the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) in the upper right of DevTools.</span></span>
*  <span data-ttu-id="7e91b-110">Na ferramenta **Elementos,** na árvore DOM, **Shift+clique em** um sublinhado ondulado em um elemento.</span><span class="sxs-lookup"><span data-stu-id="7e91b-110">In the **Elements** tool, in the DOM tree, **Shift+click** a wavy underline on an element.</span></span>
*  <span data-ttu-id="7e91b-111">No **Menu Comando ,** digite `issues` e selecione Mostrar **Problemas**.</span><span class="sxs-lookup"><span data-stu-id="7e91b-111">In the **Command Menu**, type `issues`, and then select **Show Issues**.</span></span>


## <a name="view-the-accessibility-section-of-the-issues-tool"></a><span data-ttu-id="7e91b-112">Exibir a seção Acessibilidade da ferramenta Problemas</span><span class="sxs-lookup"><span data-stu-id="7e91b-112">View the Accessibility section of the Issues tool</span></span>

1.  <span data-ttu-id="7e91b-113">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-113">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>  <span data-ttu-id="7e91b-114">No canto superior direito, o contador **Problemas** \( Contador de problemas \) é exibido, como um ícone de bolha de fala juntamente com o número de problemas ![ ](../media/issues-counter-icon.msft.png) detectados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7e91b-114">In the upper right, the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) appears, as a speech-bubble icon along with the number of automatically detected issues.</span></span>  <span data-ttu-id="7e91b-115">Um número diferente pode aparecer no navegador, e o número pode ser atualizado à medida que você usa o DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-115">A different number might appear in your browser, and the number might update as you use DevTools.</span></span>

    :::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="O contador Problemas no DevTools, indicando quantos problemas há no documento atual" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
        <span data-ttu-id="7e91b-117">O **contador Problemas** no DevTools, indicando quantos problemas há no documento atual</span><span class="sxs-lookup"><span data-stu-id="7e91b-117">The **Issues counter** in DevTools, indicating how many problems there are in the current document</span></span>
    :::image-end:::

1.  <span data-ttu-id="7e91b-118">Selecione o contador **Problemas**.</span><span class="sxs-lookup"><span data-stu-id="7e91b-118">Select the **Issues counter**.</span></span>  <span data-ttu-id="7e91b-119">A **ferramenta Issues** é aberta, na **Gaveta** na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-119">The **Issues** tool opens, in the **Drawer** at the bottom of DevTools.</span></span>

    :::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Avisos de acessibilidade exibidos na ferramenta Problemas" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
        <span data-ttu-id="7e91b-121">Avisos de acessibilidade exibidos na ferramenta Problemas</span><span class="sxs-lookup"><span data-stu-id="7e91b-121">Accessibility warnings displayed in the Issues tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="7e91b-122">Na guia **Problemas,** expanda **a seção Acessibilidade.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-122">On the **Issues** tab, expand the **Accessibility** section.</span></span>


## <a name="verify-that-input-fields-have-labels"></a><span data-ttu-id="7e91b-123">Verificar se os campos de entrada têm rótulos</span><span class="sxs-lookup"><span data-stu-id="7e91b-123">Verify that input fields have labels</span></span>

<span data-ttu-id="7e91b-124">Para verificar se os campos de entrada têm rótulos conectados a eles, use a ferramenta **Problemas,** que verifica automaticamente toda a página da Web e relata esse problema na **seção** Acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="7e91b-124">To check whether input fields have labels connected to them, use the **Issues** tool, which automatically checks the entire webpage and reports this issue in the **Accessibility** section.</span></span>

1.  <span data-ttu-id="7e91b-125">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-125">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="7e91b-126">No canto superior direito, selecione o contador **Problemas** \( ![ Contador de problemas ](../media/issues-counter-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="7e91b-126">In the upper right, select the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\).</span></span>  <span data-ttu-id="7e91b-127">A **ferramenta Issues** é aberta, na **Gaveta** na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-127">The **Issues** tool opens, in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="7e91b-128">Na guia **Problemas,** expanda **a seção Acessibilidade.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-128">On the **Issues** tab, expand the **Accessibility** section.</span></span>

1.  <span data-ttu-id="7e91b-129">Expanda **o Aviso** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute` .</span><span class="sxs-lookup"><span data-stu-id="7e91b-129">Expand the **Warning** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute`.</span></span>

1. <span data-ttu-id="7e91b-130">Selecione o link **Abrir em Elementos.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-130">Select the **Open in Elements** link.</span></span>

    :::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Ferramenta Elements mostrando o HTML problemático após selecionar o link na ferramenta Problemas" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
        <span data-ttu-id="7e91b-132">Ferramenta Elements mostrando o HTML problemático após selecionar o link na ferramenta **Problemas**</span><span class="sxs-lookup"><span data-stu-id="7e91b-132">Elements tool showing the problematic HTML after selecting the link in the **Issues** tool</span></span> :::image-end:::

    <span data-ttu-id="7e91b-133">A **ferramenta Elements** é aberta, com o elemento realçado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="7e91b-133">The **Elements** tool opens, with the element highlighted in the DOM tree.</span></span>  <span data-ttu-id="7e91b-134">O **painel Estilos** exibe as regras CSS aplicadas para o elemento.</span><span class="sxs-lookup"><span data-stu-id="7e91b-134">The **Styles** pane displays the applied CSS rules for the element.</span></span>  <span data-ttu-id="7e91b-135">O código a seguir agora é exibido.</span><span class="sxs-lookup"><span data-stu-id="7e91b-135">The following code is now displayed.</span></span>

    ```html
    <label>Search</label>
    <input type="search">
    <input type="submit" value="go">
    ```

    <span data-ttu-id="7e91b-136">No código acima, o elemento é usado incorretamente, porque não há nenhuma conexão entre `label` o elemento e um elemento `label` `input` específico.</span><span class="sxs-lookup"><span data-stu-id="7e91b-136">In the above code, the `label` element is used incorrectly, because there is no connection between the `label` element and a particular `input` element.</span></span>  <span data-ttu-id="7e91b-137">Para conectar o `label` elemento a um elemento `input` específico, use qualquer uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7e91b-137">To connect the `label` element to a specific `input` element, use any of the following options.</span></span>
    *   <span data-ttu-id="7e91b-138">Aninhar `input` o elemento dentro do `label` elemento.</span><span class="sxs-lookup"><span data-stu-id="7e91b-138">Nest the `input` element within the `label` element.</span></span>
    *   <span data-ttu-id="7e91b-139">No `label` elemento, adicione um `for` atributo que corresponde a um atributo do `id` `input` elemento.</span><span class="sxs-lookup"><span data-stu-id="7e91b-139">In the `label` element, add a `for` attribute that matches an `id` attribute of the `input` element.</span></span>

    <span data-ttu-id="7e91b-140">Também há outra maneira de testar a falta de conexões entre os elementos.</span><span class="sxs-lookup"><span data-stu-id="7e91b-140">There's also another way to test for lack of connections between elements.</span></span> <span data-ttu-id="7e91b-141">Na ferramenta **Elementos,** selecione `<label>Search</label>` o elemento na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="7e91b-141">In the **Elements** tool, select the `<label>Search</label>` element in the DOM tree.</span></span>  <span data-ttu-id="7e91b-142">Na página da Web, observe que o foco só aparece no rótulo **de** Pesquisa e não na caixa de texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e91b-142">On the webpage, notice that focus only appears on the **Search** label, and not the input textbox.</span></span>  <span data-ttu-id="7e91b-143">A implementação correta colocaria o foco na caixa de texto de `search` entrada e no rótulo **de** Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7e91b-143">The correct implementation would put focus on the `search` input textbox and the **Search** label.</span></span>

1.  <span data-ttu-id="7e91b-144">Como exemplo de uma conexão correta, selecione **o rótulo Outro** no formulário de doação.</span><span class="sxs-lookup"><span data-stu-id="7e91b-144">As an example of a correct connection, select the **Other** label on the donation form.</span></span>  <span data-ttu-id="7e91b-145">Uma caixa de indicador de foco aparece corretamente na caixa de texto de entrada ao lado do **outro** rótulo, porque há valores de correspondência e `for` `id` atributo.</span><span class="sxs-lookup"><span data-stu-id="7e91b-145">A focus-indicator box correctly appears on the input textbox next to the **Other** label, because there are matching `for` and `id` attribute values.</span></span>

1.  <span data-ttu-id="7e91b-146">Na ferramenta **Problemas,** selecione **Mais leitura** para saber mais sobre o problema.</span><span class="sxs-lookup"><span data-stu-id="7e91b-146">In the **Issues tool**, select **Further reading** to learn more about the issue.</span></span>  <span data-ttu-id="7e91b-147">Para abrir o link em uma nova guia, **Ctrl**clique no link em Windows/Linux ou Comando clique no + \*\*\*\* link \*\*\*\* + \*\*\*\* no macOS.</span><span class="sxs-lookup"><span data-stu-id="7e91b-147">To open the link in a new tab, **Ctrl**+**click** the link on Windows/Linux, or **Command**+**click** the link on macOS.</span></span>

    :::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Link na guia Problemas apontando para informações mais detalhadas sobre o problema" lightbox="../media/a11y-testing-more-information-links.msft.png":::
        <span data-ttu-id="7e91b-149">Link na guia **Problemas** apontando para informações mais detalhadas sobre o problema</span><span class="sxs-lookup"><span data-stu-id="7e91b-149">Link on the **Issues** tab pointing to more in-depth information about the issue</span></span>
    :::image-end:::


## <a name="verify-that-images-have-alt-text"></a><span data-ttu-id="7e91b-150">Verificar se as imagens têm texto alt</span><span class="sxs-lookup"><span data-stu-id="7e91b-150">Verify that images have alt text</span></span>

<span data-ttu-id="7e91b-151">Os testes básicos de acessibilidade exigem que o texto alternativo (também chamado _de texto alt)_ seja fornecido para imagens.</span><span class="sxs-lookup"><span data-stu-id="7e91b-151">Basic accessibility testing requires making sure alternative text (also called _alt text_) is provided for images.</span></span>

<span data-ttu-id="7e91b-152">Para verificar automaticamente se o texto alt é fornecido para imagens, use a **ferramenta Issues,** que tem uma **seção Accessibility.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-152">To automatically check whether alt text is provided for images, use the **Issues** tool, which has an **Accessibility** section.</span></span>  <span data-ttu-id="7e91b-153">A **ferramenta Issues** está localizada na **Gaveta** na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-153">The **Issues** tool is located in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="7e91b-154">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-154">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="7e91b-155">Para abrir a **ferramenta Problemas,** selecione o contador **Problemas** no canto superior direito do DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-155">To open the **Issues** tool, select the **Issues** counter in the upper right of DevTools.</span></span>

1.  <span data-ttu-id="7e91b-156">Na guia **Problemas,** expanda o aviso `Images must have alternate text: Element has no title attribute` .</span><span class="sxs-lookup"><span data-stu-id="7e91b-156">On the **Issues** tab, expand the warning `Images must have alternate text: Element has no title attribute`.</span></span>  <span data-ttu-id="7e91b-157">Há quatro instâncias de imagens que não têm texto alt.</span><span class="sxs-lookup"><span data-stu-id="7e91b-157">There are four instances of images that lack alt text.</span></span>

    :::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="A ferramenta Issues relata imagens que estão faltando texto alternativo" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
        <span data-ttu-id="7e91b-159">A ferramenta Issues relata imagens que estão faltando texto alternativo</span><span class="sxs-lookup"><span data-stu-id="7e91b-159">The Issues tool reporting images that are missing alternative text</span></span>
    :::image-end:::

<span data-ttu-id="7e91b-160">Para obter mais informações, navegue [até Imagens deve ter texto alternativo](https://dequeuniversity.com/rules/axe/4.1/image-alt).</span><span class="sxs-lookup"><span data-stu-id="7e91b-160">For more information, navigate to [Images must have alternate text](https://dequeuniversity.com/rules/axe/4.1/image-alt).</span></span>


## <a name="verify-that-text-colors-have-enough-contrast"></a><span data-ttu-id="7e91b-161">Verificar se as cores de texto têm contraste suficiente</span><span class="sxs-lookup"><span data-stu-id="7e91b-161">Verify that text colors have enough contrast</span></span>

<span data-ttu-id="7e91b-162">Para verificar automaticamente se as cores de texto têm contraste suficiente, use a ferramenta **Issues,** que tem uma **seção Accessibility.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-162">To automatically check whether text colors have enough contrast, use the **Issues** tool, which has an **Accessibility** section.</span></span>  <span data-ttu-id="7e91b-163">A **ferramenta Issues** está localizada na **Gaveta** na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-163">The **Issues** tool is located in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="7e91b-164">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-164">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="7e91b-165">Para abrir a **ferramenta Problemas,** selecione o contador **Problemas** no canto superior direito do DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e91b-165">To open the **Issues** tool, select the **Issues** counter in the upper right of DevTools.</span></span>  <span data-ttu-id="7e91b-166">Você pode receber avisos de que dois elementos na página da Web de demonstração não têm contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="7e91b-166">You may receive warnings that two elements on the demo webpage don't have enough contrast.</span></span>

    :::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problemas de contraste relatados na ferramenta Problemas" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
        <span data-ttu-id="7e91b-168">Problemas de contraste relatados na ferramenta Problemas</span><span class="sxs-lookup"><span data-stu-id="7e91b-168">Contrast problems reported in the Issues tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="7e91b-169">Dependendo das configurações, a guia **Problemas** pode ter um aviso, como Os usuários podem ter dificuldades para ler conteúdo de texto devido ao contraste de **cor insuficiente.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-169">Depending on your settings, the **Issues** tab might have a warning like **Users may have difficulties reading text content due to insufficient color contrast**.</span></span>   <span data-ttu-id="7e91b-170">Você pode expandir esse aviso e, em seguida, expandir **recursos afetados.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-170">You can expand that warning, and then expand **Affected resources**.</span></span>  <span data-ttu-id="7e91b-171">Uma lista de elementos aparece com uma lista de elementos que não têm contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="7e91b-171">A list of elements appears with a list of elements that don't have enough contrast.</span></span>


1.  <span data-ttu-id="7e91b-172">Selecione o `li.high` elemento.</span><span class="sxs-lookup"><span data-stu-id="7e91b-172">Select the `li.high` element.</span></span>  <span data-ttu-id="7e91b-173">Na página da Web renderizada, o link **Cachorros** na seção **Doar** é realçado, exibindo uma pequena sobreposição de informações.</span><span class="sxs-lookup"><span data-stu-id="7e91b-173">In the rendered webpage, the **Dogs** link in the **Donate** section is highlighted, displaying a small information overlay.</span></span>  <span data-ttu-id="7e91b-174">Essa é a mesma sobreposição que aparece quando você passar o mouse sobre um elemento na árvore DOM na **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-174">This is the same overlay that appears when you hover over an element in the DOM tree in the **Elements** tool.</span></span>

    :::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Elemento na página da Web realçada após selecionar um link na seção Recursos Afetados" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
        <span data-ttu-id="7e91b-176">Elemento na página da Web realçada após selecionar um link na seção **Recursos Afetados**</span><span class="sxs-lookup"><span data-stu-id="7e91b-176">Element in the webpage highlighted after selecting a link in the **Affected Resources** section</span></span>
    :::image-end:::


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a><span data-ttu-id="7e91b-177">Sublinhados ondulados na árvore DOM indicam problemas detectados automaticamente</span><span class="sxs-lookup"><span data-stu-id="7e91b-177">Wavy underlines in the DOM tree indicate automatically detected issues</span></span> 

<span data-ttu-id="7e91b-178">A árvore DOM na ferramenta **Elements** sinaliza problemas diretamente no HTML com sublinhados ondulados.</span><span class="sxs-lookup"><span data-stu-id="7e91b-178">The DOM tree in the **Elements** tool flags issues directly in the HTML with wavy underlines.</span></span>  <span data-ttu-id="7e91b-179">Esses problemas são relatados pela **ferramenta Issues.**</span><span class="sxs-lookup"><span data-stu-id="7e91b-179">These issues are reported by the **Issues** tool.</span></span>  <span data-ttu-id="7e91b-180">Quando você **clica em Shift+clique** em qualquer elemento com um sublinhado ondulado, a **ferramenta Issues** é exibida.</span><span class="sxs-lookup"><span data-stu-id="7e91b-180">When you **Shift+click** any element with a wavy underline, the **Issues tool** is displayed.</span></span>

1.  <span data-ttu-id="7e91b-181">Na ferramenta **Elementos,** na árvore DOM, **Shift+clique** no elemento `<input type="search">` , que tem uma linha ondulada em `input` .</span><span class="sxs-lookup"><span data-stu-id="7e91b-181">In the **Elements** tool, in the DOM tree, **Shift+click** the element `<input type="search">`, which has a wavy line under `input`.</span></span>  <span data-ttu-id="7e91b-182">A **ferramenta Issues** é exibida e mostra o problema desse elemento.</span><span class="sxs-lookup"><span data-stu-id="7e91b-182">The **Issues tool** is displayed, and shows the issue for that element.</span></span>

    :::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Um elemento que tem um sublinhado ondulado no exibição DOM tem um problema" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
        <span data-ttu-id="7e91b-184">Um elemento que tem um sublinhado ondulado no exibição DOM tem um problema</span><span class="sxs-lookup"><span data-stu-id="7e91b-184">An element that has a wavy underline in the DOM view has an issue</span></span>
    :::image-end:::


## <a name="see-also"></a><span data-ttu-id="7e91b-185">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7e91b-185">See also</span></span>

*  [<span data-ttu-id="7e91b-186">Encontre e corrige problemas com a ferramenta Microsoft Edge Problemas do DevTools</span><span class="sxs-lookup"><span data-stu-id="7e91b-186">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>][DevToolsIssuesTool]
*  [<span data-ttu-id="7e91b-187">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="7e91b-187">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7e91b-188">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7e91b-188">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsIssuesTool]: ../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
