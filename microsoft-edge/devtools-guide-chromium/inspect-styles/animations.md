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





# Inspecionar animações   



Inspecione e modifique as animações com o Inspetor de animação do Microsoft Edge DevTools.  

> ##### Figura 1  
> Inspetor de animação  
> ![Inspetor de animação][ImageAnimationInspector]  

### Resumo  

*   Capture animações abrindo o Inspetor de animação.  O Inspetor de animação detecta e classifica automaticamente as animações em grupos.  
*   Inspecione as animações reduzindo cada uma, reproduzindo cada uma delas ou exibindo o código-fonte.  
*   Modifique as animações alterando o intervalo, atraso, duração ou deslocamentos de quadro-chave.  

## Visão geral   

O Inspetor de animação do Microsoft Edge DevTools tem duas finalidades principais.  

*   Inspecionar animações.  Você deseja diminuir a velocidade, reproduzir ou inspecionar o código-fonte de um grupo de animação.  
*   Modificação de animações.  Você deseja modificar o intervalo, atraso, duração ou deslocamentos de quadro-chave de um grupo de animação.  Não há suporte para a edição de Bezier e a edição de quadro-chave no momento.  

O Inspetor de animação dá suporte a animações CSS, transições CSS e animações da Web.  `requestAnimationFrame` Não há suporte para animações no momento.  

### O que é um grupo de animação?  

Um grupo de animação é um grupo de animações que pode estar relacionado entre si.  Atualmente, a Web não tem um conceito real de uma animação de grupo, portanto, os designers e desenvolvedores de animação devem compor e cronometrar animações individuais para que as animações sejam renderizadas como um efeito visual coerente.  O Inspetor de animação prevê quais animações estão relacionadas com base na hora de início \ (excluindo atrasos e assim por diante \).  O Inspetor de animação também agrupa as animações lado a lado.  
Em outras palavras, um conjunto de animações que são disparadas no mesmo bloco de script são agrupados juntos.  Se uma animação for assíncrona, ela será colocada em um grupo separado.  

## Introdução  

Há duas maneiras de abrir o Inspetor de animação:  

*   Abrir o menu **Personalizar e devtools de controle**  
    1.  Navegue até o submenu **mais ferramentas** .  
    1.  Selecionar **animações**:  
        
        > ##### Figura 2  
        > Animações via menu principal  
        > ![Animações via menu principal][ImageAnimationsViaMainMenu]  
        
*   Abrir o **menu de comandos**  
    1.  Digite `Drawer: Show Animations`.  

O Inspetor de animação é aberto como uma guia ao lado da gaveta do console.  Como o Inspetor de animação é uma guia gaveta, você pode usar o Inspetor de animação em qualquer painel do DevTools.  

> ##### Figura 3  
> Inspetor de animação vazio  
> ![Inspetor de animação vazio][ImageEmptyAnimationInspector]  

O Inspetor de animação está agrupado em quatro seções principais \ (ou painéis \).  Este guia se refere a cada painel da seguinte maneira:  

| | Painel | Descrição |  
| --- |:--- |:--- |  
| um | **Controles** | Aqui você pode limpar todos os grupos de animação capturados no momento ou alterar a velocidade do grupo de animações selecionado no momento. |  
| 2 | **Visão geral** | Selecione um grupo de animação aqui para inspecioná-lo e modificá-lo no painel **detalhes** . |  
| 3D | **Linha do Tempo** | Pause e inicie uma animação aqui, ou vá até um ponto específico na animação. |  
| 4 | **Detalhes** | Inspecionar e modificar o grupo de animações selecionado no momento. |  

> ##### Figura 4  
> Inspetor de animação com anotações  
> ![Inspetor de animação com anotações][ImageAnnotatedAnimationInspector]  

Para capturar uma animação, basta executar a interação que aciona a animação enquanto o Inspetor de animação está aberto.  Se uma animação for disparada na carga da página, recarregue a página com o Inspetor de animação aberto para detectar a animação.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## Inspecionar animações   

Depois de capturar uma animação, há algumas maneiras de reproduzi-la:  

*   Passe o mouse sobre a miniatura no painel **visão geral** para exibir uma visualização dela.  
*   Selecione o grupo animação no painel de **visão geral** \ (para que ele seja exibido no painel de **detalhes** \) e pressione **o** ![ ícone do ícone reproduzir reprodução ][ImageReplayButtonIcon] .  A animação é reproduzida no visor.  Clique nos ícones de velocidade da animação **velocidade** da animação ![ ][ImageAnimationSpeedButtonsIcon] ícones para alterar a velocidade de visualização do grupo de animações selecionado no momento.  Você pode usar a barra vertical vermelha para alterar a posição atual.  
*   Clique e arraste a barra vertical vermelha para limpar a animação do visor.  

### Exibir detalhes da animação  

Depois de capturar um grupo de animação, clique nele no painel **visão geral** para ver os detalhes.  No painel de **detalhes** , cada animação individual recebe a atribuição de uma linha.  

> ##### Figura 5  
> Detalhes do grupo animação  
> ![Detalhes do grupo animação][ImageAnimationGroupDetails]  

Passe o mouse sobre uma animação para realçá-la no visor.  Clique na animação para selecioná-la no painel de **elementos** .  

> ##### Figura 6  
> Passe o mouse sobre a animação para realçá-la no visor  
> ![Passe o mouse sobre a animação para realçá-la no visor][ImageHoverOverAnimationHighlightViewport]  

A seção mais à esquerda de uma animação é a definição.  A seção direita e mais esmaecida representa iterações.  Por exemplo, na [Figura 7](#figure-7), as seções dois e três representam iterações da seção um.  

> ##### Figura 7  
> Diagrama de iterações de animação  
> ![Diagrama de iterações de animação][ImageDiagramAnimationIterations]  

Se dois elementos tiverem a mesma animação aplicada, o Inspetor de animação atribuirá a mesma cor aos elementos.  A cor é aleatória e não tem importância.  Por exemplo, na [Figura 8](#figure-8) , os dois elementos `div.cwccw.earlier` e `div.cwccw.later` têm a mesma animação \ ( `spinrightleft` \) aplicada, como os `div.ccwcw.earlier` elementos e `div.ccwcw.later` .  

> ##### Figura 8  
> Animações codificadas por cor  
> ![Animações codificadas por cor][ImageColorCodedAnimations]  

## Modificar animações   

Há três maneiras de modificar uma animação com o Inspetor de animação:  

*   Duração da animação.  
*   Intervalos do quadro-chave.  
*   Intervalo de tempo de início.  

Para esta seção, suponha que a [Figura 9](#figure-9) represente a animação original:  

> ##### Figura 9  
> Animação original antes da modificação  
> ![Animação original antes da modificação][ImageOriginalAnimationBeforeModification]  

Para alterar a duração de uma animação, clique e arraste o primeiro ou o último círculo.  

> ##### Figura 10  
> Duração modificada  
> ![Duração modificada][ImageModifiedDuration]  

Se a animação define quaisquer regras de quadro-chave, elas são representadas como círculos internos brancos.  Clique e arraste uma destas para alterar o intervalo do quadro-chave.  

> ##### Figura 11  
> Quadro-chave modificado  
> ![Quadro-chave modificado][ImageModifiedKeyframe]  

Para adicionar um atraso a uma animação, clique e arraste-a para qualquer lugar, exceto os círculos.  

> ##### Figura 12  
> Atraso modificado  
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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
