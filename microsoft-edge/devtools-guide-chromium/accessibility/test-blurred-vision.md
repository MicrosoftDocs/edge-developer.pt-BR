---
description: Para verificar se uma página da Web pode ser usada com visão desfocado, na ferramenta Renderização, use a lista suspenso Deficiências de visão emular.
title: Verifique se a página pode ser usada com visão turva
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2fc1a1cf7746591573fce07946c7fb11abf42705
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597207"
---
# <a name="verify-that-the-page-is-usable-with-blurred-vision"></a><span data-ttu-id="2655d-104">Verifique se a página pode ser usada com visão turva</span><span class="sxs-lookup"><span data-stu-id="2655d-104">Verify that the page is usable with blurred vision</span></span>

<!-- Rendering tool: Emulate vision deficiencies: Blurred vision -->

<span data-ttu-id="2655d-105">Para simular a visão desfocado, na ferramenta **Rendering,** use o menu **Emular deficiências de** visão.</span><span class="sxs-lookup"><span data-stu-id="2655d-105">To simulate blurred vision, in the **Rendering** tool, use the **Emulate vision deficiencies** menu.</span></span>  <span data-ttu-id="2655d-106">Quando você usa esse recurso com a página da Web de demonstração, você pode ver que a sombra de soltar no texto no menu superior dificulta a leitura dos itens do menu.</span><span class="sxs-lookup"><span data-stu-id="2655d-106">When you use this feature with the demo webpage, you can see that the drop shadow on the text in the upper menu makes it hard to read the menu items.</span></span>

<span data-ttu-id="2655d-107">Para verificar se uma página da Web é usável com visão desfocado:</span><span class="sxs-lookup"><span data-stu-id="2655d-107">To check whether a webpage is usable with blurred vision:</span></span>

1.  <span data-ttu-id="2655d-108">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="2655d-108">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="2655d-109">Selecione **Esc** para abrir a Gaveta na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="2655d-109">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="2655d-110">Selecione o ícone na parte superior da Gaveta para exibir a lista de ferramentas e selecione **+** **Renderização**.</span><span class="sxs-lookup"><span data-stu-id="2655d-110">Select the **+** icon at the top of the Drawer to display the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="2655d-111">Na lista **lista suspenso Deficiências de visão** emular, selecione Visão **desfocado**.</span><span class="sxs-lookup"><span data-stu-id="2655d-111">In the **Emulate vision deficiencies** dropdown list, select **Blurred vision**.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simulando uma página desfocado" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
        <span data-ttu-id="2655d-113">Simulando uma página desfocado</span><span class="sxs-lookup"><span data-stu-id="2655d-113">Simulating a blurred page</span></span>
    :::image-end:::

    <span data-ttu-id="2655d-114">Observe que a `text-shadow` propriedade CSS torna o texto dos itens de menu difíceis de ler no menu superior.</span><span class="sxs-lookup"><span data-stu-id="2655d-114">Notice that the `text-shadow` CSS property makes the text of the menu items difficult to read on the upper menu.</span></span> <span data-ttu-id="2655d-115">Por exemplo, revise **Home**, **Adopt a Pet**e outros itens de menu.</span><span class="sxs-lookup"><span data-stu-id="2655d-115">For example, review the **Home**, **Adopt a Pet**, and other menu items.</span></span>
    
1.  <span data-ttu-id="2655d-116">Na ferramenta **Rendering,** em **Emular**deficiências de visão, selecione **Nenhuma emulação** para remover a simulação de visão desfocado.</span><span class="sxs-lookup"><span data-stu-id="2655d-116">In the **Rendering** tool, in **Emulate vision deficiencies**, select **No emulation** to remove the blurred vision simulation.</span></span>


## <a name="see-also"></a><span data-ttu-id="2655d-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2655d-117">See also</span></span>

*  [<span data-ttu-id="2655d-118">Emular deficiências visuais</span><span class="sxs-lookup"><span data-stu-id="2655d-118">Emulate vision deficiencies</span></span>](emulate-vision-deficiencies.md)
*  [<span data-ttu-id="2655d-119">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="2655d-119">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2655d-120">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2655d-120">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
