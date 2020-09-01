---
title: Inspecionar animações
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a6970d76f4ff70031ef4cc8c6de119a41d1a5b80
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983342"
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





# <span data-ttu-id="e7b3f-103">Inspecionar animações</span><span class="sxs-lookup"><span data-stu-id="e7b3f-103">Inspect animations</span></span>   



<span data-ttu-id="e7b3f-104">Inspecione e modifique as animações com o Inspetor de animação do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-104">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Inspetor de animação" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="e7b3f-106">Inspetor de animação</span><span class="sxs-lookup"><span data-stu-id="e7b3f-106">animation inspector</span></span>  
:::image-end:::  

### <span data-ttu-id="e7b3f-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="e7b3f-107">Summary</span></span>  

*   <span data-ttu-id="e7b3f-108">Capture animações abrindo o Inspetor de animação.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-108">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="e7b3f-109">O Inspetor de animação detecta e classifica automaticamente as animações em grupos.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-109">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="e7b3f-110">Inspecione as animações reduzindo cada uma, reproduzindo cada uma delas ou exibindo o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-110">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="e7b3f-111">Modifique as animações alterando o intervalo, atraso, duração ou deslocamentos de quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-111">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="e7b3f-112">Visão geral</span><span class="sxs-lookup"><span data-stu-id="e7b3f-112">Overview</span></span>   

<span data-ttu-id="e7b3f-113">O Inspetor de animação do Microsoft Edge DevTools tem duas finalidades principais.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-113">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="e7b3f-114">Inspecionar animações.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-114">Inspecting animations.</span></span>  <span data-ttu-id="e7b3f-115">Você deseja diminuir a velocidade, reproduzir ou inspecionar o código-fonte de um grupo de animação.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-115">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="e7b3f-116">Modificação de animações.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-116">Modifying animations.</span></span>  <span data-ttu-id="e7b3f-117">Você deseja modificar o intervalo, atraso, duração ou deslocamentos de quadro-chave de um grupo de animação.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-117">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="e7b3f-118">Não há suporte para a edição de Bezier e a edição de quadro-chave no momento.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-118">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="e7b3f-119">O Inspetor de animação dá suporte a animações CSS, transições CSS e animações da Web.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-119">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="e7b3f-120">Não há suporte para animações no momento.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-120">animations are currently not supported.</span></span>  

### <span data-ttu-id="e7b3f-121">O que é um grupo de animação?</span><span class="sxs-lookup"><span data-stu-id="e7b3f-121">What is an Animation Group?</span></span>  

<span data-ttu-id="e7b3f-122">Um grupo de animação é um grupo de animações que pode estar relacionado entre si.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-122">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="e7b3f-123">Atualmente, a Web não tem um conceito real de uma animação de grupo, portanto, os designers e desenvolvedores de animação devem compor e cronometrar animações individuais para que as animações sejam renderizadas como um efeito visual coerente.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-123">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="e7b3f-124">O Inspetor de animação prevê quais animações estão relacionadas com base na hora de início \ (excluindo atrasos e assim por diante \).</span><span class="sxs-lookup"><span data-stu-id="e7b3f-124">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="e7b3f-125">O Inspetor de animação também agrupa as animações lado a lado.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-125">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="e7b3f-126">Em outras palavras, um conjunto de animações que são disparadas no mesmo bloco de script são agrupados juntos.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-126">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="e7b3f-127">Se uma animação for assíncrona, ela será colocada em um grupo separado.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-127">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="e7b3f-128">Introdução</span><span class="sxs-lookup"><span data-stu-id="e7b3f-128">Get started</span></span>  

<span data-ttu-id="e7b3f-129">Há duas maneiras de abrir o Inspetor de animação:</span><span class="sxs-lookup"><span data-stu-id="e7b3f-129">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="e7b3f-130">Abrir o menu **Personalizar e devtools de controle**</span><span class="sxs-lookup"><span data-stu-id="e7b3f-130">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="e7b3f-131">Navegue até o submenu **mais ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="e7b3f-131">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="e7b3f-132">Selecionar **animações**:</span><span class="sxs-lookup"><span data-stu-id="e7b3f-132">Select **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animações usando o menu principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="e7b3f-134">**Animações** usando o menu principal</span><span class="sxs-lookup"><span data-stu-id="e7b3f-134">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="e7b3f-135">Abrir o **menu de comandos**</span><span class="sxs-lookup"><span data-stu-id="e7b3f-135">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="e7b3f-136">Digite `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-136">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="e7b3f-137">O Inspetor de animação é aberto como uma guia ao lado da gaveta do console.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-137">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="e7b3f-138">Como o Inspetor de animação é uma guia gaveta, você pode usar o Inspetor de animação em qualquer painel do DevTools.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-138">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspetor de animação vazio" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="e7b3f-140">Inspetor de animação vazio</span><span class="sxs-lookup"><span data-stu-id="e7b3f-140">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="e7b3f-141">O Inspetor de animação está agrupado em quatro seções principais \ (ou painéis \).</span><span class="sxs-lookup"><span data-stu-id="e7b3f-141">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="e7b3f-142">Este guia se refere a cada painel da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7b3f-142">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="e7b3f-143">Painel</span><span class="sxs-lookup"><span data-stu-id="e7b3f-143">Pane</span></span> | <span data-ttu-id="e7b3f-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7b3f-144">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="e7b3f-145">um</span><span class="sxs-lookup"><span data-stu-id="e7b3f-145">1</span></span> | **<span data-ttu-id="e7b3f-146">Controles</span><span class="sxs-lookup"><span data-stu-id="e7b3f-146">Controls</span></span>** | <span data-ttu-id="e7b3f-147">Aqui você pode limpar todos os grupos de animação capturados no momento ou alterar a velocidade do grupo de animações selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-147">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="e7b3f-148">2</span><span class="sxs-lookup"><span data-stu-id="e7b3f-148">2</span></span> | **<span data-ttu-id="e7b3f-149">Visão geral</span><span class="sxs-lookup"><span data-stu-id="e7b3f-149">Overview</span></span>** | <span data-ttu-id="e7b3f-150">Selecione um grupo de animação aqui para inspecioná-lo e modificá-lo no painel **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="e7b3f-150">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="e7b3f-151">3D</span><span class="sxs-lookup"><span data-stu-id="e7b3f-151">3</span></span> | **<span data-ttu-id="e7b3f-152">Linha do Tempo</span><span class="sxs-lookup"><span data-stu-id="e7b3f-152">Timeline</span></span>** | <span data-ttu-id="e7b3f-153">Pause e inicie uma animação aqui, ou vá até um ponto específico na animação.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-153">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="e7b3f-154">4</span><span class="sxs-lookup"><span data-stu-id="e7b3f-154">4</span></span> | **<span data-ttu-id="e7b3f-155">Detalhes</span><span class="sxs-lookup"><span data-stu-id="e7b3f-155">Details</span></span>** | <span data-ttu-id="e7b3f-156">Inspecionar e modificar o grupo de animações selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-156">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspetor de animação com anotações" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="e7b3f-158">Inspetor de animação com anotações</span><span class="sxs-lookup"><span data-stu-id="e7b3f-158">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="e7b3f-159">Para capturar uma animação, basta executar a interação que aciona a animação enquanto o Inspetor de animação está aberto.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-159">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="e7b3f-160">Se uma animação for disparada na carga da página, recarregue a página com o Inspetor de animação aberto para detectar a animação.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-160">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="e7b3f-161">Inspecionar animações</span><span class="sxs-lookup"><span data-stu-id="e7b3f-161">Inspect animations</span></span>   

<span data-ttu-id="e7b3f-162">Depois de capturar uma animação, há algumas maneiras de reproduzi-la:</span><span class="sxs-lookup"><span data-stu-id="e7b3f-162">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="e7b3f-163">Passe o mouse sobre a miniatura no painel **visão geral** para exibir uma visualização dela.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-163">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="e7b3f-164">Selecione o grupo animação no painel de **visão geral** \ (para que ele seja exibido no painel de **detalhes** \) e pressione o ícone **reexecutar** \ ( ![ ícone de reprodução ][ImageReplayButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e7b3f-164">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** \(![replay icon][ImageReplayButtonIcon]\) icon.</span></span>  <span data-ttu-id="e7b3f-165">A animação é reproduzida no visor.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-165">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="e7b3f-166">Clique nos ícones **velocidade da animação** \ ( ![ ícones de velocidade da animação ][ImageAnimationSpeedButtonsIcon] \) para alterar a velocidade de visualização do grupo de animações selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-166">Click on the **animation speed** \(![animation speed icons][ImageAnimationSpeedButtonsIcon]\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="e7b3f-167">Você pode usar a barra vertical vermelha para alterar a posição atual.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-167">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="e7b3f-168">Clique e arraste a barra vertical vermelha para limpar a animação do visor.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-168">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <span data-ttu-id="e7b3f-169">Exibir detalhes da animação</span><span class="sxs-lookup"><span data-stu-id="e7b3f-169">View animation details</span></span>  

<span data-ttu-id="e7b3f-170">Depois de capturar um grupo de animação, clique nele no painel **visão geral** para ver os detalhes.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-170">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="e7b3f-171">No painel de **detalhes** , cada animação individual recebe a atribuição de uma linha.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-171">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Detalhes do grupo animação" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="e7b3f-173">Detalhes do grupo animação</span><span class="sxs-lookup"><span data-stu-id="e7b3f-173">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="e7b3f-174">Passe o mouse sobre uma animação para realçá-la no visor.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-174">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="e7b3f-175">Clique na animação para selecioná-la no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="e7b3f-175">Click on the animation to select it in the **Elements** panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Passe o mouse sobre a animação para realçá-la no visor" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="e7b3f-177">Passe o mouse sobre a animação para realçá-la no visor</span><span class="sxs-lookup"><span data-stu-id="e7b3f-177">Hover over the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="e7b3f-178">A seção mais à esquerda de uma animação é a definição.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-178">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="e7b3f-179">A seção direita e mais esmaecida representa iterações.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-179">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="e7b3f-180">Por exemplo, na figura a seguir, as seções dois e três representam iterações da seção um.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-180">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagrama de iterações de animação" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="e7b3f-182">Diagrama de iterações de animação</span><span class="sxs-lookup"><span data-stu-id="e7b3f-182">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="e7b3f-183">Se dois elementos tiverem a mesma animação aplicada, o Inspetor de animação atribuirá a mesma cor aos elementos.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-183">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="e7b3f-184">A cor é aleatória e não tem importância.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-184">The color is random and has no significance.</span></span>  <span data-ttu-id="e7b3f-185">Por exemplo, na figura a seguir, os dois elementos `div.cwccw.earlier` e `div.cwccw.later` têm a mesma animação \ ( `spinrightleft` \) aplicada, como os `div.ccwcw.earlier` elementos e `div.ccwcw.later` .</span><span class="sxs-lookup"><span data-stu-id="e7b3f-185">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animações codificadas por cor" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="e7b3f-187">Animações codificadas por cor</span><span class="sxs-lookup"><span data-stu-id="e7b3f-187">Color-coded animations</span></span>  
:::image-end:::  

## <span data-ttu-id="e7b3f-188">Modificar animações</span><span class="sxs-lookup"><span data-stu-id="e7b3f-188">Modify animations</span></span>   

<span data-ttu-id="e7b3f-189">Há três maneiras como você pode modificar uma animação com o Inspetor de animação.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-189">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="e7b3f-190">Duração da animação.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-190">Animation duration.</span></span>  
*   <span data-ttu-id="e7b3f-191">Intervalos do quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-191">Keyframe timings.</span></span>  
*   <span data-ttu-id="e7b3f-192">Intervalo de tempo de início.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-192">Start time delay.</span></span>  
    
<span data-ttu-id="e7b3f-193">Na figura a seguir, a animação original é representada.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-193">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animação original antes da modificação" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="e7b3f-195">Animação original antes da modificação</span><span class="sxs-lookup"><span data-stu-id="e7b3f-195">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="e7b3f-196">Para alterar a duração de uma animação, clique e arraste o primeiro ou o último círculo.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-196">To change the duration of an animation, click and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Duração modificada" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="e7b3f-198">Duração modificada</span><span class="sxs-lookup"><span data-stu-id="e7b3f-198">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="e7b3f-199">Se a animação define quaisquer regras de quadro-chave, elas são representadas como círculos internos brancos.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-199">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="e7b3f-200">Clique e arraste uma destas para alterar o intervalo do quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-200">Click and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Quadro-chave modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="e7b3f-202">Quadro-chave modificado</span><span class="sxs-lookup"><span data-stu-id="e7b3f-202">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="e7b3f-203">Para adicionar um atraso a uma animação, clique e arraste-a para qualquer lugar, exceto os círculos.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-203">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Atraso modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="e7b3f-205">Atraso modificado</span><span class="sxs-lookup"><span data-stu-id="e7b3f-205">Modified delay</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="e7b3f-206">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="e7b3f-206">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e7b3f-207">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e7b3f-207">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e7b3f-209">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e7b3f-209">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
