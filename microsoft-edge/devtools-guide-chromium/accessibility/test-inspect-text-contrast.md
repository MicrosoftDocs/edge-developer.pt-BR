---
description: Verifique o contraste de cor do texto no estado padrão usando a sobreposição de informações da ferramenta Inspecionar na página, que tem uma seção Acessibilidade que inclui informações de contraste.
title: Verifique o contraste de cor de texto no estado padrão usando a ferramenta Inspecionar
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ade9fd6d685f6f7cea6311b1645a527ece352a38
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597170"
---
# <a name="check-text-color-contrast-in-the-default-state-using-the-inspect-tool"></a><span data-ttu-id="ef3cb-104">Verifique o contraste de cor de texto no estado padrão usando a ferramenta Inspecionar</span><span class="sxs-lookup"><span data-stu-id="ef3cb-104">Check text-color contrast in the default state using the Inspect tool</span></span>

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

<span data-ttu-id="ef3cb-105">Verifique o contraste de cor do texto no estado padrão usando a **ferramenta Inspecionar.**</span><span class="sxs-lookup"><span data-stu-id="ef3cb-105">Check text color contrast in the default state by using the **Inspect** tool.</span></span>  <span data-ttu-id="ef3cb-106">A **sobreposição** de informações da ferramenta Inspect na página da Web tem uma seção **Accessibility** que inclui informações **de contraste.**</span><span class="sxs-lookup"><span data-stu-id="ef3cb-106">The **Inspect** tool's information overlay on the webpage has an **Accessibility** section that includes **Contrast** information.</span></span>

<span data-ttu-id="ef3cb-107">Para verificar o contraste de cor de texto no estado padrão usando a sobreposição de informações da ferramenta Inspect, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-107">To check text-color contrast in the default state using the Inspect tool's information overlay, perform the following steps.</span></span>

<!-- Inspect tool -->
<span data-ttu-id="ef3cb-108">Para elementos com texto, a sobreposição de informações da ferramenta **Inspect** mostra o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ef3cb-108">For elements that have text, the **Inspect** tool's information overlay shows the following:</span></span>
*  <span data-ttu-id="ef3cb-109">A taxa de contraste entre cores de texto e plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-109">The contrast ratio of text versus background colors.</span></span>
*  <span data-ttu-id="ef3cb-110">Um ícone de marca de verificação verde para elementos com contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-110">A green check mark icon for elements with enough contrast.</span></span>
*  <span data-ttu-id="ef3cb-111">Um ícone de alerta amarelo para elementos que não têm contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-111">A yellow alert icon for elements that don't have enough contrast.</span></span>

<span data-ttu-id="ef3cb-112">Em alguns casos, o contraste é afetado pela configuração do navegador como tema claro ou tema escuro.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-112">In some cases, contrast is affected by setting the browser to light theme or dark theme.</span></span>

<span data-ttu-id="ef3cb-113">Como exemplo, na página de demonstração, os links azuis do menu de navegação da barra lateral têm contraste suficiente, mas o link verde **Cachorros** na seção **Status** de Doação não tem contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-113">As an example, on the demo page, the blue links of the sidebar navigation menu have enough contrast, but the green **Dogs** link in the **Donation status** section does not have enough contrast.</span></span>  <span data-ttu-id="ef3cb-114">Examine esses elementos usando **a ferramenta Inspecionar,** da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="ef3cb-114">Review those elements using the **Inspect** tool, as follows:</span></span>

1.  <span data-ttu-id="ef3cb-115">Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia.  Em seguida, **selecione F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-115">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="ef3cb-116">Selecione o **botão Inspecionar** \( Inspecionar botão \) no canto superior esquerdo do DevTools para que o ícone seja ![ realçado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="ef3cb-116">Select the **Inspect** \(![Inspect button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="ef3cb-117">Na página da Web renderizada, passe o mouse sobre o link **azul Gatos** do menu de navegação da barra lateral.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-117">In the rendered webpage, hover over the blue **Cats** link of the sidebar navigation menu.</span></span>  <span data-ttu-id="ef3cb-118">A **sobreposição** de informações da ferramenta Inspect é exibida.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-118">The **Inspect** tool's information overlay appears.</span></span>  <span data-ttu-id="ef3cb-119">Na seção **Acessibilidade da** sobreposição de informações, uma marca de seleção verde é exibida na linha **Contraste,** indicando que esse elemento tem contraste suficiente da cor do texto em relação à cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-119">In the **Accessibility** section of the information overlay, a green checkmark appears on the **Contrast** row, indicating that this element has enough contrast of text color versus background color.</span></span>

    :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Os itens de menu têm contraste suficiente, conforme mostrado na ferramenta Inspecionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
        <span data-ttu-id="ef3cb-121">Os itens de menu têm contraste suficiente, conforme mostrado na ferramenta Inspecionar</span><span class="sxs-lookup"><span data-stu-id="ef3cb-121">The menu items have enough contrast, as shown in the Inspect tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="ef3cb-122">Na página da Web renderizada, na seção Status da **Doação,** passe o mouse sobre o link **Cachorros.**</span><span class="sxs-lookup"><span data-stu-id="ef3cb-122">In the rendered webpage, in the **Donation Status** section, hover over the **Dogs** link.</span></span>  <span data-ttu-id="ef3cb-123">A **sobreposição** de informações da ferramenta Inspect mostra um ponto de exclamação laranja na linha **Contraste,** indicando que esse elemento não tem contraste suficiente de texto versus cores de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-123">The **Inspect** tool's information overlay shows an orange exclamation point on the **Contrast** row, indicating that this element doesn't have enough contrast of text versus background colors.</span></span>

    :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Um elemento que não tem contraste suficiente, conforme mostrado pelo aviso na ferramenta Inspecionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
        <span data-ttu-id="ef3cb-125">Um elemento que não tem contraste suficiente, conforme mostrado pelo aviso na ferramenta Inspecionar</span><span class="sxs-lookup"><span data-stu-id="ef3cb-125">An element that doesn't have enough contrast, as shown by the warning in the Inspect tool</span></span>
    :::image-end:::


## <a name="different-options-to-inspect-text-color-contrast-in-devtools"></a><span data-ttu-id="ef3cb-126">Opções diferentes para inspecionar o contraste de cor de texto no DevTools</span><span class="sxs-lookup"><span data-stu-id="ef3cb-126">Different options to inspect text-color contrast in DevTools</span></span>

<span data-ttu-id="ef3cb-127">Use os seguintes recursos de DevTools para inspecionar o contraste de cor de texto.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-127">Use the following DevTools features to inspect text-color contrast.</span></span>

*  <span data-ttu-id="ef3cb-128">Use a **ferramenta Inspecionar** (como uma sobreposição de informações na página da Web) para verificar se um elemento de página individual tem contraste de cor de texto suficiente.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-128">Use the **Inspect** tool (as an information overlay on the webpage) to check whether an individual page element has enough text-color contrast.</span></span>  <span data-ttu-id="ef3cb-129">A **sobreposição** de informações da ferramenta Inspect inclui uma seção **Accessibility** que tem uma linha **de informações Contraste.**</span><span class="sxs-lookup"><span data-stu-id="ef3cb-129">The **Inspect** tool's information overlay includes an **Accessibility** section that has a **Contrast** information row.</span></span>  <span data-ttu-id="ef3cb-130">A **ferramenta Inspect** mostra apenas informações de contraste de texto para o estado atual.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-130">The **Inspect** tool only shows text-contrast information for the current state.</span></span>  <span data-ttu-id="ef3cb-131">Essa abordagem é descrita no artigo atual.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-131">This approach is described in the current article.</span></span>

*  <span data-ttu-id="ef3cb-132">A **ferramenta Issues** relata automaticamente quaisquer problemas de contraste de cor para toda a página da Web, quando o texto e a cor do plano de fundo não são contrastados o suficiente.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-132">The **Issues** tool automatically reports any color-contrast issues for the entire webpage, when text and background color don't contrast enough.</span></span>  <span data-ttu-id="ef3cb-133">Esta abordagem é descrita em [Verificar se as cores de texto têm contraste suficiente.](test-issues-tool.md#verify-that-text-colors-have-enough-contrast)</span><span class="sxs-lookup"><span data-stu-id="ef3cb-133">This approach is described in [Verify that text colors have enough contrast](test-issues-tool.md#verify-that-text-colors-have-enough-contrast).</span></span>

*  <span data-ttu-id="ef3cb-134">Emular um estado não padrão, como o estado, usando o Estado do Elemento Toggle no painel Estilos, descrito em Verificar acessibilidade de todos os `hover` estados de [elementos](test-inspect-states.md). \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ef3cb-134">Emulate a non-default state, such as the `hover` state, by using **Toggle Element State** in the **Styles** pane, described in [Verify accessibility of all states of elements](test-inspect-states.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="ef3cb-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ef3cb-135">See also</span></span>

*  [<span data-ttu-id="ef3cb-136">Verifique a acessibilidade de todos os estados dos elementos</span><span class="sxs-lookup"><span data-stu-id="ef3cb-136">Verify accessibility of all states of elements</span></span>][DevtoolsAccessibilityTestInspectStates]
*  [<span data-ttu-id="ef3cb-137">Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web</span><span class="sxs-lookup"><span data-stu-id="ef3cb-137">Use the Inspect tool to detect accessibility issues by hovering over the webpage</span></span>](test-inspect-tool.md)
*  [<span data-ttu-id="ef3cb-138">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="ef3cb-138">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ef3cb-139">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ef3cb-139">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityTestInspectStates]: test-inspect-states.md "Verifique a acessibilidade de todos os estados de elementos | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
