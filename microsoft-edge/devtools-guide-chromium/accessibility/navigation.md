---
title: Navegar no Microsoft Edge DevTools com tecnologia assistencial
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 5de27e46d20957a1be79f72cf36074291566e6e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560844"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Navegar no Microsoft Edge DevTools com tecnologia assistencial   



Este guia tem como objetivo ajudar os usuários que dependem principalmente da tecnologia adaptativa, como leitores de tela, a usar o Microsoft Edge DevTools.  O Microsoft Edge DevTools é um pacote de ferramentas de desenvolvedor da Web integrado ao navegador Microsoft Edge.  <!--See [Accessibility Reference][DevtoolsAccessibilityReference] if you are looking for DevTools features related to improving the accessibility of a web page.  -->

<!--todo: add edge devtools index section when available  -->  
<!--todo: add reference (Accessibility Reference) section when available  -->  

A acessibilidade do DevTools é um trabalho em andamento.  Alguns painéis e guias funcionam melhor com a tecnologia assistencial do que outros.  Este guia o orienta pelos painéis que são mais acessíveis e realça problemas específicos que você pode encontrar ao longo do caminho.  

## Visão geral   

Antes de começar, é útil ter um modelo mental de como a interface do usuário do DevTools é estruturada.  DevTools é dividido em uma série de painéis que são organizados em um [Aria `tablist` ][W3CWaiAriaTablist].  

Por exemplo:  

*   O painel **elementos** permite que você visualize e altere os nós dom ou [CSS] [DevtoolsCssIndex].  
*   O [painel do**console** ] [DevtoolsConsoleIndex] permite que você leia os logs de JavaScript e os objetos de edição ao vivo.  

<!--todo:  add dom nodes (dom nodes) section when available  -->  

Na área de conteúdo de cada painel, há várias ferramentas diferentes, muitas vezes chamadas de guias ou painéis na documentação.  
Por exemplo, o painel **elementos** contém guias adicionais para inspecionar ouvintes de eventos, a árvore de acessibilidade e muito mais.  A distinção entre guias e painéis é um pouco arbitrária.  A única razão pela qual você pode ver um termo ou o outro é manter a consistência com o restante da documentação oficial do DevTools.  

## Atalhos de teclado   

A [DevTools de atalhos de teclado do [] é um cheatsheet útil.  Certifique-se de marcá-lo e consultá-lo enquanto explora os diferentes painéis.  

## Abrir o DevTools   

Para começar, leia [Open Microsoft Edge DevTools] [DevtoolsOpen].  Há várias maneiras de abrir o DevTools, por meio de atalhos de teclado ou itens de menu.  

## Navegar entre painéis   

### Navegar por teclado   

*   Com o devtools aberto, pressione `Control` + `]` \ (Windows \) ou `Command` + `]` \ (MacOS \) para concentrar o próximo painel.  
*   Pressione `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) para concentrar o painel anterior.  
*   Também é possível usar `Shift` + `Tab` para mover o foco para o [Aria `tablist` ][W3CWaiAriaTablist] de um painel e usar as teclas de direção para alterar os painéis, embora ele possa ser mais rápido de usar os atalhos mencionados anteriormente.  

#### Problemas conhecidos   

*   Alguns painéis, como o **console** e os painéis de **desempenho** , podem mover o foco para a área de conteúdo assim que eles são ativados.  Isso pode dificultar a navegação pelas teclas de direção.  
*   O nome do painel selecionado é anunciado, mas só depois que ele lê o conteúdo focalizado no painel.  Isso pode facilitar a perda.  

### Navegar por menu de comando   

Para focalizar um painel específico, use o [**menu de comando**] [DevtoolsCommandMenuIndex]:  

1.  Com o devtools aberto, pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.  
    O **menu de comando** é um ComboBox AutoComplete de pesquisa difusa.  
1.  Digite o nome do painel que você deseja abrir e use o `Down Arrow` no teclado para navegar até a opção correta.  
1.  Pressione `Enter` para executar um comando.  

Por exemplo, para abrir o painel **elementos** :  

1.  Abrir o **menu de comandos**.  
1.  Digite `E` então `L` .  O **painel > opção Mostrar elementos** está selecionado.  
1.  Pressione `Enter` para executar o comando que abre o painel.  

Abrir um painel dessa maneira direciona o foco para o conteúdo do painel.  No caso do painel **elementos** , o foco se move para a **árvore DOM**.  

## Painel elementos   

### Inspecionar um elemento na página   

1.  Navegue até o elemento que você deseja inspecionar usando o cursor no leitor de tela.  
1.  Simule um clique com o botão direito do mouse no elemento para abrir o menu de contexto.  
1.  Escolha a opção **inspecionar** .  Isso abre o painel de **elementos** e enfoca o elemento na **árvore DOM**.  

<!--todo:  add dom nodes (elements pane) section when available  -->  

A **árvore DOM** é disposta como um [Aria `tree` ][W3CWaiAriaTree].  <!--See [Navigate the **DOM Tree** with a keyboard][DevtoolsDomIndexNavigateDomTreeKeyboard] for an example.  -->  

<!--todo: add dom index navigation tree section then available  -->

### Copiar o código de um elemento na árvore DOM   

1.  Com o foco em um nó na **árvore DOM**, abra o menu de contexto clique com o botão direito do mouse.  
1.  Expanda a opção de **cópia** .  
1.  Selecione **copiar OuterHtml**.  

#### Problemas conhecidos   

*   **Copy OuterHtml** geralmente não seleciona o nó atual, em vez disso, seleciona o nó pai.  No entanto, o conteúdo do elemento ainda deve estar na outerHTML copiada.  

### Modificar os atributos de um elemento na árvore DOM   

*   Com o foco em um nó na **árvore DOM**, pressione `Enter` para torná-lo editável.  
*   Pressione `Tab` para mover-se entre os valores de atributo.  Quando você ouvir "espaço", você está dentro de uma entrada de texto vazia e poderá digitar um novo valor de atributo.  
*   Pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para aceitar a alteração e ouvir todo o conteúdo do elemento.  

#### Problemas conhecidos   

*   Ao digitar na entrada de texto, você não recebe nenhum comentário.  Se você cometer um digitador e usar as teclas de direção para explorar a entrada, também não receberá nenhum comentário.  A maneira mais fácil de verificar seu trabalho é aceitar a alteração e, em seguida, escutar o elemento inteiro a ser anunciado.  

### Editar o HTML de um elemento na árvore DOM   

*   Com o foco em um nó na **árvore DOM**, pressione `Enter` para torná-lo editável.  
*   Pressione `Tab` para mover-se entre os valores de atributo.  Quando você ouvir o nome do elemento, por exemplo, "H2", você está dentro de uma entrada de texto e poderá alterar o tipo do elemento.  
*   Pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para aceitar a alteração.  

Por exemplo, digitar `h3` e pressionar `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) altera as marcas de início e término do elemento para `h3` .  

## Guias do painel elementos   

O painel **elementos** contém guias adicionais para inspecionar itens como o CSS aplicado a um elemento ou o local relevante na árvore de acessibilidade.  

*   Com o foco em um nó na **árvore DOM**, pressione `Tab` até ouvir que o painel **estilos** está selecionado.  
*   Use a `Right Arrow` para explorar outras guias disponíveis.  

A **árvore DOM** transforma elementos com `href` atributos em links que podem ser focados, portanto, talvez seja necessário pressionar `Tab` mais de uma vez para acessar o painel de **estilos** .  

### Problemas conhecidos   

As guias de **pontos de interrupção** e **Propriedades** do dom não são acessíveis pelo teclado.  

### Painel estilos   

No painel **estilos** , encontre controles para filtrar estilos, alternar entre Estados de elemento \ (como [`:active`][MDNActive] e [`:focus`][MDNFocus] \), alternar classes e adicionar novas classes.  Também existe uma ferramenta de inspeção de estilo eficiente para explorar e modificar os estilos atualmente aplicados ao elemento que está em foco na **árvore DOM**.  

O conceito de chave para entender o painel **estilos** é que ele só mostra os estilos do nó atualmente selecionado na **árvore DOM**.  Por exemplo, suponha que você tenha concluído a inspeção dos estilos de um `<header>` nó e agora deseja examinar os estilos de um `<footer>` nó.  Para fazer isso, primeiro você precisa selecionar o `<footer>` nó na **árvore DOM**.  Você pode achar mais rápido usar o fluxo de trabalho [inspecionar](#inspect-an-element-on-the-page) para inspecionar um nó que está na proximidade geral do `footer` nó \ (como um link dentro do rodapé \), que enfoca a **árvore DOM**e use o teclado para navegar até o nó exato no qual você está interessado.  

#### Navegar pelo painel estilos   

Como todas as ferramentas de estilo se conectam de uma maneira ou de outra volta ao painel **estilos** , faz sentido dominar essa ferramenta primeiro.  

*   Com o foco no painel **estilos** , pressione `Tab` para mover o foco dentro e explore o conteúdo.  
*   Pressione `Tab` até que o primeiro estilo se torne ativo.  Se você estiver usando um leitor de tela, este primeiro estilo será anunciado como "elemento. Style {} ".  
*   Pressione `Down Arrow` para navegar pela lista de estilos em ordem de específica.  Um leitor de tela anuncia cada estilo que começa com o nome do arquivo CSS, o número da linha em que o estilo aparece e o nome do estilo.  Por exemplo: "Main. css: 233. card__img {} "  
*   Pressione `Enter` para inspecionar um estilo em mais detalhes.  O foco começa em uma versão editável do nome do estilo.  
*   Pressione `Tab` para mover-se entre as versões editáveis de cada propriedade CSS e seus valores correspondentes.  No final de cada bloco de estilo está um campo de texto editável em branco que você pode usar para adicionar outras propriedades CSS.  
*   Você pode continuar a pressionar `Tab` para percorrer a lista de estilos ou pressionar `Escape` para sair desse modo e voltar para navegar pelas teclas de direção.  

Não deixe de ler a [referência do teclado do painel de estilos] [DevtoolsShortcutsStylesPaneKeyboard] para obter atalhos adicionais.  

##### Problemas conhecidos   

*   Se você usar o campo de texto de **filtro** editável, não será mais possível navegar na lista de estilos.  

#### Alternar o estado do elemento   

Para alternar o estado de um elemento, como `:active` ou `:focus` :  

1.  Navegue até o painel **estilos** e pressione `Tab` até o botão **alternar estado do elemento** ter foco.  
1.  Pressione `Enter` para expandir a coleção de Estados do elemento.  Os Estados dos elementos são apresentados como um grupo de caixas de seleção.  
1.  Pressione `Tab` até o primeiro Estado, `:active` com foco.  
1.  Pressione `Space` para habilitá-la.  Se o elemento atualmente selecionado na árvore DOM tiver um `:active` estilo, ele será aplicado agora.  
1.  Continue pressionando `Tab` para explorar todos os Estados disponíveis.  

#### Adicionar uma classe existente   

Adjacente ao botão **alternar estado do elemento** é o botão **classes do elemento** .  Para mover o foco para ele, pressione `Tab` em seguida `Enter` .  O foco se move para um campo de edição de texto rotulado **Adicionar nova classe**.  

O botão **classes de elemento** é usado principalmente para adicionar classes existentes a um elemento.  Por exemplo, se a sua folha de estilos contiver uma classe auxiliar chamada `.clearfix` você pode pressionar `.` dentro do campo de edição de texto para ver uma lista de sugestões de classes e usar o `Down Arrow` para localizar a `.clearfix` sugestão.  Ou digite o nome da classe e pressione `Enter` para aplicá-la.  

#### Adicionar uma nova regra de estilo   

Adjacente ao botão **classes de elemento** é o botão **nova regra de estilo** .  Para mover o foco para ele, `Tab` pressione e pressione `Enter` .  O foco se move para um campo de texto editável dentro do Inspetor de estilo.  O conteúdo de texto inicial do campo é o nome da marca do elemento selecionado na **árvore DOM**.  
Você pode digitar qualquer nome de classe desejado nesse campo e, em seguida, pressionar `Tab` para atribuir propriedades CSS a ele.  

### Guia calculada   

Com o foco na guia **calculada** , pressione `Tab` para mover o foco dentro e explore o conteúdo.  Na guia **calculada** há controles para explorar quais propriedades de CSS são realmente aplicadas a um elemento em ordem de poder específica.  

<!--todo: add computed tab section when available  -->  

#### Explorar todos os estilos calculados   

Pressione `Tab` até chegar à coleção de estilos calculados.  Eles são apresentados como um [Aria `tree` ][W3CWaiAriaTree].  Expandir uma ListBox revela quais seletores de CSS estão aplicando o estilo calculado.  Esses seletores são organizados por uma específica.  Um leitor de tela anuncia o valor calculado, em que o seletor de CSS está atualmente em correspondência, o nome do arquivo da folha de estilos que contém o seletor e o número da linha do seletor.  

#### Problemas conhecidos   

*   Se você usar o campo texto do **filtro** , não será mais possível inspecionar os estilos.  

### Guia ouvintes de eventos   

No painel **elementos** , você pode inspecionar os ouvintes de eventos aplicados a um elemento usando a guia **ouvintes de eventos** .  Com o foco no painel **estilos** , pressione a `Right Arrow` para navegar até a guia **ouvintes de eventos** .  

#### Explorar ouvintes de eventos   

Ouvintes de eventos são apresentados como [Aria `tree` ][W3CWaiAriaTree].  Você pode usar as teclas de direção para navegar.  Um leitor de tela anuncia o nome do objeto DOM ao qual o ouvinte de eventos está associado, bem como o nome do arquivo em que o ouvinte de evento é definido e o número da linha.  

### Painel de acessibilidade   

Com o foco no painel de **acessibilidade** , pressione `Tab` para mover o foco dentro e explore o conteúdo.  No painel **acessibilidade** , há controles para explorar a árvore de acessibilidade, os atributos do Aria aplicados a um elemento e as propriedades de acessibilidade calculadas.  

<!--todo: add reference (Accessibility pane) section when available  -->  

#### Árvore de acessibilidade   

A **árvore de acessibilidade** é apresentada como [um `tree` Aria][W3CWaiAriaTree] em que cada `treeitem` um corresponde a um elemento no dom.  A árvore anuncia a função calculada para o nó selecionado.  Elementos genéricos como `div` e `span` são anunciados como "GenericContainer" na árvore.  Use as teclas de direção para percorrer a árvore e explorar as relações pai-filho.  

#### Problemas conhecidos   

*   O tipo de [Aria `tree` ][W3CWaiAriaTree] usado pelo painel de **acessibilidade** pode não estar exposto corretamente no Microsoft Edge para leitores de tela do MacOS, como o VoiceOver.  Assine o [problema do Chromium #868480][ChromiumIssues868480] ser informado sobre o progresso sobre esse problema.  
*   Cada um dos **atributos do Aria** e as seções de **Propriedades calculadas** são marcados [como `tree` Aria ][W3CWaiAriaTree], mas cada um não tem atualmente o gerenciamento de foco e não tem o teclado virtual.  

## Painel auditorias   

O painel **auditorias** você deve executar uma série de testes em um site para verificar problemas comuns relacionados a desempenho, acessibilidade, SEO e várias outras categorias.  

### Configurar e executar uma auditoria   

1.  Quando o painel **auditorias** é aberto pela primeira vez, o foco é colocado no botão **executar auditoria** no final do formulário.  Por padrão, o formulário é configurado para executar auditorias para cada categoria usando emulação de celular em uma conexão 3G simulada.  
1.  Use `Shift` + `Tab` ou navegue de volta no modo de navegação para alterar as configurações de auditoria.  
1.  Quando estiver pronto para executar a auditoria, navegue de volta para o botão **executar auditoria** e pressione `Enter` .  
1.  O foco se move em uma janela modal com um botão **Cancelar** que permite que você saia da auditoria.  Você pode ouvir uma série de earcons à medida que a auditoria é executada e atualiza a página várias vezes.  

#### Problemas conhecidos   

*   As diferentes seções do formulário de configuração não estão atualmente marcadas com um `fieldset` elemento.  Pode ser mais fácil navegar no modo de procura para descobrir quais controles estão associados a cada seção.  
*   Não há anúncio earcon ou região ao vivo quando a execução da auditoria termina.  Geralmente, demora cerca de 30 segundos, após o qual você deve conseguir navegar até os resultados.  Usar o modo de procura pode ser a maneira mais fácil de alcançar os resultados.  

### Navegar no relatório de auditoria   

O relatório de auditoria é organizado em seções que correspondem a cada uma das categorias de auditoria.  O relatório é aberto com uma lista de resultados para cada categoria.  Esses resultados também são links que podem ser usados para pular para as seções relevantes.  Em cada seção `details` , há elementos expansíveis que contêm informações relacionadas a auditorias aprovadas ou falhas.  Por padrão, somente as auditorias com falha são mostradas.  Cada seção termina com um `details` elemento final que contém todas as auditorias passadas.  

Para executar uma nova auditoria, use `Shift` + `Tab` para sair do relatório e procure o botão **executar uma auditoria** .  

## Privacidade Jurídica   

*   Envie relatórios de bug DevTools ou solicitações de recursos para [Chromium Issue Tracker][MonorailChromiumIssues].  
*   Envie qualquer comentário relacionado a este documento para o [GitHub][GithubEdgeDeveloperNewIssue].  

<!-- image links -->  

<!-- links -->  

<!--[DevtoolsAccessibilityReference]: reference.md "Accessibility Reference"  -->  
<!--[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "The Accessibility pane - Accessibility Reference"  -->  

<!--[MicrosoftEdgeDevtoolsIndex]: ../index.md "Microsoft Edge DevTools"  -->  
[DevtoolsCommandMenuIndex]: .. /Command-menu/index.MD "executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevtoolsConsoleIndex]: .. /console/index.MD "visão geral do console"  
[DevtoolsCssIndex]: .. /CSS/index.MD "comece a exibir e alterar CSS"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get Started With Viewing And Changing The DOM"  -->  
<!--[DevtoolsDomIndexNavigateDomTreeKeyboard]: ../dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get Started With Viewing And Changing The DOM"  -->
[DevtoolsOpen]: .. /open.md "abrir o Microsoft Edge DevTools"  
[DevtoolsShortcuts]: .. /shortcuts.md "atalhos de teclado do Microsoft Edge DevTools"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # estilos-painel-atalhos de teclado "atalhos de teclado do painel estilos-atalhos de teclado do Microsoft Edge DevTools"  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problema 868480-expor árvores do ARIA como tabelas na acessibilidade do Mac"  
[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Novo problema-MicrosoftDocs/Edge-Developer | GitHub"  
[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": ativo | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": foco | MDN"  
[MonorailChromiumIssues]: https://crbug.com "Problemas-Chromium-monorail"  
[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "tablist (função)-aplicativos da Internet sofisticados acessíveis (WAI-ARIA) 1,1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "Tree (função)-aplicativos sofisticados da Internet acessíveis (WAI-ARIA) 1,1 | W3C"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) e é criada por [Rob Dodson][RobDodson] \ (colaborador, Google webfundamentals \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
