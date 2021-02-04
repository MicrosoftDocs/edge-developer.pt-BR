---
description: Saiba como alterar estilos e configurações de fonte CSS usando o painel Estilos no Microsoft Edge DevTools.
title: Editar estilos e configurações de fonte CSS no painel Estilos no DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 928f7abb0f74839708cbe5c904ad321109ae33f0
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313091"
---
# <span data-ttu-id="93c92-104">Editar estilos e configurações de fonte CSS no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="93c92-104">Edit CSS font styles and settings in the Styles pane</span></span>  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

<span data-ttu-id="93c92-105">A tipografia na Web é uma parte importante da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="93c92-105">Typography on the web is an important part of the user experience.</span></span>  <span data-ttu-id="93c92-106">Você deseja garantir que você conheça as diretrizes da marca corporativa e que seu conteúdo seja exibido conforme o esperado em vários dispositivos.</span><span class="sxs-lookup"><span data-stu-id="93c92-106">You want to ensure you meet corporate brand guidelines, and your content displays as expected on various devices.</span></span>  <span data-ttu-id="93c92-107">O texto deve ser fácil de ler usando tamanho e altura de linha.</span><span class="sxs-lookup"><span data-stu-id="93c92-107">Text must be easy to read using size and line-height.</span></span>  <span data-ttu-id="93c92-108">Os usuários podem re tamanho das fontes para atender às necessidades individuais.</span><span class="sxs-lookup"><span data-stu-id="93c92-108">Users may resize fonts to meet individual needs.</span></span>  <span data-ttu-id="93c92-109">Para situações em que fontes específicas não estão disponíveis em um dispositivo de usuário, você deve fornecer opções de fonte de fallback.</span><span class="sxs-lookup"><span data-stu-id="93c92-109">For situations when specific fonts are not available on a user device, you should provide fallback font options.</span></span>  

<span data-ttu-id="93c92-110">CSS fornece melhor suporte para tipografia nos últimos anos.</span><span class="sxs-lookup"><span data-stu-id="93c92-110">CSS provides better support for typography in recent years.</span></span>  <span data-ttu-id="93c92-111">Há dezenas de unidades CSS diferentes disponíveis para definir o tamanho do texto.</span><span class="sxs-lookup"><span data-stu-id="93c92-111">There are dozens of different CSS units available to define the size of text.</span></span>  <span data-ttu-id="93c92-112">Você também tem várias propriedades CSS que afetam o tamanho da fonte, o espaçamento, a altura da linha e outros recursos tipográficos.</span><span class="sxs-lookup"><span data-stu-id="93c92-112">You also have several CSS properties that affect font-size, spacing, line height, and other typographic features.</span></span>  

<span data-ttu-id="93c92-113">Para facilitar o trabalho com tipografia, um **Editor** de Fontes visual agora está **no** painel Estilos.</span><span class="sxs-lookup"><span data-stu-id="93c92-113">To make it easier when working with typography, a visual **Font Editor** is now in the **Styles** pane.</span></span>  <span data-ttu-id="93c92-114">Você pode alterar as configurações de fonte e as alterações são renderizadas imediatamente no navegador.</span><span class="sxs-lookup"><span data-stu-id="93c92-114">You may change your font settings, and the changes are rendered immediately in the browser.</span></span>  <span data-ttu-id="93c92-115">Tudo sem conhecimento profundo do CSS.</span><span class="sxs-lookup"><span data-stu-id="93c92-115">All without in-depth knowledge of CSS.</span></span>  

<span data-ttu-id="93c92-116">Atualmente, **a ferramenta Habilitar** nova ferramenta de editor de fontes no recurso do painel Estilos é experimental e você precisa ative-a para ferramentas de desenvolvedor do [Microsoft Edge.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="93c92-116">Currently the **Enable new font editor tool within the Styles pane** feature is experimental and you need to [turn it on for Microsoft Edge Developer Tools][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures].</span></span>  

<span data-ttu-id="93c92-117">Qualquer CSS no painel **Estilos,** seja definições de fonte ou estilos em linha, exibe automaticamente um ícone que abre o Editor de **Fonte**visual.</span><span class="sxs-lookup"><span data-stu-id="93c92-117">Any CSS in the **Styles** pane, either font definitions or inline styles, automatically displays an icon that opens the visual **Font Editor**.</span></span>  <span data-ttu-id="93c92-118">Para abrir o **Editor de Fonte**visual, escolha o ícone do Editor **de** Fontes.</span><span class="sxs-lookup"><span data-stu-id="93c92-118">To open the visual **Font Editor**, choose the **Font Editor** icon.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="O ícone no painel Estilos para editar configurações de fonte" lightbox="../media/font-editor-icon.msft.png":::
         <span data-ttu-id="93c92-120">O ícone no painel **Estilos** para editar configurações de fonte</span><span class="sxs-lookup"><span data-stu-id="93c92-120">The icon in the **Styles** pane to edit font settings</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="O Editor de Fontes aberto na parte superior do painel Estilos" lightbox="../media/font-editor-open.msft.png":::
         <span data-ttu-id="93c92-122">O **Editor de** Fontes aberto na parte superior do painel Estilos \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93c92-122">The **Font Editor** open on top of the **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="93c92-123">Todos os campos no Editor de **Fonte visual** são preenchidos a partir dos valores no CSS **no** painel Estilos.</span><span class="sxs-lookup"><span data-stu-id="93c92-123">All fields in the visual **Font Editor** are populated from the values in the CSS in the **Styles** pane.</span></span>  <span data-ttu-id="93c92-124">Por exemplo, a definição é definida como no painel Estilos, para que o campo de texto de altura da linha seja exibido, e a lista suspenso `line-height` `160%` de unidade é \*\*\*\* `160` `%` exibida.</span><span class="sxs-lookup"><span data-stu-id="93c92-124">For example, the `line-height` definition is set to `160%` in the **Styles** pane, so the line height text field displays `160`, and the unit dropdown displays `%`.</span></span>  <span data-ttu-id="93c92-125">Além disso, o controle deslizante é automaticamente definido para corresponder aos valores do campo de texto.</span><span class="sxs-lookup"><span data-stu-id="93c92-125">Also, the slider is automatically set to match the values of the text field.</span></span>  

<span data-ttu-id="93c92-126">O **Editor de** Fontes consiste em duas partes: o seletor de Família de Fontes e o editor de Propriedades css.</span><span class="sxs-lookup"><span data-stu-id="93c92-126">The **Font Editor** consists of two parts:  the Font Family selector, and the CSS Properties editor.</span></span>  

## <span data-ttu-id="93c92-127">O seletor de Família de Fontes</span><span class="sxs-lookup"><span data-stu-id="93c92-127">The Font Family selector</span></span>  

<span data-ttu-id="93c92-128">O seletor de Família de Fontes é a parte superior do Editor de **Fonte visual.**</span><span class="sxs-lookup"><span data-stu-id="93c92-128">The Font Family selector is the upper part of the visual **Font Editor**.</span></span>  <span data-ttu-id="93c92-129">Para escolher as fontes da regra CSS, no editor de CSS, use o **seletor de Família de** Fontes.</span><span class="sxs-lookup"><span data-stu-id="93c92-129">To choose the fonts of the CSS rule, in the CSS editor, use the **Font Family** selector.</span></span>  <span data-ttu-id="93c92-130">Você pode escolher fontes principais e de fallback para cada regra CSS.</span><span class="sxs-lookup"><span data-stu-id="93c92-130">You may choose main and fallback fonts for each CSS rule.</span></span>  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="O Editor de Fontes aberto na parte superior do painel Estilos com o seletor da Família de Fontes realçado" lightbox="../media/font-editor-font-family.msft.png":::
   <span data-ttu-id="93c92-132">O **Editor de** Fontes aberto na parte superior do painel **Estilos** com o **seletor da Família de** Fontes realçado</span><span class="sxs-lookup"><span data-stu-id="93c92-132">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="93c92-133">Use o **menu suspenso Família** de Fontes para escolher em uma lista de fontes.</span><span class="sxs-lookup"><span data-stu-id="93c92-133">Use the **Font Family** dropdown to choose from a list of fonts.</span></span>  <span data-ttu-id="93c92-134">As fontes são organizadas em quatro grupos.</span><span class="sxs-lookup"><span data-stu-id="93c92-134">Fonts are organized into four groups.</span></span>  

1.  <span data-ttu-id="93c92-135">Fontes computadas, que são as fontes disponíveis na folha de estilos no **painel** Estilos.</span><span class="sxs-lookup"><span data-stu-id="93c92-135">Computed fonts, which are the fonts available in the stylesheet in the **Styles** pane.</span></span>  
1.  <span data-ttu-id="93c92-136">Fontes do sistema, que são as fontes disponíveis no sistema operacional atual.</span><span class="sxs-lookup"><span data-stu-id="93c92-136">System fonts, which are the fonts that are available on the current operating system.</span></span>  
1.  <span data-ttu-id="93c92-137">Famílias de fontes genéricas, como `serif` ou `sans-serif` .</span><span class="sxs-lookup"><span data-stu-id="93c92-137">Generic font families, such as `serif` or `sans-serif`.</span></span>  
1.  <span data-ttu-id="93c92-138">Valores globais, como `inherit` , `initial` e `unset` .</span><span class="sxs-lookup"><span data-stu-id="93c92-138">Global values, such as `inherit`, `initial`, and `unset`.</span></span>  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="O editor de fontes aberto na parte superior do painel Estilos com o seletor da Família de Fontes realçado" lightbox="../media/font-editor-font-family-list.msft.png":::
   <span data-ttu-id="93c92-140">O **Editor de** Fontes aberto na parte superior do painel **Estilos** com o **seletor da Família** de Fontes realçado</span><span class="sxs-lookup"><span data-stu-id="93c92-140">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="93c92-141">Depois de escolher uma fonte, outro menu suspenso é exibido para você escolher fontes de fallback.</span><span class="sxs-lookup"><span data-stu-id="93c92-141">After you choose a font, another dropdown menu is displayed for you to choose fallback fonts.</span></span>  <span data-ttu-id="93c92-142">Você pode escolher até oito fontes de fallback.</span><span class="sxs-lookup"><span data-stu-id="93c92-142">You may choose up to eight fallback fonts.</span></span>  <span data-ttu-id="93c92-143">Para remover uma fonte, escolha o **ícone Excluir Família de** Fontes.</span><span class="sxs-lookup"><span data-stu-id="93c92-143">To remove a font, choose the **Delete Font Family** icon.</span></span>  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> <span data-ttu-id="93c92-144">Se você escolher um valor global para a família de fontes, não obterá outro menu suspenso, pois não há fallback para ele no CSS.</span><span class="sxs-lookup"><span data-stu-id="93c92-144">If you choose a global value for font family, you do not get another dropdown since there is no fallback for it in CSS.</span></span>  

## <span data-ttu-id="93c92-145">O editor de Propriedades CSS</span><span class="sxs-lookup"><span data-stu-id="93c92-145">The CSS Properties editor</span></span>  

<span data-ttu-id="93c92-146">You may change CSS font properties in the lower part of the visual **Font Editor**.</span><span class="sxs-lookup"><span data-stu-id="93c92-146">You may change CSS font properties in the lower part of the visual **Font Editor**.</span></span>  <span data-ttu-id="93c92-147">Você pode alterar o tamanho da fonte, a altura da linha, o peso da fonte e o espaçamento entre letras usando qualquer um dos controles da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="93c92-147">You may change the font size, line height, font weight, and letter spacing using any of the UI controls.</span></span>  <span data-ttu-id="93c92-148">Suas alterações são aplicadas imediatamente no navegador.</span><span class="sxs-lookup"><span data-stu-id="93c92-148">Your changes are applied immediately in the browser.</span></span>  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="O editor de fontes aberto na parte superior do painel Estilos com as propriedades CSS realçadas" lightbox="../media/font-editor-css-properties.msft.png":::
   <span data-ttu-id="93c92-150">O **Editor de** Fontes aberto na parte superior do painel **Estilos** com as propriedades CSS realçadas</span><span class="sxs-lookup"><span data-stu-id="93c92-150">The **Font Editor** open on top of the **Styles** pane with the CSS properties highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="93c92-151">Você também pode converter unidades CSS usando o **Editor de Fonte visual.**</span><span class="sxs-lookup"><span data-stu-id="93c92-151">You may also convert CSS units using the visual **Font Editor**.</span></span>  <span data-ttu-id="93c92-152">For example, you may use the tool on a CSS rule where the **Font Size** slider is initially set to `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="93c92-152">For example, you may use the tool on a CSS rule where the **Font Size** slider is initially set to `16 pixels`.</span></span>  <span data-ttu-id="93c92-153">Agora, use o menu suspenso de unidade e escolha o `em` valor.</span><span class="sxs-lookup"><span data-stu-id="93c92-153">Now, use the unit dropdown and choose the value `em`.</span></span>  <span data-ttu-id="93c92-154">O `1 em` exibido é igual a `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="93c92-154">The `1 em` displayed is equal to `16 pixels`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Alterar o tamanho da fonte para 16 pixels" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         <span data-ttu-id="93c92-156">Alterar o tamanho da fonte para</span><span class="sxs-lookup"><span data-stu-id="93c92-156">Change the font size to</span></span> `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Abrir o menu suspenso de unidade para converter em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         <span data-ttu-id="93c92-158">Abrir o menu suspenso de unidade para converter em</span><span class="sxs-lookup"><span data-stu-id="93c92-158">Open the unit dropdown to convert to</span></span> `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="93c92-159">O menu suspenso de unidade fornece todas as unidades CSS numéricas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="93c92-159">The unit dropdown provides all the numeric CSS units that are available.</span></span>  <span data-ttu-id="93c92-160">Tamanho da fonte, altura da linha, peso da fonte e espaçamento usam unidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="93c92-160">Font size, line height, font weight, and spacing all use different units.</span></span>  <span data-ttu-id="93c92-161">Quando as caixas de texto têm foco, você pode selecionar as teclas e `arrow up` `arrow down` as teclas para ajustar suas configurações.</span><span class="sxs-lookup"><span data-stu-id="93c92-161">When the text boxes have focus, you may select the `arrow up` and `arrow down` keys to fine-tune your settings.</span></span>  <span data-ttu-id="93c92-162">Para usar os controles deslizantes com um teclado, selecione `arrow left` as `arrow down` teclas e as teclas.</span><span class="sxs-lookup"><span data-stu-id="93c92-162">To use the sliders with a keyboard, select the `arrow left` and `arrow down` keys.</span></span>  

<span data-ttu-id="93c92-163">O editor de Propriedades CSS também inclui palavras-chave predefinidas.</span><span class="sxs-lookup"><span data-stu-id="93c92-163">The CSS Properties editor also includes preset keywords.</span></span>  <span data-ttu-id="93c92-164">Para usar as palavras-chave predefinidas, no lado direito, escolha o `Toggle Input Type` ícone.</span><span class="sxs-lookup"><span data-stu-id="93c92-164">To use the preset keywords, on the right-hand side, choose the `Toggle Input Type` icon.</span></span>  <span data-ttu-id="93c92-165">A interface do usuário muda e um menu suspenso de palavras-chave predefinidas é exibido.</span><span class="sxs-lookup"><span data-stu-id="93c92-165">The UI changes, and a dropdown of preset keywords are displayed.</span></span>  <span data-ttu-id="93c92-166">Para retornar à interface do usuário com o controle deslizante e outros controles de interface do usuário, escolha o `Toggle Input Type` ícone novamente.</span><span class="sxs-lookup"><span data-stu-id="93c92-166">To return to the UI with the slider and other UI controls, choose the `Toggle Input Type` icon again.</span></span>  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Abrir a interface de palavra-chave predefinida" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   <span data-ttu-id="93c92-168">Abrir a interface de palavra-chave predefinida</span><span class="sxs-lookup"><span data-stu-id="93c92-168">Open the preset keyword interface</span></span>  
:::image-end:::  

## <span data-ttu-id="93c92-169">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="93c92-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Ativar recursos experimentais - recursos experimentais | Microsoft Docs"  
