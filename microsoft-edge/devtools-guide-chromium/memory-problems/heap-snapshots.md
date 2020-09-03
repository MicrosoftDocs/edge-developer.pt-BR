---
description: Saiba como registrar instantâneos de heap com o Microsoft Edge DevTools heap Profiler e localizar vazamentos de memória.
title: Como gravar instantâneos de pilha
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 15692b0258de6db66c0b58a2659348a6e849aaca
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993468"
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

# <span data-ttu-id="69c43-104">Como gravar instantâneos de pilha</span><span class="sxs-lookup"><span data-stu-id="69c43-104">How to record heap snapshots</span></span>  

<span data-ttu-id="69c43-105">Saiba como registrar instantâneos de heap com o Microsoft Edge DevTools heap Profiler e localizar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="69c43-105">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="69c43-106">O gerador de perfil de heap do Microsoft Edge DevTools mostra a distribuição de memória pelos objetos JavaScript e nós DOM relacionados da página.</span><span class="sxs-lookup"><span data-stu-id="69c43-106">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="69c43-107">Use-o para fazer instantâneos JavaScript heap \ (JS heap \), analisar gráficos de memória, comparar instantâneos e localizar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="69c43-107">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="69c43-108">Consulte também [árvore de retenção de objetos][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="69c43-108">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="69c43-109">Fazer um instantâneo</span><span class="sxs-lookup"><span data-stu-id="69c43-109">Take a snapshot</span></span>  

<span data-ttu-id="69c43-110">No painel **memória** , escolha **tirar instantâneo**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="69c43-110">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="69c43-111">Você também pode pressionar `Ctrl` + `E` \ (Windows \) ou `Cmd` + `E` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="69c43-111">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Selecionar o tipo de perfil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="69c43-113">Selecionar o tipo de perfil</span><span class="sxs-lookup"><span data-stu-id="69c43-113">Select profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="69c43-114">Os **instantâneos** são inicialmente armazenados na memória do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="69c43-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="69c43-115">Os instantâneos são transferidos para o DevTools sob demanda, quando você clica no ícone de instantâneo para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="69c43-115">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="69c43-116">Após o instantâneo ser carregado no DevTools e ter sido analisado, o número abaixo do título do instantâneo será exibido e mostrará o [Tamanho total dos objetos JavaScript acessíveis][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="69c43-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Tamanho total dos objetos acessíveis" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="69c43-118">Tamanho total dos objetos acessíveis</span><span class="sxs-lookup"><span data-stu-id="69c43-118">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="69c43-119">Somente objetos alcançáveis são incluídos em instantâneos.</span><span class="sxs-lookup"><span data-stu-id="69c43-119">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="69c43-120">Além disso, fazer um instantâneo sempre começa com uma coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="69c43-120">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="69c43-121">Limpar instantâneos</span><span class="sxs-lookup"><span data-stu-id="69c43-121">Clear snapshots</span></span>  

<span data-ttu-id="69c43-122">Clique no ícone **limpar todos os perfis** para remover instantâneos \ (ambos do devtools e qualquer memória associada ao processo de renderizador \).</span><span class="sxs-lookup"><span data-stu-id="69c43-122">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Remover instantâneos" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="69c43-124">Remover instantâneos</span><span class="sxs-lookup"><span data-stu-id="69c43-124">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="69c43-125">Fechar a janela DevTools não exclui os perfis da memória associada ao processo de renderizador.</span><span class="sxs-lookup"><span data-stu-id="69c43-125">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="69c43-126">Ao reabrir o DevTools, todos os instantâneos feitos anteriormente reaparecem na lista de instantâneos.</span><span class="sxs-lookup"><span data-stu-id="69c43-126">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="69c43-127">Experimente este exemplo de [objetos dispersos][GlitchDevtoolsMemoryExample03] e perfilie-o usando o gerador de perfil de heap.</span><span class="sxs-lookup"><span data-stu-id="69c43-127">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="69c43-128">Você deve ver uma quantidade de atribuições de itens \ (objeto \).</span><span class="sxs-lookup"><span data-stu-id="69c43-128">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="69c43-129">Exibir instantâneos</span><span class="sxs-lookup"><span data-stu-id="69c43-129">View snapshots</span></span>  

<span data-ttu-id="69c43-130">Exiba instantâneos de diferentes perspectivas para tarefas diferentes.</span><span class="sxs-lookup"><span data-stu-id="69c43-130">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="69c43-131">O **modo de exibição de resumo** mostra objetos agrupados pelo nome do construtor.</span><span class="sxs-lookup"><span data-stu-id="69c43-131">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="69c43-132">Use-o para procurar objetos \ (e o uso de memória \) com base no tipo agrupado pelo nome do construtor.</span><span class="sxs-lookup"><span data-stu-id="69c43-132">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="69c43-133">Isso é particularmente útil para **acompanhar os vazamentos dom**.</span><span class="sxs-lookup"><span data-stu-id="69c43-133">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="69c43-134">**Exibição de comparação**.</span><span class="sxs-lookup"><span data-stu-id="69c43-134">**Comparison view**.</span></span>  <span data-ttu-id="69c43-135">Exibe a diferença entre dois instantâneos.</span><span class="sxs-lookup"><span data-stu-id="69c43-135">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="69c43-136">Use-o para comparar dois (ou mais \) instantâneos de memória de antes e depois de uma operação.</span><span class="sxs-lookup"><span data-stu-id="69c43-136">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="69c43-137">Inspecionar o Delta na memória liberada e contagem de referência permite que você confirme a presença e causa de perda de memória.</span><span class="sxs-lookup"><span data-stu-id="69c43-137">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="69c43-138">**Modo de exibição de confinamento**.</span><span class="sxs-lookup"><span data-stu-id="69c43-138">**Containment view**.</span></span>  <span data-ttu-id="69c43-139">Permite explorar o conteúdo da pilha.</span><span class="sxs-lookup"><span data-stu-id="69c43-139">Allows exploration of heap contents.</span></span>  <span data-ttu-id="69c43-140">O **modo de exibição de detenção** fornece uma visão melhor da estrutura de objetos, ajudando a analisar objetos referenciados no namespace global \ (janela \) para descobrir o que está mantendo objetos.</span><span class="sxs-lookup"><span data-stu-id="69c43-140">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="69c43-141">Use-o para analisar os fechamentos e mergulhe em seus objetos em um nível baixo.</span><span class="sxs-lookup"><span data-stu-id="69c43-141">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="69c43-142">Para alternar entre os modos de exibição, use o seletor na parte superior do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="69c43-142">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Alternar seletor de modos de exibição" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="69c43-144">Alternar seletor de modos de exibição</span><span class="sxs-lookup"><span data-stu-id="69c43-144">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="69c43-145">Nem todas as propriedades são armazenadas na pilha JavaScript.</span><span class="sxs-lookup"><span data-stu-id="69c43-145">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="69c43-146">As propriedades implementadas usando getters que executam o código nativo não são capturadas.</span><span class="sxs-lookup"><span data-stu-id="69c43-146">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="69c43-147">Além disso, valores não cadeia de caracteres, como números, não são capturados.</span><span class="sxs-lookup"><span data-stu-id="69c43-147">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="69c43-148">Modo de exibição Resumo</span><span class="sxs-lookup"><span data-stu-id="69c43-148">Summary view</span></span>  

<span data-ttu-id="69c43-149">Inicialmente, um instantâneo é aberto no modo de exibição de resumo, exibindo totais de objetos, que podem ser expandidos para mostrar instâncias:</span><span class="sxs-lookup"><span data-stu-id="69c43-149">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Modo de exibição Resumo" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="69c43-151">Modo de exibição **Resumo**</span><span class="sxs-lookup"><span data-stu-id="69c43-151">**Summary** view</span></span>  
:::image-end:::  

<span data-ttu-id="69c43-152">As entradas de nível superior são linhas de "total".</span><span class="sxs-lookup"><span data-stu-id="69c43-152">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="69c43-153">Entradas de nível superior</span><span class="sxs-lookup"><span data-stu-id="69c43-153">Top-level entries</span></span> | <span data-ttu-id="69c43-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="69c43-154">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="69c43-155">Construtor</span><span class="sxs-lookup"><span data-stu-id="69c43-155">Constructor</span></span>** | <span data-ttu-id="69c43-156">Representa todos os objetos criados usando esse construtor.</span><span class="sxs-lookup"><span data-stu-id="69c43-156">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="69c43-157">Distância</span><span class="sxs-lookup"><span data-stu-id="69c43-157">Distance</span></span>** | <span data-ttu-id="69c43-158">exibe a distância para a raiz usando o caminho simples mais curto dos nós.</span><span class="sxs-lookup"><span data-stu-id="69c43-158">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="69c43-159">Tamanho superficial</span><span class="sxs-lookup"><span data-stu-id="69c43-159">Shallow size</span></span>** | <span data-ttu-id="69c43-160">Exibe a soma dos tamanhos superficiais de todos os objetos criados por uma determinada função de construtor.</span><span class="sxs-lookup"><span data-stu-id="69c43-160">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="69c43-161">O tamanho superficial é o tamanho da memória mantida por um objeto \ (geralmente, matrizes e cadeias de caracteres têm tamanhos mais superficiaiss \).</span><span class="sxs-lookup"><span data-stu-id="69c43-161">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="69c43-162">Consulte também [tamanhos de objeto][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="69c43-162">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="69c43-163">Tamanho retido</span><span class="sxs-lookup"><span data-stu-id="69c43-163">Retained size</span></span>** | <span data-ttu-id="69c43-164">Exibe o tamanho máximo retido entre o mesmo conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="69c43-164">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="69c43-165">O tamanho da memória que você pode liberar após um objeto ser excluído \ (e os dependentes não são mais acessados \) é chamado de tamanho retido.</span><span class="sxs-lookup"><span data-stu-id="69c43-165">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="69c43-166">Consulte também [tamanhos de objeto][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="69c43-166">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="69c43-167">Após expandir uma linha de totais no modo de exibição superior, todas as instâncias são exibidas.</span><span class="sxs-lookup"><span data-stu-id="69c43-167">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="69c43-168">Para cada instância, os tamanhos superficial e retido são exibidos nas colunas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="69c43-168">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="69c43-169">O número após o `@` caractere é a ID exclusiva do objeto, permitindo que você compare instantâneos de heap na base por objeto.</span><span class="sxs-lookup"><span data-stu-id="69c43-169">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="69c43-170">Lembre-se de que os objetos amarelos têm referências JavaScript e os objetos vermelhos são nós desanexados que são referenciados de um com um plano de fundo amarelo.</span><span class="sxs-lookup"><span data-stu-id="69c43-170">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="69c43-171">Quais são as várias entradas do Construtor \ (Grupo \) no perfil de heap que correspondem a?</span><span class="sxs-lookup"><span data-stu-id="69c43-171">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Grupos de Construtor" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="69c43-173">Grupos de **Construtor**</span><span class="sxs-lookup"><span data-stu-id="69c43-173">**Constructor** groups</span></span>  
:::image-end:::  

| <span data-ttu-id="69c43-174">Entrada do Construtor \ (Grupo \)</span><span class="sxs-lookup"><span data-stu-id="69c43-174">Constructor \(group\) entry</span></span> | <span data-ttu-id="69c43-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="69c43-175">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="69c43-176">\ (Propriedade global \)</span><span class="sxs-lookup"><span data-stu-id="69c43-176">\(global property\)</span></span>** | <span data-ttu-id="69c43-177">Os objetos intermediários entre um objeto global \ (como `window` \) e um objeto referenciado por ele.</span><span class="sxs-lookup"><span data-stu-id="69c43-177">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="69c43-178">Se um objeto é criado usando um construtor `Person` e é mantido por um objeto global, o caminho de retenção ficaria como `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="69c43-178">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="69c43-179">Isso contrasta com a norma, onde os objetos fazem referência diretamente uns aos outros.</span><span class="sxs-lookup"><span data-stu-id="69c43-179">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="69c43-180">Existem objetos intermediários por motivos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="69c43-180">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="69c43-181">Os globais são modificados regularmente e as otimizações de acesso à propriedade fazem um bom trabalho para objetos não globais não se aplicam a globais.</span><span class="sxs-lookup"><span data-stu-id="69c43-181">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="69c43-182">\ (raízes \)</span><span class="sxs-lookup"><span data-stu-id="69c43-182">\(roots\)</span></span>** | <span data-ttu-id="69c43-183">As entradas raiz no modo de exibição de árvore de retenção são as entidades que têm referências ao objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="69c43-183">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="69c43-184">As entradas também podem ser referências criadas pelo mecanismo para fins específicos do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="69c43-184">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="69c43-185">O mecanismo tem caches que fazem referência a objetos, mas todas essas referências são fracas e não impedem que um objeto seja coletado, Considerando que não há nenhuma referência realmente forte.</span><span class="sxs-lookup"><span data-stu-id="69c43-185">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="69c43-186">\ (fechamento \)</span><span class="sxs-lookup"><span data-stu-id="69c43-186">\(closure\)</span></span>** | <span data-ttu-id="69c43-187">Uma contagem de referências a um grupo de objetos por meio de fechamentos de função.</span><span class="sxs-lookup"><span data-stu-id="69c43-187">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="69c43-188">\ (matriz, Cadeia de caracteres, número, RegExp \)</span><span class="sxs-lookup"><span data-stu-id="69c43-188">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="69c43-189">Uma lista de tipos de objeto com propriedades que fazem referência a uma matriz, Cadeia de caracteres, número ou expressão regular.</span><span class="sxs-lookup"><span data-stu-id="69c43-189">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="69c43-190">\ (código compilado \)</span><span class="sxs-lookup"><span data-stu-id="69c43-190">\(compiled code\)</span></span>** | <span data-ttu-id="69c43-191">Tudo relacionado ao código compilado.</span><span class="sxs-lookup"><span data-stu-id="69c43-191">Everything related to compiled code.</span></span>  <span data-ttu-id="69c43-192">O script é semelhante a uma função, mas corresponde a um `<script>` corpo.</span><span class="sxs-lookup"><span data-stu-id="69c43-192">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="69c43-193">SharedFunctionInfos \ (SFI \) são objetos posicionados entre funções e código compilado.</span><span class="sxs-lookup"><span data-stu-id="69c43-193">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="69c43-194">As funções geralmente têm um contexto, enquanto SFIs não.</span><span class="sxs-lookup"><span data-stu-id="69c43-194">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="69c43-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="69c43-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="69c43-196">Referências a elementos ou objetos de documento de um determinado tipo referenciados pelo seu código.</span><span class="sxs-lookup"><span data-stu-id="69c43-196">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="69c43-197">Modo de exibição comparação</span><span class="sxs-lookup"><span data-stu-id="69c43-197">Comparison view</span></span>  

<span data-ttu-id="69c43-198">Encontre objetos vazados comparando vários instantâneos.</span><span class="sxs-lookup"><span data-stu-id="69c43-198">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="69c43-199">Para verificar se uma operação específica do aplicativo não cria vazamentos \ (por exemplo, geralmente um par de operações diretas e inversas, como abrir um documento e, em seguida, fechá-lo, não deve deixar qualquer tipo de lixo \), você pode seguir o cenário abaixo:</span><span class="sxs-lookup"><span data-stu-id="69c43-199">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="69c43-200">Faça um instantâneo de heap antes de executar uma operação.</span><span class="sxs-lookup"><span data-stu-id="69c43-200">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="69c43-201">Executar uma operação \ (interaja com uma página de uma maneira que acredite em causar um vazamento \).</span><span class="sxs-lookup"><span data-stu-id="69c43-201">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="69c43-202">Executar uma operação invertida \ (faça a interação oposta e repita-a algumas vezes \).</span><span class="sxs-lookup"><span data-stu-id="69c43-202">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="69c43-203">Faça um segundo instantâneo de heap e altere o modo de exibição de um para **comparação**, comparando-o com o **instantâneo 1**.</span><span class="sxs-lookup"><span data-stu-id="69c43-203">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="69c43-204">Na exibição **comparação** , a diferença entre dois instantâneos é exibida.</span><span class="sxs-lookup"><span data-stu-id="69c43-204">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="69c43-205">Ao expandir uma entrada de total, instâncias de objetos adicionadas e excluídas são mostradas.</span><span class="sxs-lookup"><span data-stu-id="69c43-205">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Modo de exibição comparação" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="69c43-207">Modo de exibição **comparação**</span><span class="sxs-lookup"><span data-stu-id="69c43-207">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="69c43-208">Modo de exibição de contenção</span><span class="sxs-lookup"><span data-stu-id="69c43-208">Containment view</span></span>  

<span data-ttu-id="69c43-209">O modo de exibição de **detenção** é essencialmente um "modo de exibição de pássaro" da estrutura objetos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69c43-209">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="69c43-210">Ele permite que você retome os fechamentos de função dentro para observar os objetos internos da máquina virtual, que juntos compõem seus objetos JavaScript e para compreender a quantidade de memória que seu aplicativo usa em um nível muito baixo.</span><span class="sxs-lookup"><span data-stu-id="69c43-210">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="69c43-211">Pontos de entrada do modo de exibição de detenção</span><span class="sxs-lookup"><span data-stu-id="69c43-211">Containment view entry points</span></span> | <span data-ttu-id="69c43-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="69c43-212">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="69c43-213">Objetos DOMWindow</span><span class="sxs-lookup"><span data-stu-id="69c43-213">DOMWindow objects</span></span>** | <span data-ttu-id="69c43-214">Objetos globais para código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="69c43-214">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="69c43-215">Raízes GC</span><span class="sxs-lookup"><span data-stu-id="69c43-215">GC roots</span></span>** | <span data-ttu-id="69c43-216">As raízes GC reais usadas pelo lixo da VM.</span><span class="sxs-lookup"><span data-stu-id="69c43-216">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="69c43-217">As raízes de GC são compostas de mapas de objetos internos, tabelas de símbolos, pilhas de threads de VM, caches de compilação, escopos de manipulação e identificadores globais.</span><span class="sxs-lookup"><span data-stu-id="69c43-217">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="69c43-218">Objetos nativos</span><span class="sxs-lookup"><span data-stu-id="69c43-218">Native objects</span></span>** | <span data-ttu-id="69c43-219">Objetos do navegador "pressionados" dentro da máquina virtual JavaScript \ (JavaScript VM \) para permitir a automação, por exemplo, nós DOM, regras de CSS.</span><span class="sxs-lookup"><span data-stu-id="69c43-219">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Modo de exibição de contenção" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="69c43-221">Modo de exibição de **contenção**</span><span class="sxs-lookup"><span data-stu-id="69c43-221">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="69c43-222">Uma dica sobre os fechamentos.</span><span class="sxs-lookup"><span data-stu-id="69c43-222">A tip about closures.</span></span>  <span data-ttu-id="69c43-223">Nomeie as funções para que você possa distinguir facilmente os fechamentos do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="69c43-223">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="69c43-224">Por exemplo, este exemplo não usa funções nomeadas.</span><span class="sxs-lookup"><span data-stu-id="69c43-224">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="69c43-225">O snippet followingcode usa funções nomeadas.</span><span class="sxs-lookup"><span data-stu-id="69c43-225">The followingcode snippet uses named functions.</span></span>  
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
> > <span data-ttu-id="69c43-226">Experimente este exemplo de [por que `eval` é perigoso][GlitchDevtoolsMemoryExample07] analisar o impacto dos fechamentos na memória.</span><span class="sxs-lookup"><span data-stu-id="69c43-226">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="69c43-227">Você também pode estar interessado em fazê-lo com este exemplo que o orientará através da gravação de atribuições de [heap][GlitchDevtoolsMemoryExample08].</span><span class="sxs-lookup"><span data-stu-id="69c43-227">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="69c43-228">Pesquisar codificação de cores</span><span class="sxs-lookup"><span data-stu-id="69c43-228">Look up color coding</span></span>  

<span data-ttu-id="69c43-229">Propriedades e valores de propriedade de objetos têm tipos diferentes e são coloridos de acordo.</span><span class="sxs-lookup"><span data-stu-id="69c43-229">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="69c43-230">Cada propriedade tem um dos quatro tipos.</span><span class="sxs-lookup"><span data-stu-id="69c43-230">Each property has one of four types.</span></span>  

| <span data-ttu-id="69c43-231">Tipo de propriedade</span><span class="sxs-lookup"><span data-stu-id="69c43-231">Property Type</span></span> | <span data-ttu-id="69c43-232">Descrição</span><span class="sxs-lookup"><span data-stu-id="69c43-232">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="69c43-233">a: Propriedade</span><span class="sxs-lookup"><span data-stu-id="69c43-233">a: property</span></span>** | <span data-ttu-id="69c43-234">Uma propriedade regular com um nome, acessada por meio do `.` operador \ (ponto \) ou por meio da `[` `]` notação de \ (colchetes \), por exemplo `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="69c43-234">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="69c43-235">0: elemento</span><span class="sxs-lookup"><span data-stu-id="69c43-235">0: element</span></span>** | <span data-ttu-id="69c43-236">Uma propriedade regular com um índice numérico, acessada por meio de uma `[` `]` notação de \ (colchetes \).</span><span class="sxs-lookup"><span data-stu-id="69c43-236">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="69c43-237">a: var de contexto</span><span class="sxs-lookup"><span data-stu-id="69c43-237">a: context var</span></span>** |  <span data-ttu-id="69c43-238">Uma variável em um contexto de função, acessível pelo nome de variável dentro de um fechamento de função.</span><span class="sxs-lookup"><span data-stu-id="69c43-238">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="69c43-239">a: prop System prop</span><span class="sxs-lookup"><span data-stu-id="69c43-239">a: system prop</span></span>** | <span data-ttu-id="69c43-240">Uma propriedade adicionada pela VM JavaScript, não pode ser acessada a partir do código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="69c43-240">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="69c43-241">Objetos designados como `System` não têm um tipo de JavaScript correspondente.</span><span class="sxs-lookup"><span data-stu-id="69c43-241">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="69c43-242">Cada parte da implementação do sistema de objetos da VM JavaScript.</span><span class="sxs-lookup"><span data-stu-id="69c43-242">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="69c43-243">V8 aloca a maioria dos objetos internos na mesma heap dos objetos JS do usuário.</span><span class="sxs-lookup"><span data-stu-id="69c43-243">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="69c43-244">Portanto, são apenas V8 internos.</span><span class="sxs-lookup"><span data-stu-id="69c43-244">So these are just V8 internals.</span></span>  

## <span data-ttu-id="69c43-245">Localizar um objeto específico</span><span class="sxs-lookup"><span data-stu-id="69c43-245">Find a specific object</span></span>  

<span data-ttu-id="69c43-246">Para localizar um objeto na pilha coletada, você pode pesquisar usando `Ctrl` + `F` e dar a identificação do objeto.</span><span class="sxs-lookup"><span data-stu-id="69c43-246">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="69c43-247">Descobrir vazamentos do DOM</span><span class="sxs-lookup"><span data-stu-id="69c43-247">Uncover DOM leaks</span></span>  

<span data-ttu-id="69c43-248">O gerador de perfil de heap tem a capacidade de refletir dependências bidirecionais entre objetos nativos do navegador \ (nós DOM, regras CSS \) e objetos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="69c43-248">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="69c43-249">Isso ajuda a descobrir vazamentos de outra forma invisíveis devido às subárvores do DOM desanexadas esquecidas em torno.</span><span class="sxs-lookup"><span data-stu-id="69c43-249">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="69c43-250">Os vazamentos DOM podem ser maiores do que você imagina.</span><span class="sxs-lookup"><span data-stu-id="69c43-250">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="69c43-251">Considere o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="69c43-251">Consider the following sample.</span></span>  <span data-ttu-id="69c43-252">Quando o #tree GC?</span><span class="sxs-lookup"><span data-stu-id="69c43-252">When is the #tree GC?</span></span>  

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

<span data-ttu-id="69c43-253">O `#leaf` mantém uma referência para o pai (ParentNode \) relevante e, recursivamente `#tree` , apenas quando leafRef é nullified é a árvore inteira em `#tree` um candidato para GC.</span><span class="sxs-lookup"><span data-stu-id="69c43-253">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Subárvores DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="69c43-255">Subárvores DOM</span><span class="sxs-lookup"><span data-stu-id="69c43-255">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="69c43-256">Exemplos: Experimente este exemplo de um [nó de Dom vazando][GlitchDevtoolsMemoryExample06] para compreender onde ele pode vazar e como detectá-lo.</span><span class="sxs-lookup"><span data-stu-id="69c43-256">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="69c43-257">Você também pode examinar esse exemplo de [vazamentos de dom maior do que o esperado][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="69c43-257">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="69c43-258">Para ler mais sobre vazamentos de DOM e fundamentos de análise de memória, desfaça o check-out [da descoberta e Depurando vazamentos de memória com o Microsoft Edge devtools][GonzaloRuizdeVillaMemory] por Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="69c43-258">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <span data-ttu-id="69c43-259">Entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="69c43-259">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="69c43-269">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="69c43-269">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="69c43-270">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) e é criada por [Meggin Kearney][MegginKearney] \ (redator técnico \).</span><span class="sxs-lookup"><span data-stu-id="69c43-270">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="69c43-272">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="69c43-272">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
