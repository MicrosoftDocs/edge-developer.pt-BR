---
description: Esta seção descreve termos comuns usados na análise de memória e é aplicável a uma variedade de ferramentas de criação de perfil de memória para idiomas diferentes.
title: Terminologia de memória
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c9659255e2bf0082cd1be3e6615c9d54c293b967
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519307"
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

# <a name="memory-terminology"></a>Terminologia de memória  

Este artigo descreve termos comuns usados na análise de memória e é aplicável a várias ferramentas de criação de perfil de memória para idiomas diferentes.  

Os termos e noções descritas aqui referem-se ao [painel Memória][DevtoolsMemoryProblemsHeapSnapshots].  Se você já trabalhou com o Java, o .NET ou outro profiler de memória, este artigo pode ser um atualizador.  

## <a name="object-sizes"></a>Tamanhos de objetos  

Pense na memória como um gráfico com tipos primitivos \(como números e cadeias de caracteres\) e objetos \(matrizes associativas\).  Ele pode ser exibido como um gráfico com muitos pontos interconectados, como a figura a seguir.  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Representação visual da memória" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   Representação visual da memória  
:::image-end:::  

Um objeto pode conter memória de duas maneiras:  

*   Diretamente pelo objeto.  
*   Implicitamente segurando referências a outros objetos e, portanto, impedindo que esses objetos são descartados automaticamente por um coletor de lixo.  

Ao trabalhar [][DevtoolsMemoryProblemsHeapSnapshots] com o painel Memória no DevTools \(uma ferramenta para investigar problemas de memória encontrados em **Memória**\), você pode ver algumas colunas de informações diferentes.  Dois que se destacam são **Tamanho Superficial** e **Tamanho Retido**, mas o que eles representam?  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tamanho superficial e retido" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   Tamanho superficial e retido  
:::image-end:::  

### <a name="shallow-size"></a>Tamanho superficial  

Esse é o tamanho da memória que é mantida pelo objeto.  

Objetos JavaScript típicos têm alguma memória reservada para sua descrição e para armazenar valores imediatos.  Normalmente, apenas matrizes e cadeias de caracteres são capazes de ter um tamanho superficial significativo.  No entanto, cadeias de caracteres e matrizes externas geralmente têm seu armazenamento principal na memória do renderador, expondo apenas um pequeno objeto wrapper na pilha JavaScript.  

A memória do renderador é toda a memória do processo em que uma página inspecionada é renderizada: memória nativa + memória de pilha JS da página + memória de pilha JS de todos os funcionários dedicados iniciados pela página.  No entanto, mesmo um objeto pequeno é capaz de manter uma grande quantidade de memória indiretamente, impedindo que outros objetos são descartados pelo processo de coleta automática de lixo.  

### <a name="retained-size"></a>Tamanho retido  

Esse é o tamanho da memória que é liberada depois que o objeto é excluído juntamente com os objetos dependentes que foram inacessível a partir das raízes do Coletor de **Lixo.**  

**As raízes** do Coletor de Lixo são feitas de **alças criadas** \(local ou global\) ao fazer uma referência do código nativo para um objeto JavaScript fora do V8.  Todas essas alças podem ser encontradas em um instantâneo de pilha sob raízes **de GC**Manipular escopo e  >  **** raízes **de GC**  >  **Alças globais**.  Descrever as alças nesta documentação sem mergulhar em detalhes da implementação do navegador pode ser confuso.  As raízes do Coletor de Lixo e as alças não são algo com o que você precisa se preocupar.  

Há muitas raízes internas do Coletor de Lixo, a maioria das quais não são interessantes para os usuários.  Do ponto de vista de aplicativos, há os seguintes tipos de raízes.  

*   Objeto global da janela \(em cada iframe\).  Nos instantâneos de pilha, o campo indica o número de referências de propriedade no caminho de retenção mais `distance` curto da janela.  
*   A árvore DOM do documento, que consiste em todos os nós DOM nativos que podem ser alcançadas ao percorrer o documento.  Nem todos os nós têm invólucros JavaScript, mas se um nó tiver um wrapper, o nó está vivo enquanto o documento está vivo.  
*   Às vezes, os objetos são mantidos pelo contexto de depuração na ferramenta **Sources** e **no Console**, como após a avaliação do Console.  Crie instantâneos de pilha com uma ferramenta **console** des limpa e nenhum ponto de interrupção ativo no depurador na **ferramenta Sources.**

>[!TIP]
> Antes de tirar um instantâneo de pilha na [ferramenta Memória,][DevtoolsMemoryProblemsHeapSnapshots] limpe a **ferramenta Console** e desative pontos de interrupção na **ferramenta Sources.**  Para limpar a **ferramenta Console,** execute o `clear()` método.  

O gráfico de memória começa com uma raiz, que pode ser o objeto do navegador ou o objeto `window` `Global` de um Node.js módulo.  Você não controla como o objeto raiz é coletado.  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Você não é capaz de controlar como o objeto raiz é coletado." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   Você não é capaz de controlar como o objeto raiz é coletado.  
:::image-end:::  

O que não puder ser obtido da raiz obtém o lixo coletado.  

> [!NOTE]
> As [colunas Tamanho Superficial](#shallow-size) e [Tamanho Retido](#retained-size) representam dados em bytes.  

## <a name="objects-retaining-tree"></a>Árvore de retenção de objetos  

A pilha é uma rede de objetos interconectados.  No mundo matemático, essa estrutura é chamada de **gráfico ou** gráfico de memória.  Um gráfico é construído a partir de **nós conectados** por meio de **bordas**, ambos são determinados rótulos.  

*   **Nós** \(ou **objetos**\) são rotulados **** usando o nome da função de construtor que foi usada para criar eles.  
*   **Bordas** são rotuladas usando os nomes das **propriedades**.  

Saiba [como registrar um perfil usando o Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].  Na figura a seguir, algumas das coisas notáveis [][DevtoolsMemoryProblemsHeapSnapshots] na gravação de Instantâneo de Pilha na ferramenta Memória incluem distância: a distância da raiz coletor de lixo.  Se quase todos os objetos do mesmo tipo estão na mesma distância e alguns estão a uma distância maior, isso é algo que vale a pena investigar.  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distância da raiz" lightbox="../media/memory-problems-root.msft.png":::
   Distância da raiz  
:::image-end:::  

## <a name="dominators"></a>Dominadores  

Os objetos Dominator são compostos por uma estrutura de árvore porque cada objeto tem exatamente um dominador.  Um dominador de um objeto pode não ter referências diretas a um objeto que ele domina; ou seja, a árvore do dominador não é uma árvore de abrangção do gráfico.  

Na figura a seguir, a instrução a seguir é verdadeira.  

*   Nó 1 domina o nó 2  
*   O nó 2 domina os nós 3, 4 e 6  
*   Nó 3 domina o nó 5  
*   O nó 5 domina o nó 8  
*   Nó 6 domina o nó 7  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Estrutura de árvore do Dominator" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   Estrutura de árvore do Dominator  
:::image-end:::  

Na figura a seguir, o nó é o dominador de , mas também existe em cada caminho simples de `#3` Coletor de Lixo para `#10` `#7` `#10` .  Portanto, um objeto B é um dominador de um objeto A se B existir em cada caminho simples da raiz para o objeto A.  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Ilustração do dominador animado" lightbox="../media/memory-problems-dominators.msft.gif":::
   Ilustração do dominador animado  
:::image-end:::  

## <a name="v8-specifics"></a>Especificações da V8  

Ao perfilar memória, é útil entender por que os instantâneos de pilha têm uma certa aparência.  Esta seção descreve alguns tópicos relacionados à memória especificamente correspondentes à máquina **virtual JavaScript V8** \(V8 VM ou VM\).  

### <a name="javascript-object-representation"></a>Representação de objeto JavaScript  

Há três tipos primitivos:  

*   Números \(por exemplo `3.14159...` \)  
*   Booleans \( `true` or `false` \)  
*   Cadeias de caracteres \(por exemplo `"Werner Heisenberg"` \)  

Primitivos não são capazes de referenciar outros valores e são sempre folhas ou nós de término.  

**Os** números podem ser armazenados como:  

*   um valor inteiro imediato de 31 bits chamado **números inteiros** pequenos \(**SMI**s\) ou  
*   objetos heap, chamados de **números de pilha**. Os números de pilha são usados para armazenar valores que não se ajustam ao formulário SMI, como **duplos**, ou quando um valor precisa ser in a **box,** como a definição de propriedades nele.  

**Cadeias de caracteres** podem ser armazenadas em:  

*   a **pilha de VM**ou
*   externamente na **memória do renderador**.  Um objeto **wrapper** é criado e usado para acessar o armazenamento externo em que, por exemplo, as fontes de script e outros conteúdos recebidos da Web são armazenados, em vez de copiados para a pilha de VM.

A memória para novos objetos JavaScript é alocada de uma pilha JavaScript dedicada \(ou **pilha de VM**\).  Esses objetos são gerenciados pelo coletor de lixo em V8 e, portanto, permanecem vivos desde que haja pelo menos uma referência forte a eles.  

Qualquer coisa que não seja na pilha JavaScript é chamado de **objeto nativo**.  Os objetos nativos, em contraste com objetos heap, não são gerenciados pelo coletor de lixo V8 durante todo o tempo de vida e só podem ser acessados do JavaScript usando o objeto wrapper JavaScript.  

**A cadeia de** caracteres cons é um objeto que consiste em pares de cadeias de caracteres armazenadas e ingressadas e é resultado de concatenação.  A junção do conteúdo da cadeia **de caracteres** de cons ocorre apenas conforme necessário.  Por exemplo, quando uma subdistência de uma cadeia de caracteres ingressada precisa ser construída.

Por exemplo, se você concatenar `a` e , você obter uma cadeia de `b` `(a, b)` caracteres que representa o resultado da concatenação.  Se você tiver concatenado `d` posteriormente com esse resultado, você obterá outra **cadeia de caracteres contras:** `((a, b, d)` .  

**Matriz** é um objeto com chaves numéricas. **As matrizes** são amplamente usadas na V8 VM para armazenar grandes quantidades de dados. Conjuntos de pares de valores-chave, como dicionários, são respaldados **por matrizes**.  

Um objeto JavaScript típico é armazenado como apenas um dos dois tipos **de** matriz:  

*   propriedades nomeadas e  
*   elementos numéricos  

Quando há um pequeno número de propriedades, as propriedades são armazenadas internamente no objeto JavaScript.  

**Map** é um objeto que descreve o tipo de objeto que é e o layout. Por exemplo, mapas são usados para descrever hierarquias de objetos implícitos para [acesso rápido a propriedades][V8FastProperties].  

### <a name="object-groups"></a>Grupos de objetos  

Cada **grupo de objetos** nativos é feito de objetos que têm referências mútuas entre si.  Considere, por exemplo, uma subárvore DOM onde cada nó tem um link para o pai relativo e links para o próximo filho e o próximo irmão, portanto, formando um gráfico conectado.  

> [!NOTE]
> Os objetos nativos não são representados na pilha JavaScript.  A falta de representação é o motivo pelo qual os objetos nativos têm tamanho zero. Em vez disso, os objetos wrapper são criados.  

Cada objeto wrapper contém uma referência ao objeto nativo correspondente, para redirecionar comandos para ele.  Por sua vez, um grupo de objetos contém objetos wrapper.  No entanto, isso não cria um ciclo inigualável, pois o Coletor de Lixo é inteligente o suficiente para liberar grupos de objetos cujos wrappers não são mais referenciados.  Mas esquecer de liberar um único wrapper contém todo o grupo e wrappers associados.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Como registrar instantâneos de pilha | Microsoft Docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propriedades rápidas no V8 | V8"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) e é de autoria de [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
