---
description: Verifique se as páginas da Web podem ser usáveis por pessoas com deficiências de cor usando a lista lista suspenso Deficiências de Visão emular na ferramenta Renderização.
title: Verifique se a página pode ser usada por pessoas com daltonismo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 54cd7230f0402bfeb4b5ee28d2bcd0947794676f
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597205"
---
# <a name="verify-that-the-page-is-usable-by-people-with-color-blindness"></a><span data-ttu-id="9a414-104">Verifique se a página pode ser usada por pessoas com daltonismo</span><span class="sxs-lookup"><span data-stu-id="9a414-104">Verify that the page is usable by people with color blindness</span></span>

<!-- Rendering tool: Emulate vision deficiencies: Protanopia -->

<span data-ttu-id="9a414-105">Para verificar se uma página da Web pode ser usada por pessoas com deficiências de cor, na ferramenta **Rendering,** use a lista suspenso Deficiências de visão **emular.**</span><span class="sxs-lookup"><span data-stu-id="9a414-105">To check that a webpage is usable by people with color blindness, in the **Rendering** tool, use the **Emulate vision deficiencies** dropdown list.</span></span>

<span data-ttu-id="9a414-106">Na página da web de demonstração de teste de acessibilidade, os diferentes estados de doação usam a cor como o único meio de diferenciação.</span><span class="sxs-lookup"><span data-stu-id="9a414-106">On the accessibility-testing demo webpage, the different donation states use color as the only means of differentiation.</span></span>
*  <span data-ttu-id="9a414-107">Verde significa que uma grande quantidade de doações foram recebidas.</span><span class="sxs-lookup"><span data-stu-id="9a414-107">Green means a high amount of donations have been received.</span></span>
*  <span data-ttu-id="9a414-108">Amarelo significa que uma quantidade média de doações foi recebida.</span><span class="sxs-lookup"><span data-stu-id="9a414-108">Yellow means a medium amount of donations have been received.</span></span>
*  <span data-ttu-id="9a414-109">Vermelho significa que uma baixa quantidade de doações foi recebida.</span><span class="sxs-lookup"><span data-stu-id="9a414-109">Red means a low amount of donations have been received.</span></span>

<span data-ttu-id="9a414-110">Mas você não pode esperar que todos os seus usuários experimentem essas cores conforme o pretendido.</span><span class="sxs-lookup"><span data-stu-id="9a414-110">But you can't expect all of your users to experience these colors as intended.</span></span>  <span data-ttu-id="9a414-111">Usando o recurso **Emular** deficiências de visão da ferramenta **Rendering,** você pode descobrir que esse design não é bom o suficiente, simulando como as pessoas com uma visão diferente perceberiam seu design.</span><span class="sxs-lookup"><span data-stu-id="9a414-111">By using the **Emulate vision deficiencies** feature of the **Rendering** tool, you can find out that this design is not good enough, by simulating how people with different vision would perceive your design.</span></span>


<span data-ttu-id="9a414-112">Para verificar se uma página da Web pode ser usável por pessoas com deficiência de cor:</span><span class="sxs-lookup"><span data-stu-id="9a414-112">To check whether a webpage is usable by people with color blindness:</span></span>

1.  <span data-ttu-id="9a414-113">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a414-113">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="9a414-114">Selecione **Esc** para abrir a Gaveta na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a414-114">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="9a414-115">Selecione o ícone na parte superior da Gaveta para ver a lista de ferramentas e selecione **+** **Renderização**.</span><span class="sxs-lookup"><span data-stu-id="9a414-115">Select the **+** icon at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="9a414-116">Na lista lista lista suspenso **Deficiências de visão** emular, selecione **Protanopia**.</span><span class="sxs-lookup"><span data-stu-id="9a414-116">In the **Emulate vision deficiencies** dropdown list, select **Protanopia**.</span></span>  <span data-ttu-id="9a414-117">_A protanopia_ reduz a sensibilidade à luz vermelha, tornando difícil diferenciar verde, vermelho e amarelo.</span><span class="sxs-lookup"><span data-stu-id="9a414-117">_Protanopia_ is reduced sensitivity to red light, making it hard to differentiate green, red, and yellow.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Mostrar o documento como alguém com protanopia o verá" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
        <span data-ttu-id="9a414-119">Mostrar o documento como alguém com protanopia o verá</span><span class="sxs-lookup"><span data-stu-id="9a414-119">Showing the document as someone with protanopia would see it</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="9a414-120">Na ferramenta **Renderização,** abaixo **Emular**deficiências de visão, selecione **Nenhuma emulação** para remover a simulação.</span><span class="sxs-lookup"><span data-stu-id="9a414-120">In the **Rendering** tool, below **Emulate vision deficiencies**, select **No emulation** to remove the simulation.</span></span>


## <a name="see-also"></a><span data-ttu-id="9a414-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9a414-121">See also</span></span>

*  <span data-ttu-id="9a414-122">[Emular][DevToolsVisionDeficiencies] deficiências de visão - Define \*\*\*\* os itens na lista de lista suspenso deficiências de visão emular, incluindo Protanopia, Deuteranopia, Tritanopia e Achromatopsia.</span><span class="sxs-lookup"><span data-stu-id="9a414-122">[Emulate vision deficiencies][DevToolsVisionDeficiencies] - Defines the items in the **Emulate vision deficiencies** dropdown list, including Protanopia, Deuteranopia, Tritanopia, and Achromatopsia.</span></span>
*  [<span data-ttu-id="9a414-123">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="9a414-123">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9a414-124">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9a414-124">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emular deficiências de visão | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
