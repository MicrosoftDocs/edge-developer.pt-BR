---
description: Use a ferramenta Problemas para identificar e corrigir problemas com a página da Web atual.
title: Encontrar e corrigir problemas usando a ferramenta Problemas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 86277c509aa4b67635661ba3a316fb5b1e3b9d14
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624679"
---
<!-- Copyright Sam Dutton

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-and-fix-problems-using-the-issues-tool"></a><span data-ttu-id="c52e3-104">Encontrar e corrigir problemas usando a ferramenta Problemas</span><span class="sxs-lookup"><span data-stu-id="c52e3-104">Find and fix problems using the Issues tool</span></span>

<span data-ttu-id="c52e3-105">No Microsoft Edge DevTools, a ferramenta **Issues** analisa automaticamente a página da Web atual, relata problemas agrupados por tipo e fornece documentação para ajudar a explicar e resolver os problemas.</span><span class="sxs-lookup"><span data-stu-id="c52e3-105">In Microsoft Edge DevTools, the **Issues** tool automatically analyzes the current webpage, reports issues grouped by type, and provides documentation to help explain and resolve the issues.</span></span>

<span data-ttu-id="c52e3-106">A **ferramenta Issues** fornece comentários nas seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="c52e3-106">The **Issues** tool provides feedback in the following categories:</span></span>
*  <span data-ttu-id="c52e3-107">Acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="c52e3-107">Accessibility.</span></span>
*  <span data-ttu-id="c52e3-108">Compatibilidade entre navegadores.</span><span class="sxs-lookup"><span data-stu-id="c52e3-108">Compatibility across browsers.</span></span>
*  <span data-ttu-id="c52e3-109">Desempenho.</span><span class="sxs-lookup"><span data-stu-id="c52e3-109">Performance.</span></span>
*  <span data-ttu-id="c52e3-110">Aplicativos Web Progressivos.</span><span class="sxs-lookup"><span data-stu-id="c52e3-110">Progressive Web Apps.</span></span>
*  <span data-ttu-id="c52e3-111">Segurança.</span><span class="sxs-lookup"><span data-stu-id="c52e3-111">Security.</span></span>
*  <span data-ttu-id="c52e3-112">Outro.</span><span class="sxs-lookup"><span data-stu-id="c52e3-112">Other.</span></span>

<span data-ttu-id="c52e3-113">Os comentários na ferramenta **Issues** são fornecidos por várias fontes, incluindo a plataforma Chromium, o eixo Deque, os dados de compatibilidade do navegador MDN e o webhint.</span><span class="sxs-lookup"><span data-stu-id="c52e3-113">Feedback in the **Issues** tool is provided by several sources, including the Chromium platform, Deque axe, MDN browser compatibility data, and webhint.</span></span>  <span data-ttu-id="c52e3-114">Para obter informações sobre essas fontes de comentários que preenchem a **ferramenta Problemas,** navegue até:</span><span class="sxs-lookup"><span data-stu-id="c52e3-114">For information about these sources of feedback that populate the **Issues** tool, navigate to:</span></span>
*  [<span data-ttu-id="c52e3-115">visão geral das ferramentas de eixo</span><span class="sxs-lookup"><span data-stu-id="c52e3-115">axe Tools Overview</span></span>][DequeAxe]
*  [<span data-ttu-id="c52e3-116">browser-compat-data repo</span><span class="sxs-lookup"><span data-stu-id="c52e3-116">browser-compat-data repo</span></span>][MDNCompat]
*  [<span data-ttu-id="c52e3-117">Dica da web</span><span class="sxs-lookup"><span data-stu-id="c52e3-117">webhint</span></span>][webhintIo]


## <a name="open-the-issues-tool"></a><span data-ttu-id="c52e3-118">Abra a ferramenta Problemas</span><span class="sxs-lookup"><span data-stu-id="c52e3-118">Open the Issues tool</span></span>

<span data-ttu-id="c52e3-119">Execute as etapas a seguir para abrir a **ferramenta Problemas** usando uma página de demonstração.</span><span class="sxs-lookup"><span data-stu-id="c52e3-119">Perform the following steps to open the **Issues** tool using a demo page.</span></span>


1.  <span data-ttu-id="c52e3-120">Navegue até uma página da Web que contém problemas para corrigir.</span><span class="sxs-lookup"><span data-stu-id="c52e3-120">Navigate to a webpage that contains issues to fix.</span></span>  <span data-ttu-id="c52e3-121">Por exemplo, abra a [página de demonstração de][A11ytestingPagewitherrors] teste de acessibilidade em uma nova guia ou janela.</span><span class="sxs-lookup"><span data-stu-id="c52e3-121">For example, open the [accessibility-testing demo page][A11ytestingPagewitherrors] in a new tab or window.</span></span>

1.  <span data-ttu-id="c52e3-122">Abra DevTools.</span><span class="sxs-lookup"><span data-stu-id="c52e3-122">Open DevTools.</span></span>  <span data-ttu-id="c52e3-123">Após alguns segundos, o contador **Problemas** \( Contador de problemas ![ \) é exibido, no canto superior direito do ](../media/issues-counter-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="c52e3-123">After a few seconds, the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) appears, in the upper right corner of DevTools.</span></span>  <span data-ttu-id="c52e3-124">O número de problemas no contador Problemas pode ser diferente.</span><span class="sxs-lookup"><span data-stu-id="c52e3-124">The number of issues in your Issues counter might be different.</span></span>

1.  <span data-ttu-id="c52e3-125">Selecione o contador **Problemas**.</span><span class="sxs-lookup"><span data-stu-id="c52e3-125">Select the **Issues counter**.</span></span>  <span data-ttu-id="c52e3-126">A **ferramenta Issues** é aberta com problemas agrupados em categorias diferentes.</span><span class="sxs-lookup"><span data-stu-id="c52e3-126">The **Issues** tool opens with issues grouped into different categories.</span></span>

    :::image type="complex" source="../media/issues-tool-categories.msft.png" alt-text="Categorias de problemas na ferramenta Problemas na página de demonstração" lightbox="../media/issues-tool-categories.msft.png":::
       <span data-ttu-id="c52e3-128">Categorias de problemas na ferramenta Problemas na página de demonstração</span><span class="sxs-lookup"><span data-stu-id="c52e3-128">Categories of issues in the Issues tool on the demo page</span></span>
    :::image-end:::

### <a name="other-ways-to-open-the-issues-tool"></a><span data-ttu-id="c52e3-129">Outras maneiras de abrir a ferramenta Problemas</span><span class="sxs-lookup"><span data-stu-id="c52e3-129">Other ways to open the Issues tool</span></span>

<span data-ttu-id="c52e3-130">Há várias maneiras adicionais de abrir a **ferramenta Problemas:**</span><span class="sxs-lookup"><span data-stu-id="c52e3-130">There are several additional ways to open the **Issues** tool:</span></span>
*  <span data-ttu-id="c52e3-131">Selecione o **menu Mais Ferramentas** ( ) no painel principal ou na **+** **Gaveta**e selecione **Problemas**.</span><span class="sxs-lookup"><span data-stu-id="c52e3-131">Select the **More Tools** (**+**) menu in the main panel or the **Drawer**, and then select **Issues**.</span></span>
*  <span data-ttu-id="c52e3-132">Selecione **Personalizar e controlar DevTools**Mais problemas  >  **de**  >  **ferramentas.**</span><span class="sxs-lookup"><span data-stu-id="c52e3-132">Select **Customize and control DevTools** > **More tools** > **Issues**.</span></span>
*  <span data-ttu-id="c52e3-133">Na árvore DOM na ferramenta **Elementos,** selecione e clique em um nome `Shift` de elemento sublinhado ondulado.</span><span class="sxs-lookup"><span data-stu-id="c52e3-133">In the DOM tree in the **Elements** tool, select `Shift` and then click a wavy-underlined element name.</span></span>  <span data-ttu-id="c52e3-134">Ou abra o menu de contexto em um elemento sublinhado ondulado e selecione **Exibir problemas**.</span><span class="sxs-lookup"><span data-stu-id="c52e3-134">Or, open the context menu on a wavy-underlined element and then select **View issues**.</span></span>

### <a name="issues-are-automatically-ordered-by-severity"></a><span data-ttu-id="c52e3-135">Os problemas são ordenados automaticamente por gravidade</span><span class="sxs-lookup"><span data-stu-id="c52e3-135">Issues are automatically ordered by severity</span></span>

<span data-ttu-id="c52e3-136">Em cada categoria de problemas, primeiro os erros são listados, depois avisos e dicas.</span><span class="sxs-lookup"><span data-stu-id="c52e3-136">Within each category of issues, first the errors are listed, then warnings, and then tips.</span></span>

:::image type="complex" source="../media/issues-ordered-by-severity.msft.png" alt-text="A ferramenta Issues exibe problemas de desempenho classificação por gravidade" lightbox="../media/issues-ordered-by-severity.msft.png":::
   <span data-ttu-id="c52e3-138">A **ferramenta Issues** exibe problemas de desempenho classificação por gravidade</span><span class="sxs-lookup"><span data-stu-id="c52e3-138">The **Issues** tool displays Performance issues sorted by severity</span></span>
:::image-end:::

### <a name="include-third-party-issues"></a><span data-ttu-id="c52e3-139">Incluir problemas de terceiros</span><span class="sxs-lookup"><span data-stu-id="c52e3-139">Include third-party issues</span></span>

<span data-ttu-id="c52e3-140">Para incluir problemas causados por sites de terceiros, na parte superior da ferramenta **Problemas,** selecione a caixa de seleção Incluir **problemas** de terceiros.</span><span class="sxs-lookup"><span data-stu-id="c52e3-140">To include issues that are caused by third-party sites, at the top of the **Issues** tool, select the **Include third-party issues** checkbox.</span></span>


## <a name="expand-entries-in-the-issues-tool"></a><span data-ttu-id="c52e3-141">Expandir entradas na ferramenta Problemas</span><span class="sxs-lookup"><span data-stu-id="c52e3-141">Expand entries in the Issues tool</span></span>

<span data-ttu-id="c52e3-142">A **ferramenta Issues** apresenta documentação adicional e correções recomendadas para aplicar a cada problema.</span><span class="sxs-lookup"><span data-stu-id="c52e3-142">The **Issues** tool presents additional documentation and recommended fixes to apply to each issue.</span></span>  <span data-ttu-id="c52e3-143">Para expandir um problema para obter essas informações adicionais, selecione um problema, da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="c52e3-143">To expand an issue to get this additional information, select an issue, as follows.</span></span>

1.  <span data-ttu-id="c52e3-144">Abra a [página de demonstração][A11ytestingPagewitherrors] em uma nova janela ou guia e abra DevTools.</span><span class="sxs-lookup"><span data-stu-id="c52e3-144">Open the [demo page][A11ytestingPagewitherrors] in a new window or tab, and then open DevTools.</span></span>

1.  <span data-ttu-id="c52e3-145">Abra a **ferramenta Problemas** selecionando o contador **Problemas** \( Contador de ![ problemas ](../media/issues-counter-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="c52e3-145">Open the **Issues** tool by selecting the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\).</span></span>

1.  <span data-ttu-id="c52e3-146">Selecione um problema para expandir o problema.</span><span class="sxs-lookup"><span data-stu-id="c52e3-146">Select an issue to expand the issue.</span></span>

    :::image type="complex" source="../media/issues-tool-initial-view-accessibility-page.msft.png" alt-text="A ferramenta Issues que exibe informações adicionais sobre como corrigir o problema" lightbox="../media/issues-tool-initial-view-accessibility-page.msft.png":::
       <span data-ttu-id="c52e3-148">A **ferramenta Issues** que exibe informações adicionais sobre como corrigir o problema</span><span class="sxs-lookup"><span data-stu-id="c52e3-148">The **Issues** tool displaying additional information on how to fix the issue</span></span>
    :::image-end:::

<span data-ttu-id="c52e3-149">Cada problema exibido tem os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="c52e3-149">Each displayed issue has the following components:</span></span>
*   <span data-ttu-id="c52e3-150">Uma título que descreve o problema.</span><span class="sxs-lookup"><span data-stu-id="c52e3-150">A headline describing the issue.</span></span>
*   <span data-ttu-id="c52e3-151">Uma descrição que fornece mais contexto e soluções propostas.</span><span class="sxs-lookup"><span data-stu-id="c52e3-151">A description providing more context and proposed solutions.</span></span>
*   <span data-ttu-id="c52e3-152">Uma **seção RECURSOS AFETADOs** que se vincula a recursos no DevTools, como **a ferramenta Elementos,** **Fontes** **ou** Rede.</span><span class="sxs-lookup"><span data-stu-id="c52e3-152">An **AFFECTED RESOURCES** section that links to resources in DevTools, such as the **Elements**, **Sources**, or **Network** tool.</span></span>
*   <span data-ttu-id="c52e3-153">Links para documentação posterior.</span><span class="sxs-lookup"><span data-stu-id="c52e3-153">Links to further documentation.</span></span>


## <a name="view-issues-in-context-of-an-associated-tool"></a><span data-ttu-id="c52e3-154">Exibir problemas no contexto de uma ferramenta associada</span><span class="sxs-lookup"><span data-stu-id="c52e3-154">View issues in context of an associated tool</span></span>

<span data-ttu-id="c52e3-155">Um problema na ferramenta **Problemas** pode incluir um ou mais links que abrem ferramentas diferentes, como **a ferramenta Elementos,** **Fontes** **ou** Rede.</span><span class="sxs-lookup"><span data-stu-id="c52e3-155">An issue in the **Issues** tool may include one or more links that open different tools, such as the **Elements**, **Sources**, or **Network** tool.</span></span> <span data-ttu-id="c52e3-156">Você pode abrir uma dessas ferramentas para executar etapas adicionais de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="c52e3-156">You can open one of these tools to perform additional troubleshooting steps.</span></span> <span data-ttu-id="c52e3-157">Para abrir uma ferramenta vinculada da **ferramenta Problemas,** execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c52e3-157">To open a linked tool from the **Issues** tool, perform the following steps.</span></span>

1.  <span data-ttu-id="c52e3-158">Conforme descrito na seção anterior, abra a página de demonstração e expanda um problema na **ferramenta Problemas.**</span><span class="sxs-lookup"><span data-stu-id="c52e3-158">As described in the previous section, open the demo page and then expand an issue in the **Issues** tool.</span></span>

1.  <span data-ttu-id="c52e3-159">Em **RECURSOS**  >  **AFETADOs Abra**em , selecione o nome da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="c52e3-159">In **AFFECTED RESOURCES** > **Open in**, select the tool name.</span></span>  <span data-ttu-id="c52e3-160">O recurso afetado é exibido na ferramenta selecionada.</span><span class="sxs-lookup"><span data-stu-id="c52e3-160">The affected resource is displayed in the selected tool.</span></span>

    :::image type="complex" source="../media/issues-tool-affected-resource-opens-elements-tool.msft.png" alt-text="Selecione uma ferramenta para abrir um recurso afetado de dentro da ferramenta Issues" lightbox="../media/issues-tool-affected-resource-opens-elements-tool.msft.png":::
       <span data-ttu-id="c52e3-162">Selecione uma ferramenta para abrir um recurso afetado de dentro da ferramenta Issues</span><span class="sxs-lookup"><span data-stu-id="c52e3-162">Select a tool to open an affected resource from within the Issues tool</span></span>
    :::image-end:::

    <span data-ttu-id="c52e3-163">Um problema expandido pode ter um link **Rede** para exibir o recurso afetado na **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="c52e3-163">An expanded issue may have a **Network** link, to display the affected resource in the **Network** tool.</span></span>

    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="A ferramenta Rede é aberta quando você seleciona um link de recurso rede" lightbox="../media/issues-tab-view-issue.msft.png":::
    <span data-ttu-id="c52e3-165">A **ferramenta Rede** é aberta quando você seleciona um link de **recurso** rede</span><span class="sxs-lookup"><span data-stu-id="c52e3-165">The **Network** tool opens when you select a **Network** resource link</span></span>
    :::image-end:::


## <a name="open-issues-from-the-dom-tree"></a><span data-ttu-id="c52e3-166">Abrir problemas da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="c52e3-166">Open issues from the DOM tree</span></span>

<span data-ttu-id="c52e3-167">Se um elemento tiver um problema associado, a árvore DOM na ferramenta **Elements** mostrará um sublinhado ondulado sob o nome do elemento.</span><span class="sxs-lookup"><span data-stu-id="c52e3-167">If an element has an associated issue, the DOM tree in the **Elements** tool shows a wavy underline under the element name.</span></span>  <span data-ttu-id="c52e3-168">Você pode abrir o menu de contexto (clique com o botão direito do mouse) no elemento e selecione **Exibir**problemas ou selecione e clique com o botão esquerdo no elemento com o `Shift` sublinhado ondulado.</span><span class="sxs-lookup"><span data-stu-id="c52e3-168">You can open the context menu (right-click) on the element and then select **View issues**, or select `Shift` and left-click the element with the wavy underline.</span></span>

<span data-ttu-id="c52e3-169">Para exibir um problema para elementos com sublinhados ondulados na árvore DOM, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c52e3-169">To display an issue for elements with wavy underlines in the DOM tree, perform the following steps.</span></span>

1.  <span data-ttu-id="c52e3-170">Abra uma página, como a página [de demonstração][A11ytestingPagewitherrors], em uma nova guia ou janela.</span><span class="sxs-lookup"><span data-stu-id="c52e3-170">Open a page, such as the [demo page][A11ytestingPagewitherrors], in a new tab or window.</span></span>

1.  <span data-ttu-id="c52e3-171">Abra DevTools e selecione a **guia Elementos.**</span><span class="sxs-lookup"><span data-stu-id="c52e3-171">Open DevTools and then select the **Elements** tab.</span></span>

1.  <span data-ttu-id="c52e3-172">Na árvore DOM, expanda `<body>`  >  `<header>`  >  `<form>` .</span><span class="sxs-lookup"><span data-stu-id="c52e3-172">In the DOM tree, expand `<body>` > `<header>` > `<form>`.</span></span>  <span data-ttu-id="c52e3-173">Observe que o `<input>` elemento tem um sublinhado ondulado.</span><span class="sxs-lookup"><span data-stu-id="c52e3-173">Notice that the `<input>` element has a wavy underline.</span></span>

    :::image type="complex" source="../media/issues-wavy-underlines-dom-tree.msft.png" alt-text="Problemas sublinhados ondulados na árvore DOM na ferramenta Elements" lightbox="../media/issues-wavy-underlines-dom-tree.msft.png":::
       <span data-ttu-id="c52e3-175">Problemas sublinhados ondulados na árvore **DOM** na **ferramenta Elements**</span><span class="sxs-lookup"><span data-stu-id="c52e3-175">Wavy-underlined issues in the **DOM tree** in the **Elements** tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="c52e3-176">Passe o mouse sobre o `<input>` elemento.</span><span class="sxs-lookup"><span data-stu-id="c52e3-176">Hover over the `<input>` element.</span></span>  <span data-ttu-id="c52e3-177">Uma dica de ferramenta exibe informações sobre o problema.</span><span class="sxs-lookup"><span data-stu-id="c52e3-177">A tooltip displays information about the issue.</span></span>

1.  <span data-ttu-id="c52e3-178">Abra o menu de contexto no elemento com o sublinhado ondulado e selecione **Exibir problemas**.</span><span class="sxs-lookup"><span data-stu-id="c52e3-178">Open the context menu on the element with the wavy underline, and then select **View issues**.</span></span>  <span data-ttu-id="c52e3-179">A **ferramenta Issues** abre e exibe o problema associado a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="c52e3-179">The **Issues** tool opens and displays the issue that's associated with that element.</span></span>

    :::image type="complex" source="../media/issues-opened-from-dom-tree-wavy-underline.msft.png" alt-text="Detalhes sobre problemas em um elemento sublinhado ondulado na árvore DOM" lightbox="../media/issues-opened-from-dom-tree-wavy-underline.msft.png":::
       <span data-ttu-id="c52e3-181">Detalhes sobre problemas em um elemento sublinhado **ondulado** na árvore DOM</span><span class="sxs-lookup"><span data-stu-id="c52e3-181">Details about issues on a wavy-underlined element in the **DOM tree**</span></span>
    :::image-end:::


## <a name="see-also"></a><span data-ttu-id="c52e3-182">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c52e3-182">See also</span></span>

* [<span data-ttu-id="c52e3-183">Teste automaticamente uma página da Web em busca de problemas de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="c52e3-183">Automatically test a webpage for accessibility issues</span></span>](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c52e3-184">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c52e3-184">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

<!-- links -->
[DevtoolsOpenIndex]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"
<!-- external links -->
[A11ytestingPagewitherrors]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página de demonstração de teste de acessibilidade | Microsoft Docs"
[DequeAxe]: https://www.deque.com/axe "axe Tools Overview | Deque"
[MDNCompat]: https://github.com/mdn/browser-compat-data "Dados de Compatibilidade do Navegador MDN | GitHub"
[webhintIo]: https://webhint.io "webhint.io"

> [!NOTE]
> <span data-ttu-id="c52e3-190">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c52e3-190">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>
> <span data-ttu-id="c52e3-191">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/issues/index) e é de autoria de [Sam Dutton][SamDutton] \(Developer Advocate\).</span><span class="sxs-lookup"><span data-stu-id="c52e3-191">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>
<span data-ttu-id="c52e3-192">[ ![ Licença do Creative Commons Este][CCby4Image]][CCA4IL] trabalho é licenciado sob uma Licença Internacional de [Atribuição do Creative Commons 4.0.][CCA4IL]</span><span class="sxs-lookup"><span data-stu-id="c52e3-192">[![Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton
