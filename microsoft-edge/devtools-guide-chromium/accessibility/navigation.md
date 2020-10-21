---
description: Um guia sobre como navegar no Microsoft Edge DevTools usando a tecnologia assistencial, como leitores de tela.
title: Navegar no Microsoft Edge DevTools com tecnologia assistencial
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f4ec63a0d432925b7db99ce695db66dd61f8bcf1
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125290"
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

O artigo a seguir destina-se a ajudar os usuários que dependem principalmente da tecnologia adaptativa, como leitores de tela, e usam [o Microsoft Edge devtools][MicrosoftEdgeDevtoolsMain].  O [Microsoft Edge devtools][MicrosoftEdgeDevtoolsMain] é um pacote de ferramentas de desenvolvedor da Web integrado ao navegador Microsoft Edge.  Se você estiver procurando por recursos DevTools relacionados para melhorar a acessibilidade de uma página da Web, consulte [referência de acessibilidade][DevtoolsAccessibilityReference].  

A acessibilidade do DevTools é um trabalho em andamento.  Alguns painéis e guias funcionam melhor com a tecnologia assistencial do que outros.  Este guia o orienta pelos painéis que são mais acessíveis e realça problemas específicos que você pode encontrar ao longo do caminho.  

## Visão geral  

Antes de começar, é útil ter um modelo mental de como a interface do usuário do DevTools é estruturada.  DevTools é dividido em uma série de painéis que são organizados em um [tablist do Aria][W3CWaiAriaTablist].  

Por exemplo:  

*   O painel **elementos** permite que você [exiba e altere os nós dom] [DevtoolsDomIndexNavigateDomTreeKeyboard] ou [CSS][DevtoolsCssIndex].  
*   O [painel de console][DevtoolsConsoleIndex] permite ler os logs de JavaScript e os objetos de edição ao vivo.  

Na área de conteúdo de cada painel, há várias ferramentas diferentes, muitas vezes chamadas de guias ou painéis na documentação.  
Por exemplo, o painel **elementos** contém guias adicionais para inspecionar ouvintes de eventos, a árvore de acessibilidade e muito mais.  A distinção entre guias e painéis é um pouco arbitrária.  A única razão pela qual você pode ver um termo ou o outro é manter a consistência com o restante da documentação oficial do DevTools.  

## Atalhos de teclado  

A [DevTools de atalhos de teclado do [] é um cheatsheet útil.  Certifique-se de marcá-lo e consultá-lo enquanto explora os diferentes painéis.  

## Abrir DevTools  

Para começar, navegue até [Open Microsoft Edge DevTools] [DevtoolsOpen].  Há várias maneiras de abrir o DevTools, por meio de atalhos de teclado ou itens de menu.  

## Navegar entre painéis  

### Navegar por teclado  

*   Com o devtools aberto, selecione `Control` + `]` \ (Windows, Linux \) ou `Command` + `]` \ (MacOS \) para concentrar o próximo painel.  
*   Selecione `Control` + `[` \ (Windows, Linux \) ou `Command` + `[` \ (MacOS \) para concentrar o painel anterior.  
*   Também é possível usar `Shift` + `Tab` para mover o foco para a [tablist do Aria][W3CWaiAriaTablist] de um painel e usar as teclas de direção para alterar os painéis, embora possa ser mais rápido usar os atalhos mencionados anteriormente.  

**Problemas conhecidos**  

*   Alguns painéis, como o **console** e os painéis de **desempenho** , podem mover o foco para a área de conteúdo do painel assim que cada painel é ativado.  Isso pode dificultar a navegação pelas teclas de direção.  
*   O nome do painel selecionado é anunciado, mas só depois que ele lê o conteúdo focalizado no painel.  Isso pode facilitar a perda.  

### Navegar por menu de comando  

Para focalizar um painel específico, use o [menu de comando][DevtoolsCommandMenuIndex]:  

1.  Com o devtools aberto, selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.  
    O **menu de comando** é um ComboBox AutoComplete de pesquisa difusa.  
1.  Digite o nome do painel que você deseja abrir e use o `Down Arrow` no teclado para navegar até a opção correta.  
1.  Selecione `Enter` para executar um comando.  

Conclua as seguintes ações para abrir o painel de **elementos** .  

1.  Abrir o **menu de comandos**.  
1.  Digite `E` então `L` .  O **painel > opção Mostrar elementos** está selecionado.  
1.  Selecione `Enter` para executar o comando que abre o painel.  

Abrir um painel dessa maneira direciona o foco para o conteúdo do painel.  No caso do painel **elementos** , o foco se move para a **árvore DOM**.  

## Painel elementos  

### Inspecionar um elemento na página  

1.  Navegue até o elemento que você deseja inspecionar usando o cursor no leitor de tela.  
1.  Simule um clique com o botão direito do mouse usando um mouse sobre o elemento para abrir o menu de contexto.  
1.  Escolha a opção **inspecionar** .  Isso [abre o painel de elementos e enfoca o elemento na árvore DOM] [DevtoolsDomIndexViewDomNodes].  

A **árvore DOM** é disposta como uma [árvore do Aria][W3CWaiAriaTree].  Para obter um exemplo, navegue até [navegar pela **árvore DOM** com um teclado] [DevtoolsDomIndexNavigateDomTreeKeyboard].  

### Copiar o código de um elemento na árvore DOM  

1.  Com o foco em um nó na **árvore DOM**, passe o mouse sobre o nó e abra o menu contextual \ (clique com o botão direito do mouse \).  
1.  Expanda a opção de **cópia** .  
1.  Escolha **copiar OuterHtml**.  

**Problemas conhecidos**  

*   **Copy OuterHtml** geralmente não seleciona o nó atual, em vez disso, seleciona o nó pai.  No entanto, o conteúdo do elemento ainda deve estar na outerHTML copiada.  

### Modificar os atributos de um elemento na árvore DOM  

*   Com o foco em um nó na **árvore DOM**, selecione `Enter` para torná-lo editável.  
*   Selecione `Tab` para mover entre valores de atributo.  Quando você ouvir "espaço", você está dentro de uma entrada de texto vazia e poderá digitar um novo valor de atributo.  
*   Selecione `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \) para aceitar a alteração e ouvir todo o conteúdo do elemento.  

**Problemas conhecidos**  

*   Ao digitar na entrada de texto, você não recebe nenhum comentário.  Se você cometer um digitador e usar as teclas de direção para explorar a entrada, também não receberá nenhum comentário.  A maneira mais fácil de verificar seu trabalho é aceitar a alteração e, em seguida, escutar o elemento inteiro a ser anunciado.  

### Editar o HTML de um elemento na árvore DOM  

*   Com o foco em um nó na **árvore DOM**, selecione `Enter` para torná-lo editável.  
*   Selecione `Tab` para mover entre valores de atributo.  Quando você ouvir o nome do elemento, por exemplo, `h2` estiver dentro de uma entrada de texto e poderá alterar o tipo do elemento.  
*   Selecione `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \) para aceitar a alteração.  

Por exemplo, quando você digita `h3` e seleciona `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \), as marcas de início e término do `h3` elemento são alteradas.  

## Guias do painel elementos  

O painel **elementos** contém guias adicionais para inspecionar itens como o CSS aplicado a um elemento ou o local relevante na árvore de acessibilidade.  

*   Com o foco em um nó na **árvore DOM**, selecione `Tab` até ouvir que o painel **estilos** está selecionado.  
*   Use a `Right Arrow` para explorar outras guias disponíveis.  

A **árvore DOM** transforma elementos com `href` atributos em links com foco, portanto, talvez seja necessário selecionar `Tab` mais de uma vez para acessar o painel de **estilos** .  

**Problemas conhecidos**  

As guias de **pontos de interrupção** e **Propriedades** do dom não são acessíveis pelo teclado.  

### Painel estilos  

No painel **estilos** , encontre controles para filtrar estilos, alternar entre Estados de elemento \ (como [: ativo][MDNActive] e [: Focus][MDNFocus]\), alternar classes e adicionar novas classes.  Também existe uma ferramenta de inspeção de estilo eficiente para explorar e modificar os estilos atualmente aplicados ao elemento que está em foco na **árvore DOM**.  

O conceito de chave para entender o painel **estilos** é que ele só mostra os estilos do nó atualmente selecionado na **árvore DOM**.  Por exemplo, suponha que você tenha concluído a inspeção dos estilos de um `<header>` nó e agora deseja examinar os estilos de um `<footer>` nó.  Para fazer isso, primeiro você precisa selecionar o `<footer>` nó na **árvore DOM**.  Você pode achar mais rápido usar o fluxo de trabalho [inspecionar](#inspect-an-element-on-the-page) para inspecionar um nó que está na proximidade geral do `footer` nó \ (como um link dentro do rodapé \), que enfoca a **árvore DOM**e use o teclado para navegar até o nó exato no qual você está interessado.  

#### Navegar pelo painel estilos  

Como todas as ferramentas de estilo se conectam de uma maneira ou de outra volta ao painel **estilos** , faz sentido tornar-se um especialista nesta ferramenta primeiro.  

*   Com o foco no painel **estilos** , selecione `Tab` para mover o foco dentro e explorar o conteúdo.  
*   Selecionar `Tab` até que o primeiro estilo se torne ativo.  Se você estiver usando um leitor de tela, este primeiro estilo será anunciado `element.style {}` .  
*   Selecione `Down Arrow` para navegar pela lista de estilos em ordem de específica.  Um leitor de tela anuncia cada estilo que começa com o nome do arquivo CSS, o número da linha em que o estilo aparece e o nome do estilo.  Por exemplo, `main.css:233 .card__img {}`.  
*   Selecione `Enter` para inspecionar um estilo com mais detalhes.  O foco começa em uma versão editável do nome do estilo.  
*   Selecione `Tab` para mover entre versões editáveis de cada propriedade CSS e os valores correspondentes.  No final de cada bloco de estilo está um campo de texto editável em branco que você pode usar para adicionar outras propriedades CSS.  
*   Você pode continuar a selecionar `Tab` para mover-se pela lista de estilos ou selecionar `Escape` para sair do modo e voltar para navegar pelas teclas de direção.  

Para obter atalhos adicionais, navegue até [referência do teclado do painel estilos] [DevtoolsShortcutsStylesPaneKeyboard].  

**Problemas conhecidos**  

*   Se você usar o campo de texto de **filtro** editável, não será mais possível navegar na lista de estilos.  

#### Alternar o estado do elemento  

Para alternar o estado de um elemento, como `:active` ou `:focus` :  

1.  Navegue até o painel **estilos** e selecione `Tab` até o botão **alternar estado do elemento** ficar em foco.  
1.  Selecione `Enter` para expandir a coleção de Estados do elemento.  Os Estados dos elementos são apresentados como um grupo de caixas de seleção.  
1.  Selecionar `Tab` até o primeiro Estado, `:active` , tem foco.  
1.  Selecione `Space` para habilitá-la.  Se o elemento atualmente selecionado na árvore DOM tiver um `:active` estilo, ele será aplicado agora.  
1.  Mantenha pressionado `Tab` para explorar todos os Estados disponíveis.  

#### Adicionar uma classe existente  

Adjacente ao botão **alternar estado do elemento** é o botão **classes do elemento** .  Para mover o foco para ele, selecione `Tab` e selecione `Enter` .  O foco se move para um campo de edição de texto rotulado **Adicionar nova classe**.  

O botão **classes de elemento** é usado principalmente para adicionar classes existentes a um elemento.  Por exemplo, se a sua folha de estilos contiver uma classe auxiliar nomeada `.clearfix` , você poderá selecionar `.` dentro do campo de edição de texto para ver uma lista de sugestões de classes e usar o `Down Arrow` para localizar a `.clearfix` sugestão.  Ou digite o nome da classe e selecione `Enter` para aplicá-la.  

#### Adicionar uma nova regra de estilo  

Adjacente ao botão **classes de elemento** é o botão **nova regra de estilo** .  Para mover o foco para ele, selecione `Tab` e selecione `Enter` .  O foco se move para um campo de texto editável dentro do Inspetor de estilo.  O conteúdo de texto inicial do campo é o nome da marca do elemento selecionado na **árvore DOM**.  
Você pode digitar qualquer nome de classe desejado nesse campo e, em seguida, selecionar `Tab` para atribuir propriedades CSS a ele.  

### Guia calculada  

Com o foco na guia **calculada** , selecione `Tab` para mover o foco dentro e explorar o conteúdo.  Na guia **calculada** há controles para explorar quais propriedades de CSS são realmente aplicadas a um elemento em ordem de poder específica.  

<!--todo: add computed tab section when available  -->  

#### Explorar todos os estilos calculados  

Selecione `Tab` até chegar à coleção de estilos calculados.  Eles são apresentados como uma [árvore do Aria][W3CWaiAriaTree].  Expandir uma ListBox revela quais seletores de CSS estão aplicando o estilo calculado.  Esses seletores são organizados por uma específica.  Um leitor de tela anuncia o valor calculado, em que o seletor de CSS está atualmente em correspondência, o nome do arquivo da folha de estilos que contém o seletor e o número da linha do seletor.  

**Problemas conhecidos**  

*   Se você usar o campo texto do **filtro** , não será mais possível inspecionar os estilos.  

### Guia ouvintes de eventos  

No painel **elementos** , você pode inspecionar os ouvintes de eventos aplicados a um elemento usando a guia **ouvintes de eventos** .  Com o foco no painel **estilos** , selecione a `Right Arrow` para navegar até a guia **ouvintes de eventos** .  

#### Explorar ouvintes de eventos  

Ouvintes de eventos são apresentados como uma [árvore do Aria][W3CWaiAriaTree].  Você pode usar as teclas de direção para navegar.  Um leitor de tela anuncia o nome do objeto DOM ao qual o ouvinte de eventos está associado, bem como o nome do arquivo em que o ouvinte de evento é definido e o número da linha.  

### Painel de acessibilidade  

Com o foco no painel **acessibilidade** , selecione `Tab` para mover o foco dentro e explorar o conteúdo.  No [painel Acessibilidade][DevtoolsAccessibilityReference] , há controles para explorar a árvore de acessibilidade, os atributos do Aria aplicados a um elemento e as propriedades de acessibilidade calculadas.  

#### Árvore de acessibilidade  

A **árvore de acessibilidade** é apresentada como uma [árvore do Aria][W3CWaiAriaTree] em que cada `treeitem` uma corresponde a um elemento no dom.  A árvore anuncia a função calculada para o nó selecionado.  Elementos genéricos como `div` e `span` são anunciados como "GenericContainer" na árvore.  Use as teclas de direção para percorrer a árvore e explorar as relações pai-filho.  

**Problemas conhecidos**  

*   O tipo de [árvore do Aria][W3CWaiAriaTree] usado pelo painel de **acessibilidade** pode não estar exposto corretamente no Microsoft Edge para leitores de tela do MacOS, como o VoiceOver.  Assine o [problema do Chromium #868480][ChromiumIssues868480] ser informado sobre o progresso sobre esse problema.  
*   Cada um dos **atributos do Aria** e as seções de **Propriedades calculadas** são marcados como uma [árvore do Aria][W3CWaiAriaTree], mas cada um não tem atualmente o gerenciamento de foco e não é o teclado virtual.  

## Painel auditorias  

O painel **auditorias** você deve executar uma série de testes em um site para verificar problemas comuns relacionados a desempenho, acessibilidade, SEO e várias outras categorias.  

### Configurar e executar uma auditoria  

1.  Quando o painel **auditorias** é aberto pela primeira vez, o foco é colocado no botão **executar auditoria** no final do formulário.  Por padrão, o formulário é configurado para executar auditorias para cada categoria usando emulação de celular em uma conexão 3G simulada.  
1.  Use `Shift` + `Tab` ou navegue de volta no modo de navegação para alterar as configurações de auditoria.  
1.  Quando estiver pronto para executar a auditoria, navegue novamente até o botão **executar auditoria** e selecione `Enter` .  
1.  O foco se move em uma janela modal com um botão **Cancelar** que permite que você saia da auditoria.  Você pode ouvir uma série de earcons à medida que a auditoria é executada e atualiza a página várias vezes.  

**Problemas conhecidos**  

*   As diferentes seções do formulário de configuração não estão atualmente marcadas com um `fieldset` elemento.  Pode ser mais fácil navegar no modo de procura para descobrir quais controles estão associados a cada seção.  
*   Não há anúncio earcon ou região ao vivo quando a execução da auditoria termina.  Geralmente, demora cerca de 30 segundos, após o qual você deve conseguir navegar até os resultados.  Usar o modo de procura pode ser a maneira mais fácil de alcançar os resultados.  

### Navegar no relatório de auditoria  

O relatório de auditoria é organizado em seções que correspondem a cada uma das categorias de auditoria.  O relatório é aberto com uma lista de resultados para cada categoria.  Esses resultados também são links que podem ser usados para pular para as seções relevantes.  Em cada seção `details` , há elementos expansíveis que contêm informações relacionadas a auditorias aprovadas ou falhas.  Por padrão, somente as auditorias com falha são mostradas.  Cada seção termina com um `details` elemento final que contém todas as auditorias passadas.  

Para executar uma nova auditoria, use `Shift` + `Tab` para sair do relatório e procure o botão **executar uma auditoria** .  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityReference]: ./reference.md "Referência de acessibilidade | Documentos da Microsoft"  
[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "O painel Acessibilidade-referência de acessibilidade | Documentos da Microsoft"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Documentos da Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /Dom/index.MD # View-dom-Nodes "Exibir nós DOM-introdução à exibição e alteração do DOM | Documentos da Microsoft "  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /Dom/index.MD # Navigate-The-dom-Tree-by-a-Keyboard "navegue pela árvore DOM com um teclado-comece a exibir e a alterar o DOM | Documentos da Microsoft "  
[DevtoolsOpen]: .. /open.md "abrir o Microsoft Edge DevTools | Documentos da Microsoft "  
[DevtoolsShortcuts]: .. /shortcuts.md "atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft "  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # estilos-painel-atalhos de teclado "atalhos de teclado do painel estilos-atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft "  

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
