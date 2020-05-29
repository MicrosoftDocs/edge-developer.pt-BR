---
title: Terminologia da memória
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: e3373cf1475ec0eeaabcebf1a7f49505c7a3c1bb
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611724"
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
   limitations under the License. -->





# Terminologia da memória   



Esta seção descreve os termos comuns usados na análise de memória e se aplica a uma variedade de ferramentas de criação de perfil de memória para diferentes idiomas.  

Os termos e noções aqui descritos referem-se ao [painel memória][DevtoolsMemoryProblemsHeapSnapshots].  Se você já trabalhou com o Java, .NET ou outro gerador de perfil de memória, isso pode ser uma atualização.  

## Tamanhos de objeto  

Pense na memória como um gráfico com tipos primitivos \ (como números e cadeias de caracteres \) e objetos \ (matrizes associativas \).  Ele pode ser representado visualmente como um gráfico com uma série de pontos interconectados da seguinte maneira:  

> ##### Figura 1  
> Representação visual da memória  
>![Representação visual da memória][ImageThinkGraph]  

Um objeto pode conter memória de duas maneiras:  

*   Diretamente pelo objeto.  
*   Implicitamente, mantém referências a outros objetos e, portanto, impedindo que esses objetos sejam descartados automaticamente por um coletor de lixo \ (**GC** para short \).  

Ao trabalhar com o [painel memória][DevtoolsMemoryProblemsHeapSnapshots] no devtools \ (uma ferramenta para investigar problemas de memória encontrados em "memória" \), você pode ver em algumas colunas de informação diferentes.  Dois que se destacam são o tamanho e o **tamanho retidos** **superficiais** , mas o que representam?  

> ##### Figura 2  
> Tamanho superficial e retido  
>![Tamanho superficial e retido][ImageShallowRetained]  

### Tamanho superficial  

Esse é o tamanho da memória que é mantida pelo objeto.  

Objetos JavaScript típicos têm uma certa memória reservada para sua descrição e para armazenar valores imediatos.  Geralmente, somente matrizes e cadeias de caracteres podem ter um tamanho superficial significativo.  No entanto, cadeias de caracteres e matrizes externos geralmente têm seu armazenamento principal na memória do renderizador, expondo apenas um pequeno objeto envoltório na pilha JavaScript.  

Memória do renderizador é toda a memória do processo em que uma página inspecionada é renderizada: memória nativa + JS da memória do JS da memória de heap de página + JS de todos os trabalhadores dedicados iniciados pela página.  No entanto, até mesmo um pequeno objeto pode manter uma grande quantidade de memória indiretamente, evitando que outros objetos sejam descartados pelo processo de coleta de lixo automático.  

### Tamanho retido  

Esse é o tamanho da memória que é liberada depois que o objeto é excluído juntamente com os objetos dependentes que se tornaram inatingíveis de **raízes do coletor de lixo** \ (raízes GC \).  

As **raízes do coletor de lixo** \ (raízes GC \) são formadas por **identificadores** criados \ (local ou global \) ao fazer uma referência do código nativo para um objeto JavaScript fora do V8.  Todos esses identificadores podem ser encontrados em um instantâneo de heap em identificadores de **raiz de GC**  >  **Handle scope** e **GC roots**  >  **identificadores globais**de raízes GC.  Descrever as alças desta documentação sem mergulhar nos detalhes da implementação do navegador pode ser confuso.  As raízes do coletor de lixo (GC) e as alças não são algo de que você precisa se preocupar.  

Há muitas raízes internas de GC, a maioria delas não é interessante para os usuários.  Do ponto de vista dos aplicativos, há tipos de raízes a seguir.  

*   Objeto global da janela \ (em cada iframe \).  Há um campo de distância nos instantâneos de heap que é o número de referências de propriedade no caminho de retenção mais curto da janela.  
*   Documentar a árvore DOM que consiste em todos os nós DOM nativos alcançáveis ao atravessar o documento.  Nem todos os nós podem ter invólucros do JS, mas se um nó tiver um wrapper, ele estará vivo enquanto o documento estiver vivo.  
*   Às vezes, os objetos podem ser mantidos pelo contexto do depurador no painel **fontes** e no **console** \ (por exemplo, após a avaliação do console \).  Crie instantâneos de heap com um painel de **console** limpo e nenhum ponto de interrupção ativo no depurador no painel **fontes** .

>[!TIP]
> Limpe o painel do **console** executando `clear()` e desative pontos de interrupção no painel **fontes** antes de colocar um instantâneo de heap no [painel memória][DevtoolsMemoryProblemsHeapSnapshots].

O gráfico memória começa com uma raiz, que pode ser o `window` objeto do navegador ou o `Global` objeto de um módulo node. js.  Você não controla como esse objeto raiz é coletado como lixo (MDC).  

> ##### Figura 3  
> Você não pode controlar como o objeto raiz é coletado como lixo \ (MDC \).  
>![Você não pode controlar como o objeto raiz é coletado como lixo (MDC).][ImageDontControl]  

O que não for alcançável da raiz será obtido com o Garbage Collector \ (MDC \).  

> [!NOTE]
> As colunas [tamanho superficial](#shallow-size) e [tamanho retido](#retained-size) representam dados em bytes.  

## Árvore de retenção de objetos  

O heap é uma rede de objetos interconectados.  No mundo matemático, essa estrutura é chamada de gráfico de **gráfico** ou de memória.  Um gráfico é construído a partir de **nós** conectados por meio de **bordas**, ambos recebem rótulos.  

*   Os **nós** \ (ou **objetos**\) são rotulados usando o nome da função do **Construtor** que foi usado para construí-los.  
*   As **bordas** são rotuladas usando os nomes das **Propriedades**.  

Saiba [como gravar um perfil usando o gerador de perfil de heap][DevtoolsMemoryProblemsHeapSnapshots].  Algumas das coisas que você pode ver na gravação do instantâneo de heap no [painel memória][DevtoolsMemoryProblemsHeapSnapshots] na [Figura 4](#figure-4) incluem distância: a distância da raiz do coletor de lixo \ (GC \).  Se praticamente todos os objetos do mesmo tipo estiverem na mesma distância, e alguns estiverem a uma distância maior, isso é algo digno de investigação.  

> ##### Figura 4  
> Distância da raiz  
>![Distância da raiz][ImageRoot]  

## Dominadores  

Os objetos Dominator são compostos de uma estrutura de árvore porque cada objeto tem exatamente um Dominator.  Um Dominator de um objeto pode não ter referências diretas a um objeto que ele domina; ou seja, a árvore do Dominator não é uma árvore de abrangência do gráfico.  

Na [Figura 5](#figure-5):  

*   O nó 1 domina o nó 2  
*   O nó 2 domina os nós 3, 4 e 6  
*   O nó 3 domina o nó 5  
*   Nó 5 dominaos nó 8  
*   O nó 6 domina o nó 7  

> ##### Figura 5  
> Estrutura de árvore Dominator  
>![Estrutura de árvore Dominator][ImageDominatorsSpanning]  

Na [Figura 6](#figure-6), nó `#3` é o Dominator de `#10` , mas `#7` também existe em cada caminho simples do Garbage Collector \ (GC \) a `#10` .  Portanto, um objeto B é um Dominator de um objeto A se B existir em cada caminho simples da raiz para o objeto A.  

> ##### Figura 6  
> Ilustração Dominator animada  
>![Ilustração Dominator animada][ImageDominators]  

## Especificações do V8  

Ao criar o perfil da memória, é útil entender por que os instantâneos de pilha parecem uma determinada maneira.  Esta seção descreve alguns tópicos relacionados à memória, especificamente correspondentes à **máquina virtual V8 JavaScript** \ (V8 VM ou VM \).  

### Representação de objeto JavaScript  

Há três tipos primitivos:  

*   Números \ (por exemplo `3.14159...` \)  
*   Booleanos \ ( `true` ou `false` \)  
*   Cadeias de caracteres \ (por exemplo, `"Werner Heisenberg"` \)  

Primitivas não podem fazer referência a outros valores e são sempre folhas ou nós de terminação.  

Os **números** podem ser armazenados como:  

*   um valor inteiro de 31 bits imediato chamado **pequenos inteiros** \ (**SMI**s \) ou  
*   objetos de heap, chamados de **números de heap**. Os números de pilha são usados para armazenar valores que não se enquadram no formulário SMI, como **duplicatas**, ou quando um valor precisa ser **in box**, como definir propriedades nele.  

**Cadeias de caracteres** podem ser armazenadas em ambos:  

*   o **heap de VM**ou
*   externamente na **memória do renderizador**.  Um **objeto envoltório** é criado e usado para acessar o armazenamento externo em que, por exemplo, as fontes de script e outros conteúdos recebidos da Web são armazenados, em vez de serem copiados para o heap de VM.

A memória de novos objetos JavaScript é atribuída a partir de uma heap JavaScript dedicada \ (ou **heap de VM**\).  Esses objetos são gerenciados pelo coletor de lixo no V8 e, portanto, permanecerão ativos desde que haja pelo menos uma referência forte a ele.  

Qualquer coisa que não esteja na pilha JavaScript é chamada de **objeto nativo**.  Os objetos nativos, em contraste a objetos de heap, não são gerenciados pelo coletor de lixo do V8 durante o ciclo de vida, e só podem ser acessados a partir do JavaScript usando o objeto de invólucro JavaScript.  

A **cadeia de caracteres de desvantagens** é um objeto que consiste em pares de cadeias de caracteres armazenadas e depois Unidas, e é um resultado de concatenação.  A junção do conteúdo da **cadeia de caracteres de desvantagens** ocorre apenas conforme necessário. Um exemplo seria quando uma subcadeia de caracteres de uma cadeia de caracteres associada precisa ser criada.

Por exemplo, se você concatenar `a` e `b` receber uma cadeia de caracteres `(a, b)` que representa o resultado da concatenação.  Se mais tarde concatenar `d` com esse resultado, você receber outra **cadeia de caracteres de contras**: `((a, b, d)` .  

**Matriz** é um objeto com teclas numéricas. As **matrizes** são usadas amplamente na VM V8 para armazenar grandes quantidades de dados. Conjuntos de pares de valor chave, como dicionários, são copiados por **matrizes**.  

Um objeto JavaScript típico é armazenado apenas como um dos dois tipos de **matriz** :  

*   propriedades nomeadas e  
*   elementos numéricos  

Quando há um pequeno número de propriedades, as propriedades são armazenadas internamente no objeto JavaScript.  

**Mapa** é um objeto que descreve o tipo de objeto e o layout. Por exemplo, os mapas são usados para descrever hierarquias de objetos implícitos para [acesso rápido a Propriedades][V8FastProperties].  


### Grupos de objetos  

Cada grupo de **objetos nativos** é composto por objetos que mantêm referências mútuas entre si.  Considere, por exemplo, uma subárvore DOM em que cada nó tenha um link para o pai relativo e se vincule ao próximo filho e ao próximo irmão, criando um gráfico conectado.  Observe que os objetos nativos não são representados na pilha JavaScript – é por isso que os objetos nativos têm tamanho zero. Em vez disso, os objetos de conteúdo adicional são criados.  

Cada objeto envoltório mantém uma referência ao objeto nativo correspondente, para redirecionar comandos para ele.  Por sua vez, um grupo de objetos contém objetos envoltório.  No entanto, isso não cria um ciclo não colecionável, pois o coletor de lixo \ (GC \) é inteligente o suficiente para liberar grupos de objetos cujos wrappers não são mais referenciados. Mas esquecer de liberar um único wrapper mantém o grupo inteiro e os wrappers associados.  

<!--## Feedback   -->  



<!-- image links -->  

[ImageThinkGraph]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-thinkgraph.msft.png "Figura 1: representação visual da memória"  
[ImageShallowRetained]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-shallow-retained.msft.png "Figura 2: tamanho superficial e retido"  
[ImageDontControl]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dontcontrol.msft.png "Figura 3: você não pode controlar como o objeto raiz é lixo coletado (MDC)."  
[ImageRoot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-root.msft.png "Figura 4: distância da raiz"  
[ImageDominatorsSpanning]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dominatorsspanning.msft.png "Figura 5: estrutura de árvore Dominator"  
[ImageDominators]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dominators.msft.gif "Figura 6: ilustração Dominator animada"  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: /microsoft-edge/devtools-guide-chromium/media/memory-problems/heap-snapshots "/microsoft-edge/devtools-guide-chromium/media/memory-problems"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propriedades rápidas no V8 | V8"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) e é criada por [Meggin Kearney][MegginKearney] \ (redator técnico \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
