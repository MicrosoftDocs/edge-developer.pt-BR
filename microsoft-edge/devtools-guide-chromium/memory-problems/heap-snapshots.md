---
description: Saiba como registrar instantâneos de heap com o Microsoft Edge DevTools heap Profiler e localizar vazamentos de memória.
title: Como gravar instantâneos de pilha
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 9762cb1d4932ce1a5d0b1c3944aa0b85d78b1060
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125458"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Como gravar instantâneos de pilha  

Saiba como registrar instantâneos de heap com o Microsoft Edge DevTools heap Profiler e localizar vazamentos de memória.  

O gerador de perfil de heap do Microsoft Edge DevTools mostra a distribuição de memória pelos objetos JavaScript e nós DOM relacionados da página.  Use-o para fazer instantâneos JavaScript heap \ (JS heap \), analisar gráficos de memória, comparar instantâneos e localizar vazamentos de memória.  Consulte também [árvore de retenção de objetos][DevtoolsMemoryProblems101ObjectsRetainingTree].  

## Fazer um instantâneo  

No painel **memória** , escolha **tirar instantâneo**e escolha **Iniciar**.  Você também pode selecionar `Ctrl` + `E` \ (Windows, Linux \) ou `Cmd` + `E` \ (MacOS \).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Selecionar o tipo de perfil  
:::image-end:::  

Os **instantâneos** são inicialmente armazenados na memória do processo de renderização.  Os instantâneos são transferidos para o DevTools sob demanda, quando você clica no ícone de instantâneo para exibi-lo.  

Após o instantâneo ser carregado no DevTools e ter sido analisado, o número abaixo do título do instantâneo será exibido e mostrará o [Tamanho total dos objetos JavaScript acessíveis][DevtoolsMemoryProblems101ObjectSizes].  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Tamanho total dos objetos acessíveis  
:::image-end:::  

> [!NOTE]
> Somente objetos alcançáveis são incluídos em instantâneos.  Além disso, fazer um instantâneo sempre começa com uma coleta de lixo.  

## Limpar instantâneos  

Escolha limpar o ícone de **todos os perfis** para remover instantâneos \ (ambos do devtools e qualquer memória associada ao processo de renderizador \).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Remover instantâneos  
:::image-end:::  

Fechar a janela DevTools não exclui os perfis da memória associada ao processo de renderizador.  Ao reabrir o DevTools, todos os instantâneos feitos anteriormente reaparecem na lista de instantâneos.  

> [!NOTE]
> Experimente este exemplo de [objetos dispersos][GlitchDevtoolsMemoryExample03] e perfilie-o usando o gerador de perfil de heap.  Você deve ver uma quantidade de atribuições de itens \ (objeto \).  

## Exibir instantâneos  

Exiba instantâneos de diferentes perspectivas para tarefas diferentes.  

O **modo de exibição de resumo** mostra objetos agrupados pelo nome do construtor.  Use-o para procurar objetos \ (e o uso de memória \) com base no tipo agrupado pelo nome do construtor.  Isso é particularmente útil para **acompanhar os vazamentos dom**.

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Exibição de comparação**.  Exibe a diferença entre dois instantâneos.  Use-o para comparar dois (ou mais \) instantâneos de memória de antes e depois de uma operação.  Inspecionar o Delta na memória liberada e contagem de referência permite que você confirme a presença e causa de perda de memória.  

**Modo de exibição de confinamento**.  Permite explorar o conteúdo da pilha.  O **modo de exibição de detenção** fornece uma visão melhor da estrutura de objetos, ajudando a analisar objetos referenciados no namespace global \ (janela \) para descobrir o que está mantendo objetos.  Use-o para analisar os fechamentos e mergulhe em seus objetos em um nível baixo.  

Para alternar entre os modos de exibição, use o seletor na parte superior do modo de exibição.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Alternar seletor de modos de exibição  
:::image-end:::  

> [!NOTE]
> Nem todas as propriedades são armazenadas na pilha JavaScript.  As propriedades implementadas usando getters que executam o código nativo não são capturadas.  Além disso, valores não cadeia de caracteres, como números, não são capturados.  

### Modo de exibição Resumo  

Inicialmente, um instantâneo é aberto no modo de exibição de resumo, exibindo totais de objetos, que podem ser expandidos para mostrar instâncias:  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   Modo de exibição **Resumo**  
:::image-end:::  

As entradas de nível superior são linhas de "total".  

| Entradas de nível superior | Descrição |  
|:--- |:--- |  
| **Construtor** | Representa todos os objetos criados usando esse construtor.  |  
| **Distância** | exibe a distância para a raiz usando o caminho simples mais curto dos nós.  |  
| **Tamanho superficial** | Exibe a soma dos tamanhos superficiais de todos os objetos criados por uma determinada função de construtor.  O tamanho superficial é o tamanho da memória mantida por um objeto \ (geralmente, matrizes e cadeias de caracteres têm tamanhos mais superficiaiss \).  Consulte também [tamanhos de objeto][DevtoolsMemoryProblems101ObjectSizes].  |  
| **Tamanho retido** | Exibe o tamanho máximo retido entre o mesmo conjunto de objetos.  O tamanho da memória que você pode liberar após um objeto ser excluído \ (e os dependentes não são mais acessados \) é chamado de tamanho retido.  Consulte também [tamanhos de objeto][DevtoolsMemoryProblems101ObjectSizes].  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

Após expandir uma linha de totais no modo de exibição superior, todas as instâncias são exibidas.  Para cada instância, os tamanhos superficial e retido são exibidos nas colunas correspondentes.  O número após o `@` caractere é a ID exclusiva do objeto, permitindo que você compare instantâneos de heap na base por objeto.  

Lembre-se de que os objetos amarelos têm referências JavaScript e os objetos vermelhos são nós desanexados que são referenciados de um com um plano de fundo amarelo.  

**Quais são as várias entradas do Construtor \ (Grupo \) no perfil de heap que correspondem a?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   Grupos de **Construtor**  
:::image-end:::  

| Entrada do Construtor \ (Grupo \) | Descrição |  
|:--- |:--- |  
| **\ (Propriedade global \)** | Os objetos intermediários entre um objeto global \ (como `window` \) e um objeto referenciado por ele.  Se um objeto é criado usando um construtor `Person` e é mantido por um objeto global, o caminho de retenção ficaria como `[global] > \(global property\) > Person` .  Isso contrasta com a norma, onde os objetos fazem referência diretamente uns aos outros.  Existem objetos intermediários por motivos de desempenho.  Os globais são modificados regularmente e as otimizações de acesso à propriedade fazem um bom trabalho para objetos não globais não se aplicam a globais.  |  
| **\ (raízes \)** | As entradas raiz no modo de exibição de árvore de retenção são as entidades que têm referências ao objeto selecionado.  As entradas também podem ser referências criadas pelo mecanismo para fins específicos do mecanismo.  O mecanismo tem caches que fazem referência a objetos, mas todas essas referências são fracas e não impedem que um objeto seja coletado, Considerando que não há nenhuma referência realmente forte.  |  
| **\ (fechamento \)** | Uma contagem de referências a um grupo de objetos por meio de fechamentos de função.  |  
| **\ (matriz, Cadeia de caracteres, número, RegExp \)** | Uma lista de tipos de objeto com propriedades que fazem referência a uma matriz, Cadeia de caracteres, número ou expressão regular.  |  
| **\ (código compilado \)** | Tudo relacionado ao código compilado.  O script é semelhante a uma função, mas corresponde a um `<script>` corpo.  SharedFunctionInfos \ (SFI \) são objetos posicionados entre funções e código compilado.  As funções geralmente têm um contexto, enquanto SFIs não.  |  
| **HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**e assim por diante.  | Referências a elementos ou objetos de documento de um determinado tipo referenciados pelo seu código.  |  

<!--todo: add heap profiling summary section when available -->  

### Modo de exibição comparação  

Encontre objetos vazados comparando vários instantâneos.  Para verificar se uma operação específica do aplicativo não cria vazamentos \ (por exemplo, geralmente um par de operações diretas e inversas, como abrir um documento e, em seguida, fechá-lo, não deve deixar qualquer tipo de lixo \), você pode seguir o cenário abaixo:  

1.  Faça um instantâneo de heap antes de executar uma operação.  
1.  Executar uma operação \ (interaja com uma página de uma maneira que acredite em causar um vazamento \).  
1.  Executar uma operação invertida \ (faça a interação oposta e repita-a algumas vezes \).  
1.  Faça um segundo instantâneo de heap e altere o modo de exibição de um para **comparação**, comparando-o com o **instantâneo 1**.  
    
Na exibição **comparação** , a diferença entre dois instantâneos é exibida.  Ao expandir uma entrada de total, instâncias de objetos adicionadas e excluídas são mostradas.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   Modo de exibição **comparação**  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### Modo de exibição de contenção  

O modo de exibição de **detenção** é essencialmente um "modo de exibição de pássaro" da estrutura objetos do seu aplicativo.  Ele permite que você retome os fechamentos de função dentro para observar os objetos internos da máquina virtual, que juntos compõem seus objetos JavaScript e para compreender a quantidade de memória que seu aplicativo usa em um nível muito baixo.  

| Pontos de entrada do modo de exibição de detenção | Descrição |  
|:--- |:--- |  
| **Objetos DOMWindow** | Objetos globais para código JavaScript.  |  
| **Raízes GC** | As raízes GC reais usadas pelo lixo da VM.  As raízes de GC são compostas de mapas de objetos internos, tabelas de símbolos, pilhas de threads de VM, caches de compilação, escopos de manipulação e identificadores globais.  |  
| **Objetos nativos** | Objetos do navegador "pressionados" dentro da máquina virtual JavaScript \ (JavaScript VM \) para permitir a automação, por exemplo, nós DOM, regras de CSS.  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   Modo de exibição de **contenção**  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Uma dica sobre os fechamentos.  Nomeie as funções para que você possa distinguir facilmente os fechamentos do instantâneo.  Por exemplo, este exemplo não usa funções nomeadas.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> O snippet followingcode usa funções nomeadas.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > Experimente este exemplo de [por que `eval` é perigoso][GlitchDevtoolsMemoryExample07] analisar o impacto dos fechamentos na memória.  Você também pode estar interessado em fazê-lo com este exemplo que o orientará através da gravação de atribuições de [heap][GlitchDevtoolsMemoryExample08].  
> 

## Pesquisar codificação de cores  

Propriedades e valores de propriedade de objetos têm tipos diferentes e são coloridos de acordo.  Cada propriedade tem um dos quatro tipos.  

| Tipo de propriedade | Descrição |  
|:--- |:--- |  
| **a: Propriedade** | Uma propriedade regular com um nome, acessada por meio do `.` operador \ (ponto \) ou por meio da `[` `]` notação de \ (colchetes \), por exemplo `["foo bar"]` .  |  
| **0: elemento** | Uma propriedade regular com um índice numérico, acessada por meio de uma `[` `]` notação de \ (colchetes \).  |  
| **a: var de contexto** |  Uma variável em um contexto de função, acessível pelo nome de variável dentro de um fechamento de função.  |  
| **a: prop System prop** | Uma propriedade adicionada pela VM JavaScript, não pode ser acessada a partir do código JavaScript.  |  

Objetos designados como `System` não têm um tipo de JavaScript correspondente.  Cada parte da implementação do sistema de objetos da VM JavaScript.  V8 aloca a maioria dos objetos internos na mesma heap dos objetos JS do usuário.  Portanto, são apenas V8 internos.  

## Localizar um objeto específico  

Para localizar um objeto na pilha coletada, você pode pesquisar usando `Ctrl` + `F` e dar a identificação do objeto.  

## Descobrir vazamentos do DOM  

O gerador de perfil de heap tem a capacidade de refletir dependências bidirecionais entre objetos nativos do navegador \ (nós DOM, regras CSS \) e objetos JavaScript.
Isso ajuda a descobrir vazamentos de outra forma invisíveis devido às subárvores do DOM desanexadas esquecidas em torno.  

Os vazamentos DOM podem ser maiores do que você imagina.  Considere o exemplo a seguir.  Quando o #tree GC?  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

O `#leaf` mantém uma referência para o pai (ParentNode \) relevante e, recursivamente `#tree` , apenas quando leafRef é nullified é a árvore inteira em `#tree` um candidato para GC.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-tree-gc.msft.png":::
   Subárvores DOM  
:::image-end:::  

> [!NOTE]
> Exemplos: Experimente este exemplo de um [nó de Dom vazando][GlitchDevtoolsMemoryExample06] para compreender onde ele pode vazar e como detectá-lo.  Você também pode examinar esse exemplo de [vazamentos de dom maior do que o esperado][GlitchDevtoolsMemoryExample09].  

Para ler mais sobre vazamentos de DOM e fundamentos de análise de memória, desfaça o check-out [da descoberta e Depurando vazamentos de memória com o Microsoft Edge devtools][GonzaloRuizdeVillaMemory] por Gonzalo Ruiz de Villa.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Tamanhos de objeto-terminologia de memória | Documentos da Microsoft"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Árvore de retenção de objetos – terminologia da memória | Documentos da Microsoft"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html-Microsoft Edge (Chromium) DevTools | Problema"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html-Microsoft Edge (Chromium) DevTools | Problema"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html-Microsoft Edge (Chromium) DevTools | Problema"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html-Microsoft Edge (Chromium) DevTools | Problema"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html-Microsoft Edge (Chromium) DevTools | Problema"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html-Microsoft Edge (Chromium) DevTools | Problema"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "memória | Próximos"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) e é criada por [Meggin Kearney][MegginKearney] \ (redator técnico \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
