---
title: Inspecionar animações
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 6466c7f0e1f8680a2429b565e8022d152d05d733
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562076"
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





# <span data-ttu-id="b1897-103">Inspecionar animações</span><span class="sxs-lookup"><span data-stu-id="b1897-103">Inspect animations</span></span>   



<span data-ttu-id="b1897-104">Inspecione e modifique as animações com o Inspetor de animação do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b1897-104">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

> ##### <span data-ttu-id="b1897-105">Figura 1</span><span class="sxs-lookup"><span data-stu-id="b1897-105">Figure 1</span></span>  
> <span data-ttu-id="b1897-106">Inspetor de animação</span><span class="sxs-lookup"><span data-stu-id="b1897-106">Animation inspector</span></span>  
> ![Inspetor de animação][ImageAnimationInspector]  

### <span data-ttu-id="b1897-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b1897-108">Summary</span></span>  

*   <span data-ttu-id="b1897-109">Capture animações abrindo o Inspetor de animação.</span><span class="sxs-lookup"><span data-stu-id="b1897-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="b1897-110">O Inspetor de animação detecta e classifica automaticamente as animações em grupos.</span><span class="sxs-lookup"><span data-stu-id="b1897-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="b1897-111">Inspecione as animações reduzindo cada uma, reproduzindo cada uma delas ou exibindo o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="b1897-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="b1897-112">Modifique as animações alterando o intervalo, atraso, duração ou deslocamentos de quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="b1897-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="b1897-113">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b1897-113">Overview</span></span>   

<span data-ttu-id="b1897-114">O Inspetor de animação do Microsoft Edge DevTools tem duas finalidades principais.</span><span class="sxs-lookup"><span data-stu-id="b1897-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="b1897-115">Inspecionar animações.</span><span class="sxs-lookup"><span data-stu-id="b1897-115">Inspecting animations.</span></span>  <span data-ttu-id="b1897-116">Você deseja diminuir a velocidade, reproduzir ou inspecionar o código-fonte de um grupo de animação.</span><span class="sxs-lookup"><span data-stu-id="b1897-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="b1897-117">Modificação de animações.</span><span class="sxs-lookup"><span data-stu-id="b1897-117">Modifying animations.</span></span>  <span data-ttu-id="b1897-118">Você deseja modificar o intervalo, atraso, duração ou deslocamentos de quadro-chave de um grupo de animação.</span><span class="sxs-lookup"><span data-stu-id="b1897-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="b1897-119">Não há suporte para a edição de Bezier e a edição de quadro-chave no momento.</span><span class="sxs-lookup"><span data-stu-id="b1897-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="b1897-120">O Inspetor de animação dá suporte a animações CSS, transições CSS e animações da Web.</span><span class="sxs-lookup"><span data-stu-id="b1897-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="b1897-121">Não há suporte para animações no momento.</span><span class="sxs-lookup"><span data-stu-id="b1897-121">animations are currently not supported.</span></span>  

### <span data-ttu-id="b1897-122">O que é um grupo de animação?</span><span class="sxs-lookup"><span data-stu-id="b1897-122">What is an Animation Group?</span></span>  

<span data-ttu-id="b1897-123">Um grupo de animação é um grupo de animações que pode estar relacionado entre si.</span><span class="sxs-lookup"><span data-stu-id="b1897-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="b1897-124">Atualmente, a Web não tem um conceito real de uma animação de grupo, portanto, os designers e desenvolvedores de animação devem compor e cronometrar animações individuais para que as animações sejam renderizadas como um efeito visual coerente.</span><span class="sxs-lookup"><span data-stu-id="b1897-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="b1897-125">O Inspetor de animação prevê quais animações estão relacionadas com base na hora de início \ (excluindo atrasos e assim por diante \).</span><span class="sxs-lookup"><span data-stu-id="b1897-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="b1897-126">O Inspetor de animação também agrupa as animações lado a lado.</span><span class="sxs-lookup"><span data-stu-id="b1897-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="b1897-127">Em outras palavras, um conjunto de animações que são disparadas no mesmo bloco de script são agrupados juntos.</span><span class="sxs-lookup"><span data-stu-id="b1897-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="b1897-128">Se uma animação for assíncrona, ela será colocada em um grupo separado.</span><span class="sxs-lookup"><span data-stu-id="b1897-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="b1897-129">Introdução</span><span class="sxs-lookup"><span data-stu-id="b1897-129">Get started</span></span>  

<span data-ttu-id="b1897-130">Há duas maneiras de abrir o Inspetor de animação:</span><span class="sxs-lookup"><span data-stu-id="b1897-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="b1897-131">Abrir o menu **Personalizar e devtools de controle**</span><span class="sxs-lookup"><span data-stu-id="b1897-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="b1897-132">Navegue até o submenu **mais ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="b1897-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="b1897-133">Selecionar **animações**:</span><span class="sxs-lookup"><span data-stu-id="b1897-133">Select **Animations**:</span></span>  
        
        > ##### <span data-ttu-id="b1897-134">Figura 2</span><span class="sxs-lookup"><span data-stu-id="b1897-134">Figure 2</span></span>  
        > <span data-ttu-id="b1897-135">Animações via menu principal</span><span class="sxs-lookup"><span data-stu-id="b1897-135">Animations via Main Menu</span></span>  
        > ![Animações via menu principal][ImageAnimationsViaMainMenu]  
        
*   <span data-ttu-id="b1897-137">Abrir o **menu de comandos**</span><span class="sxs-lookup"><span data-stu-id="b1897-137">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="b1897-138">Digite `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="b1897-138">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="b1897-139">O Inspetor de animação é aberto como uma guia ao lado da gaveta do console.</span><span class="sxs-lookup"><span data-stu-id="b1897-139">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="b1897-140">Como o Inspetor de animação é uma guia gaveta, você pode usar o Inspetor de animação em qualquer painel do DevTools.</span><span class="sxs-lookup"><span data-stu-id="b1897-140">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

> ##### <span data-ttu-id="b1897-141">Figura 3</span><span class="sxs-lookup"><span data-stu-id="b1897-141">Figure 3</span></span>  
> <span data-ttu-id="b1897-142">Inspetor de animação vazio</span><span class="sxs-lookup"><span data-stu-id="b1897-142">Empty Animation Inspector</span></span>  
> ![Inspetor de animação vazio][ImageEmptyAnimationInspector]  

<span data-ttu-id="b1897-144">O Inspetor de animação está agrupado em quatro seções principais \ (ou painéis \).</span><span class="sxs-lookup"><span data-stu-id="b1897-144">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="b1897-145">Este guia se refere a cada painel da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b1897-145">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="b1897-146">Painel</span><span class="sxs-lookup"><span data-stu-id="b1897-146">Pane</span></span> | <span data-ttu-id="b1897-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1897-147">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="b1897-148">um</span><span class="sxs-lookup"><span data-stu-id="b1897-148">1</span></span> | **<span data-ttu-id="b1897-149">Controles</span><span class="sxs-lookup"><span data-stu-id="b1897-149">Controls</span></span>** | <span data-ttu-id="b1897-150">Aqui você pode limpar todos os grupos de animação capturados no momento ou alterar a velocidade do grupo de animações selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="b1897-150">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="b1897-151">2</span><span class="sxs-lookup"><span data-stu-id="b1897-151">2</span></span> | **<span data-ttu-id="b1897-152">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b1897-152">Overview</span></span>** | <span data-ttu-id="b1897-153">Selecione um grupo de animação aqui para inspecioná-lo e modificá-lo no painel **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="b1897-153">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="b1897-154">3D</span><span class="sxs-lookup"><span data-stu-id="b1897-154">3</span></span> | **<span data-ttu-id="b1897-155">Linha do Tempo</span><span class="sxs-lookup"><span data-stu-id="b1897-155">Timeline</span></span>** | <span data-ttu-id="b1897-156">Pause e inicie uma animação aqui, ou vá até um ponto específico na animação.</span><span class="sxs-lookup"><span data-stu-id="b1897-156">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="b1897-157">4</span><span class="sxs-lookup"><span data-stu-id="b1897-157">4</span></span> | **<span data-ttu-id="b1897-158">Detalhes</span><span class="sxs-lookup"><span data-stu-id="b1897-158">Details</span></span>** | <span data-ttu-id="b1897-159">Inspecionar e modificar o grupo de animações selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="b1897-159">Inspect and modify the currently selected Animation Group.</span></span> |  

> ##### <span data-ttu-id="b1897-160">Figura 4</span><span class="sxs-lookup"><span data-stu-id="b1897-160">Figure 4</span></span>  
> <span data-ttu-id="b1897-161">Inspetor de animação com anotações</span><span class="sxs-lookup"><span data-stu-id="b1897-161">Annotated Animation Inspector</span></span>  
> ![Inspetor de animação com anotações][ImageAnnotatedAnimationInspector]  

<span data-ttu-id="b1897-163">Para capturar uma animação, basta executar a interação que aciona a animação enquanto o Inspetor de animação está aberto.</span><span class="sxs-lookup"><span data-stu-id="b1897-163">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="b1897-164">Se uma animação for disparada na carga da página, recarregue a página com o Inspetor de animação aberto para detectar a animação.</span><span class="sxs-lookup"><span data-stu-id="b1897-164">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="b1897-165">Inspecionar animações</span><span class="sxs-lookup"><span data-stu-id="b1897-165">Inspect animations</span></span>   

<span data-ttu-id="b1897-166">Depois de capturar uma animação, há algumas maneiras de reproduzi-la:</span><span class="sxs-lookup"><span data-stu-id="b1897-166">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="b1897-167">Passe o mouse sobre a miniatura no painel **visão geral** para exibir uma visualização dela.</span><span class="sxs-lookup"><span data-stu-id="b1897-167">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="b1897-168">Selecione o grupo animação no painel de **visão geral** \ (para que ele seja exibido no painel de **detalhes** \) e pressione **o** ![ ícone do ícone reproduzir reprodução ][ImageReplayButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="b1897-168">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** ![replay icon][ImageReplayButtonIcon] icon.</span></span>  <span data-ttu-id="b1897-169">A animação é reproduzida no visor.</span><span class="sxs-lookup"><span data-stu-id="b1897-169">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="b1897-170">Clique nos ícones de velocidade da animação **velocidade** da animação ![ ][ImageAnimationSpeedButtonsIcon] ícones para alterar a velocidade de visualização do grupo de animações selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="b1897-170">Click on the **animation speed** ![animation speed icons][ImageAnimationSpeedButtonsIcon] icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="b1897-171">Você pode usar a barra vertical vermelha para alterar a posição atual.</span><span class="sxs-lookup"><span data-stu-id="b1897-171">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="b1897-172">Clique e arraste a barra vertical vermelha para limpar a animação do visor.</span><span class="sxs-lookup"><span data-stu-id="b1897-172">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  

### <span data-ttu-id="b1897-173">Exibir detalhes da animação</span><span class="sxs-lookup"><span data-stu-id="b1897-173">View animation details</span></span>  

<span data-ttu-id="b1897-174">Depois de capturar um grupo de animação, clique nele no painel **visão geral** para ver os detalhes.</span><span class="sxs-lookup"><span data-stu-id="b1897-174">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="b1897-175">No painel de **detalhes** , cada animação individual recebe a atribuição de uma linha.</span><span class="sxs-lookup"><span data-stu-id="b1897-175">In the **Details** pane each individual animation is assigned the a row.</span></span>  

> ##### <span data-ttu-id="b1897-176">Figura 5</span><span class="sxs-lookup"><span data-stu-id="b1897-176">Figure 5</span></span>  
> <span data-ttu-id="b1897-177">Detalhes do grupo animação</span><span class="sxs-lookup"><span data-stu-id="b1897-177">Animation Group details</span></span>  
> ![Detalhes do grupo animação][ImageAnimationGroupDetails]  

<span data-ttu-id="b1897-179">Passe o mouse sobre uma animação para realçá-la no visor.</span><span class="sxs-lookup"><span data-stu-id="b1897-179">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="b1897-180">Clique na animação para selecioná-la no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="b1897-180">Click on the animation to select it in the **Elements** panel.</span></span>  

> ##### <span data-ttu-id="b1897-181">Figura 6</span><span class="sxs-lookup"><span data-stu-id="b1897-181">Figure 6</span></span>  
> <span data-ttu-id="b1897-182">Passe o mouse sobre a animação para realçá-la no visor</span><span class="sxs-lookup"><span data-stu-id="b1897-182">Hover over the animation to highlight it in viewport</span></span>  
> ![Passe o mouse sobre a animação para realçá-la no visor][ImageHoverOverAnimationHighlightViewport]  

<span data-ttu-id="b1897-184">A seção mais à esquerda de uma animação é a definição.</span><span class="sxs-lookup"><span data-stu-id="b1897-184">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="b1897-185">A seção direita e mais esmaecida representa iterações.</span><span class="sxs-lookup"><span data-stu-id="b1897-185">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="b1897-186">Por exemplo, na [Figura 7](#figure-7), as seções dois e três representam iterações da seção um.</span><span class="sxs-lookup"><span data-stu-id="b1897-186">For example, in [Figure 7](#figure-7), sections two and three represent iterations of section one.</span></span>  

> ##### <span data-ttu-id="b1897-187">Figura 7</span><span class="sxs-lookup"><span data-stu-id="b1897-187">Figure 7</span></span>  
> <span data-ttu-id="b1897-188">Diagrama de iterações de animação</span><span class="sxs-lookup"><span data-stu-id="b1897-188">Diagram of animation iterations</span></span>  
> ![Diagrama de iterações de animação][ImageDiagramAnimationIterations]  

<span data-ttu-id="b1897-190">Se dois elementos tiverem a mesma animação aplicada, o Inspetor de animação atribuirá a mesma cor aos elementos.</span><span class="sxs-lookup"><span data-stu-id="b1897-190">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="b1897-191">A cor é aleatória e não tem importância.</span><span class="sxs-lookup"><span data-stu-id="b1897-191">The color is random and has no significance.</span></span>  <span data-ttu-id="b1897-192">Por exemplo, na [Figura 8](#figure-8) , os dois elementos `div.cwccw.earlier` e `div.cwccw.later` têm a mesma animação \ ( `spinrightleft` \) aplicada, como os `div.ccwcw.earlier` elementos e `div.ccwcw.later` .</span><span class="sxs-lookup"><span data-stu-id="b1897-192">For example, in [Figure 8](#figure-8) the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

> ##### <span data-ttu-id="b1897-193">Figura 8</span><span class="sxs-lookup"><span data-stu-id="b1897-193">Figure 8</span></span>  
> <span data-ttu-id="b1897-194">Animações codificadas por cor</span><span class="sxs-lookup"><span data-stu-id="b1897-194">Color-coded animations</span></span>  
> ![Animações codificadas por cor][ImageColorCodedAnimations]  

## <span data-ttu-id="b1897-196">Modificar animações</span><span class="sxs-lookup"><span data-stu-id="b1897-196">Modify animations</span></span>   

<span data-ttu-id="b1897-197">Há três maneiras de modificar uma animação com o Inspetor de animação:</span><span class="sxs-lookup"><span data-stu-id="b1897-197">There are three ways you are able to modify an animation with the Animation Inspector:</span></span>  

*   <span data-ttu-id="b1897-198">Duração da animação.</span><span class="sxs-lookup"><span data-stu-id="b1897-198">Animation duration.</span></span>  
*   <span data-ttu-id="b1897-199">Intervalos do quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="b1897-199">Keyframe timings.</span></span>  
*   <span data-ttu-id="b1897-200">Intervalo de tempo de início.</span><span class="sxs-lookup"><span data-stu-id="b1897-200">Start time delay.</span></span>  

<span data-ttu-id="b1897-201">Para esta seção, suponha que a [Figura 9](#figure-9) represente a animação original:</span><span class="sxs-lookup"><span data-stu-id="b1897-201">For this section suppose that [Figure 9](#figure-9) represents the original animation:</span></span>  

> ##### <span data-ttu-id="b1897-202">Figura 9</span><span class="sxs-lookup"><span data-stu-id="b1897-202">Figure 9</span></span>  
> <span data-ttu-id="b1897-203">Animação original antes da modificação</span><span class="sxs-lookup"><span data-stu-id="b1897-203">Original animation before modification</span></span>  
> ![Animação original antes da modificação][ImageOriginalAnimationBeforeModification]  

<span data-ttu-id="b1897-205">Para alterar a duração de uma animação, clique e arraste o primeiro ou o último círculo.</span><span class="sxs-lookup"><span data-stu-id="b1897-205">To change the duration of an animation, click and drag the first or last circle.</span></span>  

> ##### <span data-ttu-id="b1897-206">Figura 10</span><span class="sxs-lookup"><span data-stu-id="b1897-206">Figure 10</span></span>  
> <span data-ttu-id="b1897-207">Duração modificada</span><span class="sxs-lookup"><span data-stu-id="b1897-207">Modified duration</span></span>  
> ![Duração modificada][ImageModifiedDuration]  

<span data-ttu-id="b1897-209">Se a animação define quaisquer regras de quadro-chave, elas são representadas como círculos internos brancos.</span><span class="sxs-lookup"><span data-stu-id="b1897-209">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="b1897-210">Clique e arraste uma destas para alterar o intervalo do quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="b1897-210">Click and drag one of these to change the timing of the keyframe.</span></span>  

> ##### <span data-ttu-id="b1897-211">Figura 11</span><span class="sxs-lookup"><span data-stu-id="b1897-211">Figure 11</span></span>  
> <span data-ttu-id="b1897-212">Quadro-chave modificado</span><span class="sxs-lookup"><span data-stu-id="b1897-212">Modified keyframe</span></span>  
> ![Quadro-chave modificado][ImageModifiedKeyframe]  

<span data-ttu-id="b1897-214">Para adicionar um atraso a uma animação, clique e arraste-a para qualquer lugar, exceto os círculos.</span><span class="sxs-lookup"><span data-stu-id="b1897-214">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

> ##### <span data-ttu-id="b1897-215">Figura 12</span><span class="sxs-lookup"><span data-stu-id="b1897-215">Figure 12</span></span>  
> <span data-ttu-id="b1897-216">Atraso modificado</span><span class="sxs-lookup"><span data-stu-id="b1897-216">Modified delay</span></span>  
> ![Atraso modificado][ImageModifiedDelay]  

<!--   -->  



<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: /microsoft-edge/devtools-guide-chromium/media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/replay-button-icon.msft.png  

[ImageAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-completed.msft.png "Figura 1: Inspetor de animação"  
[ImageAnimationsViaMainMenu]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-more-tools-animations.msft.png "Figura 2: animações via menu principal"  
[ImageEmptyAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations.msft.png "Figura 3: Inspetor de animação vazio"  
[ImageAnnotatedAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png "Figura 4: Inspetor de animação anotado"  
[ImageAnimationGroupDetails]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png "Figura 5: detalhes do grupo de animação"  
[ImageHoverOverAnimationHighlightViewport]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png "Figura 6: passe o mouse sobre a animação para realçá-la no visor"  
[ImageDiagramAnimationIterations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations-highlight.msft.png "Figura 7: diagrama de iterações de animação"  
[ImageColorCodedAnimations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations.msft.png "Figura 8: animações codificadas por cor"  
[ImageOriginalAnimationBeforeModification]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations.msft.png "Figura 9: animação original antes da modificação"  
[ImageModifiedDuration]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png "Figura 10: duração modificada"  
[ImageModifiedKeyframe]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png "Figura 11: quadro-chave modificado"  
[ImageModifiedDelay]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png "Figura 12: atraso modificado"  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="b1897-230">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="b1897-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b1897-231">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b1897-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b1897-233">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b1897-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
