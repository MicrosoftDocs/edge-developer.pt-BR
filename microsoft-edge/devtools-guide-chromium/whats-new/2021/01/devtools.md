---
description: A ferramenta Novidades agora se chama Bem-Vindo, Editor de Fonte Visual no painel Estilos, ferramentas de depuração do CSS Flexbox e muito mais.
title: Novidades no DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.localizationpriority: high
ms.openlocfilehash: 9eb9f35427829dbe262b4c71d8ff5474b28eae77
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597156"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-89"></a><span data-ttu-id="6a3f1-104">Novidades no DevTools (Microsoft Edge 89)</span><span class="sxs-lookup"><span data-stu-id="6a3f1-104">What's New In DevTools (Microsoft Edge 89)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a><span data-ttu-id="6a3f1-105">A ferramenta Novidades agora chama-se Bem-vindo</span><span class="sxs-lookup"><span data-stu-id="6a3f1-105">What's New is now Welcome</span></span>  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="6a3f1-106">A ferramenta **Novidades** do Microsoft Edge DevTools agora tem uma nova aparência e um novo nome: **Bem-vindo.**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-106">The **What's New** tool in the Microsoft Edge DevTools now has a new appearance and a new name:  **Welcome**.</span></span>  <span data-ttu-id="6a3f1-107">A ferramenta **Bem-vindo** ainda exibe as últimas notícias e atualizações do DevTools.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-107">The **Welcome** tool still displays the latest DevTools news and updates.</span></span>  <span data-ttu-id="6a3f1-108">Agora também inclui links para a documentação do Microsoft Edge DevTools, maneiras de enviar comentários e muito mais.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-108">It now also includes links to Microsoft Edge DevTools documentation, ways to submit feedback, and more.</span></span>  <span data-ttu-id="6a3f1-109">Para exibir a ferramenta **Bem-vindo** após cada atualização para o Microsoft Edge, escolha a caixa de seleção ao lado da **guia Abrir após cada atualização** sob o título.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-109">To display the **Welcome** tool after each update to Microsoft Edge, choose the checkbox next to **Open tab after each update** under the title.</span></span>  <span data-ttu-id="6a3f1-110">Para fechar a ferramenta **Bem-vindo**, escolha o **X** no lado direito do título da guia.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-110">To close the **Welcome** tool, choose the **X** on the right-side of the tab title.</span></span>  <span data-ttu-id="6a3f1-111">Se você preferir a ferramenta original **Novidades,** navegue até [Configurações][DevtoolsCustomizeIndexSettings]  > **Experimentos** e remova o X da caixa de seleção ao lado da **guia Habilitar Bem-vindo.**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-111">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="A ferramenta Bem-vindo é realçada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   <span data-ttu-id="6a3f1-113">A ferramenta **Bem-vindo** é realçada</span><span class="sxs-lookup"><span data-stu-id="6a3f1-113">The **Welcome** tool is highlighted</span></span>  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a><span data-ttu-id="6a3f1-114">Editor de Fonte visual no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="6a3f1-114">Visual Font Editor in the Styles pane</span></span>  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="6a3f1-115">Quando você trabalha com fontes em CSS, use o novo [Editor de Fonte][DevtoolsInspectStylesEditFonts] visual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-115">When you work with fonts in CSS, use the new visual [Font Editor][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="6a3f1-116">Você pode definir fontes de fallback e usar controles deslizantes para definir o peso, o tamanho, a altura da linha e o espaçamento.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-116">You may define fallback fonts, and use sliders to define font weight, size, line-height, and spacing.</span></span>  <span data-ttu-id="6a3f1-117">O **Editor de Fonte** ajuda você a concluir as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-117">The **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="6a3f1-118">Alternar entre unidades para propriedades de fonte diferentes</span><span class="sxs-lookup"><span data-stu-id="6a3f1-118">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="6a3f1-119">Alternar entre palavras-chave para propriedades de fonte diferentes</span><span class="sxs-lookup"><span data-stu-id="6a3f1-119">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="6a3f1-120">Converter unidades</span><span class="sxs-lookup"><span data-stu-id="6a3f1-120">Convert units</span></span>  
*   <span data-ttu-id="6a3f1-121">Gerar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="6a3f1-121">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="6a3f1-122">Para ativar esse experimento, navegue até [Configurações][DevtoolsCustomizeIndexSettings] > **Experimentos** e escolha a caixa de seleção ao lado de **Habilitar as novas ferramentas de Editor de fonte dentro do painel Estilos**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-122">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new Font Editor tools within Styles pane**.</span></span>  <span data-ttu-id="6a3f1-123">Para obter mais informações, navegue até [Editar estilos de fonte CSS e configurações no painel Estilos no DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-123">For more information, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="6a3f1-124">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1093229][CR1093229].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-124">To review the history of this feature in the Chromium open-source project, navigate to Issue [1093229][CR1093229].</span></span>  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="O Editor de fonte visual é realçado no painel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   <span data-ttu-id="6a3f1-126">O **Editor de fonte** visual é realçado no painel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-126">The visual **Font editor** is highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a><span data-ttu-id="6a3f1-127">Ferramentas de depuração do CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="6a3f1-127">CSS Flexbox debugging tools</span></span>  

<span data-ttu-id="6a3f1-128">Os recursos de depuração do Flexbox estão em desenvolvimento ativo.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-128">Flexbox debugging features are in active development.</span></span>  <span data-ttu-id="6a3f1-129">Para ativar o experimento para os dois recursos a seguir, navegue até [Configurações][DevtoolsCustomizeIndexSettings] > **Experimentos**e escolha a caixa de seleção ao lado de **Habilitar novos recursos de depuração do CSS Flexbox.**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-129">To turn on the experiment for the following two features, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new CSS Flexbox debugging features**.</span></span>  <span data-ttu-id="6a3f1-130">Para analisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1136394][CR1136394] e [1139949][CR1139949].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-130">To review the history of this feature in the Chromium open-source project, navigate to Issues [1136394][CR1136394] and [1139949][CR1139949].</span></span>  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a><span data-ttu-id="6a3f1-131">Novo ícone do Flexbox (flex) ajuda a identificar e exibir contêineres flexíveis</span><span class="sxs-lookup"><span data-stu-id="6a3f1-131">New Flexbox (flex) icon helps identify and display flex containers</span></span>  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="6a3f1-132">Na ferramenta **Elementos,** o novo ícone flexbox (flex) ajuda a identificar contêineres do Flexbox em seu código.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-132">In the **Elements** tool, the new Flexbox (flex) icon helps you identify Flexbox containers in your code.</span></span>  <span data-ttu-id="6a3f1-133">Escolha o ícone Flexbox \(flex\) para ativar ou desativar o efeito de sobreposição que descreve um contêiner do Flexbox.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-133">Choose the Flexbox \(flex\) icon to turn on or off the overlay effect that outlines a Flexbox container.</span></span>  <span data-ttu-id="6a3f1-134">Você pode personalizar a cor da sobreposição no painel **Layout,** que está localizado ao lado de **Estilos** e **Calculado**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-134">You may customize the color of the overlay in the **Layout** pane, which is located next to **Styles** and **Computed**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="6a3f1-135">Para ativar e desativar o efeito de sobreposição que descreve o contêiner Flexbox, escolha o ícone Flexbox \( `flex` \).</span><span class="sxs-lookup"><span data-stu-id="6a3f1-135">To turn on and off the overlay effect that outlines the Flexbox container, choose the Flexbox \(`flex`\) icon.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="6a3f1-136">Você pode personalizar a cor da sobreposição no painel **Layout** ao lado de **Estilos** e **Calculado**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-136">You may customize the color of the overlay in the **Layout** pane next to **Styles** and **Computed**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="O ícone e a página da Web do Flexbox (flex) realçados" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         <span data-ttu-id="6a3f1-138">O ícone e a página da Web do **Flexbox** `flex` \( \) realçados</span><span class="sxs-lookup"><span data-stu-id="6a3f1-138">The **Flexbox** \(`flex`\) icon and webpage highlighted</span></span> :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="As sobreposições do Flexbox realçadas no painel Layout" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         <span data-ttu-id="6a3f1-140">As **sobreposições do Flexbox** realçadas no painel **Layout**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-140">The **Flexbox overlays** highlighted in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-visual-guides-when-flexbox-layouts-change-using-css-properties"></a><span data-ttu-id="6a3f1-141">Exibir ícones de alinhamento e guias visuais quando os layouts do Flexbox mudam usando propriedades CSS</span><span class="sxs-lookup"><span data-stu-id="6a3f1-141">Display alignment icons and visual guides when Flexbox layouts change using CSS properties</span></span>  

<!--  Title: Display alignment icons and visual guides for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="6a3f1-142">Quando você edita o CSS para o layout do Flexbox, o preenchimento automático do CSS no painel **Estilos** agora exibe ícones úteis ao lado de propriedades relevantes do Flexbox.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-142">When you edit CSS for your Flexbox layout, CSS autocompletes in the **Styles** pane now displays helpful icons next to relevant Flexbox properties.</span></span>  <span data-ttu-id="6a3f1-143">Para experimentar esse novo recurso, abra a ferramenta **Elementos** e selecione um contêiner flexível.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-143">To try this new feature, open the **Elements** tool and select a flex container.</span></span>  <span data-ttu-id="6a3f1-144">Em seguida, adicione ou altere uma propriedade nesse contêiner no painel **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-144">Then add or change a property on that container in the **Styles** pane.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="6a3f1-145">O menu de preenchimento automático agora exibe ícones que indicam o efeito das propriedades de alinhamento, como `align-content` e `align-items`.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-145">The autocomplete menu now displays icons that indicate the effect of alignment properties such as `align-content` and `align-items`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="6a3f1-146">Além disso, o DevTools agora exibe uma linha de orientação para ajudá-lo a revisar melhor a propriedade CSS `align-items`.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-146">Additionally, DevTools now displays a guiding line to help you better review the `align-items` CSS property.</span></span>  <span data-ttu-id="6a3f1-147">A propriedade CSS `gap` também tem suporte.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-147">The `gap` CSS property is supported as well.</span></span>  <span data-ttu-id="6a3f1-148">Na figura a seguir, a propriedade CSS `gap` é definida como `gap: 12px;` e o padrão de eclosão para cada intervalo é exibido.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-148">In the following figure, the `gap` CSS property is set to `gap: 12px;` and the hatching pattern for each gap is displayed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menu de preenchimento automático realçado para propriedades CSS que começam com alinhamento-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         <span data-ttu-id="6a3f1-150">Menu de preenchimento automático realçado para propriedades CSS que começam com</span><span class="sxs-lookup"><span data-stu-id="6a3f1-150">Autocomplete menu highlighted for CSS properties that start with</span></span> `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Lacuna do Flexbox em propriedades CSS e página da Web realçadas" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         <span data-ttu-id="6a3f1-152">Flexbox `gap` em propriedades CSS e página da Web realçadas</span><span class="sxs-lookup"><span data-stu-id="6a3f1-152">Flexbox `gap` in CSS properties and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a><span data-ttu-id="6a3f1-153">Adicionar ferramentas rapidamente com o novo botão Mais Ferramentas</span><span class="sxs-lookup"><span data-stu-id="6a3f1-153">Add tools quickly with new More Tools button</span></span>  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="6a3f1-154">Agora você tem uma nova maneira de abrir mais ferramentas no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-154">You now have a new way to open more tools in the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="6a3f1-155">Depois de ativar esse experimento, o ícone **Mais Ferramentas** será exibido como um sinal de mais (`+`) à direita do painel principal.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-155">After you turn on this experiment, the **More Tools** icon displays as a plus sign (`+`) to the right of the main panel.</span></span>  <span data-ttu-id="6a3f1-156">Para exibir uma lista de outras ferramentas para adicionar ao painel principal, escolha o ícone **Mais Ferramentas** \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="6a3f1-156">To display a list of other tools to add to the main panel, choose the **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="6a3f1-157">Para ativar esse experimento, navegue até [Configurações][DevtoolsCustomizeIndexSettings]  > **Experimentos** e, em seguida, escolha a caixa de seleção ao lado de **Habilitar + menus de guia para abrir mais ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-157">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**, and then choose the checkbox next to **Enable + button tab menus to open more tools**.</span></span>  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Mais Ferramentas realçado no DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   <span data-ttu-id="6a3f1-159">**Mais Ferramentas** realçado no DevTools</span><span class="sxs-lookup"><span data-stu-id="6a3f1-159">**More Tools** highlighted in DevTools</span></span>  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a><span data-ttu-id="6a3f1-160">Tecnologias assistivas agora anunciam posição e contagem de sugestões CSS</span><span class="sxs-lookup"><span data-stu-id="6a3f1-160">Assistive technologies now announce position and count of CSS suggestions</span></span>  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

<span data-ttu-id="6a3f1-161">Quando você edita CSS, você tem um menu suspenso de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-161">When you edit CSS, you get a dropdown of features.</span></span>  <span data-ttu-id="6a3f1-162">Esse recurso não estava disponível para usuários de tecnologias assistivas, já que ele está anunciado no Microsoft Edge versão 89.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-162">This feature was not available to users of assistive technologies, since it is announced in Microsoft Edge version 89.</span></span>  <span data-ttu-id="6a3f1-163">Um usuário de tecnologias assistivas agora pode navegar por sugestões CSS no painel **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-163">A user of assistive technologies may now navigate CSS suggestions in the **Styles** pane.</span></span>  <span data-ttu-id="6a3f1-164">No Microsoft Edge versão 88 e anterior, a tecnologia assistiva apresentava `Suggestion` à medida que um usuário navegava pela lista de sugestões ao editar CSS no painel **Estilos**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-164">In Microsoft Edge version 88 and earlier, assistive technology announced `Suggestion` as a user navigated through the list of suggestions when editing CSS in the **Styles** pane.</span></span>  <span data-ttu-id="6a3f1-165">No Microsoft Edge versão 89, um usuário de tecnologia assistida agora ouve a posição e a contagem da sugestão atual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-165">In Microsoft Edge version 89, a user of assistive technology now hears the position and count of the current suggestion.</span></span>  <span data-ttu-id="6a3f1-166">Cada sugestão é anunciada à medida que o usuário navega pela lista de sugestões, como a Sugestão 3 de 5.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-166">Each suggestion is announced as the user navigates through the list of suggestions, such as Suggestion 3 of 5.</span></span>  <span data-ttu-id="6a3f1-167">Para saber mais sobre como escrever CSS no DevTools, navegue até [Alterar CSS][DevtoolsCssReferenceChangeCss].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-167">To learn more about writing CSS in the DevTools, navigate to [Change CSS][DevtoolsCssReferenceChangeCss].</span></span>  <span data-ttu-id="6a3f1-168">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1157329][CR1157329].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-168">To review the history of this feature in the Chromium open-source project, navigate to Issue [1157329][CR1157329].</span></span>  

<span data-ttu-id="6a3f1-169">Para exibir um vídeo que exibe e lê em voz alta várias sugestões com esse experimento ativado, navegue até [Voiceover anunciando opções de devtools](https://youtu.be/9TcUpleEwwA) no YouTube.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-169">To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.</span></span>  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="A sugestão realçada no painel Estilos" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   <span data-ttu-id="6a3f1-171">A lista `suggestion` realçada no painel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-171">The `suggestion` list highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a><span data-ttu-id="6a3f1-172">Emular o Surface Duo e o Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="6a3f1-172">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

<span data-ttu-id="6a3f1-173">Teste a aparência do seu site ou aplicativo nos seguintes dispositivos no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-173">Test the appearance of your website or app on the following devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="6a3f1-174">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="6a3f1-174">Surface Duo</span></span>][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [<span data-ttu-id="6a3f1-175">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="6a3f1-175">Samsung Galaxy Fold</span></span>][SamsungUsMobileGalaxyFold]  
    
<span data-ttu-id="6a3f1-176">Ative os **recursos da Plataforma Web Experimental** para acessar o novo [recurso de abrangência de tela de mídia CSS][DualScreenWebCssMediaSpanning] e [a API JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-176">Turn on **Experimental Web Platform features** to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [getWindowSegments JavaScript API][DualScreenWebJavascriptGetwindowsegments].</span></span>  <span data-ttu-id="6a3f1-177">Navegue até `edge://flags` e alterne o sinalizador ao lado dos recursos para **recursos da Plataforma Web Experimental**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-177">Navigate to `edge://flags` and toggle the flag next to **Experimental Web Platform features**.</span></span>  <span data-ttu-id="6a3f1-178">Para ajudar a aprimorar seu site ou aplicativo para dispositivos de tela dupla e dobráveis, use os seguintes recursos ao [emular o dispositivo][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-178">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="6a3f1-179">[Abrangência][DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices], que é quando seu site \(ou app\) aparece em ambas as telas.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>  
*   <span data-ttu-id="6a3f1-180">[Renderização da junção][DualScreenIntroductionHowToWorkWithSeam], que é o espaço entre as duas telas.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-180">[Rendering the seam][DualScreenIntroductionHowToWorkWithSeam], which is the space between the two screens.</span></span>  
    
<span data-ttu-id="6a3f1-181">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1054281][CR1054281].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-181">To review the history of this feature in the Chromium open-source project, navigate to Issue [1054281][CR1054281].</span></span>  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular tela dupla" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   <span data-ttu-id="6a3f1-183">Emular tela dupla</span><span class="sxs-lookup"><span data-stu-id="6a3f1-183">Emulate dual-screen</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a><span data-ttu-id="6a3f1-184">O Microsoft Edge Developer Tools para o Visual Studio Code versão 1.1.2</span><span class="sxs-lookup"><span data-stu-id="6a3f1-184">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2</span></span>  

<span data-ttu-id="6a3f1-185">O [Microsoft Edge Developer Tools para o Visual Studio Code ][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extensão versão 1.1.2 para Microsoft Visual Studio Code tem as seguintes alterações desde a versão anterior.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-185">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="6a3f1-186">O Microsoft Visual Studio Code atualiza as extensões automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-186">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="6a3f1-187">Para atualizar manualmente para a versão 1.1.2, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="6a3f1-187">To manually update to version 1.1.2, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

*   <span data-ttu-id="6a3f1-188">Adicionado um botão **Fechar instância** a cada item na lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span><span class="sxs-lookup"><span data-stu-id="6a3f1-188">Added a **Close instance** button to each item on the target list \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span></span>  
*   <span data-ttu-id="6a3f1-189">Modificada versão [Microsoft Edge DevTools][DevtoolsIndex] de 84.0.522.63 para [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span><span class="sxs-lookup"><span data-stu-id="6a3f1-189">Bumped [Microsoft Edge DevTools][DevtoolsIndex] version from 84.0.522.63 to [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span></span>  
*   <span data-ttu-id="6a3f1-190">Incluído [Depurador para o Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como uma dependência \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span><span class="sxs-lookup"><span data-stu-id="6a3f1-190">Included [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] as a dependency  \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span></span>  
*   <span data-ttu-id="6a3f1-191">Opção de configurações implementadas para alterar temas de extensão \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span><span class="sxs-lookup"><span data-stu-id="6a3f1-191">Implemented settings option to change extension themes \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span></span>  
    
<span data-ttu-id="6a3f1-192">Você pode registrar problemas e contribuir para a extensão no [repositório do GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-192">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="6a3f1-193">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="6a3f1-193">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a><span data-ttu-id="6a3f1-194">Captura de tela do nó de captura além do visor</span><span class="sxs-lookup"><span data-stu-id="6a3f1-194">Capture node screenshot beyond viewport</span></span>  

<span data-ttu-id="6a3f1-195">No Microsoft Edge versão 89, as capturas de tela do nó são mais precisas, capturando o nó completo, mesmo que o conteúdo do nó não seja visível no visor.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-195">In Microsoft Edge version 89, node screenshots are more accurate, capturing the full node even if content from the node is not visible in the viewport.</span></span>  <span data-ttu-id="6a3f1-196">Na ferramenta **Elementos,** passe o mouse em um elemento, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Captura de tela do nó**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-196">In the **Elements** tool, hover  on an element, open the contextual menu \(right-click\), and choose **Capture node screenshot**.</span></span>  <span data-ttu-id="6a3f1-197">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1003629][CR1003629].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-197">To review the history of this feature in the Chromium open-source project, navigate to Issue [1003629][CR1003629].</span></span>  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de tela do nó realçada no menu de contexto na ferramenta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   <span data-ttu-id="6a3f1-199">**Captura de tela do nó** realçada no menu de contexto na ferramenta **Elementos**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-199">**Capture node screenshot** highlighted on the context menu in the **Elements** tool</span></span>  
:::image-end:::  

### <a name="elements-tool-updates"></a><span data-ttu-id="6a3f1-200">Atualizações da ferramenta Elementos</span><span class="sxs-lookup"><span data-stu-id="6a3f1-200">Elements tool updates</span></span>  

#### <a name="support-forcing-the-target-css-state"></a><span data-ttu-id="6a3f1-201">Suporte forçando o estado CSS :target</span><span class="sxs-lookup"><span data-stu-id="6a3f1-201">Support forcing the :target CSS state</span></span>  

<span data-ttu-id="6a3f1-202">Você pode agora usar o DevTools para forçar a pseudo-classe CSS [:target][MdnDocsWebCssTarget].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-202">You may now use DevTools to force the [:target][MdnDocsWebCssTarget] CSS pseudo-class.</span></span>  <span data-ttu-id="6a3f1-203">A pseudo-classe `:target` é disparada quando um elemento exclusivo \(o elemento alvo\) tem um `id` que corresponde a um fragmento da URL.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-203">The `:target` pseudo-class is triggered when a unique element \(the target element\) has an `id` that matches a fragment of the URL.</span></span>  <span data-ttu-id="6a3f1-204">Por exemplo, a URL `http://www.example.com/index.html#section1` dispara a pseudo-classe `:target` em um elemento HTML com `id="section1"`.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-204">For example, the `http://www.example.com/index.html#section1` URL triggers the `:target` pseudo-class on an HTML element with `id="section1"`.</span></span>  <span data-ttu-id="6a3f1-205">Para experimentar uma demonstração com a seção 1 realçada, navegue até [demonstração do CSS :target][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-205">To try a demo with section 1 highlighted, navigate to [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span></span>  <span data-ttu-id="6a3f1-206">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1156628][CR1156628].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-206">To review the history of this feature in the Chromium open-source project, navigate to Issue [1156628][CR1156628].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="A página da Web realçada sem CSS forçado" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         <span data-ttu-id="6a3f1-208">Página da Web realçada sem CSS forçado</span><span class="sxs-lookup"><span data-stu-id="6a3f1-208">Webpage highlighted with no forced CSS</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text="CSS :target forçado e página da Web realçada" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` <span data-ttu-id="6a3f1-210">CSS forçado e página da Web realçada</span><span class="sxs-lookup"><span data-stu-id="6a3f1-210">CSS forced and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a><span data-ttu-id="6a3f1-211">Usar Duplicar elemenos para copiar elementos</span><span class="sxs-lookup"><span data-stu-id="6a3f1-211">Use Duplicate elements to copy elements</span></span>  

<span data-ttu-id="6a3f1-212">Use o novo atalho **Duplicar elemento** para clonar um elemento.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-212">Use the new **Duplicate element** shortcut to clone an element.</span></span>  <span data-ttu-id="6a3f1-213">Na ferramenta **Elementos**, passe o mouse em um elemento, abra o menu contextual \(clique com o botão direito do mouse\), escolha **Duplicar elemento**. </span><span class="sxs-lookup"><span data-stu-id="6a3f1-213">In the **Elements** tool, hover on an element, open the contextual menu \(right-click\), choose **Duplicate element**.</span></span>  <span data-ttu-id="6a3f1-214">Um novo elemento é criado sob o elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-214">A new element is created under the selected element.</span></span>  <span data-ttu-id="6a3f1-215">Para duplicar o elemento com um atalho de teclado, selecione `Shift` +`Alt`+`Down Arrow` \(Windows/Linux\) ou `Shift`+`Option`+`Down Arrow` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="6a3f1-215">To duplicate the element with a keyboard shortcut, select `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) or `Shift`+`Option`+`Down Arrow` \(macOS\).</span></span>  <span data-ttu-id="6a3f1-216">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1150797][CR1150797].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-216">To review the history of this feature in the Chromium open-source project, navigate to Issue [1150797][CR1150797].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="A opção Duplicar elemento é realçada no menu de contexto em um elemento na ferramenta Elementos" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   <span data-ttu-id="6a3f1-218">A opção **Duplicar elemento** é realçada no menu de contexto em um elemento na ferramenta **Elements**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-218">The **Duplicate element** is highlighted in the context menu on an element in the **Elements** tool</span></span>  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a><span data-ttu-id="6a3f1-219">Seletores de cores para propriedades CSS personalizadas</span><span class="sxs-lookup"><span data-stu-id="6a3f1-219">Color pickers for custom CSS properties</span></span>  

<span data-ttu-id="6a3f1-220">O painel **Estilos** agora exibe seletores de cores para propriedades CSS personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-220">The **Styles** pane now displays color pickers for custom CSS properties.</span></span>  <span data-ttu-id="6a3f1-221">Para passar pelos formatos RGBA, HSLA e Hex do valor de cor, segure `Shift` e escolha o seletor de cor.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-221">To cycle through the RGBA, HSLA, and Hex formats of the color value, hold `Shift` and choose the color picker.</span></span>  <span data-ttu-id="6a3f1-222">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1147016][CR1147016].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-222">To review the history of this feature in the Chromium open-source project, navigate to Issue [1147016][CR1147016].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Seletores de cores para propriedades CSS personalizadas" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   <span data-ttu-id="6a3f1-224">Seletores de cores para propriedades CSS personalizadas</span><span class="sxs-lookup"><span data-stu-id="6a3f1-224">Color pickers for custom CSS properties</span></span>  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a><span data-ttu-id="6a3f1-225">Copiar classes e propriedades CSS</span><span class="sxs-lookup"><span data-stu-id="6a3f1-225">Copy CSS classes and properties</span></span>  

<span data-ttu-id="6a3f1-226">Agora você pode copiar as propriedades CSS mais rapidamente com algumas novas opções no menu contextual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-226">You may now copy CSS properties quicker with a few new options in the contextual menu.</span></span>  <span data-ttu-id="6a3f1-227">Na ferramenta **Elementos,** escolha um elemento.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-227">In the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="6a3f1-228">Para copiar o valor, no painel **Estilos,** passe o mouse em uma classe CSS ou em uma propriedade CSS, abra um menu contextual \(clique com o botão direito do mouse\) e escolha a opção de cópia.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-228">To copy the value, in the **Styles** pane, hover on a CSS class or a CSS property, open a contextual menu \(right-click\), and choose the copy option.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="6a3f1-229">Opções de cópia para uma classe CSS.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-229">Copy options for a CSS class.</span></span>  
      
      | <span data-ttu-id="6a3f1-230">Opção</span><span class="sxs-lookup"><span data-stu-id="6a3f1-230">Option</span></span> | <span data-ttu-id="6a3f1-231">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6a3f1-231">Details</span></span> |  
      |:--- |:--- |  
      | **<span data-ttu-id="6a3f1-232">Copiar seletor</span><span class="sxs-lookup"><span data-stu-id="6a3f1-232">Copy selector</span></span>** | <span data-ttu-id="6a3f1-233">Copiar o nome do seletor atual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-233">Copy the current selector name.</span></span> |  
      | **<span data-ttu-id="6a3f1-234">Copiar regra</span><span class="sxs-lookup"><span data-stu-id="6a3f1-234">Copy rule</span></span>** | <span data-ttu-id="6a3f1-235">Copie a regra do seletor atual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-235">Copy the rule of the current selector.</span></span> |  
      | **<span data-ttu-id="6a3f1-236">Copiar todas as declarações</span><span class="sxs-lookup"><span data-stu-id="6a3f1-236">Copy all declarations</span></span>** | <span data-ttu-id="6a3f1-237">Copiar todas as declarações sob a regra atual, incluindo propriedades não válidas e prefixadas.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-237">Copy all declarations under the current rule, including non-valid and prefixed properties.</span></span> |  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="6a3f1-238">Opções de cópia para uma propriedade CSS.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-238">Copy options for a CSS property.</span></span>  
      
      | <span data-ttu-id="6a3f1-239">Opção</span><span class="sxs-lookup"><span data-stu-id="6a3f1-239">Option</span></span> | <span data-ttu-id="6a3f1-240">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6a3f1-240">Details</span></span> |      
      |:--- |:--- |  
      | **<span data-ttu-id="6a3f1-241">Copiar declaração</span><span class="sxs-lookup"><span data-stu-id="6a3f1-241">Copy declaration</span></span>** | <span data-ttu-id="6a3f1-242">Copiar a declaração da linha atual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-242">Copy the declaration of the current line.</span></span> |  
      | **<span data-ttu-id="6a3f1-243">Copiar propriedade</span><span class="sxs-lookup"><span data-stu-id="6a3f1-243">Copy property</span></span>** | <span data-ttu-id="6a3f1-244">Copiar a propriedade da linha atual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-244">Copy the property of the current line.</span></span> |  
      | **<span data-ttu-id="6a3f1-245">Copiar valor</span><span class="sxs-lookup"><span data-stu-id="6a3f1-245">Copy value</span></span>** | <span data-ttu-id="6a3f1-246">Copiar o valor da linha atual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-246">Copy the value of the current line.</span></span> |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Opções de cópia para uma classe CSS no menu contextual" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         <span data-ttu-id="6a3f1-248">Opções de cópia para uma classe CSS no menu contextual</span><span class="sxs-lookup"><span data-stu-id="6a3f1-248">Copy options for a CSS class in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Opções de cópia de uma propriedade CSS no menu contextual" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         <span data-ttu-id="6a3f1-250">Opções de cópia de uma propriedade CSS no menu contextual</span><span class="sxs-lookup"><span data-stu-id="6a3f1-250">Copy options for a CSS property in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="6a3f1-251">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1152391][CR1152391].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-251">To review the history of this feature in the Chromium open-source project, navigate to Issue [1152391][CR1152391].</span></span>  

### <a name="cookies-updates"></a><span data-ttu-id="6a3f1-252">Atualizações de cookies</span><span class="sxs-lookup"><span data-stu-id="6a3f1-252">Cookies updates</span></span>  

#### <a name="new-option-to-display-url-decoded-cookies"></a><span data-ttu-id="6a3f1-253">Nova opção para exibir cookies decodificados por URL</span><span class="sxs-lookup"><span data-stu-id="6a3f1-253">New option to display URL-decoded cookies</span></span>  

<span data-ttu-id="6a3f1-254">Agora, você pode optar por exibir o valor de cookies decodificados por URL no painel **Cookies.**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-254">You may now opt to display the URL-decoded cookies value in the **Cookies** pane.</span></span>  <span data-ttu-id="6a3f1-255">Para exibir o cookie decodificado, navegue até **Aplicativo** >  painel **Cookies**, escolha qualquer cookie na lista e marque a caixa de seleção ao lado de **Mostrar URL decodificada**. </span><span class="sxs-lookup"><span data-stu-id="6a3f1-255">To display the decoded cookie, navigate to **Application** > **Cookies** pane, choose any cookie on the list, and choose the checkbox next to **Show URL decoded**.</span></span>  <span data-ttu-id="6a3f1-256">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [997625][CR997625].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-256">To review the history of this feature in the Chromium open-source project, navigate to Issue [997625][CR997625].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opção para exibir cookies decodificados por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   <span data-ttu-id="6a3f1-258">Opção para exibir cookies decodificados de URL</span><span class="sxs-lookup"><span data-stu-id="6a3f1-258">Option to display URL decoded cookies</span></span>  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a><span data-ttu-id="6a3f1-259">Filtrar e limpar cookies visíveis</span><span class="sxs-lookup"><span data-stu-id="6a3f1-259">Filter and clear visible cookies</span></span>  

<span data-ttu-id="6a3f1-260">Na versão 88 ou anterior do Microsoft Edge, a ferramenta **Application** fornecia apenas uma maneira de limpar todos os cookies com o botão **Limpar todos os cookies**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-260">In Microsoft Edge version 88 or earlier, the **Application** tool only provided a way to clear all cookies with the **Clear all cookies** button.</span></span>  <span data-ttu-id="6a3f1-261">Na versão 89 do Microsoft Edge, agora você pode escolher **Limpar cookies filtrados** para excluir somente os cookies filtrados.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-261">In Microsoft Edge version 89, you may now choose **Clear filtered cookies** to delete only the filtered cookies.</span></span>  <span data-ttu-id="6a3f1-262">Para filtrar cookies, navegue até **Aplicativo** > **Cookies** e digite na caixa de texto **Filtrar**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-262">To filter cookies, navigate to **Application** > **Cookies**, and type in the **Filter** textbox.</span></span>  <span data-ttu-id="6a3f1-263">Para excluir os cookies exibidos, escolha o botão **Limpar cookies filtrados**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-263">To delete the displayed cookies, choose the **Clear filtered cookies** button.</span></span>  <span data-ttu-id="6a3f1-264">Para exibir todos os outros cookies, limpe o texto do filtro.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-264">To display all other cookies, clear the filter text.</span></span>  <span data-ttu-id="6a3f1-265">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [978059][CR978059].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-265">To review the history of this feature in the Chromium open-source project, navigate to Issue [978059][CR978059].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Limpar somente os cookies visíveis" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   <span data-ttu-id="6a3f1-267">Limpar somente os cookies visíveis</span><span class="sxs-lookup"><span data-stu-id="6a3f1-267">Clear only visible cookies</span></span>  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a><span data-ttu-id="6a3f1-268">Nova opção para limpar cookies de terceiros no painel Armazenamento</span><span class="sxs-lookup"><span data-stu-id="6a3f1-268">New option to clear third-party cookies in the Storage pane</span></span>  

<span data-ttu-id="6a3f1-269">Agora, o DevTools limpa apenas cookies de terceiros por padrão.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-269">DevTools now clear only first-party cookies by default.</span></span>  <span data-ttu-id="6a3f1-270">Para limpar somente os dados do site e os cookies de terceiros, navegue até **Aplicativo** > **Armazenamento**e escolha **Limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-270">To clear website data and first-party cookies only, navigate to **Application** > **Storage**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="6a3f1-271">Para limpar os dados do site e todos os cookies, navegue até **Aplicativo** > **Armazenamento**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-271">To clear website data and all cookies, navigate to **Application** > **Storage**.</span></span>  <span data-ttu-id="6a3f1-272">Marque a caixa de seleção ao lado de **incluir cookies de terceiros**e escolha **Limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-272">Choose the checkbox next to **including third-party cookies**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="6a3f1-273">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1012337][CR1012337].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1012337][CR1012337].</span></span>  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opção para limpar cookies de terceiros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   <span data-ttu-id="6a3f1-275">Opção para limpar cookies de terceiros</span><span class="sxs-lookup"><span data-stu-id="6a3f1-275">Option to clear third-party cookies</span></span>  
:::image-end:::  

### <a name="network-tool-updates"></a><span data-ttu-id="6a3f1-276">Atualizações da ferramenta de rede</span><span class="sxs-lookup"><span data-stu-id="6a3f1-276">Network tool updates</span></span>  

#### <a name="persist-record-network-log-setting"></a><span data-ttu-id="6a3f1-277">Mantida a Configuração de Registro de log de rede </span><span class="sxs-lookup"><span data-stu-id="6a3f1-277">Persist Record network log setting</span></span>  

<span data-ttu-id="6a3f1-278">Na versão 88 ou anterior do Microsoft Edge, o DevTools redefinia a configuração **Registro de log de rede** quando uma página da Web era atualizada.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-278">In Microsoft Edge version 88 or earlier, DevTools reset the **Record network log** setting when a webpage refreshes.</span></span>  <span data-ttu-id="6a3f1-279">Na versão 89 do Microsoft Edge, o DevTools agora mantem a configuração **Registro de log de rede**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-279">In Microsoft Edge version 89, DevTools now persist the **Record network log** setting.</span></span>  <span data-ttu-id="6a3f1-280">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1122580][CR1122580].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122580][CR1122580].</span></span>  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registrar log de rede" lightbox="../../media/2021/01/network-log.msft.png":::
   <span data-ttu-id="6a3f1-282">Registrar log de rede</span><span class="sxs-lookup"><span data-stu-id="6a3f1-282">Record network log</span></span>  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a><span data-ttu-id="6a3f1-283">A opção Online agora chama-se Sem Limitação (No throttling)</span><span class="sxs-lookup"><span data-stu-id="6a3f1-283">Online option is now No throttling option</span></span>  

<span data-ttu-id="6a3f1-284">A opção de emulação de rede **Online** foi renomeada para **Sem Limitação**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-284">The network emulation option **Online** is now renamed to **No Throttling**.</span></span>  <span data-ttu-id="6a3f1-285">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1028078][CR1028078].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-285">To review the history of this feature in the Chromium open-source project, navigate to Issue [1028078][CR1028078].</span></span>  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Opção Sem limitação" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   <span data-ttu-id="6a3f1-287">Opção **Sem limitação** </span><span class="sxs-lookup"><span data-stu-id="6a3f1-287">**No throttling** option</span></span>  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a><span data-ttu-id="6a3f1-288">Novas opções de cópia na ferramenta Console, ferramenta Fontes e no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="6a3f1-288">New copy options in the Console tool, Sources tool, and Styles pane</span></span>

#### <a name="copy-object-in-the-console-and-sources-tool"></a><span data-ttu-id="6a3f1-289">Copiar objeto nas ferramentas Console e Fontes</span><span class="sxs-lookup"><span data-stu-id="6a3f1-289">Copy object in the Console and Sources tool</span></span>  

<span data-ttu-id="6a3f1-290">Agora você pode copiar valores de objeto nas ferramentas **Console** e **Fontes**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-290">You may now copy object values in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="6a3f1-291">A capacidade de copiar valores de objetos é útil ao trabalhar com objetos grandes.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-291">The ability to copy object values is useful when working with large objects.</span></span>  <span data-ttu-id="6a3f1-292">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até os Problemas [1148353][CR1148353]e [1149859][CR1149859].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-292">To review the history of this feature in the Chromium open-source project, navigate to Issues [1148353][CR1148353] and [1149859][CR1149859].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="6a3f1-293">Na ferramenta **Console**, passe o mouse sobre um objeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar objeto**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-293">In the **Console** tool, hover on an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="6a3f1-294">Na ferramenta**Fontes**, em um ponto de interrupção, passe o mouse sobre um objeto, na janela pop-up **Objeto**, realce um objeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar objeto**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-294">In the **Sources** tool, on a breakpoint, hover on an object, in the **Object** popup window, highlight an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copiar objeto no Console" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         <span data-ttu-id="6a3f1-296">Copiar objeto no **Console**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-296">Copy object in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copiar objeto em Fontes" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         <span data-ttu-id="6a3f1-298">Copiar objeto em **Fontes**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-298">Copy object in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a><span data-ttu-id="6a3f1-299">Copiar o nome do arquivo na ferramenta Fontes e no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="6a3f1-299">Copy file name in the Sources tool and Styles pane</span></span>  

<span data-ttu-id="6a3f1-300">Agora você pode copiar um nome de arquivo usando o menu contextual.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-300">You may now copy a file name using the contextual menu.</span></span>  <span data-ttu-id="6a3f1-301">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1155120][CR1155120].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-301">To review the history of this feature in the Chromium open-source project, navigate to Issues [1155120][CR1155120].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="6a3f1-302">Na ferramenta **Fontes**, passe o mouse sobre um nome de arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar nome do arquivo**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-302">In the **Sources** tool, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="6a3f1-303">Na ferramenta **Elementos** > painel **Estilos**, passe o mouse sobre um nome de arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar nome do arquivo**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-303">In the **Elements** tool > **Styles** pane, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar nome do arquivo em Fontes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         <span data-ttu-id="6a3f1-305">Copiar nome do arquivo em **Fontes**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-305">Copy file name in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar nome do arquivo no painel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         <span data-ttu-id="6a3f1-307">Copiar nome do arquivo no painel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-307">Copy file name in **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a><span data-ttu-id="6a3f1-308">Atualizações nos detalhes de Quadro</span><span class="sxs-lookup"><span data-stu-id="6a3f1-308">Updates to Frame details</span></span>  

#### <a name="service-workers-information-in-frame-details"></a><span data-ttu-id="6a3f1-309">Informações dos Trabalhos de Serviço nos detalhes de Quadro</span><span class="sxs-lookup"><span data-stu-id="6a3f1-309">Service Workers information in Frame details</span></span>  

<span data-ttu-id="6a3f1-310">O DevTools agora lista um trabalho de serviço dedicado sob o quadro pai.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-310">DevTools now lists a dedicated service worker under the parent frame.</span></span>  <span data-ttu-id="6a3f1-311">Na figura a seguir, são exibidos os detalhes do trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-311">In the following figure, service worker details are displayed.</span></span>  <span data-ttu-id="6a3f1-312">Para exibir os detalhes do trabalho de serviço navegue até **Aplicativo** > **Quadros** > `top` > **Trabalhos de serviços** e escolha um trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-312">To display the service worker details, navigate to **Application** > **Frames** > `top` > **Service Workers** and then choose a service worker.</span></span>  <span data-ttu-id="6a3f1-313">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1122507][CR1122507].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-313">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122507][CR1122507].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Informações dos Trabalhos de serviço nos detalhes de Quadros" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   <span data-ttu-id="6a3f1-315">Informações dos **Trabalhos de Serviço** nos detalhes de **Quadros**</span><span class="sxs-lookup"><span data-stu-id="6a3f1-315">**Service Workers** information in the **Frames** details</span></span>  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a><span data-ttu-id="6a3f1-316">Medir informações de memória nos detalhes de Quadro</span><span class="sxs-lookup"><span data-stu-id="6a3f1-316">Measure Memory information in Frame details</span></span>  

<span data-ttu-id="6a3f1-317">O status `performance.measureMemory()` da API agora é exibido na seção **disponibilidade de API**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-317">The `performance.measureMemory()` API status is now displayed under the **API availability** section.</span></span>  <span data-ttu-id="6a3f1-318">A nova `performance.measureMemory()` da API estima o uso da memória de toda a página da Web.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-318">The new `performance.measureMemory()` API estimates the memory usage of the entire webpage.</span></span>  <span data-ttu-id="6a3f1-319">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema[1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-319">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir memória" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   <span data-ttu-id="6a3f1-321">Medir memória</span><span class="sxs-lookup"><span data-stu-id="6a3f1-321">Measure Memory</span></span>  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a><span data-ttu-id="6a3f1-322">Quadros descartados na ferramenta Desempenho</span><span class="sxs-lookup"><span data-stu-id="6a3f1-322">Dropped frames in the Performance tool</span></span>  

<span data-ttu-id="6a3f1-323">Quando você [analisa o desempenho da carga na ferramenta Desempenho][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], a seção **Quadros** agora marca quadros descartados como vermelhos.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-323">When you [analyze load performance in the Performance tool][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], the **Frames** section now marks dropped frames as red.</span></span>  <span data-ttu-id="6a3f1-324">Para exibir a taxa de quadros, passe o mouse sobre um quadro descartado.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-324">To display the frame rate, hover on a dropped frame.</span></span>  <span data-ttu-id="6a3f1-325">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até Problema[1075865][CR1075865].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-325">To review the history of this feature in the Chromium open-source project, navigate to Issue [1075865][CR1075865].</span></span>  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Quadros descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   <span data-ttu-id="6a3f1-327">Quadros descartados</span><span class="sxs-lookup"><span data-stu-id="6a3f1-327">Dropped frames</span></span>  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a><span data-ttu-id="6a3f1-328">Novo cálculo de contraste de cor - Algoritmo Avançado de Percepção de Contraste (APCA)</span><span class="sxs-lookup"><span data-stu-id="6a3f1-328">New color contrast calculation - Advanced Perceptual Contrast Algorithm (APCA)</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="6a3f1-329">O [Algoritmo Avançado de Percepção de Contraste (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] substitui as diretrizes [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] de índice de contraste no [Seletor de Cor][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-329">The [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] replaces the [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] guidelines contrast ratio in the [Color Picker][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span></span>  <span data-ttu-id="6a3f1-330">O APCA é uma nova maneira de calcular o contraste.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-330">APCA is a new way to compute contrast.</span></span>  <span data-ttu-id="6a3f1-331">Ele se baseia na pesquisa moderna sobre a percepção de cores.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-331">It is based on modern research on color perception.</span></span>  <span data-ttu-id="6a3f1-332">Comparada com as diretrizes de AA/AAA, a APCA depende mais do contexto.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-332">Compared to AA/AAA guidelines, APCA is more context-dependent.</span></span>  <span data-ttu-id="6a3f1-333">O contraste é calculado com base nas seguintes propriedades do texto, cor e contexto.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-333">The contrast is calculated based on the following spatial properties of the text, color, and context.</span></span>  

*   <span data-ttu-id="6a3f1-334">Propriedades da fonte do texto que incluem a peso e o tamanho da fonte.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-334">Spatial properties of text that include font weight and size.</span></span>  
*   <span data-ttu-id="6a3f1-335">Propriedades da cor que incluem o contraste percebido entre o texto e o plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-335">Spatial properties of color that include perceived contrast between text and background.</span></span>  
*   <span data-ttu-id="6a3f1-336">Propriedades do contexto que incluem luz ambiente, arredores e objetivo pretendido.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-336">Spatial properties of context that include ambient light, surroundings, and intended purpose.</span></span>  
    
<span data-ttu-id="6a3f1-337">Para ativar esse experimento, navegue até [Configurações][DevtoolsCustomizeIndexSettings] > **Experimentos** e marque a caixa de seleção ao lado de **Habilitar o novo APCA (Algoritmo Avançado de Percepção  Contraste), substituindo a taxa de contraste anterior e as diretrizes de AA/AAA**.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-337">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable new Advanced Perceptual Contrast Algorithm (APCA) replacing previous contrast ratio and AA/AAA guidelines**.</span></span>  <span data-ttu-id="6a3f1-338">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1121900][CR1121900].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-338">To review the history of this feature in the Chromium open-source project, navigate to Issue [1121900][CR1121900].</span></span>  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA no Seletor de Cor" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   <span data-ttu-id="6a3f1-340">APCA no Seletor de Cor</span><span class="sxs-lookup"><span data-stu-id="6a3f1-340">APCA in the Color Picker</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="6a3f1-341">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6a3f1-341">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="6a3f1-342">Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-342">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="6a3f1-343">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="6a3f1-343">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="6a3f1-344">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6a3f1-344">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: ../../../accessibility/color-picker.md "Teste o contraste da cor do texto usando o Seletor de Cor | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: ../../../css/reference.md#change-css "Alterar CSS - Referência de CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalizar atalhos de teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices]: ../../../device-mode/dual-screen-and-foldables.md#test-on-foldable-and-dual-screen-devices "Teste em dispositivos dobáveis e de tela dupla : emular dispositivos de duas telas e dobáveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular visor móvel – Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: ../../../evaluate-performance/reference.md#record-load-performance "Registrar desempenho de carga - Referência de análise de desempenho | Microsoft Docs"  
[DevtoolsIndex]: ../../../index.md "Visão geral das Ferramentas para Desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: ../../../inspect-styles/edit-fonts.md "Editar configurações e estilos de fonte CSS no painel Estilos no DevTools | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a junção – Introdução aos dispositivos de duas telas | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Recurso de abrangência de tela de mídia CSS para detecção de dualidade de tela | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de duas telas | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Seção 1 - demonstração do CSS :target para Novidades do DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: implementando o menu suspenso em configurações para alterar os temas | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: incluindo o Depurador do Microsoft Edge como uma dependência| GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: atualizando a versão do Microsoft Edge DevTools para 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Adicionar botões de fechamento único ao painel de instâncias | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Selecione as características da fonte e as cores de plano de fundo para fornecer contraste suficiente para facilitar a leitura | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos Confiáveis | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Novo Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Marketplace de Extensões | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador do Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs do Chromium"  
[CR978059]: https://crbug.com/978059 "Problema 978059: excluindo cookies durante a filtragem deles, excluir todos os cookies e não apenas os filtrados | Bugs do Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: solicitação de novo recurso | é necessária uma opção para ver o valor de URL decodificado nos cookies | Bugs do Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problema 1003629: recurso Capturar Nó não faz mais a captura de tela do nó abaixo da dobra. | Bugs do Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problema 1012337: recurso Limpar os dados do site destruirá a sessão do Google em sites que não são do Google | Bugs do Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problema 1028078: colocar Online e Offline próximos um do outro na lista | Bugs do Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: solicitação de recurso: o DevTools deve emular dispositivos dobráveis e de duas telas | Bugs do Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problema 1075865: mostrar quadros descartados na linha do tempo do Devtools | Bugs do Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: oferecer uma interface de usuário de editor de face de tipos especializada | Bugs do Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: atualizar lógica de cálculo de contraste por nova especificação | Bugs do Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: informações sobre o worker do Surface no modo de exibição árvore de quadros | Bugs do Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problema 1122580: é impossível desabilitar a gravação de rede ao recarregar | Bugs do Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: ferramentas Flexbox | Bugs de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: relatar a disponibilidade da API restringida na exibição de detalhes do quadro | Erros do Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: sobreposição de Flexbox | Bugs do Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problema 1147016: o seletor de cor não é exibido na função var(). | Bugs do Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problema 1148353: solicitação de recurso: copiar objeto do console do Devtools | Bugs do Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitação de recurso][Console] adicionar copiar objeto ao item da área de transferência no menu contextual | Bugs do Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problema 1150797: adicionar Duplicar elemento ao menu contextual no painel Elemento | Bugs do Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problema 1152391: suporte para copiar o menu de contexto CSS no painel estilos | Bugs do Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Suporte para copiar nome do arquivo e número de linha | Bugs do Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: adicionar suporte ao elemento :target no recurso forçar estado do elemento | Bugs do Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Acessibilidade – Narrador: o Narrador não está anunciando a contagem e a posição para sugestões de código disponíveis na guia Estilos | Bugs do Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (aprimorado) - Como atender a WCAG (Referência Rápida) | W3c"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (mínimo) - Como atender a WCAG (Referência Rápida) | W3c"  

> [!NOTE]
> <span data-ttu-id="6a3f1-399">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-399">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6a3f1-400">A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-89) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="6a3f1-400">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-89) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6a3f1-402">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6a3f1-402">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen

[SpanningPlaceholder]: link-t-b-d "Espaços reservados de abrangência"  
