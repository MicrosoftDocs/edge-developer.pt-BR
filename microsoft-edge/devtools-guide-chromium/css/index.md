---
description: Saiba como usar o Microsoft Edge DevTools para exibir e alterar a CSS de uma página.
title: Introdução à Visualização e Mudança da CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3cd833c97cb2e7b746943f18526d09481b4e3cc5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125206"
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

# Introdução à Visualização e Mudança da CSS  

Preencha esses tutoriais interativos para aprender as noções básicas de exibição e alteração do CSS para uma página usando o Microsoft Edge DevTools.  

## Exemplos de CSS abertos  

1.  Segure `Control` \ (Windows, Linux \) ou `Command` \ (MacOS \) e escolha **exemplos CSS** para abrir em uma nova janela.  
    
    [Exemplos de CSS][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Se você quiser [encaixar a janela do devtools][DevToolsCustomizePlacement] à direita do seu visor \ (exibido na figura \), escolha **Personalizar e controlar devtools** `...` .  No menu suspenso **Personalizar e controlar devtools** , na seção do lado do **encaixe** , escolha **encaixar à direita**.  
    
## Exibir o CSS de um elemento  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Passe o cursor do mouse sobre o `Inspect Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
    1.  No DevTools, no painel **elementos** , na guia **árvore DOM** , o `Inspect Me!` elemento é realçado.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           Figura 1: o elemento inspecionado é realçado na **árvore DOM**  
        :::image-end:::  
        
    1.  No `Inspect Me!` elemento, localize o valor do `data-message` atributo e copie-o.  
1.  Na página, no **valor de `data-message` :** TextBox, insira o valor.  
1.  Passe o cursor do mouse sobre o `Inspect Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
    1.  No DevTools, no painel **elementos** , selecione a guia **estilos** .  
    1.  Na guia **estilos** , o `Inspect Me!` elemento é realçado.  
    1.  No `Inspect Me!` elemento, localize a `aloha` regra de classe.  
        
        > [!NOTE]
        > Você vê esta regra porque ela está sendo aplicada ao `Inspect Me!` elemento.  
        
    1.  Na `aloha` classe, localize o valor para o `padding` estilo e copie-o.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Figura 2: as classes CSS aplicadas ao elemento selecionado, como, por exemplo `aloha` , são exibidas na guia **estilos**  
        :::image-end:::  
        
1.  Na página, no **valor de `padding` :** TextBox, insira o valor.  

## Adicionar uma declaração CSS a um elemento  

Use a guia **estilos** quando desejar alterar ou adicionar declarações CSS a um elemento.  

> [!NOTE]
> Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Passe o cursor do mouse sobre o `Add A Background Color To Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
1.  Selecione `element.style` próximo à parte superior da guia **estilos** .  
1.  Digite `background-color` e selecione `Enter` .  
1.  Digite `honeydew` e selecione `Enter` .  Na **árvore DOM** , você verá que uma declaração de estilo embutido foi aplicada ao elemento.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       Figura 3: a `background-color:honeydew` declaração foi aplicada ao elemento usando a `element.style` seção da guia **estilos**  
    :::image-end:::  
    
## Adicionar uma classe CSS a um elemento  

Use a guia **estilos** para ver como um elemento se parece quando uma classe CSS é aplicada a ou removida de um elemento.  

> [!NOTE]
> Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Passe o cursor do mouse sobre o `Add A Class To Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
1.  Choose **. CLS**.  DevTools revela uma caixa de texto onde você pode adicionar classes ao elemento selecionado.  
1.  Digite `color_me` na caixa de texto **Adicionar nova classe** e, em seguida, selecione `Enter` .  Uma caixa de seleção é exibida abaixo da caixa de texto **Adicionar nova classe** , em que você pode ativar e desativar a classe.  Se o `Add A Class To Me!` elemento tiver outras classes aplicadas a ele, você também poderá alternar entre eles.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       Figura 4: a `color_me` classe foi aplicada ao elemento usando a seção **. CLS** da guia **estilos**  
    :::image-end:::  
    
## Adicionar um PseudoState a uma classe  

Use a guia **estilos** para aplicar permanentemente um PseudoState CSS a um elemento.  DevTools dá suporte a `:active` ,, `:focus` `:hover` e `:visited` .  

> [!NOTE]
> Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Passe o mouse sobre o `Hover Over Me!` texto.  A cor do plano de fundo muda.  
1.  Passe o cursor do mouse sobre o `Hover Over Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
1.  Na guia **estilos** , escolha **: Hov**.  
1.  Marque a caixa de seleção **: hover** .  A cor do plano de fundo muda como antes, mesmo que você não esteja efetivamente passando o mouse sobre o elemento.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Figura 5: alternando o `:hover` pseudo-estado em um elemento  
    :::image-end:::  
    
## Alterar as dimensões de um elemento  

Use o diagrama interativo do **modelo de caixa** na guia **estilos** para alterar a largura, a altura, o enchimento, a margem ou o comprimento da borda de um elemento.  

> [!NOTE]
> Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.  

1.  [Exemplos de CSS abertos](#open-css-examples).  
1.  Passe o cursor do mouse sobre o `Change My Margin!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
1.  No diagrama de **modelo de caixa** na guia **estilos** , passe o mouse sobre o **preenchimento**.  O preenchimento de um elemento é realçado no visor.  

    > [!NOTE]
    > Dependendo do tamanho da janela do DevTools, talvez seja necessário rolar até a parte inferior da guia **estilos** para ver o **modelo de caixa**.  

1.  Clique duas vezes na margem esquerda no **modelo de caixa**, que atualmente tem um valor `-` que indica que o elemento não tem uma margem esquerda.  
1.  Digite `100px` e selecione `Enter` .  O **modelo de caixa** tem como padrão pixels, mas também aceita outros valores, como `25%` ou `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Figura 6: passando o cursor sobre o preenchimento do elemento  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Figura 7: alterando a margem esquerda do elemento  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Depuração de consultas de mídia  

As [consultas de mídia][MDNUsingMediaGueries] são uma maneira de fazer com que seu produto da Web reajam a alterações nas definições de configuração de cada usuário.  O caso de uso mais significativo é fornecer ao seu produto um layout CSS diferente, dependendo das dimensões do visor.  O uso de layouts separados permite um layout de uma coluna para dispositivos móveis e layouts de várias colunas quando há mais bens de tela disponíveis.  

Se você quiser depurar ou testar as consultas de mídia definidas em seu CSS, use as etapas a seguir.  

1.  Abra as ferramentas de desenvolvedor e selecione o ícone de **barra de ferramentas de alternância de dispositivo** em segundo lugar no canto superior esquerdo ou selecione `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` no MacOS \).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Figura 8: abrindo a barra de ferramentas do dispositivo  
    :::image-end:::  
    
1.  Com a barra de ferramentas do dispositivo aberta, selecione o `...` menu no canto superior direito e escolha **Exibir consultas de mídia**.  Você deve ver barras coloridas acima da exibição da página que representa as diferentes consultas de mídia.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Figura 9: mostrando consultas de mídia na barra de ferramentas do dispositivo  
    :::image-end:::  
    
1.  Passe o mouse sobre os limites nas barras para ver os valores das diferentes consultas de mídia. Selecione cada um para redimensionar a página da Web para corresponder.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Figura 10: selecionando consulta de mídia na barra de visualização  
    :::image-end:::  
    
1.  Para depurar consultas de mídia e abrir o arquivo CSS no `Sources` editor; passe o mouse sobre qualquer um dos segmentos de barras, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Figura 11: revelando consultas de mídia no editor de fontes  
    :::image-end:::  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemplos de CSS-Microsoft Edge (Chromium) DevTools | Problema"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usando consultas de mídia | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
