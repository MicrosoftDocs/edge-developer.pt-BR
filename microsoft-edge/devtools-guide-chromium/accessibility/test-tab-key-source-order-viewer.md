---
description: Para ver rapidamente a ordem de tabulação das seções de uma página, use o Visualizador de Ordem de Origem na ferramenta Acessibilidade, à direita da guia Estilos.
title: Teste o suporte ao teclado usando o Visualizador de Ordem de Origem
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7e90221b581280a6eb63cee4d073622a80871903
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597168"
---
# <a name="test-keyboard-support-using-the-source-order-viewer"></a><span data-ttu-id="fccfe-104">Teste o suporte ao teclado usando o Visualizador de Ordem de Origem</span><span class="sxs-lookup"><span data-stu-id="fccfe-104">Test keyboard support using the Source Order Viewer</span></span>

<span data-ttu-id="fccfe-105">A ordem de origem de um documento é importante para a tecnologia assistida e pode ser diferente da ordem na qual os elementos aparecem na página renderizada.</span><span class="sxs-lookup"><span data-stu-id="fccfe-105">The source order of a document is important for assistive technology, and can be different than the order in which elements appear on the rendered page.</span></span>  <span data-ttu-id="fccfe-106">Usando CSS, você pode re-ordenar elementos de página de forma visual, mas isso não significa que a tecnologia auxiliar, como leitores de tela, representaria elementos de página na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="fccfe-106">Using CSS, you can re-order page elements in a visual way, but that doesn't mean that assistive technology such as screen readers would represent page elements in the same order.</span></span>  

<span data-ttu-id="fccfe-107">Para garantir que o documento tenha uma \*\*\*\* ordem lógica, você pode usar o Visualizador de Ordem de Origem para rotular diferentes elementos de página com números que especificam a ordem no código-fonte do documento.</span><span class="sxs-lookup"><span data-stu-id="fccfe-107">To ensure that the document has a logical order, you can use the **Source Order Viewer** to label different page elements with numbers that specify the order in the source code of the document.</span></span>  <span data-ttu-id="fccfe-108">O **Visualizador de Ordem de** Origem está na guia **Acessibilidade** (perto da **guia Estilos).**</span><span class="sxs-lookup"><span data-stu-id="fccfe-108">The **Source Order Viewer** is in the **Accessibility** tab (near the **Styles** tab).</span></span>


## <a name="analyzing-the-order-of-keyboard-access-through-sections-of-the-page"></a><span data-ttu-id="fccfe-109">Analisando a ordem de acesso ao teclado por meio de seções da página</span><span class="sxs-lookup"><span data-stu-id="fccfe-109">Analyzing the order of keyboard access through sections of the page</span></span>

<span data-ttu-id="fccfe-110">A [página da Web][DevToolsA11yErrorsDemopage] de demonstração de teste de acessibilidade tem uma ordem de tabulação contraintuitiva, onde os usuários de teclado acessam o menu de navegação da barra lateral somente depois de fazer a tabulação de todos os links **Mais.**</span><span class="sxs-lookup"><span data-stu-id="fccfe-110">The [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] has a counterintuitive tabbing order, where keyboard users access the sidebar navigation menu only after tabbing through all the **More** links.</span></span>  <span data-ttu-id="fccfe-111">O menu de navegação da barra lateral deve ser um atalho para alcançar profundamente o conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="fccfe-111">The sidebar navigation menu is meant to be a shortcut to reach deep into the page content.</span></span>  <span data-ttu-id="fccfe-112">Porém, como você precisa passar por toda a página antes de chegar ao menu de navegação da barra lateral, esse menu de navegação é ineficaz para usuários de teclado.</span><span class="sxs-lookup"><span data-stu-id="fccfe-112">But because you need to go through the entire page before you reach the sidebar navigation menu, that navigation menu is ineffective for keyboard users.</span></span>

<span data-ttu-id="fccfe-113">A `Tab` ordem de chave na página de demonstração é:</span><span class="sxs-lookup"><span data-stu-id="fccfe-113">The `Tab` key order on the demo page is:</span></span>
1. <span data-ttu-id="fccfe-114">O **campo** Pesquisa e, em seguida, **o botão ir** para o **campo** Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fccfe-114">The **Search** field, then the **go** button for the **Search** field.</span></span>
1. <span data-ttu-id="fccfe-115">O **botão Mais** na seção **Gatos,** para navegar até uma página da Web "Gatos".</span><span class="sxs-lookup"><span data-stu-id="fccfe-115">The **More** button in the **Cats** section, to navigate to a "Cats" webpage.</span></span>  <span data-ttu-id="fccfe-116">Em seguida, os **outros botões Mais,** para Cachorros, Cavalos, Cavalos e, em seguida, Alpacas.</span><span class="sxs-lookup"><span data-stu-id="fccfe-116">Then the other **More** buttons, for Dogs, Sheep, Horses, and then Alpacas.</span></span>
1. <span data-ttu-id="fccfe-117">Os links azuis do menu de navegação da \*\*\*\* barra lateral: **Gatos**, **Cachorros,** **Cavalos,** Cavalos e **Alpacas**.</span><span class="sxs-lookup"><span data-stu-id="fccfe-117">The blue links of the sidebar navigation menu: **Cats**, **Dogs**, **Sheep**, **Horses**, and then **Alpacas**.</span></span>
1. <span data-ttu-id="fccfe-118">A caixa de texto de doação no formulário de doação.</span><span class="sxs-lookup"><span data-stu-id="fccfe-118">The donation textbox in the donation form.</span></span>
1. <span data-ttu-id="fccfe-119">Os botões na barra de navegação superior: **Home**, **Adopt a pet**, **Doar**, **Trabalhos**e, em seguida, **Sobre Nós**.</span><span class="sxs-lookup"><span data-stu-id="fccfe-119">The buttons in the top navigation bar: **Home**, **Adopt a pet**, **Donate**, **Jobs**, and then **About Us**.</span></span>
1. <span data-ttu-id="fccfe-120">A interface top-of-window do navegador.</span><span class="sxs-lookup"><span data-stu-id="fccfe-120">The browser's top-of-window interface.</span></span>

<span data-ttu-id="fccfe-121">O motivo da ordem de chave confusa é que a ordem experimentada ao usar um teclado é determinada pela `Tab` ordem de origem do documento.</span><span class="sxs-lookup"><span data-stu-id="fccfe-121">The reason for the confusing `Tab` key order is that the order experienced when using a keyboard is determined by the source order of the document.</span></span>  <span data-ttu-id="fccfe-122">A ordem experimentado usando um teclado pode ser modificada usando o atributo em elementos, o que tira esse elemento `tabindex` da ordem de origem.</span><span class="sxs-lookup"><span data-stu-id="fccfe-122">The order experienced using a keyboard can be modified using the `tabindex` attribute on elements, which takes that element out of the source order.</span></span>

<span data-ttu-id="fccfe-123">No código-fonte do documento, o menu de navegação da barra lateral é exibido após o conteúdo principal da página da Web.</span><span class="sxs-lookup"><span data-stu-id="fccfe-123">In the source code of the document, the sidebar navigation menu appears after the main content of the webpage.</span></span>  <span data-ttu-id="fccfe-124">CSS foi usado para posicionar o menu de navegação da barra lateral acima da maioria do conteúdo principal da página da Web.</span><span class="sxs-lookup"><span data-stu-id="fccfe-124">CSS was used to position the sidebar navigation menu above most of the main content of the webpage.</span></span> 

<span data-ttu-id="fccfe-125">Você pode testar a ordem dos elementos de página usando o Visualizador de Ordem **de Origem** na guia **Acessibilidade.**  O **Visualizador de Ordem de Origem** é um recurso experimental.</span><span class="sxs-lookup"><span data-stu-id="fccfe-125">You can test the order of page elements by using the **Source Order Viewer** in the **Accessibility** tab.  The **Source Order Viewer** is an experimental feature.</span></span> <span data-ttu-id="fccfe-126">Para obter mais informações, navegue até [Source Order Viewer](../experimental-features/index.md#source-order-viewer).</span><span class="sxs-lookup"><span data-stu-id="fccfe-126">For more information, navigate to [Source Order Viewer](../experimental-features/index.md#source-order-viewer).</span></span>


<span data-ttu-id="fccfe-127">Para ativar o Visualizador de Ordem de Origem:</span><span class="sxs-lookup"><span data-stu-id="fccfe-127">To turn on the Source Order Viewer:</span></span>

1.  <span data-ttu-id="fccfe-128">No DevTools, no canto superior direito, selecione o botão **Configurações** \( Configurações ![ botão ](../media/settings-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="fccfe-128">In DevTools, in the upper right, select the **Settings** \(![Settings button](../media/settings-button-icon.msft.png)\) button.</span></span>  

1.  <span data-ttu-id="fccfe-129">Abaixo **Configurações**, selecione **Experimentos**.</span><span class="sxs-lookup"><span data-stu-id="fccfe-129">Below **Settings**, select **Experiments**.</span></span>  

1.  <span data-ttu-id="fccfe-130">Selecione a **caixa de seleção Visualizador de Ordem** de Origem.</span><span class="sxs-lookup"><span data-stu-id="fccfe-130">Select the **Source Order Viewer** checkbox.</span></span>

1.  <span data-ttu-id="fccfe-131">No canto superior direito da **página** Configurações, selecione **X** para fechar a página Configurações.</span><span class="sxs-lookup"><span data-stu-id="fccfe-131">In the upper-right corner of the **Settings** page, select **X** to close the Settings page.</span></span>  <span data-ttu-id="fccfe-132">Na parte superior do DevTools, a mensagem Uma ou mais configurações foram **alteradas,** o que exige que uma recarga entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="fccfe-132">At the top of DevTools, the message **One or more settings have changed which require a reload to take effect.**</span></span> <span data-ttu-id="fccfe-133">é exibido.</span><span class="sxs-lookup"><span data-stu-id="fccfe-133">is displayed.</span></span>  <span data-ttu-id="fccfe-134">Selecione o **botão Recarregar DevTools.**</span><span class="sxs-lookup"><span data-stu-id="fccfe-134">Select the **Reload DevTools** button.</span></span>



<span data-ttu-id="fccfe-135">Para ativar e usar o Visualizador de Ordem de Origem, com a página de demonstração:</span><span class="sxs-lookup"><span data-stu-id="fccfe-135">To activate and use the Source Order Viewer, with the demo page:</span></span>

1.  <span data-ttu-id="fccfe-136">Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia.  Em seguida, **selecione F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="fccfe-136">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="fccfe-137">Na ferramenta **Elementos,** à direita da guia **Estilos,** selecione **a guia** Acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="fccfe-137">In the **Elements** tool, to the right of the **Styles** tab, select the **Accessibility** tab.</span></span>

1.  <span data-ttu-id="fccfe-138">Na seção **Visualizador de Ordem de** Origem, selecione a caixa de seleção **Mostrar ordem de** origem.</span><span class="sxs-lookup"><span data-stu-id="fccfe-138">In the **Source Order Viewer** section, select the **Show source order** checkbox.</span></span>  <span data-ttu-id="fccfe-139">Na página da Web renderizada, os números aparecem, indicando a ordem como controlada pela ordem de linhas de `Tab` código no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="fccfe-139">In the rendered webpage, numbers appear, indicating the `Tab` order as controlled by the order of lines of code in the source file.</span></span>

1.  <span data-ttu-id="fccfe-140">Na árvore DOM na ferramenta **Elementos,** selecione um elemento de layout principal, como o `header` elemento.</span><span class="sxs-lookup"><span data-stu-id="fccfe-140">In the DOM tree in the **Elements** tool, select a major layout element, such as the `header` element.</span></span>  <span data-ttu-id="fccfe-141">As sobreposições numéricas agora são exibidas em seções da página renderizada, que indicam a ordem de origem dos diferentes elementos.</span><span class="sxs-lookup"><span data-stu-id="fccfe-141">Numeric overlays are now displayed on sections of the rendered page, which indicate the source order of the different elements.</span></span> 

    :::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="Ativar o Visualizador de Ordem de Origem mostra a ordem dos elementos na origem como sobreposições na página" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
        <span data-ttu-id="fccfe-143">Ativar o **Visualizador de Ordem** de Origem mostra a ordem dos elementos na origem como sobreposições na página</span><span class="sxs-lookup"><span data-stu-id="fccfe-143">Activating the **Source Order Viewer** shows the order of the elements in the source as overlays on the page</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="fccfe-144">Role a página para ver todas as sobreposições numéricas, incluindo na seção rodapé da página.</span><span class="sxs-lookup"><span data-stu-id="fccfe-144">Scroll the page to see all of the numeric overlays, including on the page footer section.</span></span>


## <a name="see-also"></a><span data-ttu-id="fccfe-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fccfe-145">See also</span></span>

*  [<span data-ttu-id="fccfe-146">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="fccfe-146">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="fccfe-147">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fccfe-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
