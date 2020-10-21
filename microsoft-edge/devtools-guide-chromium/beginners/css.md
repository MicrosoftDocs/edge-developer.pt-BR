---
description: Introdução ao CSS
title: 'DevTools para iniciantes: introdução ao CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 62821084af8c22809f6e14ca4038ee173efd964a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125332"
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

# DevTools para iniciantes: introdução ao CSS  

Neste tutorial, você aprenderá a usar CSS para estilizar uma página da Web.  Você também aprenderá a usar o Microsoft Edge DevTools para experimentar alterações de CSS.  

O artigo a seguir é o segundo tutorial em uma série de tutoriais que ensina a você noções básicas sobre o desenvolvimento da Web e o Microsoft Edge DevTools.  Na verdade, você ganha experiência prática ao criar seu próprio website.  Você não precisa concluir o primeiro tutorial antes de seguir o segundo.  [Configurar seu código](#set-up-your-code) mostra como fazer a configuração.  

> [!NOTE]
> Este tutorial foi projetado para principiantes absolutos e se concentra nos **fundamentos do desenvolvimento na Web** e nas noções básicas de como usar o devtools para experimentar com CSS.  Se quiser um tutorial que só se concentre no DevTools, navegue até [introdução ao exibir e alterar CSS][DevtoolsCssIndex].  

No início do tutorial, o seu site deve ter a aparência da figura a seguir.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-intro1.msft.png":::
   Qual é a aparência de seu site  
:::image-end:::  

Depois de concluir o tutorial, o site deve ter a aparência da figura a seguir.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-intro2.msft.png":::
   Qual deve ser a aparência de seu site no final do tutorial  
:::image-end:::  

## Goal  

Siga este tutorial para compreender melhor os conceitos e tarefas a seguir.  

*   Como usar CSS para estilizar uma página da Web.  
*   Como usar o Microsoft Edge DevTools para experimentar com CSS.  
*   A diferença entre estruturas CSS e CSS.  

Você está criando um site real.  

## Pré-requisitos  

Antes de tentar este tutorial, complete os pré-requisitos a seguir.  

*   Conclua [a introdução ao HTML e ao dom][DevtoolsBeginnersHtml] ou certifique-se de ter uma compreensão do HTML e do dom semelhante ao que é ensinado nesse tutorial.  
*   Baixar o navegador da Web [Microsoft Edge][MicrosoftEdgeInsider] .  O tutorial a seguir usa um conjunto de ferramentas de desenvolvimento da Web, chamado de Microsoft Edge DevTools, incorporado ao Microsoft Edge.  

## Configurar seu código  

Para criar seu site, primeiro você deve concluir as seguintes ações para configurar o código.  

> [!NOTE]
> Se você já concluiu o primeiro tutorial da série, pule para a próxima seção.  Continue usando o código do último tutorial, [introdução ao HTML e ao dom][DevtoolsBeginnersHtml].  

1.  Abra o [código-fonte][GlitchCookedAmphibianIndex].  A guia in-Focus do seu navegador é referenciada como a **guia edição**.  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-setup1.msft.png":::
       A guia **edição**  
    :::image-end:::  
    
1.  Escolha **cozinhá-Amphibian**.  Um menu é exibido.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-setup2.msft.png":::
       O menu opções do Project  
    :::image-end:::  

1.  Escolha **projeto remix**.  Falha cria uma cópia do projeto que você pode editar.  
    
    > [!NOTE]
    > A falha gera um nome aleatório para o novo projeto.  
    
1.  Escolha **Mostrar** e escolha **em uma nova janela**.  Outra guia abre com uma visualização dinâmica do seu site.  A guia em foco do seu navegador é referenciada como a **guia ao vivo**.  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-setup3.msft.png":::
       A **guia ao vivo**  
    :::image-end:::  

## Entender CSS  

**CSS** é um idioma de computador que determina o layout e o estilo de páginas da Web.  A figura a seguir é um parágrafo com uma borda.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   O texto foi estilizado com CSS  
:::image-end:::  

O trecho de código a seguir é o código HTML e CSS usado para criar o parágrafo na figura anterior.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` Provavelmente parece novidade para você.  O restante deve parecer familiar.  Caso contrário, conclua a [introdução com HTML e o dom][DevtoolsBeginnersHtml] antes de tentar as seções a seguir.  

## Adicionar estilos em linha  

Conclua as ações a seguir para usar **estilos embutidos** para aplicar estilos a um único elemento.  

1.  Volte para a guia edição e abra `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-inline1.msft.png":::
       Abrir `index.html` na guia edição  
    :::image-end:::  
    
1.  Adicionar `style="background-color: aliceblue;"` à sua `<nav>` .  No bloco de código abaixo, a quarta linha de código é aquela que você precisa alterar.  O restante está apenas lá, portanto, você pode garantir que está colocando o novo código no lugar certo.  
    
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
    
1.  Vá para a **guia ao vivo** para ver as alterações!  O plano de fundo da `<nav>` seção agora está em azul.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-inline2.msft.png":::
       A cor do plano de fundo por trás da **página inicial** e dos links de **contatos** agora está azul  
    :::image-end:::  
    
## Reutilizar estilos em uma única página com folhas de estilos internas  

Em um trecho de código anterior, um estilo embutido aplicou um estilo a uma única `<p>` marca.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

E se você quiser que todos os `<p>` elementos na sua página da Web tenham o estilo da mesma maneira?  Você precisaria copiar e colar o código em cada marca única `<p>` do seu site.  Isso é muito tempo e esforço.  E, se precisar fazer uma edição, você precisaria alterar todas as marcas novamente.  Conclua as ações a seguir para usar uma **folha de estilos interna** para escrever seu CSS uma vez para que ele se aplique a vários elementos.  

1.  Na guia ao vivo, escolha **contato** para acessar a página do contato.  Observe a fonte de **casa** e do **contato**.  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-internal1.msft.png":::
       Página de contato  
    :::image-end:::  
    
1.  Na **guia Editor**, vá para `contact.html` .  
1.  Adicione o código a seguir a `contact.html` .  Lembre-se de que as linhas começando com `<style>` e terminando `</style>` são o que você precisa adicionar.  O outro código está aqui para que você saiba onde colocar o novo código.  
    
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
1.  Escolha **contato** para voltar para a página de contato.  A fonte de **casa** e o **contato** foram alteradas.  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-internal2.msft.png":::
       A fonte dos links de **página inicial** e **contato** foi alterada  
    :::image-end:::  
    
### Entender as folhas de estilos internas  

As folhas de estilos internas aplicam estilos usando **seletores**.  Os seletores são padrões que podem ser aplicados a um ou mais elementos HTML.  O trecho de código anterior adicionou o estilo a seguir.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` é um seletor que traduz para "qualquer `<li>` elemento que contém um `<a>` elemento".  O navegador altera a fonte dos links de **página inicial** e de **contato** porque cada um dos grupos de marcas corresponde ao padrão.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` é uma **declaração**.  Uma declaração é feita das duas partes A seguir.  

:::row:::
   :::column span="1":::
      **folha**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      A propriedade descreve uma maneira geral pela qual você pode alterar o estilo do elemento.  
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

Por exemplo, `font-family: 'Courier New', Courier, serif` o navegador dá a seguinte instrução: "definir a fonte dos elementos que correspondem ao padrão `li a` `'Courier New'` .  Se essa fonte não estiver disponível, use `Courier` .  Se isso não estiver disponível, use `serif` ".  

### Adicionar vários seletores a um RuleSet  

Um bloco de código CSS, como o que você vê abaixo, é chamado de **RuleSet**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Conclua as seguintes ações para usar vírgulas para adicionar vários seletores a um RuleSet.  

1.  Na **guia Editor**, abra `contact.html` .  
1.  Após o `li a` tipo `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    O trecho de código anterior informa ao navegador para `<h1>` elementos de estilo da mesma maneira que ele estiliza elementos que correspondem ao padrão `li a` .  
    
1.  Ir para a **guia ao vivo**.  
1.  Escolha o link do **contato** para voltar para a página de contato.  Agora, **entre em contato comigo!** tem a mesma fonte dos links de navegação.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-multiple1.msft.png":::
       O texto **fale comigo!** Agora tem a mesma fonte dos links de **página inicial** e de **contato**  
    :::image-end:::  
    
## Experimente com o DevTools  

Ao continuar a viagem para se tornar um especialista no desenvolvimento na Web, você pode descobrir que o CSS é complicado.  Você pode escrever um CSS e esperar que ele exiba uma maneira, mas o navegador faz algo completamente diferente.  O Microsoft Edge DevTools torna mais fácil experimentar as alterações e ver imediatamente como as alterações afetam a página.  

### Adicionar uma declaração a um rulet existente no DevTools  

Conclua as ações a seguir para iterar no estilo de um elemento existente, adicionar uma declaração a um RuleSet existente.  

1.  Passe o mouse sobre o link **início** , abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-add1.msft.png":::
       Inspecionar o link home  
    :::image-end:::  
    
    O DevTools é aberto juntamente com sua página.  O código que representa o link início `<a href="/">Home</a>` é em azul realçado na árvore DOM.  O trecho de código e a visualização devem estar familiarizados [com o introdução ao HTML e ao dom][DevtoolsBeginnersHtml].  
    
    :::row:::
       :::column span="":::
          Na figura a seguir, a `font-family: 'Courier New', Courier, serif` declaração que você adicionou anteriormente `contact.html` é vista na guia **estilos** abaixo da árvore DOM.  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-add2.msft.png":::
             A guia **estilos** está abaixo da árvore DOM  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Se a janela do DevTools for ampla, a guia estilos estará à direita da árvore DOM.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-add3.msft.png":::
             A guia **estilos** está à direita da árvore DOM  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Escolha a linha vazia abaixo `font-family: 'Courier New', Courier, Serif` para adicionar uma nova declaração.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-add4.msft.png":::
       Adicionar uma nova declaração  
    :::image-end:::  
    
1.  Digite `color` e selecione `Enter` .  A interface do usuário de AutoCompletar sugere opções à medida que você digita.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-add5.msft.png":::
       Tipo `color`  
    :::image-end:::  
    
1.  Digite `magenta` e selecione `Enter` .  Todo o texto na página de contato agora é magenta.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-add6.msft.png":::
       Tipo `magenta`  
    :::image-end:::  
    
### Editar uma declaração no DevTools  

Conclua as seguintes ações para editar as declarações existentes no DevTools.  

1.  Escolha o quadrado magenta ao lado de `magenta` .  Um seletor de cores aparece.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-edit1.msft.png":::
       O seletor de cores  
    :::image-end:::  
    
1.  Use o seletor de cores para alterar o texto da fonte para uma cor que você quiser.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-edit2.msft.png":::
       Alterar a cor da fonte para roxo com o seletor de cores  
    :::image-end:::  
    
### Adicionar um novo RuleSet no DevTools  

Conclua as seguintes ações para adicionar novos RuleSets ao DevTools.  

1.  Escolha **novo regra de estilo** \ ( ![ nova regra ][ImageNewStyleRuleIcon] de estilo \) que é ao lado de **. CLS**.  Um RuleSet vazio aparece `a` como o seletor.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-rule1.msft.png":::
       Adicionar uma nova regra  
    :::image-end:::  
    
1.  Substituir `a` por `a:hover` .  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-rule2.msft.png":::
       Substituir `a` por `a:hover`  
    :::image-end:::  
    
    `:hover` é uma **pseudo-classe**.  Use pseudovariáveis para elementos de estilo que podem inserir Estados especiais.  Por exemplo, o `a:hover` estilo somente tem efeito quando você estiver passando o mouse sobre um `<a>` elemento.  
    
1.  Escolha entre os colchetes para adicionar uma nova declaração.  
1.  Digite `background-color` o nome da declaração e selecione `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-rule3.msft.png":::
       Tipo `background-color`  
    :::image-end:::  
    
1.  Digite `green` o valor da declaração e selecione `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-rule4.msft.png":::
       Tipo `green`  
    :::image-end:::  
    
1.  Passe o mouse sobre o link **início** .  O plano de fundo do link fica verde.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-rule5.msft.png":::
       Passe o mouse sobre o link home para revelar o plano de fundo verde  
    :::image-end:::  
    
## Reutilizar estilos em páginas com folhas de estilo externas  

Em uma etapa anterior, você adicionou o trecho de código a seguir como uma folha de estilos interna `contact.html` .  

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

E se você quisesse estilizar `index.html` da mesma maneira?  E se você tivesse um grande número de páginas para as quais você deseja aplicar seus estilos?  Você precisaria copiar e colar a folha de estilos interna em cada página da Web em seu site.  Conclua as ações a seguir para adicionar uma **folha de estilos externa** para permitir que você escreva sua CSS uma vez e a aplique em várias páginas.  

1.  Primeiro, recarregue a guia ao vivo para remover as alterações feitas no DevTools.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external1.msft.png":::
        Depois de atualizar a página, as alterações que foram feitas no DevTools são perdidas  
    :::image-end:::  
    
1.  Volte para a **guia Editor** e abra `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Exclua tudo entre `<style>` e `</style>` , incluindo `<style>` e `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external3.msft.png":::
       A marca de estilo foi removida  
    :::image-end:::  
    
1.  Vá para `index.html` e remova `style="background-color: aliceblue;"` da `<nav>` marca.  Você já removeu toda a CSS que você adicionou anteriormente ao seu site.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external4.msft.png":::
       O estilo embutido foi removido do elemento NAV  
    :::image-end:::  
    
1.  Escolha **novo arquivo**.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external5.msft.png":::
       A caixa de diálogo novo arquivo  
    :::image-end:::  
    
1.  Substituir `cool-file.js` por `style.css` e escolha **Adicionar arquivo**.  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external6.msft.png":::
       Tipo `style.css`  
    :::image-end:::  
    
1.  Adicione o trecho de código a seguir ao seu `style.css` arquivo.  
    
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external7.msft.png":::
       Adicionar código a `style.css`  
    :::image-end:::  
    
    Certifique-se de que você criou uma folha de estilos externa. O HTML não está ciente de que ele existe.  
    
1.  Abrir `index.html` .  
1.  Adicione `<link rel="stylesheet" href="style.css">` ao seu HTML.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external8.msft.png":::
       Link para `style.css`  
    :::image-end:::  
    
1.  Abra o `contact.html` arquivo e adicione o link ali.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external9.msft.png":::
       Link para `style.css` em `contact.html`  
    :::image-end:::  
    
1.  Ir para a **guia ao vivo**.  A Home Page agora tem a mesma fonte da última seção e uma seção azul de navegação.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external10.msft.png":::
       A Home Page  
    :::image-end:::  
    
1.  Escolha o link do **contato** para acessar a página do contato.  A página de contato tem a mesma formatação que a Home Page.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-external11.msft.png":::
       Página de contato  
    :::image-end:::  
    
## Usar uma estrutura CSS  

**Estruturas CSS** são coleções de estilos criados por outros desenvolvedores que facilitam a criação de sites atraentes.  Em vez de definir estilos por conta própria, uma estrutura fornece um conjunto de estilos que você pode usar em seus elementos de página.  

1.  Copie o código a seguir:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Vá para a guia edição e cole o código em `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-framework1.msft.png":::
       Link para a estrutura em `contact.html`  
    :::image-end:::  
    
1.  Abra o `index.html` arquivo e adicione o código.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-framework2.msft.png":::
       Link para a estrutura em `index.html`  
    :::image-end:::  
    
1.  Volte para a guia ao vivo para ver suas alterações.  Enquanto a cor da tela de fundo do `<nav>` elemento e a fonte `<li>` dos `<a>` elementos e são iguais, a fonte dos outros elementos mudava.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-framework3.msft.png":::
       Parte da fonte na página inicial foi alterada por causa da estrutura  
    :::image-end:::  
    
### Usar uma classe  

Na última seção, você adicionou a inicialização às páginas da Web, o que altera as fontes de alguns dos elementos do seu site.  As estruturas CSS ajudam você a fazer alterações importantes na sua página com um pouco de código.  Conclua as ações a seguir para alterar o cabeçalho.  

1.  Copie o trecho de código a seguir.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Adicione o trecho de código anterior à sua `<header>` marca `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Adicionar classes em `index.html`  
    :::image-end:::  
    
1.  Adicione o código à sua `<header>` marca `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Adicionar classes em `contact.html`  
    :::image-end:::  
    
1.  Exiba suas alterações na guia ao vivo.  Há uma grande caixa cinza em torno do seu cabeçalho.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       Agora o cabeçalho tem uma grande caixa cinza ao seu lado  
    :::image-end:::  
    
### Compreender classes  

As classes permitem atribuir coleções de estilos a elementos arbitrários.  Use o trecho de código a seguir para aplicar vários estilos ao `<header>` elemento depois de definir o `class` atributo para `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Uma vantagem de uma classe é permitir que você aplique estilos a qualquer elemento desejado.  Por exemplo, suponha que você queira definir a cor da tela de fundo de alguns `<p>` elementos como roxo, mas não todos os `<p>` elementos.  Use o trecho de código a seguir para definir o estilo em uma classe.  

```css
.custom-background {
  background-color: purple;
}
```  

Em seguida, aplique a classe somente aos `<p>` elementos que você deseja aplicar o estilo.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### Alinhar elementos  

Conclua as ações a seguir para inicializar e fornecer classes para alinhar elementos.  

1.  Volte para a guia Editor e abra `index.html` .  
1.  Adicionar `class="container-fluid"` à sua `<body>` marca.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-align1.msft.png":::
       Adicionar a `container-fluid` classe  
    :::image-end:::  
    
1.  Envolver seus `<nav>` `<main>` elementos e em `<div class="row">` .  Certifique-se de colocar `</div>` após para `</main>` fechar corretamente a nova marca.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-align2.msft.png":::
       Adicionar uma linha  
    :::image-end:::  
    
1.  Adicione `class="col-3"` à sua `<nav>` marca e `class="col-9"` à sua `<main>` marca.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-align3.msft.png":::
       Adicionar as `col-3` `col-9` classes e  
    :::image-end:::  
    
1.  Exiba suas alterações na guia ao vivo.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-align4.msft.png":::
       O conteúdo de NAV agora está à esquerda do conteúdo principal  
    :::image-end:::  
    
## Próximas etapas  

Parabéns! você concluiu.  

*   A melhor maneira de ficar melhor no desenvolvimento na Web é criar mais sites.  Não se preocupe com as coisas quebradas.  Só Divirta-se e saiba o máximo possível ao longo do caminho.  
*   Para saber mais sobre como estilizar páginas da Web, navegue até [introdução ao CSS][MDNCssFirstSteps].  
*   Para saber mais sobre como usar o DevTools para experimentar a CSS de uma página, navegue até [começar a exibir e alterar a CSS][DevtoolsCssIndex].  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para iniciantes: introdução ao HTML e ao DOM | Documentos da Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cozinhá-Amphibian | Problema"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeiras etapas da CSS | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/css) e é criada pela [Katherine Jackson][KatherineJackson] \ (redatora técnica, Chrome devtools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
