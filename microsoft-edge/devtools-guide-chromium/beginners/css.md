---
description: Introdução css
title: 'DevTools para iniciantes: Começar com CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools
ms.openlocfilehash: 6f34cfa8610848505c8aa795c4fab16e5d2a98ed
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564641"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="devtools-for-beginners-get-started-with-css"></a>DevTools para iniciantes: Começar com CSS  

Neste tutorial, você aprenderá a usar CSS para estilo de uma página da Web.  Você também aprenderá a usar o Microsoft Edge DevTools para experimentar alterações CSS.  

O artigo a seguir é o segundo tutorial de uma série de tutoriais que ensina as noções básicas de desenvolvimento da Web e Microsoft Edge DevTools.  Você ganha experiência prática criando seu próprio site.  Não é preciso concluir o primeiro tutorial antes de seguir o segundo.  [Configurar seu código](#set-up-your-code) mostra como configurar.  

> [!NOTE]
> Este tutorial foi projetado para iniciantes absolutos e se concentra nos fundamentos do desenvolvimento da Web e noções **básicas** de como usar o DevTools para experimentar CSS.  Se você quiser um tutorial que se concentre apenas no DevTools, navegue até Introdução [exibindo e alterando CSS][DevtoolsCssIndex].  

No início do tutorial, seu site deve ter a aparência da figura a seguir.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Qual é a aparência do seu site no momento" lightbox="../media/beginners-css-intro1.msft.png":::
   Qual é a aparência do seu site no momento  
:::image-end:::  

Depois de concluir o tutorial, o site deve ter a aparência da figura a seguir.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Como seu site deve ser no final do tutorial" lightbox="../media/beginners-css-intro2.msft.png":::
   Como seu site deve ser no final do tutorial  
:::image-end:::  

## <a name="goals"></a>Metas  

Siga este tutorial para entender melhor os seguintes conceitos e tarefas.  

*   Como usar CSS para estilar uma página da Web.  
*   Como usar Microsoft Edge DevTools para experimentar CSS.  
*   A diferença entre estruturas CSS e CSS.  

Você está criando um site real.  

## <a name="prerequisites"></a>Pré-requisitos  

Antes de tentar este tutorial, conclua os seguintes pré-requisitos.  

*   Conclua [Introdução com HTML][DevtoolsBeginnersHtml] e o DOM ou certifique-se de que você tenha um entendimento sobre HTML e o DOM semelhantes ao que é ministrado nesse tutorial.  
*   Baixe o [Microsoft Edge][MicrosoftEdgeInsider] da Web.  O tutorial a seguir usa um conjunto de ferramentas de desenvolvimento da Web, chamada Microsoft Edge DevTools, que são criadas em Microsoft Edge.  

## <a name="set-up-your-code"></a>Configurar seu código  

Para criar seu site, você deve primeiro concluir as seguintes ações para configurar seu código.  

> [!NOTE]
> Se você já concluiu o primeiro tutorial da série, pule para a próxima seção.  Continue usando seu código do último tutorial, Introdução [html e dom][DevtoolsBeginnersHtml].  

1.  Abra o [código-fonte][GlitchCookedAmphibianIndex].  A guia em foco do navegador é referenciada como a **guia de edição**.  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="A guia edição" lightbox="../media/beginners-css-setup1.msft.png":::
       A **guia edição**  
    :::image-end:::  
    
1.  Escolha **cooked-amphibian**.  Um menu é aberto.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="O menu Project opções" lightbox="../media/beginners-css-setup2.msft.png":::
       O menu Project opções  
    :::image-end:::  

1.  Escolha **Mesclar Project**.  A falha cria uma cópia do projeto que você pode editar.  
    
    > [!NOTE]
    > A falha gera um nome aleatório para o novo projeto.  
    
1.  Escolha **Mostrar** e escolher **Em uma nova janela**.  Outra guia é aberta com uma exibição ao vivo do seu site.  A guia em foco do navegador é referenciada como a **guia ao vivo**.  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="A guia ao vivo" lightbox="../media/beginners-css-setup3.msft.png":::
       A **guia ao vivo**  
    :::image-end:::  

## <a name="understand-css"></a>Entender CSS  

**CSS** é uma linguagem de computador que determina o layout e o estilo de páginas da Web.  A figura a seguir é um parágrafo com uma borda.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="O texto foi estilado com CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   O texto foi estilado com CSS  
:::image-end:::  

O trecho de código a seguir é o código HTML e CSS usado para criar o parágrafo na figura anterior.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` provavelmente parece novo para você.  O restante deve parecer familiar.  Caso não, [conclua Introdução html e o DOM][DevtoolsBeginnersHtml] antes de tentar as seções a seguir.  

## <a name="add-inline-styles"></a>Adicionar estilos em linha  

Conclua as seguintes ações para usar **estilos em linha** para aplicar estilos a um único elemento.  

1.  Volte para a guia edição e abra `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       Abra `index.html` na guia edição  
    :::image-end:::  
    
1.  Adicione `style="background-color: aliceblue;"` ao `<nav>` seu .  No bloco de código abaixo, a quarta linha de código é a que você precisa alterar.  O restante está apenas lá, portanto, você pode garantir que você está colocando o novo código no lugar certo.  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  Para exibir as alterações, navegue até a **guia ao vivo**.  O plano de fundo `<nav>` da seção agora está azul.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="A cor do plano de fundo por trás dos links Home e Contact agora é azul" lightbox="../media/beginners-css-inline2.msft.png":::
       A cor do plano de fundo por trás dos links **Home** e **Contact** agora é azul  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a>Rea uso de estilos em uma única página com folhas de estilos internas  

Em um trecho de código anterior, um estilo em linha aplicava um estilo a uma única `<p>` marca.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

E se você quiser que todos os `<p>` elementos em sua página da Web sejam estilados da mesma maneira?  Você precisa copiar e colar o código em cada marca `<p>` única em seu site.  Isso é muito tempo e esforço.  E, se você precisar fazer uma edição, terá que alterar cada marca novamente.  Conclua as seguintes ações para usar **uma folha de** estilos Interna para gravar o CSS uma vez para que ela se aplique a vários elementos.  

1.  Na guia ao vivo, escolha **Contato** para navegar até a página de contato.  Observe a fonte de **Home** e **Contact**.  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="A página Contato" lightbox="../media/beginners-css-internal1.msft.png":::
       A página Contato  
    :::image-end:::  
    
1.  Na **guia editor,** abra `contact.html` .  
1.  Adicione o código a seguir a `contact.html` .  Lembre-se de que as linhas que começam `<style>` com e terminam `</style>` com são o que você precisa adicionar.  O outro código está apenas lá para que você saiba onde colocar o novo código.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  Volte para a **guia ao vivo**.  
1.  Escolha **Contato** para voltar à página de contato.  A fonte de **Home** e **Contact** foi alterada.  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="A fonte dos links Home e Contact foi alterada" lightbox="../media/beginners-css-internal2.msft.png":::
       A fonte dos links **Home** e **Contact** foi alterada  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a>Compreender folhas de estilos internas  

As folhas de estilos internas aplicam estilos usando **seletores**.  Seletores são padrões que podem se aplicar a um ou mais elementos HTML.  O trecho de código anterior adicionou o seguinte estilo.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` é um seletor que se converte em "qualquer `<li>` elemento que contenha um `<a>` elemento".  O navegador altera a fonte dos links **Home** e **Contact** porque cada um dos grupos de marca corresponder ao padrão.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` é uma **declaração**.  Uma declaração é feita de duas partes a seguir.  

:::row:::
   :::column span="1":::
      **property**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      A propriedade descreve uma maneira geral de você poder alterar o estilo do elemento.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **value**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      O valor descreve exatamente como o estilo do elemento deve mudar.  
   :::column-end:::
:::row-end:::  

Por exemplo, `font-family: 'Courier New', Courier, serif` fornece ao navegador a seguinte instrução: "Definir a fonte de elementos que corresponderem ao padrão como `li a` `'Courier New'` .  Se essa fonte não estiver disponível, use `Courier` .  Se isso não estiver disponível, use `serif` ."  

### <a name="add-multiple-selectors-to-a-ruleset"></a>Adicionar vários seletores a um ruleset  

Um bloco de código CSS como o trecho de código a seguir é chamado de **ruleset**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Conclua as seguintes ações para usar vírgulas para adicionar vários seletores a um ruleset.  

1.  Na **guia editor,** abra `contact.html` .  
1.  Após `li a` o tipo `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    O trecho de código anterior informa ao navegador os elementos de estilo da mesma maneira que ele estilos `<h1>` os elementos que corresponderem ao padrão `li a` .  
    
1.  Navegue até **a guia ao vivo**.  
1.  Escolha o link **Contato** para voltar à página de contato.  Agora, **entre em contato comigo!** tem a mesma fonte dos links de navegação.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="O texto Fale comigo!  agora tem a mesma fonte que os links Home e Contact" lightbox="../media/beginners-css-multiple1.msft.png":::
       O texto **Fale comigo!** agora tem a mesma fonte que os links **Home** e **Contact**  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a>Experimento com DevTools  

À medida que você continua sua jornada para se tornar um especialista em desenvolvimento da Web, você pode descobrir que CSS é complicado.  Você pode escrever alguns CSS e esperar que ele seja exibido de uma maneira, mas o navegador faz algo completamente diferente.  Microsoft Edge O DevTools facilita o experimento com alterações e exibe imediatamente como as alterações afetam a página.  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a>Adicionar uma declaração a um rulest existente no DevTools  

Conclua as seguintes ações para iterar no estilo de um elemento existente, adicione uma declaração a um ruleset existente.  

1.  Passe o **mouse** no link Home, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspecionar o link Home" lightbox="../media/beginners-css-add1.msft.png":::
       Inspecionar o link Home  
    :::image-end:::  
    
    O DevTools abre junto com sua página.  O código que representa o link Home é `<a href="/">Home</a>` realçado em azul na Árvore DOM.  O trecho de código e a visualização devem estar familiarizados Introdução [html e dom][DevtoolsBeginnersHtml].  
    
    :::row:::
       :::column span="":::
          Na figura a seguir, a declaração à qual você adicionou anteriormente é exibida na `font-family: 'Courier New', Courier, serif` guia Estilos abaixo da árvore `contact.html` DOM. ****  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="A guia Estilos está abaixo da árvore DOM" lightbox="../media/beginners-css-add2.msft.png":::
             A **guia Estilos** está abaixo da árvore DOM  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Se sua janela DevTools for ampla, a guia Estilos será à direita da árvore DOM.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="A guia Estilos fica à direita da árvore DOM" lightbox="../media/beginners-css-add3.msft.png":::
             A **guia Estilos** fica à direita da árvore DOM  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Escolha a linha vazia abaixo `font-family: 'Courier New', Courier, Serif` para adicionar uma nova declaração.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Adicionar uma nova declaração" lightbox="../media/beginners-css-add4.msft.png":::
       Adicionar uma nova declaração  
    :::image-end:::  
    
1.  Digite `color` e selecione `Enter` .  A interface do usuário de preenchimento automático sugere opções conforme você digita.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Cor do tipo" lightbox="../media/beginners-css-add5.msft.png":::
       Tipo `color`  
    :::image-end:::  
    
1.  Digite `magenta` e selecione `Enter` .  Todo o texto na página de contato agora é magenta.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Digite magenta" lightbox="../media/beginners-css-add6.msft.png":::
       Tipo `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a>Editar uma declaração no DevTools  

Conclua as seguintes ações para editar declarações existentes no DevTools.  

1.  Escolha o quadrado magenta ao lado de `magenta` .  Um se picker de cores aparece.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="O Se picker de cores" lightbox="../media/beginners-css-edit1.msft.png":::
       O Se picker de cores  
    :::image-end:::  
    
1.  Use o se picker de cores para alterar o texto da fonte para uma cor que você gosta.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Altere a cor da fonte para roxo com o Selador de Cores" lightbox="../media/beginners-css-edit2.msft.png":::
       Altere a cor da fonte para roxo com o Selador de Cores  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a>Adicionar um novo conjunto de regras no DevTools  

Conclua as seguintes ações para adicionar novos rulesets no DevTools.  

1.  Escolha **Nova Regra de Estilo** \( Nova Regra de Estilo ![ ](../media/new-style-rule-icon.msft.png) \) que está ao lado de **.cls**.  Um ruleset vazio é exibido `a` como seletor.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Adicionar uma nova regra" lightbox="../media/beginners-css-rule1.msft.png":::
       Adicionar uma nova regra  
    :::image-end:::  
    
1.  Substitua `a` por `a:hover` .  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Substituir um por um:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       Substituir `a` por `a:hover`  
    :::image-end:::  
    
    `:hover` é uma **pseudo-classe**.  Use pseudo classes para elementos de estilo que podem inserir estados especiais.  Por exemplo, o `a:hover` estilo só entra em vigor quando você está pairando sobre um `<a>` elemento.  
    
1.  Escolha entre os colchetes para adicionar uma nova declaração.  
1.  Digite `background-color` o nome da declaração e selecione `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Digite background-color" lightbox="../media/beginners-css-rule3.msft.png":::
       Tipo `background-color`  
    :::image-end:::  
    
1.  Digite `green` o valor da declaração e selecione `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Digite verde" lightbox="../media/beginners-css-rule4.msft.png":::
       Tipo `green`  
    :::image-end:::  
    
1.  Passe o mouse sobre o link **Página** 1.  O plano de fundo do link fica verde.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Passe o mouse no link Home para revelar seu plano de fundo verde" lightbox="../media/beginners-css-rule5.msft.png":::
       Passe o mouse no link Home para revelar seu plano de fundo verde  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a>Rea uso de estilos em páginas com folhas de estilos externas  

Em uma etapa anterior, você adicionou o seguinte trecho de código como uma folha de estilos interna a `contact.html` .  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

E se você quiser ter `index.html` o mesmo estilo?  E se você tivesse um grande número de páginas para as quais você queria aplicar seus estilos?  Você precisa copiar e colar a folha de estilos interna em cada página da Web única em seu site.  Conclua as seguintes ações para adicionar uma **folha de** estilos externa para permitir que você escreva seu CSS uma vez e aplicá-lo a várias páginas.  

1.  Primeiro, atualize a guia ao vivo para remover as alterações feitas no DevTools.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Depois de atualizar a página, as alterações feitas no DevTools se foram" lightbox="../media/beginners-css-external1.msft.png":::
        Depois de atualizar a página, as alterações feitas no DevTools se foram  
    :::image-end:::  
    
1.  Volte para a **guia editor e** abra `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Exclua tudo `<style>` entre e , incluindo e `</style>` `<style>` `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="A marca de estilo foi removida" lightbox="../media/beginners-css-external3.msft.png":::
       A marca de estilo foi removida  
    :::image-end:::  
    
1.  Abra `index.html` e remova da `style="background-color: aliceblue;"` `<nav>` marca.  Agora você removeu todo o CSS adicionado anteriormente ao seu site.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="O estilo em linha foi removido do elemento nav" lightbox="../media/beginners-css-external4.msft.png":::
       O estilo em linha foi removido do elemento nav  
    :::image-end:::  
    
1.  Escolha **Novo Arquivo**.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="A nova caixa de diálogo de arquivo" lightbox="../media/beginners-css-external5.msft.png":::
       A nova caixa de diálogo de arquivo  
    :::image-end:::  
    
1.  Substitua `cool-file.js` e escolha Adicionar `style.css` **Arquivo**.  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Tipo style.css" lightbox="../media/beginners-css-external6.msft.png":::
       Tipo `style.css`  
    :::image-end:::  
    
1.  Adicione o seguinte trecho de código ao seu `style.css` arquivo.  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Adicionar código a style.css" lightbox="../media/beginners-css-external7.msft.png":::
       Adicionar código ao `style.css`  
    :::image-end:::  
    
    Verifique se você criou uma folha de estilos externa. Seu HTML não está ciente de que ele existe.  
    
1.  Abra `index.html` .  
1.  Adicione `<link rel="stylesheet" href="style.css">` ao HTML.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Link para style.css" lightbox="../media/beginners-css-external8.msft.png":::
       Link para `style.css`  
    :::image-end:::  
    
1.  Abra o `contact.html` arquivo e adicione o link lá.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Link para style.css em contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       Link para `style.css` em `contact.html`  
    :::image-end:::  
    
1.  Navegue até **a guia ao vivo**.  A home page agora tem a mesma fonte da última seção e uma seção de navegação azul.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="A home page" lightbox="../media/beginners-css-external10.msft.png":::
       A home page  
    :::image-end:::  
    
1.  Escolha o link **Contato** para navegar até a página de contato.  A página de contato tem a mesma formatação da home page.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="A página de contato" lightbox="../media/beginners-css-external11.msft.png":::
       A página de contato  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a>Usar uma estrutura CSS  

**Estruturas CSS** são coleções de estilos criadas por outros desenvolvedores que facilitam a criação de sites atraentes.  Em vez de definir estilos por conta própria, uma estrutura fornece uma coleção de estilos que você pode usar em seus elementos de página.  

1.  Copie o seguinte código:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Abra a guia edição e colar o código em `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Link para a estrutura em contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       Link para a estrutura em `contact.html`  
    :::image-end:::  
    
1.  Abra o `index.html` arquivo e adicione o código lá.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Link para a estrutura em index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       Link para a estrutura em `index.html`  
    :::image-end:::  
    
1.  Volte para a guia ao vivo para exibir suas alterações.  Embora a cor de plano de fundo do elemento e a fonte dos elementos e sejam as mesmas, a `<nav>` fonte dos outros elementos foi `<li>` `<a>` alterada.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Parte da fonte na home page foi alterada devido à estrutura" lightbox="../media/beginners-css-framework3.msft.png":::
       Parte da fonte na home page foi alterada devido à estrutura  
    :::image-end:::  
    
### <a name="use-a-class"></a>Usar uma classe  

Na última seção, você adicionou Bootstrap às páginas da Web, que alterou as fontes de alguns dos elementos em seu site.  As estruturas CSS ajudam você a fazer alterações importantes em sua página com muito pouco código.  Conclua as seguintes ações para alterar o seu header.  

1.  Copie o seguinte trecho de código.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Adicione o trecho de código anterior à `<header>` sua marca em `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Adicionar classes em index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Adicionar classes em `index.html`  
    :::image-end:::  
    
1.  Adicione o código à `<header>` sua marca em `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Adicionar classes em contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Adicionar classes em `contact.html`  
    :::image-end:::  
    
1.  Exibir suas alterações na guia ao vivo.  Há uma caixa grande e cinza ao redor do seu header.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="O header agora tem uma caixa grande e cinza ao seu redor" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       O header agora tem uma caixa grande e cinza ao seu redor  
    :::image-end:::  
    
### <a name="understand-classes"></a>Compreender classes  

Classes permitem atribuir coleções de estilos a elementos arbitrários.  Use o seguinte trecho de código para aplicar vários estilos ao elemento depois de `<header>` definir o atributo como `class` `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Uma vantagem de uma classe é que ela permite que você aplique estilos a qualquer elemento que você deseja.  Por exemplo, suponha que você queira definir a cor de plano de fundo de alguns `<p>` elementos como roxo, mas não todos os `<p>` elementos.  Use o seguinte trecho de código para definir o estilo em uma classe.  

```css
.custom-background {
  background-color: purple;
}
```  

Em seguida, aplique a classe apenas aos `<p>` elementos que você deseja estilo.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a>Alinhar elementos  

Conclua as seguintes ações para inicializar e forneça classes para elementos de alinhamento.  

1.  Volte para a guia editor e abra `index.html` .  
1.  Adicione `class="container-fluid"` à `<body>` sua marca.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Adicionar a classe de fluido de contêiner" lightbox="../media/beginners-css-align1.msft.png":::
       Adicionar a `container-fluid` classe  
    :::image-end:::  
    
1.  Wrap your `<nav>` and `<main>` elements in `<div class="row">` .  Certifique-se de `</div>` colocar depois para fechar `</main>` corretamente a nova marca.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Adicionar uma linha" lightbox="../media/beginners-css-align2.msft.png":::
       Adicionar uma linha  
    :::image-end:::  
    
1.  Adicione `class="col-3"` à sua marca e à sua `<nav>` `class="col-9"` `<main>` marca.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Adicionar as classes col-3 e col-9" lightbox="../media/beginners-css-align3.msft.png":::
       Adicionar as `col-3` classes e `col-9`  
    :::image-end:::  
    
1.  Exibir suas alterações na guia ao vivo.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="O conteúdo de nav agora está à esquerda do conteúdo principal" lightbox="../media/beginners-css-align4.msft.png":::
       O conteúdo de nav agora está à esquerda do conteúdo principal  
    :::image-end:::  
    
## <a name="next-steps"></a>Próximas etapas  

Parabéns, você terminou.  

*   A melhor maneira de melhorar o desenvolvimento da Web é criar mais sites.  Não se preocupe com quebra de material.  Divirta-se e aprenda o máximo possível ao longo do caminho.  
*   Para saber mais sobre o estilo de páginas da Web, navegue até [Introdução ao CSS][MDNCssFirstSteps].  
*   Para saber mais sobre como usar o DevTools para experimentar o CSS de uma página, navegue até Introdução [exibição e alteração css][DevtoolsCssIndex].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para Iniciantes: Introdução html e o dom | Microsoft Docs"  
[DevtoolsCssIndex]: ../css/index.md "Introdução Com exibição e alteração de css | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html - cooked-amphibian | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "As primeiras etapas do CSS | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original foi encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/css) e foi criada por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
