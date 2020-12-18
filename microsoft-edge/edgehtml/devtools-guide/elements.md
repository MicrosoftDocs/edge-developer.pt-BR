---
description: Use o painel elementos para inspecionar o HTML, CSS, DOM e acessibilidade da página.
title: DevTools-elementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, elementos, HTML, CSS, pontos de interrupção do dom, eventos, acessibilidade
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 14052bc40b9f94e628f0b575ede6c1ca8ccf179a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231357"
---
# <span data-ttu-id="68a7b-104">Elementos</span><span class="sxs-lookup"><span data-stu-id="68a7b-104">Elements</span></span>

<span data-ttu-id="68a7b-105">O painel **elementos** ajuda você a:</span><span class="sxs-lookup"><span data-stu-id="68a7b-105">The **Elements** panel helps you to:</span></span>

* <span data-ttu-id="68a7b-106">[Identificar e Editar elementos na árvore HTML](#html-tree-view) da página atual</span><span class="sxs-lookup"><span data-stu-id="68a7b-106">[Identify and edit elements in the HTML tree](#html-tree-view) of the current page</span></span>
* <span data-ttu-id="68a7b-107">[Inspecionar e modificar CSS](./elements/styles.md) na página, incluindo pseudo-estados e pseudoelementos</span><span class="sxs-lookup"><span data-stu-id="68a7b-107">[Inspect and modify CSS](./elements/styles.md) on the page, including pseudo-states and pseudo-elements</span></span>
* <span data-ttu-id="68a7b-108">[Entender o layout CSS e o estilo em cascata](./elements/computed.md) acontecendo na página</span><span class="sxs-lookup"><span data-stu-id="68a7b-108">[Understand the CSS layout and style cascade](./elements/computed.md) happening on the page</span></span>
* <span data-ttu-id="68a7b-109">[Rastrear manipuladores de eventos não autorizados](./elements/events.md) para que você possa depurá-los</span><span class="sxs-lookup"><span data-stu-id="68a7b-109">[Track down rogue event handlers](./elements/events.md) so you can debug them</span></span>
* <span data-ttu-id="68a7b-110">[Definir pontos de interrupção de depuração para alterações visuais inesperadas](./elements/dom-breakpoints.md) para saltar para o código que os causou</span><span class="sxs-lookup"><span data-stu-id="68a7b-110">[Set debugging breakpoints for unexpected visual changes](./elements/dom-breakpoints.md) to jump into the code causing them</span></span>
* <span data-ttu-id="68a7b-111">[Obter informações detalhadas sobre as fontes usadas na página](./elements/fonts.md) e onde elas estão sendo carregadas</span><span class="sxs-lookup"><span data-stu-id="68a7b-111">[Get detailed information about the fonts used on the page](./elements/fonts.md) and where they're loading from</span></span>
* <span data-ttu-id="68a7b-112">[Exibir sua página a partir de um ponto de vista do leitor de tela](./elements/accessibility.md) para verificar e testar a acessibilidade</span><span class="sxs-lookup"><span data-stu-id="68a7b-112">[View your page from a screen reader's point of view](./elements/accessibility.md) to verify and test accessibility</span></span> 
* <span data-ttu-id="68a7b-113">[Revisar uma comparação em execução das alterações de CSS](./elements/changes.md) feitas enquanto você depura a interface do usuário da página</span><span class="sxs-lookup"><span data-stu-id="68a7b-113">[Review a running diff of the CSS changes](./elements/changes.md) you make as you debug the UI of your page</span></span>

## <span data-ttu-id="68a7b-114">Modo de exibição de árvore HTML</span><span class="sxs-lookup"><span data-stu-id="68a7b-114">HTML tree view</span></span>

![O painel elementos DevTools do Microsoft Edge](./media/elements.png)

1. <span data-ttu-id="68a7b-116">Use a ferramenta **Select Element** ( `Ctrl+B` ) para localizar um elemento no **modo de exibição de árvore HTML** clicando nele na página.</span><span class="sxs-lookup"><span data-stu-id="68a7b-116">Use the **Select element** (`Ctrl+B`) tool to locate an element in the **HTML tree view** by clicking on it in the page.</span></span>

2. <span data-ttu-id="68a7b-117">Use a ferramenta de **realce de elemento** ( `Ctrl+Shift+L` ) para localizar um elemento na página passando o mouse sobre ele no **modo de exibição de árvore HTML**.</span><span class="sxs-lookup"><span data-stu-id="68a7b-117">Use the **Element highlighting** (`Ctrl+Shift+L`) tool to locate an element on the page by hovering over it in the **HTML tree view**.</span></span>

3. <span data-ttu-id="68a7b-118">Abra a ferramenta **seletor de cores** ( `Ctrl+K` ) para ver uma lista das cores em uso na página atual.</span><span class="sxs-lookup"><span data-stu-id="68a7b-118">Open the **Color picker** (`Ctrl+K`) tool to see a list of the colors in use on the current page.</span></span> <span data-ttu-id="68a7b-119">Clicar em uma cor na lista fornece mais detalhes (Matiz, saturação, luminosidade, alfa).</span><span class="sxs-lookup"><span data-stu-id="68a7b-119">Clicking on a color on the list will provide further details (Hue, Saturation, Lightness, Alpha).</span></span> <span data-ttu-id="68a7b-120">O *seletor de cores* também é aberto quando você clica no quadrado colorido ao lado de um valor de cor no painel **estilos** , permitindo que você edite a cor de um elemento de página e veja os resultados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="68a7b-120">The *Color picker* also opens when you click on the colored square next to a color value in the **Styles** pane, allowing you to edit the color of a page element and immediately see the results.</span></span>

4. <span data-ttu-id="68a7b-121">O botão da **árvore de acessibilidade** ( `Ctrl+Shift+A` ) abrirá o painel de [árvore de acessibilidade](./elements/accessibility.md) mostrando a estrutura da sua página como seria exibido para uma tecnologia assistencial, como o [narrador do Windows](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) leitor.</span><span class="sxs-lookup"><span data-stu-id="68a7b-121">The **Accessibility tree** (`Ctrl+Shift+A`) button will open the [Accessibility tree](./elements/accessibility.md) pane showing the structure of your page as it would appear to an assistive technology, such as the [Windows Narrator](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) screenreader.</span></span>

5. <span data-ttu-id="68a7b-122">Você também pode **encontrar** ( `Ctrl+F` ) um elemento no modo de exibição de árvore HTML procurando por seu nome de marca, atributos ou conteúdo de texto.</span><span class="sxs-lookup"><span data-stu-id="68a7b-122">You can also **Find** (`Ctrl+F`) an element in the HTML tree view by searching for its tag name, attributes, or text content.</span></span>

### <span data-ttu-id="68a7b-123">Editando elementos</span><span class="sxs-lookup"><span data-stu-id="68a7b-123">Editing elements</span></span>

<span data-ttu-id="68a7b-124">Você pode editar um elemento clicando com o botão direito do mouse nele dentro do modo de exibição de árvore HTML e selecionando **Editar como HTML** no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="68a7b-124">You can edit an element by right-clicking on it within the HTML tree view and selecting **Edit as HTML** from the context menu.</span></span> <span data-ttu-id="68a7b-125">O menu de contexto também fornece opções para excluir, recortar, copiar, colar, definir pseudovariáveis CSS (*: ativo*, *: foco*, *: focalizar*, *: visitado*) e adicionar atributos.</span><span class="sxs-lookup"><span data-stu-id="68a7b-125">The context menu also provides options to delete, cut, copy, paste, set CSS pseudo-classes (*:active*, *:focus*, *:hover*, *:visited*) and add attributes.</span></span> <span data-ttu-id="68a7b-126">Outra maneira de editar um atributo e/ou seu valor é clicar duas vezes nele no modo de exibição de árvore HTML.</span><span class="sxs-lookup"><span data-stu-id="68a7b-126">Another way to edit an attribute and/or its value is to double-click it from the HTML tree view.</span></span>

![Menu de contexto da exibição em árvore HTML](./media/elements_html_tree_context.png)

> [!NOTE]
> <span data-ttu-id="68a7b-128">Editar a árvore HTML não afeta a marcação de origem subjacente.</span><span class="sxs-lookup"><span data-stu-id="68a7b-128">Editing the HTML tree does not affect the underlying source markup.</span></span> <span data-ttu-id="68a7b-129">Atualizar a página reverterá as alterações e renderizará apenas o layout determinado pela fonte da página.</span><span class="sxs-lookup"><span data-stu-id="68a7b-129">Refreshing the page will revert your changes and render only the layout determined by the page source.</span></span> <span data-ttu-id="68a7b-130">Você pode **copiar** o HTML modificado para a área de transferência clicando com o botão direito do mouse no elemento desejado (ou no `html` elemento global, se você quiser a página inteira) para abrir o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="68a7b-130">You can **Copy** your modified HTML to the clipboard by right-clicking the desired element (or the global `html` element, if you want the entire page) to open up the context menu.</span></span> <span data-ttu-id="68a7b-131">(As opções de**recorte** e **colagem** também estão disponíveis).</span><span class="sxs-lookup"><span data-stu-id="68a7b-131">(**Cut** and **Paste** options are also available).</span></span>

<span data-ttu-id="68a7b-132">No painel [estilos](./elements/styles.md) , você também pode adicionar/excluir/Editar pseudoelementos e pseudoelementos CSS.</span><span class="sxs-lookup"><span data-stu-id="68a7b-132">From the [Styles](./elements/styles.md) pane you can also add/delete/edit CSS pseudo-states and pseudo-elements.</span></span>

## <span data-ttu-id="68a7b-133">Painéis de ferramentas</span><span class="sxs-lookup"><span data-stu-id="68a7b-133">Tool Panes</span></span>

<span data-ttu-id="68a7b-134">Depois de selecionar um elemento de página de interesse, você pode usar os painéis de ferramentas para inspecionar ainda mais seus diferentes estilos e propriedades de acessibilidade, exibir seus ouvintes de eventos e definir pontos de interrupção de mutação DOM.</span><span class="sxs-lookup"><span data-stu-id="68a7b-134">Once you have selected a page element of interest, you can use the tool panes to further inspect its different styles and accessibility properties, view its event listeners, and set DOM mutation breakpoints.</span></span>

![Painéis ferramentas no painel elementos](./media/elements_toolpanes.png)

1. <span data-ttu-id="68a7b-136">[**Estilos**](./elements/styles.md): estilos atualmente aplicados organizados por folha de estilos</span><span class="sxs-lookup"><span data-stu-id="68a7b-136">[**Styles**](./elements/styles.md): Currently applied styles organized by stylesheet</span></span>

2. <span data-ttu-id="68a7b-137">[**Calculado**](./elements/computed.md): estilos atualmente aplicados organizados por atributos de CSS</span><span class="sxs-lookup"><span data-stu-id="68a7b-137">[**Computed**](./elements/computed.md): Currently applied styles organized by CSS attributes</span></span>

3. <span data-ttu-id="68a7b-138">[**Eventos**](./elements/events.md): ouvintes de eventos registrados no elemento atual e nos elementos ancestrais</span><span class="sxs-lookup"><span data-stu-id="68a7b-138">[**Events**](./elements/events.md): Event listeners registered on the current element and ancestor elements</span></span>

4. <span data-ttu-id="68a7b-139">[**Pontos**](./elements/dom-breakpoints.md)de interrupção dom: pontos de interrupção de mutação dom</span><span class="sxs-lookup"><span data-stu-id="68a7b-139">[**DOM breakpoints**](./elements/dom-breakpoints.md): DOM Mutation Breakpoints</span></span> 

5. <span data-ttu-id="68a7b-140">[**Fontes**](./elements/fonts.md): fontes aplicadas atualmente para um elemento selecionado</span><span class="sxs-lookup"><span data-stu-id="68a7b-140">[**Fonts**](./elements/fonts.md): Currently applied fonts for a selected element</span></span>

6. <span data-ttu-id="68a7b-141">[**Acessibilidade**](./elements/accessibility.md): Propriedades de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="68a7b-141">[**Accessibility**](./elements/accessibility.md):  Accessibility properties</span></span>

7. <span data-ttu-id="68a7b-142">[**Alterações**](./elements/changes.md): alterações de CSS feitas durante a sessão de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="68a7b-142">[**Changes**](./elements/changes.md): CSS changes made during diagnostic session</span></span>  

## <span data-ttu-id="68a7b-143">Atalhos</span><span class="sxs-lookup"><span data-stu-id="68a7b-143">Shortcuts</span></span>

| <span data-ttu-id="68a7b-144">Ação</span><span class="sxs-lookup"><span data-stu-id="68a7b-144">Action</span></span>               | <span data-ttu-id="68a7b-145">Atalho</span><span class="sxs-lookup"><span data-stu-id="68a7b-145">Shortcut</span></span>               |
|:---------------------|:-----------------------|
| <span data-ttu-id="68a7b-146">Painel elementos</span><span class="sxs-lookup"><span data-stu-id="68a7b-146">Elements panel</span></span>       | `Ctrl` + `1`           |
| <span data-ttu-id="68a7b-147">Realce de elemento</span><span class="sxs-lookup"><span data-stu-id="68a7b-147">Element highlighting</span></span> | `Ctrl` + `Shift` + `L` |
| <span data-ttu-id="68a7b-148">Selecionar elemento</span><span class="sxs-lookup"><span data-stu-id="68a7b-148">Select element</span></span>       | `Ctrl` + `B`           |
| <span data-ttu-id="68a7b-149">Seletor de cor</span><span class="sxs-lookup"><span data-stu-id="68a7b-149">Color picker</span></span>         | `Ctrl` + `K`           |
| <span data-ttu-id="68a7b-150">Árvore de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="68a7b-150">Accessibility tree</span></span>   | `Ctrl` + `Shift` + `A` |
