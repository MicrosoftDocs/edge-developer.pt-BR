---
description: Inspecionar e modificar animações com o inspetor de animação Microsoft Edge DevTools.
title: Inspecionar animações
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a695517cb56da057e62293b5ca92b22058602f44
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564214"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="inspect-animations"></a><span data-ttu-id="f64cb-104">Inspecionar animações</span><span class="sxs-lookup"><span data-stu-id="f64cb-104">Inspect animations</span></span>  

<span data-ttu-id="f64cb-105">Inspecionar e modificar animações com o inspetor de animação Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="f64cb-105">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspetor de animação" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="f64cb-107">inspetor de animação</span><span class="sxs-lookup"><span data-stu-id="f64cb-107">animation inspector</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="f64cb-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f64cb-108">Summary</span></span>  

*   <span data-ttu-id="f64cb-109">Capture animações abrindo o Inspetor de Animação.</span><span class="sxs-lookup"><span data-stu-id="f64cb-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="f64cb-110">O Inspetor de Animação detecta automaticamente e classifica animações em grupos.</span><span class="sxs-lookup"><span data-stu-id="f64cb-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="f64cb-111">Inspecione animações diminuindo cada uma delas, reprisando cada uma ou exibindo o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="f64cb-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="f64cb-112">Modifique animações alterando os deslocamentos de tempo, atraso, duração ou estrutura de chaves.</span><span class="sxs-lookup"><span data-stu-id="f64cb-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <a name="overview"></a><span data-ttu-id="f64cb-113">Visão geral</span><span class="sxs-lookup"><span data-stu-id="f64cb-113">Overview</span></span>  

<span data-ttu-id="f64cb-114">O Microsoft Edge DevTools Animation Inspector tem duas finalidades principais.</span><span class="sxs-lookup"><span data-stu-id="f64cb-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="f64cb-115">Inspecionando animações.</span><span class="sxs-lookup"><span data-stu-id="f64cb-115">Inspecting animations.</span></span>  <span data-ttu-id="f64cb-116">Você deseja reduzir a velocidade, repetir ou inspecionar o código-fonte de um Grupo de Animação.</span><span class="sxs-lookup"><span data-stu-id="f64cb-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="f64cb-117">Modificando animações.</span><span class="sxs-lookup"><span data-stu-id="f64cb-117">Modifying animations.</span></span>  <span data-ttu-id="f64cb-118">Você deseja modificar os deslocamentos de tempo, atraso, duração ou estrutura de chaves de um Grupo de Animação.</span><span class="sxs-lookup"><span data-stu-id="f64cb-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="f64cb-119">No momento, a edição do Bezier e a edição de estrutura de chave não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="f64cb-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="f64cb-120">O Inspetor de Animação dá suporte a animações CSS, transições CSS e animações da Web.</span><span class="sxs-lookup"><span data-stu-id="f64cb-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="f64cb-121">no momento, não há suporte para animações.</span><span class="sxs-lookup"><span data-stu-id="f64cb-121">animations are currently not supported.</span></span>  

### <a name="what-is-an-animation-group"></a><span data-ttu-id="f64cb-122">O que é um Grupo de Animação?</span><span class="sxs-lookup"><span data-stu-id="f64cb-122">What is an Animation Group?</span></span>  

<span data-ttu-id="f64cb-123">Um Grupo de Animação é um grupo de animações que pode estar relacionado uns aos outros.</span><span class="sxs-lookup"><span data-stu-id="f64cb-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="f64cb-124">Atualmente, a Web não tem um conceito real de animação de grupo, portanto, designers de movimento e desenvolvedores devem compor e temporizar animações individuais para que as animações renderizarem como um efeito visual coerente.</span><span class="sxs-lookup"><span data-stu-id="f64cb-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="f64cb-125">O Inspetor de Animação prevê quais animações estão relacionadas com base na hora de início \(excluindo atrasos e assim por diante\).</span><span class="sxs-lookup"><span data-stu-id="f64cb-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="f64cb-126">O Inspetor de Animação também grupos as animações lado a lado.</span><span class="sxs-lookup"><span data-stu-id="f64cb-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="f64cb-127">Em outras palavras, um conjunto de animações que são todas disparadas no mesmo bloco de scripts são agrupadas.</span><span class="sxs-lookup"><span data-stu-id="f64cb-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="f64cb-128">Se uma animação for assíncrona, ela será colocada em um grupo separado.</span><span class="sxs-lookup"><span data-stu-id="f64cb-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <a name="get-started"></a><span data-ttu-id="f64cb-129">Introdução</span><span class="sxs-lookup"><span data-stu-id="f64cb-129">Get started</span></span>  

<span data-ttu-id="f64cb-130">Há duas maneiras de abrir o Inspetor de Animação:</span><span class="sxs-lookup"><span data-stu-id="f64cb-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="f64cb-131">Abra o **menu Personalizar e Controlar DevTools**</span><span class="sxs-lookup"><span data-stu-id="f64cb-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="f64cb-132">Navegue até o sub menu **Mais** ferramentas.</span><span class="sxs-lookup"><span data-stu-id="f64cb-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="f64cb-133">Escolha **Animações**:</span><span class="sxs-lookup"><span data-stu-id="f64cb-133">Choose **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animações usando o Menu Principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="f64cb-135">**Animações usando** o Menu Principal</span><span class="sxs-lookup"><span data-stu-id="f64cb-135">**Animations** using Main Menu</span></span>  
        :::image-end:::  
        
*   <span data-ttu-id="f64cb-136">Abra o **Menu de Comando**</span><span class="sxs-lookup"><span data-stu-id="f64cb-136">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="f64cb-137">Digite `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="f64cb-137">Type `Drawer: Show Animations`.</span></span>  
        
<span data-ttu-id="f64cb-138">O Inspetor de Animação abre ao lado da **ferramenta Console.**</span><span class="sxs-lookup"><span data-stu-id="f64cb-138">The Animation Inspector opens next to the **Console** tool.</span></span>  <span data-ttu-id="f64cb-139">Como o Inspetor de Animação é uma ferramenta Drawer, você pode usar o Inspetor de Animação de qualquer painel DevTools.</span><span class="sxs-lookup"><span data-stu-id="f64cb-139">Since the Animation Inspector is a Drawer tool, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspetor de Animação Vazia" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="f64cb-141">Inspetor de Animação Vazia</span><span class="sxs-lookup"><span data-stu-id="f64cb-141">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="f64cb-142">O Inspetor de Animação é agrupado em quatro seções principais \(ou painéis\).</span><span class="sxs-lookup"><span data-stu-id="f64cb-142">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="f64cb-143">Este guia se refere a cada painel da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="f64cb-143">This guide refers to each pane as follows:</span></span>  

| <span data-ttu-id="f64cb-144">Índice</span><span class="sxs-lookup"><span data-stu-id="f64cb-144">Index</span></span> | <span data-ttu-id="f64cb-145">Painel</span><span class="sxs-lookup"><span data-stu-id="f64cb-145">Pane</span></span> | <span data-ttu-id="f64cb-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="f64cb-146">Description</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="f64cb-147">1</span><span class="sxs-lookup"><span data-stu-id="f64cb-147">1</span></span> | **<span data-ttu-id="f64cb-148">Controles</span><span class="sxs-lookup"><span data-stu-id="f64cb-148">Controls</span></span>** | <span data-ttu-id="f64cb-149">A partir daqui, você pode limpar todos os Grupos de Animação capturados no momento ou alterar a velocidade do Grupo de Animação atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="f64cb-149">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="f64cb-150">2</span><span class="sxs-lookup"><span data-stu-id="f64cb-150">2</span></span> | **<span data-ttu-id="f64cb-151">Visão geral</span><span class="sxs-lookup"><span data-stu-id="f64cb-151">Overview</span></span>** | <span data-ttu-id="f64cb-152">Escolha um Grupo de Animação aqui para inspecionar e modificá-lo no painel **Detalhes.**</span><span class="sxs-lookup"><span data-stu-id="f64cb-152">Choose an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="f64cb-153">3</span><span class="sxs-lookup"><span data-stu-id="f64cb-153">3</span></span> | **<span data-ttu-id="f64cb-154">Linha do Tempo</span><span class="sxs-lookup"><span data-stu-id="f64cb-154">Timeline</span></span>** | <span data-ttu-id="f64cb-155">Pause e inicie uma animação a partir daqui ou pule para um ponto específico na animação.</span><span class="sxs-lookup"><span data-stu-id="f64cb-155">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="f64cb-156">4</span><span class="sxs-lookup"><span data-stu-id="f64cb-156">4</span></span> | **<span data-ttu-id="f64cb-157">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f64cb-157">Details</span></span>** | <span data-ttu-id="f64cb-158">Inspecionar e modificar o Grupo de Animação selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="f64cb-158">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspetor de animação anotado" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="f64cb-160">Inspetor de animação anotado</span><span class="sxs-lookup"><span data-stu-id="f64cb-160">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="f64cb-161">Para capturar uma animação, basta executar a interação que dispara a animação enquanto o Inspetor de Animação está aberto.</span><span class="sxs-lookup"><span data-stu-id="f64cb-161">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="f64cb-162">Se uma animação for disparada no carregamento da página, atualize a página com o Inspetor de Animação aberto para detectar a animação.</span><span class="sxs-lookup"><span data-stu-id="f64cb-162">If an animation is triggered on page load, refresh the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a><span data-ttu-id="f64cb-163">Inspecionar animações</span><span class="sxs-lookup"><span data-stu-id="f64cb-163">Inspect animations</span></span>  

<span data-ttu-id="f64cb-164">Depois de capturar uma animação, há algumas maneiras de replay dela:</span><span class="sxs-lookup"><span data-stu-id="f64cb-164">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="f64cb-165">Passe o mouse na miniatura no painel **Visão** geral para exibir uma visualização dela.</span><span class="sxs-lookup"><span data-stu-id="f64cb-165">Hover on the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="f64cb-166">Escolha o Grupo \*\*\*\* de Animação no painel Visão geral \(para que ele seja exibido no **painel** Detalhes\) e escolha o ícone de **repetição** \( ícone de ![ repetição ](../media/replay-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f64cb-166">Choose the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and choose the **replay** \(![replay icon](../media/replay-button-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="f64cb-167">A animação é reprisada no viewport.</span><span class="sxs-lookup"><span data-stu-id="f64cb-167">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="f64cb-168">Escolha os **ícones de** velocidade de animação \( ícones de velocidade de ![ animação \) para alterar a velocidade de visualização do Grupo de Animação selecionado ](../media/animation-speed-buttons-icon.msft.png) no momento.</span><span class="sxs-lookup"><span data-stu-id="f64cb-168">Choose the **animation speed** \(![animation speed icons](../media/animation-speed-buttons-icon.msft.png)\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="f64cb-169">Você pode usar a barra vertical vermelha para alterar sua posição atual.</span><span class="sxs-lookup"><span data-stu-id="f64cb-169">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="f64cb-170">Escolha e arraste a barra vertical vermelha para limpar a animação do viewport.</span><span class="sxs-lookup"><span data-stu-id="f64cb-170">Choose and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <a name="view-animation-details"></a><span data-ttu-id="f64cb-171">Exibir detalhes da animação</span><span class="sxs-lookup"><span data-stu-id="f64cb-171">View animation details</span></span>  

<span data-ttu-id="f64cb-172">Depois de capturar um Grupo de Animação, escolha-o no painel **Visão** geral para exibir os detalhes.</span><span class="sxs-lookup"><span data-stu-id="f64cb-172">After you capture an Animation Group, choose on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="f64cb-173">No painel **Detalhes,** cada animação individual é atribuída a uma linha.</span><span class="sxs-lookup"><span data-stu-id="f64cb-173">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Detalhes do Grupo de Animação" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="f64cb-175">Detalhes do Grupo de Animação</span><span class="sxs-lookup"><span data-stu-id="f64cb-175">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="f64cb-176">Passe o mouse em uma animação para realça-la no viewport.</span><span class="sxs-lookup"><span data-stu-id="f64cb-176">Hover on an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="f64cb-177">Escolha a animação para selecioná-la na **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="f64cb-177">Choose the animation to select it in the **Elements** tool.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Passe o mouse na animação para realça-la no viewport" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="f64cb-179">Passe o mouse na animação para realça-la no viewport</span><span class="sxs-lookup"><span data-stu-id="f64cb-179">Hover on the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="f64cb-180">A seção mais à esquerda e mais escura de uma animação é a definição.</span><span class="sxs-lookup"><span data-stu-id="f64cb-180">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="f64cb-181">A seção à direita, mais desbotada representa iterações.</span><span class="sxs-lookup"><span data-stu-id="f64cb-181">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="f64cb-182">Por exemplo, na figura a seguir, as seções dois e três representam iterações da seção um.</span><span class="sxs-lookup"><span data-stu-id="f64cb-182">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagrama de iterações de animação" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="f64cb-184">Diagrama de iterações de animação</span><span class="sxs-lookup"><span data-stu-id="f64cb-184">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="f64cb-185">Se dois elementos têm a mesma animação aplicada, o Inspetor de Animação atribui a mesma cor aos elementos.</span><span class="sxs-lookup"><span data-stu-id="f64cb-185">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="f64cb-186">A cor é aleatória e não tem significância.</span><span class="sxs-lookup"><span data-stu-id="f64cb-186">The color is random and has no significance.</span></span>  <span data-ttu-id="f64cb-187">Por exemplo, na figura a seguir, os dois elementos e têm a mesma animação `div.cwccw.earlier` `div.cwccw.later` \( `spinrightleft` \) aplicada, assim como os `div.ccwcw.earlier` elementos `div.ccwcw.later` e.</span><span class="sxs-lookup"><span data-stu-id="f64cb-187">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animações codificadas por cores" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="f64cb-189">Animações codificadas por cores</span><span class="sxs-lookup"><span data-stu-id="f64cb-189">Color-coded animations</span></span>  
:::image-end:::  

## <a name="modify-animations"></a><span data-ttu-id="f64cb-190">Modificar animações</span><span class="sxs-lookup"><span data-stu-id="f64cb-190">Modify animations</span></span>  

<span data-ttu-id="f64cb-191">Há três maneiras de modificar uma animação com o Inspetor de Animação.</span><span class="sxs-lookup"><span data-stu-id="f64cb-191">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="f64cb-192">Duração da animação.</span><span class="sxs-lookup"><span data-stu-id="f64cb-192">Animation duration.</span></span>  
*   <span data-ttu-id="f64cb-193">Períodos de estrutura de chaves.</span><span class="sxs-lookup"><span data-stu-id="f64cb-193">Keyframe timings.</span></span>  
*   <span data-ttu-id="f64cb-194">Iniciar atraso de tempo.</span><span class="sxs-lookup"><span data-stu-id="f64cb-194">Start time delay.</span></span>  
    
<span data-ttu-id="f64cb-195">Na figura a seguir, a animação original é representada.</span><span class="sxs-lookup"><span data-stu-id="f64cb-195">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animação original antes da modificação" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="f64cb-197">Animação original antes da modificação</span><span class="sxs-lookup"><span data-stu-id="f64cb-197">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="f64cb-198">Para alterar a duração de uma animação, escolha e arraste o primeiro ou último círculo.</span><span class="sxs-lookup"><span data-stu-id="f64cb-198">To change the duration of an animation, choose and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Duração modificada" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="f64cb-200">Duração modificada</span><span class="sxs-lookup"><span data-stu-id="f64cb-200">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="f64cb-201">Se a animação definir qualquer regra de estrutura de chaves, elas serão representadas como círculos internos em branco.</span><span class="sxs-lookup"><span data-stu-id="f64cb-201">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="f64cb-202">Escolha e arraste um desses para alterar o tempo do keyframe.</span><span class="sxs-lookup"><span data-stu-id="f64cb-202">Choose and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Keyframe modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="f64cb-204">Keyframe modificado</span><span class="sxs-lookup"><span data-stu-id="f64cb-204">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="f64cb-205">Para adicionar um atraso a uma animação, escolha e arraste-a em qualquer lugar, exceto os círculos.</span><span class="sxs-lookup"><span data-stu-id="f64cb-205">To add a delay to an animation, choose and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Atraso modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="f64cb-207">Atraso modificado</span><span class="sxs-lookup"><span data-stu-id="f64cb-207">Modified delay</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f64cb-208">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f64cb-208">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="f64cb-209">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f64cb-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f64cb-210">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="f64cb-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f64cb-212">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f64cb-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
