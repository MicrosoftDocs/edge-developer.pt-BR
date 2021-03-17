---
description: Inspecionar e modificar animações com o Inspetor de Animação do Microsoft Edge DevTools.
title: Inspecionar animações
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: dba948087ca06015f686d17ba48584199373805a
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439539"
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

# <a name="inspect-animations"></a>Inspecionar animações  

Inspecionar e modificar animações com o Inspetor de Animação do Microsoft Edge DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspetor de animação" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   inspetor de animação  
:::image-end:::  

### <a name="summary"></a>Resumo  

*   Capture animações abrindo o Inspetor de Animação.  O Inspetor de Animação detecta automaticamente e classifica animações em grupos.  
*   Inspecione animações diminuindo cada uma delas, reprisando cada uma ou exibindo o código-fonte.  
*   Modifique animações alterando os deslocamentos de tempo, atraso, duração ou estrutura de chaves.  

## <a name="overview"></a>Visão geral  

O Inspetor de Animação do Microsoft Edge DevTools tem duas finalidades principais.  

*   Inspecionando animações.  Você deseja reduzir a velocidade, repetir ou inspecionar o código-fonte de um Grupo de Animação.  
*   Modificando animações.  Você deseja modificar os deslocamentos de tempo, atraso, duração ou estrutura de chaves de um Grupo de Animação.  No momento, a edição do Bezier e a edição de estrutura de chave não são suportadas.  

O Inspetor de Animação dá suporte a animações CSS, transições CSS e animações da Web.  `requestAnimationFrame` no momento, não há suporte para animações.  

### <a name="what-is-an-animation-group"></a>O que é um Grupo de Animação?  

Um Grupo de Animação é um grupo de animações que pode estar relacionado uns aos outros.  Atualmente, a Web não tem um conceito real de animação de grupo, portanto, designers de movimento e desenvolvedores devem compor e temporizar animações individuais para que as animações renderizarem como um efeito visual coerente.  O Inspetor de Animação prevê quais animações estão relacionadas com base na hora de início \(excluindo atrasos e assim por diante\).  O Inspetor de Animação também grupos as animações lado a lado.  
Em outras palavras, um conjunto de animações que são todas disparadas no mesmo bloco de scripts são agrupadas.  Se uma animação for assíncrona, ela será colocada em um grupo separado.  

## <a name="get-started"></a>Introdução  

Há duas maneiras de abrir o Inspetor de Animação:  

*   Abra o **menu Personalizar e Controlar DevTools**  
    1.  Navegue até o sub menu **Mais** ferramentas.  
    1.  Escolha **Animações**:  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animações usando o Menu Principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Animações usando** o Menu Principal  
    :::image-end:::  
        
*   Abra o **Menu de Comando**  
    1.  Digite `Drawer: Show Animations`.  

O Inspetor de Animação abre ao lado da **ferramenta Console.**  Como o Inspetor de Animação é uma ferramenta Drawer, você pode usar o Inspetor de Animação de qualquer painel DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspetor de Animação Vazia" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Inspetor de Animação Vazia  
:::image-end:::  

O Inspetor de Animação é agrupado em quatro seções principais \(ou painéis\).  Este guia se refere a cada painel da seguinte forma:  

| Índice | Painel | Descrição |  
|:--- |:--- |:--- |  
| 1 | **Controles** | A partir daqui, você pode limpar todos os Grupos de Animação capturados no momento ou alterar a velocidade do Grupo de Animação atualmente selecionado. |  
| 2 | **Visão geral** | Escolha um Grupo de Animação aqui para inspecionar e modificá-lo no painel **Detalhes.** |  
| 3 | **Linha do Tempo** | Pause e inicie uma animação a partir daqui ou pule para um ponto específico na animação. |  
| 4 | **Detalhes** | Inspecionar e modificar o Grupo de Animação selecionado no momento. |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspetor de animação anotado" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Inspetor de animação anotado  
:::image-end:::  

Para capturar uma animação, basta executar a interação que dispara a animação enquanto o Inspetor de Animação está aberto.  Se uma animação for disparada no carregamento da página, atualize a página com o Inspetor de Animação aberto para detectar a animação.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a>Inspecionar animações  

Depois de capturar uma animação, há algumas maneiras de replay dela:  

*   Passe o mouse na miniatura no painel **Visão** geral para exibir uma visualização dela.  
*   Escolha o Grupo **** de Animação no painel Visão geral \(para que ele seja exibido no **painel** Detalhes\) e escolha o ícone de **repetição** \( ícone de ![ repetição ](../media/replay-button-icon.msft.png) \).  A animação é reprisada no viewport.  Escolha os **ícones de** velocidade de animação \( ícones de velocidade de ![ animação \) para alterar a velocidade de visualização do Grupo de Animação selecionado ](../media/animation-speed-buttons-icon.msft.png) no momento.  Você pode usar a barra vertical vermelha para alterar sua posição atual.  
*   Escolha e arraste a barra vertical vermelha para limpar a animação do viewport.  
    
### <a name="view-animation-details"></a>Exibir detalhes da animação  

Depois de capturar um Grupo de Animação, escolha-o no painel **Visão** geral para exibir os detalhes.  No painel **Detalhes,** cada animação individual é atribuída a uma linha.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Detalhes do Grupo de Animação" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Detalhes do Grupo de Animação  
:::image-end:::  

Passe o mouse em uma animação para realça-la no viewport.  Escolha a animação para selecioná-la na **ferramenta Elementos.**  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Passe o mouse na animação para realça-la no viewport" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Passe o mouse na animação para realça-la no viewport  
:::image-end:::  

A seção mais à esquerda e mais escura de uma animação é a definição.  A seção à direita, mais desbotada representa iterações.  Por exemplo, na figura a seguir, as seções dois e três representam iterações da seção um.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagrama de iterações de animação" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Diagrama de iterações de animação  
:::image-end:::  

Se dois elementos têm a mesma animação aplicada, o Inspetor de Animação atribui a mesma cor aos elementos.  A cor é aleatória e não tem significância.  Por exemplo, na figura a seguir, os dois elementos e têm a mesma animação `div.cwccw.earlier` `div.cwccw.later` \( `spinrightleft` \) aplicada, assim como os `div.ccwcw.earlier` elementos `div.ccwcw.later` e.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animações codificadas por cores" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Animações codificadas por cores  
:::image-end:::  

## <a name="modify-animations"></a>Modificar animações  

Há três maneiras de modificar uma animação com o Inspetor de Animação.  

*   Duração da animação.  
*   Períodos de estrutura de chaves.  
*   Iniciar atraso de tempo.  
    
Na figura a seguir, a animação original é representada.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animação original antes da modificação" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Animação original antes da modificação  
:::image-end:::  

Para alterar a duração de uma animação, escolha e arraste o primeiro ou último círculo.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Duração modificada" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Duração modificada  
:::image-end:::  

Se a animação definir qualquer regra de estrutura de chaves, elas serão representadas como círculos internos em branco.  Escolha e arraste um desses para alterar o tempo do keyframe.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Keyframe modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Keyframe modificado  
:::image-end:::  

Para adicionar um atraso a uma animação, escolha e arraste-a em qualquer lugar, exceto os círculos.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Atraso modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Atraso modificado  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

(.. /media/animation-speed-buttons-icon.msft.png): .. /media/animation-speed-buttons-icon.msft.png  
(.. /media/replay-button-icon.msft.png): .. /media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
