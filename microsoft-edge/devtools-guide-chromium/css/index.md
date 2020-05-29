---
title: Introdução à exibição e alteração de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601814"
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





# Introdução à exibição e alteração de CSS   



Preencha esses tutoriais interativos para aprender as noções básicas de exibição e alteração do CSS para uma página usando o Microsoft Edge DevTools.  

## Exemplos de CSS abertos  

1.  Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos CSS** para abrir em uma nova janela.  
    
    [Exemplos de CSS][GlitchDevToolsCssExamples]  

> [!NOTE]
> Se você quiser [encaixar a janela do devtools][DevToolsCustomizePlacement] à direita do seu visor \ (exibido na [Figura 1](#figure-1)\), clique em **Personalizar e controlar o devtools** `...` .  No menu suspenso **Personalizar e controlar devtools** , na seção do lado do **encaixe** , selecione **encaixar à direita**.  
    
## Exibir o CSS de um elemento   

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Clique com o botão direito do mouse no `Inspect Me!` texto e selecione **inspecionar**.  
    1.  No DevTools, no painel **elementos** , na guia **árvore DOM** , o `Inspect Me!` elemento é realçado.  
        
        > ##### Figura 1  
        > O elemento inspecionado é realçado na **árvore DOM**  
        > ![O elemento inspecionado é realçado na árvore DOM][ImageInspect]  
        
    1.  No `Inspect Me!` elemento, localize o valor do `data-message` atributo e copie-o.  
1.  Na página, no **valor de `data-message` :** TextBox, insira o valor.  
1.  Clique com o botão direito do mouse no `Inspect Me!` texto e selecione **inspecionar**.  
    
    1.  No DevTools, no painel **elementos** , selecione a guia **estilos** .  
    1.  Na guia **estilos** , o `Inspect Me!` elemento é realçado.  
    1.  No `Inspect Me!` elemento, localize a `aloha` regra de classe.  
        
        > [!NOTE]
        > Você vê esta regra porque ela está sendo aplicada ao `Inspect Me!` elemento.  
        
    1.  Na `aloha` classe, localize o valor para o `padding` estilo e copie-o.  
        
        > ##### Figura 2  
        > As classes CSS aplicadas ao elemento selecionado, como `aloha` , são exibidas na guia **estilos**  
        > ![As classes CSS aplicadas ao elemento inspecionado são realçadas na guia estilos][ImageAloha]  
        
1.  Na página, no **valor de `padding` :** TextBox, insira o valor.  

## Adicionar uma declaração CSS a um elemento   

Use a guia **estilos** quando desejar alterar ou adicionar declarações CSS a um elemento.  

> [!NOTE]
> Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Clique com o botão direito do mouse no `Add A Background Color To Me!` texto e selecione **inspecionar**.  
1.  Clique `element.style` próximo à parte superior da guia **estilos** .  
1.  Digite `background-color` e pressione `Enter` .  
1.  Digite `honeydew` e pressione `Enter` .  Na **árvore DOM** , você verá que uma declaração de estilo embutido foi aplicada ao elemento.  

> ##### Figura 3  
> A `background-color:honeydew` declaração foi aplicada ao elemento usando a `element.style` seção da guia **estilos**  
> ![Adicionando uma declaração CSS ao elemento usando a guia estilos][ImageDeclaration]  

## Adicionar uma classe CSS a um elemento   

Use a guia **estilos** para ver como um elemento se parece quando uma classe CSS é aplicada a ou removida de um elemento.  

> [!NOTE]
> Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Clique com o botão direito do mouse no `Add A Class To Me!` elemento e selecione **inspecionar**.  
1.  Clique em **. CLS**.  DevTools revela uma caixa de texto onde você pode adicionar classes ao elemento selecionado.  
1.  Digite `color_me` na caixa de texto **Adicionar nova classe** e pressione `Enter` .  Uma caixa de seleção é exibida abaixo da caixa de texto **Adicionar nova classe** , em que você pode ativar e desativar a classe.  Se o `Add A Class To Me!` elemento tiver outras classes aplicadas a ele, você também poderá alternar entre eles.  

> ##### Figura 4  
> A `color_me` classe foi aplicada ao elemento usando a seção **. CLS** da guia **estilos**  
> ![Aplicando a classe color_me ao elemento][ImageApplyClass]  

## Adicionar um PseudoState a uma classe   

Use a guia **estilos** para aplicar permanentemente um PseudoState CSS a um elemento.  DevTools dá suporte a `:active` ,, `:focus` `:hover` e `:visited` .  

> [!NOTE]
> Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Passe o mouse sobre o `Hover Over Me!` texto.  A cor do plano de fundo muda.  
1.  Clique com o botão direito do mouse no `Hover Over Me!` texto e selecione **inspecionar**.  
1.  Na guia **estilos** , clique em **: Hov**.  
1.  Marque a caixa de seleção **: hover** .  A cor do plano de fundo muda como antes, mesmo que você não esteja efetivamente passando o mouse sobre o elemento.  

> ##### Figura 5  
> Alternando o `:hover` PseudoState em um elemento  
> ![Alternando o PseudoState de foco em um elemento][ImageSetHover]  

## Alterar as dimensões de um elemento   

Use o diagrama interativo do **modelo de caixa** na guia **estilos** para alterar a largura, a altura, o enchimento, a margem ou o comprimento da borda de um elemento.  

> [!NOTE]
> Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Clique com o botão direito do mouse no `Change My Margin!` elemento e selecione **inspecionar**.  
1.  No diagrama de **modelo de caixa** na guia **estilos** , passe o mouse sobre o **preenchimento**.  O preenchimento de um elemento é realçado no visor.  

    > [!NOTE]
    > Dependendo do tamanho da janela do DevTools, talvez seja necessário rolar até a parte inferior da guia **estilos** para ver o **modelo de caixa**.  

1.  Clique duas vezes na margem esquerda no **modelo de caixa**, que atualmente tem um valor `-` que indica que o elemento não tem uma margem esquerda.  
1.  Digite `100px` e pressione `Enter` .  O **modelo de caixa** tem como padrão pixels, mas também aceita outros valores, como `25%` ou `10vw` .  

> ##### Figura 6  
> Passando o cursor sobre o preenchimento do elemento  
> ![Passando o cursor sobre o preenchimento do elemento][ImageShowPadding]  

> ##### Figura 7  
> Alterar a margem esquerda do elemento  
> ![Alterar a margem esquerda do elemento][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Figura 1: o elemento inspecionado é realçado na árvore DOM"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Figura 2: as classes CSS aplicadas ao elemento inspecionado são realçadas na guia estilos"  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Figura 3: adicionando uma declaração CSS ao elemento usando a guia estilos"  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Figura 4: aplicando a classe color_me ao elemento"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Figura 5: alternando o pseudo-passe de hover em um elemento"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Figura 6: passando o cursor sobre o preenchimento do elemento"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Figura 7: alterando a margem esquerda do elemento"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemplos de CSS-Microsoft Edge (Chromium) DevTools | Problema"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
