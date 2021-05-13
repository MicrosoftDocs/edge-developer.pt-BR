---
description: Saiba como gravar instantâneos de pilha com o profiler de pilha Microsoft Edge DevTools e encontrar vazamentos de memória.
title: Como registrar instantâneos de pilha
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5f097cc45facc7f366a99a9564cf6f3d443f2058
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565012"
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
# <a name="how-to-record-heap-snapshots"></a>Como registrar instantâneos de pilha  

Saiba como gravar instantâneos de pilha com o profiler de pilha Microsoft Edge DevTools e encontrar vazamentos de memória.  

O Microsoft Edge de pilha de DevTools mostra a distribuição de memória pelos objetos JavaScript e nós DOM relacionados da sua página.  Use-o para fazer instantâneos de pilha de JavaScript \(JS heap\) , analisar gráficos de memória, comparar instantâneos e encontrar vazamentos de memória.  Navegue [até a árvore de retenção de objetos][DevtoolsMemoryProblems101ObjectsRetainingTree].  

## <a name="take-a-snapshot"></a>Tirar um instantâneo  

No painel **Memória,** escolha **Tirar instantâneo**e, em seguida, escolha **Iniciar**.  Você também pode selecionar `Ctrl` + `E` \(Windows, Linux\) `Cmd` + `E` ou \(macOS\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Escolher tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Escolher tipo de perfil  
:::image-end:::  

**Os instantâneos** são armazenados inicialmente na memória do processo de renderização.  Instantâneos são transferidos para o DevTools sob demanda, quando você escolhe no ícone de instantâneo para exibi-lo.  

Depois que o instantâneo for carregado no DevTools e tiver sido analisado, o número abaixo do título do instantâneo será exibido e mostrará o tamanho total dos objetos [JavaScript acessíveis.][DevtoolsMemoryProblems101ObjectSizes]  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Tamanho total de objetos acessíveis" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Tamanho total de objetos acessíveis  
:::image-end:::  

> [!NOTE]
> Somente objetos acessíveis são incluídos em instantâneos.  Além disso, tirar um instantâneo sempre começa com uma coleta de lixo.  

## <a name="clear-snapshots"></a>Limpar instantâneos  

Escolha **Limpar todos os perfis** ícone para remover instantâneos \(tanto do DevTools quanto de qualquer memória associada ao processo de renderização\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Remover instantâneos" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Remover instantâneos  
:::image-end:::  

Fechar a janela DevTools não exclui perfis da memória associada ao processo de renderização.  Ao reabrir o DevTools, todos os instantâneos tirados anteriormente reaparecem na lista de instantâneos.  

> [!NOTE]
> Experimente este exemplo de objetos [espalhados e][GlitchDevtoolsMemoryExample03] perfile-o usando o Heap Profiler.  Várias alocações de itens \(object\) são exibidas.  

## <a name="view-snapshots"></a>Exibir instantâneos  

Exibir instantâneos de diferentes perspectivas para tarefas diferentes.  

**O resumo** mostra objetos agrupados pelo nome do construtor.  Use-o para procurar objetos \(e o uso de memória\) com base no tipo agrupado pelo nome do construtor.  É particularmente útil para rastrear **vazamentos de DOM.**

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Exibição de comparação**.  Exibe a diferença entre dois instantâneos.  Use-o para comparar dois instantâneos de memória \(ou mais\) de antes e depois de uma operação.  Inspecionar o delta na memória liberada e na contagem de referência permite confirmar a presença e a causa de um vazamento de memória.  

**Exibição de contenção**.  Permite a exploração de conteúdo de pilha.  **O exibição de** contenção fornece uma melhor visão da estrutura de objetos, ajudando a analisar objetos referenciados no namespace global \(window\) para descobrir o que está mantendo objetos ao redor.  Use-o para analisar fechamentos e mergulhar em seus objetos em um nível baixo.  

Para alternar entre exibições, use o seletor na parte superior do exibição.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Seletor de exibições de opção" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Seletor de exibições de opção  
:::image-end:::  

> [!NOTE]
> Nem todas as propriedades são armazenadas na pilha JavaScript.  As propriedades implementadas usando getters que executem código nativo não são capturadas.  Além disso, valores não-cadeias de caracteres, como números, não são capturados.  

### <a name="summary-view"></a>Exibição de resumo  

Inicialmente, um instantâneo é aberto no exibição Resumo, exibindo totais de objeto, que podem ser expandidos para mostrar instâncias:  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Exibição de resumo" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   **Exibição de** resumo  
:::image-end:::  

As entradas de nível superior são linhas "totais".  

| Entradas de nível superior | Descrição |  
|:--- |:--- |  
| **Construtor** | Representa todos os objetos criados usando esse construtor.  |  
| **Distância** | exibe a distância até a raiz usando o caminho mais curto e simples dos nós.  |  
| **Tamanho superficial** | Exibe a soma de tamanhos rasos de todos os objetos criados por uma determinada função de construtor.  O tamanho superficial é o tamanho da memória mantida por um objeto \(geralmente, matrizes e cadeias de caracteres têm tamanhos rasos maiores\).  Navegue até [Tamanhos de objeto][DevtoolsMemoryProblems101ObjectSizes].  |  
| **Tamanho retido** | Exibe o tamanho máximo retido entre o mesmo conjunto de objetos.  O tamanho da memória que você pode liberar depois que um objeto é excluído \(e os dependentes não são mais acessíveis\) é chamado de tamanho retido.  Navegue até [Tamanhos de objeto][DevtoolsMemoryProblems101ObjectSizes].  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

Depois de expandir uma linha total na exibição superior, todas as instâncias serão exibidas.  Para cada instância, os tamanhos superficial e retido são exibidos nas colunas correspondentes.  O número após o caractere é a ID exclusiva do objeto, permitindo comparar instantâneos de pilha `@` por objeto.  

Lembre-se de que objetos amarelos têm referências JavaScript e objetos vermelhos são nós desvinculados que são referenciados de um com um plano de fundo amarelo.  

**O que as várias entradas do construtor \(group\) no profiler heap correspondem?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Grupos de construtores" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   **Grupos de construtores**  
:::image-end:::  

| Entrada do construtor \(group\) | Descrição |  
|:--- |:--- |  
| **\(propriedade global\)** | Os objetos intermediários entre um objeto global \(like `window` \) e um objeto referenciado por ele.  Se um objeto for criado usando um construtor e for mantido por um objeto global, o caminho de retenção poderá ser `Person` representado como `[global] > \(global property\) > Person` .  Isso contrasta com a norma, onde os objetos se referenciam diretamente uns aos outros.  Objetos intermediários existem por motivos de desempenho.  Os globais são modificados regularmente e as otimizações de acesso a propriedades fazem um bom trabalho para objetos não globais não são aplicáveis para globais.  |  
| **\(roots\)** | As entradas raiz na exibição de árvore de retenção são as entidades que têm referências ao objeto selecionado.  As entradas também podem ser referências criadas pelo mecanismo para fins específicos do mecanismo.  O mecanismo tem caches que objetos de referência, mas todas essas referências são fracas e não impedem que um objeto seja coletado, já que não há referências realmente fortes.  |  
| **\(closure\)** | Uma contagem de referências a um grupo de objetos por meio de fechamentos de função.  |  
| **\(matriz, cadeia de caracteres, número, regexp\)** | Uma lista de tipos de objeto com propriedades que referenciam uma matriz, cadeia de caracteres, número ou expressão regular.  |  
| **\(código compilado\)** | Tudo relacionado ao código compilado.  O script é semelhante a uma função, mas corresponde a um `<script>` corpo.  SharedFunctionInfos \(SFI\) são objetos entre funções e código compilado.  As funções geralmente têm um contexto, enquanto os SFIs não.  |  
| **HTMLDivElement,** **HTMLAnchorElement,** **DocumentFragment**e assim por diante.  | Referências a elementos ou objetos de documento de um tipo específico referenciado pelo código.  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a>Exibição de comparação  

Encontre objetos vazados comparando vários instantâneos uns com os outros.  Para verificar se uma determinada operação de aplicativo não cria vazamentos \(por exemplo, geralmente um par de operações diretas e inversas, como abrir um documento e, em seguida, fecha-lo, não deve deixar lixo\), você pode seguir o cenário abaixo:  

1.  Tire um instantâneo de pilha antes de executar uma operação.  
1.  Execute uma operação \(interaja com uma página de alguma forma que você acredita estar causando um vazamento\).  
1.  Execute uma operação inversa \(faça a interação oposta e repita-a algumas vezes\).  
1.  Pegue um segundo instantâneo de pilha e altere a exibição deste para **Comparison**, comparando-o com **Instantâneo 1**.  
    
No **visualização Comparação,** a diferença entre dois instantâneos é exibida.  Ao expandir uma entrada total, as instâncias de objeto adicionadas e excluídas são mostradas.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Exibição de comparação" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   **Exibição de** comparação  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a>Exibição de contenção  

O **ponto de vista** de contenção é essencialmente um "ponto de vista do pássaro" da estrutura de objetos do seu aplicativo.  Ele permite espiar os fechamentos de função, observar objetos internos \(VM\) da máquina virtual que juntos compõe seus objetos JavaScript e entender quanta memória seu aplicativo usa em um nível muito baixo.  

| Pontos de entrada do visualização de contenção | Descrição |  
|:--- |:--- |  
| **Objetos DOMWindow** | Objetos globais para código JavaScript.  |  
| **Raízes de GC** | As raízes de GC reais usadas pelo lixo da VM.  As raízes de GC são compostas por mapas de objetos integrados, tabelas de símbolos, pilhas de threadS VM, caches de compilação, escopos de alças globais e escopos de compilação.  |  
| **Objetos nativos** | Objetos de navegador "pressionados" dentro da máquina virtual JavaScript \(JavaScript VM\) para permitir a automação, por exemplo, nós dom, regras CSS.  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Exibição de contenção" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   **Exibição de** contenção  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Uma dica sobre fechamentos.  Nomeia as funções para que você possa distinguir facilmente entre fechamentos no instantâneo.  Por exemplo, este exemplo não usa funções nomeadas.  
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
> O trecho de código a seguir usa funções nomeadas.  
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
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > Experimente este exemplo de [por que `eval` é ruim][GlitchDevtoolsMemoryExample07] analisar o impacto de fechamentos na memória.  Você também pode estar interessado em segui-lo com este exemplo que o leva através da gravação de [alocações de heap][GlitchDevtoolsMemoryExample08].  
> 

## <a name="look-up-color-coding"></a>Procurar codificação de cores  

Propriedades e valores de propriedade de objetos têm tipos diferentes e são coloridos de acordo.  Cada propriedade tem um dos quatro tipos.  

| Tipo de propriedade | Descrição |  
|:--- |:--- |  
| **a: propriedade** | Uma propriedade regular com um nome, acessada por meio do `.` operador \(dot\) ou por meio de `[` `]` notação \(colchetes\) por exemplo `["foo bar"]` .  |  
| **0: elemento** | Uma propriedade regular com um índice numérico, acessada `[` `]` por meio de notação \(brackets\).  |  
| **a: var de contexto** |  Uma variável em um contexto de função, acessível pelo nome da variável de dentro de um fechamento de função.  |  
| **a: prop do sistema** | Uma propriedade adicionada pela VM JavaScript, não acessível a partir do código JavaScript.  |  

Os objetos `System` designados como não têm um tipo JavaScript correspondente.  Cada um faz parte da implementação do sistema de objetos da VM Javascript.  O V8 aloca a maioria dos objetos internos na mesma pilha que os objetos JS do usuário.  Portanto, são apenas internos V8.  

## <a name="find-a-specific-object"></a>Encontrar um objeto específico  

Para encontrar um objeto na pilha coletada, você pode pesquisar usando `Ctrl` + `F` e dar a ID do objeto.  

## <a name="uncover-dom-leaks"></a>Descobrir vazamentos de DOM  

O profiler de pilha tem a capacidade de refletir dependências bidirecionais entre objetos nativos do navegador \(nós DOM, regras CSS\) e objetos JavaScript.
Isso ajuda a descobrir, caso contrário, vazamentos invisíveis que ocorrem devido a subárvores DOM desvinculadas esquecidas flutuando.  

Vazamentos de DOM podem ser maiores do que você pensa.  Considere o exemplo a seguir.  Quando é o #tree GC?  

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

O mantém uma referência ao pai `#leaf` relevante \(parentNode\) e recursivamente até , portanto, somente quando leafRef é anulado é a árvore WHOLE sob um candidato `#tree` para `#tree` GC.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Subárvores DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   Subárvores DOM  
:::image-end:::  

> [!NOTE]
> Exemplos: experimente este exemplo de [um nó DOM][GlitchDevtoolsMemoryExample06] que vaza para entender onde ele pode vazar e como detectá-lo.  Você também pode ver este exemplo de [vazamentos de DOM maiores do que o esperado][GlitchDevtoolsMemoryExample09].  

Para ler mais sobre vazamentos de DOM e análises de memória fundamentais checkout Localizar e depurar vazamentos de memória com o [Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] por Gonzalo Gonçalves de Vila.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Tamanhos de objeto - Terminologia de memória | Microsoft Docs"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Árvore de retenção de objetos - Terminologia de memória | Microsoft Docs"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html - Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "memória | Slides"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) e é de autoria de [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
