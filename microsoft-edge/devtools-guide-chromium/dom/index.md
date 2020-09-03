---
description: Como exibir nós, pesquisar nós, editar nós, nós de referência no console, interromper alterações de nó e muito mais.
title: Começar a exibir e alterar o DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 555e627b70f0cc5e50c0676cf90067c2709a9ae3
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992950"
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





# Começar a exibir e alterar o DOM   



Preencha esses tutoriais interativos para aprender as noções básicas de como Visualizar e alterar o DOM de uma página usando o Microsoft Edge DevTools.  

Este tutorial pressupõe que você saiba a diferença entre o DOM e o HTML.  Consulte [Apêndice: HTML versus o dom](#appendix-html-versus-the-dom) para obter uma explicação.  

## Exemplos abertos do DOM  

1.  Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos de Dom** para abrir em uma nova guia.  
    
    [Exemplos de DOM][GlitchDomExamples]  
    
## Exibir nós DOM   

A árvore DOM do painel elementos é onde você faz todas as atividades relacionadas ao DOM no DevTools.  

### Inspecionar um nó   

Quando você está interessado em um nó DOM específico, **inspecionar** é uma maneira rápida de abrir o devtools e investigar esse nó.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **inspecionar um nó**, clique com o botão direito do mouse em **Michelangelo** e selecione **inspecionar**.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspecionar um nó" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Inspecionar um nó  
    :::image-end:::  
    
    1.  O painel **elementos** do devtools é aberto.  `<li>Michelangelo</li>` é realçado na **árvore DOM**.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Realce o nó Michelangelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Realce o `Michelangelo` nó  
        :::image-end:::  
        
        1.  Clique no ícone **inspecionar** \ ( ![ inspecionar ][ImageInspectIcon] \) no canto superior esquerdo do devtools.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="O ícone inspecionar" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               O ícone **inspecionar**  
            :::image-end:::  
            
1.  Em **inspecionar um nó**, clique no texto de **Tóquio** .  Agora `<li>Tokyo</li>` está realçado na árvore DOM.  

Inspecionar um nó também é a primeira etapa em direção à exibição e alteração dos estilos de um nó.  Confira [introdução à exibição e à alteração da CSS][DevToolsCssGetStarted].  

### Navegar pela árvore DOM com um teclado   

Depois de selecionar um nó na árvore DOM, você poderá navegar pela árvore DOM com o teclado.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **navegar pela árvore DOM com um teclado**, clique com o botão direito do mouse em **Ringo** e selecione **inspecionar**.  `<li>Ringo</li>` está selecionado na árvore DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspecione o nó Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Inspecionar o `Ringo` nó  
    :::image-end:::  
    
    1.  Pressione a `Up` tecla de direção 2 vezes.  `<ul>`  está selecionada.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspecionar o nó UL" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Inspecionar o `ul` nó  
        :::image-end:::  
        
    1.  Pressione a `Left` tecla de direção.  A `<ul>` lista é recolhida.  
    1.  Pressione a `Left` tecla de direção novamente.  O pai do `<ul>` nó está selecionado.  Nesse caso, é o `<div>` com ID `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Pressione a `Down` tecla de direção 2 vezes para selecionar novamente a `<ul>` lista que você acabou de recolhido.  Ele deve ser assim: `<ul>... </ul>`  
    1.  Pressione a `Right` tecla de direção.  A lista é expandida.  

### Rolar para o modo de exibição   

Ao exibir a árvore DOM, você pode estar interessado em um nó DOM que não está no visor no momento.  Por exemplo, suponha que você tenha rolagem para a parte inferior da página e esteja interessado no `<h1>` nó na parte superior da página.  **Acessar o modo de exibição** permite reposicionar rapidamente o visor para que você possa ver o nó.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **rolar para a exibição**, clique com o botão direito do mouse em **Magritte** e selecione **inspecionar**.  
1.  Role até a parte inferior da página de exemplos do DOM.  
1.  O `<li>Magritte</li>` nó ainda deve ser selecionado na sua árvore DOM.  Caso contrário, volte para rolar para o [modo de exibição](#scroll-into-view) e recomeçar.  
1.  Clique com o botão direito do mouse no `<li>Magritte</li>` nó e selecione **rolar para o modo de exibição**.  O visor rola novamente para que você possa ver o nó **Magritte** .  Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver a opção **rolar para a exibição** .
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Rolar para o modo de exibição" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Rolar para o modo de exibição**  
    :::image-end:::  

### Pesquisar nós   

Você pode pesquisar a árvore DOM por cadeia de caracteres, seletor de CSS ou seletor XPath.  

1.  Focalize o cursor no painel **elementos** .  
1.  Pressione `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \).  A barra de pesquisa é aberta na parte inferior da árvore DOM.  
1.  Digite `The Moon is a Harsh Mistress`.  A última sentença é realçada na árvore DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Realçar a consulta na barra de pesquisa" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Realçar a consulta na barra de pesquisa  
    :::image-end:::  
    
Conforme mencionado acima, a barra de pesquisa também oferece suporte a seletores CSS e XPath.  

## Editar o DOM   

Você pode editar o DOM instantaneamente e ver como essas alterações afetam a página.  

### Editar conteúdo   

Para editar o conteúdo de um nó, clique duas vezes no conteúdo na árvore DOM.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **editar conteúdo**, clique com o botão direito do mouse em **Michelle** e selecione **inspecionar**.  
    1.  Na árvore DOM, clique duas vezes `Michelle` .  Em outras palavras, clique duas vezes no texto entre `<li>` e `</li>` .  O texto é realçado para indicar que está selecionado.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Editar o texto" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Editar o texto  
        :::image-end:::  
        
    1.  Excluir `Michelle` , digite `Leela` e, em seguida, pressione `Enter` para confirmar a alteração.  O texto no DOM muda de **Michelle** para **Leela**.  

### Editar atributos   

Para editar atributos, clique duas vezes no nome ou no valor do atributo.  Siga as instruções para saber como adicionar atributos a um nó.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **Editar atributos**, clique com o botão direito do mouse em **Howard** e selecione **inspecionar**.  
1.  Clique duas vezes `<li>` .  O texto é realçado para indicar que o nó está selecionado.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Editar o nó" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Editar o nó  
    :::image-end:::  
    
1.  Pressione a `Right` tecla de seta, adicione um espaço, digite `style="background-color:gold"` e pressione `Enter` .  A cor da tela de fundo do nó muda para ouro.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Adicionar um atributo Style ao nó" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Adicionar um `style` atributo ao nó  
    :::image-end:::  
    
### Editar tipo de nó   

Para editar o tipo de um nó, clique duas vezes no tipo e, em seguida, digite o novo tipo.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **Editar tipo de nó**, clique com o botão direito do mouse em **Hank** e selecione **inspecionar**.  
    1.  Clique duas vezes `<li>` .  O texto `li` é realçado.  
    1.  Excluir `li` , digite `button` e, em seguida, pressione `Enter` .  O `<li>` nó muda para um `<button>` nó.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Alterar o botão do tipo de nó" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Alterar o tipo de nó para `button`  
        :::image-end:::  
        
### Reordenar nós DOM   

Arraste os nós para reorganizá-los.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **Reordenar nós dom**, clique com o botão direito do mouse em **Elvis Presley** e selecione **inspecionar**.  
    
    > [!NOTE]
    > É o último item na lista.  
    
    1.  Na árvore DOM, arraste `<li>Elvis Presley</li>` para a parte superior da lista.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Arraste o nó para a parte superior da lista" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Arraste o nó para a parte superior da lista  
        :::image-end:::  
        
### Forçar estado   

Você pode forçar os nós a permanecer nos Estados, incluindo `:active` ,,, `:hover` `:focus` `:visited` e `:focus-within` .  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **forçar estado**, passe o mouse sobre **o Lord dos voa**.  A cor do plano de fundo se torna laranja.  
    1.  Clique com o botão direito do mouse **no Lord dos voas** e selecione **inspecionar**.  
    1.  Clique com o botão direito do mouse `<li class="demo--hover">The Lord of the Flies</li>` e selecione **forçar estado**  >  **: focalizar**.  Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não vir essa opção.  A cor do plano de fundo permanece laranja, mesmo que você não esteja efetivamente passando o mouse sobre o nó.  

### Ocultar um nó   

Pressione `H` para ocultar um nó.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **ocultar um nó**, clique com o botão direito **do mouse no meu destino de estrelas** e selecione **inspecionar**.  
    1.  Pressione a `H` tecla.  O nó está oculto.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Qual é a aparência do nó na árvore DOM após ele estar oculto" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Qual é a aparência do nó na árvore DOM após ele estar oculto  
        :::image-end:::  
        
    1.  Pressione a `H` tecla novamente.  O nó é mostrado novamente.  

### Excluir um nó   

Pressione `Delete` para excluir um nó.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **excluir um nó**, clique com o botão direito do mouse em **base** e selecione **inspecionar**.  
    1.  Pressione a `Delete` tecla.  O nó é excluído.  
    1.  Pressione `Control` + `Z` \ (Windows \) ou `Command` + `Z` \ (MacOS \).  A última ação é desfeita e o nó é exibido novamente.  

## Acessar nós no console   

O DevTools fornece alguns atalhos para acessar nós DOM do console ou obter referências de JavaScript a cada um.  

### Fazer referência ao nó atualmente selecionado com o $0   

Quando você inspeciona um nó, o `== $0` texto ao lado do nó significa que você pode fazer referência a esse nó no console com a variável `$0` .  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **referenciar o nó selecionado no momento com o $0**, clique com o botão direito do mouse **na mão esquerda da escuridão** e selecione **inspecionar**.  
    1.  Pressione a `Escape` tecla para abrir a gaveta do console.  
    1.  Digite `$0` e pressione a `Enter` tecla.  O resultado da expressão mostra que `$0` é avaliado como `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="O resultado da primeira expressão $0 no console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            O resultado da primeira `$0` expressão no **console**  
        :::image-end:::  
        
    1.  Passe o mouse sobre o resultado.  O nó é realçado no visor.  
    1.  Clique `<li>Dune</li>` na árvore DOM, digite `$0` novamente no console e pressione `Enter` novamente.  Agora, `$0` é avaliada como `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="O resultado da segunda expressão $0 no console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           O resultado da segunda `$0` expressão no **console**  
        :::image-end:::  
        
### Armazenar como variável global   

Se você precisar consultar novamente um nó muitas vezes, armazene-o como uma variável global.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **armazenar como variável global**, clique com o botão direito **do mouse na grande suspensão** e selecione **inspecionar**.  
    1.  Clique com o botão direito do mouse `<li>The Big Sleep</li>` na árvore DOM e selecione **armazenar como variável global**.  Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não vir essa opção.  
    1.  Digite `temp1` o console e pressione `Enter` .  O resultado da expressão mostra que a variável é avaliada como o nó.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="O resultado da expressão temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           O resultado da `temp1` expressão  
        :::image-end:::  
        
### Copiar caminho do JS   

Copie o caminho JavaScript para um nó quando precisar referenciá-lo em um teste automatizado.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **copiar o caminho do js**, clique com o botão direito **do mouse na Karamazov da Brothers** e selecione **inspecionar**.  
    1.  Clique com o botão direito do mouse `<li>The Brothers Karamazov</li>` na árvore DOM e selecione **copiar**o  >  **caminho do js**.  Uma `document.querySelector()` expressão que é resolvida para o nó foi copiada para a área de transferência.  
    1.  Pressione `Control` + `V` \ (Windows \) ou `Command` + `V` \ (MacOS \) para colar a expressão no console.  
    1.  Pressione `Enter` para avaliar a expressão.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="O resultado da expressão de caminho do JS de cópia" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           O resultado da expressão de **caminho do js de cópia**  
        :::image-end:::  
        
## Interromper alterações de DOM   

O DevTools permite pausar o JavaScript de uma página quando o JavaScript modifica o DOM.  

### Interromper alterações de atributo   

Use pontos de interrupção de modificação de atributo quando você quiser pausar o JavaScript que faz com que qualquer atributo de um nó seja alterado.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **interromper as modificações de atributo**, clique com o botão direito do mouse em **sauerkraut** e selecione **inspecionar**.  
    1.  Na árvore DOM, clique com o botão direito do mouse `<li id="target">Sauerkraut</li>` e selecione **interromper nas**  >  **modificações de atributo**.  Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Interromper alterações de atributo" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Interromper alterações de atributo**  
        :::image-end:::  
        
    1.  Na próxima etapa, você será instruído a clicar em um botão que Pause o código da página.  Depois que a página for pausada, você não poderá mais rolar a página.  Você deve clicar em **retomar script** \ ( ![ continuar script ][ImageResumeScriptIcon] \) para que a página seja rolável novamente.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Onde continuar a execução do script" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Onde continuar a execução do script  
        :::image-end:::  
        
    1.  Clique no botão **definir plano de fundo** acima.  Isso define o `style` atributo do nó para `background-color:thistle` .  DevTools pausará a página e realçará o código que fez com que o atributo fosse alterado.  
    1.  Clique em **retomar script** \ ( ![ continuar script ][ImageResumeScriptIcon] \), conforme mencionado anteriormente.  
    
### Interromper a remoção do nó   

Se você quiser pausar quando um nó específico for removido, use pontos de interrupção de remoção de nó.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **interromper a remoção do nó**, clique com o botão direito do mouse em **Neuromancer** e selecione **inspecionar**.  
    1.  Na árvore DOM, clique com o botão direito do mouse `<li id="target">Neuromancer</li>` e selecione **interromper na**  >  **remoção do nó**.  Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.  
    1.  Clique no botão **excluir** acima.  DevTools pausará a página e realçará o código que fez com que o nó fosse removido.  
    1.  Clique em **retomar script** \ ( ![ retomar script ][ImageResumeScriptIcon] \).  
    
### Interromper modificações de subárvore   

Depois que você colocar um ponto de interrupção de modificação de subárvore em um nó, o DevTools pausará a página quando qualquer um dos descendentes do nó for adicionado ou removido.  

1.  [Exemplos abertos do dom](#open-dom-examples).  
1.  Em **interromper modificações de subárvore**, clique com o botão direito do mouse em **um incêndio na profundidade** e selecione **inspecionar**.  
    1.  Na árvore DOM, clique com o botão direito do mouse `<ul id="target">` , que é o nó acima `<li>A Fire Upon the Deep</li>` e selecione **interromper**  >  **alterações de subárvore**.  Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.  
    1.  Clique em **Adicionar filho**.  O código é pausado porque um `<li>` nó foi adicionado à lista.  
    1.  Clique em **retomar script** \ ( ![ retomar script ][ImageResumeScriptIcon] \).  
    
## Próximas etapas   

Isso abrange a maioria dos recursos relacionados ao DOM no DevTools.  Você pode descobrir o restante deles clicando com o botão direito do mouse nos nós na árvore DOM e experimentando as outras opções que não foram abordadas neste tutorial.  Consulte também [atalhos de teclado do painel elementos][DevToolsShortcutsElements].  

Confira a [Home Page do Microsoft Edge devtools][MicrosoftEdgeDevTools] para descobrir tudo o que você pode fazer com o devtools.  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## Apêndice: HTML versus DOM   

A seção a seguir explica rapidamente a diferença entre HTML e DOM.  

:::row:::
   :::column span="":::
      Quando você usa um navegador da Web para solicitar uma página, o servidor retorna HTML como o trecho de código a seguir  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      O navegador analisa o HTML e cria uma árvore de objetos como a lista a seguir.  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

Essa árvore de objetos, ou nós, que representa o conteúdo da página é chamada de DOM.  

:::row:::
   :::column span="":::
      No momento, ele tem a mesma aparência do HTML, mas suponha que o script referenciado na parte inferior do HTML executa o trecho de código a seguir.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Esse código remove o `h1` nó e adiciona outro `p` nó ao dom.  O DOM completo agora exibe a lista a seguir.  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

O HTML da página agora é diferente do DOM.  Em outras palavras, HTML representa o conteúdo inicial da página, e o DOM representa o conteúdo da página atual.  Quando o JavaScript adiciona, remove ou edita nós, o DOM se torna diferente do HTML.  

Consulte [introdução ao dom][MDNIntroductionToDOM] para saber mais.  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
   Scroll into view  
:::image-end:::  
    -->  

## Apêndice: opções ausentes   

Muitas das instruções neste tutorial instruem você a clicar com o botão direito do mouse em um nó na árvore DOM e selecionar uma opção no menu de contexto exibido.  Se você não vir a opção especificado no menu de contexto, tente clicar com o botão direito do mouse sobre o texto do nó.  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Onde clicar se você não estiver vendo todas as opções" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Onde clicar se você não estiver vendo todas as opções  
:::image-end:::  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \) | Documentos da Microsoft"  
[DevToolsCssGetStarted]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Atalhos de teclado do painel elementos-atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemplo de DOM do Microsoft Edge (Chromium) DevTools | Problema"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao DOM | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/dom/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
