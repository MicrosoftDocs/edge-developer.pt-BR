---
description: Saiba como usar o Microsoft Edge DevTools para exibir e alterar o CSS de uma página.
title: Introdução à visualização e mudança da CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: b3d19d34f329fec7a3903fb37e8be3558ba4d31d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399089"
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

# <a name="get-started-with-viewing-and-changing-css"></a>Introdução à visualização e mudança da CSS  

Conclua estes tutoriais interativos para aprender os conceitos básicos de exibição e alteração do CSS para uma página usando o Microsoft Edge DevTools.  

## <a name="open-css-examples"></a>Exemplos de CSS abertos  

1.  Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e escolha **Exemplos CSS** para abrir em uma nova janela.  
    
    [Exemplos CSS][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Se você quiser encaixar sua janela [DevTools][DevToolsCustomizePlacement] à direita do visor \(exibido na figura a seguir\), escolha Personalizar e controlar **DevTools** `...` .  No menu **suspenso Personalizar e controlar DevTools,** na seção Lado **do** Encaixe, escolha **Doca para a direita**.  
    
## <a name="view-the-css-for-an-element"></a>Exibir o CSS para um elemento  

1.  [Abra exemplos css](#open-css-examples).  
1.  Passe o mouse `Inspect Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
    1.  No DevTools, na **ferramenta Elementos,** no painel **Árvore DOM,** o `Inspect Me!` elemento é realçado.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           O elemento inspecionado é realçado na árvore **DOM**  
        :::image-end:::  
        
    1.  No `Inspect Me!` elemento, encontre o valor do `data-message` atributo e copie-o.  
1.  Na página, na caixa **de texto Valor de `data-message` :** , insira o valor.  
1.  Passe o mouse `Inspect Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
    1.  No DevTools, na ferramenta **Elementos,** selecione o **painel Estilos.**  
    1.  No painel **Estilos,** o `Inspect Me!` elemento é realçado.  
    1.  No `Inspect Me!` elemento, encontre a `aloha` regra de classe.  
        
        > [!NOTE]
        > Essa regra é exibida porque está sendo aplicada ao `Inspect Me!` elemento.  
        
    1.  Na `aloha` classe, encontre o valor do `padding` estilo e copie-o.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Classes CSS são aplicadas ao elemento inspecionado são realçadas no painel Estilos" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Classes CSS são aplicadas ao elemento selecionado, como `aloha` , são exibidas no painel **Estilos**  
        :::image-end:::  
        
1.  Na página, na caixa **de texto Valor de `padding` :** , insira o valor.  

## <a name="add-a-css-declaration-to-an-element"></a>Adicionar uma declaração CSS a um elemento  

Use o **painel Estilos** quando quiser alterar ou adicionar declarações CSS a um elemento.  

> [!NOTE]
> Conclua [o tutorial Exibir o CSS para um](#view-the-css-for-an-element) elemento antes de fazer este.  

1.  [Abra exemplos css](#open-css-examples).  
1.  Passe o mouse `Add A Background Color To Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
1.  Escolha `element.style` perto da parte superior do painel **Estilos.**  
1.  Digite `background-color` e selecione `Enter` .  
1.  Digite `honeydew` e selecione `Enter` .  Na Árvore **DOM,** uma declaração de estilo em linha aplicada ao elemento é exibida.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Adicionar uma declaração CSS ao elemento usando o painel Estilos" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       A `background-color:honeydew` declaração é aplicada ao elemento usando a seção do painel `element.style` **Estilos**  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a>Adicionar uma classe CSS a um elemento  

Para exibir a aparência de um elemento quando uma classe CSS é aplicada ou removida de um elemento, navegue até o **painel Estilos.**  

> [!NOTE]
> Conclua [o tutorial Exibir o CSS para um](#view-the-css-for-an-element) elemento antes de fazer este.  

1.  [Abra exemplos css](#open-css-examples).  
1.  Passe o mouse `Add A Class To Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
1.  Escolha **.cls**.  DevTools revela uma caixa de texto onde você pode adicionar classes ao elemento selecionado.  
1.  Digite `color_me` a caixa de texto Adicionar **nova** classe e selecione `Enter` .  Uma caixa de seleção é exibida abaixo da caixa de texto **Adicionar nova** classe, onde você pode alternar a classe para cima e para baixo.  Se o elemento tiver outras classes aplicadas a ele, você também poderá `Add A Class To Me!` alternar cada uma delas daqui.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Aplicar a color_me ao elemento" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       A `color_me` classe é aplicada ao elemento usando a seção **.cls** do painel **Estilos**  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a>Adicionar um pseudostate a uma classe  

Use o **painel Estilos** para aplicar permanentemente um pseudostate CSS a um elemento.  O DevTools dá `:active` suporte a , e `:focus` `:hover` `:visited` .  

> [!NOTE]
> Conclua [o tutorial Exibir o CSS para um](#view-the-css-for-an-element) elemento antes de fazer este.  

1.  [Abra exemplos css](#open-css-examples).  
1.  Passe o mouse no `Hover Over Me!` texto.  A cor do plano de fundo muda.  
1.  Passe o mouse `Hover Over Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
1.  No painel **Estilos,** escolha **:hov**.  
1.  Marque a **caixa de seleção :hover.**  A cor do plano de fundo muda como antes, mesmo que você não está realmente pairando sobre o elemento.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Alternar o pseudostate de foco em um elemento" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Alternar o `:hover` pseudostate em um elemento  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a>Alterar as dimensões de um elemento  

Use o **diagrama interativo Modelo** de Caixa no painel **Estilos** para alterar a largura, altura, preenchimento, margem ou comprimento da borda de um elemento.  

> [!NOTE]
> Conclua [o tutorial Exibir o CSS para um](#view-the-css-for-an-element) elemento antes de fazer este.  

1.  [Abra exemplos css](#open-css-examples).  
1.  Passe o mouse `Change My Margin!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
1.  No diagrama **Modelo de** Caixa no painel **Estilos,** passe o mouse sobre **preenchimento**.  O preenchimento de um elemento é realçado no viewport.  

    > [!NOTE]
    > Dependendo do tamanho da janela DevTools, talvez seja necessário rolar até a parte inferior do painel **Estilos** para exibir **o Modelo de Caixa**.  

1.  Clique duas vezes na margem esquerda no **Modelo**de Caixa , que atualmente tem um valor de significado de que o elemento não `-` tem uma margem esquerda.  
1.  Digite `100px` e selecione `Enter` .  O **Modelo de Caixa** é padrão para pixels, mas também aceita outros valores, como , ou `25%` `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Passe o mouse no preenchimento do elemento" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Passe o mouse no preenchimento do elemento  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Alterar a margem esquerda do elemento" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Alterar a margem esquerda do elemento  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a>Depuração de consultas de mídia  

[Consultas de mídia][MDNUsingMediaGueries] são uma maneira de fazer com que seu produto Web reaja às alterações nas configurações de cada usuário.  O caso de uso mais significativo é fornecer ao seu produto um layout CSS diferente, dependendo das dimensões do modo de exibição.  O uso de layouts separados permite um layout de uma coluna para dispositivos móveis e layouts de várias colunas quando há mais propriedades de tela disponíveis.  

Se você quiser depurar ou testar as Consultas de Mídia definidas em seu CSS, use as etapas a seguir.  

1.  Abra as ferramentas do desenvolvedor e selecione o ícone da barra de ferramentas do dispositivo **De** alternar segundo na parte superior esquerda ou selecione `Ctrl` + `Shift` + `M` \( `Cmd` + `Shift` + `M` no macOS\).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Abra a barra de ferramentas do dispositivo" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Abra a barra de ferramentas do dispositivo  
    :::image-end:::  
    
1.  Com a barra de ferramentas do dispositivo aberta, selecione o menu na `...` parte superior direita e escolha Exibir Consultas de **Mídia**.  As barras coloridas exibidas acima da página da Web representam as diferentes consultas de mídia.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Mostrar consultas de mídia na barra de ferramentas do dispositivo" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Mostrar consultas de mídia na barra de ferramentas do dispositivo  
    :::image-end:::  
    
1.  Passe o mouse nos limites nas barras para exibir os valores das diferentes consultas de mídia.  Escolha cada um para reorganizar a página da Web para corresponder.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Escolha Consulta de Mídia na barra de visualização" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Escolha Consulta de Mídia na barra de visualização  
    :::image-end:::  
    
1.  Para depurar consultas de mídia e abrir o arquivo CSS no editor; passe o mouse em qualquer um dos segmentos de barra, abra o menu contextual \(clique com o botão direito `Sources` do mouse\) e selecione `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Revelar consultas de mídia no Editor de Fontes" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Revelar consultas de mídia no Editor de Fontes  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (Desfazer, Encaixar na Parte Inferior, Encaixe para a Esquerda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemplos css - Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usando consultas de mídia | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/css/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
