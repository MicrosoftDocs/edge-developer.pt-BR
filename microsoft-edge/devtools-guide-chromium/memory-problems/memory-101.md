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





# <span data-ttu-id="79c94-103">Terminologia da memória</span><span class="sxs-lookup"><span data-stu-id="79c94-103">Memory Terminology</span></span>   



<span data-ttu-id="79c94-104">Esta seção descreve os termos comuns usados na análise de memória e se aplica a uma variedade de ferramentas de criação de perfil de memória para diferentes idiomas.</span><span class="sxs-lookup"><span data-stu-id="79c94-104">This section describes common terms used in memory analysis, and is applicable to a variety of memory profiling tools for different languages.</span></span>  

<span data-ttu-id="79c94-105">Os termos e noções aqui descritos referem-se ao [painel memória][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="79c94-105">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="79c94-106">Se você já trabalhou com o Java, .NET ou outro gerador de perfil de memória, isso pode ser uma atualização.</span><span class="sxs-lookup"><span data-stu-id="79c94-106">If you have ever worked with either the Java, .NET, or some other memory profiler, then this may be a refresher.</span></span>  

## <span data-ttu-id="79c94-107">Tamanhos de objeto</span><span class="sxs-lookup"><span data-stu-id="79c94-107">Object sizes</span></span>  

<span data-ttu-id="79c94-108">Pense na memória como um gráfico com tipos primitivos \ (como números e cadeias de caracteres \) e objetos \ (matrizes associativas \).</span><span class="sxs-lookup"><span data-stu-id="79c94-108">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="79c94-109">Ele pode ser representado visualmente como um gráfico com uma série de pontos interconectados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="79c94-109">It might visually be represented as a graph with a number of interconnected points as follows:</span></span>  

> ##### <span data-ttu-id="79c94-110">Figura 1</span><span class="sxs-lookup"><span data-stu-id="79c94-110">Figure 1</span></span>  
> <span data-ttu-id="79c94-111">Representação visual da memória</span><span class="sxs-lookup"><span data-stu-id="79c94-111">Visual representation of memory</span></span>  
>![Representação visual da memória][ImageThinkGraph]  

<span data-ttu-id="79c94-113">Um objeto pode conter memória de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="79c94-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="79c94-114">Diretamente pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="79c94-114">Directly by the object.</span></span>  
*   <span data-ttu-id="79c94-115">Implicitamente, mantém referências a outros objetos e, portanto, impedindo que esses objetos sejam descartados automaticamente por um coletor de lixo \ (**GC** para short \).</span><span class="sxs-lookup"><span data-stu-id="79c94-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector \(**GC** for short\).</span></span>  

<span data-ttu-id="79c94-116">Ao trabalhar com o [painel memória][DevtoolsMemoryProblemsHeapSnapshots] no devtools \ (uma ferramenta para investigar problemas de memória encontrados em "memória" \), você pode ver em algumas colunas de informação diferentes.</span><span class="sxs-lookup"><span data-stu-id="79c94-116">When working with the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] in DevTools \(a tool for investigating memory issues found under "Memory"\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="79c94-117">Dois que se destacam são o tamanho e o **tamanho retidos** **superficiais** , mas o que representam?</span><span class="sxs-lookup"><span data-stu-id="79c94-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

> ##### <span data-ttu-id="79c94-118">Figura 2</span><span class="sxs-lookup"><span data-stu-id="79c94-118">Figure 2</span></span>  
> <span data-ttu-id="79c94-119">Tamanho superficial e retido</span><span class="sxs-lookup"><span data-stu-id="79c94-119">Shallow and Retained Size</span></span>  
>![Tamanho superficial e retido][ImageShallowRetained]  

### <span data-ttu-id="79c94-121">Tamanho superficial</span><span class="sxs-lookup"><span data-stu-id="79c94-121">Shallow size</span></span>  

<span data-ttu-id="79c94-122">Esse é o tamanho da memória que é mantida pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="79c94-122">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="79c94-123">Objetos JavaScript típicos têm uma certa memória reservada para sua descrição e para armazenar valores imediatos.</span><span class="sxs-lookup"><span data-stu-id="79c94-123">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="79c94-124">Geralmente, somente matrizes e cadeias de caracteres podem ter um tamanho superficial significativo.</span><span class="sxs-lookup"><span data-stu-id="79c94-124">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="79c94-125">No entanto, cadeias de caracteres e matrizes externos geralmente têm seu armazenamento principal na memória do renderizador, expondo apenas um pequeno objeto envoltório na pilha JavaScript.</span><span class="sxs-lookup"><span data-stu-id="79c94-125">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="79c94-126">Memória do renderizador é toda a memória do processo em que uma página inspecionada é renderizada: memória nativa + JS da memória do JS da memória de heap de página + JS de todos os trabalhadores dedicados iniciados pela página.</span><span class="sxs-lookup"><span data-stu-id="79c94-126">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="79c94-127">No entanto, até mesmo um pequeno objeto pode manter uma grande quantidade de memória indiretamente, evitando que outros objetos sejam descartados pelo processo de coleta de lixo automático.</span><span class="sxs-lookup"><span data-stu-id="79c94-127">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <span data-ttu-id="79c94-128">Tamanho retido</span><span class="sxs-lookup"><span data-stu-id="79c94-128">Retained size</span></span>  

<span data-ttu-id="79c94-129">Esse é o tamanho da memória que é liberada depois que o objeto é excluído juntamente com os objetos dependentes que se tornaram inatingíveis de **raízes do coletor de lixo** \ (raízes GC \).</span><span class="sxs-lookup"><span data-stu-id="79c94-129">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots** \(GC roots\) .</span></span>  

<span data-ttu-id="79c94-130">As **raízes do coletor de lixo** \ (raízes GC \) são formadas por **identificadores** criados \ (local ou global \) ao fazer uma referência do código nativo para um objeto JavaScript fora do V8.</span><span class="sxs-lookup"><span data-stu-id="79c94-130">**Garbage Collector roots** \(GC roots\) are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="79c94-131">Todos esses identificadores podem ser encontrados em um instantâneo de heap em identificadores de **raiz de GC**  >  **Handle scope** e **GC roots**  >  **identificadores globais**de raízes GC.</span><span class="sxs-lookup"><span data-stu-id="79c94-131">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="79c94-132">Descrever as alças desta documentação sem mergulhar nos detalhes da implementação do navegador pode ser confuso.</span><span class="sxs-lookup"><span data-stu-id="79c94-132">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="79c94-133">As raízes do coletor de lixo (GC) e as alças não são algo de que você precisa se preocupar.</span><span class="sxs-lookup"><span data-stu-id="79c94-133">Both Garbage Collector (GC) roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="79c94-134">Há muitas raízes internas de GC, a maioria delas não é interessante para os usuários.</span><span class="sxs-lookup"><span data-stu-id="79c94-134">There are lots of internal GC roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="79c94-135">Do ponto de vista dos aplicativos, há tipos de raízes a seguir.</span><span class="sxs-lookup"><span data-stu-id="79c94-135">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="79c94-136">Objeto global da janela \ (em cada iframe \).</span><span class="sxs-lookup"><span data-stu-id="79c94-136">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="79c94-137">Há um campo de distância nos instantâneos de heap que é o número de referências de propriedade no caminho de retenção mais curto da janela.</span><span class="sxs-lookup"><span data-stu-id="79c94-137">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="79c94-138">Documentar a árvore DOM que consiste em todos os nós DOM nativos alcançáveis ao atravessar o documento.</span><span class="sxs-lookup"><span data-stu-id="79c94-138">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="79c94-139">Nem todos os nós podem ter invólucros do JS, mas se um nó tiver um wrapper, ele estará vivo enquanto o documento estiver vivo.</span><span class="sxs-lookup"><span data-stu-id="79c94-139">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="79c94-140">Às vezes, os objetos podem ser mantidos pelo contexto do depurador no painel **fontes** e no **console** \ (por exemplo, após a avaliação do console \).</span><span class="sxs-lookup"><span data-stu-id="79c94-140">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="79c94-141">Crie instantâneos de heap com um painel de **console** limpo e nenhum ponto de interrupção ativo no depurador no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="79c94-141">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="79c94-142">Limpe o painel do **console** executando `clear()` e desative pontos de interrupção no painel **fontes** antes de colocar um instantâneo de heap no [painel memória][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="79c94-142">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="79c94-143">O gráfico memória começa com uma raiz, que pode ser o `window` objeto do navegador ou o `Global` objeto de um módulo node. js.</span><span class="sxs-lookup"><span data-stu-id="79c94-143">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="79c94-144">Você não controla como esse objeto raiz é coletado como lixo (MDC).</span><span class="sxs-lookup"><span data-stu-id="79c94-144">You do not control how this root object is garbage collected (GCd).</span></span>  

> ##### <span data-ttu-id="79c94-145">Figura 3</span><span class="sxs-lookup"><span data-stu-id="79c94-145">Figure 3</span></span>  
> <span data-ttu-id="79c94-146">Você não pode controlar como o objeto raiz é coletado como lixo \ (MDC \).</span><span class="sxs-lookup"><span data-stu-id="79c94-146">You are not able to control how the root object is garbage collected \(GCd\).</span></span>  
>![Você não pode controlar como o objeto raiz é coletado como lixo (MDC).][ImageDontControl]  

<span data-ttu-id="79c94-148">O que não for alcançável da raiz será obtido com o Garbage Collector \ (MDC \).</span><span class="sxs-lookup"><span data-stu-id="79c94-148">Whatever is not reachable from the root gets garbage collected \(GCd\).</span></span>  

> [!NOTE]
> <span data-ttu-id="79c94-149">As colunas [tamanho superficial](#shallow-size) e [tamanho retido](#retained-size) representam dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="79c94-149">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <span data-ttu-id="79c94-150">Árvore de retenção de objetos</span><span class="sxs-lookup"><span data-stu-id="79c94-150">Objects retaining tree</span></span>  

<span data-ttu-id="79c94-151">O heap é uma rede de objetos interconectados.</span><span class="sxs-lookup"><span data-stu-id="79c94-151">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="79c94-152">No mundo matemático, essa estrutura é chamada de gráfico de **gráfico** ou de memória.</span><span class="sxs-lookup"><span data-stu-id="79c94-152">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="79c94-153">Um gráfico é construído a partir de **nós** conectados por meio de **bordas**, ambos recebem rótulos.</span><span class="sxs-lookup"><span data-stu-id="79c94-153">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="79c94-154">Os **nós** \ (ou **objetos**\) são rotulados usando o nome da função do **Construtor** que foi usado para construí-los.</span><span class="sxs-lookup"><span data-stu-id="79c94-154">**Nodes**  \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="79c94-155">As **bordas** são rotuladas usando os nomes das **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="79c94-155">**Edges**  are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="79c94-156">Saiba [como gravar um perfil usando o gerador de perfil de heap][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="79c94-156">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="79c94-157">Algumas das coisas que você pode ver na gravação do instantâneo de heap no [painel memória][DevtoolsMemoryProblemsHeapSnapshots] na [Figura 4](#figure-4) incluem distância: a distância da raiz do coletor de lixo \ (GC \).</span><span class="sxs-lookup"><span data-stu-id="79c94-157">Some of the eye-catching things that you may see in the Heap Snapshot recording in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] in [Figure 4](#figure-4) include distance: the distance from the Garbage Collector \(GC\) root.</span></span>  <span data-ttu-id="79c94-158">Se praticamente todos os objetos do mesmo tipo estiverem na mesma distância, e alguns estiverem a uma distância maior, isso é algo digno de investigação.</span><span class="sxs-lookup"><span data-stu-id="79c94-158">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

> ##### <span data-ttu-id="79c94-159">Figura 4</span><span class="sxs-lookup"><span data-stu-id="79c94-159">Figure 4</span></span>  
> <span data-ttu-id="79c94-160">Distância da raiz</span><span class="sxs-lookup"><span data-stu-id="79c94-160">Distance from root</span></span>  
>![Distância da raiz][ImageRoot]  

## <span data-ttu-id="79c94-162">Dominadores</span><span class="sxs-lookup"><span data-stu-id="79c94-162">Dominators</span></span>  

<span data-ttu-id="79c94-163">Os objetos Dominator são compostos de uma estrutura de árvore porque cada objeto tem exatamente um Dominator.</span><span class="sxs-lookup"><span data-stu-id="79c94-163">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="79c94-164">Um Dominator de um objeto pode não ter referências diretas a um objeto que ele domina; ou seja, a árvore do Dominator não é uma árvore de abrangência do gráfico.</span><span class="sxs-lookup"><span data-stu-id="79c94-164">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="79c94-165">Na [Figura 5](#figure-5):</span><span class="sxs-lookup"><span data-stu-id="79c94-165">In [Figure 5](#figure-5):</span></span>  

*   <span data-ttu-id="79c94-166">O nó 1 domina o nó 2</span><span class="sxs-lookup"><span data-stu-id="79c94-166">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="79c94-167">O nó 2 domina os nós 3, 4 e 6</span><span class="sxs-lookup"><span data-stu-id="79c94-167">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="79c94-168">O nó 3 domina o nó 5</span><span class="sxs-lookup"><span data-stu-id="79c94-168">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="79c94-169">Nó 5 dominaos nó 8</span><span class="sxs-lookup"><span data-stu-id="79c94-169">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="79c94-170">O nó 6 domina o nó 7</span><span class="sxs-lookup"><span data-stu-id="79c94-170">Node 6 dominates node 7</span></span>  

> ##### <span data-ttu-id="79c94-171">Figura 5</span><span class="sxs-lookup"><span data-stu-id="79c94-171">Figure 5</span></span>  
> <span data-ttu-id="79c94-172">Estrutura de árvore Dominator</span><span class="sxs-lookup"><span data-stu-id="79c94-172">Dominator tree structure</span></span>  
>![Estrutura de árvore Dominator][ImageDominatorsSpanning]  

<span data-ttu-id="79c94-174">Na [Figura 6](#figure-6), nó `#3` é o Dominator de `#10` , mas `#7` também existe em cada caminho simples do Garbage Collector \ (GC \) a `#10` .</span><span class="sxs-lookup"><span data-stu-id="79c94-174">In [Figure 6](#figure-6), node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector \(GC\) to `#10`.</span></span>  <span data-ttu-id="79c94-175">Portanto, um objeto B é um Dominator de um objeto A se B existir em cada caminho simples da raiz para o objeto A.</span><span class="sxs-lookup"><span data-stu-id="79c94-175">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

> ##### <span data-ttu-id="79c94-176">Figura 6</span><span class="sxs-lookup"><span data-stu-id="79c94-176">Figure 6</span></span>  
> <span data-ttu-id="79c94-177">Ilustração Dominator animada</span><span class="sxs-lookup"><span data-stu-id="79c94-177">Animated dominator illustration</span></span>  
>![Ilustração Dominator animada][ImageDominators]  

## <span data-ttu-id="79c94-179">Especificações do V8</span><span class="sxs-lookup"><span data-stu-id="79c94-179">V8 specifics</span></span>  

<span data-ttu-id="79c94-180">Ao criar o perfil da memória, é útil entender por que os instantâneos de pilha parecem uma determinada maneira.</span><span class="sxs-lookup"><span data-stu-id="79c94-180">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="79c94-181">Esta seção descreve alguns tópicos relacionados à memória, especificamente correspondentes à **máquina virtual V8 JavaScript** \ (V8 VM ou VM \).</span><span class="sxs-lookup"><span data-stu-id="79c94-181">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <span data-ttu-id="79c94-182">Representação de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="79c94-182">JavaScript object representation</span></span>  

<span data-ttu-id="79c94-183">Há três tipos primitivos:</span><span class="sxs-lookup"><span data-stu-id="79c94-183">There are three primitive types:</span></span>  

*   <span data-ttu-id="79c94-184">Números \ (por exemplo `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="79c94-184">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="79c94-185">Booleanos \ ( `true` ou `false` \)</span><span class="sxs-lookup"><span data-stu-id="79c94-185">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="79c94-186">Cadeias de caracteres \ (por exemplo, `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="79c94-186">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="79c94-187">Primitivas não podem fazer referência a outros valores e são sempre folhas ou nós de terminação.</span><span class="sxs-lookup"><span data-stu-id="79c94-187">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="79c94-188">Os **números** podem ser armazenados como:</span><span class="sxs-lookup"><span data-stu-id="79c94-188">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="79c94-189">um valor inteiro de 31 bits imediato chamado **pequenos inteiros** \ (**SMI**s \) ou</span><span class="sxs-lookup"><span data-stu-id="79c94-189">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="79c94-190">objetos de heap, chamados de **números de heap**.</span><span class="sxs-lookup"><span data-stu-id="79c94-190">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="79c94-191">Os números de pilha são usados para armazenar valores que não se enquadram no formulário SMI, como **duplicatas**, ou quando um valor precisa ser **in box**, como definir propriedades nele.</span><span class="sxs-lookup"><span data-stu-id="79c94-191">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="79c94-192">**Cadeias de caracteres** podem ser armazenadas em ambos:</span><span class="sxs-lookup"><span data-stu-id="79c94-192">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="79c94-193">o **heap de VM**ou</span><span class="sxs-lookup"><span data-stu-id="79c94-193">the **VM heap**, or</span></span>
*   <span data-ttu-id="79c94-194">externamente na **memória do renderizador**.</span><span class="sxs-lookup"><span data-stu-id="79c94-194">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="79c94-195">Um **objeto envoltório** é criado e usado para acessar o armazenamento externo em que, por exemplo, as fontes de script e outros conteúdos recebidos da Web são armazenados, em vez de serem copiados para o heap de VM.</span><span class="sxs-lookup"><span data-stu-id="79c94-195">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="79c94-196">A memória de novos objetos JavaScript é atribuída a partir de uma heap JavaScript dedicada \ (ou **heap de VM**\).</span><span class="sxs-lookup"><span data-stu-id="79c94-196">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="79c94-197">Esses objetos são gerenciados pelo coletor de lixo no V8 e, portanto, permanecerão ativos desde que haja pelo menos uma referência forte a ele.</span><span class="sxs-lookup"><span data-stu-id="79c94-197">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="79c94-198">Qualquer coisa que não esteja na pilha JavaScript é chamada de **objeto nativo**.</span><span class="sxs-lookup"><span data-stu-id="79c94-198">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="79c94-199">Os objetos nativos, em contraste a objetos de heap, não são gerenciados pelo coletor de lixo do V8 durante o ciclo de vida, e só podem ser acessados a partir do JavaScript usando o objeto de invólucro JavaScript.</span><span class="sxs-lookup"><span data-stu-id="79c94-199">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="79c94-200">A **cadeia de caracteres de desvantagens** é um objeto que consiste em pares de cadeias de caracteres armazenadas e depois Unidas, e é um resultado de concatenação.</span><span class="sxs-lookup"><span data-stu-id="79c94-200">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="79c94-201">A junção do conteúdo da **cadeia de caracteres de desvantagens** ocorre apenas conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="79c94-201">The joining of the **cons string** contents occurs only as needed.</span></span> <span data-ttu-id="79c94-202">Um exemplo seria quando uma subcadeia de caracteres de uma cadeia de caracteres associada precisa ser criada.</span><span class="sxs-lookup"><span data-stu-id="79c94-202">An example would be when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="79c94-203">Por exemplo, se você concatenar `a` e `b` receber uma cadeia de caracteres `(a, b)` que representa o resultado da concatenação.</span><span class="sxs-lookup"><span data-stu-id="79c94-203">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="79c94-204">Se mais tarde concatenar `d` com esse resultado, você receber outra **cadeia de caracteres de contras**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="79c94-204">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="79c94-205">**Matriz** é um objeto com teclas numéricas.</span><span class="sxs-lookup"><span data-stu-id="79c94-205">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="79c94-206">As **matrizes** são usadas amplamente na VM V8 para armazenar grandes quantidades de dados.</span><span class="sxs-lookup"><span data-stu-id="79c94-206">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="79c94-207">Conjuntos de pares de valor chave, como dicionários, são copiados por **matrizes**.</span><span class="sxs-lookup"><span data-stu-id="79c94-207">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="79c94-208">Um objeto JavaScript típico é armazenado apenas como um dos dois tipos de **matriz** :</span><span class="sxs-lookup"><span data-stu-id="79c94-208">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="79c94-209">propriedades nomeadas e</span><span class="sxs-lookup"><span data-stu-id="79c94-209">named properties, and</span></span>  
*   <span data-ttu-id="79c94-210">elementos numéricos</span><span class="sxs-lookup"><span data-stu-id="79c94-210">numeric elements</span></span>  

<span data-ttu-id="79c94-211">Quando há um pequeno número de propriedades, as propriedades são armazenadas internamente no objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="79c94-211">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="79c94-212">**Mapa** é um objeto que descreve o tipo de objeto e o layout.</span><span class="sxs-lookup"><span data-stu-id="79c94-212">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="79c94-213">Por exemplo, os mapas são usados para descrever hierarquias de objetos implícitos para [acesso rápido a Propriedades][V8FastProperties].</span><span class="sxs-lookup"><span data-stu-id="79c94-213">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  


### <span data-ttu-id="79c94-214">Grupos de objetos</span><span class="sxs-lookup"><span data-stu-id="79c94-214">Object groups</span></span>  

<span data-ttu-id="79c94-215">Cada grupo de **objetos nativos** é composto por objetos que mantêm referências mútuas entre si.</span><span class="sxs-lookup"><span data-stu-id="79c94-215">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="79c94-216">Considere, por exemplo, uma subárvore DOM em que cada nó tenha um link para o pai relativo e se vincule ao próximo filho e ao próximo irmão, criando um gráfico conectado.</span><span class="sxs-lookup"><span data-stu-id="79c94-216">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, thus forming a connected graph.</span></span>  <span data-ttu-id="79c94-217">Observe que os objetos nativos não são representados na pilha JavaScript – é por isso que os objetos nativos têm tamanho zero.</span><span class="sxs-lookup"><span data-stu-id="79c94-217">Note that native objects are not represented in the JavaScript heap  —  that is why native objects have zero size.</span></span> <span data-ttu-id="79c94-218">Em vez disso, os objetos de conteúdo adicional são criados.</span><span class="sxs-lookup"><span data-stu-id="79c94-218">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="79c94-219">Cada objeto envoltório mantém uma referência ao objeto nativo correspondente, para redirecionar comandos para ele.</span><span class="sxs-lookup"><span data-stu-id="79c94-219">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="79c94-220">Por sua vez, um grupo de objetos contém objetos envoltório.</span><span class="sxs-lookup"><span data-stu-id="79c94-220">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="79c94-221">No entanto, isso não cria um ciclo não colecionável, pois o coletor de lixo \ (GC \) é inteligente o suficiente para liberar grupos de objetos cujos wrappers não são mais referenciados.</span><span class="sxs-lookup"><span data-stu-id="79c94-221">However, this does not create an uncollectable cycle, as Garbage Collector \(GC\) is smart enough to release object groups whose wrappers are no longer referenced.</span></span> <span data-ttu-id="79c94-222">Mas esquecer de liberar um único wrapper mantém o grupo inteiro e os wrappers associados.</span><span class="sxs-lookup"><span data-stu-id="79c94-222">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

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
> <span data-ttu-id="79c94-231">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="79c94-231">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="79c94-232">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) e é criada por [Meggin Kearney][MegginKearney] \ (redator técnico \).</span><span class="sxs-lookup"><span data-stu-id="79c94-232">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="79c94-234">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="79c94-234">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
