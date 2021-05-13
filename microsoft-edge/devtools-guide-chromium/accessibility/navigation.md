---
description: Um guia sobre como navegar Microsoft Edge DevTools usando tecnologias assistivas, como leitores de tela.
title: Navegue Microsoft Edge DevTools com tecnologia assistida
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: cf2742dfb08ee482b26fe43417b7454e5b6ff809
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564578"
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
# <a name="navigate-microsoft-edge-devtools-with-assistive-technology"></a>Navegue Microsoft Edge DevTools com tecnologia assistida  

O artigo a seguir tem como objetivo ajudar os usuários que dependem principalmente de tecnologias assistivas, como leitores de tela, acessar e usar Microsoft Edge [DevTools][MicrosoftEdgeDevtoolsMain].  [Microsoft Edge DevTools][MicrosoftEdgeDevtoolsMain] é um pacote de ferramentas de desenvolvedor web internas no Microsoft Edge navegador.  Se você estiver procurando recursos do DevTools relacionados a melhorar a acessibilidade de uma página da Web, navegue até [Referência de Acessibilidade][DevtoolsAccessibilityReference].  

A acessibilidade do DevTools é um trabalho em andamento.  Alguns painéis e guias funcionam melhor com tecnologia assistida do que outras.  Este guia orienta você pelos painéis que são os mais acessíveis e destaca problemas específicos que você pode encontrar ao longo do caminho.  

## <a name="overview"></a>Visão geral  

Antes de começar, ele ajuda a ter um modelo mental de como a interface do usuário do DevTools é estruturada.  DevTools é dividido em uma série de painéis que são organizados em uma [lista de guias do ARIA][W3CWaiAriaTablist].  

Por exemplo:  

*   A **ferramenta Elements** permite que você [exibir e alterar nós dom][DevtoolsDomIndexNavigateDomTreeKeyboard] ou [CSS][DevtoolsCssIndex].  
*   O [painel Console][DevtoolsConsoleIndex] permite que você leia logs JavaScript e objetos de edição ao vivo.  

Na área de conteúdo de cada painel, há várias ferramentas diferentes, geralmente conhecidas como guias ou painéis na documentação.  
Por exemplo, a **ferramenta Elements** contém guias adicionais para inspecionar ouvintes de eventos, a árvore de acessibilidade e muito mais.  A distinção entre guias e painéis é um pouco arbitrária.  O único motivo pelo qual você pode revisar um termo ou outro é manter a consistência com o restante da documentação oficial do DevTools.  

## <a name="keyboard-shortcuts"></a>Atalhos de teclado  

A referência [Atalhos de Teclado do DevTools][DevtoolsShortcuts] é uma planilha útil.  Certifique-se de marcar e fazer referência a ele à medida que você explora os diferentes painéis.  

## <a name="open-devtools"></a>Abrir o DevTools  

Para começar, navegue até [Open Microsoft Edge DevTools][DevtoolsOpen].  Há várias maneiras de abrir o DevTools, por meio de atalhos de teclado ou itens de menu.  

## <a name="navigate-between-panels"></a>Navegar entre painéis  

### <a name="navigate-by-keyboard"></a>Navegar pelo teclado  

*   Com o DevTools aberto, selecione `Control` + `]` \(Windows, `Command` + `]` Linux\) ou \(macOS\) para focalizar o próximo painel.  
*   Selecione `Control` + `[` \(Windows, Linux\) `Command` + `[` ou \(macOS\) para focalizar o painel anterior.  
*   Também é possível usar para mover o foco para a lista de guias do ARIA de um painel e usar as teclas de seta para alterar painéis, embora possa ser mais rápido usar os `Shift` + `Tab` atalhos mencionados anteriormente. [][W3CWaiAriaTablist]  

**Problemas conhecidos**  

*   Alguns painéis, como as ferramentas **Console** e **Performance,** podem mover o foco para a área de conteúdo do painel assim que cada painel for ativado.  Isso pode dificultar a navegação por teclas de seta.  
*   O nome do painel selecionado é anunciado, mas somente depois de ter lido o conteúdo focado no painel.  Isso pode tornar muito fácil falhar.  

### <a name="navigate-by-command-menu"></a>Menu Navegar por Comando  

Para focalizar um painel específico, use o [Menu de Comando][DevtoolsCommandMenuIndex]:  

1.  Com o DevTools aberto, selecione `Control` + `Shift` + `P` \(Windows, `Command` + `Shift` + `P` Linux\) ou \(macOS\) para abrir o **Menu de Comando**.  
    O **Menu de Comando** é uma caixa de combinação de preenchimento automático de pesquisa difusa.  
1.  Digite o nome do painel que você deseja abrir e use o no teclado para `Down Arrow` navegar até a opção correta.  
1.  Selecione `Enter` para executar um comando.  

Conclua as seguintes ações para abrir a **ferramenta Elements.**  

1.  Abra o **Menu de Comando**.  
1.  Digite `E` em `L` seguida .  A **opção Painel > Mostrar Elementos** está selecionada.  
1.  Selecione `Enter` para executar o comando que abre o painel.  

Abra um painel dessa forma direciona o foco para o conteúdo do painel.  No caso da ferramenta **Elements,** o foco se move para a **árvore DOM**.  

## <a name="elements-panel"></a>Painel Elementos  

### <a name="inspect-an-element-on-the-page"></a>Inspecionar um elemento na página  

1.  Navegue até o elemento que você deseja inspecionar usando o cursor no leitor de tela.  
1.  Simule um clique com o botão direito do mouse no elemento para abrir o menu de contexto.  
1.  Escolha a **opção Inspecionar.**  Isso [abre o painel Elementos e focaliza o elemento na Árvore DOM][DevtoolsDomIndexViewDomNodes].  

A **árvore DOM** é definida como uma árvore [ARIA.][W3CWaiAriaTree]  Por exemplo, navegue até [Navegue até a Árvore **DOM** com um teclado][DevtoolsDomIndexNavigateDomTreeKeyboard].  

### <a name="copy-the-code-for-an-element-in-the-dom-tree"></a>Copie o código de um elemento na árvore DOM  

1.  Com o foco em um nó na Árvore **DOM,** passe o mouse no nó e abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Expanda **a opção Copiar.**  
1.  Escolha **Copiar ohtml externo**.  

**Problemas conhecidos**  

*   **Copiar oHTML externo** geralmente não seleciona o nó atual, mas seleciona o nó pai.  No entanto, o conteúdo do elemento ainda deve estar noHTML externo copiado.  

### <a name="modify-the-attributes-of-an-element-in-the-dom-tree"></a>Modificar os atributos de um elemento na árvore DOM  

*   Com o foco em um nó na Árvore **DOM,** selecione `Enter` para torná-lo editável.  
*   Selecione `Tab` para mover entre valores de atributo.  Quando você ouvir "espaço" você está dentro de uma entrada de texto vazia e é capaz de digitar um novo valor de atributo.  
*   Selecione `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) para aceitar a alteração e ouvir todo o conteúdo do elemento.  

**Problemas conhecidos**  

*   Quando você digita na entrada de texto, não há comentários.  Se você fizer um erro de digitação e usar as teclas de seta para explorar sua entrada, você também não obterá comentários.  A maneira mais fácil de verificar seu trabalho é aceitar a alteração e ouvir todo o elemento a ser anunciado.  

### <a name="edit-the-html-of-an-element-in-the-dom-tree"></a>Editar o HTML de um elemento na árvore DOM  

*   Com o foco em um nó na Árvore **DOM,** selecione `Enter` para torná-lo editável.  
*   Selecione `Tab` para mover entre valores de atributo.  Quando você ouvir o nome do elemento, por exemplo, , está dentro de uma entrada de texto e pode alterar o `h2` tipo do elemento.  
*   Selecione `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` ou \(macOS\) para aceitar a alteração.  

Por exemplo, quando você digita e seleciona `h3` `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` ou \(macOS\), `h3` as marcas inicial e final do elemento mudam.  

## <a name="elements-tool-panels"></a>Painéis da ferramenta Elements  

A **ferramenta Elements** contém guias adicionais para inspecionar coisas como o CSS aplicado a um elemento ou o local relevante na árvore de acessibilidade.  

*   Com o foco em um nó na Árvore **DOM,** selecione `Tab` até ouvir que o painel **Estilos** está selecionado.  
*   Use o `Right Arrow` para explorar outras guias disponíveis.  

A **Árvore DOM** transforma elementos com atributos em links focalizados, portanto, talvez seja necessário selecionar mais de uma vez para `href` alcançar o painel `Tab` **Estilos.**  

**Problemas conhecidos**  

As **guias Pontos de Interrupção** e **Propriedades** dom não são acessíveis ao teclado.  

### <a name="styles-pane"></a>Painel Estilos  

No painel **Estilos,** encontre controles para estilos de filtragem, estados do elemento de agregação \(como [:active][MDNActive] e [:focus][MDNFocus]\), classes de agregação e adição de novas classes.  Há também uma ferramenta de inspeção de estilo poderosa para explorar e modificar estilos atualmente aplicados ao elemento que está em foco na **árvore DOM**.  

O conceito-chave a ser entendido sobre o painel **Estilos** é que ele mostra apenas estilos para o nó selecionado no momento na **árvore DOM**.  Por exemplo, suponha que você tenha terminado de inspecionar os estilos de um nó e agora você deseja examinar os `<header>` estilos de um `<footer>` nó.  Para fazer isso, você primeiro precisa selecionar o `<footer>` nó na árvore **DOM**.  Talvez seja mais rápido usar o fluxo de trabalho [Inspecionar](#inspect-an-element-on-the-page) para inspecionar um nó que está nas proximidades gerais do nó \(como um link dentro do rodapé\), que focaliza a Árvore DOM e, em seguida, use seu teclado para navegar até o nó exato no qual `footer` você está interessado. ****  

#### <a name="navigate-the-styles-pane"></a>Navegar no painel Estilos  

Como todas as ferramentas de estilo se conectam de uma forma ou de outra ao painel **Estilos,** faz sentido se tornar um especialista nessa ferramenta primeiro.  

*   Com foco no painel **Estilos,** selecione `Tab` para mover o foco para dentro e explorar o conteúdo.  
*   Selecione `Tab` até que o primeiro estilo fique ativo.  Se você estiver usando um leitor de tela, esse primeiro estilo será anunciado como `element.style {}` .  
*   Selecione `Down Arrow` para navegar na lista de estilos em ordem de especificidade.  Um leitor de tela anuncia cada estilo começando com o nome do arquivo CSS, o número de linha no qual o estilo aparece e o nome do estilo.  Por exemplo, `main.css:233 .card__img {}`.  
*   Selecione `Enter` para inspecionar um estilo com mais detalhes.  O foco começa em uma versão editável do nome de estilo.  
*   Selecione `Tab` para mover entre versões editáveis de cada propriedade CSS e os valores correspondentes.  No final de cada bloco de estilos há um campo de texto editável em branco que você pode usar para adicionar propriedades CSS adicionais.  
*   Você pode continuar selecionando para mover pela lista de estilos ou selecionar para sair do modo e voltar para navegar por `Tab` `Escape` teclas de seta.  

Para atalhos adicionais, navegue até [Referência do teclado do painel estilos][DevtoolsShortcutsStylesPaneKeyboard].  

**Problemas conhecidos**  

*   Se você usar o **campo de** texto editável filtro, não poderá mais navegar na lista de estilos.  

#### <a name="toggle-element-state"></a>Estado do elemento Toggle  

Para alternar o estado de um elemento, como `:active` ou `:focus` :  

1.  Navegue até o painel **Estilos** e selecione até que o botão Estado do `Tab` Elemento de **Alternância** tenha foco.  
1.  Selecione `Enter` para expandir a coleção de estados de elemento.  Os estados do elemento são apresentados como um grupo de caixas de seleção.  
1.  Selecione `Tab` até o primeiro estado, , tem `:active` foco.  
1.  Selecione `Space` para habilita-lo.  Se o elemento selecionado no momento na Árvore DOM tiver um `:active` estilo, ele agora será aplicado.  
1.  Mantenha `Tab` a espera para explorar todos os estados disponíveis.  

#### <a name="add-an-existing-class"></a>Adicionar uma classe existente  

Adjacente ao botão **Estado do Elemento de Alternância** está o botão Classes **de** Elemento.  Para mover o foco para ele, selecione `Tab` e selecione `Enter` .  O foco se move para um campo de texto de edição rotulado **Adicionar Nova Classe**.  

O **botão Classes de** Elemento é usado principalmente para adicionar classes existentes a um elemento.  Por exemplo, se sua folha de estilos contiver uma classe auxiliar chamada, você poderá selecionar dentro do campo de texto de edição para exibir uma lista de sugestões de classes e usar a para encontrar `.clearfix` `.` a `Down Arrow` `.clearfix` sugestão.  Ou digite o nome da classe por conta própria e selecione `Enter` para aplicá-lo.  

#### <a name="add-a-new-style-rule"></a>Adicionar uma nova regra de estilo  

Adjacente ao botão **Classes de Elemento** está o botão Nova Regra **de** Estilo.  Para mover o foco para ele, selecione `Tab` e selecione `Enter` .  O foco se move para um campo de texto editável dentro do inspetor de estilos.  O conteúdo de texto inicial do campo é o nome da marca do elemento selecionado na **Árvore DOM**.  
Você pode digitar qualquer nome de classe que quiser neste campo e, em seguida, selecionar `Tab` para atribuir propriedades CSS a ele.  

### <a name="computed-tab"></a>Guia Computada  

Com o foco na **guia Computada,** selecione `Tab` para mover o foco para dentro e explorar o conteúdo.  Na guia **Computed,** há controles para explorar quais propriedades CSS são realmente aplicadas a um elemento em ordem de especificidade.  

<!--todo: add computed tab section when available  -->  

#### <a name="explore-all-computed-styles"></a>Explorar todos os estilos calculados  

Selecione `Tab` até chegar à coleção de estilos calculados.  Elas são apresentadas como uma [árvore ARIA][W3CWaiAriaTree].  Expandir uma caixa de listagem revela quais seletores CSS estão aplicando o estilo calculado.  Esses seletores são organizados por especificidade.  Um leitor de tela anuncia o valor calculado, qual seletor CSS está correspondendo no momento, o nome do arquivo da folha de estilos que contém o seletor e o número de linha do seletor.  

**Problemas conhecidos**  

*   Se você usar o **campo de** texto Filtro, não poderá mais inspecionar estilos.  

### <a name="event-listeners-tab"></a>Guia Ouvintes de eventos  

Na ferramenta **Elementos,** você pode inspecionar os ouvintes de eventos aplicados a um elemento usando a guia **Ouvintes de** Eventos.  Com o foco no painel **Estilos,** selecione o `Right Arrow` para navegar até o painel **Ouvintes de** Eventos.  

#### <a name="explore-event-listeners"></a>Explorar ouvintes de eventos  

Ouvintes de eventos são apresentados como uma [árvore ARIA][W3CWaiAriaTree].  Você pode usar as teclas de seta para navegar por elas.  Um leitor de tela anuncia o nome do objeto DOM ao qual o ouvinte de eventos está anexado, bem como o nome do arquivo no qual o ouvinte de eventos é definido e o número de linha.  

### <a name="accessibility-pane"></a>Painel acessibilidade  

Com foco no painel **Acessibilidade,** selecione `Tab` para mover o foco para dentro e explorar o conteúdo.  No painel [Acessibilidade,][DevtoolsAccessibilityReference] há controles para explorar a árvore de acessibilidade, os atributos ARIA aplicados a um elemento e as propriedades de acessibilidade calculadas.  

#### <a name="accessibility-tree"></a>Árvore de Acessibilidade  

A **Árvore de Acessibilidade** é apresentada como uma árvore [ARIA][W3CWaiAriaTree] onde cada uma corresponde `treeitem` a um elemento no DOM.  A árvore anuncia a função computada para o nó selecionado.  Elementos genéricos `div` como `span` e são anunciados como "GenericContainer" na árvore.  Use as teclas de seta para percorrer a árvore e explorar relações pai-filho.  

**Problemas conhecidos**  

*   O tipo de [árvore ARIA][W3CWaiAriaTree] usada pelo painel **Acessibilidade** pode não ser exposto corretamente no Microsoft Edge para leitores de tela macOS, como VoiceOver.  [Inscreva-se Chromium problema #868480][ChromiumIssues868480] para ser informado sobre o andamento deste problema.  
*   Cada uma das seções Atributos do **ARIA** e Propriedades Computadas está marcada como uma árvore [ARIA][W3CWaiAriaTree], mas cada uma delas não tem atualmente o gerenciamento de foco e não é operada por teclado. ****  

## <a name="audits-panel"></a>Painel auditorias  

A **ferramenta Auditorias** deve executar uma série de testes em um site para verificar se há problemas comuns relacionados ao desempenho, acessibilidade, SEO e várias outras categorias.  

### <a name="configure-and-run-an-audit"></a>Configurar e executar uma auditoria  

1.  Quando a **ferramenta Auditorias** é aberta pela primeira vez, o foco é colocado no botão **Executar Auditoria** no final do formulário.  Por padrão, o formulário é configurado para executar auditorias para cada categoria usando a emulação móvel em uma conexão 3G simulada.  
1.  Use `Shift` + `Tab` ou navegue de volta no modo Procurar para alterar as configurações de auditoria.  
1.  Quando estiver pronto para executar a auditoria, navegue até o botão **Executar Auditoria** e selecione `Enter` .  
1.  O foco se move para uma janela modal com um **botão Cancelar** que permite que você saia da auditoria.  Você pode ouvir uma série de earcons à medida que a auditoria é executado e atualiza a página várias vezes.  

**Problemas conhecidos**  

*   As diferentes seções do formulário de configuração não estão marcadas no momento com um `fieldset` elemento.  Pode ser mais fácil navegar por eles no modo Procurar para descobrir quais controles estão associados a cada seção.  
*   Não há nenhum comunicado de earcon ou região ao vivo quando a auditoria terminar de ser executado.  Geralmente, leva cerca de 30 segundos, após o qual você deve ser capaz de navegar até os resultados.  Usar o modo Procurar pode ser a maneira mais fácil de alcançar os resultados.  

### <a name="navigate-the-audit-report"></a>Navegar no relatório de auditoria  

O relatório de auditoria é organizado em seções que correspondem a cada uma das categorias de auditoria.  O relatório é aberto com uma lista de pontuações para cada categoria.  Essas pontuações também são links que podem ser usados para pular para as seções relevantes.  Em cada seção há elementos expansíveis, que contêm `details` informações relacionadas a auditorias passadas ou com falha.  Por padrão, apenas as auditorias com falha são mostradas.  Cada seção termina com um elemento final `details` que contém todas as auditorias passadas.  

Para executar uma nova auditoria, use `Shift` + `Tab` para sair do relatório e procure o botão **Executar uma auditoria.**  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityReference]: ./reference.md "Referência de acessibilidade | Microsoft Docs"  
[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "O painel Acessibilidade - Referência de Acessibilidade | Microsoft Docs"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Executar comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Microsoft Docs"  
[DevtoolsCssIndex]: ../css/index.md "Introdução Com exibição e alteração de css | Microsoft Docs"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /dom/index.md#view-dom-nodes "Exibir nós DOM - Começar a exibir e alterar o dom | Microsoft Docs"  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navegue pela Árvore DOM com um teclado - Começar a exibir e alterar o dom | Microsoft Docs"  
[DevtoolsOpen]: .. /open/index.md "Open Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcuts]: .. /shortcuts/index.md "Microsoft Edge atalhos de teclado do DevTools | Microsoft Docs"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /shortcuts/index.md#styles-panel-keyboard-shortcuts "Estilos de atalhos de teclado do painel - Microsoft Edge Atalhos de Teclado do DevTools | Microsoft Docs"  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problema 868480 - Expor árvores ARIA como tabelas na acessibilidade do Mac"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Novo problema - MicrosoftDocs/edge-developer | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ":active | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ":focus | MDN"  

[MonorailChromiumIssues]: https://crbug.com "Problemas - cromo - Monotrilho"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "tablist (função) - Aplicativos de Internet Rich Acessível (ARIA-ARIA) 1.1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "árvore (função) - Aplicativos de Internet Rich Acessível (ARIA-ARIA) 1.1 | W3C"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) e é de autoria de [Rob Dodson][RobDodson] \(Colaborador, Google WebFundamentals\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[RobDodson]: https://developers.google.com/web/resources/contributors#rob-dodson  
