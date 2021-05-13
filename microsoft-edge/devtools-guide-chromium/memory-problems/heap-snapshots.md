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
# <a name="how-to-record-heap-snapshots"></a><span data-ttu-id="055c1-104">Como registrar instantâneos de pilha</span><span class="sxs-lookup"><span data-stu-id="055c1-104">How to record heap snapshots</span></span>  

<span data-ttu-id="055c1-105">Saiba como gravar instantâneos de pilha com o profiler de pilha Microsoft Edge DevTools e encontrar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="055c1-105">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="055c1-106">O Microsoft Edge de pilha de DevTools mostra a distribuição de memória pelos objetos JavaScript e nós DOM relacionados da sua página.</span><span class="sxs-lookup"><span data-stu-id="055c1-106">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="055c1-107">Use-o para fazer instantâneos de pilha de JavaScript \(JS heap\) , analisar gráficos de memória, comparar instantâneos e encontrar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="055c1-107">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="055c1-108">Navegue [até a árvore de retenção de objetos][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="055c1-108">Navigate to [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <a name="take-a-snapshot"></a><span data-ttu-id="055c1-109">Tirar um instantâneo</span><span class="sxs-lookup"><span data-stu-id="055c1-109">Take a snapshot</span></span>  

<span data-ttu-id="055c1-110">No painel **Memória,** escolha **Tirar instantâneo**e, em seguida, escolha **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="055c1-110">On the **Memory** panel, choose **Take snapshot**, then choose **Start**.</span></span>  <span data-ttu-id="055c1-111">Você também pode selecionar `Ctrl` + `E` \(Windows, Linux\) `Cmd` + `E` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="055c1-111">You may also select `Ctrl`+`E` \(Windows, Linux\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Escolher tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="055c1-113">Escolher tipo de perfil</span><span class="sxs-lookup"><span data-stu-id="055c1-113">Choose profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="055c1-114">**Os instantâneos** são armazenados inicialmente na memória do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="055c1-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="055c1-115">Instantâneos são transferidos para o DevTools sob demanda, quando você escolhe no ícone de instantâneo para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="055c1-115">Snapshots are transferred to the DevTools on demand, when you choose on the snapshot icon to view it.</span></span>  

<span data-ttu-id="055c1-116">Depois que o instantâneo for carregado no DevTools e tiver sido analisado, o número abaixo do título do instantâneo será exibido e mostrará o tamanho total dos objetos [JavaScript acessíveis.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="055c1-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Tamanho total de objetos acessíveis" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="055c1-118">Tamanho total de objetos acessíveis</span><span class="sxs-lookup"><span data-stu-id="055c1-118">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="055c1-119">Somente objetos acessíveis são incluídos em instantâneos.</span><span class="sxs-lookup"><span data-stu-id="055c1-119">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="055c1-120">Além disso, tirar um instantâneo sempre começa com uma coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="055c1-120">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <a name="clear-snapshots"></a><span data-ttu-id="055c1-121">Limpar instantâneos</span><span class="sxs-lookup"><span data-stu-id="055c1-121">Clear snapshots</span></span>  

<span data-ttu-id="055c1-122">Escolha **Limpar todos os perfis** ícone para remover instantâneos \(tanto do DevTools quanto de qualquer memória associada ao processo de renderização\).</span><span class="sxs-lookup"><span data-stu-id="055c1-122">Choose **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Remover instantâneos" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="055c1-124">Remover instantâneos</span><span class="sxs-lookup"><span data-stu-id="055c1-124">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="055c1-125">Fechar a janela DevTools não exclui perfis da memória associada ao processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="055c1-125">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="055c1-126">Ao reabrir o DevTools, todos os instantâneos tirados anteriormente reaparecem na lista de instantâneos.</span><span class="sxs-lookup"><span data-stu-id="055c1-126">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="055c1-127">Experimente este exemplo de objetos [espalhados e][GlitchDevtoolsMemoryExample03] perfile-o usando o Heap Profiler.</span><span class="sxs-lookup"><span data-stu-id="055c1-127">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="055c1-128">Várias alocações de itens \(object\) são exibidas.</span><span class="sxs-lookup"><span data-stu-id="055c1-128">A number of \(object\) item allocations are displayed.</span></span>  

## <a name="view-snapshots"></a><span data-ttu-id="055c1-129">Exibir instantâneos</span><span class="sxs-lookup"><span data-stu-id="055c1-129">View snapshots</span></span>  

<span data-ttu-id="055c1-130">Exibir instantâneos de diferentes perspectivas para tarefas diferentes.</span><span class="sxs-lookup"><span data-stu-id="055c1-130">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="055c1-131">**O resumo** mostra objetos agrupados pelo nome do construtor.</span><span class="sxs-lookup"><span data-stu-id="055c1-131">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="055c1-132">Use-o para procurar objetos \(e o uso de memória\) com base no tipo agrupado pelo nome do construtor.</span><span class="sxs-lookup"><span data-stu-id="055c1-132">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="055c1-133">É particularmente útil para rastrear **vazamentos de DOM.**</span><span class="sxs-lookup"><span data-stu-id="055c1-133">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="055c1-134">**Exibição de comparação**.</span><span class="sxs-lookup"><span data-stu-id="055c1-134">**Comparison view**.</span></span>  <span data-ttu-id="055c1-135">Exibe a diferença entre dois instantâneos.</span><span class="sxs-lookup"><span data-stu-id="055c1-135">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="055c1-136">Use-o para comparar dois instantâneos de memória \(ou mais\) de antes e depois de uma operação.</span><span class="sxs-lookup"><span data-stu-id="055c1-136">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="055c1-137">Inspecionar o delta na memória liberada e na contagem de referência permite confirmar a presença e a causa de um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="055c1-137">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="055c1-138">**Exibição de contenção**.</span><span class="sxs-lookup"><span data-stu-id="055c1-138">**Containment view**.</span></span>  <span data-ttu-id="055c1-139">Permite a exploração de conteúdo de pilha.</span><span class="sxs-lookup"><span data-stu-id="055c1-139">Allows exploration of heap contents.</span></span>  <span data-ttu-id="055c1-140">**O exibição de** contenção fornece uma melhor visão da estrutura de objetos, ajudando a analisar objetos referenciados no namespace global \(window\) para descobrir o que está mantendo objetos ao redor.</span><span class="sxs-lookup"><span data-stu-id="055c1-140">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="055c1-141">Use-o para analisar fechamentos e mergulhar em seus objetos em um nível baixo.</span><span class="sxs-lookup"><span data-stu-id="055c1-141">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="055c1-142">Para alternar entre exibições, use o seletor na parte superior do exibição.</span><span class="sxs-lookup"><span data-stu-id="055c1-142">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Seletor de exibições de opção" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="055c1-144">Seletor de exibições de opção</span><span class="sxs-lookup"><span data-stu-id="055c1-144">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="055c1-145">Nem todas as propriedades são armazenadas na pilha JavaScript.</span><span class="sxs-lookup"><span data-stu-id="055c1-145">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="055c1-146">As propriedades implementadas usando getters que executem código nativo não são capturadas.</span><span class="sxs-lookup"><span data-stu-id="055c1-146">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="055c1-147">Além disso, valores não-cadeias de caracteres, como números, não são capturados.</span><span class="sxs-lookup"><span data-stu-id="055c1-147">Also, non-string values such as numbers are not captured.</span></span>  

### <a name="summary-view"></a><span data-ttu-id="055c1-148">Exibição de resumo</span><span class="sxs-lookup"><span data-stu-id="055c1-148">Summary view</span></span>  

<span data-ttu-id="055c1-149">Inicialmente, um instantâneo é aberto no exibição Resumo, exibindo totais de objeto, que podem ser expandidos para mostrar instâncias:</span><span class="sxs-lookup"><span data-stu-id="055c1-149">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Exibição de resumo" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="055c1-151">**Exibição de** resumo</span><span class="sxs-lookup"><span data-stu-id="055c1-151">**Summary** view</span></span>  
:::image-end:::  

<span data-ttu-id="055c1-152">As entradas de nível superior são linhas "totais".</span><span class="sxs-lookup"><span data-stu-id="055c1-152">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="055c1-153">Entradas de nível superior</span><span class="sxs-lookup"><span data-stu-id="055c1-153">Top-level entries</span></span> | <span data-ttu-id="055c1-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="055c1-154">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="055c1-155">Construtor</span><span class="sxs-lookup"><span data-stu-id="055c1-155">Constructor</span></span>** | <span data-ttu-id="055c1-156">Representa todos os objetos criados usando esse construtor.</span><span class="sxs-lookup"><span data-stu-id="055c1-156">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="055c1-157">Distância</span><span class="sxs-lookup"><span data-stu-id="055c1-157">Distance</span></span>** | <span data-ttu-id="055c1-158">exibe a distância até a raiz usando o caminho mais curto e simples dos nós.</span><span class="sxs-lookup"><span data-stu-id="055c1-158">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="055c1-159">Tamanho superficial</span><span class="sxs-lookup"><span data-stu-id="055c1-159">Shallow size</span></span>** | <span data-ttu-id="055c1-160">Exibe a soma de tamanhos rasos de todos os objetos criados por uma determinada função de construtor.</span><span class="sxs-lookup"><span data-stu-id="055c1-160">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="055c1-161">O tamanho superficial é o tamanho da memória mantida por um objeto \(geralmente, matrizes e cadeias de caracteres têm tamanhos rasos maiores\).</span><span class="sxs-lookup"><span data-stu-id="055c1-161">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="055c1-162">Navegue até [Tamanhos de objeto][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="055c1-162">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="055c1-163">Tamanho retido</span><span class="sxs-lookup"><span data-stu-id="055c1-163">Retained size</span></span>** | <span data-ttu-id="055c1-164">Exibe o tamanho máximo retido entre o mesmo conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="055c1-164">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="055c1-165">O tamanho da memória que você pode liberar depois que um objeto é excluído \(e os dependentes não são mais acessíveis\) é chamado de tamanho retido.</span><span class="sxs-lookup"><span data-stu-id="055c1-165">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="055c1-166">Navegue até [Tamanhos de objeto][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="055c1-166">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="055c1-167">Depois de expandir uma linha total na exibição superior, todas as instâncias serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="055c1-167">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="055c1-168">Para cada instância, os tamanhos superficial e retido são exibidos nas colunas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="055c1-168">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="055c1-169">O número após o caractere é a ID exclusiva do objeto, permitindo comparar instantâneos de pilha `@` por objeto.</span><span class="sxs-lookup"><span data-stu-id="055c1-169">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="055c1-170">Lembre-se de que objetos amarelos têm referências JavaScript e objetos vermelhos são nós desvinculados que são referenciados de um com um plano de fundo amarelo.</span><span class="sxs-lookup"><span data-stu-id="055c1-170">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="055c1-171">O que as várias entradas do construtor \(group\) no profiler heap correspondem?</span><span class="sxs-lookup"><span data-stu-id="055c1-171">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Grupos de construtores" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="055c1-173">**Grupos de construtores**</span><span class="sxs-lookup"><span data-stu-id="055c1-173">**Constructor** groups</span></span>  
:::image-end:::  

| <span data-ttu-id="055c1-174">Entrada do construtor \(group\)</span><span class="sxs-lookup"><span data-stu-id="055c1-174">Constructor \(group\) entry</span></span> | <span data-ttu-id="055c1-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="055c1-175">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="055c1-176">\(propriedade global\)</span><span class="sxs-lookup"><span data-stu-id="055c1-176">\(global property\)</span></span>** | <span data-ttu-id="055c1-177">Os objetos intermediários entre um objeto global \(like `window` \) e um objeto referenciado por ele.</span><span class="sxs-lookup"><span data-stu-id="055c1-177">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="055c1-178">Se um objeto for criado usando um construtor e for mantido por um objeto global, o caminho de retenção poderá ser `Person` representado como `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="055c1-178">If an object is created using a constructor `Person` and is held by a global object, the retaining path may be represented as `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="055c1-179">Isso contrasta com a norma, onde os objetos se referenciam diretamente uns aos outros.</span><span class="sxs-lookup"><span data-stu-id="055c1-179">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="055c1-180">Objetos intermediários existem por motivos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="055c1-180">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="055c1-181">Os globais são modificados regularmente e as otimizações de acesso a propriedades fazem um bom trabalho para objetos não globais não são aplicáveis para globais.</span><span class="sxs-lookup"><span data-stu-id="055c1-181">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="055c1-182">\(roots\)</span><span class="sxs-lookup"><span data-stu-id="055c1-182">\(roots\)</span></span>** | <span data-ttu-id="055c1-183">As entradas raiz na exibição de árvore de retenção são as entidades que têm referências ao objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="055c1-183">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="055c1-184">As entradas também podem ser referências criadas pelo mecanismo para fins específicos do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="055c1-184">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="055c1-185">O mecanismo tem caches que objetos de referência, mas todas essas referências são fracas e não impedem que um objeto seja coletado, já que não há referências realmente fortes.</span><span class="sxs-lookup"><span data-stu-id="055c1-185">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="055c1-186">\(closure\)</span><span class="sxs-lookup"><span data-stu-id="055c1-186">\(closure\)</span></span>** | <span data-ttu-id="055c1-187">Uma contagem de referências a um grupo de objetos por meio de fechamentos de função.</span><span class="sxs-lookup"><span data-stu-id="055c1-187">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="055c1-188">\(matriz, cadeia de caracteres, número, regexp\)</span><span class="sxs-lookup"><span data-stu-id="055c1-188">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="055c1-189">Uma lista de tipos de objeto com propriedades que referenciam uma matriz, cadeia de caracteres, número ou expressão regular.</span><span class="sxs-lookup"><span data-stu-id="055c1-189">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="055c1-190">\(código compilado\)</span><span class="sxs-lookup"><span data-stu-id="055c1-190">\(compiled code\)</span></span>** | <span data-ttu-id="055c1-191">Tudo relacionado ao código compilado.</span><span class="sxs-lookup"><span data-stu-id="055c1-191">Everything related to compiled code.</span></span>  <span data-ttu-id="055c1-192">O script é semelhante a uma função, mas corresponde a um `<script>` corpo.</span><span class="sxs-lookup"><span data-stu-id="055c1-192">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="055c1-193">SharedFunctionInfos \(SFI\) são objetos entre funções e código compilado.</span><span class="sxs-lookup"><span data-stu-id="055c1-193">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="055c1-194">As funções geralmente têm um contexto, enquanto os SFIs não.</span><span class="sxs-lookup"><span data-stu-id="055c1-194">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="055c1-195">**HTMLDivElement,** **HTMLAnchorElement,** **DocumentFragment**e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="055c1-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="055c1-196">Referências a elementos ou objetos de documento de um tipo específico referenciado pelo código.</span><span class="sxs-lookup"><span data-stu-id="055c1-196">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a><span data-ttu-id="055c1-197">Exibição de comparação</span><span class="sxs-lookup"><span data-stu-id="055c1-197">Comparison view</span></span>  

<span data-ttu-id="055c1-198">Encontre objetos vazados comparando vários instantâneos uns com os outros.</span><span class="sxs-lookup"><span data-stu-id="055c1-198">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="055c1-199">Para verificar se uma determinada operação de aplicativo não cria vazamentos \(por exemplo, geralmente um par de operações diretas e inversas, como abrir um documento e, em seguida, fecha-lo, não deve deixar lixo\), você pode seguir o cenário abaixo:</span><span class="sxs-lookup"><span data-stu-id="055c1-199">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="055c1-200">Tire um instantâneo de pilha antes de executar uma operação.</span><span class="sxs-lookup"><span data-stu-id="055c1-200">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="055c1-201">Execute uma operação \(interaja com uma página de alguma forma que você acredita estar causando um vazamento\).</span><span class="sxs-lookup"><span data-stu-id="055c1-201">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="055c1-202">Execute uma operação inversa \(faça a interação oposta e repita-a algumas vezes\).</span><span class="sxs-lookup"><span data-stu-id="055c1-202">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="055c1-203">Pegue um segundo instantâneo de pilha e altere a exibição deste para **Comparison**, comparando-o com **Instantâneo 1**.</span><span class="sxs-lookup"><span data-stu-id="055c1-203">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="055c1-204">No **visualização Comparação,** a diferença entre dois instantâneos é exibida.</span><span class="sxs-lookup"><span data-stu-id="055c1-204">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="055c1-205">Ao expandir uma entrada total, as instâncias de objeto adicionadas e excluídas são mostradas.</span><span class="sxs-lookup"><span data-stu-id="055c1-205">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Exibição de comparação" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="055c1-207">**Exibição de** comparação</span><span class="sxs-lookup"><span data-stu-id="055c1-207">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a><span data-ttu-id="055c1-208">Exibição de contenção</span><span class="sxs-lookup"><span data-stu-id="055c1-208">Containment view</span></span>  

<span data-ttu-id="055c1-209">O **ponto de vista** de contenção é essencialmente um "ponto de vista do pássaro" da estrutura de objetos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="055c1-209">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="055c1-210">Ele permite espiar os fechamentos de função, observar objetos internos \(VM\) da máquina virtual que juntos compõe seus objetos JavaScript e entender quanta memória seu aplicativo usa em um nível muito baixo.</span><span class="sxs-lookup"><span data-stu-id="055c1-210">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="055c1-211">Pontos de entrada do visualização de contenção</span><span class="sxs-lookup"><span data-stu-id="055c1-211">Containment view entry points</span></span> | <span data-ttu-id="055c1-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="055c1-212">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="055c1-213">Objetos DOMWindow</span><span class="sxs-lookup"><span data-stu-id="055c1-213">DOMWindow objects</span></span>** | <span data-ttu-id="055c1-214">Objetos globais para código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="055c1-214">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="055c1-215">Raízes de GC</span><span class="sxs-lookup"><span data-stu-id="055c1-215">GC roots</span></span>** | <span data-ttu-id="055c1-216">As raízes de GC reais usadas pelo lixo da VM.</span><span class="sxs-lookup"><span data-stu-id="055c1-216">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="055c1-217">As raízes de GC são compostas por mapas de objetos integrados, tabelas de símbolos, pilhas de threadS VM, caches de compilação, escopos de alças globais e escopos de compilação.</span><span class="sxs-lookup"><span data-stu-id="055c1-217">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="055c1-218">Objetos nativos</span><span class="sxs-lookup"><span data-stu-id="055c1-218">Native objects</span></span>** | <span data-ttu-id="055c1-219">Objetos de navegador "pressionados" dentro da máquina virtual JavaScript \(JavaScript VM\) para permitir a automação, por exemplo, nós dom, regras CSS.</span><span class="sxs-lookup"><span data-stu-id="055c1-219">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Exibição de contenção" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="055c1-221">**Exibição de** contenção</span><span class="sxs-lookup"><span data-stu-id="055c1-221">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="055c1-222">Uma dica sobre fechamentos.</span><span class="sxs-lookup"><span data-stu-id="055c1-222">A tip about closures.</span></span>  <span data-ttu-id="055c1-223">Nomeia as funções para que você possa distinguir facilmente entre fechamentos no instantâneo.</span><span class="sxs-lookup"><span data-stu-id="055c1-223">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="055c1-224">Por exemplo, este exemplo não usa funções nomeadas.</span><span class="sxs-lookup"><span data-stu-id="055c1-224">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="055c1-225">O trecho de código a seguir usa funções nomeadas.</span><span class="sxs-lookup"><span data-stu-id="055c1-225">The followingcode snippet uses named functions.</span></span>  
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
> > <span data-ttu-id="055c1-226">Experimente este exemplo de [por que `eval` é ruim][GlitchDevtoolsMemoryExample07] analisar o impacto de fechamentos na memória.</span><span class="sxs-lookup"><span data-stu-id="055c1-226">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="055c1-227">Você também pode estar interessado em segui-lo com este exemplo que o leva através da gravação de [alocações de heap][GlitchDevtoolsMemoryExample08].</span><span class="sxs-lookup"><span data-stu-id="055c1-227">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <a name="look-up-color-coding"></a><span data-ttu-id="055c1-228">Procurar codificação de cores</span><span class="sxs-lookup"><span data-stu-id="055c1-228">Look up color coding</span></span>  

<span data-ttu-id="055c1-229">Propriedades e valores de propriedade de objetos têm tipos diferentes e são coloridos de acordo.</span><span class="sxs-lookup"><span data-stu-id="055c1-229">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="055c1-230">Cada propriedade tem um dos quatro tipos.</span><span class="sxs-lookup"><span data-stu-id="055c1-230">Each property has one of four types.</span></span>  

| <span data-ttu-id="055c1-231">Tipo de propriedade</span><span class="sxs-lookup"><span data-stu-id="055c1-231">Property Type</span></span> | <span data-ttu-id="055c1-232">Descrição</span><span class="sxs-lookup"><span data-stu-id="055c1-232">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="055c1-233">a: propriedade</span><span class="sxs-lookup"><span data-stu-id="055c1-233">a: property</span></span>** | <span data-ttu-id="055c1-234">Uma propriedade regular com um nome, acessada por meio do `.` operador \(dot\) ou por meio de `[` `]` notação \(colchetes\) por exemplo `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="055c1-234">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="055c1-235">0: elemento</span><span class="sxs-lookup"><span data-stu-id="055c1-235">0: element</span></span>** | <span data-ttu-id="055c1-236">Uma propriedade regular com um índice numérico, acessada `[` `]` por meio de notação \(brackets\).</span><span class="sxs-lookup"><span data-stu-id="055c1-236">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="055c1-237">a: var de contexto</span><span class="sxs-lookup"><span data-stu-id="055c1-237">a: context var</span></span>** |  <span data-ttu-id="055c1-238">Uma variável em um contexto de função, acessível pelo nome da variável de dentro de um fechamento de função.</span><span class="sxs-lookup"><span data-stu-id="055c1-238">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="055c1-239">a: prop do sistema</span><span class="sxs-lookup"><span data-stu-id="055c1-239">a: system prop</span></span>** | <span data-ttu-id="055c1-240">Uma propriedade adicionada pela VM JavaScript, não acessível a partir do código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="055c1-240">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="055c1-241">Os objetos `System` designados como não têm um tipo JavaScript correspondente.</span><span class="sxs-lookup"><span data-stu-id="055c1-241">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="055c1-242">Cada um faz parte da implementação do sistema de objetos da VM Javascript.</span><span class="sxs-lookup"><span data-stu-id="055c1-242">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="055c1-243">O V8 aloca a maioria dos objetos internos na mesma pilha que os objetos JS do usuário.</span><span class="sxs-lookup"><span data-stu-id="055c1-243">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="055c1-244">Portanto, são apenas internos V8.</span><span class="sxs-lookup"><span data-stu-id="055c1-244">So these are just V8 internals.</span></span>  

## <a name="find-a-specific-object"></a><span data-ttu-id="055c1-245">Encontrar um objeto específico</span><span class="sxs-lookup"><span data-stu-id="055c1-245">Find a specific object</span></span>  

<span data-ttu-id="055c1-246">Para encontrar um objeto na pilha coletada, você pode pesquisar usando `Ctrl` + `F` e dar a ID do objeto.</span><span class="sxs-lookup"><span data-stu-id="055c1-246">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <a name="uncover-dom-leaks"></a><span data-ttu-id="055c1-247">Descobrir vazamentos de DOM</span><span class="sxs-lookup"><span data-stu-id="055c1-247">Uncover DOM leaks</span></span>  

<span data-ttu-id="055c1-248">O profiler de pilha tem a capacidade de refletir dependências bidirecionais entre objetos nativos do navegador \(nós DOM, regras CSS\) e objetos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="055c1-248">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="055c1-249">Isso ajuda a descobrir, caso contrário, vazamentos invisíveis que ocorrem devido a subárvores DOM desvinculadas esquecidas flutuando.</span><span class="sxs-lookup"><span data-stu-id="055c1-249">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="055c1-250">Vazamentos de DOM podem ser maiores do que você pensa.</span><span class="sxs-lookup"><span data-stu-id="055c1-250">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="055c1-251">Considere o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="055c1-251">Consider the following sample.</span></span>  <span data-ttu-id="055c1-252">Quando é o #tree GC?</span><span class="sxs-lookup"><span data-stu-id="055c1-252">When is the #tree GC?</span></span>  

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

<span data-ttu-id="055c1-253">O mantém uma referência ao pai `#leaf` relevante \(parentNode\) e recursivamente até , portanto, somente quando leafRef é anulado é a árvore WHOLE sob um candidato `#tree` para `#tree` GC.</span><span class="sxs-lookup"><span data-stu-id="055c1-253">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Subárvores DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="055c1-255">Subárvores DOM</span><span class="sxs-lookup"><span data-stu-id="055c1-255">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="055c1-256">Exemplos: experimente este exemplo de [um nó DOM][GlitchDevtoolsMemoryExample06] que vaza para entender onde ele pode vazar e como detectá-lo.</span><span class="sxs-lookup"><span data-stu-id="055c1-256">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="055c1-257">Você também pode ver este exemplo de [vazamentos de DOM maiores do que o esperado][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="055c1-257">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="055c1-258">Para ler mais sobre vazamentos de DOM e análises de memória fundamentais checkout Localizar e depurar vazamentos de memória com o [Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] por Gonzalo Gonçalves de Vila.</span><span class="sxs-lookup"><span data-stu-id="055c1-258">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="055c1-259">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="055c1-259">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="055c1-269">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="055c1-269">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="055c1-270">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) e é de autoria de [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="055c1-270">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="055c1-272">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="055c1-272">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
