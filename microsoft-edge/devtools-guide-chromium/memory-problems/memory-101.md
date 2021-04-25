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

# <a name="memory-terminology"></a><span data-ttu-id="854cb-104">Terminologia de memória</span><span class="sxs-lookup"><span data-stu-id="854cb-104">Memory terminology</span></span>  

<span data-ttu-id="854cb-105">Este artigo descreve termos comuns usados na análise de memória e é aplicável a várias ferramentas de criação de perfil de memória para idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="854cb-105">This article describes common terms used in memory analysis, and is applicable to various memory profiling tools for different languages.</span></span>  

<span data-ttu-id="854cb-106">Os termos e noções descritas aqui referem-se ao [painel Memória][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="854cb-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="854cb-107">Se você já trabalhou com o Java, o .NET ou outro profiler de memória, este artigo pode ser um atualizador.</span><span class="sxs-lookup"><span data-stu-id="854cb-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this article may be a refresher.</span></span>  

## <a name="object-sizes"></a><span data-ttu-id="854cb-108">Tamanhos de objetos</span><span class="sxs-lookup"><span data-stu-id="854cb-108">Object sizes</span></span>  

<span data-ttu-id="854cb-109">Pense na memória como um gráfico com tipos primitivos \(como números e cadeias de caracteres\) e objetos \(matrizes associativas\).</span><span class="sxs-lookup"><span data-stu-id="854cb-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="854cb-110">Ele pode ser exibido como um gráfico com muitos pontos interconectados, como a figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="854cb-110">It may display as a graph with many interconnected points such as following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Representação visual da memória" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="854cb-112">Representação visual da memória</span><span class="sxs-lookup"><span data-stu-id="854cb-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="854cb-113">Um objeto pode conter memória de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="854cb-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="854cb-114">Diretamente pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="854cb-114">Directly by the object.</span></span>  
*   <span data-ttu-id="854cb-115">Implicitamente segurando referências a outros objetos e, portanto, impedindo que esses objetos são descartados automaticamente por um coletor de lixo.</span><span class="sxs-lookup"><span data-stu-id="854cb-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector.</span></span>  

<span data-ttu-id="854cb-116">Ao trabalhar [][DevtoolsMemoryProblemsHeapSnapshots] com o painel Memória no DevTools \(uma ferramenta para investigar problemas de memória encontrados em **Memória**\), você pode ver algumas colunas de informações diferentes.</span><span class="sxs-lookup"><span data-stu-id="854cb-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="854cb-117">Dois que se destacam são **Tamanho Superficial** e **Tamanho Retido**, mas o que eles representam?</span><span class="sxs-lookup"><span data-stu-id="854cb-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tamanho superficial e retido" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="854cb-119">Tamanho superficial e retido</span><span class="sxs-lookup"><span data-stu-id="854cb-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <a name="shallow-size"></a><span data-ttu-id="854cb-120">Tamanho superficial</span><span class="sxs-lookup"><span data-stu-id="854cb-120">Shallow size</span></span>  

<span data-ttu-id="854cb-121">Esse é o tamanho da memória que é mantida pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="854cb-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="854cb-122">Objetos JavaScript típicos têm alguma memória reservada para sua descrição e para armazenar valores imediatos.</span><span class="sxs-lookup"><span data-stu-id="854cb-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="854cb-123">Normalmente, apenas matrizes e cadeias de caracteres são capazes de ter um tamanho superficial significativo.</span><span class="sxs-lookup"><span data-stu-id="854cb-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="854cb-124">No entanto, cadeias de caracteres e matrizes externas geralmente têm seu armazenamento principal na memória do renderador, expondo apenas um pequeno objeto wrapper na pilha JavaScript.</span><span class="sxs-lookup"><span data-stu-id="854cb-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="854cb-125">A memória do renderador é toda a memória do processo em que uma página inspecionada é renderizada: memória nativa + memória de pilha JS da página + memória de pilha JS de todos os funcionários dedicados iniciados pela página.</span><span class="sxs-lookup"><span data-stu-id="854cb-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="854cb-126">No entanto, mesmo um objeto pequeno é capaz de manter uma grande quantidade de memória indiretamente, impedindo que outros objetos são descartados pelo processo de coleta automática de lixo.</span><span class="sxs-lookup"><span data-stu-id="854cb-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <a name="retained-size"></a><span data-ttu-id="854cb-127">Tamanho retido</span><span class="sxs-lookup"><span data-stu-id="854cb-127">Retained size</span></span>  

<span data-ttu-id="854cb-128">Esse é o tamanho da memória que é liberada depois que o objeto é excluído juntamente com os objetos dependentes que foram inacessível a partir das raízes do Coletor de **Lixo.**</span><span class="sxs-lookup"><span data-stu-id="854cb-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots**.</span></span>  

<span data-ttu-id="854cb-129">**As raízes** do Coletor de Lixo são feitas de **alças criadas** \(local ou global\) ao fazer uma referência do código nativo para um objeto JavaScript fora do V8.</span><span class="sxs-lookup"><span data-stu-id="854cb-129">**Garbage Collector roots** are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="854cb-130">Todas essas alças podem ser encontradas em um instantâneo de pilha sob raízes **de GC**Manipular escopo e  >  \*\*\*\* raízes **de GC**  >  **Alças globais**.</span><span class="sxs-lookup"><span data-stu-id="854cb-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="854cb-131">Descrever as alças nesta documentação sem mergulhar em detalhes da implementação do navegador pode ser confuso.</span><span class="sxs-lookup"><span data-stu-id="854cb-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="854cb-132">As raízes do Coletor de Lixo e as alças não são algo com o que você precisa se preocupar.</span><span class="sxs-lookup"><span data-stu-id="854cb-132">Both Garbage Collector roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="854cb-133">Há muitas raízes internas do Coletor de Lixo, a maioria das quais não são interessantes para os usuários.</span><span class="sxs-lookup"><span data-stu-id="854cb-133">There are lots of internal Garbage Collector roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="854cb-134">Do ponto de vista de aplicativos, há os seguintes tipos de raízes.</span><span class="sxs-lookup"><span data-stu-id="854cb-134">From the applications standpoint, there are the following kinds of roots.</span></span>  

*   <span data-ttu-id="854cb-135">Objeto global da janela \(em cada iframe\).</span><span class="sxs-lookup"><span data-stu-id="854cb-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="854cb-136">Nos instantâneos de pilha, o campo indica o número de referências de propriedade no caminho de retenção mais `distance` curto da janela.</span><span class="sxs-lookup"><span data-stu-id="854cb-136">In the heap snapshots, the `distance` field indicates the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="854cb-137">A árvore DOM do documento, que consiste em todos os nós DOM nativos que podem ser alcançadas ao percorrer o documento.</span><span class="sxs-lookup"><span data-stu-id="854cb-137">The document DOM tree, consisting of all native DOM nodes that are reachable by traversing the document.</span></span>  <span data-ttu-id="854cb-138">Nem todos os nós têm invólucros JavaScript, mas se um nó tiver um wrapper, o nó está vivo enquanto o documento está vivo.</span><span class="sxs-lookup"><span data-stu-id="854cb-138">Not all of the nodes have JavaScript wrappers, but if a node has a wrapper, the node is alive while the document is alive.</span></span>  
*   <span data-ttu-id="854cb-139">Às vezes, os objetos são mantidos pelo contexto de depuração na ferramenta **Sources** e **no Console**, como após a avaliação do Console.</span><span class="sxs-lookup"><span data-stu-id="854cb-139">Sometimes objects are retained by the debug context in the **Sources** tool and the **Console**, such as after Console evaluation.</span></span>  <span data-ttu-id="854cb-140">Crie instantâneos de pilha com uma ferramenta **console** des limpa e nenhum ponto de interrupção ativo no depurador na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="854cb-140">Create heap snapshots with a cleared **Console** tool and no active breakpoints in the debugger in the **Sources** tool.</span></span>

>[!TIP]
> <span data-ttu-id="854cb-141">Antes de tirar um instantâneo de pilha na [ferramenta Memória,][DevtoolsMemoryProblemsHeapSnapshots] limpe a **ferramenta Console** e desative pontos de interrupção na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="854cb-141">Before taking a heap snapshot in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool, clear the **Console** tool and deactivate breakpoints in the **Sources** tool.</span></span>  <span data-ttu-id="854cb-142">Para limpar a **ferramenta Console,** execute o `clear()` método.</span><span class="sxs-lookup"><span data-stu-id="854cb-142">To clear the **Console** tool, run the `clear()` method.</span></span>  

<span data-ttu-id="854cb-143">O gráfico de memória começa com uma raiz, que pode ser o objeto do navegador ou o objeto `window` `Global` de um Node.js módulo.</span><span class="sxs-lookup"><span data-stu-id="854cb-143">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="854cb-144">Você não controla como o objeto raiz é coletado.</span><span class="sxs-lookup"><span data-stu-id="854cb-144">You do not control how the root object is garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Você não é capaz de controlar como o objeto raiz é coletado." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="854cb-146">Você não é capaz de controlar como o objeto raiz é coletado.</span><span class="sxs-lookup"><span data-stu-id="854cb-146">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="854cb-147">O que não puder ser obtido da raiz obtém o lixo coletado.</span><span class="sxs-lookup"><span data-stu-id="854cb-147">Whatever is not reachable from the root gets garbage collected.</span></span>  

> [!NOTE]
> <span data-ttu-id="854cb-148">As [colunas Tamanho Superficial](#shallow-size) e [Tamanho Retido](#retained-size) representam dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="854cb-148">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <a name="objects-retaining-tree"></a><span data-ttu-id="854cb-149">Árvore de retenção de objetos</span><span class="sxs-lookup"><span data-stu-id="854cb-149">Objects retaining tree</span></span>  

<span data-ttu-id="854cb-150">A pilha é uma rede de objetos interconectados.</span><span class="sxs-lookup"><span data-stu-id="854cb-150">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="854cb-151">No mundo matemático, essa estrutura é chamada de **gráfico ou** gráfico de memória.</span><span class="sxs-lookup"><span data-stu-id="854cb-151">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="854cb-152">Um gráfico é construído a partir de **nós conectados** por meio de **bordas**, ambos são determinados rótulos.</span><span class="sxs-lookup"><span data-stu-id="854cb-152">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="854cb-153">**Nós** \(ou **objetos**\) são rotulados \*\*\*\* usando o nome da função de construtor que foi usada para criar eles.</span><span class="sxs-lookup"><span data-stu-id="854cb-153">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="854cb-154">**Bordas** são rotuladas usando os nomes das **propriedades**.</span><span class="sxs-lookup"><span data-stu-id="854cb-154">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="854cb-155">Saiba [como registrar um perfil usando o Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="854cb-155">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="854cb-156">Na figura a seguir, algumas das coisas notáveis [][DevtoolsMemoryProblemsHeapSnapshots] na gravação de Instantâneo de Pilha na ferramenta Memória incluem distância: a distância da raiz coletor de lixo.</span><span class="sxs-lookup"><span data-stu-id="854cb-156">In the following figure, some of the notable things in the Heap Snapshot recording in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool include distance:  the distance from the Garbage Collector root.</span></span>  <span data-ttu-id="854cb-157">Se quase todos os objetos do mesmo tipo estão na mesma distância e alguns estão a uma distância maior, isso é algo que vale a pena investigar.</span><span class="sxs-lookup"><span data-stu-id="854cb-157">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distância da raiz" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="854cb-159">Distância da raiz</span><span class="sxs-lookup"><span data-stu-id="854cb-159">Distance from root</span></span>  
:::image-end:::  

## <a name="dominators"></a><span data-ttu-id="854cb-160">Dominadores</span><span class="sxs-lookup"><span data-stu-id="854cb-160">Dominators</span></span>  

<span data-ttu-id="854cb-161">Os objetos Dominator são compostos por uma estrutura de árvore porque cada objeto tem exatamente um dominador.</span><span class="sxs-lookup"><span data-stu-id="854cb-161">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="854cb-162">Um dominador de um objeto pode não ter referências diretas a um objeto que ele domina; ou seja, a árvore do dominador não é uma árvore de abrangção do gráfico.</span><span class="sxs-lookup"><span data-stu-id="854cb-162">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="854cb-163">Na figura a seguir, a instrução a seguir é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="854cb-163">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="854cb-164">Nó 1 domina o nó 2</span><span class="sxs-lookup"><span data-stu-id="854cb-164">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="854cb-165">O nó 2 domina os nós 3, 4 e 6</span><span class="sxs-lookup"><span data-stu-id="854cb-165">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="854cb-166">Nó 3 domina o nó 5</span><span class="sxs-lookup"><span data-stu-id="854cb-166">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="854cb-167">O nó 5 domina o nó 8</span><span class="sxs-lookup"><span data-stu-id="854cb-167">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="854cb-168">Nó 6 domina o nó 7</span><span class="sxs-lookup"><span data-stu-id="854cb-168">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Estrutura de árvore do Dominator" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="854cb-170">Estrutura de árvore do Dominator</span><span class="sxs-lookup"><span data-stu-id="854cb-170">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="854cb-171">Na figura a seguir, o nó é o dominador de , mas também existe em cada caminho simples de `#3` Coletor de Lixo para `#10` `#7` `#10` .</span><span class="sxs-lookup"><span data-stu-id="854cb-171">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector to `#10`.</span></span>  <span data-ttu-id="854cb-172">Portanto, um objeto B é um dominador de um objeto A se B existir em cada caminho simples da raiz para o objeto A.</span><span class="sxs-lookup"><span data-stu-id="854cb-172">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Ilustração do dominador animado" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="854cb-174">Ilustração do dominador animado</span><span class="sxs-lookup"><span data-stu-id="854cb-174">Animated dominator illustration</span></span>  
:::image-end:::  

## <a name="v8-specifics"></a><span data-ttu-id="854cb-175">Especificações da V8</span><span class="sxs-lookup"><span data-stu-id="854cb-175">V8 specifics</span></span>  

<span data-ttu-id="854cb-176">Ao perfilar memória, é útil entender por que os instantâneos de pilha têm uma certa aparência.</span><span class="sxs-lookup"><span data-stu-id="854cb-176">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="854cb-177">Esta seção descreve alguns tópicos relacionados à memória especificamente correspondentes à máquina **virtual JavaScript V8** \(V8 VM ou VM\).</span><span class="sxs-lookup"><span data-stu-id="854cb-177">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <a name="javascript-object-representation"></a><span data-ttu-id="854cb-178">Representação de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="854cb-178">JavaScript object representation</span></span>  

<span data-ttu-id="854cb-179">Há três tipos primitivos:</span><span class="sxs-lookup"><span data-stu-id="854cb-179">There are three primitive types:</span></span>  

*   <span data-ttu-id="854cb-180">Números \(por exemplo `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="854cb-180">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="854cb-181">Booleans \( `true` or `false` \)</span><span class="sxs-lookup"><span data-stu-id="854cb-181">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="854cb-182">Cadeias de caracteres \(por exemplo `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="854cb-182">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="854cb-183">Primitivos não são capazes de referenciar outros valores e são sempre folhas ou nós de término.</span><span class="sxs-lookup"><span data-stu-id="854cb-183">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="854cb-184">**Os** números podem ser armazenados como:</span><span class="sxs-lookup"><span data-stu-id="854cb-184">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="854cb-185">um valor inteiro imediato de 31 bits chamado **números inteiros** pequenos \(**SMI**s\) ou</span><span class="sxs-lookup"><span data-stu-id="854cb-185">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="854cb-186">objetos heap, chamados de **números de pilha**.</span><span class="sxs-lookup"><span data-stu-id="854cb-186">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="854cb-187">Os números de pilha são usados para armazenar valores que não se ajustam ao formulário SMI, como **duplos**, ou quando um valor precisa ser in a **box,** como a definição de propriedades nele.</span><span class="sxs-lookup"><span data-stu-id="854cb-187">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="854cb-188">**Cadeias de caracteres** podem ser armazenadas em:</span><span class="sxs-lookup"><span data-stu-id="854cb-188">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="854cb-189">a **pilha de VM**ou</span><span class="sxs-lookup"><span data-stu-id="854cb-189">the **VM heap**, or</span></span>
*   <span data-ttu-id="854cb-190">externamente na **memória do renderador**.</span><span class="sxs-lookup"><span data-stu-id="854cb-190">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="854cb-191">Um objeto **wrapper** é criado e usado para acessar o armazenamento externo em que, por exemplo, as fontes de script e outros conteúdos recebidos da Web são armazenados, em vez de copiados para a pilha de VM.</span><span class="sxs-lookup"><span data-stu-id="854cb-191">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="854cb-192">A memória para novos objetos JavaScript é alocada de uma pilha JavaScript dedicada \(ou **pilha de VM**\).</span><span class="sxs-lookup"><span data-stu-id="854cb-192">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="854cb-193">Esses objetos são gerenciados pelo coletor de lixo em V8 e, portanto, permanecem vivos desde que haja pelo menos uma referência forte a eles.</span><span class="sxs-lookup"><span data-stu-id="854cb-193">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="854cb-194">Qualquer coisa que não seja na pilha JavaScript é chamado de **objeto nativo**.</span><span class="sxs-lookup"><span data-stu-id="854cb-194">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="854cb-195">Os objetos nativos, em contraste com objetos heap, não são gerenciados pelo coletor de lixo V8 durante todo o tempo de vida e só podem ser acessados do JavaScript usando o objeto wrapper JavaScript.</span><span class="sxs-lookup"><span data-stu-id="854cb-195">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="854cb-196">**A cadeia de** caracteres cons é um objeto que consiste em pares de cadeias de caracteres armazenadas e ingressadas e é resultado de concatenação.</span><span class="sxs-lookup"><span data-stu-id="854cb-196">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="854cb-197">A junção do conteúdo da cadeia **de caracteres** de cons ocorre apenas conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="854cb-197">The joining of the **cons string** contents occurs only as needed.</span></span>  <span data-ttu-id="854cb-198">Por exemplo, quando uma subdistência de uma cadeia de caracteres ingressada precisa ser construída.</span><span class="sxs-lookup"><span data-stu-id="854cb-198">For example, when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="854cb-199">Por exemplo, se você concatenar `a` e , você obter uma cadeia de `b` `(a, b)` caracteres que representa o resultado da concatenação.</span><span class="sxs-lookup"><span data-stu-id="854cb-199">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="854cb-200">Se você tiver concatenado `d` posteriormente com esse resultado, você obterá outra **cadeia de caracteres contras:** `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="854cb-200">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="854cb-201">**Matriz** é um objeto com chaves numéricas.</span><span class="sxs-lookup"><span data-stu-id="854cb-201">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="854cb-202">**As matrizes** são amplamente usadas na V8 VM para armazenar grandes quantidades de dados.</span><span class="sxs-lookup"><span data-stu-id="854cb-202">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="854cb-203">Conjuntos de pares de valores-chave, como dicionários, são respaldados **por matrizes**.</span><span class="sxs-lookup"><span data-stu-id="854cb-203">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="854cb-204">Um objeto JavaScript típico é armazenado como apenas um dos dois tipos **de** matriz:</span><span class="sxs-lookup"><span data-stu-id="854cb-204">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="854cb-205">propriedades nomeadas e</span><span class="sxs-lookup"><span data-stu-id="854cb-205">named properties, and</span></span>  
*   <span data-ttu-id="854cb-206">elementos numéricos</span><span class="sxs-lookup"><span data-stu-id="854cb-206">numeric elements</span></span>  

<span data-ttu-id="854cb-207">Quando há um pequeno número de propriedades, as propriedades são armazenadas internamente no objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="854cb-207">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="854cb-208">**Map** é um objeto que descreve o tipo de objeto que é e o layout.</span><span class="sxs-lookup"><span data-stu-id="854cb-208">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="854cb-209">Por exemplo, mapas são usados para descrever hierarquias de objetos implícitos para [acesso rápido a propriedades][V8FastProperties].</span><span class="sxs-lookup"><span data-stu-id="854cb-209">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <a name="object-groups"></a><span data-ttu-id="854cb-210">Grupos de objetos</span><span class="sxs-lookup"><span data-stu-id="854cb-210">Object groups</span></span>  

<span data-ttu-id="854cb-211">Cada **grupo de objetos** nativos é feito de objetos que têm referências mútuas entre si.</span><span class="sxs-lookup"><span data-stu-id="854cb-211">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="854cb-212">Considere, por exemplo, uma subárvore DOM onde cada nó tem um link para o pai relativo e links para o próximo filho e o próximo irmão, portanto, formando um gráfico conectado.</span><span class="sxs-lookup"><span data-stu-id="854cb-212">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="854cb-213">Os objetos nativos não são representados na pilha JavaScript.</span><span class="sxs-lookup"><span data-stu-id="854cb-213">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="854cb-214">A falta de representação é o motivo pelo qual os objetos nativos têm tamanho zero.</span><span class="sxs-lookup"><span data-stu-id="854cb-214">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="854cb-215">Em vez disso, os objetos wrapper são criados.</span><span class="sxs-lookup"><span data-stu-id="854cb-215">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="854cb-216">Cada objeto wrapper contém uma referência ao objeto nativo correspondente, para redirecionar comandos para ele.</span><span class="sxs-lookup"><span data-stu-id="854cb-216">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="854cb-217">Por sua vez, um grupo de objetos contém objetos wrapper.</span><span class="sxs-lookup"><span data-stu-id="854cb-217">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="854cb-218">No entanto, isso não cria um ciclo inigualável, pois o Coletor de Lixo é inteligente o suficiente para liberar grupos de objetos cujos wrappers não são mais referenciados.</span><span class="sxs-lookup"><span data-stu-id="854cb-218">However, this does not create an uncollectable cycle, as Garbage Collector is smart enough to release object groups whose wrappers are no longer referenced.</span></span>  <span data-ttu-id="854cb-219">Mas esquecer de liberar um único wrapper contém todo o grupo e wrappers associados.</span><span class="sxs-lookup"><span data-stu-id="854cb-219">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="854cb-220">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="854cb-220">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Como registrar instantâneos de pilha | Microsoft Docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propriedades rápidas no V8 | V8"  

> [!NOTE]
> <span data-ttu-id="854cb-223">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="854cb-223">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="854cb-224">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) e é de autoria de [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="854cb-224">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="854cb-226">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="854cb-226">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
