---
description: Verifique se as páginas da Web são usáveis com a animação da interface do usuário desligada (movimento reduzido) usando o recurso de mídia CSS emular prefere a lista suspensa de movimento reduzido na ferramenta Rendering.
title: Verifique se a página pode ser usada com a animação da interface do usuário desligada
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ec30925b706b4b1c6dfaaa6ce66a38fab8759ac2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597171"
---
# <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off"></a><span data-ttu-id="4d9a7-104">Verifique se a página pode ser usada com a animação da interface do usuário desligada</span><span class="sxs-lookup"><span data-stu-id="4d9a7-104">Verify that the page is usable with UI animation turned off</span></span>

<span data-ttu-id="4d9a7-105">Uma página da Web não deve mostrar animações para um usuário que desligou animações no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-105">A webpage should not show animations to a user who turned off animations in the operating system.</span></span>  <span data-ttu-id="4d9a7-106">As animações podem ajudar a usabilidade de um produto, mas também podem causar distrações, confusão ou enjoo.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-106">Animations can help the usability of a product, but they can also cause distraction, confusion, or nausea.</span></span>

<span data-ttu-id="4d9a7-107">Para verificar se uma página da Web pode ser usada com a animação da interface do usuário desligada (movimento reduzido), na ferramenta **Renderização,** use o recurso de mídia **CSS emular** prefere a lista suspensa de movimento reduzido.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-107">To check that a webpage is usable with UI animation turned off (reduced motion), in the **Rendering** tool, use the **Emulate CSS media feature prefers-reduced-motion** dropdown list.</span></span>

<span data-ttu-id="4d9a7-108">Na página da Web de demonstração de teste de acessibilidade, quando você desativar animações no sistema operacional ou emular essas configurações usando DevTools, a página da Web não usa rolagem suave quando você seleciona os links do menu de navegação de barra lateral.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-108">In the accessibility-testing demo webpage, when you turn off animations in the operating system, or emulate that settings by using DevTools, the webpage doesn't use smooth scrolling when you select the links of the sidebar navigation menu.</span></span>  <span data-ttu-id="4d9a7-109">Isso é obtido envolvendo a configuração de rolagem suave em CSS em uma consulta de mídia e, em seguida, usando a ferramenta **Rendering** para emular a configuração do sistema operacional para animação reduzida.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-109">This is achieved by wrapping the smooth-scrolling setting in CSS in a media query, and then using the **Rendering** tool to emulate the operating system setting for reduced animation.</span></span>

<span data-ttu-id="4d9a7-110">Para verificar se a página pode ser usável com animações desligadas:</span><span class="sxs-lookup"><span data-stu-id="4d9a7-110">To check whether the page is usable with animations turned off:</span></span>

1.  <span data-ttu-id="4d9a7-111">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-111">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="4d9a7-112">Na parte superior do DevTools, selecione a ferramenta **Fontes** e, no **painel** navegação à esquerda, selecione `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="4d9a7-112">At the top of DevTools, select the **Sources** tool, and then in the **Navigation** pane on the left, select `styles.css`.</span></span>  <span data-ttu-id="4d9a7-113">O arquivo CSS aparece no **painel Editor.**</span><span class="sxs-lookup"><span data-stu-id="4d9a7-113">The CSS file appears in the **Editor** pane.</span></span>

1.  <span data-ttu-id="4d9a7-114">Selecione **Ctrl+F no** Windows/Linux ou **Command+F** no macOS e insira `@media` .</span><span class="sxs-lookup"><span data-stu-id="4d9a7-114">Select **Ctrl+F** on Windows/Linux or **Command+F** on macOS, and then enter `@media`.</span></span>  <span data-ttu-id="4d9a7-115">A seguinte consulta de mídia CSS é exibida, o que confirma que ela é usada na página da Web.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-115">The following CSS media query is displayed, which confirms that it is used on the webpage.</span></span>

    ```css
    @media (prefers-reduced-motion: no-preference) {
      html {
        scroll-behavior: smooth;
      }
    }
    ```

    <span data-ttu-id="4d9a7-116">Em seguida, emular a configuração do sistema operacional para reduzir a animação, da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-116">Next, emulate the operating system setting to reduce animation, as follows.</span></span>

1.  <span data-ttu-id="4d9a7-117">Selecione **Esc** para abrir a Gaveta na parte inferior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-117">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="4d9a7-118">Selecione o **botão Mais ferramentas** ( ) na parte superior da Gaveta para ver a lista de ferramentas e selecione **+** **Renderização**.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-118">Select the **More tools** (**+**) button at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="4d9a7-119">No recurso **de mídia CSS emular prefere a** lista suspenso de movimento reduzido, selecione **prefers-reduced-motion: reduced**.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-119">In the **Emulate CSS media feature prefers-reduced-motion** dropdown list, select **prefers-reduced-motion: reduced**.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulando o movimento reduzido e o CSS que garante que a rolagem suave só acontece quando o usuário o deseja" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
        <span data-ttu-id="4d9a7-121">Simulando o movimento reduzido e o CSS que garante que a rolagem suave só acontece quando o usuário o deseja</span><span class="sxs-lookup"><span data-stu-id="4d9a7-121">Simulating reduced motion and the CSS that makes sure that smooth scrolling only happens when the user wants it</span></span>
    :::image-end:::

1.  <span data-ttu-id="4d9a7-122">Na página da Web, selecione os itens de menu azul, como **Cavalos** ou **Alpacas**.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-122">In the webpage, select the blue menu items, such as **Horses** or **Alpacas**.</span></span>  <span data-ttu-id="4d9a7-123">Agora, a página da Web rola instantaneamente para a seção selecionada, em vez de usar a animação de rolagem suave.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-123">Now the webpage instantly scrolls to the selected section, rather than using the smooth-scrolling animation.</span></span>

1.  <span data-ttu-id="4d9a7-124">Na ferramenta **Rendering,** abaixo Emular o recurso de mídia **CSS prefere movimento reduzido,** selecione **Sem emulação** para remover essa configuração.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-124">In the **Rendering** tool, below **Emulate CSS media feature prefers-reduced-motion**, select **No emulation** to remove this setting.</span></span>
   
<span data-ttu-id="4d9a7-125">Observe que a página da Web de demonstração ainda executa as seguintes animações, mesmo com as configurações de consulta e emulação de mídia acima.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-125">Notice that the demo webpage still runs the following animations, even with the above media query and emulation settings.</span></span> <span data-ttu-id="4d9a7-126">Ao criar seu produto Web, certifique-se de corrigir todas as animações semelhantes.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-126">When building your web product, ensure you fix all similar animations.</span></span>  
*  <span data-ttu-id="4d9a7-127">Animação dos itens de menu azul quando você passar o mouse sobre eles.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-127">Animation of the blue menu items when you hover over them.</span></span>
*  <span data-ttu-id="4d9a7-128">Animação dos círculos nos links **Mais** quando você passar o mouse sobre eles.</span><span class="sxs-lookup"><span data-stu-id="4d9a7-128">Animation of the circles on the **More** links when you hover over them.</span></span>



## <a name="see-also"></a><span data-ttu-id="4d9a7-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4d9a7-129">See also</span></span>

*  [<span data-ttu-id="4d9a7-130">Simulação de movimento reduzido</span><span class="sxs-lookup"><span data-stu-id="4d9a7-130">Reduced motion simulation</span></span>](reduced-motion-simulation.md)
*  [<span data-ttu-id="4d9a7-131">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="4d9a7-131">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4d9a7-132">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4d9a7-132">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
