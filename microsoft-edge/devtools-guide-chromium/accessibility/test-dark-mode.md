---
description: Verifique se há problemas de contraste com tema escuro e tema claro (para modo escuro e modo claro) usando o recurso de mídia \"Emular mídia CSS prefers-color-scheme\" na ferramenta Rendering.
title: Verifique se há problemas de contraste com o tema escuro e o tema claro
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 052c75b610ec872329f387e46819867f299a8ca9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597204"
---
# <a name="check-for-contrast-issues-with-dark-theme-and-light-theme"></a><span data-ttu-id="f4f3f-104">Verifique se há problemas de contraste com o tema escuro e o tema claro</span><span class="sxs-lookup"><span data-stu-id="f4f3f-104">Check for contrast issues with dark theme and light theme</span></span>

<!-- Rendering tool: Emulate CSS media feature prefers-color-scheme -->

<span data-ttu-id="f4f3f-105">Ao testar a acessibilidade de cores, pode haver diferentes temas de cores de exibição que você precisa testar para problemas de contraste.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-105">When testing color accessibility, there could be different display color themes that you need to test for contrast issues.</span></span>

<span data-ttu-id="f4f3f-106">A maioria dos sistemas operacionais vem com um modo escuro e um modo claro.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-106">Most operating systems come with a dark mode and a light mode.</span></span>  <span data-ttu-id="f4f3f-107">Sua página da Web pode reagir a essa configuração do sistema operacional usando uma consulta de mídia CSS.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-107">Your webpage can react to this operating system setting, by using a CSS media query.</span></span>  <span data-ttu-id="f4f3f-108">Você pode testar esses temas e testar sua consulta de mídia CSS sem precisar alterar a configuração do sistema operacional usando as opções CSS na `prefers-color-scheme` ferramenta **Rendering.**</span><span class="sxs-lookup"><span data-stu-id="f4f3f-108">You can test these themes and test your CSS media query without having to change your operating system setting, by using the `prefers-color-scheme` CSS options in the **Rendering** tool.</span></span>

<span data-ttu-id="f4f3f-109">Como exemplo, a página de demonstração de teste de acessibilidade inclui um tema claro e um tema escuro.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-109">As an example, the accessibility-testing demo page includes a light theme and a dark theme.</span></span>  <span data-ttu-id="f4f3f-110">A página de demonstração herda a configuração de tema escuro ou claro do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-110">The demo page inherits the dark or light theme setting from the operating system.</span></span>  <span data-ttu-id="f4f3f-111">Se usarmos o DevTools para simular o sistema operacional que está sendo definido como um esquema de luz e atualizar a página da Web de demonstração, a ferramenta **Issues** mostrará seis problemas de contraste de cor em vez de dois.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-111">If we use DevTools to simulate the operating system being set to a light scheme and then refresh the demo webpage, the **Issues** tool shows six color-contrast problems instead of two.</span></span>  <span data-ttu-id="f4f3f-112">(Você pode ver números diferentes.)</span><span class="sxs-lookup"><span data-stu-id="f4f3f-112">(You might see different numbers.)</span></span>


<span data-ttu-id="f4f3f-113">Para emular a seleção de um usuário do tema de cor preferencial:</span><span class="sxs-lookup"><span data-stu-id="f4f3f-113">To emulate a user's selection of preferred color theme:</span></span>

1.  <span data-ttu-id="f4f3f-114">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-114">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="f4f3f-115">Selecione **Esc** para abrir a Gaveta na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-115">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="f4f3f-116">Selecione o ícone na parte superior da Gaveta para ver a lista de ferramentas e selecione **+** **Renderização**.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-116">Select the **+** icon at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  <span data-ttu-id="f4f3f-117">A ferramenta Rendering é exibida.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-117">The Rendering tool appears.</span></span>

1.  <span data-ttu-id="f4f3f-118">No recurso **de mídia CSS emular prefere a lista** suspenso esquema de cores, selecione **prefers-color-scheme: light**.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-118">In the **Emulate CSS media feature prefers-color-scheme** dropdown list, select **prefers-color-scheme: light**.</span></span>      <span data-ttu-id="f4f3f-119">A página da Web é renderizada usando `light-theme.css` .</span><span class="sxs-lookup"><span data-stu-id="f4f3f-119">The webpage is re-rendered using `light-theme.css`.</span></span>


    :::image type="complex" source="../media/a11y-testing-simulating-light-mode.msft.png" alt-text="Usar a ferramenta Rendering para simular um modo de luz e disparar o outro tema do documento" lightbox="../media/a11y-testing-simulating-light-mode.msft.png":::
        <span data-ttu-id="f4f3f-121">Usar a ferramenta Rendering para simular um modo de luz e disparar o outro tema do documento</span><span class="sxs-lookup"><span data-stu-id="f4f3f-121">Using the Rendering tool to simulate a light mode and triggering the other theme of the document</span></span>
    :::image-end:::


1.  <span data-ttu-id="f4f3f-122">Selecione a **ferramenta Problemas** e expanda a **seção Acessibilidade.**</span><span class="sxs-lookup"><span data-stu-id="f4f3f-122">Select the **Issues** tool, and then expand the **Accessibility** section.</span></span>  <span data-ttu-id="f4f3f-123">Dependendo de vários fatores, você pode receber `Insufficient color contrast` avisos.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-123">Depending on various factors, you might get `Insufficient color contrast` warnings.</span></span> <span data-ttu-id="f4f3f-124">Observe nos **RECURSOS AFETADOs** que há 6 elementos com contraste de cor insuficiente.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-124">Notice in **AFFECTED RESOURCES** there are 6 elements with insufficient color contrast.</span></span>
    
    :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Novos problemas de contraste detectados devido à alteração para tema claro" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
        <span data-ttu-id="f4f3f-126">Novos problemas de contraste detectados devido à alteração para tema claro</span><span class="sxs-lookup"><span data-stu-id="f4f3f-126">New contrast issues detected because of the change to light theme</span></span>
    :::image-end:::
    
    <span data-ttu-id="f4f3f-127">Em nossa página de demonstração, a seção **Status** de doação da página é ilegível no modo claro e precisa ser mudada.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-127">On our demo page, the **Donation status** section of the page is unreadable in light mode, and needs to change.</span></span> 
    
    :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="A seção Status da Doação tem problemas de contraste no modo claro" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
        <span data-ttu-id="f4f3f-129">A **seção Status da Doação** tem problemas de contraste no modo claro</span><span class="sxs-lookup"><span data-stu-id="f4f3f-129">The **Donation Status** section has contrast issues in light mode</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="f4f3f-130">No DevTools, selecione a ferramenta **Elementos** e selecione **Ctrl+F** em Windows/Linux ou **Command+F** no macOS.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-130">In DevTools, select the **Elements** tool, and then select **Ctrl+F** on Windows/Linux or **Command+F** on macOS.</span></span>  <span data-ttu-id="f4f3f-131">A **caixa** de texto Encontrar é exibida, para pesquisar na árvore DOM HTML.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-131">The **Find** textbox appears, to search within the HTML DOM tree.</span></span>
 
1.  <span data-ttu-id="f4f3f-132">Insira `scheme` .</span><span class="sxs-lookup"><span data-stu-id="f4f3f-132">Enter `scheme`.</span></span>  <span data-ttu-id="f4f3f-133">As seguintes consultas de mídia CSS são encontradas e os arquivos CSS correspondentes agora podem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="f4f3f-133">The following CSS media queries are found, and the corresponding CSS files can now be updated.</span></span>

    ```html
    <link rel="stylesheet" href="css/light-theme.css" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)">
    <link rel="stylesheet" href="css/dark-theme.css" media="(prefers-color-scheme: dark)">
    ```


## <a name="see-also"></a><span data-ttu-id="f4f3f-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f4f3f-134">See also</span></span>

*  [<span data-ttu-id="f4f3f-135">Simulação de esquema de cores escuro ou claro</span><span class="sxs-lookup"><span data-stu-id="f4f3f-135">Dark or light color scheme simulation</span></span>][DevToolsColorSchemeSimulation]
*  [<span data-ttu-id="f4f3f-136">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="f4f3f-136">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f4f3f-137">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f4f3f-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Simulação de esquema de cores escuro ou claro | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
