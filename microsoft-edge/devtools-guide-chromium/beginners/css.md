---
title: 'DevTools para iniciantes: introdução ao CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: fba049a20a7b5f981130b4d9e60c37b07dc7e092
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882734"
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

Este é o segundo tutorial em uma série de tutoriais que ensina noções básicas de desenvolvimento da Web e do Microsoft Edge DevTools.  Na verdade, você ganha experiência prática ao criar seu próprio website.  Você não precisa concluir o primeiro tutorial antes de fazer isso.  Você pode começar aqui.  [Configurar seu código](#set-up-your-code) mostra como fazer a configuração.  

> [!NOTE]
> Este tutorial foi projetado para principiantes absolutos e se concentra nos **fundamentos do desenvolvimento na Web** e nas noções básicas de como usar o devtools para experimentar com CSS.  Se você quiser um tutorial que só se concentre no DevTools, confira [introdução e alterar CSS][DevtoolsCssIndex].  

No momento, o seu site tem a seguinte aparência:  

> ##### Figura 1  
> Qual é a aparência de seu site  
> ![Qual é a aparência de seu site][ImageCssIntro1]  

Depois de concluir o tutorial, ele terá a seguinte aparência:  

> ##### Figura 2  
> Qual será a aparência do seu site no final do tutorial  
> ![Qual será a aparência do seu site no final do tutorial][ImageCssIntro2]  

## Goal   

No final deste tutorial, você compreenderá:  

*   Como usar CSS para estilizar uma página da Web.  
*   Como usar o Microsoft Edge DevTools para experimentar com CSS.  
*   A diferença entre estruturas CSS e CSS.  

Você também terá um site real!  

## Pré-requisitos   

Antes de tentar este tutorial, complete os seguintes pré-requisitos:  

*   Conclua [a introdução ao HTML e ao dom][DevToolsBeginnersHtml] ou certifique-se de que você tenha uma compreensão do HTML e do dom semelhante ao ensinado nesse tutorial.  
*   Baixar o navegador da Web [Microsoft Edge][MicrosoftEdgeInsider] .  Este tutorial usa um conjunto de ferramentas de desenvolvimento da Web, chamado de Microsoft Edge DevTools, incorporado ao Microsoft Edge.  

## Configurar seu código   

Para começar a criar seu site, você precisa configurar seu código:  

1.  **Se você já concluiu o primeiro tutorial desta série, pule esta seção!  Continue usando o código do último tutorial, [introdução ao HTML e ao dom][DevToolsBeginnersHtml].**  
1.  Abra o [código-fonte][GlitchCookedAmphibianIndex].  Esta guia do seu navegador será chamada de **guia edição**.  
    
    > ##### Figura 3  
    > A guia edição  
    > ![A guia edição][ImageCssSetup1]  
    
1.  Clique em **cozinhá-Amphibian**.  Um menu é exibido.  
    
    > ##### Figura 4  
    > O menu opções do Project  
    > ![O menu opções do Project][ImageCssSetup2]  

1.  Clique em **remix projeto**.  Falha cria uma cópia do projeto que você pode editar.  
    
    > [!NOTE]
    > A falha gera um nome aleatório para o novo projeto.  
    
1.  Clique em **Mostrar** e selecione **em uma nova janela**.  Outra guia abre com uma visualização dinâmica do seu site.  Esta guia do seu navegador será chamada de **guia ao vivo**.  
    
    > ##### Figura 5  
    > A guia ao vivo  
    > ![A guia ao vivo][ImageCssSetup3]  

## Entender CSS   

**CSS** é um idioma de computador que determina o layout e o estilo de páginas da Web.  Por exemplo, aqui está um parágrafo com uma borda:  

> ##### Figura 6  
> Isso foi estilizado com CSS  
> ![Isso foi estilizado com CSS][ImageCssStyled]  

Aqui está o código HTML e CSS usado para criar esse parágrafo:  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` Provavelmente parece novidade para você.  O restante deve parecer familiar.  Caso contrário, conclua [a introdução com HTML e o dom antes de][DevToolsBeginnersHtml] tentar este tutorial.  

## Adicionar estilos em linha   

Use **estilos embutidos** quando você quiser aplicar estilos a um único elemento.  Experimente agora:  

1.  Volte para a guia edição e abra `index.html` .  
    
    > ##### Figura 7  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  Adicionar `style="background-color: aliceblue;"` à sua `<nav>` .  No bloco de código abaixo, a quarta linha de código é aquela que você precisa alterar.  O restante está aqui para que você possa ter certeza de que está colocando o novo código no lugar certo.  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  Vá para a **guia ao vivo** para ver as alterações!  O plano de fundo da `<nav>` seção agora está em azul.  
    
    > ##### Figura 8  
    > A cor do plano de fundo por trás da página inicial e dos links de contatos agora está azul  
    > ![A cor do plano de fundo por trás da página inicial e dos links de contatos agora está azul][ImageCssInline2]  

## Reutilizar estilos em uma única página com folhas de estilos internas   

Anteriormente, você viu um estilo embutido que aplicou um estilo a uma única `<p>` marca como esta:  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

E se você quiser que todos os `<p>` elementos na sua página da Web tenham o estilo da mesma maneira?  Você precisaria copiar e colar o código em cada marca única `<p>` do seu site.  Isso é muito tempo e esforço.  E, se precisar fazer uma edição, você terá que alterar todas as marcas novamente.  As **folhas de estilos internas** permitem que você escreva seu CSS uma vez para que ele se aplique a vários elementos.  Experimente agora:  

1.  Na guia ao vivo, clique em **contato** para acessar a página do contato.  Observe a fonte de **casa** e do **contato**.  
    
    > ##### Figura 9  
    > Página de contato  
    > ![Página de contato][ImageCssInternal1]  

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
1.  Clique em **contato** para voltar para a página de contato.  A fonte de **casa** e o **contato** foram alteradas.  
    
    > ##### Figura 10  
    > A fonte dos links de página inicial e contato foi alterada  
    > ![A fonte dos links de página inicial e contato foi alterada][ImageCssInternal2]  
    
### Entender as folhas de estilos internas   

As folhas de estilos internas aplicam estilos usando **seletores**.  Os seletores são padrões que podem ser aplicados a um ou mais elementos HTML.  Por exemplo, no código anterior:  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` é um seletor que traduz para "qualquer `<li>` um que contenha um `<a>` ".  O navegador altera a fonte dos links de **página inicial** e de **contato** porque eles correspondem a esse padrão.  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` é uma **declaração**.  Uma declaração é feita de duas partes: uma **Propriedade** e um **valor**.  `font-family` é a propriedade e `'Courier New', Courier, serif` é o valor dessa propriedade.  A propriedade descreve uma maneira geral de que você pode alterar o estilo do elemento, e o valor indica exatamente que ele deve ser alterado.  Por exemplo, `font-family: 'Courier New', Courier, serif` o navegador oferece esta instrução: "definir a fonte dos elementos que correspondem ao padrão `li a` `'Courier New'` .  Se essa fonte não estiver disponível, use `Courier` .  Se isso não estiver disponível, use `serif` ".  

### Adicionar vários seletores a um RuleSet   

Um bloco de código CSS, como o que você vê abaixo, é chamado de **RuleSet**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Use vírgulas para adicionar vários seletores a um RuleSet.  Experimente agora:  

1.  Na **guia Editor**, abra `contact.html` .  
1.  Após o `li a` tipo `, h1` .  

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

    Isso informa ao navegador para `<h1>` elementos de estilo da mesma maneira que ele estiliza elementos que correspondem ao padrão `li a` .  
    
1.  Ir para a **guia ao vivo**.  
1.  Clique no link do **contato** para voltar para a página de contato.  Agora, **entre em contato comigo!** tem a mesma fonte dos links de navegação.  
    
    > ##### Figura 11  
    > O texto ' Fale comigo! ' Agora tem a mesma fonte dos links de página inicial e de contato  
    > ![O texto fale comigo!  Agora tem a mesma fonte dos links de página inicial e de contato][ImageCssMultiple1]  

## Experimente com o DevTools   

Ao continuar a viagem para o desenvolvimento mestre na Web, você descobrirá que a CSS pode ser difícil.  Você escreverá algumas CSS e esperará que elas sejam exibidas de uma maneira, mas o navegador faz algo completamente diferente.  O Microsoft Edge DevTools torna mais fácil experimentar as alterações e ver imediatamente como essas alterações afetam a página.  

### Adicionar uma declaração a um rulet existente no DevTools   

Quando você quiser iterar no estilo de um elemento existente, adicione uma declaração a um RuleSet existente.  Experimente agora:  

1.  Clique com o botão direito do mouse no link **início** e selecione **inspecionar**.  
    
    > ##### Figura 12  
    > Inspecionar o link home  
    > ![Inspecionar o link home][ImageCssAdd1]  
    
    O DevTools é aberto juntamente com sua página.  O código que representa o link início `<a href="/">Home</a>` é em azul realçado na árvore DOM.  Isso deve ser familiar em introdução [ao HTML e ao dom][DevToolsBeginnersHtml].  Na guia **estilos** abaixo da árvore DOM, você pode ver a `font-family: 'Courier New', Courier, serif` declaração que você adicionou ao `contact.html` anterior.  
    
    > ##### Figura 13  
    > A guia estilos está abaixo da árvore DOM  
    > ![A guia estilos está abaixo da árvore DOM][ImageCssAdd2]  
    
    Se a janela do DevTools for ampla, a guia estilos estará à direita da árvore DOM.  
    
    > ##### Figura 14  
    > A guia estilos está à direita da árvore DOM  
    > ![A guia estilos está à direita da árvore DOM][ImageCssAdd3]  
    
1.  Clique no espaço em branco abaixo `font-family: 'Courier New', Courier, Serif` para adicionar uma nova declaração.  
    
    > ##### Figura 15  
    > Adicionando uma nova declaração  
    > ![Adicionando uma nova declaração][ImageCssAdd4]  
    
1.  Digite `color` e pressione `Enter` .  A interface do usuário de AutoCompletar sugere opções à medida que você digita.  
    
    > ##### Figura 16  
    > Digitação `color`  
    > ![Digitando cor][ImageCssAdd5]  

1.  Digite `magenta` e, em seguida, pressione `Enter` novamente.  Todo o texto na página de contato agora é magenta.  
    
    > ##### Figura 17  
    > Digitação `magenta`  
    > ![Digitando magenta][ImageCssAdd6]  
    
### Editar uma declaração no DevTools   

Você também pode editar declarações existentes no DevTools.  Experimente agora:  

1.  Clique no quadrado magenta ao lado de `magenta` .  Um seletor de cores aparece.  
    
    > ##### Figura 18  
    > O seletor de cores  
    > ![O seletor de cores][ImageCssEdit1]  
    
1.  Use o seletor de cores para alterar o texto da fonte para uma cor que você quiser.  
    
    > ##### Figura 19  
    > Alterando a cor da fonte para roxo com o seletor de cores  
    > ![Alterando a cor da fonte para roxo com o seletor de cores][ImageCssEdit2]  

### Adicionar um novo RuleSet no DevTools   

Você também pode adicionar novos RuleSets ao DevTools.  Experimente agora:  

1.  Clique em nova regra de **estilo** ![ nova regra ][ImageNewStyleRuleIcon] de estilo que está ao lado de **. CLS**.  Um RuleSet vazio aparece `a` como o seletor.  
    
    > ##### Figura 20  
    > Adicionando uma nova regra  
    > ![Adicionando uma nova regra][ImageCssRule1]  
    
1.  Substituir `a` por `a:hover` .  
    
    > ##### Figura 21  
    > Substituindo `a` por `a:hover`  
    > ![Substituindo a com a:hover][ImageCssRule2]  
    
    `:hover` é uma **pseudo-classe**.  Use pseudovariáveis para elementos de estilo quando eles inserem Estados especiais.  Por exemplo, o `a:hover` estilo somente tem efeito quando você estiver passando o mouse sobre um `<a>` elemento.  
    
1.  Clique entre os colchetes para adicionar uma nova declaração.  
1.  Digite `background-color` o nome da declaração e pressione `Enter` .  
    
    > ##### Figura 22  
    > Digitação `background-color`  
    > ![Digitando a cor da tela de fundo][ImageCssRule3]  
    
1.  Digite `green` o valor da declaração e pressione `Enter` .  
    
    > ##### Figura 23  
    > Digitação `green`  
    > ![Digitando verde][ImageCssRule4]  
    
1.  Passe o mouse sobre o link **início** .  O plano de fundo do link fica verde.  
    
    > ##### Figura 24  
    > Passando o mouse sobre o link home para revelar seu plano de fundo verde  
    > ![Passando o mouse sobre o link home para revelar seu plano de fundo verde][ImageCssRule5]  
    
## Reutilizar estilos em páginas com folhas de estilo externas   

Antes de você ter adicionado esta folha de estilos interna a `contact.html` :  

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

E se você quisesse estilizar `index.html` da mesma maneira?  E se você tiver *milhares* de páginas e quiser aplicar esses estilos a todas elas?  Você precisaria copiar e colar esta folha de estilos interna em cada página da Web em seu site.  As **folhas de estilo externas** permitem que você escreva a CSS uma vez, aplica-a a várias páginas.  Experimente agora:  

1.  Primeiro, recarregue a guia ao vivo para remover as alterações feitas no DevTools.  
    
    > ##### Figura 25  
    >  Depois de recarregar a página, as alterações feitas no DevTools são perdidas  
    > ![ Depois de recarregar a página, as alterações feitas no DevTools são perdidas][ImageCssExternal01]  
    
1.  Volte para a **guia Editor** e abra `contact.html` .  
    
    > ##### Figura 26  
    > `contact.html`  
    > ![contact.html][ImageCssExternal02]  
    
1.  Exclua tudo entre `<style>` e `</style>` , incluindo `<style>` e `</style>` .  
    
    > ##### Figura 27  
    > A marca de estilo foi removida  
    > ![A marca de estilo foi removida][ImageCssExternal03]  
    
1.  Vá para `index.html` e remova `style="background-color: aliceblue;"` da `<nav>` marca.  Você já removeu toda a CSS que você adicionou anteriormente ao seu site.  
    
    > ##### Figura 28  
    > O estilo embutido foi removido do elemento NAV  
    > ![O estilo embutido foi removido do elemento NAV][ImageCssExternal04]  

1.  Clique em **novo arquivo**.  
    
    > ##### Figura 29  
    > A caixa de diálogo novo arquivo  
    > ![A caixa de diálogo novo arquivo][ImageCssExternal05]  
    
1.  Substituir `cool-file.js` por `style.css` e, em seguida, clique em **Adicionar arquivo**.  
    
    > ##### Figura 30  
    > Digitação `style.css`  
    > ![Digitando Style. css][ImageCssExternal06]  
    
1.  Cole este código em `style.css` :  
    
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
    
    > ##### Figura 31  
    > Adicionando código a `style.css`  
    > ![Adicionando código ao Style. css][ImageCssExternal07]  
    
    Nesse ponto, você criou uma folha de estilos externa, mas o HTML não sabe que ela existe, ainda.  
    
1.  Abrir `index.html` .  
1.  Adicione `<link rel="stylesheet" href="style.css">` ao seu HTML.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### Figura 32  
    > Vinculando a `style.css`  
    > ![Vinculando a Style. css][ImageCssExternal08]  

1.  Acesse `contact.html` e adicione o link lá também.  
    
    > ##### Figura 33  
    > Vinculando a `style.css` em `contact.html`  
    > ![Vinculando a Style. CSS em contact.html][ImageCssExternal09]  

1.  Ir para a **guia ao vivo**.  A Home Page agora tem a mesma fonte da última seção e uma seção azul de navegação.  
    
    > ##### Figura 34  
    > A Home Page  
    > ![A Home Page][ImageCssExternal10]  
    
1.  Clique no link do **contato** para acessar a página do contato.  A página de contato tem a mesma formatação que a Home Page.  
    
    > ##### Figura 35  
    > Página de contato  
    > ![Página de contato][ImageCssExternal11]  
    
## Usar uma estrutura CSS   

**Estruturas CSS** são coleções de estilos criados por outros desenvolvedores que facilitam a criação de sites atraentes.  Em vez de definir estilos por conta própria, uma estrutura oferece um conjunto de estilos que você pode usar em seus elementos de página.  

1.  Copie o código a seguir:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Vá para a guia edição e cole o código em `contact.html` .  
    
    > ##### Figura 36  
    > Vinculando à estrutura em `contact.html`  
    > ![Vinculando à estrutura no contact.html][ImageCssFramework1]  
    
1.  Cole o código em `index.html` , também.  
    
    > ##### Figura 37  
    > Vinculando à estrutura em `index.html`  
    > ![Vinculando à estrutura no index.html][ImageCssFramework2]  
    
1.  Volte para a guia ao vivo para ver suas alterações.  Enquanto a cor do plano de fundo da `<nav>` fonte e da fonte dos `li a` elementos são iguais, a fonte dos outros elementos mudava.  
    
    > ##### Figura 38  
    > Algumas fontes na Home Page foram alteradas devido à estrutura  
    > ![Algumas fontes na Home Page foram alteradas devido à estrutura][ImageCssFramework3]  

### Usar uma classe   

Na última seção, você adicionou a inicialização às páginas da Web, o que altera as fontes de alguns dos elementos do seu site.  As estruturas CSS podem ajudá-lo a fazer alterações importantes na sua página com um pouco de código.  Experimente agora alterando seu cabeçalho:  

1.  Copie este código:  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Adicione este código à sua `<header>` marca `index.html` .  
    
    > ##### Figura 39  
    > Adicionando classes em `index.html`  
    > ![Adicionando classes no index.html][ImageCssJumbotron1]  
    
1.  Adicione também o código à sua `<header>` marca `contact.html` .  
    
    > ##### Figura 40  
    > Adicionando classes em `contact.html`  
    > ![Adicionando classes no contact.html][ImageCssJumbotron2]  
    
1.  Exiba suas alterações na guia ao vivo.  Há uma grande caixa cinza em torno do seu cabeçalho agora.  
    
    > ##### Figura 41  
    > Agora o cabeçalho tem uma grande caixa cinza ao seu lado  
    > ![Agora o cabeçalho tem uma grande caixa cinza ao seu lado][ImageCssJumbotron3]  
    
### Compreender classes   

As classes permitem atribuir coleções de estilos a elementos arbitrários.  Por exemplo, configurar o `class` atributo das `<header>` marcas para `jumbotron` aplicar os seguintes estilos a elas:  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Uma vantagem das classes é que elas permitem aplicar estilos a qualquer elemento desejado.  Por exemplo, suponha que você queira definir a cor da tela de fundo de *alguns* `<p>` elementos como roxo, mas não *todos* eles.  Você pode definir o estilo em uma classe:  

```css
.custom-background {
  background-color: purple;
}
```  

E, em seguida, aplicar a classe somente aos `<p>` elementos que você deseja estilizar:  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### Alinhar elementos   

Bootstrap também fornece classes para alinhar elementos.  Experimente agora:  

1.  Volte para a guia Editor e abra `index.html` .  
1.  Adicionar `class="container-fluid"` à sua `<body>` marca.  
    
    > ##### Figura 42  
    > Adicionar a `container-fluid` classe  
    > ![Adicionando a classe container-fluido][ImageCssAlign1]  

1.  Envolver seus `<nav>` `<main>` elementos e em `<div class="row">` .  Certifique-se de colocar `</div>` após para `</main>` fechar corretamente a nova marca.  
    
    > ##### Figura 43  
    > Adicionar uma linha  
    > ![Adicionar uma linha][ImageCssAlign2]  
    
1.  Adicione `class="col-3"` à sua `<nav>` marca e `class="col-9"` à sua `<main>` marca.  
    
    > ##### Figura 44  
    > Adicionando as `col-3` `col-9` classes e  
    > ![Adicionando as classes Col-3 e col-9][ImageCssAlign3]  
    
1.  Exiba suas alterações na guia ao vivo.  
    
    > ##### Figura 45  
    > O conteúdo de NAV agora está à esquerda do conteúdo principal  
    > ![O conteúdo de NAV agora está à esquerda do conteúdo principal][ImageCssAlign4]  
    
## Próximas etapas   

Parabéns!  Concluído!  

*   A melhor maneira de ficar melhor no desenvolvimento na Web é criar mais sites.  Não se preocupe em quebrar itens.  Só Divirta-se e saiba o quanto puder ao longo do caminho.  
*   Consulte [a introdução à CSS][MDNCssFirstSteps] para saber mais sobre o estilo de páginas da Web.  
*   Trabalhe com o tutorial de introdução ao [Exibir e alterar][DevtoolsCssIndex] o tutorial em CSS para saber mais sobre como você pode usar o devtools para experimentar a CSS de uma página.  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Figura 1: o que o site tem atualmente"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "Figura 2: qual será a aparência do seu site no final do tutorial"  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Figura 3: a guia edição"  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Figura 4: o menu de opções do Project"  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Figura 5: a guia ao vivo"  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Figura 6: foi estilizado com CSS"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Figura 7: index.html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Figura 8: a cor da tela de fundo por trás dos links para casa e contatos agora está azul"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Figura 9: página de contato"  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Figura 10: a fonte dos links de página inicial e de contato foi alterada"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Figura 11: o texto "entrar em contato!" agora tem a mesma fonte dos links de página inicial e de contato"  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Figura 12: inspecionar o link home"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Figura 13: a guia estilos está abaixo da árvore DOM"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Figura 14: a guia estilos está à direita da árvore DOM"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Figura 15: adicionando uma nova declaração"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Figura 16: digitando cor"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Figura 17: digitação de magenta"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Figura 18: o seletor de cores"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "Figura 19: alterando a cor da fonte para roxo com o seletor de cores"  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Figura 20: adicionando uma nova regra"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Figura 21: substituindo a com a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Figura 22: digitando a cor da tela de fundo"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Figura 23: digitando verde"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Figura 24: passando o mouse sobre o link home para revelar o plano de fundo verde"  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Figura 25: depois de recarregar a página, as alterações feitas no DevTools são perdidas"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Figura 26: contact.html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Figura 27: a marca de estilo foi removida"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Figura 28: o estilo embutido foi removido do elemento NAV"  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Figura 29: a caixa de diálogo novo arquivo"  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Figura 30: digitando Style. css"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Figura 31: adicionando código ao estilo. css"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Figura 32: vinculando ao estilo. css"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Figura 33: vinculando ao estilo. CSS em contact.html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Figura 34: a Home Page"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Figura 35: a página de contato"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Figura 36: vinculando à estrutura no contact.html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Figura 37: vinculando à estrutura no index.html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Figura 38: parte da fonte da página inicial foi alterada devido à estrutura"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Figura 39: adicionando classes no index.html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Figura 40: adicionando classes no contact.html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Figura 41: o cabeçalho agora tem uma grande caixa cinza ao seu lado"  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Figura 42: adicionando a classe container-fluido"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Figura 43: adicionando uma linha"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Figura 44: adicionando as classes Col-3 e col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Figura 45: o conteúdo de NAV agora está à esquerda do conteúdo principal"  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools para iniciantes: introdução ao HTML e ao DOM"  
[DevtoolsCssIndex]: ../css/index.md "Introdução à exibição e alteração de CSS"  

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
