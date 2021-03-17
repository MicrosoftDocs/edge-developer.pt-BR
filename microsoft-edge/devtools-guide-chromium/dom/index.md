---
description: Como exibir nós, pesquisar nós, editar nós, fazer referência a nós no Console, pausar alterações no nó e muito mais.
title: Começar a exibir e alterar o DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e4c08fb2fd5f360f037502c04edabaabb873ba16
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439237"
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

# <a name="get-started-with-viewing-and-changing-the-dom"></a>Começar a exibir e alterar o DOM  

Conclua estes tutoriais interativos para aprender os conceitos básicos de exibição e alteração do DOM de uma página usando o Microsoft Edge DevTools.  

Este tutorial supõe que você sabe a diferença entre DOM e HTML.  Navegue [até Apêndice: HTML versus DOM](#appendix-html-versus-the-dom) para uma explicação.  

## <a name="open-dom-examples"></a>Abrir exemplos dom  

1.  Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e escolha **Exemplos dom** para abrir em uma nova guia.  
    
    [Exemplos dom][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a>Exibir nós DOM  

A Árvore DOM do painel Elementos é onde você faz todas as atividades relacionadas ao DOM no DevTools.  

### <a name="inspect-a-node"></a>Inspecionar um nó  

Quando você estiver interessado em um nó DOM específico, **Inspecionar** é uma maneira rápida de abrir o DevTools e investigar esse nó.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Inspecionar um Nó,** escolha Com a direita **o Próprio Ângelo** e escolha **Inspecionar**.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspecionar um nó" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Inspecionar um nó  
    :::image-end:::  
    
    1.  A **ferramenta Elements** do DevTools é aberta.  `<li>Michelangelo</li>` é realçada na árvore **DOM**.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Realça o nó Delângelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Realça o `Michelangelo` nó  
        :::image-end:::  
        
        1.  Escolha o **ícone Inspecionar** \( ![ Inspecionar ](../media/inspect-icon.msft.png) \) no canto superior esquerdo do DevTools.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="O ícone Inspecionar" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               O **ícone Inspecionar**  
            :::image-end:::  
            
1.  Em **Inspecionar um Nó,** escolha o **texto de** Tokyo.  Agora, `<li>Tokyo</li>` é realçado na árvore DOM.  

Inspecionar um nó também é a primeira etapa para exibir e alterar os estilos de um nó.  Navegue [até Começar a exibir e alterar CSS][DevToolsCssGetStarted].  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a>Navegue pela Árvore DOM com um teclado  

Depois de selecionar um nó na Árvore DOM, você poderá navegar na Árvore DOM com o teclado.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Navegar na Árvore DOM com um Teclado,** escolha **Ringo** com a direita e escolha **Inspecionar**.  `<li>Ringo</li>` está selecionado na Árvore DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspecionar o nó Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Inspecionar o `Ringo` nó  
    :::image-end:::  
    
    1.  Selecione a `Up` tecla de seta duas vezes.  `<ul>`  está selecionada.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspecionar o nó ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Inspecionar o `ul` nó  
        :::image-end:::  
        
    1.  Selecione a `Left` tecla de seta.  A `<ul>` lista colapsa.  
    1.  Selecione a `Left` tecla de seta novamente.  O pai do `<ul>` nó está selecionado.  Nesse caso, é o `<div>` com a ID `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Selecione a tecla de seta 2 vezes para que você tenha selecionado a `Down` lista que você acabou de `<ul>` recolhido.  Ele deve ser assim: `<ul>... </ul>`  
    1.  Selecione a `Right` tecla de seta.  A lista se expande.  

### <a name="scroll-into-view"></a>Rolar para a exibição  

Ao exibir a Árvore DOM, você pode se interessar por um nó DOM que não esteja no viewport no momento.  Por exemplo, suponha que você tenha rolado até a parte inferior da página e esteja interessado no nó na `<h1>` parte superior da página.  **Rolar para o modo** de exibição permite que você reposicionar rapidamente o modo de exibição para que você possa revisar o nó.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Rolar para Exibir**, escolha **Magritte à** direita e escolha **Inspecionar**.  
1.  Role até a parte inferior da página Exemplos dom.  
1.  O `<li>Magritte</li>` nó ainda deve ser selecionado em sua Árvore DOM.  Caso não seja, volte para [Rolar para a exibição](#scroll-into-view) e comece de novo.  
1.  Passe o mouse `<li>Magritte</li>` no nó, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Rolar para exibição**.  Seu modo de exibição rola de volta para cima para que você possa revisar o nó **Magritte.**  Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se você não for capaz de revisar a opção **Rolar para exibição.**
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Rolar para a exibição" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Rolar para a exibição**  
    :::image-end:::  

### <a name="search-for-nodes"></a>Pesquisar nós  

Você pode pesquisar a Árvore DOM por cadeia de caracteres, seletor CSS ou seletor XPath.  

1.  Concentre o cursor na **ferramenta Elementos.**  
1.  Selecione `Control` + `F` \(Windows, Linux\) `Command` + `F` ou \(macOS\).  A barra de pesquisa é aberta na parte inferior da árvore DOM.  
1.  Digite `The Moon is a Harsh Mistress`.  A última frase é realçada na Árvore DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Realça a consulta na barra de pesquisa" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Realça a consulta na barra de pesquisa  
    :::image-end:::  
    
Como mencionado acima, a barra de pesquisa também dá suporte a seletores CSS e XPath.  

## <a name="edit-the-dom"></a>Editar o DOM  

Você pode editar o DOM em tempo real e analisar como as alterações afetam a página.  

### <a name="edit-content"></a>Editar conteúdo  

Para editar o conteúdo de um nó, clique duas vezes no conteúdo na Árvore DOM.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Editar Conteúdo,** escolha **Michelle** com o direito e escolha **Inspecionar**.  
    1.  Na Árvore DOM, clique duas vezes `Michelle` em .  Em outras palavras, clique duas vezes no texto `<li>` entre `</li>` e .  O texto é realçado para indicar que ele está selecionado.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Editar o texto" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Editar o texto  
        :::image-end:::  
        
    1.  `Michelle`Exclua , digite e selecione para confirmar a `Leela` `Enter` alteração.  O texto no DOM muda de **Michelle** para **Leela**.  

### <a name="edit-attributes"></a>Editar atributos  

Para editar atributos, clique duas vezes no nome ou no valor do atributo.  Siga as instruções para saber como adicionar atributos a um nó.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Editar Atributos,** escolha Com o direito **Descaro e** escolha **Inspecionar**.  
1.  Clique duas vezes `<li>` em .  O texto é realçado para indicar que o nó está selecionado.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Editar o nó" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Editar o nó  
    :::image-end:::  
    
1.  Selecione a `Right` tecla de seta, adicione um espaço, digite `style="background-color:gold"` e selecione `Enter` .  A cor de plano de fundo do nó muda para ouro.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Adicionar um atributo de estilo ao nó" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Adicionar um `style` atributo ao nó  
    :::image-end:::  
    
### <a name="edit-node-type"></a>Editar tipo de nó  

Para editar o tipo de nó, clique duas vezes no tipo e digite o novo tipo.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Editar Tipo de Nó,** escolha à direita o **Hank** e escolha **Inspecionar**.  
    1.  Clique duas vezes `<li>` em .  O texto `li` é realçado.  
    1.  Excluir `li` , `button` digitar, em seguida, selecione `Enter` .  O `<li>` nó muda para um `<button>` nó.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Alterar o tipo de nó para botão" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Alterar o tipo de nó para `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a>Reordenar nós DOM  

Arraste nós para reordená-los.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Reorder DOM Nodes**, escolha Com o direito **o nome de Elvis Presley** e escolha **Inspecionar**.  
    
    > [!NOTE]
    > É o último item da lista.  
    
    1.  Na Árvore DOM, arraste `<li>Elvis Presley</li>` até a parte superior da lista.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Arraste o nó para a parte superior da lista" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Arraste o nó para a parte superior da lista  
        :::image-end:::  
        
### <a name="force-state"></a>Estado de força  

Você pode forçar nós a permanecerem em estados, incluindo `:active` , , , e `:hover` `:focus` `:visited` `:focus-within` .  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Estado de Força**, passe o mouse sobre O Senhor das **Moscas.**  A cor do plano de fundo se torna laranja.  
    1.  Passe o **mouse em O Senhor das Moscas**, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
    1.  Passe o mouse sobre , abra o menu contextual \(clique com o botão `<li class="demo--hover">The Lord of the Flies</li>` direito do mouse\) e escolha **Force State**  >  **:hover**.  Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se a opção não for exibida.  A cor do plano de fundo permanece laranja, mesmo que você não seja realmente pairando sobre o nó.  

### <a name="hide-a-node"></a>Ocultar um nó  

Selecione `H` para ocultar um nó.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Ocultar um nó**, escolha Com a direita As Estrelas Meu **Destino** e escolha **Inspecionar**.  
    1.  Selecione a `H` tecla.  O nó está oculto.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Como o nó se parece na árvore DOM depois que ele está oculto" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Como o nó se parece na árvore DOM depois que ele está oculto  
        :::image-end:::  
        
    1.  Selecione a `H` tecla novamente.  O nó é mostrado novamente.  

### <a name="delete-a-node"></a>Excluir um nó  

Selecione `Delete` para excluir um nó.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Excluir um Nó,** escolha à direita **Foundation** e escolha **Inspecionar**.  
    1.  Selecione a `Delete` tecla.  O nó é excluído.  
    1.  Selecione `Control` + `Z` \(Windows, Linux\) `Command` + `Z` ou \(macOS\).  A última ação é desfeita e o nó reaparece.  

## <a name="access-nodes-in-the-console"></a>Acessar nós no Console  

O DevTools fornece alguns atalhos para acessar nós DOM do Console ou obter referências javaScript para cada um deles.  

### <a name="reference-the-currently-selected-node-with-0"></a>Fazer referência ao nó selecionado no momento com $0  

Quando você inspeciona um nó, o texto ao lado do nó significa que você pode fazer referência a esse nó no `== $0` Console com a variável `$0` .  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em Referência, o nó selecionado no momento com **$0**, escolha à direita **A Mão** Esquerda da Escuridão e escolha **Inspecionar**.  
    1.  Selecione a `Escape` chave para abrir a Gaveta do Console.  
    1.  Digite `$0` e selecione a `Enter` tecla.  O resultado da expressão mostra que `$0` avalia `<li>The Left Hand of Darkness</li>` como .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="O resultado da primeira expressão $0 no Console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            O resultado da primeira `$0` expressão no **Console**  
        :::image-end:::  
        
    1.  Passe o mouse no resultado.  O nó é realçado no viewport.  
    1.  Escolha `<li>Dune</li>` na Árvore DOM, digite o Console novamente `$0` e selecione `Enter` novamente.  Agora, `$0` avalia como `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="O resultado da segunda expressão $0 no Console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           O resultado da segunda `$0` expressão no **Console**  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a>Armazenar como variável global  

Se você precisar fazer referência a um nó muitas vezes, armazene-o como uma variável global.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Store como variável global,** passe o mouse em **O Grande Sono,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
    1.  Passe o `<li>The Big Sleep</li>` mouse na Árvore DOM, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Store como variável global**.  Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se a opção não for exibida.  
    1.  Digite `temp1` o Console e selecione `Enter` .  O resultado da expressão mostra que a variável é avaliada para o nó.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="O resultado da expressão temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           O resultado da `temp1` expressão  
        :::image-end:::  
        
### <a name="copy-js-path"></a>Copiar caminho JS  

Copie o caminho JavaScript para um nó quando precisar fazer referência a ele em um teste automatizado.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Copiar caminho JS,** passe o mouse em **Os Irmãos Karamazov**, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
    1.  Passe o mouse na Árvore DOM, abra o menu contextual \(clique com o botão direito do `<li>The Brothers Karamazov</li>` mouse\) e escolha **Copiar Copiar**  >  **Caminho JS**.  Uma `document.querySelector()` expressão que resolve o nó foi copiada para sua área de transferência.  
    1.  Selecione `Control` + `V` \(Windows, Linux\) ou `Command` + `V` \(macOS\) para colar a expressão no Console.  
    1.  Selecione `Enter` para avaliar a expressão.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="O resultado da expressão Copiar Caminho JS" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           O resultado da expressão **Copiar Caminho JS**  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a>Quebra nas alterações dom  

O DevTools permite pausar o JavaScript de uma página quando o JavaScript modifica o DOM.  

### <a name="break-on-attribute-modifications"></a>Quebra de modificações de atributo  

Use pontos de interrupção de modificação de atributo quando quiser pausar o JavaScript que faz com que qualquer atributo de um nó seja modificado.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Modificações de atributo Break on**, escolha **Sauerkraut** com a direita e escolha **Inspecionar**.  
    1.  Na Árvore DOM, passe o mouse sobre , abra o menu contextual \(clique com o botão direito do `<li id="target">Sauerkraut</li>` mouse\) e escolha **Quebrar Modificações**  >  **de Atributo**.  Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se a opção não for exibida.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Quebra de modificações de atributo" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Quebra de modificações de atributo**  
        :::image-end:::  
        
    1.  Na próxima etapa, você será instruído a escolher um botão que pausa o código da página.  Depois que a página for pausada, você não poderá mais rolar a página.  Você deve escolher **Resume Script** \( Resume ![ Script ](../media/resume-script-icon.msft.png) \) para tornar a página rolável novamente.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Onde retomar a execução do script" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Onde retomar a execução do script  
        :::image-end:::  
        
    1.  Escolha o **botão Definir Plano de** Fundo acima.  Isso define o `style` atributo do nó como `background-color:thistle` .  O DevTools pausa a página e realça o código que causou a alteração do atributo.  
    1.  Escolha **Retomar Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \), conforme mencionado anteriormente.  
    
### <a name="break-on-node-removal"></a>Quebra na remoção do nó  

Se você quiser pausar quando um nó específico for removido, use pontos de interrupção de remoção de nó.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Quebra na Remoção de Nó**, escolha Com o direito o **Neuromancer** e escolha **Inspecionar**.  
    1.  Na Árvore DOM, passe o mouse sobre , abra o menu contextual \(clique com o botão direito `<li id="target">Neuromancer</li>` do mouse\) e escolha Break **On**  >  **Node Removal**.  Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se a opção não for exibida.  
    1.  Escolha o **botão Excluir** acima.  O DevTools pausa a página e realça o código que fez com que o nó fosse removido.  
    1.  Escolha **Retomar Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \).  
    
### <a name="break-on-subtree-modifications"></a>Quebra em modificações de subárvore  

Depois de colocar um ponto de interrupção de modificação de subárvore em um nó, o DevTools pausa a página quando qualquer um dos descendentes do nó é adicionado ou removido.  

1.  [Abra exemplos dom](#open-dom-examples).  
1.  Em **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** e choose **Inspect**.  
    1.  Na Árvore DOM, passe o mouse sobre , que é o nó acima, abra o menu contextual \(clique com o botão direito do mouse\) e escolha `<ul id="target">` `<li>A Fire Upon the Deep</li>` Quebrar **modificações**  >  **de subárvore**.  Se a opção não for exibida, navegue até [Apêndice: Opções ausentes](#appendix-missing-options).  
    1.  Escolha **Adicionar Filho**.  O código pausa porque um `<li>` nó foi adicionado à lista.  
    1.  Escolha **Retomar Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \).  
    
## <a name="next-steps"></a>Próximas etapas  

Isso abrange a maioria dos recursos relacionados ao DOM no DevTools.  Você pode descobrir o restante dos recursos, pairando em nós na Árvore DOM, abrindo o menu contextual \(clique com o botão direito do mouse\) e experimentando as outras opções que não foram abordadas neste tutorial.  Navegue até atalhos de teclado [do painel Elementos.][DevToolsShortcutsElements]  

Confira a página [inicial do Microsoft Edge DevTools][MicrosoftEdgeDevTools] para descobrir tudo o que você pode fazer com o DevTools.  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a>Apêndice: HTML versus DOM  

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
      O navegador analisará o HTML e criará uma árvore de objetos como a lista a seguir.  
      
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
      No momento, ele tem a mesma aparência do HTML, mas suponha que o script referenciado na parte inferior do HTML executa o seguinte trecho de código.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Esse código remove o `h1` nó e adiciona outro nó ao `p` DOM.  O DOM completo agora exibe a lista a seguir.  
      
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

O HTML da página agora é diferente do DOM.  Em outras palavras, HTML representa o conteúdo inicial da página e o DOM representa o conteúdo da página atual.  Quando JavaScript adiciona, remove ou edita nós, o DOM se torna diferente do HTML.  

Navegue [até Introdução ao DOM][MDNIntroductionToDOM] para saber mais.  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a>Apêndice: Opções ausentes  

Muitas das instruções neste tutorial instruim você a passar o mouse em um nó na Árvore DOM, abra o menu contextual \(clique com o botão direito do mouse\) e escolha uma opção no menu de contexto que aparece.  Se a opção especificada no menu de contexto não for exibida, tente passar o mouse para longe do texto do nó e abrir o menu contextual \(clique com o botão direito do mouse\).  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Onde escolher se todas as opções não são exibidas" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Onde escolher se todas as opções não são exibidas  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge \(Chromium\) | Microsoft Docs"  
[DevToolsCssGetStarted]: ../css/index.md "Começar a exibir e alterar o css | Microsoft Docs"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Atalhos de teclado de ferramentas de elementos - Atalhos de teclado do Microsoft Edge DevTools | Microsoft Docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemplo do Microsoft Edge (Chromium) DevTools DOM | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao dom | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/dom/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
