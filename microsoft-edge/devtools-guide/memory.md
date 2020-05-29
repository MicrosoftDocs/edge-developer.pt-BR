---
description: Use o painel memória para
title: DevTools-memória
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, memória, heap, GC, coleta de lixo, tamanho retido, dominadores
ms.custom: seodec18
ms.openlocfilehash: 416ba144f7e22bd50f5d2a3437bc21d9d31a9035
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561409"
---
# <span data-ttu-id="b3b69-104">Memória</span><span class="sxs-lookup"><span data-stu-id="b3b69-104">Memory</span></span>

<span data-ttu-id="b3b69-105">Use o painel **memória** para medir o uso de recursos do sistema e comparar instantâneos de heap em diferentes Estados de execução de código.</span><span class="sxs-lookup"><span data-stu-id="b3b69-105">Use the **Memory** panel to measure your use of system resources and compare heap snapshots at different states of code execution.</span></span> <span data-ttu-id="b3b69-106">Com ele, você pode:</span><span class="sxs-lookup"><span data-stu-id="b3b69-106">With it, you can:</span></span>

- <span data-ttu-id="b3b69-107">[Representar o gráfico do consumo de memória de sua página em tempo real](#memory-usage-timeline) e tirar instantâneos da pilha</span><span class="sxs-lookup"><span data-stu-id="b3b69-107">[Graph the memory consumption of your page in real time](#memory-usage-timeline) and take snapshots of the heap</span></span>
- <span data-ttu-id="b3b69-108">[Identificar possíveis problemas de memória](#snapshot-summary) em seu código, como objetos retidos não associados ao dom</span><span class="sxs-lookup"><span data-stu-id="b3b69-108">[Identify potential memory issues](#snapshot-summary) in your code, such as retained objects not attached to the DOM</span></span>
- <span data-ttu-id="b3b69-109">[Revise os dados de uso de memória](#snapshot-details) por tipo de objeto, contagem de instâncias, tamanho e referências para ajudar a isolar problemas</span><span class="sxs-lookup"><span data-stu-id="b3b69-109">[Review memory usage data](#snapshot-details) by object type, instance count, size, and references to help isolate issues</span></span>
- <span data-ttu-id="b3b69-110">[Aplicar filtros de dados de instantâneo](#filters) para reduzir o ruído de informações não acionáveis</span><span class="sxs-lookup"><span data-stu-id="b3b69-110">[Apply snapshot data filters](#filters) to reduce the noise of non-actionable information</span></span>
- <span data-ttu-id="b3b69-111">[Identificar o custo de memória de um objeto específico](#object-references) e as referências que o mantêm ativo</span><span class="sxs-lookup"><span data-stu-id="b3b69-111">[Identify the memory cost of a specific object](#object-references) and the references keeping it alive</span></span>
- <span data-ttu-id="b3b69-112">[Diferenciar a pilha em fases diferentes da sua investigação](#snapshot-comparison) para acompanhar a origem de vazamentos de memória e outros problemas</span><span class="sxs-lookup"><span data-stu-id="b3b69-112">[Diff the heap at different phases of your investigation](#snapshot-comparison) to track down the source of memory leaks and other problems</span></span>

![O painel memória do Microsoft Edge DevTools](./media/memory.png)


## <span data-ttu-id="b3b69-114">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="b3b69-114">Toolbar</span></span>

1. <span data-ttu-id="b3b69-115">**Iniciar/parar sessão de criação de perfil (Ctrl + E)**: ativar o profiler permite que você controle o uso da memória e faça instantâneos do heap.</span><span class="sxs-lookup"><span data-stu-id="b3b69-115">**Start/Stop profiling session (Ctrl+E)**: Turning on the profiler enables you to track memory usage and take snapshots of the heap.</span></span>
2. <span data-ttu-id="b3b69-116">**Importar sessão de criação de perfil (Ctrl + O)**: carregar uma sessão de diagnóstico de memória devtools salva.</span><span class="sxs-lookup"><span data-stu-id="b3b69-116">**Import profiling session (Ctrl+O)**: Load a saved  DevTools memory diagnostic session.</span></span>
3. <span data-ttu-id="b3b69-117">**Exportar sessão de criação de perfil (Ctrl + S)**: Salve a sessão de diagnóstico atual em disco.</span><span class="sxs-lookup"><span data-stu-id="b3b69-117">**Export profiling session (Ctrl+S)**: Save the current diagnostic session to disk.</span></span>
4. <span data-ttu-id="b3b69-118">**Criar instantâneo de heap (Ctrl + Shift + T)**: Registre as atribuições de memória atuais para um determinado ponto de tempo.</span><span class="sxs-lookup"><span data-stu-id="b3b69-118">**Take heap snapshot (Ctrl+Shift+T)**: Record current memory allocations for a given point of time.</span></span>


## <span data-ttu-id="b3b69-119">Linha do tempo de uso da memória</span><span class="sxs-lookup"><span data-stu-id="b3b69-119">Memory usage timeline</span></span>

<span data-ttu-id="b3b69-120">Os problemas de memória podem ser um dos principais culpados dos problemas de desempenho, fazendo com que sua página fique cada vez mais inresponsiva e esgotada ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="b3b69-120">Memory problems can be a major culprit of performance issues, causing your page to become increasingly unresponsive and laggy over time.</span></span>

<span data-ttu-id="b3b69-121">A primeira etapa para analisar o uso da memória da sua página é [iniciar uma sessão de criação de perfil](#toolbar) para levar antes/depois dos instantâneos da pilha enquanto você reproduz as etapas que causam o excesso de memória ou um vazamento de memória suspeita.</span><span class="sxs-lookup"><span data-stu-id="b3b69-121">The first step to analyzing the memory usage of your page is to [start a profiling session](#toolbar) in order to take before/after snapshots of the heap as you repro the steps causing memory bloat or a suspected memory leak.</span></span>

<span data-ttu-id="b3b69-122">Ao iniciar o criador de perfil de memória, você verá um gráfico de memória do processo que permite observar o conjunto de trabalho particular geral (a quantidade de memória consumida pela página) ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="b3b69-122">When you start the memory profiler, you will see a process memory graph that allows you to observe the overall private working set (the amount of memory consumed by the page) over time.</span></span> <span data-ttu-id="b3b69-123">O gráfico memória mostra uma visualização dinâmica da memória do processo da guia, que inclui bytes privados, memória nativa e heap JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b3b69-123">The memory graph shows you a live view of the tab's process memory, which includes private bytes, native memory, and the JavaScript heap.</span></span> 

![Linha do tempo de uso da memória](./media/memory_timeline.png)

 <span data-ttu-id="b3b69-125">O gráfico fornece uma indicação da tendência da memória para a página que permite que você julgar quando é adequado [fazer um instantâneo de heap](#toolbar) para comparação posterior, por exemplo, quando você vê períodos de retenção de memória inesperada.</span><span class="sxs-lookup"><span data-stu-id="b3b69-125">The graph gives you an indication of the memory trend for the page which enables you to judge when it is appropriate to [take a heap snapshot](#toolbar) for later comparison, such as when you see periods of unexpected memory retention.</span></span>

### <span data-ttu-id="b3b69-126">Performance. Mark ()</span><span class="sxs-lookup"><span data-stu-id="b3b69-126">Performance.mark()</span></span>

<span data-ttu-id="b3b69-127">Você pode adicionar **marcas de usuário** personalizadas à linha do tempo para ajudar a identificar os principais eventos durante o curso da sessão de análise chamando o [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) método de dentro do seu código ou do [**console**](./console.md)do devtools.</span><span class="sxs-lookup"><span data-stu-id="b3b69-127">You can add custom **User marks** to the timeline to help identify  key events during the course of your analysis session by calling the [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) method from within your code or the  DevTools [**Console**](./console.md).</span></span>

### <span data-ttu-id="b3b69-128">Console. takeheapSnapshot ()</span><span class="sxs-lookup"><span data-stu-id="b3b69-128">Console.takeheapSnapshot()</span></span>

<span data-ttu-id="b3b69-129">Às vezes, você precisa fazer instantâneos em points-in-time muito específicos, como imediatamente antes de uma grande mutação do DOM.</span><span class="sxs-lookup"><span data-stu-id="b3b69-129">Sometimes you need to take snapshots at very specific points in time, such as immediately before a large mutation of the DOM.</span></span> <span data-ttu-id="b3b69-130">Nesses casos, você pode fazer instantâneos programaticamente com [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) .</span><span class="sxs-lookup"><span data-stu-id="b3b69-130">In these cases,you can take snapshots programmatically with [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots).</span></span>

## <span data-ttu-id="b3b69-131">Resumo do instantâneo</span><span class="sxs-lookup"><span data-stu-id="b3b69-131">Snapshot summary</span></span>

<span data-ttu-id="b3b69-132">[Fazer um instantâneo](#toolbar) gerará um bloco de resumo que indica o tamanho do heap de JavaScript no momento em que o instantâneo foi tirado, juntamente com o número de objetos alocados e uma captura de tela da página.</span><span class="sxs-lookup"><span data-stu-id="b3b69-132">[Taking a snapshot](#toolbar) will generate a summary tile that indicates the size of the JavaScript heap at the time the snapshot was taken, along with the number of objects allocated and a screenshot of the page.</span></span> <span data-ttu-id="b3b69-133">Você pode continuar a fazer instantâneos a qualquer momento ao executar o cenário do usuário que requer análise.</span><span class="sxs-lookup"><span data-stu-id="b3b69-133">You can continue to take snapshots at any time as you run through the user scenario requiring analysis.</span></span> <span data-ttu-id="b3b69-134">Os instantâneos geram blocos adicionais, cada um indica a diferença na memória JavaScript do instantâneo anterior.</span><span class="sxs-lookup"><span data-stu-id="b3b69-134">The snapshots generate additional tiles, each of which indicates the difference in JavaScript memory from the previous snapshot.</span></span>

![Instantâneo de heap](./media/memory_snapshot.png)

<span data-ttu-id="b3b69-136">Clicar nos valores do bloco de resumo mudará para o painel mostrando [detalhes dos dados do instantâneo](#snapshot-details).</span><span class="sxs-lookup"><span data-stu-id="b3b69-136">Clicking on the values in the summary tile will switch to the pane showing [details of the snapshot data](#snapshot-details).</span></span> <span data-ttu-id="b3b69-137">Possíveis [problemas de memória são indicados](#snapshot-details) com um ícone de informação azul ("i").</span><span class="sxs-lookup"><span data-stu-id="b3b69-137">Potential [memory issues are indicated](#snapshot-details) with a blue informational ("i") icon.</span></span>

## <span data-ttu-id="b3b69-138">Detalhes do instantâneo</span><span class="sxs-lookup"><span data-stu-id="b3b69-138">Snapshot details</span></span>

<span data-ttu-id="b3b69-139">Os dados no painel do *instantâneo* mostram os objetos criados pela sua página juntamente com qualquer memória alocada por estruturas JavaScript que você possa estar consumindo.</span><span class="sxs-lookup"><span data-stu-id="b3b69-139">The data in the *Snapshot* pane shows the objects created by your page along with any memory allocated by JavaScript frameworks you may be consuming.</span></span>

![Tabela de detalhes do instantâneo](./media/memory_details.png)

<span data-ttu-id="b3b69-141">As três guias representam diferentes modos de exibição dos dados:</span><span class="sxs-lookup"><span data-stu-id="b3b69-141">The three tabs represent different views of the data:</span></span>

#### <span data-ttu-id="b3b69-142">Tipos</span><span class="sxs-lookup"><span data-stu-id="b3b69-142">Types</span></span>

<span data-ttu-id="b3b69-143">Mostra a contagem de instâncias e o tamanho total dos objetos na pilha, agrupados por tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="b3b69-143">Shows the instance count and total size of objects on the heap, grouped by object type.</span></span> <span data-ttu-id="b3b69-144">Por padrão, elas são classificadas por contagem de instâncias.</span><span class="sxs-lookup"><span data-stu-id="b3b69-144">By default, these are sorted by instance count.</span></span>

<span data-ttu-id="b3b69-145">Quando você seleciona um objeto no painel *tipos* superiores, a tabela [referências de objeto](#object-references) no painel inferior lista todos os objetos que apontam para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b3b69-145">When you select an object in the upper *Types* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

#### <span data-ttu-id="b3b69-146">Raízes</span><span class="sxs-lookup"><span data-stu-id="b3b69-146">Roots</span></span>

<span data-ttu-id="b3b69-147">Mostra uma exibição hierárquica de referências filho para descrever como os objetos são enraizada para o objeto global, evitando que eles sejam coletados como lixo.</span><span class="sxs-lookup"><span data-stu-id="b3b69-147">Shows a hierarchical view of child references to describe how objects are rooted to the global object, thus preventing them from being garbage-collected.</span></span>

<span data-ttu-id="b3b69-148">Por padrão, os nós filho são classificados pela coluna tamanho retido, com o maior na parte superior.</span><span class="sxs-lookup"><span data-stu-id="b3b69-148">By default, the child nodes are sorted by the retained size column, with the largest at the top.</span></span>

#### <span data-ttu-id="b3b69-149">Dominadores</span><span class="sxs-lookup"><span data-stu-id="b3b69-149">Dominators</span></span>

<span data-ttu-id="b3b69-150">Mostra uma lista de objetos no heap que têm referências exclusivas a outros objetos.</span><span class="sxs-lookup"><span data-stu-id="b3b69-150">Shows a list of objects on the heap that have exclusive references to other objects.</span></span> <span data-ttu-id="b3b69-151">Os dominadores são classificados pelo tamanho retido para indicar os objetos que estão consumindo a maioria das memórias que são mais fáceis de liberar.</span><span class="sxs-lookup"><span data-stu-id="b3b69-151">Dominators are sorted by retained size to indicate the objects consuming the most memory that are potentially easiest to free.</span></span>

<span data-ttu-id="b3b69-152">Veja como interpretar as colunas nos modos de exibição *tipos, raízes* e *dominadores* :</span><span class="sxs-lookup"><span data-stu-id="b3b69-152">Here's how to interpret the columns in the *Types, Roots* and *Dominators* views:</span></span>

<span data-ttu-id="b3b69-153">Coluna</span><span class="sxs-lookup"><span data-stu-id="b3b69-153">Column</span></span> | <span data-ttu-id="b3b69-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3b69-154">Description</span></span>
:------------ | :-------------
<span data-ttu-id="b3b69-155">Identificador (es)</span><span class="sxs-lookup"><span data-stu-id="b3b69-155">Identifier(s)</span></span> | <span data-ttu-id="b3b69-156">Nome que melhor identifica o objeto.</span><span class="sxs-lookup"><span data-stu-id="b3b69-156">Name that best identifies the object.</span></span> <span data-ttu-id="b3b69-157">Por exemplo, para elementos HTML, os detalhes do instantâneo mostram o valor do atributo ID, se um for usado.</span><span class="sxs-lookup"><span data-stu-id="b3b69-157">For example, for HTML elements the snapshot details show the ID attribute value, if one is used.</span></span>
<span data-ttu-id="b3b69-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3b69-158">Type</span></span> | <span data-ttu-id="b3b69-159">Tipo de objeto (por exemplo, *HTMLDivElement*).</span><span class="sxs-lookup"><span data-stu-id="b3b69-159">Object type (for example, *HTMLDivElement*).</span></span>
<span data-ttu-id="b3b69-160">Size</span><span class="sxs-lookup"><span data-stu-id="b3b69-160">Size</span></span> | <span data-ttu-id="b3b69-161">Tamanho do objeto, sem incluir o tamanho dos objetos referenciados.</span><span class="sxs-lookup"><span data-stu-id="b3b69-161">Object size, not including the size of any referenced objects.</span></span>
<span data-ttu-id="b3b69-162">Tamanho retido</span><span class="sxs-lookup"><span data-stu-id="b3b69-162">Retained size</span></span> | <span data-ttu-id="b3b69-163">Tamanho do objeto mais o tamanho de todos os objetos filho que não têm outros pais.</span><span class="sxs-lookup"><span data-stu-id="b3b69-163">Object size plus the size of all child objects that have no other parents.</span></span> <span data-ttu-id="b3b69-164">Para fins práticos, essa é a quantidade de memória retida pelo objeto, portanto, se você excluir o objeto, você recupera a quantidade especificada de memória.</span><span class="sxs-lookup"><span data-stu-id="b3b69-164">For practical purposes, this is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>
<span data-ttu-id="b3b69-165">Contagem</span><span class="sxs-lookup"><span data-stu-id="b3b69-165">Count</span></span> | <span data-ttu-id="b3b69-166">Número de instâncias do objeto.</span><span class="sxs-lookup"><span data-stu-id="b3b69-166">Number of object instances.</span></span> <span data-ttu-id="b3b69-167">Esse valor é exibido apenas no modo de exibição tipos.</span><span class="sxs-lookup"><span data-stu-id="b3b69-167">This value appears only in the Types view.</span></span>

<span data-ttu-id="b3b69-168">Quando você selecionar um objeto no painel superior *Dominars* , a tabela [referências do objeto](#object-references) no painel inferior listará todos os objetos que apontam para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b3b69-168">When you select an object in the upper *Dominators* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

### <span data-ttu-id="b3b69-169">Eles</span><span class="sxs-lookup"><span data-stu-id="b3b69-169">Filters</span></span>

<span data-ttu-id="b3b69-170">Você pode ajustar ainda mais os dados na tabela com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b3b69-170">You can further adjust data in the table with the following:</span></span>

![Filtrar por entradas internas e IDs de objetos](./media/memory_filter.png)

1. <span data-ttu-id="b3b69-172">**Filtro de identificador**: filtrar dados procurando por um identificador de objeto específico</span><span class="sxs-lookup"><span data-stu-id="b3b69-172">**Identifier filter**: Filter out data by searching for a particular object identifier</span></span>
2. <span data-ttu-id="b3b69-173">**Agrupar por Dominator**: somente objetos com referências *exclusivas* a outros objetos são mostrados na exibição de nível superior de objetos (esse é o modo de exibição padrão na guia *dodominars* ).</span><span class="sxs-lookup"><span data-stu-id="b3b69-173">**Group by dominator**: Only objects with *exclusive* references to other objects are shown in the top-level view of objects (this is the default view in the *Dominators* tab).</span></span>
3. <span data-ttu-id="b3b69-174">**Filtro de objetos internos/IDs**: por padrão, os [objetos internos JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) são incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="b3b69-174">**Built-ins / IDs filter**: By default, [JavaScript built-in objects](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) are included in the list.</span></span> <span data-ttu-id="b3b69-175">Listar IDs de objeto pode ser útil se houver vários objetos anônimos que precisam ser diferenciados.</span><span class="sxs-lookup"><span data-stu-id="b3b69-175">Listing object IDs can be useful if there are multiple anonymous objects which need to be differentiated.</span></span>

<span data-ttu-id="b3b69-176">Os modos de exibição de *tipos, raízes* e *dominadores* têm seu próprio filtro, portanto, o filtro não é preservado quando você alterna para outro modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="b3b69-176">The *Types, Roots* and *Dominators* views each has its own filter, so the filter isn't preserved when you switch to another view.</span></span>

### <span data-ttu-id="b3b69-177">Referências a objetos</span><span class="sxs-lookup"><span data-stu-id="b3b69-177">Object references</span></span>

<span data-ttu-id="b3b69-178">Nos modos de exibição [**tipos**](#types) e [**dominadores**](#dominators) , o painel inferior contém uma lista de **referências de objetos** que exibe referências compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="b3b69-178">In the [**Types**](#types) and [**Dominators**](#dominators) views, the lower pane contains an **Object references** list that displays shared references.</span></span> <span data-ttu-id="b3b69-179">Quando você escolhe um objeto no painel superior, essa lista exibe todos os objetos que apontam para esse objeto, em outras palavras, os objetos que mantêm o objeto selecionado em atividade.</span><span class="sxs-lookup"><span data-stu-id="b3b69-179">When you choose an object in the upper pane, this list displays all objects that point to that object--in other words, the objects that are keeping the selected object alive.</span></span>

<span data-ttu-id="b3b69-180">Referências circulares são mostradas com um asterisco (\*) e uma dica de ferramenta informativo e não podem ser expandidas.</span><span class="sxs-lookup"><span data-stu-id="b3b69-180">Circular references are shown with an asterisk (\*) and informational tooltip, and cannot be expanded.</span></span> <span data-ttu-id="b3b69-181">Caso contrário, ele impediria que você retorne a árvore de referência e identifique os objetos que estão retendo a memória.</span><span class="sxs-lookup"><span data-stu-id="b3b69-181">Otherwise, they would prevent you from walking up the reference tree and identifying objects that are retaining memory.</span></span>

<span data-ttu-id="b3b69-182">Para identificar rapidamente os objetos equivalentes, marque a opção de filtro [*IDs do objeto de exibição*](#filters) para exibir as IDs dos objetos ao lado dos nomes dos objetos na coluna *identificador (es)* .</span><span class="sxs-lookup"><span data-stu-id="b3b69-182">To quickly identify equivalent objects, tick the [*Display object IDs*](#filters) filter option to display object IDs next to object names in the *Identifier(s)* column.</span></span> <span data-ttu-id="b3b69-183">Objetos que têm a mesma ID são referências compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="b3b69-183">Objects that have the same ID are shared references.</span></span>

### <span data-ttu-id="b3b69-184">Comparação de instantâneos</span><span class="sxs-lookup"><span data-stu-id="b3b69-184">Snapshot comparison</span></span>

<span data-ttu-id="b3b69-185">Clicar em uma [Guia de comparação de instantâneo](#snapshot-details) ou em um link de comparação no [bloco Resumo do instantâneo](#snapshot-summary) mostrará uma comparação das informações entre os dois instantâneos.</span><span class="sxs-lookup"><span data-stu-id="b3b69-185">Clicking on a [snapshot comparison tab](#snapshot-details) or comparison link on the [snapshot summary tile](#snapshot-summary)  will show a diff of information between the two snapshots.</span></span> <span data-ttu-id="b3b69-186">No painel comparação, os modos de exibição *dominadores, tipos* e *raízes* fornecem os mesmos [*detalhes de instantâneos*](#snapshot-details) que você veria para um único instantâneos, com estes valores adicionais:</span><span class="sxs-lookup"><span data-stu-id="b3b69-186">In the comparison pane, the *Dominators, Types* and *Roots* views provide the same [*snapshot details*](#snapshot-details) you would see for a single snapshots, with these additional values:</span></span>

<span data-ttu-id="b3b69-187">Coluna</span><span class="sxs-lookup"><span data-stu-id="b3b69-187">Column</span></span> | <span data-ttu-id="b3b69-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3b69-188">Description</span></span>
:------------ | :-------------
<span data-ttu-id="b3b69-189">Diferenciar tamanho.</span><span class="sxs-lookup"><span data-stu-id="b3b69-189">Size diff.</span></span> | <span data-ttu-id="b3b69-190">Diferença entre o tamanho do objeto no instantâneo atual e seu tamanho no instantâneo anterior, sem incluir o tamanho dos objetos referenciados.</span><span class="sxs-lookup"><span data-stu-id="b3b69-190">Difference between the size of the object in the current snapshot and its size in the previous snapshot, not including the size of any referenced objects.</span></span>
<span data-ttu-id="b3b69-191">Diferenciar tamanho retido.</span><span class="sxs-lookup"><span data-stu-id="b3b69-191">Retained size diff.</span></span> | <span data-ttu-id="b3b69-192">Diferença entre o tamanho retido do objeto no instantâneo atual e o tamanho retido no instantâneo anterior.</span><span class="sxs-lookup"><span data-stu-id="b3b69-192">Difference between the retained size of the object in the current snapshot and its retained size in the previous snapshot.</span></span> <span data-ttu-id="b3b69-193">O tamanho retido inclui o tamanho do objeto mais o tamanho de todos os seus objetos filhos que não têm outros pais.</span><span class="sxs-lookup"><span data-stu-id="b3b69-193">The retained size includes the object size plus the size of all its child objects that have no other parents.</span></span> <span data-ttu-id="b3b69-194">Para fins práticos, o tamanho retido é a quantidade de memória mantida pelo objeto, portanto, se você excluir o objeto, você recupera a quantidade especificada de memória.</span><span class="sxs-lookup"><span data-stu-id="b3b69-194">For practical purposes, the retained size is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>

<span data-ttu-id="b3b69-195">Você pode usar o menu suspenso **Scope** para filtrar informações diferenciais entre instantâneos:</span><span class="sxs-lookup"><span data-stu-id="b3b69-195">You can use the **Scope** dropdown to filter differential info between snapshots:</span></span>

![Filtro de escopo para comparações de instantâneo](./media/memory_comparison_scope_filter.png)

- <strong><span data-ttu-id="b3b69-197">Objetos restantes do instantâneo # <number></strong> : mostra a comparação entre os objetos adicionados à pilha e removidos do heap do instantâneo da linha de base para o instantâneo anterior.</span><span class="sxs-lookup"><span data-stu-id="b3b69-197">Objects left over from Snapshot #<number></strong>: Shows the diff between the objects added to the heap and removed from the heap from the baseline snapshot to the previous snapshot.</span></span> <span data-ttu-id="b3b69-198">Por exemplo, se o resumo do instantâneo mostrar <em> + 205/-195 </em> na contagem de objetos, esse filtro mostrará os dez objetos que foram adicionados, mas não serão removidos.</span><span class="sxs-lookup"><span data-stu-id="b3b69-198">For example, if the snapshot summary shows <em>+205 / -195</em> in the object count, this filter will show you the ten objects that were added but not removed.</span></span>

- <strong><span data-ttu-id="b3b69-199">Objetos adicionados entre o instantâneo # <number> e # <number></strong> : mostra todos os objetos adicionados ao heap do instantâneo anterior.</span><span class="sxs-lookup"><span data-stu-id="b3b69-199">Objects added between Snapshot #<number> and #<number></strong>: Shows all objects added to the heap from the previous snapshot.</span></span>

- <strong><span data-ttu-id="b3b69-200">Todos os objetos no instantâneo # <number></strong> : mostra todos os objetos na pilha (em outras palavras, um <em> modo de exibição não filtrado </em> ).</span><span class="sxs-lookup"><span data-stu-id="b3b69-200">All objects in Snapshot #<number></strong>: Shows all objects on the heap (in other words, an <em>unfiltered</em> view).</span></span>

<span data-ttu-id="b3b69-201">Por padrão, o filtro *Mostrar referências sem correspondência* é aplicado ao modo de exibição de comparação para indicar referências a objetos que não correspondam ao filtro de escopo atual.</span><span class="sxs-lookup"><span data-stu-id="b3b69-201">By default, the *Show non-matching references* filter is applied to the comparison view to indicate object references that don't match the current Scope filter.</span></span> <span data-ttu-id="b3b69-202">Você pode desativá-lo do menu suspenso:</span><span class="sxs-lookup"><span data-stu-id="b3b69-202">You can turn it off from the dropdown menu:</span></span>

![Filtro de referências sem correspondência para comparações de instantâneo](./media/memory_comparison_matching_filter.png)


## <span data-ttu-id="b3b69-204">Teclado</span><span class="sxs-lookup"><span data-stu-id="b3b69-204">Shortcuts</span></span>

 <span data-ttu-id="b3b69-205">Ação</span><span class="sxs-lookup"><span data-stu-id="b3b69-205">Action</span></span> | <span data-ttu-id="b3b69-206">Atalho</span><span class="sxs-lookup"><span data-stu-id="b3b69-206">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="b3b69-207">Iniciar/parar sessão de criação de perfil</span><span class="sxs-lookup"><span data-stu-id="b3b69-207">Start / Stop profiling session</span></span>  | `Ctrl` + `E`
<span data-ttu-id="b3b69-208">Importar sessão de criação de perfil</span><span class="sxs-lookup"><span data-stu-id="b3b69-208">Import profiling session</span></span> | `Ctrl` + `O`
<span data-ttu-id="b3b69-209">Exportar sessão de criação de perfil</span><span class="sxs-lookup"><span data-stu-id="b3b69-209">Export profiling session</span></span> | `Ctrl` + `S`
<span data-ttu-id="b3b69-210">Criar instantâneo de heap</span><span class="sxs-lookup"><span data-stu-id="b3b69-210">Take heap snapshot</span></span> | `Ctrl` + `Shift` + `T`

## <span data-ttu-id="b3b69-211">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="b3b69-211">Known Issues</span></span>

### <span data-ttu-id="b3b69-212">Ocorreu um erro ao iniciar a sessão de criação de perfil</span><span class="sxs-lookup"><span data-stu-id="b3b69-212">An error occurred while starting the profiling session</span></span>

<span data-ttu-id="b3b69-213">Se você vir esta mensagem de erro: **ocorreu um erro ao iniciar a sessão de criação de perfil** na ferramenta de memória, siga estas etapas para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="b3b69-213">If you see this error message: **An error occurred while starting the profiling session** in the Memory tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="b3b69-214">Pressione `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="b3b69-214">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="b3b69-215">Na caixa de diálogo Executar, digite **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="b3b69-215">In the Run dialog, enter **services.msc**.</span></span>
![conhecidos-problemas-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="b3b69-217">Localize o **serviço coletor padrão do hub de diagnóstico da Microsoft (R)** e clique nele com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="b3b69-217">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![conhecidos-problemas-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="b3b69-219">Reinicie o **serviço coletor padrão do hub de diagnóstico do Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="b3b69-219">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![conhecidos-problemas-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="b3b69-221">Feche as ferramentas de desenvolvedor do Microsoft Edge e a guia. Abra uma nova guia, navegue até a página e pressione `F12` .</span><span class="sxs-lookup"><span data-stu-id="b3b69-221">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="b3b69-222">Agora você deve ser capaz de começar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="b3b69-222">You should now be able to begin profiling.</span></span> 
![conhecidos-problemas-4](./media/known_issues_4-memory.PNG)

<span data-ttu-id="b3b69-224">Ainda está com problemas?</span><span class="sxs-lookup"><span data-stu-id="b3b69-224">Still running into problems?</span></span> <span data-ttu-id="b3b69-225">Envie-nos seus comentários usando o ícone **enviar comentários** !</span><span class="sxs-lookup"><span data-stu-id="b3b69-225">Please send us your feedback using the **Send feedback** icon!</span></span> 

![conhecidos-problemas-5](./media/known_issues_5.PNG)
